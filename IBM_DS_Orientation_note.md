# What is Data Science

### <a href="#da">Data Source</a>

### <a href="#datamining">Data Mining and Big Data</a>

### <a href="#genetive">Genetive Ai, Machine Learning and Deep Learning</a>

### <a href="#ds">DS Career</a>

### <a href="#explore">Explore a DS Job</a>

### <a href="#glossary">Glossary</a>



## <a id="da">Data Source</a>

### Data Type

Delimited Text Files:

- Files used to store data as text
- Each value is separated by a delimiter

Delimiter - A sequence of one or more characters for specifying the boundary between independent entities or values.

**Comma, Tab, Colon, Vertical Bar, Space**

**XML**: Extensible Markup Language, or XML, is a markup language with set rules for encoding data.

- Readable by both humans and machines
- Self-descriptive language

- ﻿﻿Similar to .HTML in some respects
- ﻿﻿Does not use predefined tags like . HTML does
- ﻿﻿Platform independent
- ﻿﻿Programming language independent
- ﻿﻿Makes it simpler to share data between systems

**JavaScript Object Notation**, or JSON, is a text-based open standard designed for transmitting structured data over the web.

- ﻿﻿Language-independent data format
- ﻿﻿Can be read in any programming language
- ﻿﻿Easy to use
- ﻿﻿Compatible with a wide range of browsers
- ﻿﻿Considered as one of the best tools for sharing data



## <a id="datamining">Data Mining and Big Data</a>

### Data Mining and Big Data

In the 'Big Data and Data Mining' lesson, delve into the world of digital transformation driven by Big Data. Explore Cloud Computing's role, foundational Big Data concepts, tools like Hadoop and Spark, and gain insights into Data Mining techniques for informed decision-making.

| Asset name and type                                          | Description                                                  |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| "How Big Data is Driving Digital Transformation" video       | Explore the impact of Big Data on digital transformation.    |
| "Introduction to Cloud" video                                | Get introduced to the fundamentals of cloud computing.       |
| "Cloud for Data Science" video                               | Learn how the cloud is relevant in the field of data science. |
| "Foundations of Big Data" video                              | Build your understanding of key Big Data concepts.           |
| "Data Scientists at New York University" video               | Discover the work of data scientists at New York University. |
| "What is Hadoop?" video                                      | Understand the significance of Hadoop in Big Data processing. |
| "Big Data Processing Tools: Hadoop, HDFS, Hive, and Spark" video | Dive into the tools used for Big Data processing.            |
| "Data Mining" reading                                        | Read an excerpt on data mining explore the principles and concepts of data mining. |
| Practice quiz                                                | Take a practice quiz to evaluate how well you’ve understood the material presented in this lesson. |
| Glossary                                                     | Use this glossary of terms to review the terminology presented in this lesson. |
| Graded quiz                                                  | Test your knowledge from this lesson by taking the graded quiz. |

### Data Mining

#### Establishing Data Mining Goals

Key questions: 

- the concerns about the costs and benefits of the exercise. 
- determine the expected level of accuracy and usefulness of the results obtained from data mining.
- the cost-benefit trade-offs for the desired level of accuracy are important considerations for data mining goals

#### Selecting Data

The output of data mining depends upon: the quality of data being used.

The type of data, its size, and frequency of collection have --- a direct bearing on the cost of data mining exercise.

#### Preprocessing Data

- you identify the **irrelevant attributes** of data and **expunge** such attributes from further consideration.
-  identifying the **erroneous aspects** of the data set and **flagging** them as such is necessary.
- develop a formal method of **dealing with missing data** and determine whether the data are missing randomly or systematically.
  - missing randomly, simple
  - missing Systematically, consider the impact. The missing data can be excluded from  the entire analysis.

For instance, a particular subset of individuals in a large data set may have refused to disclose their income. Findings relying on an individual's income as input would exclude details of those individuals whose income was not reported. This would lead to systematic biases in the analysis. 

#### Transforming Data

- **Data reduction** algorithms, can reduce the number of attributes without a significant loss in information. such as <u>Principal Component Analysis</u> 
- Develop a representative indicator - aggregating income (wage income, rental properties, support payments etc.) 
- Transform variables from one type to another. (continuous variable --> a categorical variable: low, medium, high-income)

