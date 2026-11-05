---
layout: post
title: Graf rojstev
author: Janez Ignacij Jereb
date: 2026-11-1
tags: [grafi]
toc: false
highlight: WIP
---

## O čem se gre?

Pri predmetu Interaktivnost in oblikovanje informacij smo za domačo nalogo morali najti neko vizualizacijo in jo oceniti. Jaz sem izbral graf: ...

Ta graf prikazuje ... vendar ...

Ta vizualizacija me je dodatno navdihnila, da sem odločil, da poskušam narediti podoben prikaz s slovenskimi podatki. Tukaj bom prikazal (delno izmišljeno) pot do končnega prikaza:
...

## Zgodba prikaza podatkov

Podatke sem prenesel s [SURSA](...).
Začel sem tako, da sem podatke prikazal na grafu.
Vidi se podatke od leta .. do .. Vidimo, da se število rojstev povečevalo do ..., nakar se je trend obrnil in se spet zmanjšuje.

<a href="../images/graf-rojstev-imgs/img_1.png" class="glightbox">
  <img src="../images/graf-rojstev-imgs/img_1.png"
       alt="Graf rojstev"
       style="max-width: 100%;">
</a>

Naredimo še histogram podatkov, da vidimo njihovo porazdelitev.

<a href="../images/graf-rojstev-imgs/img_2.png" class="glightbox">
  <img src="../images/graf-rojstev-imgs/img_2.png"
       alt="Graf rojstev"
       style="max-width: 100%;">
</a>

Izgledajo normalno porazdeljeni s povprečjem ... in varianco ...

Glavni čar prvotne vizualizacije je bil prikaz sezonskosti rojstev. Zato bom izračunal povprečja in prikazal rojstva, glede na dan v letu.

Če poračunam povprečno število rojstev na dan dobim naslednji graf:

<a href="../images/graf-rojstev-imgs/img_3.png" class="glightbox">
  <img src="../images/graf-rojstev-imgs/img_3.png"
       alt="Graf rojstev"
       style="max-width: 100%;">
</a>

Ta graf jasno prikazuje "sinusodialno" sezonskost. 
Sedaj lahko vidimo, da je večino rojstev v ... To si najlažje razložimo tako da namesto, da bi gledali rojstva gledamo spočetja. Seveda spočetij ni v podatkih, zato jih interpoliramo s tem, da sinusoido zamaknemo za 9 mesecev levo. Bom tudi dopisal mesece spočetja, da je lažje slediti.

<a href="../images/graf-rojstev-imgs/img_4.png" class="glightbox">
  <img src="../images/graf-rojstev-imgs/img_4.png"
       alt="Graf rojstev"
       style="max-width: 100%;">
</a>

Zanimiva so odstopanja od trenda. Še posebej spodnje pike. Če narišemo praznike postane jasno, kaj je njihov razlog.

<a href="../images/graf-rojstev-imgs/img_5.png" class="glightbox">
  <img src="../images/graf-rojstev-imgs/img_5.png"
       alt="Graf rojstev"
       style="max-width: 100%;">
</a>

Če bolj podrobno pogledamo graf, lahko vidimo, da so nekje prisotne neke špice... okrog ...
Zato da lažje ocenimo, ali gre za dejanska odstopanja lahko odštejemo sinusoido in s tem dobimo
"desezonirane" podatke.

<a href="../images/graf-rojstev-imgs/img_6.png" class="glightbox">
  <img src="../images/graf-rojstev-imgs/img_6.png"
       alt="Graf rojstev"
       style="max-width: 100%;">
</a>

Dodatna potrditev za smiselnost sinusoide vidimo s tem, da se podatki na videz
porazdeljujejo normalno.

<a href="../images/graf-rojstev-imgs/img_7.png" class="glightbox">
  <img src="../images/graf-rojstev-imgs/img_7.png"
       alt="Graf rojstev"
       style="max-width: 100%;">
</a>

## Zaključek

S tem zaključimo zgodbo o tem grafu. Seveda, je še mnogo zanivih smeri, ki bi jih lahko ubrali (primerjava med leti, uporaba verjetnostnega programiranja, itd.) Upam, da je bila tako zanimiva za branje, kot je bilo meni pri preizkušanju grafa.
