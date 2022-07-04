## Install Python 3.x.x Version

This example will show steps to install python 3.7.9, replace it with your required version.

1. First, update the packages list and install the packages necessary to build Python source

    ```sh
    sudo apt update
    sudo apt install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libsqlite3-dev libreadline-dev libffi-dev wget libbz2-dev
    ```
    
2. Download the latest release’s source code from the [Python download page](https://www.python.org/downloads/source/) using the following [wget](https://linuxize.com/post/wget-command-examples/) command:
    
    ```sh
    wget https://www.python.org/ftp/python/3.7.9/Python-3.7.9.tgz
    ```

3. Once the download is complete, [extract the gzipped tarball](https://linuxize.com/post/wget-command-examples/)

    ```sh
    tar -xf Python-3.7.9.tgz
    ```

4. Next, [navigate](https://linuxize.com/post/linux-cd-command/) to the Python source directory and run the configure script which will perform a number of checks to make sure all of the dependencies on your system are present

    ```sh
    cd Python-3.7.9
    ./configure --enable-optimizations
    ```
   The --enable-optimizations option will optimize the Python binary by running multiple tests. This makes the build process slower.

5. Start the Python build process using make

    ```sh
    make -j 8
    ```
   For faster build time, modify the -j flag according to your processor. If you do not know the number of cores in your processor, you can find it by typing nproc. The system used in this guide has 8 cores, so we are using the -j8 flag.
    
6. When the build is done, install the Python binaries by running the following command

    ```sh
    sudo make altinstall
    ```

7. That’s it. Python 3.7 has been installed and ready to be used. Verify it by typing

    ```sh
    python3.7 --version
    ```
    The output will show the Python version
    ```
    Python 3.7.9
    ```
