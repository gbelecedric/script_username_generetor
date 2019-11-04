# script_username_generetor
```python 

import codecs 
import uuid 


def generateUsername(nom,prenom):
    username = ""
    if (len(nom) > 1 or len(prenom) > 1):
        first_letter_nom = nom[:1] 
        first_letter_prenom = prenom[:1]
        key = uuid.uuid4().hex[:3].upper() 
        print(key)
        code = first_letter_nom.upper() + first_letter_prenom.upper() + key 
        code = codecs.encode(code, 'rot_13') 
        username = ("Nan3.20_" + code) 
       
        
    return username

print(generateUsername('gbele','hans'))

```
