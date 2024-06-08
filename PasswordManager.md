
# Secret Manager Needed

---

> [!CAUTION]  
> eval() is an [unsafe command](https://www.codiga.io/blog/python-eval/) with literal_eval() being one workaround

```
class Pers:
  def __init__(self,msg):
    self.secret = msg
  def tell(self, hidden):
    print(hidden)
    return "told"

  pers1 = Pers("Rot26 is the best")
  pers2 = Pers("Rot13 is the best")
  my = Pers("Rot39 is the best")

gossip = my.secret

def duh (pers1,pers2):
  if eval("pers1.tell(pers2.secret)") == "told":
    pers1.tell(gossip)

duh(pers1,pers2)
```

## Key-Considerations: Security and Ease of Use
**Past Experience:** Lastpass and KeePass\
**Thoughts:** Local > Cloud for security\
**Potential Issues:** Recoverability potential issues.

### KeePassXC
KeePassXC cross platform, good security and known experience (+Ease of Use +Security)

### BitWarden
Would be fun project (+Learning -Time)

**Selection: KeePassXC**

#### Optional:
`sudo apt search KeepassXC`
`sudo apt show KeepassXC`
#### Non-Optional:
`sudo apt install KeePassXC`

## Bonus Features
TOTP QR Code Integration w/ QR Generation