#### Storing Data

- store data in a format, keep it secure, avoid data scattered on different servers for data mining algorithm
- Data safety and privacy should be a prime concern for storing data.

#### Mining Data

This step covers <u>data analysis methods</u>, including **parametric and non-parametric methods,** and machine-learning algorithms. A good starting point for data mining is **data visualization**. Multidimensional views of the data using the advanced graphing capabilities of data mining software are very helpful in developing a preliminary understanding of the trends hidden in the data set.

#### Evaluating Mining Results

Do a formal evaluation of the results.

Formal evaluation could include testing **the predictive capabilities of the models on observed data** to see **how effective and efficient the algorithms have been in reproducing data**. This is known as an "in-sample forecast". (正式评估可包括在观测数据上测试模型的预测能力，以了解算法在再现数据方面的有效性和效率。这就是所谓的 "样本内预测"。)

Data mining and evaluating the results becomes an iterative process such that the analysts use better and improved algorithms to improve the quality of results generated in light of the feedback received from the key stakeholders.

### Big Data

#### BG Characteristics

| value        | Investment in big data creates value               |
| ------------ | -------------------------------------------------- |
| **volume**   | scale of the data                                  |
| **velocity** | speed it is collected                              |
| **variety**  | comes from a variety of sources                    |
| **veracity** | conforms to facts (the quality and origin of data) |

#### Cloud Characteristics

- **On-demand** -- Access to processing, storage, and network

- **Network access** -- Resources access via the Internet

- **Resource pooling** -- Shared resources dynamically assigned

- **Elasticity** -- Automatically scales resource access
- **Measured service** -- Only pay for what you use or reserve

#### Open-source Big Data Computing Tools

- Apache Hadoop : **Distributed storage and processing** of large datasets across clusters of computers.

  **Hadoop Distributed File System**, or **HDFS**, is a storage system for big data that runs on multiple commodity hardware (products can be bought and sold) connected through a network.

  - Provides scalable and reliable big data storage by partitioning files over multiple nodes

  - Splits large files across multiple computers, allowing parallel access to them

  - Replicates file blocks on different nodes to prevent data loss

- Apache Hive : Provides large data set management

  Hive is an open-source data warehouse software for **reading, writing, and managing large data** set files that are stored directly in either HDFS or other data storage systems such as  Apache HBase

  **Read-based** -> <u>Not suitable for transaction processing</u> that involves a high percentage of write operations.

  Better suited for: • Data warehousing tasks such as ETL, reporting, and data analysis • Easy access data via SQL

- Apache Spark : Data processing engine

  Spark is a general-purpose **data processing engine** designed to **extract and process large volumes of data** for a wide range of applications.

  - ﻿﻿Interactive Analytics, Streams Processing, Machine Learning, ﻿﻿Data Integration, ETL
  
  The ultimate purpose of analytics is to summarize findings in tables and plots for effective communication of insights and findings. The content highlights that big data clusters distribute data to many computers for parallel processing.



## <a id="genetive">Genetive Ai, Machine Learning and Deep Learning</a>

### Genetive AI, Machine Learning and Deep Learning

- Big Data has five characteristics: velocity, volume, integrity, and value.
- The five cloud computing characteristics are scalability, collaboration, accessibility, and software maintenance.
- Data mining has a six-step process: goal setting, selecting data sources, preprocessing, transforming, mining, and evaluation. 
- The availability of so many disparate amounts of data created by people, tools, and machines requires new, innovative, and scalable technology to drive transformation.
- Deep learning utilizes neural networks to teach itself patterns in inputs and outputs. Machine learning is a subset of AI that uses computer algorithms to learn about data and make predictions without explicitly programming the analysis methods into the system.  
- Regression identifies the strength and amount of the correlation between one or more inputs and an output.
- Skills involved in processing Big Data include the application of statistics, machine learning models, and some computer programming.
- Generative AI, a subset of artificial intelligence, focuses on producing new data rather than just analyzing existing data. It allows machines to create content, including images, music, language, computer code, and more, mimicking creations by people.



