# :snake: py-serpent
# Informations
Implémentation de l'algorithme de chiffrement Serpent en python3, basé sur le travail de Frank Stajano<br>
Chiffrement de bloc de 128bits avec une clés de 256bits<br>
Fonctionnement possible en ECB, CBC, PCBC et CFB<br>
Hashage du mot de passe et du vecteur d'initialisation en pbkdf2_hmac sha256<br>
## <ins>Prérequis</ins>
- Python 3
- Module Python 3:
   - bitstring
<br>

# Traitement sur un texte en bytes
## <ins>_Electronic codebook (ECB)_</ins>
### Fonctionnement
<p align="center">
  <kbd>
  <img src="Image/ECB_Encrypt.png" title="ECB Encryt" border="5">
  </kbd>
  Chiffrement en ECB
</p>
<br>
<p align="center">
  <kbd>
  <img src="Image/ECB_Decrypt.png" title="ECB Decrypt" border="5">
  </kbd>
  Dechiffrement en ECB
</p>

### Chiffrement
```python
encrypted = serpent.encrypt_ECB(cleartext, password)
```
### Dechiffrement
```python
plain = serpent.decrypt_ECB(encrypted,password)
```
<br>

## <ins>_Cipher block chaining (CBC)_</ins>
### Fonctionnement
<p align="center">
  <kbd>
  <img src="Image/CBC_Encrypt.png" title="CBC Encryt" border="5">
  </kbd>
  Chiffrement en CBC
</p>
<br>
<p align="center">
  <kbd>
  <img src="Image/CBC_Decrypt.png" title="CBC Decrypt" border="5">
  </kbd>
  Dechiffrement en CBC
</p>

### Chiffrement
```python
encrypted = serpent.encrypt_CBC(cleartext, password)
```
### Dechiffrement
```python
plain = serpent.decrypt_CBC(encrypted, password)
```
<br>

## <ins>_Propagating cipher block chaining (PCBC)_</ins>
### Fonctionnement
<p align="center">
  <kbd>
  <img src="Image/PCBC_Encrypt.png" title="PCBC Encryt" border="5">
  </kbd>
  Chiffrement en PCBC
</p>
<br>
<p align="center">
  <kbd>
  <img src="Image/PCBC_Decrypt.png" title="PCBC Decrypt" border="5">
  </kbd>
  Dechiffrement en PCBC
</p>

### Chiffrement
```python
encrypted = serpent.encrypt_PCBC(cleartext, password)
```
### Dechiffrement
```python
plain = serpent.decrypt_PCBC(encrypted, password)
```
<br>

## <ins>_Cipher feedback (CFB)_</ins>
### Fonctionnement
<p align="center">
  <kbd>
  <img src="Image/CFB_Encrypt.png" title="CFB Encryt" border="5">
  </kbd>
  Chiffrement en CFB
</p>
<br>
<p align="center">
  <kbd>
  <img src="Image/CFB_Decrypt.png" title="CFB Decrypt" border="5">
  </kbd>
  Dechiffrement en CFB
</p>

### Chiffrement
```python
encrypted = serpent.encrypt_CFB(cleartext, password)
```
### Dechiffrement
```python
plain = serpent.decrypt_CFB(encrypted, password)
```
