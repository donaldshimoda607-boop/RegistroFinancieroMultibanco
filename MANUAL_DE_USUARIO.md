# Manual de usuario

Este manual explica cómo usar **Registro Financiero Multibanco** desde el primer inicio de sesión hasta la clasificación de los gastos. No necesitas conocimientos de programación.

---

## 1. Qué hace la aplicación

La aplicación se conecta a tu cuenta de Gmail, lee los correos que envían los bancos cuando haces una compra o una transferencia, y guarda esos movimientos en una base de datos local.

Después puedes:

- ver cuánto gastaste en cada mes del año;
- ver tus ingresos de cada mes (los que vienen en las cartolas PDF y los que registres a mano);
- entrar al detalle de un mes y revisar sus categorías;
- clasificar cada movimiento;
- registrar a mano los gastos pagados en efectivo y los ingresos que no llegan por correo;
- marcar transferencias propias o compras con tarjeta para que no sumen en los totales (los traspasos a tus propias cuentas y los pagos de tarjeta se reconocen solos);
- descargar las **cartolas PDF** de los bancos, archivarlas en el equipo y abrirlas en un visor interno;
- eliminar una transacción o un ingreso desde su detalle.

La aplicación **no mueve dinero** ni se conecta a la banca en línea. Solo lee correos.

---

## 2. Antes de empezar

Necesitas:

1. Un computador con **Windows 10 u 11**.
2. Una cuenta de **Gmail** donde lleguen los avisos de tus bancos.
3. **Verificación en dos pasos** activada en esa cuenta.
4. Una **contraseña de aplicación** de Google.
5. Los correos de los bancos en la cuenta. La aplicación revisa la carpeta **Todos los mensajes**, así que también encuentra correos archivados. **No revisa Spam ni Papelera.**

### Crear la contraseña de aplicación

1. Abre <https://myaccount.google.com/security>.
2. Entra a **Verificación en dos pasos**.
3. Al final de la página, elige **Contraseñas de aplicaciones**.
4. Escribe un nombre, por ejemplo `Registro Financiero`, y genera la contraseña.
5. Copia los **16 caracteres**. Puedes pegarlos con espacios: la aplicación los quita sola.

> Esa contraseña es distinta de tu contraseña normal. Si algún día la revocas, deberás generar otra y actualizarla en la aplicación.

### Instalar el programa

El programa es un solo archivo: `RegistroFinancieroMultibanco.exe`. No necesita instalación.

1. Crea una carpeta propia para el programa, por ejemplo `Documentos\Registro Financiero`, y guarda ahí el `.exe`. **El programa guarda tus datos en esa misma carpeta**, así que no lo dejes en *Descargas* ni en el escritorio junto a otros archivos.
2. Ábrelo con doble clic.
3. Si Windows muestra **«Windows protegió su PC»**, presiona **Más información** y luego **Ejecutar de todas formas**. Aparece porque el programa no tiene firma digital (ver la pregunta frecuente sobre el «Editor desconocido»).
4. La primera vez tarda unos segundos más en abrir.

Si quieres un acceso directo en el escritorio: clic derecho sobre el `.exe` → **Mostrar más opciones** → **Enviar a** → **Escritorio (crear acceso directo)**. No muevas el `.exe` al escritorio: así tus datos quedan juntos en su carpeta.

---

## 3. Primer inicio de sesión

1. Abre el programa (`RegistroFinancieroMultibanco.exe`). En la versión de prueba, primero activa tu clave en la ventana **Licencia de prueba** (ver *Solución de problemas → Versión de prueba*).
2. Si no hay credenciales guardadas, aparece la ventana **Configurar Credenciales de Gmail**.
3. Escribe tu correo completo y la contraseña de aplicación. En la versión de prueba, el Gmail de tu licencia ya viene escrito: solo agrega la contraseña de aplicación.
4. Pulsa **Guardar y Conectar**.

La aplicación prueba la conexión antes de guardar. Si funciona:

- las credenciales quedan cifradas en tu equipo;
- la ventana se cierra;
- el botón de la pestaña de extracción cambia a **🟢 Sesión Iniciada**.

Si falla, revisa:

- que el correo esté completo (`nombre@gmail.com`);
- que hayas usado la contraseña de aplicación, no la normal;
- que la verificación en dos pasos esté activa;
- que tengas conexión a internet.

Puedes actualizar la contraseña de aplicación cuando quieras con el botón **🟢 Sesión Iniciada** / **🔑 Iniciar Sesión**. El Gmail, en cambio, debe ser siempre **el de tu clave de licencia**: la ventana ya lo trae escrito y no acepta otro (ver *Preguntas frecuentes → ¿Puedo usar otra cuenta de Gmail?*).

---

## 4. La pantalla principal

La ventana tiene ocho pestañas, agrupadas por color:

| Pestaña | Color | Para qué sirve |
|---|---|---|
| **📥 Extracción** | Gris grafito | Descargar movimientos nuevos desde Gmail y ver el proceso en vivo. |
| **📊 Gastos · Tarjetas** | Rojo | Ver los totales de gastos de los 12 meses del año elegido. |
| **🔍 Gastos · Detalle** | Rojo oscuro | Revisar y clasificar los gastos de un mes. |
| **💰 Ingresos · Tarjetas** | Verde | Ver los totales de ingresos de los 12 meses del año elegido. |
| **💵 Ingresos · Detalle** | Verde oscuro | Revisar y clasificar los ingresos de un mes. |
| **✍️ Registro Manual** | Bronce | Agregar, editar y eliminar gastos e ingresos en efectivo. |
| **📄 Cartolas PDF** | Morado | Descargar cartolas, revisarlas en el visor interno, archivarlas y aplicar ingresos y gastos. |
| **❓ Ayuda** | Azul | Consultar este manual sin salir del programa. |

La barra superior mantiene el color de cada sección: la pestaña activa va con su color pleno y las demás con una versión suave del mismo, así se distingue de un vistazo dónde estás. **Gastos** va en rojo e **Ingresos** en verde, y ambos son módulos independientes: tienen sus propias tablas, categorías, excepciones y tarjetas. **Cartolas PDF** alimenta a ambos módulos.

### 4.1 Cómo usar la pestaña de ayuda

Abre **❓ Ayuda** cuando necesites consultar cómo funciona algo sin salir del programa.

- **Documento**: el documento que estás leyendo. El programa trae el **Manual de usuario**; si incluye otros documentos, también aparecen en esta lista.
- **Contenido**: a la izquierda aparece el índice del documento. Haz clic en un tema para saltar a esa sección.
- **Buscar**: escribe una palabra o frase y pulsa **🔍 Buscar** (o Enter). Se resaltan todas las coincidencias del documento actual y se muestra cuántas hay. **Limpiar** quita el resaltado.
- **📖 Abrir documento actual**: abre el manual fuera del programa, en tu editor o visor predeterminado (por ejemplo, para imprimirlo). **📂 Abrir carpeta de documentación** abre la carpeta donde está. Es una copia temporal que el programa prepara al abrirse y borra al cerrarse.
- **🔄 Recargar**: vuelve a cargar el documento.
- **ℹ️ Acerca de**: muestra la versión del programa, los datos del autor y el estado de tu licencia, con el botón **🔑 Licencia** para ver o cambiar tu clave.

Si por algún motivo el manual no se puede leer, la pestaña muestra una **guía rápida** integrada con los pasos principales y los problemas más comunes.

---

## 5. Extraer movimientos

### 5.1 Elegir bancos

En **📥 Extracción**, dentro de **Bancos a extraer**, marca uno o varios bancos:

- MACHBANK
- BANCOESTADO
- SANTANDER

Todos vienen marcados al iniciar. Si no marcas ninguno y pulsas extraer, la aplicación avisa y no hace nada.

MachBank extrae transferencias, compras con tarjeta de crédito y débito, **pagos de cuentas o servicios** (por ejemplo, celular, luz o agua) y pagos a personas. Los pagos de cuentas llegan en el correo **“Tu pago de cuentas con MACHBANK”**.

Los avisos de **pagos de cuentas** pueden venir de `machbank` o de `somosmach.com`, y la aplicación busca en ambos. Los demás avisos de MachBank se buscan solo en `machbank`.

BancoEstado extrae transferencias y compras con tarjeta de débito. Las transferencias se buscan con los tres asuntos que ha usado el banco: **“Aviso de envío o recepción de dinero”** (desde 2022), **“Aviso de Transferencia de Fondos”** (2017-2022) y **“Transferencias - A Terceros”** (2019-2020). Por eso el resumen de BancoEstado muestra tres líneas de transferencias. Todavía no se leen los **“Comprobante TEF”** de 2018-2019 ni las compras de 2019 que no dicen el tipo de tarjeta.

