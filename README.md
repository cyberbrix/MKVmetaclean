# MKVmetaclean

# cleans metadata from MKV files. Also prints when files have multiple audio or video language files
# Only cleans first audio and first video file track titles
# removes all attachments





#After cloning the repository, perform the following, if needed

#cd mediainfoclean/

#chmod a+x mediainfoclean.sh

#Account running should have permission to edit all the MKV files touched



# This script search MKV files for rogue metadata, like video/audio track file titles,
# tags such as XML tags, attachments (images, fonts, random files)
# It will also identify when more than 1 audio or video (rare) track are found
# You can list the results, which will output in CSV format
#
# Usage:
#  ./mediainfoclean.sh  -p=\"/path/to/dir/\" [--clean]
#
#   Arguments:
#   -p path  to directory. without a value, will use current directory
#   
#   --clean  optional. Script will go through and clean the following fields:
#   Tags, attachments, general title, date,segment info, previous/next filenames, uids,
#   track names for the first audio and video file
#   See https://matroska.org/technical/specs/index.html for info
#   Results will be posted after commands complete
#"
#   Files with only A/V extra tracks will not be cleaned
#   These are fields where I found misc data tucked in there by various authors. This could change.
#    
#   .mediainfoclean.ini  is created in \$HOME of the account running the script

