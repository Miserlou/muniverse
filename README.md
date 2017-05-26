# μniverse

μniverse is my attempt to wrap a bunch of HTML5 games in a single API. This is similar to [openai/universe](https://github.com/openai/universe), except that it avoids Flash and VNC.

This is a work in progress. See [Roadmap](#roadmap) for more details.

# Advantages over Universe

Compared to OpenAI Universe, μniverse will give the following advantages:

 * No need to play games in real-time.
   * No "falling behind" on slower computers
   * Play games faster than real-time on fast machines.
 * No need for a neural network to read scores from screenshots.
 * Fewer [glitches](https://github.com/openai/universe/issues/187) due to menu automation.
 * No Docker containers without accompanying source code
   * All code to generate containers will be included
   * Scripts to download & package games

Most of the above advantages come from focusing on HTML5 games rather than Flash games.

# Contents

 * **this directory** - high-level Go API for controlling environments
 * [chrome/](chrome) - Go API for controlling a headless Chrome instance
 * [games/](games) - scripts for downloading & packaging games
 * [container/](container) - build files for the Docker container
 * [codegen/](codegen) - small program to auto-generate Go games registry

# Roadmap

Here's what is done so far:

 * Go API for interfacing with headless Chrome.
 * Mechanism for downloading & packaging games.
 * JavaScript interface for controlling time (timers, Date, etc.)
 * Docker container for running headless Chrome.
 * Go API for controlling Docker containers.

Here's a (non-exhaustive) to-do list:

 * Simple interface for gym-like environment control.
 * Get more games.
