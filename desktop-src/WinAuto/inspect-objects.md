---
title: 'Herramientas de accesibilidad: inspeccionar'
description: Inspect (Inspect.exe) es una herramienta Windows que permite seleccionar cualquier elemento de la interfaz de usuario y ver los datos de accesibilidad del elemento.
ms.assetid: 38edacbc-cf24-4818-b029-561b21e3704c
keywords:
- Herramienta Inspeccionar
- Accesibilidad
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: 78ce05a0d7a771378d5fb818c015634a0d8f951b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567429"
---
# <a name="accessibility-tools---inspect"></a>Herramientas de accesibilidad: inspeccionar

> [!Important]
> **Inspeccionar** es una herramienta heredada. Se recomienda usar [accessibility Ideas](https://accessibilityinsights.io/) en su lugar.

**Inspect** (Inspect.exe) es una herramienta Windows que permite seleccionar cualquier elemento de la interfaz de usuario y ver los datos de accesibilidad del elemento. Puede ver las propiedades Automatización de la interfaz de usuario y los patrones de control de Microsoft, así como Microsoft Active Accessibility (MSAA). **Inspeccionar** también permite probar la estructura de navegación de los elementos de automatización en el árbol de Automatización de la interfaz de usuario y los objetos accesibles en la Microsoft Active Accessibility de navegación.

## <a name="requirements"></a>Requisitos

Para examinar Automatización de la interfaz de usuario, Automatización de la interfaz de usuario debe estar presente en el sistema. Para obtener más información, vea la sección "Requisitos" [de Automatización de la interfaz de usuario](entry-uiauto-win32.md).

**Inspect** se instala como parte del conjunto general de herramientas en Windows Software Development Kit (SDK), no se distribuye como una descarga independiente. El SDK Windows incluye todas las herramientas relacionadas con la accesibilidad documentadas en esta sección.

[Descargue el SDK Windows .](https://developer.microsoft.com/en-us/windows/downloads/windows-10-sdk/)

> [!NOTE]
> Para las versiones anteriores del SDK de Windows, consulte el [archivo Windows SDK y del emulador.](https://developer.microsoft.com/en-us/windows/downloads/sdk-archive/)

**Inspect.exe** se encuentra en la carpeta bin version platform> de la ruta de instalación del SDK (normalmente no tiene que \\ \\ <  > \\ <  ejecutarse como administrador).

## <a name="the-inspect-window"></a>La ventana Inspeccionar

La **ventana** Inspeccionar tiene varias partes principales:

- Barra de título. Muestra el **identificador de** ventana Inspeccionar (HWND).
- Barra de menús. Proporciona acceso a **la funcionalidad De** inspección.
- Barra de herramientas. Proporciona acceso a **la funcionalidad De** inspección.
- Vista de árbol. Presenta la estructura jerárquica de los elementos de la interfaz de usuario como un control de vista de árbol que puede usar para navegar entre los elementos.
- Vista de datos. Muestra todas las propiedades de accesibilidad expuestas para el elemento de interfaz de usuario seleccionado.

Los comandos disponibles en la barra de menús también están disponibles en la barra de herramientas. En la siguiente imagen se muestra la herramienta **Inspect** consultando las propiedades de Automatización de la interfaz de usuario del elemento de menú **Editar** del Bloc de notas.

![captura de pantalla que muestra la interfaz de usuario de la herramienta de inspección](images/inspect.png)

## <a name="using-inspect"></a>Uso de Inspeccionar

Al iniciar **Inspeccionar**  , la vista Árbol muestra la ubicación del elemento  de interfaz de usuario seleccionado actualmente en la jerarquía de elementos y la vista Datos muestra la información de propiedad del elemento de interfaz de usuario seleccionado. Puede navegar por la interfaz de usuario para ver información de accesibilidad sobre cada elemento de la interfaz de usuario. De forma predeterminada, **Inspeccionar** realiza un seguimiento del foco del teclado o del mouse. A medida que cambia el foco, **la vista** Datos se actualiza con la información de propiedad del elemento con el foco.

Para navegar entre los elementos de la interfaz de usuario, puede usar cualquiera de las siguientes opciones:

- El mouse.
- El teclado
- Control de vista de árbol en la **vista** Árbol.
- Opciones de navegación en el **menú** Navegación.
- Opciones de navegación de la barra de herramientas.

Las tres últimas opciones permiten navegar por la jerarquía de árbol de la interfaz de usuario. La estructura de este árbol puede diferir ligeramente entre los Automatización de la interfaz de usuario y Microsoft Active Accessibility automáticos.

## <a name="verifying-accessibility-property-information"></a>Comprobar la información de propiedades de accesibilidad

La **vista** Datos muestra la información de propiedad del elemento de interfaz de usuario que está seleccionado actualmente. Puede configurar **Inspeccionar para** mostrar información sobre todas las propiedades de accesibilidad o un subconjunto de esas propiedades. También puede especificar otras opciones de visualización, como si **Inspeccionar** debe permanecer encima de otras interfaces de usuario o si **Inspeccionar** debe resaltar un rectángulo delimitador alrededor del elemento seleccionado. Una vez que haya configurado **Inspeccionar para** que funcione como desee, puede empezar a navegar entre los elementos de la interfaz de usuario y ver la información de las propiedades. **Inspeccionar** guarda los valores de configuración cuando se cierra y los usa para inicializar la siguiente **sesión de inspección.**

### <a name="configure-property-settings"></a>Configurar propiedades Configuración

1. En el **menú Opciones,** seleccione **Configuración...** o seleccione **Mostrar Configuración diálogo en** la barra de herramientas.
2. En la **lista Mostrar en la ventana** principal, seleccione las propiedades que desea que se muestren en la **vista** Datos de **Inspeccionar**.
3. En la **lista Mostrar en información sobre herramientas** , seleccione las propiedades que desea que se muestren en una información sobre herramientas.
4. Para ver las propiedades que el elemento de la interfaz de usuario puede no admitir, active la casilla Mostrar **propiedades no admitidas.**
5. Haga clic en **OK**.

### <a name="to-configure-viewing-options"></a>Para configurar opciones de visualización

- En el **menú Opciones** o en la barra de herramientas, puede seleccionar las siguientes opciones de visualización.

| Cuando se selecciona esta opción | **Inspeccionar** hace esto                                                                                                                                                                                                              |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Siempre en la parte superior                | Aparece en la parte superior de cualquier otra ventana de la pantalla.                                                                                                                                                                                  |
| Modo MSAA                    | Muestra Microsoft Active Accessibility de propiedades.                                                                                                                                                                      |
| Automatización de la interfaz de usuario modo de configuración           | Muestra Automatización de la interfaz de usuario de propiedades.                                                                                                                                                                                       |
| Vista Windows solo visible    | Disponible solo en modo MSAA.                                                                                                                                                                                                       |
| Vista sin formato                     | Presenta la [vista sin formato](uiauto-treeoverview.md) del Automatización de la interfaz de usuario árbol o árbol MSAA en la **vista** Árbol.                                                                                                             |
| Vista de control                 | Presenta la [vista de](uiauto-treeoverview.md) control del Automatización de la interfaz de usuario en la **vista** Árbol. Solo está disponible Automatización de la interfaz de usuario modo de configuración.                                                                            |
| Vista de contenido                 | Presenta la [vista de contenido](uiauto-treeoverview.md) del Automatización de la interfaz de usuario en la **vista** Árbol. Solo está disponible Automatización de la interfaz de usuario modo de configuración.                                                                            |
| Barra de herramientas de mantener el puntero activo         | Activa los botones de la barra de herramientas al mantener el puntero del mouse, en lugar de requerir un clic del mouse.                                                                                                                                                      |
| Pitido en caso de error                | Pitidos cuando se detecta un error durante una operación Automatización de la interfaz de usuario o MSAA.                                                                                                                                                          |
| Marca SPI \_ SCREENREADER       | Supone que hay un lector de pantalla. Esta marca indica que una aplicación debe proporcionar información textualmente en lugar de gráficamente. No debe suponer que esta marca se establece simplemente porque hay un lector de pantalla.         |
| Mostrar rectángulo resaltado     | Resalta un rectángulo alrededor del elemento con el foco.                                                                                                                                                                              |
| Mostrar resaltado de caret         | Resalta el caret. Disponible solo en modo MSAA.                                                                                                                                                                                 |
| Mostrar información sobre herramientas     | Muestra información de propiedades en una información sobre herramientas.                                                                                                                                                                                           |
| Watch Focus                  | Sigue el foco del teclado. Cuando se selecciona, se instala un enlace de eventos de foco asincrónico y mueve el elemento de subrayado a la parte superior izquierda del elemento con el foco. Esto hace **que Inspect** actualice sus propiedades en aproximadamente un segundo. |
| Watch Caret                  | Sigue el centro de atención. Disponible solo en modo MSAA.                                                                                                                                                                                    |
| Cursor de reloj                 | Sigue el cursor.                                                                                                                                                                                                                |
| Ver información sobre herramientas               | Sigue la información sobre herramientas.                                                                                                                                                                                                              |
| Mostrar árbol                    | Muestra la **vista** Árbol.                                                                                                                                                                                                        |

## <a name="verifying-accessibility-navigation"></a>Comprobación de la navegación de accesibilidad

Una vez que haya seleccionado un elemento de interfaz de usuario mediante **Inspeccionar**, puede validar que el elemento expone la navegación Windows Automation correcta para los productos de tecnología de asistencia.

### <a name="verify-accessibility-navigation"></a>Comprobar la navegación de accesibilidad

1. Abra **Inspeccionar** y la aplicación que desea probar.
2. Seleccione el elemento de interfaz de usuario desde el que desea iniciar la navegación.
3. En la **vista** Datos, compruebe que el elemento expone las propiedades correctas relacionadas con la navegación.
4. Use la vista  **Árbol,** el menú Navegación o los botones de navegación de la barra de herramientas para navegar por la interfaz de usuario y comprobar que cada elemento expone las propiedades correctas relacionadas con la navegación.
    > [!Note]  
    > Las **opciones del menú** Navegación y los botones de la barra de herramientas de navegación cambian en función de dónde se encuentra el elemento seleccionado en el árbol.

## <a name="interacting-with-ui-elements"></a>Interacción con elementos de la interfaz de usuario

Windows Automation expone métodos que permiten a los productos de tecnología de asistencia interactuar con un elemento de interfaz de usuario como si se usara el mouse o el teclado (por ejemplo, para hacer clic en un botón). El **menú Inspeccionar** acción permite a los evaluadores invocar Windows automation en un elemento (por ejemplo, **Invoke.Invoke** llama al método [**IUIAutomationInvokePattern::Invoke).**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke)

### <a name="interact-with-ui-elements"></a>Interacción con elementos de la interfaz de usuario

1. Abra **Inspeccionar** y la aplicación que desea probar.
2. Seleccione el elemento de interfaz de usuario con el que desea interactuar.
3. En el **menú Acción** o en la barra de herramientas, seleccione la acción correspondiente a Windows automation que desea invocar.

El **menú** Acción contiene  los elementos **Actualizar** y Centrar, junto con otros elementos que varían en función de si Automatización de la interfaz de usuario modo o modo MSAA seleccionado. En Automatización de la interfaz de usuario, los demás elementos reflejan los patrones de control admitidos por el elemento de interfaz de usuario seleccionado actualmente. En el modo MSAA, los demás elementos siempre constan de lo siguiente:

| Acción                | Descripción                                                                                                           |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------|
| Actualizar               | Actualiza la interfaz de usuario. Disponible en MSAA y Automatización de la interfaz de usuario modo.                                               |
| Acción predeterminada        | Realiza la acción predeterminada para el elemento .                                                                          |
| Foco                 | Establece el foco en el elemento . Disponible en MSAA y Automatización de la interfaz de usuario modo.                                                  |
| Seleccionar                | Selecciona el elemento .                                                                                                  |
| Ampliar selección      | Extiende la selección de elementos para incluir todos los elementos entre el primer elemento seleccionado y el elemento actual. |
| Agregar a selección      | Selecciona el elemento actual (por ejemplo, un elemento de lista).                                                                    |
| Quitar de la selección | Quita el elemento actual de la selección.                                                                       |
| SetAccValue           | Establece el Microsoft Active Accessibility valor del elemento en la cadena especificada.                                 |
| Elemento secundario centrado         | Navega al elemento secundario del elemento que actualmente tiene el foco.                                                       |
| HitTest al cursor     | Navega al elemento secundario del elemento especificado por el cursor del mouse.                                                      |
| HitTest...            | Abre el **cuadro de diálogo HitTest.**                                                                                     |



 

## <a name="keyboard-shortcuts"></a>Métodos abreviados de teclado

Muchos de los elementos de menú se pueden invocar con un método abreviado de teclado incluso cuando **Inspeccionar** no es la aplicación activa. Sin embargo, tenga en cuenta que las teclas de método abreviado están en conflicto con algunas aplicaciones.

Las siguientes teclas de método abreviado de teclado activan las distintas opciones del menú:



| Para hacer esto                                                                                                                                       | Use este método abreviado de teclado |
|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| Invoque la acción predeterminada del objeto bajo el cursor (Realizar acción predeterminada). Disponible solo en modo MSAA.                                       | CTRL+MAYÚS+F2              |
| Seleccione el objeto bajo el cursor (Seleccionar). Disponible solo en modo MSAA.                                                                        | CTRL+MAYÚS+F3              |
| Establezca el foco del teclado en el objeto situado debajo del cursor (Foco).                                                                                   | CTRL+MAYÚS+F4              |
| Mueva al objeto relacionado anterior desde el que está debajo del cursor. Este comando navega a objetos solo dentro de un contenedor (anterior relacionado). | CTRL+MAYÚS+F5              |
| Moverse al elemento primario del objeto (primario).                                                                                                            | CTRL+MAYÚS+F6              |
| Desplazarse al primer elemento secundario del objeto actual (Primer elemento secundario).                                                                                     | CTRL+MAYÚS+F7              |
| Mueva al siguiente objeto relacionado desde el que está debajo del cursor. Este comando navega a objetos solo dentro de un contenedor (siguiente relacionado).         | CTRL+MAYÚS+F8              |
| Moverse al último elemento secundario del objeto actual (Último elemento secundario).                                                                                       | CTRL+MAYÚS+F9              |
| Mueva al objeto bajo el cursor del mouse (HitTest at Cursor). Disponible solo en modo MSAA.                                                      | CTRL+MAYÚS+1               |
| Copie el contenido de la vista Datos en el Portapapeles (Copiar todo).                                                                                  | CTRL+MAYÚS+4               |
| Actualice el contenido de la vista Datos (Actualizar).                                                                                                 | CTRL+MAYÚS+5               |
| Vea el objeto que tiene el foco (Watch Focus).                                                                                                   | CTRL+MAYÚS+6               |
| Muévese al objeto relacionado a la izquierda del que está sobre el que está el cursor (Izquierda). Disponible solo en modo MSAA.                                        | CTRL+MAYÚS+7               |
| Mueva al objeto relacionado encima del objeto sobre el que está el cursor (Arriba). Disponible solo en modo MSAA.                                                | CTRL+MAYÚS+8               |
| Moverse al objeto relacionado debajo del que está el cursor (Abajo). Disponible solo en modo MSAA.                                                 | CTRL+MAYÚS+9               |
| Mueva al objeto relacionado a la derecha del que está sobre el que está el cursor (derecha). Disponible solo en modo MSAA.                                      | CTRL+MAYÚS+0               |

## <a name="related-topics"></a>Temas relacionados

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Herramientas de prueba](testing-tools.md)
- [UI Accessibility Checker](ui-accessibility-checker.md)
- [UI Automation Verify](ui-automation-verify.md)
- [AccScope](accscope.md)
