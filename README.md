# Nixboard
Desktop app to organize Nix profiles, flakes, any Nix files - basically something like Docker Desktop for Nix

This is a hobby project (i.e. it will be lucky to survive 2 weeks of development and continue living).

## Tech used
Probably gonna be Iced GUI framework of Rust. It'll compile to a fast file, not gonna have to think about null pointers and
apparently it uses Elm-like functional approach, so exceptions should be minimal. We'll see what more comes bundled.

## Plan

(These are going off of my current ideas of what I'd like it to do and might not be quite realistic.)

(Funky prefix means only if I feel like it.)

- Works on Linux GNOME at least
- Filetree-like or list-like (or some funky flake-like) view of Nix flakes on a machine
  - Files can be viewed
    - With syntax higlighting
  - Files can be edited
  - Files can be moved (with or without the rest of the directory)
  - If a shell is present in flake definition, a GUI element lets the user start it
    - So having something like a devshell would spawn a new terminal window
- Nix profiles and envs similarly organized like Nix flakes above
  - Nix people will kill me, but I haven't used these two in any real capacity, so this will
    probably change a bit once I know more about them.
- Statistics of currently executed shells
  - FHS, normally (by Nix standards) spawned shells
  - Have statistics like used storage, running time, purpose, tags and whatever comes to mind
    - Probably can expand to non-executing shells as well, depends on how well Nix store will play
      with this app
  - Probably gonna steal some of Docker Desktop's ideas
  - Maybe snoop on stuff not spawned by this app too (definitely as an option setting if it will exist)
- Create new Nix files that will be watched as well.
- Custom file groups to watch
- Dark mode toggle (funky: custom theming)
- User and dev documentation
- Funky: Nix file visualiser (like Scratch or some component tree, could be cute)
- Funky: Funky animations (could be fun)
- Funky: Good user and dev documentation
- Funky: Dry changes explanation (might use some home-trained AI for this? this would be some super-voluntary
  addon though).
- Funky: addons and plugins
  - If Kernelshark taught me anything, it's that plugins are lovely, but limited feature.
  - In theory this program could be generalized, but then it would kinda just be a file manager.
- Funky: flake searcher
  - I don't download flakes, but a fast searching app could make me change my mind.
- Funky: Flake-to-normal-Nix converter
  - Out of scope, not part of problem domain, could be fun though.
- Funky: Normal-nix-to-flake converter
  - Out of scope, not part of problem domain, could be fun though.

## Author's note

I decided to start on this on a whim, so don't go thinking I'll be doing this fulltime, I just want an app for my Nix messes.

One could be less lazy and keep things better organized, but sometimes you just gotta fix what's already there y'know?
