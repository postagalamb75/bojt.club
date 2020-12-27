+++
author = "Hugo Authors"
title ="Markdown szintaxis útmutató"
date = "2019-03-11"
description = "Ez a cikk bemutatja az alapvető Markdown szintaxist és a HTML elemek formázását."
tags = [
    "markdown",
    "css",
    "html",
]
categories = [
    "themes",
    "syntax",
]
series = ["Themes Guide"]
aliases = ["migrate-from-jekyl"]
+++

Ez a cikk bemutatja a Hugo tartalomfájlokban használható alapvető Markdown szintaxis elemeit, valamint az alapvető HTML elemek CSS formázásait egy Hugo Theme-ben.
<!--more-->

## Címsorok (Headings)

Az alábbi HTML `<h1>`—`<h6>` elemek hat szintű szekció címsorokat reprezentálnak. `<h1>` a legmagasabb szekció szint míg `<h6>` a legalacsonyabb szint.

# H1
## H2
### H3
#### H4
##### H5
###### H6

## Paragrafus (Paragraph)

Xerum, quo qui aut unt expliquam qui dolut labo. Aque venitatiusda cum, voluptionse latur sitiae dolessi aut parist aut dollo enim qui voluptate ma dolestendit peritin re plis aut quas inctum laceat est volestemque commosa as cus endigna tectur, offic to cor sequas etum rerum idem sintibus eiur? Quianimin porecus evelectur, cum que nis nust voloribus ratem aut omnimi, sitatur? Quiatem. Nam, omnis sum am facea corem alique molestrunt et eos evelece arcillit ut aut eos eos nus, sin conecerem erum fuga. Ri oditatquam, ad quibus unda veliamenimin cusam et facea ipsamus es exerum sitate dolores editium rerore eost, temped molorro ratiae volorro te reribus dolorer sperchicium faceata tiustia prat.

Itatur? Quiatae cullecum rem ent aut odis in re eossequodi nonsequ idebis ne sapicia is sinveli squiatum, core et que aut hariosam ex eat.

## Idézetblokkok (Blockquotes)

Az idézetblokk elem egy olyan tartalmat reprezentál amelynek forrása külső, opcionálisan az idézés lehet „lábjegyzet” (`footer`) vagy „idézet” (`cite`) elemen belül, illetve lehetnek soron belüli változtatások, például kommentárok és rövidítések.

#### Idézetblokkok hivatkozás nélkül (Blockquote without attribution)

> Tiam, ad mint andaepu dandae nostion secatur sequo quae.
> **Megjegyzés**, *Markdown szintaxis* egy idézetblokkon belül is használható.

#### Idézetblokkok hivatkozással (Blockquote with attribution)

> Don't communicate by sharing memory, share memory by communicating.<br>
> — <cite>Rob Pike[^1]</cite>

[^1]: The above quote is excerpted from Rob Pike's [talk](https://www.youtube.com/watch?v=PAAkCSZUG1c) during Gopherfest, November 18, 2015.

## Táblázatok (Tables)

A táblázatokat nem tartalamzza a Markdown eredeti specifikációja, de a Hugo már alapból támogatja őket.

Név | Életkor
:--- |---:
Bob | 27
Alice | 23
Lizi | 19

#### Táblázaton belüli jelölé alakamazása (Inline Markdown within tables)

| Italics   | Bold     | Code   |
| --------  | -------- | ------ |
| *italics* | **bold** | `code` |

## Kódblokkok (Code Blocks)

#### Kódblokk ` backtickkel (Code block with backticks)

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Example HTML5 Document</title>
</head>
<body>
  <p>Test</p>
</body>
</html>
```

#### Kódblokk négy szóközzel behúzva (Code block indented with four spaces)

    <!doctype html>
    <html lang="en">
    <head>
      <meta charset="utf-8">
      <title>Example HTML5 Document</title>
    </head>
    <body>
      <p>Test</p>
    </body>
    </html>

#### Kódblokk Hugo Shortcode-val (Code block with Hugo's internal highlight shortcode)
{{< highlight html >}}
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Example HTML5 Document</title>
</head>
<body>
  <p>Test</p>
</body>
</html>
{{< /highlight >}}

## Listatipusok (List Types)

#### Rendezett lista (Ordered List)

1. First item
2. Second item
3. Third item

#### Rendezettlen lista (Unordered List)

* List item
* Another item
* And another item

#### Beágyazott lista (Nested list)

* Fruit
  * Apple
  * Orange
  * Banana
* Dairy
  * Milk
  * Cheese

## Egyéb elemek — abbr, sub, sup, kbd, mark

    <abbr title="Graphics Interchange Format">GIF</abbr> is a bitmap image format.
<abbr title="Graphics Interchange Format">GIF</abbr> is a bitmap image format.
***
    H<sub>2</sub>O
H<sub>2</sub>O
***
    X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>
X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>
***
    Press <kbd><kbd>CTRL</kbd>+<kbd>ALT</kbd>+<kbd>Delete</kbd></kbd> to end the session.
Press <kbd><kbd>CTRL</kbd>+<kbd>ALT</kbd>+<kbd>Delete</kbd></kbd> to end the session.
***
    Most <mark>salamanders</mark> are nocturnal, and hunt for insects,
    worms, and other small creatures.
Most <mark>salamanders</mark> are nocturnal, and hunt for insects, 
worms, and other small creatures.
***