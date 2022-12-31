# OCR-on-Hotel-website-for-webscrapping

The code was basically designed to extract phone number and email address from https://www.hotelcontact.net/

On this site more than one million worldwide hotel data is present but some of the data is in the form of images. Thus the goal of this project was not only to scrape data from this website but also to scrape the phone numbers and email addresses of worldwise hotels using OCR.

**The steps were following in order to achieve the results:**

1. Find all the hotels in any country using recursion - as the website uses hierarichal structure to save the data of any hotel in any specific location. 
2. Extract images consisting of hotel phone number and email on run-time (for reducing space complexity as the code has to extract millions of hotel data).
3. Analyzing images before pre-processing them
4. Pre-process iamges using Digital Image Processing techniques i.e.:

    - Conversion of 3D image to 2D iamge by converting image to grayscale
    - Adding extra boundary pixels on the top of the images 
    
        1. The analysis process showed that here was no space between the alphanumeric characters of phone and email 
        2. Direct application of any further image pre-processing technique was rendering the iamge and generating false positive results
        
    - image binarization
5. Application of OCR on pre-processed image using pytesseract

**Suggestions to improve the code processing speed are most welcome. Anyone can clone this and participate to make it better. But do give a credit if you are using the code publically. :)**
