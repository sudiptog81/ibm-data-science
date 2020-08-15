# Detecting Prevalence of Fake News in Newsletter E-Mails

## Which topic did you choose to apply the data science methodology to? (2 marks)

I have chosen to apply the data science methodology on electronic mails. E-Mails have structured data fields and have information about the routing, sender, recipient, and software used to send the message in the mail header, apart from the actual mail body.

## Using the topic that you selected, complete the Business Understanding stage by coming up with a problem that you would like to solve and phrasing it in the form of a question that you will use data to answer. (3 marks)

Newsletters are delivered to E-Mail inboxes of millions of people. Presence of half-truths and factual inaccuracies in the content might exploit one's confirmation bias and lead them to have an opinion based on misinformation. This might adversely affect one's opinion about legitimate facts. As observed in the real world, misinformation can lead to panic, hate or prejudice towards a topic, an issue, a business/brand or an entire community. Misinformation can be spread with malicious intent using a false identity and with newsletters pretending to be from reputed sources.
Phrasing the problem in order to apply the data science methodology: Can we determine the authenticity of the received newsletter and its contents based on the metadata available within the e-mail message?

## Briefly explain how you would complete each of the following stages for the problem that you described in the Business Understanding stage, so that you are ultimately able to answer the question that you came up with. (5 marks): Analytic Approach, Data Requirements, Data Collection, Data Understanding and Preparation, Modeling and Evaluation.

### Analytic Approach

We can use Descriptive Models to identify prevalence of words and their coherence. Pairing this with historical data, we can use statistical tools to identify behavioral trends in the mails sent by the sender. Using a Classification Model based on the results of the descriptive study, we can classify the newsletters presenting misinformation and those presenting legitimate information.

### Data Requirements

In ordered to study the problem, we have to select a cohort of e-mail messages from a sample population. These e-mails can then be structured into records having the sender information, the receiver information, the subject line, the server the message was sent from and the actual plain-text content of the E-Mail message. Organizing the data in such a way makes the data transactional for the models to be implemented.

### Data Collection

Data required for filtering junk mails from the cohort requires spam lists that can be acquired through online block-lists which are released on a regular basis. The E-Mail messages are to be procured from voluntary candidates who wish to share the data in a standard format. These messages need to be parsed and populated into data frames and proper columns. The content of the message body needs to be sliced into an array of words which is easier to process. Sources and feeds from organizations such as The International Fact-Checking Network (Poynter Institute) can be crawled to populate a list of fake news reports.

### Data Understanding and Preparation

In order to understand the data better, we can try normalizing the textual data. One way we can accomplish this is by converting everything to lowercase. We can tackle common variations of words with stemming software (e.d. port stemmer). The data will be categorical and subjective. We can use "Yes" and "No" classes to classify whether the message contains misinformation or not.

### Modelling and Evaluation

The existence of many junk mails in the data shall lead to higher accuracy for "Yes" category but poor accuracy on the "No" category. These can be filtered out on the basis of the server or domain sending the message if those values exist in the block-lists. Natutal Language Processing and Sentiment Analysis can be used to check if the contents of the message match those in the fake news reports list. In order to evaluate the algorithm and the model, we have to look into the false positives and false negatives from the model to calculate its precision and recall. The model having a high F1-score can then be selected.
