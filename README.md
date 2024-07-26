# LrLM
Low Resource Language Model using neural network base Deep learning Technique

This study explores the unique morphological structure of the Igbo language, focusing on the invariant nature of root words and their semantic enhancement through affixation. In Igbo, root words remain constant while their meanings are modulated by prefixes and suffixes, forming meaningful combinations that adhere to vowel-consonant-vowel patterns. Examples such as "Ngugu" (lungs) and phrases like "Gu-pu ya" (remove it) and "Go-zie" (bless) illustrate how roots and morphemes interact to convey different meanings.

Traditional language models, often based on subject-verb-object structures typical of English, fall short in accurately representing Igbo. Therefore, we propose a deep learning strategy using neural networks where vowels act as activators to capture these morphological patterns. This model leverages a shift-left approach and security-by-design principles to ensure robust performance and secure data handling.

Incorporating keyless encryption methods, which are resilient against quantum computing threats, guarantees the security and privacy of data, transactions, and communications within the model. The algorithm, reinforced by human feedback, forms a dynamic matrix that can represent any conceivable word or phrase in Igbo, significantly enhancing AI tasks such as translation, speech recognition, and text generation.

By leveraging this approach, we aim to bridge the gap in AI representation for low-resource languages, offering a pathway to more inclusive and culturally relevant AI applications. This work invites collaboration to harness Igbo’s linguistic richness for advanced AI development while ensuring security and privacy in the post-quantum era.

