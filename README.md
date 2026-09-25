# Password cracking with John The Ripper(JtR) and Networkwalks Tools (Hash Calculator and Password cracker) 
# Introduction
This report covers password cracking of three (3) locked PDF files, using multiple password cracking tools. This report includes the process of getting the hashes of these locked PDF files and successfully gaining access by cracking their passwods with a password cracker tool. All activities were run on Windows PC and web browser. 
I have properly documented below every step I took, including the exact tools used, the process and the results achieved. 
I have also stated the issues I encountered and how I solved the problem. I also took several screenshots of the activities as evidence.


# Tools Used
The table below lists each tool used in this report and its purpose.
| Tools | Purpose |
| :---- | :---- |
| John The Ripper(JtR) | An offline open-source password-cracking tool that recovers passwords from <br> hashes |
| 

# Activities Performed

# Offline Password Recovery via John the Ripper (JtR) (WK3 PM1)
# Objective: 
Extract and crack the cryptographic hash of a password-protected PDF document using an offline, signature-based recovery method.

STEP 1 - Environment Setup: Downloaded John the Ripper (JtR) along with the Johnny Graphical User Interface (GUI) from the official repository. Installed the packages and configured the necessary path dependencies.

STEP 2 - Hash Extraction: Launched the PDF Hash Extractor utility, uploaded the target encrypted PDF file, and isolated its cryptographic hash.

STEP 3 - Data Staging: Copied the generated hash string into a text document and saved it locally for ingestion.

STEP 4 - Attack Execution: Opened the Johnny GUI, selected "Open Password File," and imported the target hash. Initiated a signature-based recovery attack ("Start New Attack").

STEP 5 - Verification: Upon successful recovery of the plaintext password, the credentials were used to decrypt and open the PDF file.

# Browser-Based Password Recovery via Networkwalks Tools (WK3 PM2)
# Objective: 
Perform web-based cryptographic hash extraction and cloud-assisted password recovery on a secured PDF file.

STEP 1 - Target Ingestion: Downloaded the encrypted PDF file and navigated to the online Networkwalks Hash Calculator via a secure web browser.

STEP 2 - Hash Generation: Uploaded the locked PDF document to the platform to parse the file structure and calculate the corresponding hash value.

STEP 3 - Cryptanalysis: Copied the complete hash string and transitioned to the Networkwalks Password Cracker web application. Pasted the cryptographic hash into the parsing interface and executed the cracking routine.

STEP 4 - Verification: The cloud utility successfully recovered the plaintext passphrase. The retrieved credentials were then entered into the locked PDF document to successfully grant authenticated access.

# ISSUES I ENCOUNTERED AND STEPS I TOOK TO REMEDY IT

Exception Handling: The initial recovery attempt using the web-based Networkwalks Password Cracker failed to yield the plaintext password, indicating the passphrase was outside the tool's default keyspace.

Wordlist Sourcing: I downloaded a series of comprehensive, specialized wordlists (dictionaries) to expand the attack parameters.

Sequential Execution: I ran the cryptographic hash against each downloaded wordlist file sequentially.

Resolution & Verification: The plaintext password was successfully recovered after cycling through the targeted dictionaries. The retrieved credentials were then applied to the locked PDF document to successfully grant authenticated access.



