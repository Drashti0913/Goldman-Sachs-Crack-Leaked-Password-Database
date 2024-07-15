# Goldman-Sachs Password Security Assessment

## Overview
As a governance analyst, it is part of your duties to assess the level of protection offered by implemented controls and minimize the probability of a successful breach. This project aims to identify vulnerabilities in the password security mechanisms and propose enhancements to increase the overall level of security in an organization.

## Project Objectives
- **Hashing Algorithm Used**: Identify the type of hashing algorithm used to protect passwords.
- **Protection Level**: Evaluate the level of protection offered by the current password hashing mechanism.
- **Improvement Controls**: Suggest controls to make cracking passwords much harder in case of a database leak.
- **Password Policy Analysis**: Assess the organization’s password policy (e.g., password length, key space).
- **Policy Recommendations**: Propose changes to the password policy to enhance security.

## Observations
- The organization uses an outdated password hashing algorithm (MD5) which offers very little protection in the event of a password database leaking.
- Current password policy allows users to have short passwords (6 characters) and reuse usernames as part of passwords.

## Recommendations
1. **Use Stronger Hashing Algorithms**:
   - Switch to dedicated password hashing algorithms such as bcrypt, scrypt, or PBKDF2 to greatly increase the time needed to crack individual passwords.
   
2. **Implement Salting**:
   - Use salting to prevent the use of rainbow tables to speed up password cracking.

3. **Increase Minimum Password Length**:
   - Increase the minimum password length requirement to 10 characters to increase the computational effort required to crack passwords and provide additional time to change all passwords if the database is leaked.

4. **Avoid Easy-to-Guess Passwords**:
   - Prevent passwords from being the same as usernames or reused as part of the password.

5. **Educate Users on Password Creation**:
   - Train users to create safe and easy-to-remember passwords. Recommend using passphrases combining random words and including special characters and numbers.

6. **Promote the Use of Password Managers**:
   - Educate users on the benefits of password managers, allowing for the creation of very long and random passwords without the need to remember them.

## Detailed Report
### Security Algorithms Used:
- MD5: All passwords in the sample were protected using MD5, a weaker hash algorithm prone to collisions and easy to crack with tools like Hashcat and rockyou.txt wordlist.

### Cracked Passwords:
- Below are the cracked passwords identified during the analysis:
  - `experthead:e10adc3949ba59abbe56e057f20f883e` - 123456
  - `interestec:25f9e794323b453885f5181f1b624d0b` - 123456789
  - `ortspoon:d8578edf8458ce06fbc5bb76a58c5ca4` - qwerty
  - `reallychel:5f4dcc3b5aa765d61d8327deb882cf99` - password
  - `simmson56:96e79218965eb72c92a549dd5a330112` - 111111
  - `bookma:25d55ad283aa400af464c76d713c07ad` - 12345678
  - `popularkiya7:e99a18c428cb38d5f260853678922e03` - abc123
  - `eatingcake1994:fcea920f7412b5da7be0cf42b8c93759` - 1234567
  - `heroanhart:7c6a180b36896a0a8c02787eeafb0e4c` - password1
  - `edi_tesla89:6c569aabbf7775ef8fc570e228c16b98` - password!
  - `liveltekah:3f230640b78d7e71ac5514e57935eb69` - qazxsw
  - `blikimore:917eb5e9d6d6bca820922a0c6f7cc28b` - Pa$$word1
  - `johnwick007:f6a0cb102c62879d397b12b62c092c06` - bluered

## Conclusion
The current password hashing mechanism and policy at Goldman-Sachs are inadequate and pose significant security risks. Implementing the recommended changes will enhance the overall security posture and reduce the likelihood of successful password cracking attacks.

---

**Author**: Drashti Bhavsar 
**Qualification**: B.Tech Computer Science and Engineering
