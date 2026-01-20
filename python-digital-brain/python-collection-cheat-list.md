# 📦 Colecciones en Python – Métodos Más Usados

Este repositorio documenta **los métodos más utilizados de las colecciones nativas de Python**, explicado desde una perspectiva práctica y clara.

Está pensado como **chuleta de estudio**, referencia rápida y material de repaso para entrevistas o uso diario.

---

## 📋 Listas (`list`)

Las listas son **colecciones ordenadas y mutables**.

### `append(x)`

Agrega un elemento al final de la lista.

```python
numeros = [1, 2, 3]
numeros.append(4)
print(numeros)  # [1, 2, 3, 4]
```

---

### `extend(iterable)`

Agrega múltiples elementos desde otro iterable.

```python
lista = [1, 2]
lista.extend([3, 4])
print(lista)  # [1, 2, 3, 4]
```

---

### `insert(i, x)`

Inserta un elemento en una posición específica.

```python
letras = ['a', 'c']
letras.insert(1, 'b')
print(letras)  # ['a', 'b', 'c']
```

---

### `remove(x)`

Elimina la **primera aparición** del elemento indicado.

```python
nums = [1, 2, 3, 2]
nums.remove(2)
print(nums)  # [1, 3, 2]
```

---

### `pop(i)`

Elimina y retorna el elemento en la posición `i` (por defecto el último).

```python
pila = [1, 2, 3]
ultimo = pila.pop()
print(ultimo)  # 3
print(pila)    # [1, 2]
```

---

### `sort()`

Ordena la lista en el lugar.

```python
nums = [3, 1, 2]
nums.sort()
print(nums)  # [1, 2, 3]
```

---

### `reverse()`

Invierte el orden de la lista.

```python
nums = [1, 2, 3]
nums.reverse()
print(nums)  # [3, 2, 1]
```

---

## 📌 Tuplas (`tuple`)

Las tuplas son **ordenadas e inmutables**.

### `count(x)`

Cuenta cuántas veces aparece un elemento.

```python
tupla = (1, 2, 2, 3)
print(tupla.count(2))  # 2
```

---

### `index(x)`

Devuelve el índice de la primera aparición del elemento.

```python
tupla = ('a', 'b', 'c')
print(tupla.index('b'))  # 1
```

---

## 🧮 Sets (`set`)

Los sets son **colecciones desordenadas y sin duplicados**.

### `add(x)`

Agrega un elemento al set.

```python
s = {1, 2}
s.add(3)
print(s)  # {1, 2, 3}
```

---

### `remove(x)`

Elimina un elemento. Lanza error si no existe.

```python
s = {1, 2, 3}
s.remove(2)
print(s)  # {1, 3}
```

---

### `discard(x)`

Elimina un elemento **sin lanzar error** si no existe.

```python
s = {1, 2}
s.discard(3)
print(s)  # {1, 2}
```

---

### `union(set2)`

Devuelve la unión de dos sets.

```python
a = {1, 2}
b = {2, 3}
print(a.union(b))  # {1, 2, 3}
```

---

### `intersection(set2)`

Devuelve los elementos comunes.

```python
a = {1, 2, 3}
b = {2, 3, 4}
print(a.intersection(b))  # {2, 3}
```

---

## 🗂️ Diccionarios (`dict`)

Los diccionarios almacenan pares **clave → valor**.

### `get(key, default)`

Obtiene el valor de una clave sin lanzar error.

```python
usuario = {'nombre': 'Alex'}
print(usuario.get('edad', 18))  # 18
```

---

### `keys()`

Devuelve todas las claves.

```python
d = {'a': 1, 'b': 2}
print(d.keys())
```

---

### `values()`

Devuelve todos los valores.

```python
d = {'a': 1, 'b': 2}
print(d.values())
```

---

### `items()`

Devuelve pares clave-valor.

```python
d = {'a': 1, 'b': 2}
for k, v in d.items():
    print(k, v)
```

---

### `update(dict2)`

Actualiza el diccionario con otro.

```python
d = {'a': 1}
d.update({'b': 2})
print(d)  # {'a': 1, 'b': 2}
```

---

### `pop(key)`

Elimina y retorna el valor de la clave.

```python
d = {'a': 1, 'b': 2}
valor = d.pop('a')
print(valor)  # 1
print(d)      # {'b': 2}
```

---

## 🚀 Conclusión

* Aprende **listas y diccionarios primero** (90% del uso real)
* Sets son clave para eliminar duplicados y operaciones matemáticas
* Tuplas se usan para datos constantes y claves de diccionario

Este documento está pensado para **crecer**
---

✍️ *Autor: Alexander*
