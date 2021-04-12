---
title: 'Herramientas de accesibilidad: inspeccionar'
description: Inspeccionar (Inspect.exe) es una herramienta basada en Windows que permite seleccionar cualquier elemento de la interfaz de usuario y ver los datos de accesibilidad del elemento.
ms.assetid: 38edacbc-cf24-4818-b029-561b21e3704c
keywords:
- Herramienta de inspección
- Accesibilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1770c6c4db812ea7d2880c50fcc72cd0edc15022
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104420353"
---
# <a name="accessibility-tools---inspect"></a>Herramientas de accesibilidad: inspeccionar

**Inspeccionar** (Inspect.exe) es una herramienta basada en Windows que permite seleccionar cualquier elemento de la interfaz de usuario y ver los datos de accesibilidad del elemento. Puedes ver las propiedades de Automatización de la interfaz de usuario de Microsoft y patrones de control, así como las propiedades de Microsoft Active Accessibility. **Inspeccionar** también le permite probar la estructura de navegación de los elementos de automatización en el árbol de automatización de la interfaz de usuario y los objetos accesibles en la jerarquía de Microsoft Active Accessibility.

**Inspeccionar** se instala con el kit de desarrollo de software (SDK) de Windows. (También está disponible en versiones anteriores de Windows SDK). Se encuentra en la \\ carpeta bin \\ < *version* > \\ < *Platform*> de la ruta de instalación de SDK (Inspect.exe).

