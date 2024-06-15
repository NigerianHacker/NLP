  #### 4. Wikipedia Language Model
- **Technologies:** Python
- **Description:** Developed a 2-gram language model from scratch to improve speech recognition quality for a client who dictates books. The model was tailored to handle specific linguistic features of book language.
- **Challenges:** Existing models were not suitable, and the client required a model without using pre-existing solutions or external libraries.

##### Data Preprocessing:
- **Text Normalization:** Converted all text to lowercase to ensure consistency across the dataset.
- **Tokenization:** Split text into tokens (words) to build the 2-gram model.
- **Cleaning:** Removed punctuation and numbers to focus on linguistic features only.

##### Method:
- **2-gram Model:** Implemented using pure Python; calculated the probabilities of a word given the previous word in the sequence.
- **Backoff Technique:** Implemented a backoff mechanism to handle unseen word combinations during testing.

##### Experiment Design:
- **Dataset:** Used a book excerpt provided by the customer.
- **Split:** 80% training, 20% testing.
- **Hyper-parameters:** Minimized the threshold for frequency counts to decide when to backoff.

##### Evaluation Metric:
- **Perplexity:** Measured the perplexity of both the models with and without the backoff technique to assess performance improvements.

##### Findings and Improvements:
- **Without Backoff:** The model struggled with unseen word pairs, leading to higher perplexity.
- **With Backoff:** Performance improved, indicating better handling of rare words.
- **Drawbacks:** The model's simplicity means it may still struggle with complex language patterns or larger vocabularies.
- **Potential Improvements:** Future versions could incorporate higher n-grams and explore smoothing techniques.

##### Performance Comparison:
- **Impact of Backoff:** Significantly reduced perplexity, enhancing model reliability for speech recognition tasks.

##### Documentation:
- **Model Diagram:** `![Language Model Diagram](path/to/language_model_diagram.png)`
- **Perplexity Charts:** `![Perplexity Comparison Chart](path/to/perplexity_chart.png)`
