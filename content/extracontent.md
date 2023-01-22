---
title: Extra Content
omit_header_text: false
description: More definitions
type: page
menu: main
weight: 4

---


The **new definitions** on this page extend those already in [Crypto
Dictionary](https://nostarch.com/crypto-dictionary), and might appear in
future versions of the book.

This is work in progress. New definitions will appear regularly. 

(For their help, thanks to: Antony Vennard, Peter Gutmann.)

## 0

ePrint crasher.

Online:

* <https://eprint.iacr.org/2021/323>

## אתבש

Like Noekeon and ROT13, an involution.
About as secure as the latter.
Pronounced "atbash".


## API

Cryptographic APIs have often been confusing and error-prone for
cryptographers, and impenetrable for mere mortals.
The situation considerably improved since the 2010s, thanks to libraries
such as NaCl (and its sister Sodium) and built-in language APIs such as
that of Go.


## ARLEAS

Abuse resistant lawful enforcement access systems, or lawful
interception that cryptographers might live with, thanks to lossy
encryption, zero-knowledge proofs, and a global immutable ledger.

The paper formalizing ARLEAS demonstrates that "cryptographic
implausibility" of retrospective abuse-resistant interception, or access
to communication content that predates a warrant's issuance. 
It's because this would require that all participants be at
any time potentially subject to interception.

Online:

* <https://eprint.iacr.org/2021/321>


## Ate pairing

The most efficient elliptic-curve pairing known.
Ate pairings are thus often used in practice, for example within BLS
signatures over BLS curves.

See *BLS (Barreto-Lynn-Scott) curves*, *BLS (Boneh-Lynn-Shacham)
signatures*, *Pairing*.

Online:

* <https://eprint.iacr.org/2006/110.pdf>
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

Cryptographically strong propagation of changes from an input throughout
the computation of a hash function's or block cipher's rounds.
If changes in (say) a given input bit don't affect some given output
bit, or if they do only with some statistical bias, then the algorithm
doesn't behave randomly and can be attacked by differential
cryptanalysis techniques.

Stacking confusion layers may never lead to a secure cipher if they
can't bring diffusion across all the state's bits.
For example, if AES only had S-boxes—the confusion-heavy
<code>SubBytes</code> operation)—a change in any Nth input byte would
only affect the Nth output byte.
Likewise, AES without <code>ShiftRows</code>—but with all other layers
including the column-wise diffusion layer <code>MixColumns</code>—then
differences would never propagate across rows of AES's 4×4-byte square
state.

See *Diffusion*.


## Covert channel

Surreptitious transmission of information through a channel not intended
to transfer information of that sort or in that way, in order to evade
detection or analysis. Classes of covert channels include

* Storage channels, such as hiding data in innocuous-looking usage of
  some network protocol (DNS is a popular choice), steganography
  techniques, or social media services.

* Timing channels, when for example a system's response time is use to
  signal some information.

* Behavior channels, where behavior patterns encode some information.
  Port knocking can be seen as such a covert channel.

Covert channels aren't much about cryptography. They don't hide the
communication content but the fact that communication happens at all.
They're thus useful in data exfiltration and communication between illegal
network operatives, for example.

Online:

* <https://fas.org/irp/nsa/rainbow/tg030.htm>

## C.R.E.A.M.

Crypto rules everything around me.

Online:

* <https://www.youtube.com/watch?v=zhUnEg0he4A>


## Cryptozoology

Prefixing some word with "crypto" doesn't make it legitimate.


## DeFi

*De*centralized *F*raud on *i*nternet.


## Diffusion

Broad but cryptographically shallow propagation of changes from an input
throughout the computation of a hash function's or block cipher's
rounds.

See *Confusion*.


## Distributed password-authenticated symmetric key encryption (DPaSE)

Protocol involving multiple servers to allow a user to encrypt and
decrypt data with keys derived from a single password in a way that
prevents offline password guessing hides plaintext and ciphertext from
the servers.
There is an additional operational cost to run the associated
infrastructure and mitigate DoS risks.

## EAP

The turducken of authentication protocols.

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

## HopMAC

A member from the Keccak family missing from our first edition's
inventory. HopMAC is to KangrarooTwelve (K12) what HMAC is to SHA-2: a MAC
construction from a hash function, which does <code>HopMAC(K, M, C) =
K12(K, K12(M, C))</code>, where the inner K12 call returns a 256-bit hash
and the outer returns an arbitrary length hash. The parameter
<code>C</code> is a "customization string", supported as a second argument
of K12.


## Key commitment 

The property of authenticated encryption that a ciphertext requires the
correct key to decrypt to a valid plaintext.

Online:

* <https://eprint.iacr.org/2020/1456.pdf>

## Military grade

Cryptography marketed as military grade is often to crypto what military
music is to music.


## Miller loop

The core algorithm of elliptic curve pairings used in crypto (Ate, Eta,
Tate, Weil).

Online:

* <https://crypto.stanford.edu/miller/>


## MOV attack

