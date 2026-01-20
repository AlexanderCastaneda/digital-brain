# 🐍 Python Collections: Guía de Referencia Rápida
Markdown# 🐍 Python Collections: Guía de Referencia Rápida

Documentación personal sobre los métodos más comunes y eficientes para manipular estructuras de datos en Python.

---

## 1. Listas (`list`)
**Uso:** Colecciones ordenadas, mutables y permiten duplicados. Ideales para secuencias de datos.

### Métodos de Manipulación
* `lista.append(x)`: Agrega `x` al final. ($O(1)$).
* `lista.extend(iterable)`: Une otra lista o iterable al final.
* `lista.insert(i, x)`: Inserta `x` en la posición `i`. **Cuidado:** Es costoso en listas grandes.
* `lista.pop([i])`: Elimina y **retorna** el elemento en `i` (o el último si no se indica índice).

### Ordenamiento y Búsqueda
* `lista.sort(key=..., reverse=...)`: Ordena la lista *in-place* (modifica la original).
* `lista.index(x)`: Retorna el índice del primer elemento `x` encontrado.

```python
# Ejemplo Práctico
usuarios = ["Ana", "Beto", "Carla"]

usuarios.append("Daniel")     # ['Ana', 'Beto', 'Carla', 'Daniel']
ultimo = usuarios.pop()       # Retorna "Daniel"
usuarios.sort(reverse=True)   # ['Carla', 'Beto', 'Ana']
💡 Senior Tip: Si necesitas hacer muchos pop(0) (sacar elementos del inicio), no uses una lista. Usa collections.deque, es mucho más eficiente para colas (FIFO).2. Diccionarios (dict)Uso: Almacenamiento clave-valor. Búsquedas extremadamente rápidas ($O(1)$).Acceso Seguro y Manipulacióndic.get(key, default): La forma segura de buscar. Si la clave no existe, devuelve default (evita errores).dic.setdefault(key, default): Si la clave existe, retorna su valor. Si no, la crea con default.dic.update(otro_dic): Fusiona diccionarios (sobrescribe claves existentes).dic.pop(key, default): Elimina la clave y retorna el valor.Iteración (Vistas).items(): Para obtener clave y valor al tiempo..keys() / .values(): Para obtener solo claves o valores.Pythoninventario = {"manzanas": 10, "peras": 5}

# Evitar KeyError
cantidad = inventario.get("uvas", 0) 

# Loop Pythonico
for fruta, cant in inventario.items():
    print(f"{fruta}: {cant}")
3. Sets (set)Uso: Elementos únicos y desordenados. Operaciones matemáticas de conjuntos.Métodos Claves.add(x): Agrega un elemento.s.discard(x): Elimina x si existe (no lanza error si no está). Preferible sobre .remove().s.union(otro), s.intersection(otro): Operaciones lógicas.Pythonids = {101, 102, 103}
ids.discard(999) # Seguro, no rompe el código

# Truco: Eliminar duplicados de una lista
lista_sucia = [1, 2, 2, 3, 1]
unicos = list(set(lista_sucia)) # [1, 2, 3]
4. Tuplas (tuple)Uso: Inmutables. Datos que no deben cambiar.t.count(x): Cuenta apariciones de x.t.index(x): Retorna índice de x.🧠 Flujo de Decisión (Mental Model)Para elegir la estructura correcta en mis proyectos:¿Necesito orden y modificar datos? → List¿Necesito asociar datos (ID -> Valor) y velocidad? → Dict¿Necesito eliminar duplicados o verificar pertenencia? → Set¿Son datos fijos de configuración? → TupleBonus: Iteración con ÍndiceNo usar range(len(lista)). Usar siempre enumerate():Pythonfrutas = ["Mango", "Fresa"]
for i, fruta in enumerate(frutas):
    print(f"{i}: {fruta}")
