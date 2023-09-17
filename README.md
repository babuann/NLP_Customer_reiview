# NLP_Customer_reiview:

**Understand the problem**: I started by understanding the problem statement and the business context. In this case, we are building a customer experience platform for B2B customers, and one of the core components is an NLP engine that would consume textual data and generate insights. The problem statement is that the initial iteration for an e-commerce customer with their reviews data is missing context and not adding a lot of value. The business team is looking for meaningful labels that can provide context to the reviews.

**Analyze the Amazon's feedback**:nalyze the feedback received from the business team and try to understand their expectations. They have shared Amazon's mobile product page as a reference, where labels are generated based on the review text. However, they mentioned that it still misses the context, and users need to do analysis on their own. They are looking for labels that can provide context to the reviews, such as whether the battery life is good or bad, memory card is good/bad, available/not available, and camera quality is good or bad.

**Explore the data**:
    1. **Reviews**: This column contains the text of the reviews left by the customers. This is the primary column that we would use to identify the aspect terms.
		2. **Title**: This column contains the title of the reviews. While the title may not always contain aspect terms, it can provide additional context to the reviews and help in identifying the aspect terms.
		3. **Clothing ID**: This column contains the ID of the clothing item being reviewed. While this column may not directly help in identifying the aspect terms, it can be used to group the reviews by clothing item and analyze the aspect terms for each item separately.
  
**Preprocess the data**:preprocess the data by cleaning the text, removing stop words, stemming or lemmatizing the words and converting all into lowercase.

**Aspect term extraction**:I tried two approaches one will Langchain and LLama2-chathf model will return output ["Aspect",Sentiment] or detect the nouns and pronounsusing post tagging.

**Model selection**:Here we can use SVM(linear- as the requirement says good or bad), Nave Bayes as the we have small dataset.  For the time being i was using rule based model to classify which are good or bad.

 **Train the model**: a rule-based model or a machine learning model. to evaluate we can depend on f1score and precision.
 
  **Generate output**:  generate a CSV file as an output that contains all the existing columns plus a new column for the inference/output for each review. I would take Clothing ID 1078 for my analysis and code(model) as it has the maximum number of reviews.
  
 **Asumptions**:
Due to lack of computational resources i couldnt fetch the aspect and sentiment of the entire dataset .By adding pretrained aspect to menntion the rule based approach.
 