### 5.2 Iniciar la extracción

Pulsa **🚀 Extraer todo**.

Durante el proceso:

- el botón de extraer y los bancos quedan deshabilitados;
- los botones **🔎 Previsualizar** y **✅ Aplicar** de **📄 Cartolas PDF** también quedan deshabilitados: la extracción y las cartolas no pueden escribir en la base al mismo tiempo;
- se habilita **🛑 Cancelar Extracción**;
- la consola muestra cada paso.

Si intentas iniciar un proceso mientras el otro está corriendo, la aplicación avisa y espera a que termine.

La aplicación abre **una sola sesión con Gmail** y recorre los bancos y tipos seleccionados. Si un banco falla, los demás continúan.

### 5.3 Cancelar

Pulsa **🛑 Cancelar Extracción**. El proceso se detiene de forma ordenada al terminar el correo que está procesando. **Lo que ya se guardó se conserva.**

### 5.4 La consola

La consola muestra, entre otros mensajes:

- la carpeta de Gmail revisada;
- la búsqueda enviada a Gmail;
- correos encontrados y pendientes;
- cada transacción guardada;
- cada correo descartado y el motivo;
- errores de un banco.

Los mensajes `GUARDADO`, `OMITIDO` y `DESCARTADO` permiten seguir el proceso correo por correo.

### 5.5 Resumen final

Al terminar se abre la ventana **📋 Resumen de la Extracción**, con el mismo texto que queda en la consola.

Ejemplo:

```text
Extracción FINALIZADA. Registros nuevos: 2

MACHBANK
  TRANSFERENCIAS: encontrados 248 | ya guardados 247 | descargados 1 | nuevos 1
  CRÉDITO: encontrados 565 | ya guardados 564 | descargados 1 | nuevos 1
  DÉBITO: encontrados 146 | ya guardados 146 | descargados 0 | nuevos 0
  PAGOS DE CUENTAS: encontrados 0 | ya guardados 0 | descargados 0 | nuevos 0
    diagnóstico: remitente + asunto = 0 | solo remitente = 1052

BANCOESTADO
  TRANSFERENCIAS: encontrados 199 | ya guardados 133 | descargados 1 | nuevos 1 | descartados antes 65
  DÉBITO: encontrados 132 | ya guardados 108 | descargados 0 | nuevos 0 | descartados antes 24

SANTANDER
  TRANSFERENCIAS: encontrados 230 | ya guardados 222 | descargados 8 | nuevos 0
    descartes: INGRESO=8
```

#### Qué significa cada número

| Campo | Significado |
|---|---|
| **encontrados** | Correos que Gmail devolvió para esa búsqueda. Incluye los que ya estaban guardados. |
| **ya guardados** | Correos cuyo identificador ya existe en la base, o que una cartola ya registró; no se vuelven a descargar. |
| **descartados antes** | Correos que una extracción anterior descartó por un motivo que no cambia (dinero recibido, otro remitente, otro asunto); no se vuelven a descargar. |
| **descargados** | Correos que se descargaron y procesaron en esta ejecución. |
| **nuevos** | Transacciones insertadas en la base. |
| **omitidos** | Correos que se descargaron y se interpretaron bien, pero la base no los aceptó (duplicado, ya registrado por una cartola o error). |
| **descartes** | Correos rechazados antes de guardar, agrupados por motivo. |
| **diagnóstico** | Solo aparece cuando una búsqueda devuelve 0 correos; indica en qué filtro se pierde. |

Como referencia, en una ejecución normal se cumple:

```text
encontrados = ya guardados + descartados antes + descargados
descargados = nuevos + omitidos + descartes
```

Puede no cuadrar exactamente si cancelaste el proceso o si Gmail devolvió menos correos de los pedidos (la consola muestra un `AVISO` en ese caso).

### 5.6 Descartes frecuentes

| Motivo | Qué significa | Qué hacer |
|---|---|---|
| `INGRESO` | El correo es de dinero **recibido**, no de un gasto o transferencia realizada. | Nada: la extracción desde Gmail solo registra salidas. Los ingresos entran por **📄 Cartolas PDF** o a mano en **✍️ Registro Manual**. |
| `TIPO NO SOPORTADO` | BancoEstado encontró una compra con tarjeta de **crédito**, o un aviso de 2019 que no dice el tipo de tarjeta; ese banco solo procesa débito. | Nada, o revisa si esperabas ese gasto en otro banco. |
| `REMITENTE` | El correo no viene de un dominio oficial del banco (por ejemplo, un reenvío manual). | Revisa el correo; los reenvíos no se procesan. |
| `ASUNTO` | El asunto no contiene la frase esperada. | Puede ser un formato nuevo del banco. |
| `PARSER` | El cuerpo no tiene los datos esperados (monto, destinatario, fecha). | Puede ser un formato nuevo del banco. |
| `ERROR_LECTURA` | El correo no se pudo interpretar por un problema de formato. | Revisa la consola; si se repite, guarda el correo como ejemplo. |

Los descartes `INGRESO`, `TIPO NO SOPORTADO`, `REMITENTE` y `ASUNTO` se recuerdan: en las extracciones siguientes esos correos no se vuelven a descargar y aparecen como **descartados antes**. Los descartes `PARSER` y `ERROR_LECTURA` no se recuerdan: se reintentan cada vez, por si una versión futura de la aplicación sí los entiende.

Los correos **omitidos** no son descartes: se interpretaron bien, pero la base ya tenía esa transacción o no pudo guardarla. La consola muestra el motivo exacto:

| Motivo del `OMITIDO` | Qué significa |
|---|---|
| `duplicado exacto` | El mismo correo ya estaba guardado. |
| `duplicado por banco + referencia + fecha` | Otro correo con el mismo número de operación ya estaba guardado. |
| `duplicado de una cartola ya importada` | La cartola PDF ya traía ese gasto. Es normal si aplicaste las cartolas antes de extraer los correos. La cartola puede registrar el cargo hasta 4 días después del aviso, y describirlo distinto (“TEF A …” en vez de “TRANSFERENCIA: …”). |
| `aviso repetido: la cartola registra una sola compra` | El banco mandó dos correos por la misma compra. La cartola de ese período la registra una sola vez y su cargo ya tiene asociado el primer aviso. |

Si la cartola registra dos compras iguales el mismo día, cada aviso queda asociado a una y ninguna se pierde. Las compras con tarjeta de **crédito** nunca se comparan con la cartola de la cuenta corriente, porque no pasan por ella.

### 5.7 Cuando una búsqueda devuelve 0

La aplicación prueba hasta tres búsquedas de diagnóstico (dos si el tipo no exige una frase del cuerpo) y las muestra en el resumen:

```text
diagnóstico: remitente + asunto = 0 | remitente + cuerpo = 0 | solo remitente = 0
```

Interpretación:

| Resultado | Interpretación |
|---|---|
| **solo remitente = 0** | No hay correos de ese banco en **Todos los mensajes**. Pueden estar en Spam/Papelera, en otra cuenta o no existir. |
| **solo remitente > 0**, pero asunto = 0 | Hay correos del banco, pero el asunto real es distinto al esperado. Hay que ajustar la definición del banco. |
| **remitente + asunto > 0**, pero la búsqueda principal = 0 | La frase del cuerpo no calza. La aplicación reintenta automáticamente solo con remitente + asunto y valida cada correo con el parser. |

Si la frase del cuerpo no encuentra nada, el reintento por asunto **no guarda a ciegas**: cada correo se sigue validando y los que no corresponden se descartan con su motivo.

### 5.8 Rutina recomendada

1. Extrae con todos los bancos marcados.
2. Revisa el resumen final.
3. Si hay `descartes` o `omitidos`, lee la consola.
4. Ve a **📊 Gastos · Tarjetas** y actualiza el dashboard.
5. Clasifica los movimientos nuevos del mes.

---

## 6. Gastos: tarjetas mensuales

Abre **📊 Gastos · Tarjetas**.

### 6.1 Elegir el año

Usa el selector **📅 Año a Consultar**. La lista incluye el año actual y todos los años que tengan movimientos en la base.

### 6.2 Las 12 tarjetas

Se muestran en una cuadrícula de 4 × 3, de enero a diciembre. Cada tarjeta tiene:

- el nombre del mes;
- el **total gastado** en pesos;
- la **cantidad de transacciones** que suman;
- si corresponde, una línea como `excluye $50.000 en 2 transacciones`.

Las tarjetas **no suman** las transacciones marcadas como excluidas. Esa línea te recuerda cuánto quedó fuera y en cuántas transacciones.

### 6.3 Actualizar

Pulsa **🔄 Actualizar Dashboard** para volver a leer la base y redibujar los totales. La aplicación también actualiza el resumen automáticamente al terminar una extracción.

