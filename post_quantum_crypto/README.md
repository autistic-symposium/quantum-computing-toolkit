## quantum cryptography

<br>

### tl; dr

* almost all public-key cryptography right now could be broken with just a few advances in quantum computing
* the commonly-used public-key algorithms are based: factoring (rsa), finite field discrete logarithms (diffie-hellman), and elliptic curve discrete logarithms (ecdh and ecdsa) - the hidden subgroup problem, which quantum computers are good at solving
* modern design of post-quantum algorithms:
  - make constant-time implementations easy, reducing the risk of timing attacks
  - reduce reliance on random number generators (rngs) by extending nonce values with deterministic functions (shake)
  - implement random sampling techniques for non-uniform distributions, reducing the risk of attacks that rely on biased sampling
  - many are fully deterministic in their input reducing nonce reuse issues
  - many are designed to allow quick and easy generation of new keys, making it easier to provide forward secrecy

<br>

------

### shor's algorithm

<br>

* **[how quantum computers break encryption: shor's algorithm explained (video)](https://www.youtube.com/watch?v=lvTqbM5Dq4Q&t=160s)**
* **[when will a quantum computer running shor's algorithm be used to factor one of the rsa numbers for the first time?](https://www.metaculus.com/questions/3684/when-will-a-quantum-computer-running-shors-algorithm-or-a-similar-one-be-used-to-factor-one-of-the-rsa-numbers-for-the-first-time/)**

<br>

----

### nist post-quantum cryptography standardizations

<br>

#### general resources

<br>

* **[nist's pqc standardization process: second round candidate announcement](https://csrc.nist.gov/news/2019/pqc-standardization-process-2nd-round-candidates)**
* **[minimum quantum assumptions for cryptography workshop, simons institute](https://www.youtube.com/playlist?list=PLgKuh-lKre12DNtplRAQIwbJf_46HSMfB)**
* **[nist's transition to post-quantum cryptography standards, by d. moody et al. (nov/2024)](https://nvlpubs.nist.gov/nistpubs/ir/2024/NIST.IR.8547.ipd.pdf)**

<br>

#### bike

<br>

* **[bit flipping key encapsulation (BIKE)](https://bikesuite.org/)**

<br>

#### sike

* **[supersingular isogeny key encapsulation (SIKE)](https://sike.org/)**

<br>

---- 

### quantum key distribution (qkd)

<br>

* **[prototyping post-quantum and hybrid key exchange and authentication in TLS and SSH](https://openquantumsafe.org/papers/NISTPQC-CroPaqSte19.pdf)**
* **[uncloneable cryptography, by o. sattah](https://arxiv.org/pdf/2210.14265)** (review talking about quantum money and uncloneable forms of encryption)

<br>

----

### applications

<br>

* **[apple implements pq3 on imessage](https://security.apple.com/blog/imessage-pq3/)**
* **[signal implements x3dh (named pqxdh)](https://signal.org/blog/pqxdh/)**
