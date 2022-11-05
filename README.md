# dockerHomework

Prerequisite
Install Docker Desktop and python

STEPS

1. Create a docker file
   create a new file with no extension name it as Dockerfile.
2. Edit Docker File
   Edit the docker file with text editor and add these lines

   Your Dockerfile should look like this:

   FROM python:3
   ADD my_script.py /
   RUN pip install pystrich
   CMD [ "python", "./my_script.py" ]

3. Create my_script.py and add this
   my_script.py looks like the following:

   from pystrich.datamatrix import DataMatrixEncoder

   encoder = DataMatrixEncoder('This is a DataMatrix.')
   encoder.save('./datamatrix_test.png')
   print(encoder.get_ascii())

4. Build Image
   Open terminal and cd into your approriate directory and run this command

   docker build -t python-barcode .

5. Run Your Image

   docker run python-barcode