### 6.4 Abrir un mes

Haz clic en cualquier parte de una tarjeta. La aplicación:

- resalta la tarjeta;
- abre la pestaña **🔍 Gastos · Detalle**;
- muestra las categorías de ese mes.

### 6.5 Diferencia entre el total de la tarjeta y el detalle por categorías

El total de la tarjeta **excluye** las transacciones marcadas como **No sumar** (transferencias propias, transferencias devueltas o compras con tarjeta). El desglose por categorías **sí las muestra**, porque siguen siendo movimientos del mes. Por eso la suma de las categorías puede ser mayor que el total de la tarjeta.

Las filas excluidas aparecen en el detalle con fondo amarillo y la marca **🚫 No suma**.

---

## 7. Gastos: detalle del mes

Abre un mes desde las tarjetas de gastos o entra directamente a **🔍 Gastos · Detalle**.

### 7.1 Encabezado

Muestra el período activo, por ejemplo:

```text
📌 Período activo: MARZO de 2026
```

Si no has elegido un mes, indica que debes hacer clic en una tarjeta del resumen anual.

### 7.2 Tabla de categorías

Columnas:

| Columna | Contenido |
|---|---|
| **Categoría** | Categoría principal del movimiento. |
| **Cantidad de Transacciones** | Cuántas transacciones tiene esa categoría. |
| **Total Gastado** | Suma de esas transacciones, incluida la parte excluida. |

Las categorías se ordenan de mayor a menor total. Al seleccionar una, se cargan sus transacciones abajo.

### 7.3 Tabla de transacciones

Columnas visibles:

| Columna | Contenido |
|---|---|
| **Fecha** | Día del movimiento en formato `dd/mm/aaaa`. |
| **Banco** | MACHBANK, BANCOESTADO o SANTANDER; `EFECTIVO` en los gastos registrados a mano. |
| **Comercio** | Comercio o destinatario. En personas aparece `TRANSFERENCIA: ...` o `PAGO: ...`; en pagos de cuentas, `PAGO DE CUENTAS: ...`; en cartolas, la glosa del banco (por ejemplo, `Transferencia a ...`). |
| **Monto** | Monto en pesos. |
| **Excluida** | `🚫 No suma` si la transacción está excluida de los totales. |
| **Subcategoría** | Detalle libre asignado por ti. |
| **Tipo Tarjeta** | Tipo de tarjeta u operación (por ejemplo, `Crédito (Física)`, `Visa Débito`, `Transferencia Cuenta Principal`, `Pago de cuentas`, `Pago a persona`, `Cartola`, `Efectivo`). |

La columna **ID** existe pero está oculta; se usa internamente.

### 7.4 Eliminar una transacción

1. Selecciona la categoría y luego **una** transacción de la tabla inferior.
2. Pulsa **🗑️ Eliminar transacción**.
3. Revisa el resumen del cuadro de confirmación (fecha, banco, comercio y monto) y acepta.

El borrado **no se puede deshacer** y afecta solo a esa fila: la categoría, el mes y los totales se recalculan solos.

Qué pasa después, según el origen de la fila:

| Origen | Si vuelves a extraer o previsualizar |
|---|---|
| **Cartola PDF** | No reaparece: la cartola sigue registrada como procesada. |
| **Correo de Gmail** | Reaparece: el correo se descarga otra vez y la transacción se guarda de nuevo. |
| **Gasto en efectivo** | No reaparece (también puedes borrarlo desde Registro Manual). |

Por eso, si quieres que un gasto de Gmail no sume pero sin borrarlo, conviene clasificarlo con una categoría de excepción y marcar **No sumar a las tarjetas**.

---

## 8. Clasificar una transacción

### 8.1 Abrir la ventana

1. Selecciona una categoría en la tabla superior.
2. Selecciona **una** transacción en la tabla inferior.
3. Pulsa **✏️ Clasificar / Editar Selección**.

Si no hay una fila seleccionada, la aplicación avisa.

### 8.2 Qué muestra la ventana

- Comercio o destinatario.
- Monto, fecha y banco.
- Si ya está excluida, un aviso de que no suma en las tarjetas.
- Selector de **Categoría**.
- Campo de **Subcategoría**.
- Opciones de **Alcance de la regla**.

### 8.3 Categorías disponibles

La lista es fija:

- Alimentación y Comida
- Transporte y Combustible
- Servicios Básicos y Cuentas
- Entretenimiento y Ocio
- Salud y Farmacia
- Compras y Vestuario
- Insumos
- Transferencias y Terceros
- Deporte y Entrenamiento
- Transferencia propia
- Transferencia devuelta
- Otros Gastos
- Pendiente

**Transferencia propia** está disponible en cualquier movimiento: transferencias, pagos a personas y compras con tarjeta. Úsala para los traspasos entre tus cuentas o para excluir una compra que no debe sumar.

La aplicación asigna sola **Transferencia propia** (con **No suma**) a los cargos que son traspasos entre tus cuentas o pagos de una deuda cuyas compras ya se cuentan aparte, si todavía no tienen una regla tuya:

- `Transferencia a Cuenta Futuro`;
- `Transferencia a Ahorro 24/7`;
- `Aporte a FFMM` (fondos mutuos);
- `Pago de Tarjeta de Crédito` y `Pago de cuota por compra con crédito` (las compras con crédito ya se cuentan por su aviso);
- descripciones con `Cuenta propia`, `Transferencia propia` o `Traspaso a cuenta`.

Se reconocen por la descripción del movimiento, no por el nombre del titular: una transferencia a una persona con tu mismo nombre puede ser un gasto real. Si quieres que alguno de estos movimientos sume, clasifícalo con otra categoría; tu regla manda sobre la detección automática.

**Transferencia devuelta** la asigna el motor de cartolas cuando el banco rechaza una transferencia: el cargo aparece seguido de un abono por el mismo monto (`Devolución transferencia a cuenta bancaria`). El dinero nunca salió de la cuenta, así que la fila queda como **No suma**. No necesitas marcarla a mano.

`Pendiente` significa que el movimiento aún no está clasificado.

### 8.4 Subcategoría

Es un texto libre y opcional. Sirve para detallar el gasto. Si lo dejas vacío, la transacción queda sin subcategoría.

### 8.5 Alcance de la regla

El alcance define a qué transacciones afectará el cambio.

> **Las reglas solo llenan lo pendiente.** Una regla cambia la transacción que estás clasificando y las que siguen en **Pendiente**, y se usa para las transacciones que lleguen después. **Lo que ya clasificaste, a mano o con otra regla, no cambia.** Así el resultado es el mismo sin importar el orden en que clasifiques. El mensaje de confirmación indica a cuántas transacciones se aplicó.

Las opciones principales son:

#### En transferencias y pagos a personas

Se consideran personas tanto las operaciones que llegan por correo (`TRANSFERENCIA: ...` o `PAGO: ...`) como las que vienen en las **cartolas PDF** (`Transferencia a ...` o `Pago a ...`). Por eso las cartolas también ofrecen la regla por monto exacto. Esto incluye los traspasos entre tus cuentas que aparecen en la cartola (por ejemplo, `Transferencia a Cuenta Futuro - Cuenta MACH`): también muestran las tres opciones.

| Opción | Qué hace |
|---|---|
| **Solo esta transacción** | Cambia solo esta fila. No aprende una regla nueva y elimina la regla por monto de ese destinatario si existía. |
| **Este destinatario/comercio y monto exacto ($X)** | Aprende una regla solo para ese destinatario o comercio cuando el monto sea exactamente ese. Se aplica a esta transacción, a las pendientes con ese monto y a las futuras. Útil si la misma persona recibe pagos de distintas categorías. |
| **Repetir para comercio/persona** | Aprende una regla fija. Se aplica a esta transacción, a las pendientes y a las extracciones futuras. **Ignora el banco**: la misma persona en otro banco comparte la regla. Además borra las reglas por monto de ese destinatario. |

#### En compras con tarjeta

| Opción | Qué hace |
|---|---|
| **Solo esta compra** | Cambia solo esta fila. La regla del comercio sigue vigente para las demás. |
| **Repetir para comercio/persona** | Aprende una regla fija para ese comercio. Se aplica a esta compra, a las pendientes y a las extracciones futuras. La regla se comparte entre bancos. |

#### Casilla "No sumar a las tarjetas"

Cuando la categoría seleccionada es una excepción de gasto (**Transferencia propia** o **Transferencia devuelta**), aparece la casilla destacada **No sumar a las tarjetas**:

