import os

# Get the current working directory
cwd = os.getcwd()

# Initialize an empty list to store the file information
file_list = []

# Iterate over the files in the current working directory
for filename in os.listdir(cwd):
    file_path = os.path.join(cwd, filename)
    
    # Check if the file is a regular file (not a directory)
    if os.path.isfile(file_path):
        # Get the size of the file in bytes
        file_size = os.path.getsize(file_path)
        
        # Create a dictionary to store the file information
        file_info = {
            "path": filename,
            "size": file_size
        }         
        # Add the file information to the list
        file_list.append(file_info)

# Print the list of dictionaries
