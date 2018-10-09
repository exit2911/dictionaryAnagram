
#change working directory

import os
os.chdir('/Users/vyho/Downloads/english-words-master') #change working directory

filename = 'words_alpha.txt' #specifying the file to be loaded
        
def init_words(fname): # read text file and save the words in a dictionary
    words = {} #initialize an empty library named word
    with open(fname) as f: #close file once leave code block
            for line in f: 
               word = line.strip() #grab each word in each line and strip nothing from the line
               words[word] = 1 #save each word in words dictionary and assign key 1 to all
               
                    
    return words
                    

word_dict = init_words(filename)
            

def init_anagram_dict(words): 
    """ sort every word in the dictionary alphabetically and append the sorted word to the original word's 
    dictionary as a key 
    """

    anagram_dict = {} #set an empty library
    for word in words:
        sorted_word = ''.join(sorted(list(word)))
        if sorted_word not in anagram_dict:
            anagram_dict[sorted_word] = []
    
        anagram_dict[sorted_word].append(word)
    return anagram_dict


    
        
def find_anagrams(word,anagram_dict): 
    """
    take a word input that is sorted alphabetically as a query key against the anagram 
    dictionary (with sorted words as keys and their anagrams) and return the elements in the sets. an empty 
    set is returned if there are no anagrams

    """

                
    key = ''.join(sorted(list(word)))
    if key in anagram_dict:
        return set(anagram_dict[key]).difference(set([word])) #return the set of anagram(s) and take off the word the user enter from the set
    return set([])            
    
    


a = input('enter the word :') #ask users to enter a word




print(find_anagrams(a,anagram_dict)) #output all anagrams if any