- **Combinada con "Repetir para comercio/persona"**: la regla fija aprende que este comercio o persona no suma. Esta transacción, las pendientes y las que se extraigan en el futuro con ese comercio quedarán marcadas automáticamente como `🚫 No suma`.
- **Combinada con "Este destinatario/comercio y monto exacto"**: aprende la regla para ese monto y destinatario con exclusión.
- **Si solo marcas "No sumar a las tarjetas"** sin elegir otra opción: la aplicación entiende automáticamente que el cambio es **solo para esta transacción**.

### 8.6 Reglas importantes

- **Exclusión automática por comercio:** al combinar "Transferencia propia" con "Repetir para comercio/persona" y "No sumar a las tarjetas", los próximos gastos de ese comercio o persona se excluirán automáticamente al extraerlos de Gmail o al importar una cartola.
- **Las reglas respetan lo ya clasificado:** una regla nueva no cambia las transacciones que ya tienen categoría. Si pusiste una regla por error y la corriges, lo que clasificó la regla anterior sigue igual: reclasifícalo una por una, o devuélvelo a **Pendiente** y vuelve a aplicar la regla.
- **Guardar una regla sin la casilla borra la exclusión de las filas que alcanza:** si aplicas "Repetir para comercio/persona" o "destinatario/comercio + monto exacto" sin marcar **No sumar**, esta transacción y las pendientes alcanzadas quedan sumando. La única excepción es **Transferencia devuelta**, que siempre queda excluida.
- **Cambiar la categoría borra la exclusión:** si a una transacción excluida le asignas una categoría normal sin marcar "No sumar", vuelve a sumar en los totales.
- **Transferencia devuelta siempre queda excluida:** si asignas esa categoría a mano, la app mantiene la marca **No suma**, incluso si desmarcas la casilla.
- **La regla fija de una persona borra las reglas por monto** de ese destinatario, para que no queden reglas contradictorias.
- **La regla fija de un comercio** se aplica a las transacciones pendientes con ese mismo nombre de comercio, sin distinguir banco, y a las futuras.
- **La regla por monto** se guarda con el destinatario tal como aparece, incluido el banco entre paréntesis. Si la misma persona aparece con otro banco, esa regla por monto no la alcanza; la regla fija sí.
- **Las cartolas no se confunden con compras:** una descripción como `Compra con tarjeta física - SHELL` sigue siendo una compra; `Transferencia a María Noguera` se trata como persona y ofrece las reglas por destinatario. Los pagos de servicios (`PAGO DE CUENTAS: ...`) no se tratan como personas.
- **Las cartolas heredan la regla completa:** un cargo de cartola que coincide con una regla toma su categoría y también su marca **No suma**.

### 8.7 Guardar

Pulsa **💾 Guardar y Aplicar**.

- Si todo sale bien, aparece un mensaje de éxito.
- La ventana se cierra.
- El resumen y el detalle se recargan conservando el mes y la categoría.

### 8.8 Quitar una exclusión

1. Abre la transacción excluida (fila amarilla, `🚫 No suma`).
2. Elige **Solo esta transacción** (o cualquier regla que corresponda).
3. Guarda.

La marca de exclusión se borra y la transacción vuelve a sumar.

---

## 9. Registrar un gasto en efectivo

Los pagos en efectivo no llegan por correo, así que se ingresan a mano en la pestaña **✍️ Registro Manual**, en el modo **🧾 Gastos en efectivo**. Quedan guardados en la misma base y **suman en los totales** del mes, las categorías y el año.

La pestaña **✍️ Registro Manual** reúne los dos tipos de registro manual: **🧾 Gastos en efectivo** y **💵 Ingresos en efectivo**. Cambia de uno a otro con los botones de arriba; cada modo tiene su propia tabla, sus botones y su total. El botón activo se ve con su color pleno (rojo para gastos, verde para ingresos) y el otro queda en una versión suave del mismo color, para que siempre sepas qué estás viendo.

### 9.1 Agregar un gasto

1. Abre **✍️ Registro Manual** y elige **🧾 Gastos en efectivo**.
2. Pulsa **➕ Nuevo gasto en efectivo**.
3. Completa el formulario:
   - **Fecha**: día, mes y año. Si tienes un mes abierto en el detalle, se propone ese mes.
   - **Comercio o descripción**: por ejemplo `FERIA`, `ALMACÉN` o `PAGO A JUAN`.
   - **Monto (CLP)**: solo pesos enteros. Puedes escribir `12500` o `12.500`.
   - **Categoría**: la misma lista que usa la clasificación.
   - **Subcategoría**: opcional; si la dejas vacía se guarda como `Sin Clasificar`.
4. Si quieres que ese comercio quede aprendido, marca **Recordar esta categoría para este comercio**.
5. Pulsa **💾 Guardar**.

El gasto aparece de inmediato en la tabla con el origen `EFECTIVO` y el tipo `Efectivo`, y el resumen superior muestra cuántos gastos hay y su total.

### 9.2 Editar o eliminar

- Selecciona una fila y pulsa **✏️ Editar** (o haz doble clic sobre ella) para cambiar fecha, comercio, monto, categoría o subcategoría.
- Selecciona una fila y pulsa **🗑️ Eliminar**. La aplicación pide confirmación.
- **🔄 Actualizar** vuelve a leer la base y redibuja la tabla.

Solo se pueden editar o eliminar los gastos creados en esta pestaña. Los movimientos extraídos de Gmail no se borran **desde aquí**: se clasifican, se excluyen o se eliminan en **🔍 Gastos · Detalle**.

### 9.3 Cómo se reflejan en el panel

- El mes de la fecha elegida suma el gasto en su tarjeta de **Gastos · Tarjetas**.
- La categoría aparece en **Gastos · Detalle** con su monto.
- En la columna **Banco** se muestra `EFECTIVO` y en **Tipo Tarjeta**, `Efectivo`.
- La extracción de Gmail no los toca ni los duplica.

> Si registras el mismo comercio, monto y fecha dos veces, se guardan las dos filas: la aplicación entiende que son dos gastos distintos, no un duplicado.

---

## 10. Ingresos

Los ingresos tienen su propio módulo, separado de los gastos. Se guardan en una tabla distinta, con sus categorías, sus excepciones y sus tarjetas. **No se mezclan con los totales de gastos.**

### 10.1 Las dos pestañas

- **💰 Ingresos · Tarjetas**: muestra los 12 meses del año elegido, con el total recibido, la cantidad de ingresos y una línea con lo que quedó excluido. Arriba aparece el total anual.
- **💵 Ingresos · Detalle**: muestra las categorías del mes y, al elegir una, los ingresos correspondientes.

Al hacer clic en una tarjeta mensual se abre automáticamente **Ingresos · Detalle** con ese mes activo.

### 10.2 Categorías y excepciones

Categorías que **suman** en las tarjetas:

- Sueldo y Honorarios
- Transferencias recibidas
- Ventas
- Intereses y Dividendos
- Subsidios y Bonos
- Otros Ingresos
- Pendiente (aún sin clasificar)

Categorías de **excepción**, que quedan visibles pero **no suman**:

- **Transferencia propia**: dinero que viene de otra cuenta tuya.
- **Préstamo recibido**: entra dinero, pero es una deuda.
- **Reembolso**: devolución de un gasto, no un ingreso nuevo.

Las excepciones se marcan solas al guardar o clasificar el ingreso. En el detalle aparecen con la etiqueta **🚫 No suma** y la fila resaltada.

Cuando una transferencia se devuelve, la cartola trae dos filas: el cargo (que se clasifica como **Transferencia devuelta** y no suma en gastos) y el abono (`Devolución transferencia a cuenta bancaria`, que entra como **Reembolso** y tampoco suma en ingresos). Así el par no infla ningún total.

### 10.3 Registrar un ingreso manual

La creación y edición de ingresos en efectivo está en **✍️ Registro Manual**, en el modo **💵 Ingresos en efectivo**, para no duplicar botones en las pestañas de Ingresos.

1. Abre **✍️ Registro Manual** y elige **💵 Ingresos en efectivo**.
2. Pulsa **➕ Nuevo ingreso en efectivo**.
3. Completa fecha, descripción, monto, categoría y subcategoría.
4. Si quieres que esa descripción quede aprendida, marca **Recordar esta categoría para esta descripción**.
5. Pulsa **💾 Guardar**.

El ingreso aparece en el mes de su fecha. Si la categoría es una excepción, se guarda como **No suma** automáticamente.

### 10.4 Editar, clasificar y eliminar

