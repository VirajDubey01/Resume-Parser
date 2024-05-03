# importing required classes 
from pypdf import PdfReader 

# creating a pdf reader object 
reader = PdfReader('C:/Users/viraj/OneDrive/Desktop/Buisness analyst resume/Viraj_Dubey_Resume.pdf') 

# printing number of pages in pdf file 
print(len(reader.pages)) 

# creating a page object 
page = reader.pages[0] 

# extracting text from page 
print(page.extract_text()) 


# EXTRACT NAME FROM A RESUME
from pypdf import PdfReader 

# Function to extract name from text
def extract_name(text):
    # Implement your logic here to extract the name
    # This could involve using regular expressions, string manipulation, or other methods
    # For example, if the name is at the beginning of the text, you could split the text by whitespace and return the first word
    name = text.split()[0]
    return name

# creating a pdf reader object 
reader = PdfReader('C:/Users/viraj/OneDrive/Desktop/Buisness analyst resume/Viraj_Dubey_Resume.pdf') 

# creating a page object 
page = reader.pages[0] 

# extracting text from page 
text = page.extract_text()

# Extract name from the text
name = extract_name(text)
print("Name:", name)
