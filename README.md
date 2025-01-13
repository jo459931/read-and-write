# File Read & Write Challenge: Read and write to a new file

def read_and_write_file(input_filename, output_filename):
    try:
        # Open the input file in read mode
        with open(input_filename, 'r') as infile:
            content = infile.read()

        # Modify the content (for example, changing all letters to uppercase)
        modified_content = content.upper()

        # Write the modified content to the output file
        with open(output_filename, 'w') as outfile:
            outfile.write(modified_content)

        print(f"File has been successfully modified and saved to {output_filename}")

    except FileNotFoundError:
        print(f"Error: The file {input_filename} does not exist.")
    except IOError:
        print("Error: There was an issue reading or writing the file.")

# Test the function
input_file = 'input.txt'  # Replace with your file name
output_file = 'output.txt'  # Replace with your desired output file name
read_and_write_file(input_file, output_file)