- **✏️ Clasificar / Editar Selección** (en **💵 Ingresos · Detalle**): cambia la categoría y la subcategoría de un ingreso. Puedes aplicarlo **solo a ese ingreso** o como regla para **esa descripción**: se aplica a este ingreso, a los que siguen en **Pendiente** y a los futuros. Los ingresos que ya clasificaste no cambian.
- **🗑️ Eliminar ingreso** (en **💵 Ingresos · Detalle**): borra el ingreso seleccionado después de confirmar. No se puede deshacer. Si vino de una cartola, no vuelve a aparecer mientras esa cartola siga procesada; los ingresos registrados a mano también se pueden borrar desde **Registro Manual → Ingresos en efectivo**.
- En **✍️ Registro Manual → 💵 Ingresos en efectivo**: **✏️ Editar** cambia fecha, descripción, monto, categoría o subcategoría; **🗑️ Eliminar** borra el ingreso con confirmación.
- Doble clic sobre una fila en **Ingresos · Detalle**: edita el ingreso si es manual; si vino de Gmail o de una cartola, abre la clasificación.

Los ingresos de Gmail y de cartolas se pueden eliminar desde **💵 Ingresos · Detalle** con **🗑️ Eliminar ingreso**. Un ingreso de cartola no vuelve mientras la cartola siga procesada; si viniera de Gmail, reaparecería en la próxima extracción. Si solo quieres que no sume, clasifícalo con una categoría de excepción (**Transferencia propia**, **Préstamo recibido** o **Reembolso**).

### 10.5 Cartolas PDF

Los ingresos que vienen de una cartola se cargan desde la pestaña **📄 Cartolas PDF** (ver el capítulo 11). La cartola también completa los gastos que falten, así que no es necesario registrarlos a mano.

---

## 11. Cartolas PDF

La pestaña **📄 Cartolas PDF** descarga el adjunto PDF de las cartolas desde Gmail, lo lee y prepara sus movimientos. Trabaja en **dos etapas**: primero muestra una **vista previa** y nada se guarda hasta que presiones **✅ Aplicar lo revisado**.

### 11.1 Bancos soportados

| Banco | Cartola | Clave |
|---|---|---|
| **MACHBANK** | Cuenta corriente | Puede venir cifrada; se abre con la clave de cartolas |
| **SANTANDER** | Cuenta corriente | Siempre cifrada: RUT sin guion ni dígito verificador |
| **BANCOESTADO** | CuentaRUT (formato vertical antiguo y apaisado nuevo) | Siempre cifrada con los **4 últimos dígitos** del RUT; la app los toma de la clave guardada |

La búsqueda usa el remitente oficial de cada banco y solo toma correos con adjunto PDF. También revisa los correos reenviados.

En MachBank la búsqueda acepta los remitentes `contacto@mail.somosmach.com`, `noreply@somosmach.com` y `contacto@mail.machbank.cl`, y el asunto **"Cartola Cuenta Corriente"**. El banco cambió el asunto en abril de 2025 (agregó `MACHBANK`) y el remitente en junio de 2025 (pasó a `machbank.cl`); la búsqueda amplia encuentra las cartolas de ambos períodos. Desde 2026 la cartola agrega una columna **Saldo**; la app la ignora y sigue leyendo solo **Egreso** e **Ingreso**, así que el resultado no cambia.

En BancoEstado la búsqueda usa el remitente `bancoestado.cl` y el asunto **"Cartola"**, y toma solo adjuntos PDF. La cartola de CuentaRUT viene cifrada: el banco pide como contraseña los últimos cuatro dígitos del RUT sin dígito verificador (por ejemplo, RUT 12.345.678-9 → `5678`). No tienes que escribirla aparte: la app la deriva del RUT que ya guardaste.

La CuentaRUT tiene dos formatos: el antiguo, vertical, y el nuevo (`Cartola_CuentaRUT.pdf`), apaisado y con un movimiento por línea. La app lee ambos. Como la CuentaRUT menciona otros bancos en sus transferencias (“TEF A … SANTANDER”), la app la reconoce por su encabezado (“ESTADO DE MOVIMIENTOS · CuentaRUT”) y no la confunde con una cartola de esos bancos.

### 11.2 Guardar la clave de cartolas

Las cartolas de Santander y BancoEstado siempre vienen cifradas y algunos meses de MachBank también. La clave que se guarda es el **RUT del titular sin guion y sin dígito verificador**, y sirve para los tres bancos: BancoEstado usa automáticamente sus 4 últimos dígitos.

1. En **📄 Cartolas PDF**, escribe el RUT en el campo **Clave de cartolas**. Puedes escribirlo con puntos y guion: la app limpia el formato y descarta el dígito verificador.
2. Pulsa **🔒 Guardar clave**. También puedes escribirla y pulsar directamente **🔎 Previsualizar cartolas**: la app la guarda sola antes de leer.
3. La clave queda guardada **cifrada** en `cartolas_clave.enc`, con la misma llave local que la contraseña de aplicación de Gmail. No se vuelve a pedir y nunca se muestra en pantalla.

Si cambias de titular o de RUT, borra el archivo `cartolas_clave.enc` con la aplicación cerrada y guarda la clave nueva.

### 11.3 Previsualizar

1. Marca los bancos que quieres revisar (vienen todos marcados).
2. Pulsa **🔎 Previsualizar cartolas**.
3. Espera mientras la consola **Registro de cartolas** muestra los correos encontrados y las cartolas leídas. Si necesitas ver más líneas, arrastra hacia arriba la línea punteada que separa la tabla de la consola: la tabla se achica y el registro crece. El reparto queda como lo dejaste al cambiar de pestaña.
4. Revisa la tabla:

| Columna | Significado |
|---|---|
| **Banco** | Banco de la cartola. |
| **Fecha** | Fecha del movimiento. |
| **Tipo** | **INGRESO** (abono) o **GASTO** (cargo). |
| **Descripción** | Texto tal como aparece en la cartola. |
| **Monto** | Monto del movimiento en pesos. |
| **Categoría** | Clasificación propuesta. |
| **Estado** | Nuevo, ya guardado, conciliado, para revisar, sin movimientos o error. |

Estados posibles:

- **Nuevo ingreso / Nuevo gasto**: se guardará al aplicar.
- **Ingreso ya guardado / Gasto ya guardado**: ya existe en la base y no se duplica.
- **Conciliado con gasto**: el cargo corresponde a un gasto que ya estaba registrado; no se inserta de nuevo.
- **Cartola ya procesada**: esa cartola ya se aplicó antes.
- **REVISAR**: los totales que declara el banco no calzan con los movimientos leídos, o no se pudieron leer. Debajo se muestran sus movimientos para que los revises. Solo se aplica si lo confirmas (ver 11.6).
- **INFO · Sin movimientos en el período**: el banco declara ingresos y egresos en cero (un mes sin uso de la cuenta). No falta nada; al aplicar queda registrada como procesada.
- **ERROR**: la cartola no se pudo abrir o leer, por ejemplo porque la clave no la abre. No se aplica.

La vista previa **no modifica la base de datos**.

### 11.4 Ver la cartola y dónde queda guardada

Cada PDF que se descarga queda archivado en la carpeta del programa, ordenado por banco y período:

```text
Cartolas\BANCOESTADO\2020-08-26_2021-01-18_Cartola.pdf
Cartolas\SANTANDER\2026-08-31_2026-09-30_Cartola.pdf
```

El nombre empieza con el período, así que dentro de cada banco los archivos quedan en orden cronológico. Si vuelves a previsualizar la misma cartola no se duplica el archivo: solo se reescribe si el PDF cambió.

Para verla:

1. Selecciona cualquier fila de esa cartola en la tabla de la vista previa.
2. Pulsa **👁️ Ver cartola** (o haz doble clic sobre la fila).
3. Se abre el visor interno: **◀ ▶** cambian de página, **🔍− / 🔍+** cambian el zoom y las flechas del teclado también sirven.
4. **🖨️ Abrir con el visor de Windows** queda como respaldo si prefieres Edge o Adobe.

El botón **📚 Cartolas guardadas** lista todos los PDF archivados, incluso los de meses anteriores, con su banco, período y tamaño; con doble clic se abren igual que en la vista previa.

Las cartolas archivadas siguen cifradas tal como llegaron del banco: el visor usa la misma clave de cartolas que ya guardaste. Si cambias de titular, los archivos antiguos dejarán de abrirse con la clave nueva.

### 11.5 Aplicar

1. Revisa la tabla y la consola.
2. Pulsa **✅ Aplicar lo revisado** y confirma.
3. Al terminar, la app recarga las tarjetas de gastos e ingresos.

Qué hace exactamente:

