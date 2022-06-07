# CircleCI YAML configuration file parser
CLI tool that accepts a file path to a CircleCI YAML configuration file and outputs a list of images used in it.

---
__Requirements:__  

* Read input a file path from Stdin
  * without quotes
  * with quotes
  * with spaces
* Support CircleCI configuration file
  * Version
    * v2.1 - Cloud, Server 3
    * v2.0 - Server 2
  * File formats - YAML, YML
* Output a list of images from the configuration file to Stdout
  * Sorted by `<image name>:<version TAG>`
    * `<image name>`
      * ascending alphabetical order
    * `<version TAG>`
      * descending sort
      * `current` and `latest` on top
      * `numeric` above
  * Every image from a new line
* Log errors return to Stderr when
  * file path is not provided
  * file path is not found
  * image in file is not found
