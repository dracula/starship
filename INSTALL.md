### [Starship](https://starship.rs)

#### Install manually

Download using the [GitHub .zip download](https://github.com/dracula/starship/archive/master.zip) option and unzip them.

#### Activating theme

Copy the starship.toml from the unzipped download to `~/.config/starship.toml`

#### Installing using Nix home-manager

If you're a [Nix Home Manager](https://github.com/nix-community/home-manager) user add the following to your home-manager config .nix

This setup was tested using zsh, change line 3 below if you're using a shell other than zsh.

```nix
programs.starship = {
  enable = true;
  enableZshIntegration = true;
  settings = {
    cmd_duration.style = "bold #f1fa8c";
    directory.style = "bold #50fa7b";
    hostname.style = "bold #ff5555";
    git_branch.style = "bold #ff79c6";
    git_status.style = "bold #ff5555";
    username = {
      format = "[$user]($style) on ";
      style_user = "bold #bd93f9";
    };
    character = {
      success_symbol = "[λ](bold #f8f8f2)";
      error_symbol = "[λ](bold #ff5555)";
    };
  };
};
```