- Los **abonos** se guardan en la tabla de ingresos, con su categoría y subcategoría.
- Las **transferencias a cuentas propias**, los **préstamos recibidos** y los **reembolsos** se marcan como excepción y no suman en las tarjetas de ingresos.
- Si un cargo de transferencia va seguido de un abono por el mismo monto (`Devolución transferencia a cuenta bancaria`), el cargo se clasifica como **Transferencia devuelta** y tampoco suma en gastos. El par completo queda fuera de los totales, porque el dinero nunca salió de la cuenta.
- Los **cargos** se buscan primero en los gastos existentes del mismo banco y monto, con la fecha de la cartola o hasta 4 días antes (el aviso llega al instante y el banco contabiliza el cargo después). Si coinciden, se **concilian** y no se duplican.
- La descripción también cuenta: si el único gasto del día con ese monto es de un comercio claramente distinto (por ejemplo, “UBER” frente a “CAFÉ”), no se concilia. Cuando hay varios candidatos, cada cargo se empareja con el gasto más parecido, sin importar el orden del extracto.
- Las compras con tarjeta de **crédito** nunca se concilian con la cartola de la cuenta corriente, porque no pasan por ella.
- Los cargos que no existen se insertan como gastos con tipo de tarjeta **Cartola**. Si coinciden con una regla tuya, toman su categoría y su marca **No suma**; si son traspasos a cuentas propias o pagos de tarjeta, entran como **Transferencia propia**.
- Si dos cargos idénticos del mismo día existen de verdad, cada uno se concilia o se inserta por separado.

En la vista previa, las filas de una transferencia devuelta se ven con fondo crema y el detalle **Transferencia devuelta: no suma**. La devolución aparece como **Devolución de la transferencia**.

### 11.6 Seguridad de los totales

Antes de aceptar una cartola, la app compara los **totales declarados por el banco** con la suma de los movimientos leídos.

- Si **calzan**, la cartola se aplica normalmente.
- Si **no calzan**, o el PDF no trae totales legibles, la cartola aparece con una fila **REVISAR** que muestra la diferencia. No se bloquea, porque el error puede ser de la lectura y los movimientos estar bien; tampoco se aplica sin avisarte.
- Al pulsar **✅ Aplicar lo revisado**, si hay cartolas para revisar, la app pregunta:
  - **Sí**: aplica todo, incluidas esas cartolas.
  - **No**: aplica solo las cartolas que cuadran. Las otras quedan sin procesar; para incluirlas más adelante, vuelve a previsualizar y confirma.
  - **Cancelar**: no aplica nada.

Si una cartola sigue apareciendo para revisar mes a mes, probablemente el banco cambió el formato del PDF.

### 11.7 Deduplicación

- Cada movimiento recibe un identificador estable (`CARTOLA-...`) calculado con banco, período, fecha, descripción y monto.
- La tabla `cartolas_procesadas` recuerda la huella del PDF aplicado.
- Volver a previsualizar o aplicar la misma cartola no duplica ingresos ni gastos.

### 11.8 Cancelar y limpiar

- **🛑 Cancelar** detiene la descarga al terminar el correo actual. Lo que ya se aplicó se conserva y el resumen indica que se canceló.
- Mientras las cartolas se previsualizan o aplican, el botón **🚀 Extraer todo** queda deshabilitado, y al revés: los dos procesos no escriben en la base al mismo tiempo.
- **🧹 Limpiar vista** borra la tabla y descarta la vista previa, sin tocar la base.

### 11.9 Problemas frecuentes

| Problema | Qué revisar |
|---|---|
| No aparecen cartolas | Que el correo esté en Gmail, venga del remitente oficial y tenga el PDF adjunto. |
| Santander o BancoEstado piden clave | Guarda el RUT sin guion ni dígito verificador. BancoEstado usa sus 4 últimos dígitos, que la app deriva sola. |
| La clave no abre el PDF | Verifica el RUT del titular. Si pegaste el RUT completo, la app descarta el último dígito. |
| No puedo ver una cartola guardada | La carpeta `Cartolas/` se movió o se borró. Vuelve a previsualizar esa cartola: se archiva de nuevo sin duplicar movimientos. |
| Una cartola aparece para revisar | Sus totales no calzan con lo leído, o no se pudieron leer. Revisa sus movimientos en la tabla y decide al aplicar. |
| Una cartola aparece sin movimientos | El banco declara ingresos y egresos en cero: la cuenta no tuvo uso ese período. No falta nada. |
| Un cargo no se concilió | El gasto existente tiene otro monto u otro banco, una fecha fuera del rango (hasta 4 días antes de la cartola), o una descripción claramente distinta. Se insertará como gasto nuevo. |
| Algunas cartolas de Santander no abren | La app guarda una sola clave de cartolas. Si tienes cuentas a nombre de otro RUT, esas cartolas no abren con tu clave. |
| Veo dos cargos iguales el mismo día | Pueden ser dos compras reales. Si es una transferencia seguida de una devolución por el mismo monto, el cargo queda como **Transferencia devuelta** y no suma. |

---

## 12. Flujo de trabajo sugerido

1. **Extrae** todos los bancos una vez al mes, o con más frecuencia.
2. Revisa el **resumen final** y la consola.
3. Abre **📊 Gastos · Tarjetas** y elige el año.
4. Entra al mes que quieres ordenar.
5. Revisa las categorías con más gasto.
6. Clasifica primero los comercios repetidos usando **Repetir para comercio/persona**: así la regla llena de una vez todo lo pendiente de ese comercio.
7. Para personas, usa **Repetir para comercio/persona** si siempre son del mismo tipo; usa **destinatario/comercio + monto exacto** si varía. Esta opción también aparece en las transferencias que vienen de una cartola PDF.
8. Marca como **Transferencia propia** + **No sumar a las tarjetas** los traspasos entre tus propias cuentas y las compras con tarjeta que no deban sumar. Los traspasos a Cuenta Futuro, Ahorro 24/7, fondos mutuos y los pagos de tarjeta ya se reconocen solos.
9. Registra en **✍️ Registro Manual** los gastos pagados en efectivo y los ingresos en efectivo.
10. Abre **📄 Cartolas PDF**, previsualiza y aplica lo revisado para completar ingresos y gastos. Si alguna cartola aparece para revisar, mira sus movimientos antes de decidir.
11. Actualiza el dashboard y verifica los totales.

---

## 13. Solución de problemas

### La aplicación no abre

- **Espera unos segundos.** El programa se prepara antes de mostrar la ventana, sobre todo la primera vez o después de reiniciar el computador. Evita hacer doble clic varias veces.
- **Windows muestra «Windows protegió su PC»:** presiona **Más información** y luego **Ejecutar de todas formas**.
- **El antivirus lo bloqueó o lo borró:** algunos antivirus desconfían de los programas sin firma digital. Restáuralo desde la cuarentena del antivirus y márcalo como permitido.
- **Hay otra ventana del programa abierta:** revisa la barra de tareas; puede estar detrás de otras ventanas.
- **Está en una carpeta sin permisos de escritura** (por ejemplo, `Archivos de programa`) o en una carpeta de OneDrive que todavía no termina de sincronizar: muévelo a una carpeta propia, como `Documentos\Registro Financiero`, junto con sus archivos de datos.
- **Reinicia el computador** e inténtalo de nuevo.

Si sigue sin abrir, escribe al autor indicando tu versión de Windows y qué ocurre al hacer doble clic (si aparece algún mensaje, una captura ayuda).

### La pestaña Ayuda muestra la guía rápida en vez del manual completo

El manual viene dentro del programa, así que esto no debería ocurrir. Si pasa, cierra el programa y ábrelo de nuevo. Si continúa, descarga otra vez el programa desde el enlace que te envió el autor y reemplaza el `.exe` (tus datos no se tocan: están en archivos aparte, en la misma carpeta).

### No puedo iniciar sesión

- Usa la **contraseña de aplicación**, no la normal.
- Verifica que la verificación en dos pasos esté activa.
- Copia la contraseña sin espacios (la app también los ignora).
- Comprueba la conexión a internet.
- Si revocaste la contraseña anterior, genera una nueva.
- Si aparece **«Tu licencia es para el Gmail …»**, escribiste una cuenta distinta a la de tu clave. Usa el Gmail que indica el mensaje (también aparece en *❓ Ayuda → ℹ️ Acerca de*). Si ahora usas otra cuenta, pide una clave para ella (ver *Preguntas frecuentes → ¿Puedo usar otra cuenta de Gmail?*).

### Cambié de computador y no reconoce mis credenciales

Copia la carpeta completa del programa, o al menos estos archivos junto al `.exe`:

- `registro_financiero.db` (datos);
- `licencia.txt` (tu clave; si no lo copias, vuelve a pegarla en *❓ Ayuda → ℹ️ Acerca de → 🔑 Licencia*);
- `secret.key` (llave de cifrado);
- `credentials.enc` (credenciales cifradas);
- `cartolas_clave.enc` (clave de cartolas cifrada);
- `Cartolas/` (cartolas PDF archivadas; opcional).

