STEGANOGRAPHY - LSB Image Encoding Project

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




Contributing
Feel free to contribute to this project by opening issues, suggesting new features, or submitting pull requests.



Author: Pritesh Suryawanshi

Project Date: 20th June 2024

Guidance: Created under the guidance of Emertxe as part of the ECEP course.












HOW to Run Project On Linux Ubuntu :-

compile the project :- gcc test_encode.c encode.c decode.c -o a.out

enter secret message in secret.txt

to encode :- ./a.out -e beautiful.bmp secret.txt

to decode :- ./a.out -d stego.bmp

to see decoded output :- cat defaultFile.txt