## <a id="ds">DS Career</a>

### The Report Structure

Curiocity, humous sense, technical skills.

Learn math, statistics, new tech.

### Recruiter desire skills:

- Domain-specific knowledge
- Analyzing both structured and unstructured data
- Presenting and storytelling

### Should Look for the Person who has the following Skills

- Excitement to work with data
  - Excitement to work with data in their industry, Ask good questions

- Logic Mind
  	- Think analytically and computationally
  	- Background in mathematics, statistics, and probability
- Computer Programming
  - Python, R, Data Storage (SQL), Manipulate Data (Pandas), Algorithms
- Creating the narrative
  - Communicating, Instructing, Presenting, Storytelling, Synthesizing
- Reporting
  - What is gained, Defined goals, Significance, Context, Practicality and usefulness, Future developments

### Have You Done Your Job as a Writer?

As a data scientist, you are expected to do thorough analysis with the appropriate data, deploying the appropriate tools. As a writer, you are responsible for communicating your findings to the readers. Transport Policy, a leading research publication in transportation planning, offers a checklist for authors interested in publishing with the journal. The checklist is a series of questions authors are expected to consider before submitting their manuscripts to the journal. I believe the checklist is useful for budding data scientists and, therefore, I have reproduced it verbatim for their benefit.

- Have you told readers, at the outset, what they might gain by reading your paper?
- Have you made the aim of your work clear?
- Have you explained the significance of your contribution?
- Have you set your work in the appropriate context by giving sufficient background (including a complete set of relevant references) to your work?
- Have you addressed the question of practicality and usefulness?
- Have you identified future developments that might result from your work?
- Have you structured your paper in a clear and logical fashion?



## <a id="explore">Explore a DS Job</a>

Identify the following aspects of data science job post:

1. What is the company name that is advertising the job?
2. What is the job title?
3. Where is the role located?
4. What is the expected salary or salary range?
5. What is the total number of results from the search for the job post?
6. What is one technical responsibility from the job post related to something you learned about in this course?
7. What are two required technical skills from the job post?
8. What are at least two ideas or concepts you learned about in this course relevant to these job posts?



## <a id="glossary">Glossary</a>

### Deep Learning and Machine Learning Lesson Glossary

Welcome! This alphabetized glossary contains many of the terms in this course. These terms are important for you to recognize when working in the industry, participating in user groups, and participating in other certificate programs.

| Term                              | Definition                                                   | Video where the term is introduced       |
| --------------------------------- | ------------------------------------------------------------ | ---------------------------------------- |
| Artificial Neural Networks        | Collections of small computing units (neurons) that process data and learn to make decisions over time. | Artificial Intelligence and Data Science |
| Bayesian Analysis                 | A statistical technique that uses Bayes' theorem to update probabilities based on new evidence. | Applications of Machine Learning         |
| Business Insights                 | Accurate insights and reports generated by generative AI can be updated as data evolves, enhancing decision-making and uncovering hidden patterns. | Generative AI and Data Science           |
| Cluster Analysis                  | The process of grouping similar data points together based on certain features or attributes. | Neural Networks and Deep Learning        |
| Coding Automation                 | Using generative AI to automatically generate and test software code for constructing analytical models, freeing data scientists to focus on higher-level tasks. | Generative AI and Data Science           |
| Data Mining                       | The process of automatically searching and analyzing data to discover patterns and insights that were previously unknown. | Artificial Intelligence and Data Science |
| Decision Trees                    | A type of machine learning algorithm used for decision-making by creating a tree-like structure of decisions. | Applications of Machine Learning         |
| Deep Learning Models              | Includes Generative Adversarial Networks (GANs) and Variational Autoencoders (VAEs) that create new data instances by learning patterns from large datasets. | Generative AI and Data Science           |
| Five V's of Big Data              | Characteristics used to describe big data: Velocity, volume, variety, veracity, and value. | Neural Networks and Deep Learning        |
| Generative AI                     | A subset of AI that focuses on creating new data, such as images, music, text, or code, rather than just analyzing existing data. | Generative AI and Data Science           |
| Market Basket Analysis            | Analyzing which goods tend to be bought together is often used for marketing insights. | Neural Networks and Deep Learning        |
| Naive Bayes                       | A simple probabilistic classification algorithm based on Bayes' theorem. | Applications of Machine Learning         |
| Natural Language Processing (NLP) | A field of AI that enables machines to understand, generate, and interact with human language, revolutionizing content creation and chatbots. | Generative AI and Data Science           |
| Precision vs. Recall              | Metrics are used to evaluate the performance of classification models. | Applications of Machine Learning         |
| Predictive Analytics              | Using machine learning techniques to predict future outcomes or events. | Neural Networks and Deep Learning        |
| Synthetic Data                    | Artificially generated data with properties similar to real data, used by data scientists to augment their datasets and improve model training. | Generative AI and Data Science           |



