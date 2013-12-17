Anaylsis of Governor Races
==========================

Analysis of polling data about the upcoming Governor races


## Collect and Clean
The [Real Clear Politics](http://www.realclearpolitics.com) website archives many political polls. In addition, they combine related polls to form an "RCP average" estimate of public opinion over time.

First, create an `get_poll_xml` function, that finds and downloads an XML page from Real Clear Politics:

```python
def get_poll_xml(poll_id):
    url = "http://charts.realclearpolitics.com/charts/%d.xml" % poll_id
    return requests.get(url).text
# get_poll_xml(1044)
```

