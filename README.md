# BLiR
Biomarker Literature Retrieval; a supervised machine learning approach to assist with the Text Mining task of Information Retrieval.

## Dependencies

- Python 3.6
- requirements.txt: run `pip install -r requirements.txt`


## Preparing the Data
In order for the program to work, you need to provide:
1. BibTeX file(s) or text file(s) with PMIDs;
2. A text file with the PMIDs of the relevant articles.
3. Create folders for Data_Collection, Data_preprocessing and Machine_Learning.
4. Data_Collection collection has Raw_data and Processed_data subfolders

#### BibTeX file:
If you have a `.bib` file, place it in the [Raw_data](Data_Collection/Raw_data) folder.

#### Text file with PMIDs:
If you have a `.txt` file with PMIDs, place it in the [Processed_data](Data_Collection/Processed_data) folder.

#### Text file with the relevant PMIDs:
Place your `.txt` file with the PMIDs of the relevant articles in the [Data_Preprocessing](Data_Preprocessing) folder.

See the sample files provided and match your files to that format. After placing them in the apropriate location, go to the `variables.py` script (NOTE, there are three of them, one in each folder) and change the variables to match the name of your files without .bib or .txt, just the file name. 

## Individual file names                                             ######
FILE_1 = 'sample_file_1'     # Do not write sample_file_1.bib        ######
FILE_2 = 'sample_file_2'

## Data Collection
If you have a `.bib` file, run the first option in the `get_pmids_titles_abst_meta.py` script in order to get all the files in the [Processed_data](Data_Collection/Processed_data) folder.

If you have a `.txt` file with PMIDs, run the second option in the `get_pmids_titles_abst_meta.py` script in order to get the remaining three files in the [Processed_data](Data_Collection/Processed_data) folder.

NOTE: You need to uncomment the appropriate lines depending on if you have a .bib or .txt file in the Raw_data folder that you want to use.

## Data Preprocessing
Run `get_ML_data.py` in the [Data_Preprocessing](Data_Preprocessing/) folder to get all the data you need to train the models from the [ML_data](Data_Preprocessing/ML_data) folder.

## Train the models
In the [Machine_Learning](Machine_Learning) folder, choose the script with the algorithm you want to run: `DecisionTree.py`, `LogRegression.py`, `NaiveBayes.py`, `NeuralNetwork.py`, `RandomForest.py` or `SupportVectorMachine.py`. Inside each script there are further instructions and options, select the ones are more suitable for you.
