# Ejercicio: Plataforma de Streaming y Descargas

## 1. La base
Crear una clase madre llamada `Medio` con los atributos `titulo` (String) y `duracion` (int, en minutos). Agregar un método `reproducir()` que imprima en consola: *"Reproduciendo el medio: [título]"*.

## 2. Especialización
Crear dos subclases que hereden (`extends`) de `Medio`:
* **Cancion**: agrega el atributo `artista`. Debe sobrescribir (`@Override`) el método `reproducir()` para que imprima: *"Reproduciendo canción: [título] - Artista: [artista]"*.
* **Pelicula**: agrega el atributo `director`. Debe sobrescribir el método `reproducir()` para que imprima: *"Proyectando película: [título] - Dirigida por: [director]"*.

## 3. Polimorfismo
En tu clase `Main`, crear un arreglo de tipo `Medio` (tamaño 2). Guardar ahí adentro una instancia de `Cancion` y una de `Pelicula`. Recorrer el arreglo con un bucle `for` y llamar al método `reproducir()` de cada elemento.

---

## Bonus Track (Interfaces)
*Nuestra plataforma permite descargar canciones para escuchar offline, pero las películas son exclusivas de streaming.*

### Consignas extra:
4. Crear una interfaz llamada `Descargable` que defina el método vacío `void descargar()`.
5. Hacer que la clase `Cancion` implemente (`implements`) esta interfaz e imprima: *"Descargando archivo mp3 de la canción..."*.
6. **Para demostrar el poder de los contratos:** Crear una clase totalmente ajena llamada `Apunte` (con el atributo `tema`). Esta clase no hereda de `Medio`, pero sí implementa `Descargable` (imprimiendo *"Descargando PDF del apunte..."*).
