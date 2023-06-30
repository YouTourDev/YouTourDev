# Hey There! 👋

Over the years we've developed a few custom scripts, programs and tools for our workflow automation.
They all live here! Each repository here will have detailed installation instructions but most will require cloning or installing the repos here themselves.

# List of In-House Tools
Here's a brief list of the tools and what they do:

## Davinci Resolve
- [Bookie](https://github.com/youtourdev/bookie) - automatic YouTour point (segments) exporting
- [Feet](https://github.com/youtourdev/feet) - advanced keyboard macros for YouTour flythrough editing (Windows only)
- [KMFeet](https://github.com/youtourdev/kmfeet) - advanced keyboard macros for YouTour flythrough editing (Mac Only)
- [Proxima](https://github.com/youtourdev/proxima) - local, distributed proxy-transcoding (legacy)
- [Snapper](https://github.com/youtourdev/snapper) - auto-incrementing timeline snapshots
- [Squawk](https://github.com/youtourdev/squawk) - automatic, round-tripped subtitles

## Premiere
- [Smooth as Butta](https://github.com/YouTourDev/smoothasbutta) - keyboard macros and extra tools for YouTour flythrough editing (Windows only, legacy)


A python package like [Snapper](https://github.com/youtourdev/snapper) can be installed like so: 
```
pipx install git+https://github.com/youtourdev/snapper
```

If the repository is private because it contains sensitive company IP, you will need to authenticate your computer to GitHub before installing.

# Authentication

## GitHub Account
You will need access to the YouTourDev Github account.
The login details are available in the `post@youtour.com.au` LastPass Vault under `devs@youtour.com.au`.
If you require the LastPass password for `post@youtour.com.au`, contact Daniel Bunker.

## Manual
> **Note**
>
> If you're familiar with SSH, this is pretty easy (and it's OOTB cross platform), but
> if you're not and don't want to be, use the GitHub CLI method. It's a couple of extra things to install and steps to take, but it 'll hold your hand along the way.

1. If you don't already have an SSH key, [generate one](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
2. Follow [this guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) to add the SSH key to your GitHub account

## GitHub CLI
1. Login and navigate to the [SSH keys settings](https://github.com/settings/keys)
2. Install the [GitHub CLI](https://cli.github.com) app (install with [Brew](https://brew.sh) on Mac, or [Scoop](https://scoop.sh) on PC)
3. Open "Terminal" on Mac or "Windows Terminal"/"Powershell" on PC and enter the following commands:
4. Run `gh auth logout` if already logged in
5. Run `gh auth login` and follow the prompts
6. Select 'Github.com'
7. Select 'SSH'
8. Select an existing public key if you have one, otherwise generate a new one
9. Name the key after your computer
10. Select 'Login with a web browser and copy the key
11. Paste the key into the GitHub Device Activation box
12. Confirm the authentication and enter your password when prompted
13. Check the terminal output confirms authentication

You should see something like this:

```
bash-3.2$ gh auth login
? What account do you want to log into? GitHub.com
? What is your preferred protocol for Git operations? SSH
? Generate a new SSH key to add to your GitHub account? Yes
? Enter a passphrase for your new SSH key (Optional) 
? Title for your SSH key: Caleb's Mac
? How would you like to authenticate GitHub CLI? Login with a web browser

! First copy your one-time code: E167-98A8
Press Enter to open github.com in your browser...
```

![image](https://github.com/YouTourDev/YouTourDev/assets/92896767/1456f9f2-99bf-450d-a99a-aacced7bff41)

```
✓ Authentication complete.
- gh config set -h github.com git_protocol ssh
✓ Configured git protocol
✓ Uploaded the SSH key to your GitHub account: /Users/danielbunker/.ssh/id_ed25519.pub
✓ Logged in as YouTourDev
```

Now you have read and write access to all private GitHub repositories under YouTourDev.
You can directly install Python applications like this:
```
pipx install git+https://github.com/youtourdev/bookie
```


   
