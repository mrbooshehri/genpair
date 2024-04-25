# SSH Key Generator

This repository contains a Python script that automates the process of generating SSH keys for a list of users. It supports generating random passphrases for each key and allows specifying the key type.

## Features

- Generate SSH keys for multiple users.
- Supports RSA, DSA, ECDSA, and ED25519 key types.
- Optionally generate a random passphrase for each key.
- Store key information, including username, key name, passphrase, and public key fingerprint, in a user info file.

## Usage

1. **Prepare a list of users**: Create a text file with one username per line.

2. **Run the script**: Execute the script with the path to your user list file as an argument.

```bash
python ssh_key_generator.py -t rsa -p user_list.txt
```

- `-t` or `--key-type`: Specify the key type (default is `rsa`).
- `-p` or `--passphrase`: Generate a random passphrase for each key.
- `-e` or `--excel`: Export output to an Excel file.
- `user_list`: Path to the user list file.

## Example

```bash
./genpair -t ed25519 -p -e user_list.txt
```

This command will generate ED25519 keys with random passphrases for each
user listed in `user_list.txt` and `user_list.xlsx`.

## Output

The script will create SSH keys in the `output` directory and store key information in a file named `user_info`. The information includes the username, key name, passphrase (if generated), and public key fingerprint.

## Requirements

- Python 3.6 or higher
- `ssh-keygen` command available in the system's PATH

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