A technique to solve a seemingly hard elliptic-curve discrete logarithm
problem by solving a discrete logarithm in an integer multiplicative
group and translating the solution back to elliptic-curve land.

This only works for certain curves (the *supersingular* ones).

The "MOV" abbreviation is from the authors' names.

Online:

* <https://www.dima.unige.it/~morafe/MaterialeCTC/p80-menezes.pdf>


## Multi-signature

Collective signature schemes often implemented on-chain (typically via
Bitcoin scripts, or smart contracts), whose difference with threshold
signatures is that they reveal the identities of individual signers. 

## Nonrepudiation 

A legal-sounding term invented by standards group members without
consultation with lawyers to describe a service that crypto can't
provide.  X.509 eventually replaced it with "content commitment", but by
then the damage had been done.

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

## Pedersen commitment

A commitment scheme based on a hash function using algebraic operations
rather than bits-mixing operations like most hash functions. 
Thanks to the algebraic structure of the hash, it can be used to create
commitment schemes that are additively homomorphic, and provably secure
(perfectly hiding, and computationally binding under the discrete
logarithm assumption).


## Poseidon

A hash function that is zero-knowledge proof-friendly, thanks to its
compact representation as a circuit.


## Proof of possession

Part of a protocol that requires knowledge of secret key (KOSK) evidence
in order to be secure. The actual proof of possession is typically as
simple as a signature. Less sensible proofs of possession include
sending your private key to the other party. CMP, the Certificate
Mismanagement Protocol, actually does this, or at least provides for it
in the protocol.

## Proof of proof of work

A technique to verify proof-of-work chains of blocks with sublinear
complexity in the length of the chain.

Online:

* <http://fc16.ifca.ai/bitcoin/papers/KLS16.pdf>


## Proof of publication

Advanced hashing. Something to request grant money.


## PSS (probabilistic signature scheme)

Signature scheme designed to develop randomized, provably-secure RSA
signatures, standardized in PKCS#1 v2.1.
But RSA-PSS is about as secure as the simplistic deterministic full
domain hash (RSA-FDH), even when PSS is not randomized.


## ROT13

Military-grade encryption, if you live in the year 60 BC.


## SexTNFS (special extender tower NFS)

A variant of the number field sieve (NFS) algorithm to compute discrete
logarithms, found to reduce the security level of
Barreto--Naehrig (BN) curves from approximately 128 to 110 bits.
This observation prompted the Zcash project to switch to another curve,
BLS12-381, whose estimated 128-bit security level was later slightly
downgraded as well.

See *BLS (Barreto-Lynn-Scott) curves*.


## Shamir's law

Crypto is bypassed, not penetrated.

Full Shamir quote: "Cryptography is usually bypassed. I am not aware of
any major world-class security system employing cryptography in which
the hackers penetrated the system by actually going through the
cryptanalysis [...] usually there are much simpler ways of penetrating
the security system".


## SPHINX 

A message format designed to be used in mixnet-based anonymity networks,
with provable security guarantees (in the random oracle model).

Online:

* <https://www.freehaven.net/anonbib/cache/DBLP:conf/sp/DanezisG09.pdf>


## Template attack

A class of power analysis attacks where the attacker can first play with
the attacked device, controlling all values including secret keys, in
order to built a statistical model of the correlations between values
and measurements.
The actual attack then leverages this model, or template, to extract
information from physical measurements.


## Tezos

Blockchain with a funny smart contract language (Michelson), and a lot
of Ocaml.


## Verifiable timed signature

Signatures that can't be verified before a certain amount of time.
Introducing a notion of time to a blockchain (with essentially only
block indexes a a clock) can help create better blockchain-based payment
channels and safer multi-party computation protocols for on-chain
applications.

Online:

* <https://eprint.iacr.org/2020/1563.pdf>

## Yarrow

A pseudorandom generator that was notably used in Apple's OSX/macOS
until Apple replaced it by its successor Fortuna.

> Yarrow is a owering perennial with distinctive at flower heads and lay
leaves, like Queen Anne's Lae or wild arrot. Yarrow stalks have been
used for divination in China sine the Hsia dynasty, in the seond
millennium B.C.E. The fortuneteller would divide a set of 50 stalks into
piles, then repeatedly use modulo arithmetic to generate two bits of
random information (but with a nonuniform distribution) 

See *Fortuna*.

Online:

* <https://www.schneier.com/wp-content/uploads/2016/02/paper-yarrow.pdf>


## ZK-Rollup

Class of layer-2 protocols over blockchains that use zk-SNARKs to create
validity proofs recorded on the blockchain, while keeping the actual
computation off-chain, yet data on-chain.
The rollups that don't use zk-SNARKs are Optimistic Rollups and use a
different validation mechanism.
Rollups that store data on-chain are usually not called rollups, but
"plasma" or "validia" protocols.

Online:

* <https://ethereum.org/en/developers/docs/layer-2-scaling/>
* <https://l2beat.com/>
* <https://medium.com/starkware/validity-proofs-vs-fraud-proofs-strike-back-4d0bf90eed15>
