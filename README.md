
**Overview**

Welcome to the Image Similarity Finder, a Streamlit web application designed to help you upload any image and display 5 similar images. This application utilizes a pre-trained ResNet50 model and cosine similarity to identify images with similar content. I have used Google Colab and Local Tunnel for model training, embeddings generation and running the web-application.

![WhatsApp Image 2024-02-04 at 7 05 16 PM](https://github.com/AaqibbHasanie/Clothes-Similarity-App/assets/103883753/bcc24d85-cccc-4ddc-8a8b-b382caf9a2b2)


**Project Structure**

The project is organized into the following components:
**Dataset**: The dataset is sourced from a CSV file named Data ID - Sheet1.csv. Each entry includes a unique product ID and a corresponding image link.
**Data Preparation**: The dataset is read and images are downloaded using the provided URLs. The downloaded images are stored in the final image dataset directory.
**Embedding Generation**: The ResNet50 model is employed to generate embeddings for each image. The embeddings are computed and saved in a file named embeddings.pkl.
**Web Application**: The Streamlit web application will be created in the app.py file after running the entire provided code. Users can upload an image, and the application will find and display visually similar images from the dataset based on cosine similarity.

**How to Use**

Follow the below steps to run this project:
1. Clone the repository
2. Upload the file named clothes_similarity.ipynb to Google Colab.
3. Upload the dataset named Data ID.xlsx to your Google Drive.
4. Run the code present in clothes_similarity.ipynb after changing the relevant paths corresponding to your dataset location.
5. After app.py has been created and Resnet50 model has been trained, run the following command:

**!streamlit run app.py & npx localtunnel --port 8501**

From the resulting cell, click on the url given in **"Your url is = "**. Once you open this url, it will ask you for an Endpoint ID. For this purpose
copy the **External URL** given and extract the part: 35.192.125.67 from the entire External URL, **http://35.192.125.67:8501**. Hit enter and you will be able to seee
the image running.


**Important Files**
**Dataset**: Data ID - Sheet1.csv
**Embeddings File**: embeddings.pkl - It will contain the computed image embeddings for faster similarity calculations.**
**Model and Similarity Metric**
**Deep Learning Model:** The ResNet50 model pre-trained on ImageNet is used to extract features from images.

**Similarity Metric**: Cosine similarity is employed to measure the similarity between image embeddings. 


Feel free to explore and adapt the code to suit your specific needs or integrate it into your own projects. If you have any questions or issues, please don't hesitate to reach out.

Happy exploring!
