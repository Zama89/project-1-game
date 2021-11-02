# project-1-game


## The trench

Este juego está planteado mediante canvas. Su lógica es sencilla, evitar que los enemigos ocupen la trinchera donde se encuentra nuestro jugador. Más adelante veremos cómo hacerlo.


### Players

Controlaremos un solo jugador que tendrá que luchar contra oleadas de soldados que lleve la máquina. Los soldados enemigos recorrerán el mapa directamente hacia nuestra trinchera.

Para definir ambas partes, crearemos una clase "Soldier" pues tendrán propiedades que compartan.


#### Class

En el caso de "Soldier" podremos definir la propiedad (life) y método (move), aunque los valores de ambas partes luego serán diferentes.

De "Soldier" haremos dos extensiones de ésta: "Player" y "Enemy".

**Soldier** estará estructurado de la siguiente manera:

```javascript class Soldier {
  constructor(life, position) {
  this.life = life
  this.position = position
  }
 move()
}

Ya tenemos nuestro molde referencial para crear nuestros personajes. Vamos a definir a nuestro **Player** y a nuestro **Enemy**:

```class Player extends Soldier {
  constructor (life, position) {
  }
  
  ```move ()``` // Este método servirá para desplazar a nuestro jugador en únicamente dos direcciones (moveUp, moveDown) que tendremos que definir solo sobre un eje Y al borde de      nuestro canva.
  
  ```attack ()``` // Nuestro Player podrá disparar desde su posición hacia el enemigo. El disparo recorrerá todo el eje X desde la misma linea que nos encontremos.
  
  
 ``` class Enemy extends Soldier {
  constructor (life, position) {
  }```
  
  ```move () ```// Nuestro Enemy recorrerá toda una línea en dirección a nuestra trinchera. No podrá disparar, únicamente recorrer el eje X. Si llega hasta trinchera vivo, acaba con la vida de Player (Game over). 
  


>El juego además de las propiedades sencillas de las clases, su principal foco se encuentra en la interacción entre ellos mediante diversos métodos. Su funcionalidad es la clave. Partiendo de las posiciones de ambas partes, tenemos que definir el movimiento de cada una y saber aplicar el método attack sobretodo.

>El menú de inicio tendrá un fondo de imagen que ya nos permita saber qué temática contiene el juego, añadiremos un pequeño comentario para el uso de los comandos del jugador y un boton de inicio del juego.
Durante la partida, nuestro objetivo es movernos a lo largo de la trinchera y disparar al enemigo para que no tome nuestra posición. El juego acaba si un "Enemy" llega hasta trinchera, por lo que nos aparecerá "GAME OVER" y un botón de "Try again" en caso de querer volver a jugar.


