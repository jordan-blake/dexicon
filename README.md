# dexicon
The highspeed rest api for Lexicon Data

    Query word-data over HTTP
    words, definitions,synonyms, antonyms, hypernyms, hyponyms, holonyms, meronyms, derivations, and more.
    
Based on the Wordnet Lexicon, this module was created to allow fast querying of English word-data across multiple applications.

Dexicon Api uses LokiJS, plus a consolidated version of Wordnet Lexicon.

To install the module:

    $npm install dexicon 

To run the module: (navigate to the folder where dexicon is installed)

    $npm run dexicon 


Usage Examples:

    1. Get all definitions, with deep relational data for a set of english words (using jquery,ajax)
            
            $.getJSON('localhost:8383/dexicon/deep?words="rainbow,fractal,lizard"', function(data){
            
                  console.log(data); //Object containing all word data for the response
            
            });
            

    2. Get only the minimum data for a set of words
    
             $.getJSON('localhost:8383/dexicon/basic?words="rainbow,fractal,lizard"', function(data){
            
                  console.log(data); //Object containing minimum word data for the response (lemma, defintions, synonyms, antonyms) 
            
            });
            
            
   3. Get data specific to a sense of existing word data (from a previous search) 
    
             $.getJSON('localhost:8383/dexicon/basic?synsets=#synset_1,#synset_2,#synset_3', function(data){
            
                  console.log(data); //Object containing data by synsets (words by specific definitions)
            
            });
    



  
