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
# script_calcule_age

```python 

import datetime
def age(date_aniv):
    date_aniv = datetime.strptime(datestr,"%d/%m/%Y").year
    date = datetime.datetime.now().year
    age = date - date_aniv
    return age

date_aniv = '01/04/1996'

print(age(date_aniv))

```
