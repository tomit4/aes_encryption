## Encryption/Decryption Of An Image

This repository contains essential code demonstrating the encrypting and
decrypting of a simple .jpg file using AES (Advanced Encryption
Standard). Using the packages, [pycryptdome](https://pypi.org/project/pycryptodome/) as well as the [Pillow](https://pypi.org/project/pillow/), the files, `encrypt.py` as well as `decrypt.py` are utilized to encrypt and decrypt a sample `original.jpg` file for demonstration purposes.

This demo was copied from [this article on pyseek](https://pyseek.com/2024/05/how-to-encrypt-an-image-in-python-using-aes-algorithm/).

### Requirements

You will need [python3](https://www.python.org/downloads/) as well as [pip](https://pip.pypa.io/en/stable/installation/) installed. Additionally, in order to download this repository, you'll also need [git](https://pip.pypa.io/en/stable/installation/) installed. Lastly, you'll also need python's [virtualenv](https://virtualenv.pypa.io/en/latest/installation.html) installed.

### Installation

First simply clone this repository:

```sh
git clone https://github.com/tomit4/aes_encryption
```

You'll then want to activate python's virtual environment by invoking the
following commands:

```sh
python3 -m virtualenv aes_encryption && \
source aes_encryption/bin/activate && \
cd aes_encryption
```

This will set up your python virtual environment so that you don't install the
python packages globally on your system. Next let's install the dependencies. I
have provided a basic requirements.txt file that allows you to install the
dependencies simply with one command:

```sh
pip install -r requirements.txt
```

### Usage

The usage of this project is very simple as it is solely a demo. To encrypt our
image, simply invoke the `encrypt.py` file from the command line like so:

```sh
python encrypt.py
```

You'll notice within your file system an `original.jpg.iv` file as well as an
`encrypted_image.jpg`. To learn more about the `original.jpg.iv` file, refer to
[the article](https://pyseek.com/2024/05/how-to-encrypt-an-image-in-python-using-aes-algorithm/)
as well as [this wiki](https://en.wikipedia.org/wiki/Initialization_vector) on the subject.

To ensure the `encrypted_image.jpg` file is indeed encrypted, use an image
viewing application (or even just your browser) to attempt to open the file. It
should <em>not</em> be viewable. Now simply decrypt the file using the
`decrypt.py` script like so:

```sh
python decrypt.py
```

This should create a `decrypted_image.jpg` file within your directory. Test it
by opening it in an image viewer application, this <em>should</em> be visible.

Once done, you can simply exit your virtual environment like so:

```sh
deactivate
```

### Learn More

- [Wikipedia on Initialization Vector](https://en.wikipedia.org/wiki/Initialization_vector)
- [Wikipedia on SHA-2](https://en.wikipedia.org/w/index.php?title=SHA-2)
- [Wikipedia on HMAC](https://en.wikipedia.org/wiki/HMAC)
- [Wikipedia on AES](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard)
