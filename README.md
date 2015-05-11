### Concurrent spider

This repository contains a set-up to have a highly scalable web crawler using PHP, RabbitMQ and Solr. How it works?

* You start the crawler with `php start_crawler https://github.com`
* 1 item is added to the queue
* Run `php crawlurl.php` which will start picking up items from the queue
* Everytime a URL is crawled new URL's are found. These url's are posted on the queue

You can set-up as much as processes you would like, but setting up too much might flood the website.