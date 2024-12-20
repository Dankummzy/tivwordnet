# TivWordNet

**TivWordNet** is a semantic network for the Tiv language, modeled after WordNet. It provides functionality to manage synsets, retrieve hypernyms and hyponyms, and work with definitions and lemmas. The package uses SQLite database for data storage and supports basic operations for lexical semantic processing.

## Features

- **Word Definitions**: Store and retrieve meanings for various Tiv words.
- **Hypernym Relationships**: Define relationships between words to create a semantic hierarchy.
- **Data Population**: Populate the database with predefined word and hypernym data.

## Installation

To install TivWordNet, you can use `pip`:

```bash
pip install tivwordnet

Usage

Importing the Package
First, import the TivWordNet class from the package:

if __name__ == "__main__":
    word_data = [
        (1, "kwagh", "A domesticated carnivorous mammal."),  # dog
        (2, "kwer", "A small domesticated carnivorous mammal with soft fur."),  # cat
        (3, "vhe", "A thing used for transporting people or goods."),  # vehicle
        (4, "nenev", "A warm-blooded vertebrate animal characterized by the presence of hair or fur."),  # mammal
        (5, "anih", "A living organism that feeds on organic matter."),  # animal
        (6, "kikoo", "A warm-blooded vertebrate distinguished by the possession of feathers."),  # bird
        (7, "fishi", "A limbless cold-blooded vertebrate animal with gills and fins."),  # fish
        (8, "kpai", "A cold-blooded vertebrate of a class that includes snakes and lizards."),  # reptile
        (9, "anpigh", "A cold-blooded vertebrate animal that is born in water and breathes with gills."),  # amphibian
        (10, "we", "A small air-breathing arthropod with six legs."),  # insect
        (11, "fa", "Movable articles that are used to make a room or building suitable for living or working."),  # furniture
        # Add more words as needed
    ]

    hypernym_data = [
        (1, 4),
        (2, 4),
        (4, 5),
        (6, 5),
        (7, 5),
        # Add more hypernym relationships as needed
    ]

    with TivWordnetConnector() as connector:
        tiv_wordnet = TivWordnet(connector)

        # Populate the database with data
        tiv_wordnet.populate_data(word_data, hypernym_data)

        # Retrieve synsets
        synsets = connector.get_synsets()
        for synset in synsets:
            print(synset)

        # Retrieve hypernyms
        hypernyms = connector.get_hypernyms()
        for hypernym in hypernyms:
            print(hypernym)

License
TivWordNet is distributed under the MIT License. See LICENSE for more information.

Support
For questions or issues, please open an issue on GitHub or contact support at danterkum16@gmail.com.

Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your changes.

Acknowledgements
This project is inspired by [jamsic/ru-wordnet](https://github.com/jamsic/ru-wordnet/).


### Explanation

1. **Installation**: Instructions for installing the package with `pip`.
2. **Usage**: Detailed examples of how to use the package to add synsets, retrieve synsets, and get hypernyms and hyponyms.
3. **Data Files**: Information on the data files used by the package.
4. **License**: Details about the license under which the package is distributed.
5. **Support**: Information on how to get help or report issues.
6. **Contributing**: Guidelines for contributing to the project.
7. **Acknowledgements**: Credits for inspiration and sources.
