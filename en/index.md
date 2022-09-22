---
title: MNH48 Guild
description: List of Discord servers that Yaya MNH48 had joined.
lang: en
layout: article
hasENG: true
hasRMI: true
hasJWI: true
needbtt: true
redirect_from: "/"
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
  height: 88px;
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


I'm Yaya MNH48, my main communication channel is [Discord](https://discord.com/users/341115067934310411) where my user tag is `MNH48#0048`.

Shown below is the default banner and introduction on my global profile. It's what you see when you view my profile on a server if I don't set any server-specific profile banner or introduction for that server, or if you view my profile from the direct message screen.

<table>
  <tr>
    <th style="text-align: center;">Global / Default Profile Banner</th>
    <th style="text-align: center;">Global / Default Profile Introduction</th>
  </tr>
  <tr>
    <td style="text-align: center;">
      <div class="defaultimage">
        <img src="https://img.mnh48.moe/discord/server-banner/default.gif" alt="Default profile banner of Yaya MNH48" style="width: 283px; height: 100px; position: relative; top: 50%; transform: translateY(-50%);">
      </div>
    </td>
    <td style="text-align: left; line-height: 1.2em; font-size: 0.8em;" markdown="span">
      [she/her] 🇲🇾 🏳️‍⚧️ Malay demigirl nonbinary from Malaysia—DIY HRT since 14/02/2020<br/>
      <br/>
      Translating English/Chinese/Japanese to Malay—[https://tl.mnh48.moe/](https://tl.mnh48.moe/)<br/>Also: [https://guild.mnh48.moe/](https://guild.mnh48.moe/)
    </td>
  </tr>
</table>


- [Server List](#server-list)
{%- for i in (1..limit) -%}
  {%- for folder in site.data.guildlist -%}
    {%- if i == folder[1].order %}
  - [{{folder[1].name}}](#{{folder[0] | slice: 3, folder[0].size}})
    {%- endif -%}
  {%- endfor -%}
{%- endfor %}
{: .toc id="toc" data-title="Table of Content"}


## Server List
{: style="clear: none;"}

These are Discord servers that I had joined. You can join any of the public servers if you want to contact me, or if you just find it interesting and intrigued to see what the environment is on any specific server.

The servers listed are separated by the folder that contained them, except the servers in the last section titled "Servers not in folder" where they are put on their own without being contained in any folder. The header of each table section (except last section) correspond to the folder's name whereas the outer table border's colour correspond to the folder's colour.

As the profile introductions are written as-is and matched with the actual text used, some of them are not in English, and no translations will be given for those introductions as it will take too much space of the site.

If any of the links on the list not working, please tell me by joining my server or any other server listed and then send direct message to me. This list is last updated on {{ site.data.html.update.en | replace: " ", "&nbsp;" }}.


&nbsp;


{%- for i in (1..limit) -%}
  {%- for folder in site.data.guildlist -%}
    {%- if i == folder[1].order %}
<h3 id="{{folder[0] | slice: 3, folder[0].size}}">{{ folder[1].name }}</h3>
<table id="{{folder[0] | slice: 3, folder[0].size}}-table" class="guildtable">
  <tr>
    <th>Server<br/>Icon</th>
    <th>Server<br/>Name</th>
    <th>Server<br/>Summary</th>
    <th>Server-specific<br/>Profile Banner</th>
    <th>Server-specific<br/>Profile Introduction</th>
  </tr>
  {%- for entry in folder[1].guild -%}
  <tr>
    <td><img src="https://img.mnh48.moe/discord/server-icon/{{entry.icon}}" loading="lazy" alt="Server icon for {{entry.name}}"></td>
    <td><strong>
    {%- if entry.link != "private" -%}
    <a href="{{entry.link}}">{{entry.name}}</a>
    {%- else -%}
    {{entry.name}}
    {%- endif -%}
    </strong></td>
    <td markdown="span">{{entry.summary.en}}</td>
    <td markdown="span">
    {%- if entry.banner != "none" -%}
    <img src="https://img.mnh48.moe/discord/server-banner/{{entry.banner}}" loading="lazy" alt="Profile banner that is specific for {{entry.name}}">
    {%- else -%}
    *No specific banner*
    {%- endif -%}
    </td>
    <td markdown="span">
    {%- if entry.introduction != "none" -%}
    {{entry.introduction}}
    {%- else -%}
    *No specific profile*
    {%- endif -%}
    </td>
  </tr>
  {%- endfor -%}
</table>
<br/>
    {%- endif -%}
  {%- endfor -%}
{%- endfor -%}
