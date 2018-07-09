# DataStore
This is a class which uses the directory and file structure of a filesystem to store and manipulate information. It does so using unique indentifiers for folder names and .dat files to hold the content of fields.

# Hostry Timeline for DataStore
DataStore is the evolution of a class called Entity from (https://webpi.chris-shaw.com) Entity was a raw class to standardise how the WebPi software would interact with data stored within the filesystem

- Started Life as Entity.php in WebPi (https://webpi.chris-shaw.com)
- Became a general way for WebPi to access data and becoming basis for an authentication class.
- Was moved to its own repository with unit tests to be shared between progects
- Renamed to DataStore and Added to packagest for composer install

# Usage

## Creating

    $payload = [
           'id_entity' => 'testId',
           'test' => 'case'
    ];
              
    $dataStore = new DataStore('exampleID');
    $dataStore>create($payload);

## Read
              
    $dataStore = new DataStore('exampleID');
    $dataStore>getValue('fieldname');

## Updating

    $dataStore = new DataStore('exampleID');
    $dataStore>getValue('field', 'value');

## Deleting
    
    $dataStore = new DataStore('exampleID');
    $dataStore>delete();
    
## Searching

    $filters = [
        ['field','=','value'],
        ['field','>','value']
    ];
    
    $search = new DataStore();
    $results = $search->search();

# How to Install

## 1. Composer
The preferred method is using composer (https://getcomposer.org/) and can be insalled using the following command

    composer require christopher-paul-shaw/datastore 

## 2. Cloning
You can also clone the repository from github

    git clone git@github.com:christopher-paul-shaw/DataStore.git