Si no copias `secret.key`, deberás volver a ingresar el correo, la contraseña de aplicación y la clave de cartolas.

### Un banco muestra 0 correos

Mira la línea `diagnóstico:` del resumen:

- **solo remitente = 0**: no hay correos de ese banco en **Todos los mensajes**. Revisa Spam/Papelera o si la cuenta es la correcta.
- **solo remitente > 0 y asunto = 0**: el asunto cambió. Habría que ajustar la definición del banco. Algunos tipos tienen 0 de forma normal: por ejemplo, si nunca pagaste cuentas con MachBank.
- **remitente + asunto > 0**: la frase del cuerpo no calza; la aplicación reintenta sola por asunto.

### Santander encuentra correos pero no guarda ninguno

Si el resumen muestra `descartes: INGRESO=N`, son avisos de **transferencias recibidas**, no realizadas. Es el comportamiento esperado: la extracción desde Gmail solo registra salidas. Esas transferencias recibidas entran como ingresos al aplicar las **📄 Cartolas PDF**.

### BancoEstado descarta compras como TIPO NO SOPORTADO

BancoEstado solo procesa compras con **tarjeta de débito**. Se descartan como `TIPO NO SOPORTADO` las compras con crédito y los avisos de 2019 (“Notificacion de compra”, sin tilde) que no dicen el tipo de tarjeta.

### Faltan registros o el número no cuadra

1. Vuelve a extraer: los correos que no se guardaron se reintentan.
2. Revisa si el resumen muestra `omitidos` y lee el motivo en la consola.
3. `duplicado exacto` significa que esa transacción ya estaba guardada.
4. `duplicado de una cartola ya importada` significa que la cartola PDF ya registraba ese
   gasto; no falta nada.
5. `aviso repetido: la cartola registra una sola compra` significa que el banco mandó dos
   correos por la misma compra; se cuenta una vez.
6. Si el motivo es un error de base, cierra otras aplicaciones que puedan estar usando el archivo y vuelve a intentar.

### La base está bloqueada o da error al guardar

- Cierra otras instancias de la aplicación.
- Cierra visores de SQLite que tengan abierto `registro_financiero.db`.
- La aplicación espera hasta 30 segundos si el archivo está ocupado; si el error persiste, reinicia el equipo.

### Los correos reenviados no se procesan

La aplicación valida que el remitente pertenezca al dominio oficial del banco. Un correo reenviado manualmente aparece con tu dirección o con la del servicio de reenvío, por lo que se descarta como `REMITENTE`. Es intencional, para evitar duplicados y correos falsos.

### Apliqué una regla y las transacciones antiguas no cambiaron

Es el comportamiento esperado si esas transacciones **ya tenían una categoría**: una regla solo llena las que siguen en **Pendiente**, más la que estás clasificando. Así no se pierden las clasificaciones que hiciste antes, a mano o con otra regla.

Si quieres que la regla alcance también a esas filas:

1. Reclasifícalas una por una con **Solo esta compra / transacción**, o
2. Devuélvelas a **Pendiente** (clasificándolas con esa categoría y **Solo esta…**) y vuelve a aplicar la regla con **Repetir para comercio/persona**.

### La fecha no coincide con la del correo

La fecha se toma del cuerpo del aviso. Si el cuerpo no la trae, se usa la fecha del encabezado del correo, convertida a la hora local del equipo. Los pagos a personas de MachBank usan siempre la fecha del encabezado porque ese correo no trae fecha en el texto. Los pagos de cuentas de MachBank sí traen `Fecha y hora` en el cuerpo, en formato `aaaa-mm-dd`, y usan el encabezado solo como respaldo.

### No puedo iniciar la extracción o las cartolas

Si aparece el aviso *“Espera a que termine … antes de iniciar otro proceso”*, el otro proceso todavía está trabajando. La extracción y las cartolas no pueden escribir en la base al mismo tiempo. Espera a que termine, o cancélalo.

### Versión de prueba: pide una clave o dice «solo lectura»

En la versión de prueba, la ventana **Licencia de prueba** se abre al iniciar si todavía no tienes clave o si la tuya venció.

**¿Todavía no tienes clave?** La prueba es gratis. Presiona **✉️ Pedir mi clave gratis**: se abre Gmail con un correo para el autor ya redactado. Completa tu nombre y el Gmail donde te llegan los avisos del banco, y envíalo. Recibirás tu clave por correo. Si la prueba ya terminó, el botón dice **✉️ Pedir más tiempo**. También puedes escribir directamente a la dirección que aparece junto al botón (al hacer clic sobre ella se copia).

1. Copia completa la clave que recibiste por correo (empieza con `RFM1-`). Si en el correo se ve cortada en varias líneas, cópiala igual: la app junta las partes.
2. Pégala en la caja y pulsa **Activar clave**.
3. El título de la ventana muestra cuántos días quedan.

Cuando la prueba termina, la app queda en **solo lectura**: puedes ver, clasificar y revisar todos tus datos, pero no extraer correos, leer o aplicar cartolas ni registrar o editar movimientos en efectivo. Para seguir, usa el botón **✉️ Pedir más tiempo** de la ventana de licencia (o escribe al autor) y, cuando recibas la clave nueva, actívala en *❓ Ayuda → ℹ️ Acerca de → 🔑 Licencia*. Cambiar la fecha del computador no devuelve días.

La clave está **atada a tu Gmail**: el programa solo acepta configurar la cuenta para la que se emitió (la que recibe los avisos de tus bancos). Si el título dice «Licencia de otro Gmail», configura esa cuenta o pide una clave para la tuya. Si cambias de Gmail, pide una clave nueva: la pegas en *❓ Ayuda → ℹ️ Acerca de → 🔑 Licencia* y el programa te ofrece configurar la cuenta nueva.

Si recibes una **licencia completa**, se activa igual (*❓ Ayuda → ℹ️ Acerca de → 🔑 Licencia*): el título pasa a decir «Licencia completa», ya no hay cuenta regresiva y no necesitas reinstalar. Tus datos se mantienen.

### La aplicación se cerró durante una extracción

Lo que ya se había guardado se conserva. Vuelve a abrirla y extrae de nuevo: los correos ya guardados se omiten y los pendientes se procesan.

---

## 14. Datos, respaldo y privacidad

### Dónde están los datos

Todo se guarda en la misma carpeta del programa:

- `registro_financiero.db`: transacciones, ingresos, reglas, cartolas procesadas y correos descartados. Antes se llamaba `gastos_machbank.db`; si solo existe ese archivo, la app lo renombra sola al abrir.
- `secret.key`, `credentials.enc` y `cartolas_clave.enc`: credenciales y clave de cartolas cifradas.
- `licencia.txt`: tu clave de licencia.
- `Cartolas/<BANCO>/`: los PDF descargados, uno por cartola y ordenados por período. Siguen cifrados como los entrega el banco.
- `registro_financiero.db.bak-AAAAMMDD-HHMMSS`: respaldos automáticos creados antes de una migración o de una limpieza de duplicados.

### Cómo respaldar

1. Cierra la aplicación.
2. Copia `registro_financiero.db` a un lugar seguro.
3. Si quieres conservar las credenciales y la clave de cartolas, copia también `secret.key`, `credentials.enc` y `cartolas_clave.enc`. Copia también `licencia.txt`, con tu clave.
4. La carpeta `Cartolas/` es opcional en el respaldo: la base guarda los movimientos y los totales; la carpeta solo conserva los PDF para consultarlos.

Lo más simple es copiar **la carpeta completa del programa** (con la aplicación cerrada) a un pendrive o a la nube.

### Cómo restaurar un respaldo

1. Cierra la aplicación.
2. Renombra la base actual, por ejemplo `registro_financiero.db.actual`.
3. Copia el respaldo y renómbralo como `registro_financiero.db`.
4. Abre la aplicación.

### Cómo empezar de cero

1. Cierra la aplicación.
2. Renombra o elimina `registro_financiero.db` (y sus respaldos, si quieres).
3. Abre la aplicación. Se creará una base vacía.

Las credenciales y la clave de cartolas se conservan mientras no borres `secret.key`, `credentials.enc` y `cartolas_clave.enc`.

Al empezar de cero también se pierden las reglas de clasificación, porque viven en la base. Si cambiaste de cuenta, es mejor clasificar desde cero: las reglas de otra cuenta pueden no servir.

### Privacidad

- La conexión es de solo lectura: la aplicación no modifica ni marca correos como leídos.
- No envía datos a ningún servidor propio ni a terceros.
- Las credenciales están cifradas, pero la llave vive en el mismo equipo. Protégelo con contraseña de Windows y no compartas la carpeta.
- La base contiene información financiera personal: trátala como un documento sensible.
- Tus copias de respaldo pueden tener la base y las credenciales cifradas; guárdalas en un lugar protegido.

