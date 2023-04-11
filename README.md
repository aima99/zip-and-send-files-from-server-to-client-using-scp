# zip-and-send-files-from-server-to-client-using-scp

#!/bin/bash
# copy.sh

source_file="/path/to/source/file.txt"

destination_file="/path/to/destination/file.zip"

zip -r "$destination_file" "$source_file"

client_username="client_username"
client_hostname="client_hostname"
client_destination_path="/path/to/destination/"

scp "$destination_file" "${client_username}@${client_hostname}:${client_destination_path}"


#after writting this script

#make it executable with "chmod +x copy.sh"
