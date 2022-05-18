# Tasty
## 150 points
### "Well, pr0phet is a fussy eater and is only willing to eat chocolate cookies. Any other flavour and he throws a tantrum."
### "http://ctf.az.am-isd.com:9999/"

Once we access the link we see the following page:

![image](static/1.png)

The title and text are a hint for checking the cookis of this session:

![image](static/2.png)

We can change the value of `flavour` to the value of base64(chocolate) like this:

![image](static/3.png)

After a new request(refresh), we get the following page:

![image](static/4.png)

Flag: `AM{T4sty_c00kiez}`