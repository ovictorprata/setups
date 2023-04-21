# Setup Git

`apt-get install git`

## Setting your username in Git

- Set a Git username:

`git config --global user.name "XXXXXX"`

- Confirm that you have set the Git username correctly:

`git config --global user.name
> XXXXXX`

## Setting your commit email address

### Setting your email address for every repository on your computer

`git config --global user.email "XXXXXX"`

- Confirm that you have set the email address correctly in Git:

```
git config --global user.email
> email@example.com 
```


## Generating a new SSH key and adding it to the ssh-agent
- Paste the text below, substituting in your GitHub email address.
`ssh-keygen -t ed25519 -C "XXXXXX"`

### Adding your SSH key to the ssh-agent
Before adding a new SSH key to the ssh-agent to manage your keys, you should have checked for existing SSH keys and generated a new SSH key.

- Start the ssh-agent in the background:

`eval "$(ssh-agent -s)"`
`> Agent pid 59566`

Add your SSH private key to the ssh-agent. If you created your key with a different name, or if you are adding an existing key that has a different name, replace id_ed25519 in the command with the name of your private key file.

`ssh-add ~/.ssh/id_ed25519`

## Adding a new SSH key to your GitHub account

Copy the SSH public key to your clipboard.

```cat ~/.ssh/id_ed25519.pub
# Then select and copy the contents of the id_ed25519.pub file
# displayed in the terminal to your clipboard
```

Then follow these steps [here](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)