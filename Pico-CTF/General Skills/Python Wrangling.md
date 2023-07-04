# Obedient Cat


**Points:** 10

**Description:** Python scripts are invoked kind of like programs in the Terminal... Can you run this Python script using this password to get the flag?

## Solution 


### Initial Analysis

I downloded the Python script, the password, and the flag files.


### Step 1: 
I used the **cat** command to read the Python file and understand its functionality. The code provided allows for file encryption and decryption using the Fernet symmetric encryption algorithm. 
I discovered that using the -e option encrypts a file, while the -d option decrypts it. 

In the script, I noticed this line

```python
$ python " + sys.argv[0] + " -d pole.txt'\n
```
Based on the provided information, I replaced the placeholder values with the actual command.

```python
python ende.py -d flag.txt.en
```

Then I entred the provided password. 


Flag 
`picoCTF{4p0110_1n_7h3_h0us3_dbd1bea4}`