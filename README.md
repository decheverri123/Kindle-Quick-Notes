# Kindle-Quick-Notes
Handy script to organize your Kindle highlights for export to a more centralized system (e.g. Evernote, OneNote)


## Description
Do you have a Kindle? Are you tired of the clunky highlights feature that's hard to keep on you at all times? This handy little script makes it easy to extract your kindle highlights from the Clipping.txt file that lives in your kindle. Your highlights will be decluttered with all the extraneous information that you don't need so you can upload them to your OneNote or Evernote for easy access.




# Kindle QuickLights

Very simple to use script. Make sure that the Clippings.txt text that comes in your kindle is in the directory where this notebook lives. Type in the name of the book you wish extract notes from and open up your newly created file with your new highlights in perfect form for transport to OneNote, Evernote, or any other note organization platform of your choosing.


```python
def Kindle(file, name):
    title = name
    sign = '=========='
    your = '- Your'
    g = open(file+" new", 'w')
    with open(file, 'r') as f:
        data = f.readlines()
        for line in data:
            if title in line or sign in line or your in line:
                continue;
            else:
                g.write(line)
```

Example:


```python
Kindle('Art.txt', 'The War of Art (Pressfield, Steven)')
```
