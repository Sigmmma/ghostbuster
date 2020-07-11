# ghostbuster

[Phantom BSP][1] is a collision artifact which sometimes appears in Halo BSP tags compiled by the HEK's tool.exe. Ghostbuster is a command-line tool which detects and fixes these artifacts in-place by modifying the tag's node structure.

## Installation
You will need Python 3 to use this tool. Clone this repository, or simply download `ghostbuster.py` and `requirements.txt` somewhere convenient. Install dependencies with `pip install --user -r requirements.txt`.

## Usage
Ghostbuster modifies BSP tags in-place unless the `-dryrun` flag is added, so it is recommended to first backup the tag if it cannot be recompiled easily. From a command line:

```sh
python3 ghostbuster.py <path to BSP tag>
```

Due to rounding errors and the nature of how phantom BSP are detected, the script may report and "fix" a number of false positives. This does not appear to be detrimental to the map.

[1]: https://c20.reclaimers.net/h1/tags/scenario_structure_bsp/#phantom-bsp
