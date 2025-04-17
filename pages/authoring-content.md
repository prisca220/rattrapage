---
title: Authoring Content
menu:
  main:
    weight: 300
---
# Authoring Content in Markdown

Cecil supports [Markdown](https://cecil.app/documentation/content/#markdown) syntax in `.md` files as well as [front matter](https://cecil.app/documentation/content/#front-matter) to define variables.

**Table of content:**

[toc]

```markdown
[toc]
```

## Inline style

Text can be **bold**, _italic_, or ~~strikethrough~~.

```markdown
Text can be **bold**, _italic_, or ~~strikethrough~~.
```

You can [link to a page](/about.md) or [to another page](page:index).

```markdown
You can [link to a page](/about.md) or [to another page](page:index).
```

You can highlight `inline code` with backticks.

```markdown
You can highlight `inline code` with backticks.
```

## How to structure page

Cecil automatically use the page file name as title, but you can also define title and other variables in the [front matter](https://cecil.app/documentation/content/#front-matter).

You can structure content using a heading. Headings in Markdown are indicated by a number of `#` at the start of the line.

```markdown
---
title: Page title
description: Page short description.
---

# 🎓 Blog d'une étudiante de l'UAC Butembo

Salut ! Je m'appelle **[Ton Prénom]**, étudiante à l'**Université de l'Avenir du Congo (UAC)** à Butembo, en faculté d'Informatique de gestion. Ce blog est mon petit espace numérique où je partage mes découvertes, projets, et réflexions sur le monde de la tech 💻.

---

## 💡 Mes passions

Depuis que j'ai découvert l'informatique, je suis fascinée par :
- La programmation (surtout en Python et JavaScript 🐍✨)
- Les bases de données
- Le développement web
- L'intelligence artificielle (un jour, pourquoi pas ! 🤖)

---

## 🗓️ Derniers articles

👉 [Comment j'ai créé mon premier site avec Cecil](posts/cecil-debut.md)  
👉 [Pourquoi j'aime coder tard la nuit 🌙](posts/coder-la-nuit.md)  
👉 [Top 5 des outils gratuits pour les étudiants développeurs](posts/outils-etudiants.md)

---

## 📬 Me contacter

Une question ou une idée à partager ? Tu peux me retrouver :
- Par email : `ton.email@exemple.com`
- Ou sur GitHub : [@tonpseudo](https://github.com/tonpseudo)

---

> *"Rien ne vaut une ligne de code qui fonctionne."* — Moi, probablement à 3h du matin 😄

✅ Conseils supplémentaires
Tu peux créer les fichiers pour tes articles dans le dossier pages/posts/

Par exemple : pages/posts/cecil-debut.md, pages/posts/coder-la-nuit.md etc.

Et personnaliser les couleurs, le thème, et les images selon ton style.

## Image

Images use Cecil’s built-in optimized asset support.

![Cecil favicon](/favicon.png "Cecil favicon")

```markdown
![Cecil favicon](/favicon.png "Cecil favicon")
```

Cecil search images in `assets/` and `static/` folders, but relative path is also supported:

```markdown
![Cecil favicon](../assets/favicon.png "Cecil favicon")
```

## List

* Unordered list
* Unordered list
* Unordered list

1. Ordered list
2. Ordered list
3. Ordered list

* Level 1
  * Level 2
  * Level 2
    * Level 3
    * Level 3

## Blockquote

> This is a blockquote, which is commonly used when quoting another person or document.
>
> Blockquotes are indicated by a `>` at the start of each line.

```markdown
> This is a blockquote, which is commonly used when quoting another person or document.
>
> Blockquotes are indicated by a `>` at the start of each line.
```

## Code block

A code block is indicated by a block with three backticks ` ``` ` at the start and end. You can indicate the programming language being used after the opening backticks.

```php
// PHP code
$config = [
    'title'   => "My website",
    'baseurl' => 'http://localhost:8000/',
];

Builder::create($config)->build();
```

<pre>
```php
// PHP code
$config = [
    'title'   => "My website",
    'baseurl' => 'http://localhost:8000/',
];

Builder::create($config)->build();
```
</pre>

## There is a horizontal rule below this

---

## Definition list

First Term
: This is the definition of the first term.

Second Term
: This is one definition of the second term.
: This is another definition of the second term.

## Table

| Head 1       | Head 2            | Head 3 |
|:-------------|:------------------|:-------|
| ok           | good swedish fish | nice   |
| out of stock | good and plenty   | nice   |
| ok           | good `oreos`      | hmm    |
| ok           | good `zoute` drop | yumm   |

## Notes

:::
empty
:::

:::info
info
:::

:::tip
tip
:::

:::important
important
:::

:::warning
warning
:::

:::caution
caution
:::

```markdown
:::info|tip|important|warning|caution
Note here.
:::
```
