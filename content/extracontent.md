---
title: Extra Content
featured_image: '/images/cd.jpg'
omit_header_text: true
description: More definitions
type: page
menu: main
weight: 4

---


The **new definitions** on this page extend those already in [Crypto
Dictionary](https://nostarch.com/crypto-dictionary), and might appear in
future versions of the book.

This is work in progress. New definitions will appear regularly. 



## Ate pairing

The most efficient elliptic-curve pairing known.
Ate pairings are thus often used in practice, for example within BLS
signatures over BLS curves.

See *BLS (Barreto-Lynn-Scott) curves*, *BLS (Boneh-Lynn-Shacham)
signatures*, *Pairing*.

Online:

* <https://www.esat.kuleuven.be/cosic/publications/talk-73.pdf>


## Avalanche

Or avalanche effect, the quite archaic criteria that in a block cipher
or hash function all input bits should affect all output bits.
Like diffusion, this is less about cryptographic strength than
statistical randomness.


## BLS (Barreto-Lynn-Scott) curves

Elliptic curves created to make pairing operations secure and efficient,
due to the certain properties of the curve.
Such curves must have a subgroup with a high enough, yet
not enormous *embedding degree*, for pairings be efficiently computable.

BLS curves were designed with the Tate pairing in mind, but can also be
used to compute (optimal) Ate pairings, introduced six years after BLS
curves.

BLS curves have for example been used in zk-SNARK constructions, and in
BLS signatures, whose BLS is a different author set than that of the
curves.

See *Ate pairing*, *Pairing*.

Online:

* <https://eprint.iacr.org/2002/088.pdf>
* <https://tools.ietf.org/id/draft-yonezawa-pairing-friendly-curves-00.html>

## BLS12-381 

The most common BLS curve used in practice. 12 is the embedding degree
(and the degree of field extension), and 381 is the bit
size of the underlying finite field.

BLS12-381 was designed by the Zcash team, and has the simple equation
y<sup>2</sup> = x<sup>3</sup> + 4.
It initially targetted a security level of 128 bits, but was later
estimated to offer less than 120 bits of security.

Besides Zcash, BLS12-381 is used in other projects' zero-knowledge
proofs as well as in some BLS signatures, such as those of Ethereum 2.0.

See *Pairing-based cryptography*.

Online:

* <https://electriccoin.co/blog/new-snark-curve/>


## Confusion

## Covert channel

## Cryptozoology

## DeFi

*De*centralized *F*raud on *i*nternet.


## Diffusion




## Distributed password-authenticated symmetric key encryption (DPaSE)




## Eth2

Ethereum 2.0, the 3-phase evolution of Ethereum towards a more scalable
platform, with

* Proof-of-stake instead of proof-of-work, eliminating the energy
  hungriness of the network.

* Chain sharding, which splits the blockchain into smaller chains that
  work in parallel to process transactions more efficiently.

* A new virtual machine using a variant of WebAssembly, allowing
  smart contracts to be coded in languages such as JavaScript and Rust.


## Fortuna

A pseudorandom generator that was notably used in Microsoft
Windows and later in macOS.
Fortuna includes entropy pools and a reseed mechanism to provide
post-compromise security before the term "post-compromise security"
existed.

Online:

* <https://support.apple.com/en-ie/guide/security/seca0c73a75b/1/web/1>


See *Yarrow*.

## Galois

French Mathematician Évariste Galois died in a gun duel at the age of 20, in 1832, after pioneering the study of finite fields.
The night before the duel he wrote a long letter to a friend about his
latest research, concluding by asking his friend to ask "Jacobi or
Gauss" their opinion and concluded «il y aura, j'espère, des gens qui
trouveront leur profit à déchiffrer tout ce gâchis.»


## Key commitment 



## Nym server

Short for pseudonymous remailer server.  
Nym servers serve to send pseudonymous email by relaying email messages
stripped off headers to hide the initial sender, and including an
identifier called a nym identity, along with a signature from that
identity.  
Emails are encrypted between remailers, and reach their final recipient
in clear or encrypted, but always signed by the pseudonymous identity.

Online:

* <https://pdos.csail.mit.edu/papers/nymserver:ccs5.pdf>

## PASS (password-authenticated secret sharing) 



## SexTNFS (special extender tower NFS)

A variant of the number field sieve (NFS) algorithm to compute discrete
logarithms, found to reduce the security level of
Barreto--Naehrig (BN) curves from approximately 128 to 110 bits.
This observation prompted the Zcash project to switch to another curve,
BLS12-381, whose estimated 128-bit security level was later slightly
downgraded as well.

See *BLS (Barreto-Lynn-Scott) curves*.


## SPHINX 


## Template attack


## Tezos

Blockchain with a funny smart contract language (Michelson), and a lot
of Ocaml.


## Verifiable timed signature



## Yarrow

A pseudorandom generator that was notably used in Apple's OSX/macOS
until Apple replaced it by its successor Fortuna.

> Yarrow is a owering perennial with distintive at ower heads and lay leaves, like Queen Anne's Lae or wild arrot. Yarrow stalks have been used for divination in China sine the Hsia dynasty, in the seond millennium B.C.E. The fortuneteller would divide a set of 50 stalks into piles, then repeatedly use modulo arithmetic to generate two bits of random information (but with a nonuniform distribution) 

See *Fortuna*.

Online:

* <https://www.schneier.com/wp-content/uploads/2016/02/paper-yarrow.pdf>

