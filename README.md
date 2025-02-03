
# Amigo Secreto 🎁

¡Bienvenido al proyecto **Amigo Secreto**! Esta es una aplicación sencilla y divertida que te permite organizar un sorteo de "amigo secreto" entre tus amigos. Simplemente ingresa los nombres de tus amigos, y la aplicación seleccionará al azar quién será el amigo secreto de cada uno.

## Funcionalidades principales 🚀

- **Agregar nombres**: Ingresa los nombres de tus amigos en el campo de texto y haz clic en "Añadir" para agregarlos a la lista.
- **Validación de entrada**: Si el campo de texto está vacío, la aplicación te alertará para que ingreses un nombre válido.
- **Visualización de la lista**: Los nombres que agregues se mostrarán en una lista debajo del campo de entrada.
- **Sorteo aleatorio**: Al hacer clic en "Sortear amigo", la aplicación seleccionará un nombre al azar de la lista y lo mostrará como el amigo secreto.

---

## Cómo funciona el código 🛠️

### 1. **Función `agregarAmigo`**
Esta función se encarga de agregar nombres a la lista de amigos:
- **Paso 1**: Obtiene el valor del campo de texto y lo valida para asegurarse de que no esté vacío.
- **Paso 2**: Si el campo no está vacío, crea un nuevo elemento `<li>` con el nombre del amigo y lo agrega a la lista `<ul id="listaAmigos">`.
- **Paso 3**: Limpia el campo de texto después de agregar el nombre.

### 2. **Función `sortearAmigo`**
Esta función realiza el sorteo del amigo secreto:
- **Paso 1**: Obtiene todos los elementos `<li>` de la lista de amigos.
- **Paso 2**: Valida que haya al menos un amigo en la lista antes de proceder con el sorteo.
- **Paso 3**: Selecciona un amigo aleatorio de la lista utilizando `Math.random()` y `Math.floor()`.
- **Paso 4**: Muestra el resultado del sorteo en el elemento `<ul id="resultado">`.

---

## Consideraciones adicionales 📌

### **Accesibilidad**
El código está diseñado pensando en la accesibilidad:
- Se utiliza `aria-labelledby` para asociar la lista con su etiqueta.
- Se usa `aria-live="polite"` en el contenedor de resultados para que los lectores de pantalla anuncien automáticamente el resultado del sorteo.

### **Optimización**
El código es eficiente y evita operaciones innecesarias:
- Las validaciones se realizan antes de cualquier acción.
- No se realizan llamadas a APIs externas ni operaciones costosas.

---

## Instrucciones de uso 🖱️

1. Ingresa el nombre de un amigo en el campo de texto.
2. Haz clic en "Añadir" para agregarlo a la lista.
3. Repite el proceso hasta que todos los nombres estén en la lista.
4. Haz clic en "Sortear amigo" para seleccionar un nombre al azar.
5. ¡El nombre seleccionado será el amigo secreto!

---

## Ejemplo de uso

```html
<input type="text" id="amigo" placeholder="Escribe un nombre">
<button onclick="agregarAmigo()">Añadir</button>
<ul id="listaAmigos"></ul>
<button onclick="sortearAmigo()">Sortear amigo</button>
<ul id="resultado"></ul>
```

---

## Contribuciones 🤝

¡Las contribuciones son bienvenidas! Si tienes ideas para mejorar la aplicación o encuentras algún error, no dudes en abrir un **issue** o enviar un **pull request**.

---

## Licencia 📄

Este proyecto está bajo la licencia [MIT](LICENSE). ¡Siéntete libre de usarlo y modificarlo!

---

¡Espero que disfrutes usando esta aplicación para organizar tu próximo **amigo secreto**! 🎉
