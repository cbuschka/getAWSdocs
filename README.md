# getAWSdocs.py

## About

One thing that strikes me as odd with Amazon and the documentation on AWS is that there is no download all button, to make it easy to get all the documentation in one go. After creating a simple bash script that kept breaking and needed updating, I decided to rewrite in python to make it a little easier to maintain. You can download Documentation and/or WhitePapers. The script is now pported to Python3 (finally)!

I hope some of you find this useful.

## Requirements

Make sure all these python modules are installed as well as Python3:

 - argparse
 - beautifulsoup4
 - urllib3+
 - urlparse3
 - lxml

example:

```bash
sudo pip install -r requirements.txt
```

## Usage

To get all documents:

```
./getAWSdocs.py -d
```

Downloading all the docs (290 at the time of writting) can take a long time ~20mins.

To get all whitepapers:

```
./getAWSdocs.py -w
```

Files that exist on disk will not be re-downloaded (so by default only new sections/files are downloaded). To override this default and force re-download of files that exist on disk, use

```bash
./getAWSdocs.py -d -f
```

__Note:__ You can use a combination of -d and -w to download all documents at once.

Thats it!

Built by Ric: [@ric__harvey](https://twitter.com/ric__harvey)
