# Bruker OPUS Reader

## Introduction
The brukeropusreader Python package enables reading the binary OPUS files generated by Bruker spectrometers.

## Installation
### Install with pip
```pip install brukeropusreader```

## Usage
`read_file` parses OPUS file and returns `OpusData` object:
```
from brukeropusreader import read_file

opus_data = read_file('opus_file.0')
```

`OpusData` is a dict consisting of all fields found in opus file:
```
print(f'Parsed fields: '
      f'{list(opus_data.keys())}')

print(f'Absorption spectrum: '
      f'{opus_data["AB"]}'
```

For full code see [example](example.py).

## Algorithm
Algorithm taken from
https://bitbucket.org/hirschbeutel/ono/src/default/ono/bruker_opus_filereader.py

Author: @twagner

## Contact
For developer issues, please start a ticket in Github. 
You can also write to the dev team directly at brukeropusreader-dev@qed.ai. 
For other issues, please write to: brukeropusreader@qed.ai

## License
Copyright (c) 2018 [Quantitative Engineering Design](https://qed.ai). All rights reserved.
This project is released under the terms of the AGPL license, which is included in LICENSE.txt.

--
QED | https://qed.ai
