# Product-Pulse-AI
ProductPulse-AI is a Python-based tool designed to help entrepreneurs, product managers, and innovators validate and refine product ideas before launch. It leverages web scraping, sentiment analysis, and trend evaluation to provide actionable insights and a success likelihood score.


**Overview**
Launching a product is risky, especially without understanding existing competition, market trends, and user sentiment. ProductPulse-AI automates the research process by:
- Checking for similar products online  
- Collecting review-like text from e-commerce, forums, and review sites  
- Performing sentiment analysis to identify positive and negative feedback  
- Analyzing Google Trends to detect market interest and top regions  
- Computing a success score and providing a launch strategy  

**"This helps founders save time, validate ideas, and make informed decisions before investing in production and marketing."**


**Features**
- **Idea Availability Check**: Determines if similar products already exist online.  
- **Web Review Scraper**: Collects review-like paragraphs from top search results across Amazon, Flipkart, Walmart, Reddit, Trustpilot, ProductHunt, and more.  
- **Sentiment Analysis**: Uses DistilBERT (Hugging Face Transformers) to compute positive, negative, and average sentiment scores.  
- **Trend Analysis**: Fetches Google Trends data to analyze market interest and compute trend slopes.  
- **Top Regions Identification**: Identifies countries where the product idea is gaining attention.  
- **Success Score Calculation**: Composite score combining trends, sentiment, review volume, and price competitiveness.  
- **Actionable Recommendations**: Provides go-to-market strategy, content plan, launch timeline, and product improvement suggestions.  
- **Interactive CLI**: Guides users through multiple product evaluations in a single session.


  **How It Works**
1. **Idea Check**:  
   - The tool searches for existing commercial pages of the product.  
   - If similar products exist, the user is prompted to try a different idea.  
2. **Web Review Collection**:  
   - Searches for queries like `<product> reviews`, `<product> buy`, `<product> complaints`.  
   - Scrapes top results from e-commerce, forums, and review blogs.  
   - Extracts relevant text blocks for sentiment and keyword analysis.  
3. **Sentiment Analysis**:  
   - Uses DistilBERT fine-tuned for sentiment classification.  
   - Computes average sentiment score, positive %, negative %, and top negative keywords.  
4. **Trend Analysis**:  
   - Fetches Google Trends data for the product keyword.  
   - Computes trend slope (rising, steady, or declining).  
   - Identifies top countries/regions with high interest.  
5. **Success Scoring**:  
   - Combines trend slope, sentiment, review count, and price competitiveness into a single score (0–1).  
   - Categorizes the product as “Likely to succeed” or “Likely unsuccessful”.  
6. **Launch Recommendations**:  
   - Suggests marketing channels (social media, influencer campaigns, content marketing).  
   - Provides launch timeline based on trend slope.  
   - Lists key action items and product modifications based on negative feedback.  
   - Optionally generates a ready-to-use LLM prompt for an 8-week marketing plan.


**Key Technologies**
-1.Python 3.x
-2.Transformers (Hugging Face) – DistilBERT for sentiment analysis
-3.Google Trends API (pytrends) – Trend and regional interest analysis
-4.Web Scraping – requests + BeautifulSoup4
-5.Search Automation – googlesearch-python
-6.Data Processing – numpy, pandas, scikit-learn
