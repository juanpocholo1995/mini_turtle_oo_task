# mini_turtle_oo_task

**Descripción breve:**
- **Proyecto:**: Mini implementación orientada a objetos de una "tortuga" que dibuja una escalera en consola.

**Estructura del proyecto:**
- **Raíz:**: [main.py](main.py) - Punto de entrada que demuestra el uso de la clase `Tortuga`.
- **Raíz:**: [__init__.py](__init__.py) - Reexporta la clase `Tortuga`.
- **Carpeta:**: [mini_turtle_oo](mini_turtle_oo) - Contiene la implementación principal.
	- **Archivo:**: [mini_turtle_oo/turtle_class.py](mini_turtle_oo/turtle_class.py) - Implementación de la clase `Tortuga`.
- **LICENSE**: Licencia del proyecto.
- **.gitignore**: Archivos ignorados por Git.

**Descripción de `main.py`:**
- **Propósito:**: Demostrar el uso de la clase `Tortuga` creando dos instancias independientes que dibujan escalones en la consola y muestran la función `reiniciar()`.
- **Comportamiento:**: Crea `t1` y `t2` (dos `Tortuga`), realiza llamadas a `adelante()` y `abajo()` para dibujar una "escalera" y luego reinicia cada tortuga para mostrar que el estado es independiente.

**Contenido de `main.py`:**

```python
from mini_turtle_oo.turtle_class import Tortuga 

# Crea dos tortugas dibujantes independientes
t1 = Tortuga()
t2 = Tortuga()

print("--- Escalera de T1 con adelante/abajo ---")
t1.adelante(4)
t1.abajo(3)
t1.adelante(4)
t1.abajo(3)

print("\n--- Escalera de T2 con adelante/abajo ------")
t2.adelante(4)
t2.abajo(3)
t2.adelante(4)
t2.abajo(3)

print("\n--- Reiniciando T1 ---")
t1.reiniciar()
t1.adelante(4)
t1.abajo(3)
print("\n--- reiniciar ---")
t2.reiniciar()
t2.adelante(4)
t2.abajo(3)
```

**Notas rápidas sobre `mini_turtle_oo/turtle_class.py`:**
- **Clase:**: `Tortuga` — mantiene `paso_actual` como estado para calcular sangrías entre escalones.
- **Métodos:**:
	- `adelante(n)`: Dibuja un segmento horizontal con longitud `n`.
	- `abajo(n)`: Dibuja la parte vertical `n` veces y aumenta `paso_actual` para el siguiente escalón.
	- `reiniciar()`: Restablece `paso_actual` a 0.

Si deseas, puedo además:
- Ejecutar `main.py` aquí y pegar la salida de consola.
- Añadir ejemplos adicionales o documentación detallada de la API.

**Salida de ejemplo (ejecución de `main.py`):**

```
--- Escalera de T1 con adelante/abajo ---
---->      
	|     
	|     
	|     
	V     
	----> 
		|
		|
		|
		V

--- Escalera de T2 con adelante/abajo ------
---->
	|
	|
	|
	V
	---->
		|
		|
		|
		V

--- Reiniciando T1 ---
---->
	|
	|
	|
	V

--- reiniciar ---
---->
	|
	|
	|
	V
```