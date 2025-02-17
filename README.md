# Files and a tool for Finnish hyphenation and spelling in Affinity Publisher v2

This repository contains 3 files needed in Affinity Publisher for hyphenation and spell-checking of the Finnish language on **Windows** computers. These files have been forked from https://www.apt-browse.org/browse/debian/wheezy/main/all/myspell-fi/0.7-18/file/usr/share/hunspell. At the moment, the original hunspell dictionary contains some repeating and unsorted word blocks. These have been removed in this repository. **Mac** users may need hyphenation dictionary because the automatic hyphenation language does not work as expected.

## Files to get started with Finnish spelling and hyphenation

The `fi_FI.aff` file contains basic information how Finnish words are constructed. In the beginning, there is an instruction to set a correct character set. Original affix file uses **ISO8859-1** encoding. According to tests, I have been able to conduct that its works well with Finnish Windows 10. Further testing will be made with different operating systems and language versions in the future. Latest macOS versions have builtin support for Finnish language and there is no need for an additional spelling dictionary. But automatic hyphenation needs a dictionary. Only hyphenation dictionary `hyph_fi_FI.dic` is needed. Do not install other Hunspell dictionaries to your Mac. Instructions can be found on Wiki pages. There may be other sources of these files with **UTF8** encoding. In those files, the character setting on 1st row must be `SET ISO8859-1` to make spelling and hyphenation function properly. Wrong character encoding settings may add duplicate suggestions or display strange characters. The following screen shot shows correct suggestions when using dictionaries downloaded from this repository:

![image](https://user-images.githubusercontent.com/24242044/205984577-ac7ab74b-f8fe-4bb8-8969-bd34ba0f276a.png)

## Tool to update the spelling dictionary
There is a tool for updating Finish spelling dictionary. You cand add new words, import words from **Joukahainen** dictionary and maintain your dictionary with the **Spelling Maintenance Tool**. Insturctions to use the tool are found on Wiki pages or tool's Help menu. Language in the tool is Finnish only assuming that users publishing in Finnish can understand it.

![image](https://user-images.githubusercontent.com/24242044/211196521-dfa23b39-4b66-4697-8dc1-55c82eb888fc.png)

New words can be typed to _Lisättävä sana_ field (1). By hitting the enter key the word will be added to a list of words _Sanaluettelo_ (2). By pressing buttons (3) words will be saved to the spelling dictionary. _Tallenna valitut_ will save sellected words from the list and _Tallenna kaiki_ will save all words in the list. By double clicking a word in the list will remove it from the list(2) and put it back to input field (1). Word can be deleted with keys or by pressing the x symbol in the field.

## About dictionary files

The `fi_FI.dic` file is a collection of Finnish words. There is a word counter at the beginning of the file. Affinity Publisher does not maintain this file. If you teach new words to Publisher, they are stored outside of this file. You can add words to this file with the Spelling Maintenance Tool. Spelling tool in Affinity publisher can suggest some words to be inserted. Suggestions are based on a affix file `fi_FI.aff`. Due to the limitations in hunspell's algorithms it does not work very well with Finnish language. This is the reason why user must add words all the time to spelling dictionary or to Affinity Publishers custom dictionary. Saddly Publisher reads the spelling dictionary at the startup. When words are added to the spelling dictionary you musta restart Publisher in order to recognise those words.

The `hyph_fi_FI.dic` file contains instructions how to split words for hyphenation. There is also a character set definition on the 1st row. To hyphenate correctly this file must be installed to a certain folder in your system.

## Installing files 
You can download dictionary files by clicking the green Code button on the top right-hand corner. Unzip the contents to Affinity's Dictionaries folder. In **Windows** you can find this location in Affinity Publisher, through `Edit - Preferences - Tools`. 

![image](https://user-images.githubusercontent.com/24242044/205483402-095cd467-d668-45f7-826c-2dee38fca26b.png)

Open the folder by clicking `Open` then copy the unzipped dictonary files to this folder. In **Windows** copy `fi_FI.aff`, `fi_FI.dic` and `hyph_fi_FI.dic`. If you are using **Mac** computer copy only `hyph_fi_FI.dic`. 

In **Mac** computers (as macOS Ventura 13.1) put the hyphention file into folder `fi-Fi`. You must create this forlder first. For the correct path see the following picture:

<img width="377" alt="image" src="https://user-images.githubusercontent.com/24242044/211194689-19258797-d408-4af3-9aef-ec9312fe4b82.png">


## Tools for updating and cleaning the spelling dictionary
The structure of `fi_FI.dic` is very simple: On the 1st row there is a word counter, and the rest contain words in an alphabetical order, one word per row. The purpose of this repository is to provide simple tools for adding, sorting, and removing duplicates from the spelling dictionary. With appropriate tools, the dictionary can be maintained and expanded to meet our requirements. All tools can be used from a single GUI. You can add words to the speling dictonary, maintain integrity of the dictionary and import words from **Joukahainen** dictionary. It is a xml based dictionary used in **Voikko** spell checker. It contains thousands of words not found in the original **hunspell** dictionary. It can be found and downloaded from https://joukahainen.puimula.org/. 
