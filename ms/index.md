---
title: Perseikatan MNH48
description: Senarai pelayan Discord yang Yaya MNH48 telah sertai.
lang: ms
layout: article
needbtt: true
---


{%- assign limit = site.data.guildlist.size -%}
<style>
.guildtable {
  line-height:1.2em;
}
.guildtable a {
  font-weight: normal;
}
.guildtable td:first-child img {
  height: 64px;
  width: 64px;
}
.guildtable td:nth-child(2) a {
  font-weight: bold;
}
.guildtable td:nth-child(4) img {
  width: 250px;
  height: 100px;
}
.guildtable td:nth-child(5) {
  font-size: 0.8em;
  text-align: left;
}
.defaultimage {
  height: 100px;
  display: inline-block;
  overflow: hidden;
  vertical-align: middle;
  border-bottom-style: none;
  margin-bottom: 6px;
}
.toc ul[data-title]::before {
  content: attr(data-title);
  display: block;
  font-weight: bold;
  padding: 4px;
  font-size: 1.2em;
}

{%- for i in (1..limit) -%}
  {%- for folder in site.data.guildlist -%}
    {%- if i == folder[1].order %}
#{{folder[0] | slice: 3, folder[0].size}}-table {
  border: 2px solid #{{folder[1].color}};
}
    {%- endif -%}
  {%- endfor -%}
{%- endfor %}
</style>


Saya Yaya MNH48, saluran perhubungan saya yang utama ialah menerusi [Discord](https://discord.com/users/341115067934310411) yang mana tag pengguna saya ialah `MNH48#0048`.

Ditunjukkan di bawah ini ialah pengepala dan pengenalan pada profil sejagat saya. Ia dipaparkan apabila anda melihat profil saya dalam sesuatu pelayan jika saya tidak menetapkan sebarang pengepala atau pengenalan profil yang khusus untuk pelayan tersebut, atau apabila anda melihat profil saya secara terus dari layar mesej peribadi.

<table>
  <tr>
    <th style="text-align: center;">Pengepala Profil Lalai / Sejagat</th>
    <th style="text-align: center;">Pengenalan Profil Lalai / Sejagat</th>
  </tr>
  <tr>
    <td style="text-align: center;">
      <div class="defaultimage">
        <img src="https://img.mnh48.moe/discord/server-banner/default.gif" alt="Pengepala profil lalai buat Yaya MNH48" style="width: 250px; height: 168px; position: relative; top: 50%; transform: translateY(-50%);">
      </div>
    </td>
    <td style="text-align: left; line-height: 1.2em; font-size: 0.8em;" markdown="span">
      [she/her] 🇲🇾 🏳️‍⚧️ Malay demigirl nonbinary from Malaysia—DIY HRT since 14/02/2020<br/>
      <br/>
      Translating English/Chinese/Japanese to Malay—[https://tl.mnh48.moe/](https://tl.mnh48.moe/)<br/>Also: [https://guild.mnh48.moe/](https://guild.mnh48.moe/)
    </td>
  </tr>
</table>


- [Senarai Pelayan](#senarai-pelayan)
{%- for i in (1..limit) -%}
  {%- for folder in site.data.guildlist -%}
    {%- if i == folder[1].order %}
  - [{{folder[1].name}}{%- if folder[1].name-ms %} ({{folder[1].name-ms}}){%- endif -%}](#{{folder[0] | slice: 3, folder[0].size}})
    {%- endif -%}
  {%- endfor -%}
{%- endfor %}
{: .toc id="toc" data-title="Kandungan"}


## Senarai Pelayan
{: style="clear: none;"}

Ini semua pelayan Discord yang saya sertai. Anda boleh sertai mana-mana pelayan awam di bawah sekiranya anda ingin hubungi saya, atau kalau anda rasa tertarik dan berasa ingin tahu apa keadaannya di sesuatu pelayan tersebut.

Pelayan yang disenaraikan dipisahkan berdasarkan folder yang mengandungi pelayan tersebut, kecuali pelayan di bahagian terakhir bertajuk "Servers not in folder (Pelayan di luar folder)" yang mana pelayan tersebut diletakkan dengan sendirinya tanpa berada di dalam mana-mana folder. Pengepala bagi setiap bahagian jadual (kecuali bahagian terakhir) sepadan dengan nama folder tersebut beserta terjemahan dalam kurungan manakala warna garisan luar jadual sepadan dengan warna folder.

Memandangkan pengenalan profil ditulis sebagaimana adanya dan sepadan dengan tulisan sebenar yang digunakan, sesetengahnya bukan dalam bahasa Melayu, dan tiada terjemahan akan diberikan buat pengenalan tersebut kerana ia akan memakan ruang di laman ini.

Sekiranya ada pautan di bawah yang tidak berfungsi, sila beritahu saya dengan menyertai pelayan saya atau mana-mana pelayan lain yang tersenarai dan hantar mesej peribadi kepada saya. Senarai ini dikemaskini buat kali terakhir pada 14&nbsp;Julai&nbsp;2022&nbsp;(UTC+8).


&nbsp;


{%- for i in (1..limit) -%}
  {%- for folder in site.data.guildlist -%}
    {%- if i == folder[1].order %}
<h3 id="{{folder[0] | slice: 3, folder[0].size}}">{{ folder[1].name }}{%- if folder[1].name-ms %}<br/>({{folder[1].name-ms}}){%- endif -%}</h3>
<table id="{{folder[0] | slice: 3, folder[0].size}}-table" class="guildtable">
  <tr>
    <th>Ikon<br/>Pelayan</th>
    <th>Nama<br/>Pelayan</th>
    <th>Ringkasan<br/>Pelayan</th>
    <th>Pengepala Profil<br/>Khusus Pelayan</th>
    <th>Pengenalan Profil<br/>Khusus Pelayan</th>
  </tr>
  {%- for entry in folder[1].guild -%}
  <tr>
    <td><img src="https://img.mnh48.moe/discord/server-icon/{{entry.icon}}" loading="lazy" alt="Ikon pelayan untuk {{entry.name}}"></td>
    <td><strong>
    {%- if entry.link != "private" -%}
    <a href="{{entry.link}}">{{entry.name}}</a>
    {%- else -%}
    {{entry.name}}
    {%- endif -%}
    </strong></td>
    <td markdown="span">{{entry.summary.ms}}</td>
    <td markdown="span">
    {%- if entry.banner != "none" -%}
    <img src="https://img.mnh48.moe/discord/server-banner/{{entry.banner}}" loading="lazy" alt="Pengepala profil yang khusus untuk {{entry.name}}">
    {%- else -%}
    *Tiada pengepala khusus*
    {%- endif -%}
    </td>
    <td markdown="span">
    {%- if entry.introduction != "none" -%}
    {{entry.introduction}}
    {%- else -%}
    *Tiada profil khusus*
    {%- endif -%}
    </td>
  </tr>
  {%- endfor -%}
</table>
<br/>
    {%- endif -%}
  {%- endfor -%}
{%- endfor -%}
