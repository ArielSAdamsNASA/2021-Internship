# 2021-Internship

# Daily Notes

# 8/9/21

- Worked om getting cFS to run on my VM
- Read more into cppcheck, specifically was looking into the output code scanning results. Still working on running it locally. Still not sure about the artifacts on the cFS github and how they work.


See new comment on cppcheck issue: https://github.com/ArielSAdamsNASA/2021-Internship/issues/1

# 8/10/21

- Got the cppcheck errors sorted out. After doing research into cppcheck, I found out that its designed to be very hard to trigger a false positive error, so because of that, it will not generate errors often unless it is certain. This is why most all the artifacts on the NASA/cFS repo are empty.
- I was looking into finding a way to display the errors in a better way than zipped artifacts. Was thinking of writing a workflow that read the artifact as an unzipped .md file so it can be easier to read.
- still getting errors in running cFS despite cloning all the folders. Attached is the error. Seems to still be missing something.[cFS build error.txt](https://github.com/ArielSAdamsNASA/2021-Internship/files/6964504/cFS.build.error.txt)

# 8/11/21
- researched more about GitHub actions and workflows. 
- working on an improved cppcheck workflow

# 8/12/21
- Today I spent most of the day getting cFS to work. I found out that the Academy's IT Security Department was blocking the submodule updates. When I manually cloned the files it was not getting everything. I ended up using my hotspot and after a couple tried it all ended up working. Once I got cFS to work, I started going through the training manual. My understanding of cFS is definitely much better.
- I got a bit stuck with writing the COBRA github action workflow so I started researching into Coverity. I created an account and have been looking and finding a way to get it to work with github.
- With the cppcheck I tried to find a way to remove the empty archive files but I am still struggling with understanding the code. I think it might be easier to keep the current code as having more information printed is probably better.

# 8/16/21
- The only way seems to be using a MISRA.py file which is open source made by the people who make cppcheck (https://github.com/danmar/cppcheck/blob/main/addons/misra.py). Below is the usage of the python script. In order to use it you need a ton of other addon files which are also on the github. Once you get them all them to call the MISRA check you run the python script and add the file you want to check. The code will only return the error number/rule that was violated (i.e. c2012-21.3]). To get readable error messages, you need to pass in a text file with the text of the rules (there are some example formats on the github). The problem is that the rules are not open source and would need to be purchased. I spent a lot of time looking for version of the rules file  online but couldn't find it. (https://www.misra.org.uk/). I tried testing it out on my VM and below is the log which I got. I'm not 100% sure that it ended up running. This is where I am, I'm going to keep working on trying to write the shell code to run it in the action, but let me know if you think there's an easier way for me to do this.  
- https://github.com/0xsninja/Test/commit/56485847deeae10945032ad58524a6aa9c8c22cd
