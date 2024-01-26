# 🎮 CyberSpinner

[![Plataformas](https://img.shields.io/badge/Plataformas-PC-blue)](https://todo.cs.dev.spinner.com)
[![Género](https://img.shields.io/badge/G%C3%A9nero-Azar%20y%20Estrategia%20por%20turnos%2C%20Hacking%2C%20Ciberseguridad-green)](https://todo.cs.dev.spinner.com)

## 📚 Índice General

1. [🔍 Descripción](#-descripción)
2. [💻 Tecnologías Utilizadas](#-tecnologías-utilizadas)
3. [🕹️ Mecánicas de Juego](#️-mecánicas-de-juego)
   - [🌀 Codigo Aleatorio](#-codigos aleatorios-de-la-fortuna)
   - [🤖 Estaciones de Ataque](#-estaciones-de-ataque)
   - [⚔️ Combate en el Ciberespacio](#️-combate-en-el-ciberespacio)
   - [🔥 Firewall de Defensa](#-firewall-de-defensa)
   - [🏆 Objetivo del Juego](#-objetivo-del-juego)
4. [🎨 Arte y Estilo](#-arte-y-estilo)
   - [🖼️ Arte](#️-arte)
   - [📷 Cámaras](#-cámaras)
   - [🎵 Música y Sonido](#-música-y-sonido)
5. [📖 Historia y Ambientación](#-historia-y-ambientación)
6. [🔗 Integración con Plataformas y Servicios](#-integración-con-plataformas-y-servicios)
7. [📝 Notas Finales](#-notas-finales)
8. [🔍 Referencias](#-referencias)

## 📚 Índice Esquemático

A. [🔍 Interfaz de Juego](#-descripción)
B. [🔍 Menu Principal](#-descripción)
C. [🔍 Diagramas de Flujo](#-descripción)

## 🔍 Descripción

"CyberSpinner" es un juego de azar y estrategia por turnos, modo multijugador 1VS1, en el que dos jugadores asumen el papel de hackers adversarios que se enfrentan en el ciberespacio. La clave del juego es hacer girar un "Codigo Aleatorio formado por simbolos" para determinar las acciones disponibles en cada turno y elegir sabiamente cómo usar los recursos obtenidos para derrotar al oponente.

## 💻 Tecnologías Utilizadas


- Game Engine; Unity 2022.3.18f1 LTS - Sub basica.
- IDE: VS Code 1.85.2
- Control de Versiones; GIT 2.43.0 - Repositorio Monolítico
- Repositado: GitHub - https://github.com/Cyber-Spinner
- IAC: Terraform
- IAC: Kubernetes/Docker
- Otras

## 🕹️ Mecánicas de Juego y Estilo

### 🌀 Codigo Aleatorio:

- El codigo aleatorio se compone de 5 slots para simbolos.
- El jugador que empieza primero se define de forma aleatoria.
- Los jugadores giran el Codigo Aleatorio al comienzo de su turno.
- Los resultados de los codigos aleatorios determinan las acciones disponibles, como aumentar la energía, mejorar personajes o crear escudos.
- Cada jugador dispone de 3 tiradas por turno, pudiendo bloquear hasta 3 casillas de codigo que se mantendran fijas en la siguiente tirada.
- Una vez agotadas las 3 tiradas, el resultado del codigo se aplicara a la estacion del jugador y se realizara la accion correspondiente.


### 🤖 Estaciones de Jugador:

- Cada jugador controla una "Estacion", compuesta por la representacion grafica de 2 "servidores".
- Existen distintos tipos "servidores" y el jugador debe elegir solo a 2 para cada batalla.
- Cada tipo de servidor cuenta con una forma de comportarse en la batalla.
- La seleccion del tipo de servidor es agnostica al oponente, y solo se revela una vez transcurre la seccion de "Eleccion de Servidor"
- La combinacion de codigos obtenidos tras agotar las tiradas determinan el comportamiento de cada "servidor".

### ⚔️ Combate en el Ciberespacio:

- Los jugadores pueden atacar a los personajes de sus oponentes cuando su barra de energía está llena.
- El combate se resuelve mediante enfrentamientos estratégicos basados en las habilidades de los personajes y las decisiones tácticas.

### 🔥 Firewall de Defensa:

- Algunos recursos otorgados por los codigos aleatorios permiten a los jugadores defenderse de los ataques del oponente.
- El firewall actúa como una barrera con su propia barra de vida.
- Los ataques impactan contra el firewall, y cuando este se debilita, eventualmente se pierde, dejando al jugador vulnerable a ataques directos.

### 🏆 Objetivo del Juego:

- El objetivo es atacar y terminar con las vidas (10) del oponente antes de que lo haga el oponente.

## 🎨 Arte y Estilo

### 🖼️ Arte:

- Estilo cibernético y futurista, colores saturados y transparencias.
- Arte 3D low-poly

### 📷 Cámaras:

- Vista Cenital Fija

### 🎵 Música y Sonido:

- Música electrónica/experimental/ 1990s
- Efectos de sonido relacionados con la ciberseguridad y el hacking. Digital Lofi//Modems

## 📖 Historia y Ambientación

- Simple, el juego se desarrolla en un mundo virtual donde cada jugador asume el papel de un hacker y compite contra otro.

## 🔗 Integración con Plataformas y Servicios

- Integración con la plataforma de juego en la nube para partidas multijugador en línea.
- Opciones de autenticación de usuarios a través de Firebase Authentication o PlayFab.

## 📝 Notas Finales

Este Game Design Document (GDD) proporciona una visión general del juego "CyberSpinner" y sus características principales. Es un documento vivo que puede evolucionar a medida que se desarrolla el proyecto.

## 🔍 Referencias

La Referencia principal es el minijuego "Giracodigos aleatorios" del juego JRPG Sea of Stars (Juego local) desarrollado por Sabotage Studios.
CyberSpinner se podría definir como una implementación online de las mecánicas de dicho minijuego.

![Giracodigos aleatorios](./img/GDD/girarcodigos aleatorios.jpg)

1 - Es el número de tiradas que tienes en la ronda actual. 
2 - Son los símbolos del rodillo.   
3 - Los héroes y sus estadísticas.   
4 - Los “activadores” para que los héroes entren en acción.

Fuente: Eliteguias

https://www.eliteguias.com/guias/s/sos/sea-of-stars_girarcodigos aleatorios.php

+

https://store.steampowered.com/app/1244090/Sea_of_Stars/

https://www.eliteguias.com/guias/s/sos/sea-of-stars_girarcodigos aleatorios.php

https://www.youtube.com/watch?v=H0u93GogDto

https://sabotagestudio.com
