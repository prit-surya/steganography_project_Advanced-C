Steganography - LSB Image Encoding Project

What is Steganography?
Steganography is the practice of concealing a file, message, image, or video within another file, message, image, or video. It is a useful technique in digital communication for securing sensitive information.

Why Use Steganography?
To hide secret credentials.
To detect data forgery.
For secure message passing.

Where is Steganography Used?
Military and Intelligence Agencies: For covert communication and data hiding.
Online Elections: Securing votes and voter information.
Internet Banking: Protection of sensitive financial data.
Medical Imaging: Safeguarding patient data embedded within medical images.
And many more industries that require secure information exchange.
How Does Steganography Work?
Steganography can be implemented in two broad methods:

Physical Steganography:

Prints and paints.
Puzzles.
Digital Steganography:

Conceals information within digital files like images, videos, or audio.
The current project focuses on Least Significant Bit (LSB) Steganography, where the secret message is embedded within the least significant bits of a .bmp image file.
Project Overview
This project implements LSB (Least Significant Bit) Image Steganography using the BMP image format. BMP images are ideal due to their simple structure and uncompressed nature, which allows for easy manipulation of pixel data.

The project allows encoding and decoding of secret messages without noticeable degradation in image quality. The encoded secret message is stored in a new file called output_secret.txt.

Understanding the Terminology
Image & Pixel
An image consists of a fixed number of rows and columns of pixels.
Each pixel represents the brightness or intensity of a specific color.
In RGB (Red, Green, Blue) format, each pixel is defined by the intensities of these three color components.
By altering the Least Significant Bit (LSB) of each pixel's color intensity, the secret message is embedded.
Image Format - BMP
BMP (Bitmap) is an image file format used primarily in Microsoft Windows OS.
It is uncompressed, making it large in size but ideal for lossless steganography.
The BMP format is widely accepted for steganography because of its simple structure and pixel-wise accessibility.
Features
Message Encoding: Hide a secret message inside a BMP image using LSB encoding.
Message Decoding: Retrieve the hidden message from an encoded BMP image.
Output: The secret message is saved into a file called default.txt after decoding.
Directory Structure
graphql
Copy code
Steganography_Project/
│
├── encode.c                    # Encoding logic
├── decode.c                    # Decoding logic
├── test_encode.c               # Main program for encoding/decoding
├── types.h                     # Data types and enum definitions
├── default.txt           # File where the decoded secret message will be stored
├── secret.txt                  # File containing the secret message to be encoded
├── sample.bmp                  # Sample BMP image for encoding
└── README.md                   # Project Documentation
Requirements/Dependencies
C Compiler (gcc or similar)
A BMP image file (uncompressed) for encoding
Secret message in a text file (e.g., secret.txt)
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/your-repo/steganography_project.git
Navigate to the project directory:

bash
Copy code
cd steganography_project
Compile the code:

bash
Copy code
gcc test_encode.c encode.c decode.c -o stego
Usage Instructions
Encoding
To encode a secret message into an image, use the following command:

bash
Copy code
./stego -e <input_bmp_image> <secret_message_file> <output_encoded_image>
Example:

bash
Copy code
./stego -e sample.bmp secret.txt stego.bmp
This will encode the message in secret.txt into sample.bmp and save the output as stego.bmp.

Decoding
To decode a hidden message from an image, use the following command:

bash
Copy code
./stego -d <encoded_image> <output_secret_file>
Example:

bash
Copy code
./stego -d stego.bmp output_secret.txt
This will decode the hidden message from stego.bmp and save it into output_secret.txt.

Examples
Encoding Example
bash
Copy code
./stego -e sample.bmp secret.txt stego.bmp
This command encodes the message from secret.txt into sample.bmp and generates stego.bmp as the output.

Decoding Example
bash
Copy code
./stego -d stego.bmp output_secret.txt
This command decodes the hidden message from stego.bmp and stores it in output_secret.txt.

Contributing
Feel free to contribute to this project by opening issues, suggesting new features, or submitting pull requests.

License
This project is open-source under the MIT License.

Author: Pritesh Suryawanshi
Project Date: 20th June 2024
Guidance: Created under the guidance of Emertxe as part of the ECEP course.

You can copy this text, adjust the GitHub URL, and upload it to your repository’s README section! Let me know if you'd like any more customization.






