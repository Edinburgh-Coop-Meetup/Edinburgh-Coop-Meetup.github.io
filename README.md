# Edinburgh Coop Meetup


## Develop locally

To build the Jekyll site:

```
docker run --rm   --volume="$PWD:/srv/jekyll:Z" -p 4000:4000 -it jekyll/builder:4 /bin/bash -c 'gem install webrick && jekyll serve'
```

It should then be available on http://0.0.0.0:4000/


To build the DataTig admin site:

```
pip install datatig
python -m datatig.cli build . --staticsiteoutput _site/datatig
```
