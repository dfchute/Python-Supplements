# Python-Supplements
Scripts to help reformat files from the electronic medical record
#reformat notes
# Read in the file
with open('dfc17_011218111842227799_Vis.txt', 'r') as file :
  filedata = file.read()

# Replace the target string
filedata = filedata.replace('\n', '')

# Write the file out again
with open('notes.txt', 'w') as file:
  file.write(filedata)
  
# Read in the file
with open('notes.txt', 'r') as file :
  filedata = file.read()

# Replace the target string
filedata = filedata.replace('[report_end]', '\n')

# Write the file out again
with open('notes2.txt', 'w') as file:
  file.write(filedata)
