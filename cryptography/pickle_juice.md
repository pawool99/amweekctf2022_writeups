# Pickle juice
## 100 points
### "We managed to intercept communication between **pr0phet** and his hacker friends. However it is obfuscated using something. We just can't figure out what it is. Maybe you can help us find the flag?"

This challange contains a `data` file which holds a pickled (serialized) python object. To solve the challangewe need to unpickle the object, using the `pickle.load(file, *, fix_imports=True, encoding='ASCII', errors='strict')` method.

Example script:
```
import pickle
pickle_in = open("data", "rb")
data = pickle.load(pickle_in)
flag = "AM{"
for i in range(4,23):
    flag += chr(data[i])
flag += "}"
print(flag)
```

Flag: `AM{p1ckl3_y0uR_m3554g3}`