---

## 15. Preguntas frecuentes

**¿Puedo usar otra cuenta de Gmail?**
Solo la cuenta para la que se emitió tu clave: la licencia está **atada a ese Gmail** (lo ves en *❓ Ayuda → ℹ️ Acerca de*), y el programa no acepta configurar otro. Si lo intentas, aparece el mensaje «Tu licencia es para el Gmail …».

Si cambiaste de Gmail (por ejemplo, ahora los avisos de tu banco llegan a otra cuenta):

1. Escribe al autor (su correo aparece en *❓ Ayuda → ℹ️ Acerca de*) indicando tu Gmail nuevo, y pide una clave para esa cuenta.
2. Cuando la recibas, pégala en *❓ Ayuda → ℹ️ Acerca de → 🔑 Licencia*.
3. El programa te ofrecerá configurar el Gmail nuevo: ingresa esa cuenta y su contraseña de aplicación.

Tus datos se conservan: la base es la misma y los movimientos de la cuenta nueva se agregan a los que ya tenías.

El programa lee **una sola cuenta de Gmail**. Si tus bancos avisan a cuentas distintas, configúralos para que avisen todos al Gmail de tu licencia (reenviar los correos a mano no sirve: la extracción solo procesa los avisos que envía el propio banco).

**¿Se descargan los correos o se leen desde Gmail?**
Se descargan temporalmente para interpretarlos y se guardan solo los datos de la transacción en la base local. Los correos no se copian a la base ni se modifican en Gmail.

**¿Qué pasa si el mismo correo llega dos veces?**
Se guarda una sola vez. Si el banco reutiliza el mismo identificador en un correo con contenido distinto, la segunda transacción se guarda con un sufijo interno para no perderla.

**¿Por qué una compra con crédito de BancoEstado no aparece?**
Porque ese banco solo procesa transferencias y débito. Las compras con crédito se descartan como `TIPO NO SOPORTADO`.

**¿Por qué un traspaso a mi Cuenta Futuro o un pago de tarjeta no suma en los gastos?**
Porque no es un gasto: el dinero pasa a otra cuenta tuya, o paga compras con crédito que ya se cuentan por su aviso. La app los clasifica solos como **Transferencia propia**. Si quieres que alguno sume, clasifícalo con otra categoría.

**Si clasifico una transacción a mano y después creo una regla, ¿se pierde mi clasificación?**
No. Una regla solo llena lo que está en **Pendiente** y la transacción que estás clasificando. Lo que ya clasificaste se respeta, sin importar el orden.

**El banco me manda dos correos por la misma compra, ¿se cuenta dos veces?**
No, si la cartola de ese período ya está aplicada: la cartola registra la compra una vez y el segundo aviso se omite como repetido. Si la cartola todavía no está aplicada, se guardan los dos; al aplicar la cartola, uno se concilia con su cargo.

**¿Por qué una transferencia recibida no aparece en Gastos?**
Porque los ingresos son un módulo aparte. La extracción de gastos descarta los avisos de dinero recibido como `INGRESO`; esos movimientos entran por **📄 Cartolas PDF** o a mano en **✍️ Registro Manual → 💵 Ingresos en efectivo**.

**¿Los ingresos se mezclan con los gastos?**
No. Tienen su propia tabla, sus categorías, sus excepciones y sus tarjetas. Un ingreso nunca suma en **Gastos · Tarjetas** y un gasto nunca suma en **Ingresos · Tarjetas**.

**¿Puedo editar un monto o una fecha?**
En los movimientos extraídos de Gmail no: se respeta lo que informa el banco. En los gastos e ingresos en efectivo sí, desde sus formularios de edición.

**¿Puedo borrar una transacción?**
Sí, desde **🔍 Gastos · Detalle** con **🗑️ Eliminar transacción** y desde **💵 Ingresos · Detalle** con **🗑️ Eliminar ingreso**. El borrado no se puede deshacer y no afecta a las demás filas. Una fila de cartola no vuelve; una de Gmail reaparece si vuelves a extraer, porque el correo sigue en la cuenta. Si solo quieres que no sume, clasifícala con una categoría de excepción y marca **No sumar a las tarjetas**.

**¿Se pierden las cartolas si no las aplico?**
No. Cada PDF descargado se archiva en `Cartolas/<BANCO>/` al previsualizarlo, aunque después no lo apliques. El botón **📚 Cartolas guardadas** las lista todas.

**¿Puedo agregar otro banco?**
Por ahora el programa lee MachBank, BancoEstado y Santander, de Chile. Agregar un banco requiere una versión nueva del programa: si te interesa uno en particular, escríbele al autor (su correo aparece en *❓ Ayuda → ℹ️ Acerca de*).

**¿Dónde está el manual?**
En la pestaña **❓ Ayuda** del programa, con índice y búsqueda. Viene dentro del programa: no necesitas descargarlo aparte. Para imprimirlo, usa **📖 Abrir documento actual**.

**¿Dónde veo los errores detallados?**
En la consola de la pestaña de extracción y en la ventana de resumen final. Los errores de un banco no detienen a los demás.

**¿Qué pasa con mis datos cuando termina la prueba?**
Nada: siguen en tu equipo y los puedes ver y clasificar. Solo se desactiva agregar movimientos nuevos hasta que actives otra clave.

**Windows dice «Editor desconocido» al abrir el `.exe`. ¿Es un problema?**
No: significa que el programa no tiene firma digital, un certificado pagado que Windows usa para reconocer al editor. Por eso, la primera vez Windows puede mostrar **«Windows protegió su PC»**: presiona **Más información** y luego **Ejecutar de todas formas**. Los datos del programa (empresa, versión, autor) están en clic derecho → *Propiedades* → *Detalles*. Si el archivo llegó por internet, correo o USB y Windows lo sigue bloqueando, en *Propiedades* marca **Desbloquear** y acepta.

---

## 16. Glosario

| Término | Significado |
|---|---|
| **Message-ID** | Identificador único del correo. Se usa para no guardar dos veces la misma transacción. |
| **Referencia externa** | Número de operación que informa el banco (por ejemplo, el N° de TEF de BancoEstado o el identificador de pago de MachBank). |
| **Pago de cuentas** | Pago de un servicio (celular, luz, agua, etc.) informado por MachBank en el correo “Tu pago de cuentas con MACHBANK”. |
| **Gasto en efectivo** | Pago ingresado a mano en **✍️ Registro Manual**. Se guarda con banco `EFECTIVO` y tipo `Efectivo`. |
| **Ingreso en efectivo** | Dinero recibido ingresado a mano en **✍️ Registro Manual → 💵 Ingresos en efectivo**. Se guarda con banco y origen `MANUAL`. |
| **Excepción de ingreso** | Categoría de ingreso que no suma: **Transferencia propia**, **Préstamo recibido** o **Reembolso**. |
| **Descarte** | Correo rechazado antes de guardar (remitente, asunto, cuerpo o parser). Los descartes definitivos se recuerdan y no se vuelven a descargar. |
| **Omitido** | Correo interpretado correctamente que la base no guardó por duplicado, porque una cartola ya lo registraba o por error. |
| **Aviso repetido** | Segundo correo del banco por una compra que la cartola registra una sola vez. Se omite. |
| **Conciliación** | Asociar un cargo de cartola con el gasto que ya venía de un correo, para no contarlo dos veces. |
| **Transferencia propia** | Traspaso entre cuentas propias o compra que no debe sumar. Se puede excluir de los totales mensuales. |
| **Transferencia devuelta** | Cargo de una transferencia que el banco rechazó y devolvió el mismo monto. Se excluye de los totales porque el dinero nunca salió de la cuenta. |
| **Regla fija** | Clasificación de un comercio o destinatario. Se aplica a sus transacciones pendientes y a las futuras. En la ventana se elige con **Repetir para comercio/persona**. |
| **Regla por monto** | Clasificación de un destinatario cuando el monto es exactamente el indicado. Se aplica a sus transacciones pendientes con ese monto y a las futuras. |
| **Exclusión** | Marca que impide que una fila sume en las tarjetas del mes. En gastos aplica a **Transferencia propia** y **Transferencia devuelta**; en ingresos, a las tres excepciones. |
| **Cartola procesada** | Cartola ya aplicada a la base. Volver a previsualizarla la muestra como *ya procesada* y no duplica movimientos. |
| **Cartola para revisar** | Cartola cuyos totales no calzan con lo leído o no se pudieron leer. Solo se aplica si lo confirmas. |
| **Cartolas guardadas** | Carpeta `Cartolas/` con los PDF descargados, uno por cartola y ordenados por banco y período. |
