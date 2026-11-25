# Interface Design Cards

Brainstorming-cards related to **Interface Design**.

- arrange & think & discuss!
- read between the cards!

[`interfacedesigncards.csongorb.com`](http://interfacedesigncards.csongorb.com)

## Structure

This repository holds **content only**. Everything that displays the cards comes from [cardsimulator](https://github.com/csongorb/cardsimulator), included as a git submodule (pinned to a commit).

- `cards/cardset.xml`: title, repository and public address (used by the QR codes in PDFs)
- `cards/cardCategories.xml`, `cards/cards.xml`: the cards
- `texts/`: documents linked from the cards
- `index.html`: tiny loader, identical in every card set
- `.github/workflows/deploy.yml`: publishes the site to GitHub Pages on every push to `main`
- `.github/workflows/update-cardsimulator.yml`: manual run (workflow_dispatch) that bumps the `cardsimulator` submodule to the newest commit on `main` and pushes the pointer to `main`
- `cardsimulator/`: the simulator (submodule)

Run locally with any static web server (the XML can't be loaded from `file://`).

Update the simulator: run the *Update cardsimulator submodule* workflow on GitHub Actions, or locally with the help of your Git client.

## Version-History

### Release 1.1 (Work in Progress)

Structure:

- matches cardsimulator v0.5
- restructured the main architecture, separated into
	- cardsimulator
	- interfacedesigncards (that includes cardsimulator as submodule)
- this repository is now content only
	- card visualisation comes from `cardsimulator`
	- tiny loader `index.html`
	- GitHub Pages deploy workflow

Content:

- some links updated
- category "examples" renamed to "case studies"
- new color palette for the categories
- new case studies: Clair Obscur: Expedition 33, Outer Wilds
- book links point to the book's Wikipedia article (or its Goodreads page when there is none) instead of Amazon

### Release 1.0 (26. March 2021)

- first release
- created for Porn Creator 0.3
- primarily made to support a course at the UE
	- incl. all the links and topics I had already prepared for previous UI classes

## Credits

- **Csongor Baranyai**  
	- csongorb (at) gmail (dot) com  
	- [csongorb.com](http://www.csongorb.com)

Thanks to all the **universities / schools / institutions** where I had the opportunity to teach courses, supervise students and projects, and refine the idea of the brainstorming cards. And of course a huge thank you to all the **students** who have contributed with all their comments and critiques... and who have tolerated my experiments.

Additional design / content / coding:

- **Haneyeh Sam**
	- [haniyehsam.itch.io](https://haniyehsam.itch.io/)
- **Christoph Maureder**
	- [christophmaureder.me](https://christophmaureder.me/)

## License

[![Creative Commons License](https://i.creativecommons.org/l/by-nc/4.0/88x31.png)](http://creativecommons.org/licenses/by-nc/4.0/)
This work is licensed under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0/).

All other media (images, software, etc.) remain the property of their copyright holders.
