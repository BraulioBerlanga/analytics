# User Sessions Analysis
[![python][python-badge]][python-link][![jupyter][jupyter-badge]][jupyter-link][![vsc][vsc-badge]][vsc-link]

#### Analysis about user session data. Includes: 
<li>sessions</li>
<li>conversion</li>
<li>revenue</li>
<li>market segmentation</li>
<li>channel campaigns</li>
<li>CPC

![](header.png)

Obviously, we want you to analyze the data in the database file challenge.db file. This is a Zipped SQLite database with the following schema.
The data belongs to a company called Company X and contains information of e-commerce purchases that were made with Company X. Each purchase (in 'conversions' table) has a certain revenue attached to it and was made by a given user ('user_id'). In the 'session_souces' table you can find information of what sessions (a session is a set of events) happened on the company's website. Every user who made a conversion, had multiple sessions prior to this purchase which make up his customer journey. The link between conversions and those sessions is made via the 'attribution_customer_journey' table where for each conv_id from the 'conversions' table, you can find all sessions that belong to this customer journey.
The 'conversions_backend' table is exactly the same as the 'conversions' table in terms of format but contains data directly from the company's backend system and is considered true. In case the data in the 'conversions' table differs from the data in the 'conversions_backend' table, this is an issue.
Often there are external data sources (for instance for marketing costs) that come into play. In this case, there is one external data source api_adwords_costs table. This table contains per day and AdWords campaign ID the costs that Company X paid for running this ad. The campaign_id here links to the campaign_id in the 'session_sources' table.


Main libraries:

1. [![pandas][python-pandas-badge]][python-pandas-url], for data transformation
2. [![pandas][python-matplotlib-badge]][python-matplotlibe-url], for visualization

## Contributing

1.  [![Linkedin][linkedin-badge]][linkedin-url]

<!-- Markdown link & img dfn's -->
[python-pandas-badge]: https://img.shields.io/badge/python-pandas-blue
[python-pandas-url]: https://pypi.org/project/pandas/
[python-matplotlib-badge]: https://img.shields.io/badge/python-matplotlib-grenn?style=flat&logo=mats
[python-matplotlibe-url]: https://matplotlib.org/
[linkedin-badge]:https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white
[linkedin-url]:https://www.linkedin.com/in/berlangas/
[postgres-badge]:https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white
[postgres-link]:https://www.postgresql.org/
[python-badge]:https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue
[python-link]:https://www.python.org/
[jupyter-badge]:https://img.shields.io/badge/Jupyter-F37626.svg?&style=for-the-badge&logo=Jupyter&logoColor=white
[jupyter-link]:https://jupyter.org/
[vsc-badge]:https://img.shields.io/badge/VSCode-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white
[vsc-link]:https://code.visualstudio.com/
