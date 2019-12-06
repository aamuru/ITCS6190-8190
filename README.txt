Web Crawling:-

For web crawling we used Scrapy ,to run scrapy navicate to scraper folder in terminal , and run -
 scrapy crawl wallmart -o wallmart.json // fro scraping wallmart
 scrapy crawl amazon-o amazon.json // fro scraping amazon

Indexing:-

After crawling -two jason files are generated wallmart.json and amazon.json which will be our input for our program.

copy both this files in your current directory where you are going to run your program and run:
spyder-junt run
dsba=spark-submit index.py

which generates-TopRecomendation.json//for top 100 recomendation
Index.json//which is our index file 
CleanInput.json// which contains our preprocessed input ,which is look up for our index file 

Api:-

copy Index.json,TopRecomemdation.json and CleanInput.json inside API , where out API is written 
to run out API:
export FLASK_APP=Api.py
flask run

you can view the output in your localHost at- http://127.0.0.1:5000/

url gives TopRecomemdation in json format 

To search - http://127.0.0.1:5000/search/<keywords>

enter your keywords to search and is dispplayedin json format.

