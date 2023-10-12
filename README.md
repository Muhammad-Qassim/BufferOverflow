# Buffer Overflow Exploit

## Instructions

This README provides step-by-step instructions on how to run the buffer overflow exploit.

### Prerequisites

Before you begin, make sure you have the following prerequisites in place:

1. A virtual machine with Redhat 9 installed.
2. All the necessary files within the virtual machine, including `getscore.c`, `score.txt`, and `exploit.py`.

### Running the Exploit

To run the exploit:

1. Log in to the virtual machine as a privileged user (e.g., root).

2. Create a guest user account:

   ```
   useradd guest
   ```
3. Set the necessary permissions on the `getscore` program and `score.txt` :
   ```
   chmod 755 getscore
   ```
   ```
   chmod u+s getscore
   ```
   ```
   chmod 600 score.txt
   ```
4. Switch to the guest user:
   ```
   su guest
   ```
5. Run the provided Python exploit script (`exploit.py`) :
   ```
   python exploit.py
   ```

### Output

The exploit code enables a transition from the guest user to the root user, marking the successful execution of our buffer overflow attack, resulting in gaining root access.

1. To confirm that our exploit works:
   ```
   whoami
   ```
   If it gives root, it means our exploit works and now guest user have root privilege.

### Common Error

If you encounter the "failed to open source file" error, switch to the root user and adjust permissions again. 
















   
