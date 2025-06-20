Instructions to make this project.
1. Try to develop this project in some clound enviroment for smooth execution in less time because the dataset and google pretrained - model used is of very big in size nearly(600MB and 1.6GB) making execution tough for your local machine. {You can use google colab for this}
   
2. To load the dataset run the following,
     Code Snippet - 1:
         import kagglehub
         # Download latest version
         path = kagglehub.dataset_download("bharadwaj6/kindle-reviews")
         print("Path to dataset files:", path)
         import pandas as pd
         import os
         file_name = 'kindle_reviews.csv'
         full_file_path = os.path.join(path, file_name)
         df = pd.read_csv(full_file_path)
         df.head()
   Code Snippet - 1 Output:
         ![image](https://github.com/user-attachments/assets/5be1c28e-d0e6-4b71-91b3-84e909d2d9e4)

3. To load the "Google new-300 Word2Vec model" (deep learning model created by google to convert text into numeric format i.e. int/float(called vectors) run the following,
     Code Snippet - 2:
         pip install gensim (if you are installing form command promt/pwoershell)
         !pip install gensim (if you are installing from the notebook enviroment)
     Code Snippet - 2 output:
           requirement already satisfied (if you already downloaded)
                      OR
           some message will telling downloaing has been completed.

     Code Snippet - 3:
         import gensim.downloader as api
         model = api.load("word2vec-google-news-300")
      Code Snippet - 3 output:
         ![image](https://github.com/user-attachments/assets/35c44a2d-b4ca-4648-864a-c9b39522c3ed)

         
