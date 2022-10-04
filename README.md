# Docker Image Files for Python 4 DS

To build image:

- run `zip -r zipped_image.zip * .hidden` from this directory.
  - Note the dockerfile must be at root of zipped package, so don't zip the whole repo *folder* as package.
- In Lab Manager, create a new image. Select "Custom Image".
- Upload zipped file `zipped_image.zip`.
- **SELECT HTML PORT 8080 in Coursera window!!!**
- Click Apply.

## To add Python packages

- Add conda installable packages to the list around line 273
- At packages they can only be installed with pip in the line immediately below the conda installation (currently 274).