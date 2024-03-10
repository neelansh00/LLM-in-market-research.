# LLM-in-market-research.
Stock data can be overwhelming for beginners entering the stock market. This LLM app based on the skeleton of dropbox retrieval app by pathway aims to use RAG(retrieval augmented generation) to put forward relevant data from the stock sheets provided according to the query of the user.

## How to use 
User can ask questions such as :- 
1. "List the companies that gained in stock price on [specific date] along with their previous close, current price, and percentage change."
2. "List the top 5 gainer companies with highest % change in their stock price on a specific date."

    <img width="304" alt="Screenshot 2024-03-10 204856" src="https://github.com/neelansh00/LLM-in-market-research./assets/146512226/e671c35e-7b18-4503-8725-e6b45750268c">

## End User
Primary end users of the RAG-enabled LLM app for stock price data would include Novice Investors , Students and Educators, Small Investors, Financial Advisors, Entrepreneurs and Startups, General Public.

## Industry Impact
The LLM market research app for stock price data has significant industry impact by democratizing access to financial insights for beginners. By seamlessly retrieving and generating relevant data based on user queries, it empowers novice investors to make informed decisions, fostering financial literacy and participation. This democratization can potentially level the playing field in financial markets, enabling broader participation and facilitating more informed investment strategies, thus contributing to the democratization of finance.

## Business Value
The LLM market research app for stock price data holds immense business value by offering a competitive edge in the fintech sector. By providing intuitive access to comprehensive financial insights for beginners, it attracts a wider user base and enhances customer engagement. This translates to increased user retention, expanded market reach, and potential revenue growth through premium features or subscription models. Moreover, by leveraging advanced AI technologies for data retrieval and generation, the app can optimize operational efficiency, reduce costs, and stay ahead in an increasingly data-driven financial landscape.

## Utilization of the LLM App
NutriGPT utilizes the LLM (Large Language Model) App features provided by Pathway to build a real-time data pipeline.
The LLM App enables natural language processing capabilities, allowing users to ask questions in plain language and receive relevant nutrition insights.
NutriGPT leverages the LLM's ability to process and analyze text data to extract meaningful information from various sources, including its connection to an SQL database.
It specifically uses NFHS5 (National Family Health Survey 5) data to produce its results, ensuring that users have access to the most up-to-date and reliable information regarding nutrition in India.
This direct connection to the database enhances NutriGPT's capabilities, as it can access and analyze data that already resides in multiple applications and databases, providing users with comprehensive insights about nutrition data and trends. This streamlining of data retrieval and analysis significantly improves the efficiency and effectiveness of the application.

# How to run the tool
Example only supports Unix-like systems (such as Linux, macOS, BSD). If you are a Windows user, we highly recommend leveraging Windows Subsystem for Linux (WSL) or Dockerize the app to run as a container.

## Prerequisites
1. Make sure that Python 3.10 or above installed on your machine.
2. Download and Install Pip to manage project packages.
3. Create an OpenAI account and generate a new API Key: To access the OpenAI API, you will need to create an API Key. You can do this by logging into the OpenAI website and navigating to the API Key management page.
4. choose your own dropbox account

Then, follow the easy steps to install and get started using the sample app.

# Step 1: Clone the repository
This is done with the git clone command followed by the URL of the repository:
```
git clone https://github.com/neelansh00/LLM-in-market-research..git
```
Next, navigate to the project folder:
```
cd LLM-in-market-research.
```
# Step 2: Set environment variables
Create `.env` file in the root directory of the project, copy and paste the below config, and replace the `{OPENAI_API_KEY}` configuration value with your key.
```
OPENAI_API_TOKEN={OPENAI_API_KEY}
HOST=0.0.0.0
PORT=8080
EMBEDDER_LOCATOR=text-embedding-ada-002
EMBEDDING_DIMENSION=1536
MODEL_LOCATOR=gpt-3.5-turbo
MAX_TOKENS=200
TEMPERATURE=0.0
DROPBOX_LOCAL_FOLDER_PATH="../../../mnt/c/Users/bumur/Dropbox/documents"
```
Replace DROPBOX_LOCAL_FOLDER_PATH with your local Dropbox folder path and optionally, you customize other values.

# Step 3 (Optional): Create a new virtual environment
Create a new virtual environment in the same folder and activate that environment:
```
python -m venv pw-env && source pw-env/bin/activate
```
# Step 4 Install the app dependencies
Install the required packages:
```
pip install --upgrade -r requirements.txt
```
# Step 5: Run and start to use it
You start the application by navigating to llm_app folder and running main.py:
```python
python main.py
```
When the application runs successfully, you should see output something like this:

# Step 6: Run Streamlit UI for file upload
You can run the UI separately by running Streamlit app `streamlit run ui.py` command. It connects to the Pathway's backend API automatically and you will see the UI frontend is running on your browser.

# Data used 
Here i have used the data after the closing bell on 8th march 2024 but the data can be altered through dropbox.
[8thmarch.pdf](https://github.com/neelansh00/LLM-in-market-research./files/14550733/8thmarch.pdf)
