# WebScraper
## Project implementation steps
### Stages 1-3
1. Provide url address of product's opinions webpage
2. Send the request to provided url address 
3. If statuss code is OK, fetch all opinions from requested webpage
4. For all fetched opinions, parse them to extract relevant data
5. Check if there is next page with opinions
6. For all remaining pages repeat steps 2-5
7. Save obtained opinions

## Project inputs
### Products codes
- 124893467
- 116421    227
- 34935197
- 174881911
- 26968156
- 8679864
- 105022684
### Product structure
|component|name|selector|
|---------|----|--------|
|opinions Id opinios author |id|[data-entry-id]|
|authors name|name|span.user-post__author-name|
|authors recommendation|recommendation| span.user-post__author-recomendation > em|
|score expressed in number of start|score|.user-post__score-count|
|opinions content|content|div.user-post__text|
|list of product advantages|advantages|div.review-feature__item--positive|
| list of product disadvantages|disadvantages|div.review-feature__item--negative|
| how many users think that opinion was helpful|like|button.vote.yes > span|
| how many users think that opinion was unhelpful|dislike|button.vote.no > span|
| publishing date|publishing_date|span.user-post__published > time:nth-child(1)[datetime] |
| purchase date|purchase_date|span.user-post__published > time:nth-child(2)[datetime]|