### The three main deliverables:
1. Build a Low resource foundational language model using neural network deep learning techniques
2. Train the models using ML (supervise, unsupervised, and reinforce learning with human feedback (RLHF).
3. Generate sentences and compare them with known datasets for semantic reason. 


## Neural Network:

As a native speaker of Igbo. We  would build a giant matrix of words. This is to help you understand how words form from Igbo romanized alphabets. These are considered foundational vocabulary in my native language. 
Let's start with the native romanized alphabets: 
A B CH D E F G GB GH GW H I Ị J K KP KW L M N Ṅ NW NY O Ọ P R S SH T U Ụ V W Y Z. 
8 of these alphabets makes up what is known as vowels.-  A E I Ị O Ọ U Ụ. 

The rest are 28 known as consonants and diacritics.-B CH D F G GB GH GW H J K KP KW L M N Ṅ NW NY P R S SH T V W Y Z. 

There are in the last group 2 pseudo vowels M and N.

With the above insight we can now create an exhaustive list of values arranged in a matrix following the algorithm below: These are some of the consonants: B CH D F G GB GH GW H J K KP KW L M N Ṅ NW NY P R S SH T V W Y Z

(1). Using vowels as prefixes concatenate them with the consonants 
aB, aCH, aD, aF, aG, aGB, aGH, aGW, aH, aJ, aK, aKP, aKW, aL, aM, aN, aṄ, aNW, aNY, aP, aR, aS, aSH, aT, aV, aW, aY, aZ .
Continue iteration with other vowels.


(2). Using vowels as suffixes concatenate them with consonants. 
Ba, CHa, Da, Fa, Ga, GBa, GHa, GWa, Ha, Ja, Ka, KPa, KWa, La, Ma, Na, Ṅa, NWa, NYa, Pa, Ra, Sa, SHa, Ta, Va, Wa, Ya, Za .
Continue iteration with other vowels.

You can combine 1 and 2 to get the same result as in 6. 

(3). Concatenate the vowels against vowels. By default vowels start most sentences in Igbo. There are cases when they are used as interjections and they could recur. 
Aa, ee, ii, etc, 
(4). Identify all bigrams and trigrams there are. 
Ba, da, fa, ga, 
Cha, Gba, The, Gwa, …
(5) Identify the root words (bigram and trigram) as they do not change in meaning but vary based on the vowel's position.  When the vowel is in the front of the consonant they mean one thing and when the vowel is at the back they mean another. 

 

(6). Create vowel - consonant- vowel word formation with these root words in the last step show the possible combinations there are with vowels on the front as they are assuming all combinations are considered. E.g Aba, acha, Ada, Afa, Aga, etc…. Include pseudo- vowels in this prefix from root iterations in step (5).
. 
(7). With these words you have, combine or concatenate the words.
Aba acha, Aba ada, Aba Afa, etc….

(8). Form short sentences by combining vowels alone and the words you created to give a short sentence. E.g o  Aba acha, o Aba ada, o Aba Afa, etc., a word must be activated by a vowel to create intelligent strings.


(9). Combine those short sentences for longer sentences. 

(10). We will then supply you with datasets of the language to see how well you have done. 

This is how to build a giant neural network from which the words will only be activated if they follow the right order vowel-consonant-vowel. In iterations the sample will show the possible permutations and combinations. 

Congo-kwa languages exhibit this order of formation. Their meanings are in those words. 

## Implementation steps:
Application of the proposed algorithm:

Classification

Upper case	
A	B	CH	D	E	F	G	GB	GH	GW	H	I	Ị	J	K	KP	KW	L	M	N	Ṅ	NW	NY	O	Ọ	P	R	S	SH	T	U	Ụ	V	W	Y	Z

Lowercase	
a	b	ch	d	e	f	g	gb	gh	gw	h	i	ị	j	k	kp	kw	l	m	n	ṅ	nw	ny	o	ọ	p	r	s	sh	t	u	ụ	v	w	y	z

Unigram
a, b, d, e, f, g, m, n, o, ọ, p, r, s, t, y, z, 

Bigrams

                                            Ja,                      na,
bi, ch, di, fi, gb, gh, gi,  gw,  ji,  ki, kp, kw, mi, ni, nw, ny, oo, ri, si, so, ti, sh, yi, zi, 

                                  —->   jo

                                 —-->  ju
The goal is to arrive at all possible bigrams.If possible as a part of text-to-speech tag and vice-versa.. 

Trigrams
bia, chi, die, fio, gbu, gha, gii,  gwu, jie, kia, kpa, kwa, mia, nia, nwa, nye, ooo, rie, sie, tie, shi, yie, zie, 

The goal is to arrive at all possible trigrams.If possible as a part of text-to-speech tag and vice- versa. 
Vowels 
A E I Ị O Ọ U Ụ
a e i ị o ọ u ụ

Create short sentences (organic syntax synthesis by sub-words)

I di na ya / nia

I so ni-a/na ya

Ani/ala/ali oma

Nwa oma

Obi ojo

Ndi si njo 

O-di nma

Create longer sentences (organic syntax synthesis by concatenation)

Nwa oma ani/ala oma

Ndi si na njo di nma

Obi ojo, Idi nia/naya

Nwa oma obi ojo

O-di nma na I so nia/na ya


Other data sets or  corpus (larger collections):
-Ogam dictionary
-Regular dictionary
-Afa Lexicon
-Igboapi.com

Tokenization: 

You can break the large corpus down again to sub words and then to numbers in order to facilitate ML an MT. I will be using the example below for clarity of the non-repeating nature of tokens.

O-di nma na I so ni-a/na ya

['O-di', 'nma', 'na', 'I', 'so', 'ni-a', '/', 'na', 'ya']

Token to number mapping:
{'I': 0, 'so': 1, 'ya': 2, 'ni-a': 3, 'nma': 4, '/': 5, 'O-di': 6, 'na': 7}

Converted numbers:
[6, 4, 7, 0, 1, 3, 5, 7, 2]


Stemming:

The idea is to engage some mechanism better described as vowel suffix or prefix to root linking to reinforce words bases and meaning. .
                                 o-gb, a-gh, gi-a       gw-a, 
a-bi, ch-e, a-di, e-fi, gb-o,  gh-a, a-gi,   a-gw,  ji,  ki, kp, kw, mi, ni, nw, ny, oo, ri, si, 

              sh-o           a-zi
aso, oti, o-sh,  oyi,   zi-a,

Tagging:

—Make the word corresponding to a particular part of Igbo speech tagging 
Conjugation of verbs e.g je     to walk/go
                                        ga    to walk/go
                                        gọ    to harness 
                         
Je ->ije-> eje -> na-eje  
Ga -> iga -> aga ->  na a-ga -> ọ-ga-la  
Gọ -> igọ -> agọ-> na a-gọ   -> ọ-gọ-la

*******************************************
Go ->  going -> is going -> gone     *
Lọ -> lati lọ  -> m lọ | n lọ   -> lọ      *
*******************************************
Looking at this you can notice that there are already similarities in Yoruba language. 

Parsing:

—It must be expanded to the English grammar part of speech (NAVAPCIP) structure. 
Noun – Tom lives in New York.
Pronoun – Did she find the book she was looking for?
Verb – I reached home.
Adverb – The tea is too hot.
Adjective – The movie was amazing.
Preposition – The candle was kept under the table.
Conjunction – I was at home all day, but I am feeling very tired.
Interjection – Oh! I forgot to turn off the stove.
Which in other languages can be expanded in the specific speech structure. E.g 

Oooo, e-che-kwa-m na i-je-re ma-na ha si na i-bu nwa o-ma o-bi o-jo na ina ejeka.

N we-lu si ke-du e-be i-na e-je-gi?

Semantic Reasoning Functionalities:

This should be the last stage:You create inference rules to infer new facts from the existing for human understanding. 

“ Nwa oma obi ọjo kedu ebe ina e jegi?“

This is semantic artificial intelligence: Adding context, knowledge, and valuable insight into the data set supplied earlier. With reinforcement learning and human feedback we can easily speedup low resource languages into wider application of artificial intelligence for the most part. 


Conclusion
This approach significantly cuts the cost of training and removes the use of synthetic data completely.
It relies more on the root words as they exist in nature; building a symphony by using the roots as notes and chords to create sentences or musical sounds. This also presents a comprehensive framework for advancing data security through the convergence of AI, cryptography, and language modeling. By leveraging innovative technologies and redefining traditional paradigms, we aim to empower organizations and individuals to safeguard their data in an increasingly interconnected and digitized world.


