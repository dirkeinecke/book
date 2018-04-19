# Einleitung

Willkommen bei *Die Programmiersprache Rust*, einem Einführungsbuch über Rust.

Die Programmiersprache Rust hilft Ihnen dabei, schnellere und zuverlässigere Software zu schreiben. Hohe Ergonomie und Low-Level-Kontrolle sind beim Sprachdesign von Programmiersprachen oft unvereinbar. Rust stellt sich dieser Herausforderung. Durch das Ausbalancieren von technischer Leistungsfähigkeit und einer großen Entwicklererfahrung bietet Ihnen Rust die Möglichkeit, Low-Level-Details (z. B. Speicherverbrauch) ohne große Schwierigkeiten zu kontrollieren. Eine solche Überwachung ist sonst nur mit großem Aufwand machbar.

## Die Zielgruppe von Rust

Rust ist für viele Menschen aus verschiedenen Gründen ideal. Schauen wir uns ein paar der wichtigsten Gruppen an.

### Entwicklerteams

Rust bietet sich als Werkzeug bei der Zusammenarbeit in großen Teams von Entwicklern mit unterschiedlichen Kenntnisstand in der Systemprogrammierung an. Low-Level-Code ist anfällig für eine Vielzahl von schleichenden Fehlern. Diese können in den meisten anderen Sprachen nur mithilfe ausgiebiger Tests und sorgfältiger Code-Reviews von erfahrenen Entwicklern gefunden werden. In Rust werden solche schwer zu fassenden Fehler (inklusive Fehler bzgl. der Nebenläufigkeit (Concurrency Bugs)) bereits durch den Compiler entdeckt und er weigert sich dann, den Code zu übersetzen. Durch die Verwendung eines solchen Compilers kann sich das Team stärker auf die eigentliche Programmlogik konzentrieren, anstatt Fehler zu suchen.

Rust bringt zudem die folgenden modernen Entwicklerwerkzeuge mit in die Welt der Systemprogrammierung:

* Cargo, der mitgelieferte Paket-Manager und zugleich Build-Tool,
  sorgt dafür, dass das Hinzufügen, Kompilieren und Verwalten von
  Abhängigkeiten im gesamten Ökosystem von Rust reibungslos und
  konsistent verläuft.
* Rustfmt sorgt für einen einheitlichen, entwicklerübergreifenden Programmierstil.
* Der Rust Language Server bietet Code-Vervollständigung und Inline-Fehlermeldungen
  in Integrated Development Environments (IDEs).

Durch den Einsatz dieser und anderer Tools im Ökosystem von Rust wird die Produktivität der Entwickler beim Schreiben von Code für die Systemebene sichergestellt.

### Studenten

Rust richtet sich an Studenten, die sich für Systemkonzepte interessieren. Durch den Einsatz von Rust haben bereits viele Menschen etwas über Themen wie die Entwicklung von Betriebssystemen gelernt. Die Gemeinschaft ist sehr offen und beantwortet gerne Fragen der Studenten. Das Rust-Team möchte mit Hilfen wie diesem Buch Systemkonzepte mehr Menschen zugänglich machen. Ganz besonders Neueinsteigern in der Welt des Programmierens.

### Unternehmen

Hunderte kleiner und großer Unternehmen setzen auf Rust bei einer Vielzahl von Aufgaben. Zu diesen gehören Kommandozeilen-Tools, Webservices, DevOps-Tools, Embedded Devices, Audio- und Videoanalyse und -transkodierung, Krypto-Währungen, Bioinformatik, Suchmaschinen, Internet der Dinge und maschinelles Lernen. Sogar große Teile des Firefox-Webbrowsers wurden in Rust geschrieben.

### Open-Source-Entwickler

Rust richtet sich auch an all diejenigen, die an der Programmiersprache Rust, an Entwicklerwerkzeugen und Bibliotheken mitarbeiten oder sich in der Community engagieren möchten. Wir würden uns freuen, wenn du mit dabei bist und auch etwas zu Rust beiträgst.

### Menschen, die Geschwindigkeit und Stabilität schätzen

Rust ist für all diejenigen, die sich Schnelligkeit und Stabilität in einer Programmiersprache wünschen. Mit Geschwindigkeit meinen wir auf der einen Seite die Ausführungsgeschwindigkeit der Programme, die du mit Rust erstellst und auf der anderen Seite die Zeit, die du zum Schreiben der Rust-Programme benötigst. Die Überprüfungen, die der Compiler von Rust durchführt, sorgen mit Feature-Ergänzungen und Refactoring für Stabilität. Andere Sprachen sind ohne diese Überprüfungen an dieser Stelle von wackeligen Code voller Altlasten gekennzeichnet. Solchen Code möchte kein Entwickler gern verändern. Neben kostenneutraler Abstraktion und der Kompilierung von High-Level-Features zu Low-Level-Code ist Rust immer bemüht, sicheren wie auch schnellen Code zu erzeugen.

