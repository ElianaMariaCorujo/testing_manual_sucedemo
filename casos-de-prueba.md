## Caso de prueba 1 – Login exitoso

**ID:** TC-001  
**Funcionalidad:** Inicio de sesión  
**Tipo de prueba:** Funcional – Positiva  
**Prioridad:** Alta

### Objetivo:
Verificar que un usuario válido pueda iniciar sesión correctamente.

### Precondiciones:
- Usuario en estado activo
- Navegador abierto en [https://www.saucedemo.com](https://www.saucedemo.com)

### Pasos:
1. Ingresar a https://www.saucedemo.com  
2. En el campo "Username", ingresar `standard_user`  
3. En el campo "Password", ingresar `secret_sauce`  
4. Hacer clic en el botón **Login**

### Resultado esperado:
El usuario accede a la página de productos (`/inventory.html`) sin errores.

### Resultado real:
✅ Se accede correctamente a la página de productos.

### Evidencia:
🖼️  login-ok.png


## Caso de prueba 2 – Login con credenciales inválidas

**ID:** TC-002  
**Funcionalidad:** Inicio de sesión  
**Tipo de prueba:** Funcional – Negativa  
**Prioridad:** Alta

### Objetivo:
Verificar que el sistema rechace credenciales incorrectas y muestre un mensaje de error adecuado.

### Precondiciones:
- Navegador abierto en [https://www.saucedemo.com](https://www.saucedemo.com)

### Pasos:
1. Ingresar a https://www.saucedemo.com  
2. En el campo "Username", ingresar `usuario_falso`  
3. En el campo "Password", ingresar `clave_incorrecta`  
4. Hacer clic en el botón **Login**

### Resultado esperado:
El sistema no permite el acceso y muestra un mensaje de error visible como:  
> "Epic sadface: Username and password do not match any user in this service"

### Resultado real:
✅ Se mostró el mensaje de error.

### Evidencia:
🖼️ `login_error.png`


## Caso de prueba 3 – Agregar un producto al carrito

**ID:** TC-003  
**Funcionalidad:** Carrito de compras  
**Tipo de prueba:** Funcional – Positiva  
**Prioridad:** Media

### Objetivo:
Verificar que el usuario pueda agregar un producto al carrito correctamente.

### Precondiciones:
- Usuario logueado en [https://www.saucedemo.com](https://www.saucedemo.com)
- En la vista de productos (`/inventory.html`)

### Pasos:
1. Iniciar sesión con credenciales válidas  
2. Hacer clic en el botón **Add to cart** del primer producto (ej: Sauce Labs Backpack)  
3. Hacer clic en el ícono del carrito (esquina superior derecha)

### Resultado esperado:
El producto aparece en la lista del carrito, con nombre, precio y cantidad visibles.

### Resultado real:
✅ El producto se ve correctamente

### Evidencia:
🖼️ `paso1_add.png`
🖼️ `paso2_add.png`

## Caso de prueba 4 – Eliminar producto del carrito

**ID:** TC-004  
**Funcionalidad:** Carrito de compras  
**Tipo de prueba:** Funcional – Positiva  
**Prioridad:** Media

### Objetivo:
Verificar que el usuario pueda eliminar un producto del carrito correctamente.

### Precondiciones:
- Usuario logueado en [https://www.saucedemo.com](https://www.saucedemo.com)
- Producto ya agregado al carrito

### Pasos:
1. Iniciar sesión con usuario `standard_user` y contraseña `secret_sauce`  
2. Agregar un producto al carrito (ej: Sauce Labs Backpack)  
3. Ir al carrito (ícono arriba a la derecha)  
4. Hacer clic en el botón **Remove** junto al producto

### Resultado esperado:
El producto desaparece de la lista del carrito y no queda ningún ítem agregado.

### Resultado real:
✅ Se realiza la prueba correctamente

### Evidencia:
🖼️ `paso1_remove.png`
🖼️ `paso2_remove.png`


## Caso de prueba 5 – Finalizar compra (checkout)

**ID:** TC-005  
**Funcionalidad:** Proceso de pago (Checkout)  
**Tipo de prueba:** Funcional – Positiva  
**Prioridad:** Alta

### Objetivo:
Verificar que el usuario pueda completar el proceso de compra de un producto correctamente.

### Precondiciones:
- Usuario logueado en [https://www.saucedemo.com](https://www.saucedemo.com)
- Al menos un producto agregado al carrito

### Pasos:
1. Iniciar sesión con usuario `standard_user` y contraseña `secret_sauce`  
2. Agregar un producto al carrito  
3. Ir al carrito y hacer clic en **Checkout**  
4. Completar los campos obligatorios:
   - First Name: `Eliana`
   - Last Name: `Corujo`
   - Zip/Postal Code: `12345`  
5. Hacer clic en **Continue**  
6. Verificar el resumen de compra  
7. Hacer clic en **Finish**

### Resultado esperado:
El sistema muestra una página de confirmación con el mensaje:  
> "THANK YOU FOR YOUR ORDER"

### Resultado real:
✅ Prueba de proceso de compra OK. En imagen paso4_compra.jpg se visualiza el mensaje "THANK YOU FOR YOUR ORDER"

### Evidencia:
🖼️ `paso1_compra.png`
🖼️ `paso2_compra.png`
🖼️ `paso3_compra.png`
🖼️ `paso4_compra.png`

