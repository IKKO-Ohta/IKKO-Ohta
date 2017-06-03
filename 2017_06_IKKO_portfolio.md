1.History
===
## Text2Feature
Text2Feature is the OSS Japanese document search engine written by Python3.  
This system is adopted by “Q&A communication system" [SHARP CLOUD LABS](http://qac.cloudlabs.sharp.co.jp/).  
GitHub: https://github.com/IKKO-Ohta/Text2Feature  

Job:
 - June 2016 ~ December	2016 	*engineer*  
 - December 2016 ~ March 2017 	*Chief engineer*  

release:
 - April 2016	release OSS version 1.0  

## VCS-Mirador
VCS-Mirador is the Web app for humanities research. 
this app is mainly written by Ruby on Rails.  
Supporting IIIF/International Image Interoperability Framework Json data, this system make them “Documents”. The document has annotations,hypothesis and comments. If you want, document is only shared by authorized group. In addition, this system has some SNS functions.  

α Version was announced in IPSJ 2017.  
This project is under development!  
GitHub: https://github.com/IKKO-Ohta/VCS_mirador  

Job:
 - April 2017 ~ 	*Chief engineer*  


2.Text2Feature
===

## What is Text2Feature?  
Text2Feature is a OSS Japanese Document Search Engine.  
With Morphological Analysis & Dependency Analysis, Text2Feature TF-IDF vectorizes existing documents. And this engine receives a query document, calculates cosine similarity between the input and the vectorized documents, and find one which looks like the query.  

## Purposes & Goals  
One of the Our project’s purpose is make document search engine easy for everyone to use. And our goal was that *actuary* T2F is adopted by other’s project. Fortunately SHARP CLOUDS LABS’s service “Q&A communication system” did.   
Now the more greater goal is getting more and more T2F users!

## T2F’s Beautiful Points  
**Accurately and speedy!**
We implement some useful methods.  
At first, we adopted the option features called by “Dep_n_gram”. If you want, T2F consider dependency analysis’s result as one of features. Here is the example of dep_bi_gram:  

input string: “太郎はおにぎりを食べる。”   
features by unigram: [“太郎”,”は”,”おにぎり”,”を”,”食べる”]  
features by unigram + dep_bi_gram: [“太郎”,”は”、”おにぎり”,”を”,”食べる”,”太郎-は”,”おにぎり-を”,”は-食べる”]  
This option can improves the accuracy slightly in the specific area.  

Secondly we implement some manual configuration functions such as “”synonym“, “blacklist” and ”whitelist”. These configuration may look like not smart. However when your available resource is hardly limited, these function can help you to keep your product’s accuracy.  

Thirdly we succeed building the effective models of morphological analysis & dependency analysis. Especially in Dependency analysis, our model is much lighter than naive method. And our model is not only speedy & memory efficient but also accurate.  

## T2F’s file structure & class diagram  




[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)


   [dill]: <https://github.com/joemccann/dillinger>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/joemccann/dillinger/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>