An dieser Stelle haben wir nur einige der größten Interessengruppen genannt. Diese Liste ist natürlich nicht vollständig. Es gibt noch eine Vielzahl weiterer Gruppen und Bereich, in denen Rust versucht, allen hilfreich zur Seite zu stehen. Insgesamt ist Rust bemüht, die seit Jahrzehnten bestehenden Gegensätze und Kompromisse bestehend aus Sicherheit *und* Produktivität, Geschwindigkeit *und* Ergonomie aufzulösen. Probier Rust einfach mal aus und schau, ob diese Programmiersprache etwas für dich ist.

## Die Zielgruppe dieses Buches

In diesem Buch gehen wir davon aus, dass du bereits Code in einer anderen Programmiersprache geschrieben hast. Dabei ist es nicht so wichtig, welche Erfahrungen du mit anderen Programmiersprachen bereits gemacht hast oder aus welchem Bereich du kommst. Wir haben versucht, den Zugang zu Rust für alle möglichst einfach zu gestalten. Wenn du allerdings erst sehr wenige Erfahrungen oder noch gar keine Erfahrungen beim Programmieren gesammelt hast, dann empfehlen wir dir, zuvor ein Buch zu lesen, welches sich mit den Grundlagen des Programmierens im Allgemeinen beschäftigt. Darüber werden wir nämlich in diesem Buch nicht sprechen.

## How to Use This Book

In general, this book assumes that you’re reading it in sequence from front to
back. Later chapters build on concepts in earlier chapters, and earlier
chapters might not delve into details on a topic; we typically revisit the
topic in a later chapter.

You’ll find two kinds of chapters in this book: concept chapters and project
chapters. In concept chapters, you’ll learn about an aspect of Rust. In project
chapters, we’ll build small programs together, applying what you’ve learned so
far. Chapters 2, 12, and 20 are project chapters; the rest are concept chapters.

Additionally, Chapter 2 is a hands-on introduction to the Rust language. We’ll
cover concepts at a high level, and later chapters will provide additional
detail. If you want to get your hands dirty right away, Chapter 2 is the one
for that. At first, you might even want to skip Chapter 3, which covers Rust
features similar to other programming language features, and head straight to
Chapter 4 to learn about Rust’s ownership system. However, if you’re a
particularly meticulous learner who prefers to learn every detail before moving
onto the next, you might want to skip Chapter 2 and go straight to Chapter 3,
returning to Chapter 2 when you’d like to work on a project applying those
details.

Chapter 5 discusses structs and methods, and Chapter 6 covers enums, `match`
expressions, and the `if let` control flow construct. You’ll use structs and
enums to make custom types in Rust.

In Chapter 7, you’ll learn about Rust’s module system and about privacy rules
for organizing your code and its public Application Programming Interface
(API). Chapter 8 discusses some common collection data structures that the
standard library provides, such as vectors, strings, and hash maps. Chapter 9
explores Rust’s error handling philosophy and techniques.

Chapter 10 digs into generics, traits, and lifetimes, which give you the power
to define code that applies to multiple types. Chapter 11 is all about testing,
which is still necessary even with Rust’s safety guarantees to ensure your
program’s logic is correct. In Chapter 12, we’ll build our own implementation
of a subset of functionality from the `grep` command line tool that searches
for text within files. For this, we’ll use many of the concepts we discussed in
the previous chapters.

Chapter 13 explores closures and iterators: features of Rust that come from
functional programming languages. In Chapter 14, we’ll examine Cargo in more
depth and talk about best practices for sharing your libraries with others.
Chapter 15 discusses smart pointers that the standard library provides and the
traits that enable their functionality.

In Chapter 16, we’ll walk through different models of concurrent programming
and talk about how Rust helps you to program in multiple threads fearlessly.
Chapter 17 looks at how Rust idioms compare to object oriented programming
principles you might be familiar with.

Chapter 18 is a reference on patterns and pattern matching, which are powerful
ways of expressing ideas throughout Rust programs. Chapter 19 contains a
smorgasbord of advanced topics of interest, including unsafe Rust and more
about lifetimes, traits, types, functions, and closures.

In Chapter 20, we’ll complete a project in which we’ll implement a low-level
multithreaded web server!

Finally, some appendixes contain useful information about the language in a
more reference-like format. Appendix A covers Rust’s keywords. Appendix B
covers Rust’s operators and symbols. Appendix C covers derivable traits
provided by the standard library. Appendix D covers macros.

There is no wrong way to read this book: if you want to skip ahead, go for it!
You might have to jump back to earlier chapters if you experience any
confusion. But do whatever works for you.

An important part of the process of learning Rust is learning how to read the
error messages the compiler displays: these will guide you toward working code.
As such, we’ll provide many examples of code that don’t compile along with the
error message the compiler will show you in each situation. Know that if you
enter and run a random example, it may not compile! Make sure you read the
surrounding text to see whether the example you’re trying to run is meant to
error. In most situations, we’ll lead you to the correct version of any code
that doesn’t compile.

## Source Code

The source files from which this book is generated can be found on
[GitHub][book].

[book]: https://github.com/rust-lang/book/tree/master/second-edition/src