> [!NOTE]
> **Inspeccionar** es una herramienta heredada. En su lugar, se recomienda usar [información de accesibilidad](https://accessibilityinsights.io/) .

## <a name="requirements"></a>Requisitos

**Inspeccionar** se puede usar para examinar los datos de accesibilidad de los sistemas que no tienen automatización de la interfaz de usuario, pero solo pueden examinar las propiedades de Microsoft Active Accessibility. Para examinar la automatización de la interfaz de usuario, la automatización de la interfaz de usuario debe estar presente en el sistema. Para obtener más información, vea la sección "requirements" de automatización de la [interfaz de usuario](entry-uiauto-win32.md).

**Inspeccionar** se instala como parte del conjunto general de herramientas en el Windows SDK, no se distribuye como una descarga independiente. El Windows SDK incluye todas las herramientas relacionadas con la accesibilidad que se documentan en esta sección. [Obtiene el Windows SDK.](https://developer.microsoft.com/) (También hay un archivo de descarga de SDK vinculado desde esa página, si necesita una versión anterior).

Para ejecutar **inspeccionar**, busque Inspect.exe en \\ la \\ < carpeta bin *version* > \\ < *Platform*> y ejecútela (normalmente, no tiene que ejecutar como administrador).

## <a name="the-inspect-window"></a>Ventana inspeccionar

La ventana **inspeccionar** tiene varias partes principales:

- Barra de título. Muestra el identificador de ventana de **inspección** (HWND).
- Barra de menús. Proporciona acceso para **inspeccionar** la funcionalidad.
- Barra de herramientas. Proporciona acceso para **inspeccionar** la funcionalidad.
- Vista de árbol. Presenta la estructura jerárquica de los elementos de la interfaz de usuario como un control de vista de árbol que puede usar para navegar entre los elementos.
- Vista de datos. Muestra todas las propiedades de accesibilidad expuestas para el elemento de la interfaz de usuario seleccionado.

Los comandos disponibles en la barra de menús también están disponibles en la barra de herramientas. En la siguiente imagen se muestra la herramienta **Inspect** consultando las propiedades de Automatización de la interfaz de usuario del elemento de menú **Editar** del Bloc de notas.

![captura de pantalla que muestra la interfaz de usuario para la herramienta de inspección](images/inspect.png)

## <a name="using-inspect"></a>Usar inspeccionar

Al iniciar **inspeccionar**, la vista de **árbol** muestra la ubicación del elemento de la interfaz de usuario actualmente seleccionado en la jerarquía de elementos y la vista de **datos** muestra la información de la propiedad para el elemento de la interfaz de usuario seleccionado. Puede navegar por la interfaz de usuario para ver información de accesibilidad sobre cada elemento de la interfaz de usuario. De forma predeterminada, **inspeccionar** hace un seguimiento del foco del teclado o del mouse. Cuando el foco cambia, la vista de **datos** se actualiza con la información de la propiedad del elemento que tiene el foco.

Para navegar entre los elementos de la interfaz de usuario, puede usar cualquiera de los siguientes:

- El mouse
- El teclado
- Control de vista de árbol en la vista de **árbol** .
- Opciones de navegación en el menú de **navegación**
- Opciones de navegación en la barra de herramientas

Las tres últimas opciones permiten navegar por la jerarquía de árbol de la interfaz de usuario. La estructura de este árbol puede diferir ligeramente entre la automatización de la interfaz de usuario y los modos de Microsoft Active Accessibility.

## <a name="verifying-accessibility-property-information"></a>Comprobar la información de propiedades de accesibilidad

La vista de **datos** muestra la información de propiedades del elemento de la interfaz de usuario que está seleccionado actualmente. Puede configurar **inspeccionar** para que le muestre información acerca de todas las propiedades de accesibilidad o un subconjunto de esas propiedades. También puede especificar otras opciones de visualización, por ejemplo, si **inspeccionar** debe permanecer encima de otras interfaces de usuario o si **inspeccionar** debe resaltar un rectángulo delimitador alrededor del elemento seleccionado. Una vez que haya configurado **inspeccionar** para que funcione de la manera que desee, puede empezar a navegar entre los elementos de la interfaz de usuario y ver la información de la propiedad. **Inspeccione** guarda los valores de configuración cuando se cierran y los usa para inicializar la siguiente sesión de **inspección** .

### <a name="configure-property-settings"></a>Configurar valores de propiedades

1. En el menú **Opciones** , seleccione **configuración...** o seleccione **Mostrar cuadro de diálogo de configuración** en la barra de herramientas.
2. En la lista de la **ventana principal** , seleccione las propiedades que desea mostrar en la vista de **datos** de **inspeccionar**.
3. En la lista **Mostrar en información sobre herramientas** , seleccione las propiedades que desea que se muestren en una información sobre herramientas.
4. Para ver las propiedades que es posible que el elemento de la interfaz de usuario no admita, active la casilla **Mostrar propiedades no admitidas** .
5. Haga clic en **OK**.

### <a name="to-configure-viewing-options"></a>Para configurar las opciones de visualización

- En el menú **Opciones** o en la barra de herramientas, puede seleccionar las siguientes opciones de visualización.

| Cuando se selecciona esta opción | **Inspeccionar** esto                                                                                                                                                                                                              |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Siempre visible                | Aparece en la parte superior de cualquier otra ventana de la pantalla.                                                                                                                                                                                  |
| Modo MSAA                    | Muestra información de la propiedad de Microsoft Active Accessibility.                                                                                                                                                                      |
| Modo de automatización de la interfaz de usuario           | Muestra información de la propiedad de automatización de la interfaz de usuario.                                                                                                                                                                                       |
| Vista solo visible de Windows    | Solo disponible en modo MSAA.                                                                                                                                                                                                       |
| Vista sin formato                     | Presenta la [vista sin formato](uiauto-treeoverview.md) del árbol de automatización de la interfaz de usuario o del árbol de MSAA en la vista de **árbol** .                                                                                                             |
| Vista de control                 | Presenta la [vista de control](uiauto-treeoverview.md) del árbol de automatización de la interfaz de usuario en la vista de **árbol** . Solo está disponible en el modo UI Automation.                                                                            |
| Vista de contenido                 | Presenta la [vista de contenido](uiauto-treeoverview.md) del árbol de automatización de la interfaz de usuario en la vista de **árbol** . Solo está disponible en el modo UI Automation.                                                                            |
| Barra de herramientas activa         | Activa los botones de la barra de herramientas al mantener el mouse en lugar de requerir un clic del mouse.                                                                                                                                                      |
| Bip en error                | Emite un pitido cuando se detecta un error durante una automatización de la interfaz de usuario o una operación de MSAA.                                                                                                                                                          |
| \_Marca SPI SCREENREADER       | Supone que hay un lector de pantalla presente. Esta marca indica que una aplicación debe proporcionar información textual en lugar de gráficamente. No debe suponer que esta marca se establece simplemente porque hay un lector de pantalla presente.         |
| Mostrar rectángulo resaltado     | Resalta un rectángulo alrededor del elemento que tiene el foco.                                                                                                                                                                              |
| Mostrar resaltado del símbolo de intercalación         | Resalta el símbolo de intercalación. Solo disponible en modo MSAA.                                                                                                                                                                                 |
| Mostrar información sobre herramientas     | Muestra información de propiedades en una información sobre herramientas.                                                                                                                                                                                           |
| Ver el foco                  | Sigue el foco del teclado. Cuando se selecciona, se instala un enlace de eventos de foco asincrónico y se mueve el símbolo de intercalación a la parte superior izquierda del elemento con el foco. Esto hace que **inspeccionar** actualice sus propiedades en aproximadamente un segundo. |
| Ver símbolo de intercalación                  | Sigue el símbolo de intercalación. Solo disponible en modo MSAA.                                                                                                                                                                                    |
| Ver cursor                 | Sigue el cursor.                                                                                                                                                                                                                |
| Ver información sobre herramientas               | Sigue la información sobre herramientas.                                                                                                                                                                                                              |
| Mostrar árbol                    | Muestra la vista de **árbol** .                                                                                                                                                                                                        |

## <a name="verifying-accessibility-navigation"></a>Comprobando la navegación de accesibilidad

Una vez que haya seleccionado un elemento de la interfaz de usuario mediante **inspeccionar**, puede validar que el elemento exponga la navegación de automatización de Windows correcta para los productos de tecnología de asistencia.

### <a name="verify-accessibility-navigation"></a>Comprobar la navegación de accesibilidad

1. Abra **inspeccionar** y la aplicación que desea probar.
2. Seleccione el elemento de la interfaz de usuario desde el que desea iniciar la navegación.
3. En la vista de **datos** , compruebe que el elemento expone las propiedades correctas relacionadas con la navegación.
4. Use la vista de **árbol** , el menú de **navegación** o los botones de navegación de la barra de herramientas para navegar por la interfaz de usuario y comprobar que cada elemento expone las propiedades correctas relacionadas con la navegación.
    > [!Note]  
    > Las opciones de menú de **navegación** y los botones de la barra de herramientas de navegación cambian en función de dónde se encuentra el elemento seleccionado en el árbol.

## <a name="interacting-with-ui-elements"></a>Interactuar con elementos de la interfaz de usuario

Windows Automation expone métodos que permiten a los productos de tecnología de asistencia interactuar con un elemento de la interfaz de usuario como si se usara el mouse o el teclado (por ejemplo, para hacer clic en un botón). El menú de acción **inspeccionar** permite a los evaluadores invocar métodos de automatización de Windows en un elemento (por ejemplo, **Invoke. Invoke** llama al método [**IUIAutomationInvokePattern:: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) ).

### <a name="interact-with-ui-elements"></a>Interactuar con elementos de la interfaz de usuario

1. Abra **inspeccionar** y la aplicación que desea probar.
2. Seleccione el elemento de la interfaz de usuario con el que desea interactuar.
3. En el menú **acción** o en la barra de herramientas, seleccione la acción que corresponde al método de automatización de Windows que desea invocar.

El menú **acción** contiene los elementos **Actualizar** y **foco** , junto con otros elementos que varían en función de si el modo de automatización de la interfaz de usuario o el modo MSAA de están seleccionados. En el modo de automatización de la interfaz de usuario, los demás elementos reflejan los patrones de control admitidos por el elemento de la interfaz de usuario seleccionado actualmente. En el modo MSAA, los otros elementos siempre constan de lo siguiente:

| Acción                | Descripción                                                                                                           |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------|
| Actualizar               | Actualiza la interfaz de usuario. Disponible en el modo MSAA y automatización de la interfaz de usuario.                                               |
| Acción predeterminada        | Realiza la acción predeterminada para el elemento.                                                                          |
| Foco                 | Establece el foco en el elemento. Disponible en el modo MSAA y automatización de la interfaz de usuario.                                                  |
| Seleccionar                | Selecciona el elemento.                                                                                                  |
| Ampliar selección      | Extiende la selección de elementos para incluir todos los elementos entre el primer elemento seleccionado y el elemento actual. |
| Agregar a la selección      | Selecciona el elemento actual (por ejemplo, un elemento de lista).                                                                    |
| Quitar de la selección | Quita el elemento actual de la selección.                                                                       |
| SetAccValue           | Establece el valor de Microsoft Active Accessibility del elemento en la cadena especificada.                                 |
| Secundario con foco         | Navega hasta el elemento secundario del elemento que tiene actualmente el foco.                                                       |
| HitTest en cursor     | Navega hasta el elemento secundario del elemento especificado por el cursor del mouse.                                                      |
| HitTest...            | Abre el cuadro de diálogo **HitTest** .                                                                                     |



 

## <a name="keyboard-shortcuts"></a>Métodos abreviados de teclado.

Muchos de los elementos de menú se pueden invocar con un método abreviado de teclado incluso cuando **inspeccionar** no es la aplicación activa. Sin embargo, tenga en cuenta que las teclas de método abreviado entran en conflicto con algunas aplicaciones.

Las siguientes teclas de método abreviado de teclado activan las distintas opciones en el menú:



| Para hacer esto                                                                                                                                       | Use este método abreviado de teclado |
|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| Invocar la acción predeterminada del objeto debajo del cursor (acción predeterminada). Solo disponible en modo MSAA.                                       | CTRL+MAYÚS+F2              |
| Seleccione el objeto situado debajo del cursor (seleccione). Solo disponible en modo MSAA.                                                                        | CTRL+MAYÚS+F3              |
| Establezca el foco del teclado en el objeto situado debajo del cursor (foco).                                                                                   | CTRL + MAYÚS + F4              |
| Desplácese al objeto relacionado anterior desde el que está debajo del cursor. Este comando solo navega hasta objetos dentro de un contenedor (elemento relacionado anterior). | CTRL+MAYÚS+F5              |
| Desplácese hasta el elemento primario del objeto (primario).                                                                                                            | CTRL+MAYÚS+F6              |
| Moverse al primer elemento secundario del objeto actual (primer elemento secundario).                                                                                     | CTRL + MAYÚS + F7              |
| Desplácese al siguiente objeto relacionado desde el que se encuentra debajo del cursor. Este comando solo navega hasta objetos dentro de un contenedor (siguiente elemento del mismo nivel).         | CTRL + MAYÚS + F8              |
| Moverse al último elemento secundario del objeto actual (último elemento secundario).                                                                                       | CTRL+MAYÚS+F9              |
| Moverse al objeto situado debajo del cursor del mouse (HitTest en el cursor). Solo disponible en modo MSAA.                                                      | CTRL+MAYÚS+1               |
| Copiar el contenido de la vista de datos en el portapapeles (copiar todo).                                                                                  | CTRL+MAYÚS+4               |
| Actualiza el contenido de la vista de datos (actualizar).                                                                                                 | CTRL+MAYÚS+5               |
| Vea el objeto que tiene el foco (ver el foco).                                                                                                   | CTRL+MAYÚS+6               |
| Desplácese al objeto relacionado situado a la izquierda de la posición en la que se encuentra el cursor (izquierda). Solo disponible en modo MSAA.                                        | CTRL+MAYÚS+7               |
| Desplácese al objeto relacionado situado encima del objeto en el que está situado el cursor (up). Solo disponible en modo MSAA.                                                | CTRL+MAYÚS+8               |
| Desplácese hasta el objeto relacionado debajo de aquél en el que se encuentra el cursor (hacia abajo). Solo disponible en modo MSAA.                                                 | CTRL+MAYÚS+9               |
| Desplácese hasta el objeto relacionado situado a la derecha de aquél en el que se encuentra el cursor (derecha). Solo disponible en modo MSAA.                                      | CTRL + MAYÚS + 0               |

## <a name="related-topics"></a>Temas relacionados

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Herramientas de pruebas](testing-tools.md)
- [UI Accessibility Checker](ui-accessibility-checker.md)
- [UI Automation Verify](ui-automation-verify.md)
- [AccScope](accscope.md)
