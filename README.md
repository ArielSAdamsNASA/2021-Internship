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
