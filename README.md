# 🎮 CyberSpinner

[![Plataformas](https://img.shields.io/badge/Plataformas-PC-blue)](https://todo.cs.dev.spinner.com)
[![Género](https://img.shields.io/badge/G%C3%A9nero-Azar%20y%20Estrategia%20por%20turnos%2C%20Hacking%2C%20Ciberseguridad-green)](https://todo.cs.dev.spinner.com)

### 📚 Índice General

1. [🔍 Descripción](#-descripción)
2. [💻 Tecnologías Utilizadas](#-tecnologías-utilizadas)
3. [🕹️ Mecánicas de Juego y Estilo](#-mecánicas-de-juego-y-estilo)
   - [🤖 Estaciones de Jugador (Selección de "Malware")](#-estaciones-de-jugador-selección-de-malware)
   - [🦠 Tipos de Malware en CyberSpinner](#-tipos-de-malware-en-cyberspinner)
   - [🌀 Tirada de Código Aleatorio (Selección de Acción)](#-tirada-de-código-aleatorio-selección-de-acción)
   - [🔥 Símbolos del Codigo ](#-símbolos-del-codigo)
   - [⚔️ Combate (Aumento de Energía - Símbolos de Energía)](#-combate-aumento-de-energía---símbolos-de-energía)
   - [🔥 Firewall de Defensa (Construcción de un firewall - Símbolos de Defensa)](#-firewall-de-defensa-construcción-de-un-firewall---símbolos-de-defensa)
   - [🔥 Actualización de los "Malware" (Actualización de Software - Símbolos de Actualización)](#-actualización-de-los-malware-actualización-de-software---símbolos-de-actualización)
   - [🏆 Objetivo del Juego](#-objetivo-del-juego)
4. [🎨 Arte y Estilo](#-arte-y-estilo)
   - [🖼️ Arte](#-arte)
   - [📷 Cámaras](#-cámaras)
   - [🎵 Música y Sonido](#-música-y-sonido)
5. [📖 Historia y Ambientación](#-historia-y-ambientación)
6. [🔗 Integración con Plataformas y Servicios](#-integración-con-plataformas-y-servicios)
7. [📝 Notas Finales](#-notas-finales)
8. [🔍 Referencias](#-referencias)


### 📚 Índice Esquemático

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



### 🤖 Estaciones de Jugador (Seleccion de "Malware"):

- Cada jugador controla una "Estacion", compuesta por la representacion grafica de 2 ""Malware"" y un codigo central.
- Existen distintos tipos ""Malware"" y el jugador debe elegir solo a 2 para cada batalla.
- Cada tipo de servidor cuenta con una forma de comportarse en la batalla.
- La seleccion del tipo de servidor es agnostica al oponente, y solo se revela una vez transcurre la seccion de "Eleccion de Servidor"
- Los "Malware" de cada oponente se comportaran segun los valores obtenidos durante su Tirada de Codigo.


### 🌀 Tirada de Codigo Aleatorio (Seleccion de Acción):

- El jugador que tira primero es definido de forma aleatoria (TODO: Buscar elemento aleatorio representativo)
- El codigo aleatorio se compone de 5 slots para simbolos.
- Los jugadores giran el Codigo Aleatorio al comienzo de su turno y cuando este para obtiene ciertos valores.
- Los resultados de los codigos aleatorios determinan las acciones disponibles, como aumentar la energía, mejorar personajes o crear escudos.
- Cada jugador dispone de 3 tiradas por turno, pudiendo bloquear hasta 3 casillas de codigo que se mantendran fijas en la siguiente tirada.
- Una vez agotadas las 3 tiradas, el resultado del codigo se aplicara a la estacion del jugador y se realizara la accion correspondiente.

### 🦠 Tipos de Malware en CyberSpinner

- En esta sección se definen los tipos de malware seleccionables por el jugador.

   ### 🕵️‍♂️ Trojan (Guerrero):
- **Energía Necesaria para Atacar**: Baja
- **Daño**: Medio
- **Evolución**:
  - Nivel 1 a 2: Energía Moderada
  - Nivel 2 a 3: Energía Alta

### 🧙‍♂️ Polymorphic Virus (Mago):
- **Energía Necesaria para Atacar**: Media
- **Daño**: Alto
- **Evolución**:
  - Nivel 1 a 2: Energía Alta
  - Nivel 2 a 3: Energía Muy Alta

### 🏹 Ransomware (Arquero):
- **Energía Necesaria para Atacar**: Alta
- **Daño**: Alta
- **Evolución**:
  - Nivel 1 a 2: Energía Alta
  - Nivel 2 a 3: Energía Extremadamente Alta

### 🛠️ Rootkit (Ingeniero):
- **Energía Necesaria para Atacar**: Media
- **Daño**: Bajo
- **Evolución**:
  - Nivel 1 a 2: Energía Baja
  - Nivel 2 a 3: Energía Moderada

### 🗡️ Spyware (Asesino):
- **Energía Necesaria para Atacar**: Variable
- **Daño**: Bajo a Medio
- **Evolución**:
  - Nivel 1 a 2: Energía Variable
  - Nivel 2 a 3: Energía Alta

### 🚑 Adware (Sacerdote):
- **Energía Necesaria para Atacar**: Baja
- **Daño**: Ninguno
- **Evolución**:
  - Nivel 1 a 2: Energía Baja
  - Nivel 2 a 3: Energía Moderada


### ⚔️ Combate (Aumento de Energia - Simbolos de Energia)

- Los "Malware" pueden atacar a la Estacion de su oponente cuando su barra de energía está llena.
- El volumen de las barras de energia, y su costo es variable y depende del tipo de servidor.
- El valor del daño causado depende del nivel de actualizacion de servidor y su tipo.
- Un ataque puede encontrar resistencia si se encuentra con un Firewall enemigo.

### 🔥 Firewall de Defensa (Construccion de un firewall - Simbnolos de Defensa):

- Algunos recursos otorgados por los codigos aleatorios permiten a los jugadores defenderse de los ataques del oponente.
- El firewall actúa como una barrera con su propia barra de vida.
- Los ataques impactan contra el firewall, y cuando este se debilita, eventualmente se pierde, dejando al jugador vulnerable a ataques directos.

### 🔥 Actualización de los "Malware" (Actualización de Software - Símbolos de Actualización):

- Los jugadores pueden mejorar sus "Malware" utilizando símbolos específicos únicos obtenidos en la Tirada de Código Aleatorio.
- Un grupo de simbolos rellena otra barra de energia, cuando esta esta completa el servidor se actualiza (evoluciona)
- El sistema de mejoras es progresivo (3 mejoras) y permite a los jugadores personalizar su estrategia.

### 🔥 Símbolos del Codigo:

A. Slot Perdido - Símbolo de Error
- Representa un símbolo en la Tirada de Código Aleatorio que no tiene efecto y solo ocupa espacio en el rodillo.
- Este símbolo introduce un elemento de azar y riesgo, desafiando a los jugadores a adaptar su estrategia en base a resultados impredecibles.

B. Simbolos de energia de ataque - Símbolo de Malware
- Representa un símbolo en la Tirada de Código Aleatorio que sirve para aumentar la energia de ataque.
- Existen dos tipos de simbolos de energia de ataque basandose en la posicion del malware y ,a su vez,  dos tipos mas basados en el nivel de    energia que aumenta.  

   - Izquierda (Aplica a Malware de la Izquierda) 
      - Único = +Energia
      - Doble = +Energia*X

   - Derecha (Aplica a Malware de la Derecha)
      - Único = +Energia
      - Doble = +Energia*X

C. Simbolos de energia de ataque y experiencia - Símbolo de Error
- Comportamiento identico a "B. Simbolo de Energia de Ataque".
- Además de sumar energia de ataque suma experiencia en la barra de nivel del malware al que afecta.
- Los tipos disponibles son identicos a los de "B. Simbolos de energia de ataque"

D. Símbolos de construccion de Firewall
-Representa la accion de defensa y construccion del firewall.
-Levanta una "muralla" contra la que los ataques enemigos pueden perecer.
-No afecta a un personaje si no a la Estacion de Trabajo completa.
Existen dos tipos;

      - Único = +Defensa
      - Doble = +Defensa*X


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

La Referencia principal es el minijuego "girarrodillos" del juego JRPG Sea of Stars (Juego local) desarrollado por Sabotage Studios.
CyberSpinner se podría definir como una implementación online de las mecánicas de dicho minijuego.

![girarrodillos](./img/GDD/girarrodillos.jpg)

1 - Es el número de tiradas que tienes en la ronda actual. 
2 - Son los símbolos del rodillo.   
3 - Los héroes y sus estadísticas.   
4 - Los “activadores” para que los héroes entren en acción.

Fuente: Eliteguias

https://www.eliteguias.com/guias/s/sos/sea-of-stars_girarrodillos.php

+

https://store.steampowered.com/app/1244090/Sea_of_Stars/

https://www.eliteguias.com/guias/s/sos/sea-of-stars_girarrodillos.php

https://www.youtube.com/watch?v=H0u93GogDto

https://sabotagestudio.com


## Conceptos Básicos en CyberSpinner

Juego 1v1 en Cyberespacio: "CyberSpinner" es un juego uno contra uno donde los jugadores asumen el rol de hackers en el ciberespacio. Utilizan una interfaz de "Código Aleatorio" similar a una tragamonedas para combatir.

Inicio del Juego y Selección de "Malware": Al comenzar, cada jugador elige dos "Malware" o programas con habilidades únicas. Estas elecciones se revelan al inicio de la partida.

Mecánica del Código Aleatorio: Similar a la rueda de tragamonedas en "Wheels", los jugadores giran un código formado por símbolos para activar acciones. El objetivo es agotar los puntos de vida del oponente. Cada servidor reacciona de manera diferente según los símbolos obtenidos.

Energía y Acciones de "Malware": Los "Malware" actúan una vez acumulen suficiente energía, que se obtiene al hacer coincidir ciertos símbolos en el Código Aleatorio. Las acciones pueden incluir ataques, defensas o habilidades especiales.

Tácticas y Estrategias: Los jugadores deben desarrollar estrategias basadas en las habilidades de sus "Malware" y los resultados de sus códigos aleatorios, adaptándose a las jugadas del oponente y a los resultados impredecibles de la interfaz de código.

Progresión de "Malware": Al igual que en "Wheels", los "Malware" en "CyberSpinner" pueden mejorar a lo largo del juego. Esto se logra al acumular experiencias o recursos específicos, lo que puede aumentar su eficacia en combate o desbloquear nuevas habilidades.

Estrategia de Combate: Los jugadores deben equilibrar entre atacar al oponente y fortalecer sus defensas (Firewalls). La elección de cuándo y cómo mejorar los "Malware" o construir defensas forma parte de la estrategia del juego.

Elementos de Azar: El uso del "Símbolo No Computable" introduce un factor de riesgo e imprevisibilidad, desafiando a los jugadores a adaptarse constantemente y a formular estrategias en tiempo real.

Esta adaptación de las mecánicas de "Wheels" a "CyberSpinner" ofrece un marco para un juego estratégico y dinámico, donde la toma de decisiones y la adaptabilidad son clave para el éxito.