# Big Data and Data Mining Lesson Glossary

Welcome! This glossary contains many of the terms in this lesson. These terms are important for you to recognize when working in the industry, participating in user groups, and participating in other certificate programs.

| Term                                  | Definition                                                   | Video where the term is introduced                       |
| ------------------------------------- | ------------------------------------------------------------ | -------------------------------------------------------- |
| Analytics                             | The process of examining data to draw conclusions and make informed decisions is a fundamental aspect of data science, involving statistical analysis and data-driven insights. | Data Scientists at New York University                   |
| Big Data                              | Vast amounts of structured, semi-structured, and unstructured data are characterized by its volume, velocity, variety, and value, which, when analyzed, can provide competitive advantages and drive digital transformations. | How Big Data is Driving Digital Transformation           |
| Big Data Cluster                      | A distributed computing environment comprising thousands or tens of thousands of interconnected computers that collectively store and process large datasets. | What is Hadoop?                                          |
| Broad Network Access                  | The ability to access cloud resources via standard mechanisms and platforms such as mobile devices, laptops, and workstations over networks. | Introduction to Cloud                                    |
| Chief Data Officer (CDO)              | An emerging role responsible for overseeing data-related initiatives, governance, and strategies, ensuring that data plays a central role in digital transformation efforts. | How Big Data is Driving Digital Transformation           |
| Chief Information Officer (CIO)       | An executive is responsible for managing an organization's information technology and computer systems, contributing to technology-related aspects of digital transformation. | How Big Data is Driving Digital Transformation           |
| Cloud Computing                       | The delivery of on-demand computing resources, including networks, servers, storage, applications, services, and data centers, over the Internet on a pay-for-use basis. | Introduction to Cloud                                    |
| Cloud Deployment Models               | Categories that indicate where cloud infrastructure resides, who manages it, and how cloud resources and services are made available to users, including public, private, and hybrid models. | Introduction to Cloud                                    |
| Cloud Service Models                  | Models based on the layers of a computing stack, including Infrastructure as a Service (IaaS), Platform as a Service (PaaS), and Software as a Service (SaaS), represent different cloud computing offerings. | Introduction to Cloud                                    |
| Commodity Hardware                    | Standard, off-the-shelf hardware components are used in a big data cluster, offering cost-effective solutions for storage and processing without relying on specialized hardware. | What is Hadoop?                                          |
| Data Algorithms                       | Computational procedures and mathematical models used to process and analyze data made accessible in the cloud for data scientists to deploy on large datasets efficiently. | Cloud for Data Science                                   |
| Data Replication                      | A strategy in which data is duplicated across multiple nodes in a cluster to ensure data durability and availability, reducing the risk of data loss due to hardware failures. | What is Hadoop?                                          |
| Data Science                          | An interdisciplinary field that involves extracting insights and knowledge from data using various techniques, including programming, statistics, and analytical tools. | Data Scientists at New York University                   |
| Deep Learning                         | A subset of machine learning that involves artificial neural networks inspired by the human brain, capable of learning and making complex decisions from data on their own. | Data Scientists at New York University                   |
| Digital Change                        | The integration of digital technology into business processes and operations leads to improvements and innovations in how organizations operate and deliver value to customers. | How Big Data is Driving Digital Transformation           |
| Digital Transformation                | A strategic and cultural organizational change driven by data science, especially Big Data, to integrate digital technology across all areas of the organization, resulting in fundamental operational and value delivery changes. | How Big Data is Driving Digital Transformation           |
| Distributed Data                      | The practice of dividing data into smaller chunks and distributing them across multiple computers within a cluster enables parallel processing for data analysis. | What is Hadoop?                                          |
| Hadoop                                | A distributed storage and processing framework used for handling and analyzing large datasets, particularly well-suited for big data analytics and data science applications. | Data Scientists at New York University                   |
| Hadoop Distributed File System (HDFS) | A storage system within the Hadoop framework that partitions and distributes files across multiple nodes, facilitating parallel data access and fault tolerance. | What is Hadoop?                                          |
| Infrastructure as a Service (IaaS)    | A cloud service model that provides access to computing infrastructure, including servers, storage, and networking, without the need for users to manage or operate them. | Introduction to Cloud                                    |
| Java-Based Framework                  | Hadoop is implemented in Java, an open-source, high-level programming language, providing the foundation for building distributed storage and processing solutions. | Big Data Processing Tools: Hadoop, HDFS, Hive, and Spark |
| Map Process                           | The initial step in Hadoop’s MapReduce programming model, where data is processed in parallel on individual cluster nodes, often used for data transformation tasks. | What is Hadoop?                                          |
| Measured Service                      | A characteristic where users are billed for cloud resources based on their actual usage, with resource utilization transparently monitored, measured, and reported. | Introduction to Cloud                                    |
| On-Demand Self-Service                | The capability for users to access and provision cloud resources such as processing power, storage, and networking using simple interfaces without human interaction with service providers. | Introduction to Cloud                                    |
| Rapid Elasticity                      | The ability to quickly scale cloud resources up or down based on demand, allowing users to access more resources when needed and release them when not in use. | Introduction to Cloud                                    |
| Reduce Process                        | The second step in Hadoop's MapReduce model is where results from the mapping process are aggregated and processed further to produce the final output, typically used for analysis. | What is Hadoop?                                          |
| Replication                           | The act of creating copies of data pieces within a big data cluster enhances fault tolerance and ensures data availability in case of hardware or node failures. | What is Hadoop?                                          |
| Resource Pooling                      | A cloud characteristic where computing resources are shared and dynamically assigned to multiple consumers, promoting economies of scale and cost-efficiency. | Introduction to Cloud                                    |
| Skills Network Labs (SN Labs)         | Learning resources provided by IBM, including tools like Jupyter Notebooks and Spark clusters, are available to learners for cloud data science projects and skill development. | Cloud for Data Science                                   |
| Spilling to Disk                      | A technique used in memory-constrained situations where data is temporarily written to disk storage when memory resources are exhausted, ensuring uninterrupted processing. | Big Data Processing Tools: Hadoop, HDFS, Hive, and Spark |
| STEM Classes                          | Science, Technology, Engineering, and Mathematics (STEM) courses typically taught in high schools prepare students for technical careers, including data science. | Data Scientists at New York University                   |
| Variety                               | The diversity of data types, including structured and unstructured data from various sources such as text, images, video, and more, posing data management challenges. | Foundations of Big Data                                  |
| Velocity                              | The speed at which data accumulates and is generated, often in real-time or near-real-time, drives the need for rapid data processing and analytics. | Foundations of Big Data                                  |
| Veracity                              | The quality and accuracy of data, ensuring that it conforms to facts and is consistent, complete, and free from ambiguity, impacts data reliability and trustworthiness. | Foundations of Big Data                                  |
| Video Tracking System                 | A system used to capture and analyze video data from games, enabling in-depth analysis of player movements and game dynamics, contributing to data-driven decision-making in sports. | How Big Data is Driving Digital Transformation           |
| Volume                                | The scale of data generated and stored is driven by increased data sources, higher-resolution sensors, and scalable infrastructure. | Foundations of Big Data                                  |
| V's of Big Data                       | A set of characteristics common across Big Data definitions, including Velocity, Volume, Variety, Veracity, and Value, highlighting the rapid generation, scale, diversity, quality, and value of data. | Foundations of Big Data                                  |

