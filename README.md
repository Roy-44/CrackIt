# Crack It
Crack It is a multithreaded application that illustrates a password hacking using brute force technique.
One thread generates a randomized plain password, encrypts it using a randomized key and “sends” the encrypted buffer to X decrypter threads, the decrypter threads compete to decrypt the encrypted password by trying to guess the key.

Instructions:
-------------
1. run "sudo apt install libssl-dev" command.

2. run "sudo dpkg --install mta-utils-dev.deb" command.

3. run "make" command.

4. run the program using the following command "sudo ./main.out -l <passwordLen> -n <decryptersNumber> -t <timeout>"
   * -n|--num-of-decrypters – will determine how many decrypter threads will be created.
   * -l|--password-length – number of characters that will be encrypted, the more characters will be encrypted the harder it will be for the decrypters. Must be a multiplication of 8.
   * -t|--timeout(optional) – time is seconds until server regenerates a password if it didn’t.

5. You can use the command "make clean" to clean the compilation outputs.
