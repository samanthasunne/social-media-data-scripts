# Getting data from APIs

One of the ways in which companies allow you to tap into these data troves is via an API, which stands for Application Programming Interface. APIs are like a kind of middleman between the social media platform and developers who wish to access information from the platform.

An API can also allow us to make requests for specific data, which we’ll receive in a structured form. Developers can request data with a script (code that is written to perform specific and often repetitive tasks for us) by opening up a data stream (basically a very plain website that displays one data point after another based on what a developer requested) through the API and then by compiling each data point into a spreadsheet.

This directory contains scripts related to APIs.

### Using Twitter's API

#### Scripts

* [twitter_tweet_dumper.py](https://github.com/lamthuyvo/social-media-data-scripts/blob/master/scripts/twitter_tweet_dumper.py): Up to 3200 tweets from an individual account (includes tweet id, time stamp, location, text, retweet count, favorite count (though the favorite count is inaccurate for retweets), whether something was a manual retweet, how it was tweeted (Tweetdek, Android, etc.)). This script was modified from [@Yanofsky](https://gist.github.com/yanofsky/5436496)'s original script.
* [twitter_get_friends.py](https://github.com/lamthuyvo/social-media-data-scripts/blob/master/scripts/twitter_get_friends.py): Twitter user bios (name, display name, bio, followers count (at time of scraping),  following count (at time of scraping), when the account was created, location given in the bio) for all the accounts that a specific user follows.
* [twitter_get_followers.py](https://github.com/lamthuyvo/social-media-data-scripts/blob/master/scripts/twitter_get_followers.py): Twitter user bios (name, display name, bio, followers count (at time of scraping),  following count (at time of scraping), when the account was created, location given in the bio) for all the accounts that follow a specific user.
* [twitter_bio_info_compiler.py](https://github.com/lamthuyvo/social-media-data-scripts/blob/master/scripts/twitter_bio_info_compiler.py): Twitter user bios (name, display name, bio, followers count (at time of scraping),  following count (at time of scraping), when the account was created, location given in the bio) for a list of accounts you specify
* [twitter_searcher.py](https://github.com/lamthuyvo/social-media-data-scripts/blob/master/scripts/twitter_searcher.py): You can search Twitter via its search API going back 7 days and grab tweets (id, author name, timestamp when it was created, favorites (again, unreliable), retweets, text)

### Using Facebook's API

Facebook does not allow you to

#### Scripts
* [fb_get_posts_fb_group.py](https://github.com/lamthuyvo/social-media-data-scripts/blob/master/scripts/fb_get_posts_fb_group.py) or [fb_get_posts_fb_group_multiple.py](https://github.com/lamthuyvo/social-media-data-scripts/blob/master/scripts/fb_get_posts_fb_group_multiple.py): These scripts allow you to gather data from _public_ Facebook groups, either from just one or multiple groups. Adapted from [@minimaxir](https://github.com/minimaxir/facebook-page-post-scraper)'s scripts.
* [fb_get_posts_fb_page.py](https://github.com/lamthuyvo/social-media-data-scripts/blob/master/scripts/fb_get_posts_fb_page.py) or [fb_get_posts_fb_page_multiple.py](https://github.com/lamthuyvo/social-media-data-scripts/blob/master/scripts/fb_get_posts_fb_page_multiple.py): These scripts allow you to gather data from _public_ Facebook pages, either from just one or multiple pages. Adapted from [@minimaxir](https://github.com/minimaxir/facebook-page-post-scraper)'s scripts.
* [fb_get_comments_from_fb.py](https://github.com/lamthuyvo/social-media-data-scripts/blob/master/scripts/fb_get_comments.py): This script allows you to get the comments from each Facebook group or page _after_ you have run the aforementioned scripts. Adapted from [@minimaxir](https://github.com/minimaxir/facebook-page-post-scraper)'s scripts.
* [fb_get_page_info.py](https://github.com/lamthuyvo/social-media-data-scripts/blob/master/scripts/fb_get_comments.py): This script allows you to get Facebook Page information, such as the title, description, fan count, for a number of Facebook pages.  
* [fb_id_proofer.py](https://github.com/lamthuyvo/social-media-data-scripts/blob/master/scripts/fb_id_proofer.py): This script allows you to go through a list of Facebook Page IDs and see whether they are valid.


## How to run each script
1. Follow the instructions in the comments of each script to customize your API query and resulting `.csv` file
2. Run your script with the bash command `python scriptname.py` to generate a csv of tweets or Facebook posts. Then, go make do some journalism-ing!