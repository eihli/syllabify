# Syllabify


# Notes on syllabification

https://en.wikipedia.org/wiki/Syllable

> In the typical theory of syllable structure, the general structure of a syllable (σ) consists of three segments. These segments are grouped into two components:
>
> Onset (ω)
>     a consonant or consonant cluster, obligatory in some languages, optional or even restricted in others
> Rime (ρ)
>     right branch, contrasts with onset, splits into nucleus and coda
>
>     Nucleus (ν)
>         a vowel or syllabic consonant, obligatory in most languages
>     Coda (κ)
>         consonant, optional in some languages, highly restricted or prohibited in others

Also, for "ellipsis", /ps/ is not a legal internal coda in English. The /s/ can only occur as an appendix, e.g. the plural -s at the end of a word. So it should be e.lip.sis

http://www.glottopedia.org/index.php/Sonority_hierarchy

http://www.glottopedia.org/index.php/Maximal_Onset_Principle

## Nasal

Air flow goes through nose.

Examples: "n" in "nose", "m" in "may", "ŋ" in "funk".

"ŋ" is known as the letter "eng" and the technical name of the consonant is the "voiced velar nasal"

"voiced" in the above sentence refers to whether or not your vocal chords are active. Your voice chord doesn't vibrate with voiceless consonants, like "sh" "th" "p" "f". In contrast, notice the vibration in phonemes like "m" "r" "z".


## Ambisyllabism

![http://www.glottopedia.org/index.php/Ambisyllabic](http://www.glottopedia.org/index.php/Ambisyllabic)

A segment is ambisyllabic if it belongs to two syllables.

Example: 

The English word hammer cannot be divided into two syllables `ha` and `mer`; the [m] functions both as the final segment of the first syllable and as the initial consonant of the second syllable. 

This library doesn't syllabify words based on their letters. It syllabifies words based on their phonemes.

The two `m`'s in "hammer" are represented by a single phoneme, `M`. So, when it gets syllabified, the [m] only functions as an onset to the final rime. 

### Ambisyllabism TODO

Provide a function that inserts an extra phone where ambisyllabism occurs.


# Development

The initial skeleton of this library was generated from [https://github.com/seancorfield/clj-new](https://github.com/seancorfield/clj-new).

What follows is an unedited part of that skeleton. TODO: Update with syllabify-specific development documentation.

Invoke a library API function from the command-line:

    $ clojure -X com.owoga.syllabify/foo :a 1 :b '"two"'
    {:a 1, :b "two"} "Hello, World!"

Run the project's tests (they'll fail until you edit them):

    $ clojure -M:test:runner

Build a deployable jar of this library:

    $ clojure -X:jar

This will update the generated `pom.xml` file to keep the dependencies synchronized with
your `deps.edn` file. You can update the version (and SCM tag) information in the `pom.xml` using the
`:version` argument:

    $ clojure -X:jar :version '"1.2.3"'

Install it locally (requires the `pom.xml` file):

    $ clojure -X:install

Deploy it to Clojars -- needs `CLOJARS_USERNAME` and `CLOJARS_PASSWORD` environment
variables (requires the `pom.xml` file):

    $ clojure -X:deploy

Your library will be deployed to com.owoga/syllabify on clojars.org by default.

If you don't plan to install/deploy the library, you can remove the
`pom.xml` file but you will also need to remove `:sync-pom true` from the `deps.edn`
file (in the `:exec-args` for `depstar`).

## License

Copyright © 2021 Eihli

Distributed under the MIT License.
