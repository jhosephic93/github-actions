# Github-Actions

## Git Configuration

This repository includes a brief overview of Git configuration files and how they adjust its behavior.

### Configuration Files:

1. **/etc/gitconfig**  
   - Affects all users and repositories on the system.
   - Command: `git config --system`.

2. **~/.gitconfig or ~/.config/git/config**  
   - User-specific configuration.
   - Command: `git config --global`.

3. **.git/config (in the repository)**  
   - Applies only to the current repository.

Each file contains settings that Git uses to determine its behavior. You can read or modify these files depending on the level where you want the changes to apply.

### Identity Configuration:

Setting up your identity is crucial for committing changes in Git. You can configure your name and email with the following commands:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

If you want to set your identity only for a specific repository (without applying it globally), you should run the following commands at the same level of the repository (without the --global flag):

```bash
git config user.name "Your Name"
git config user.email "your.email@example.com"
```