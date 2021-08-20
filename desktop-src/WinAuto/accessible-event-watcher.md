---
title: 'Herramientas de accesibilidad: AccEvent (Accessible Event Watcher)'
description: AccEvent (Accessible Event Watcher) permite a los desarrolladores y evaluadores validar que los elementos de interfaz de usuario de una aplicación producen eventos adecuados de Microsoft Automatización de la interfaz de usuario y Microsoft Active Accessibility cuando se producen cambios en la interfaz de usuario.
ms.assetid: 0077da81-7a1f-4f8b-b519-ebefcc63d264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb2192bf6973444bf2bfc307ff4613d9d1c593d5a22f9800ecb61bc310b3a210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327812"
---
# <a name="accessibility-tools---accevent-accessible-event-watcher"></a>Herramientas de accesibilidad: AccEvent (Accessible Event Watcher)

**AccEvent (Accessible Event Watcher)** permite a los desarrolladores y evaluadores validar que los elementos de interfaz de usuario de una aplicación producen eventos adecuados de Microsoft Automatización de la interfaz de usuario y Microsoft Active Accessibility cuando se producen cambios en la interfaz de usuario. Los cambios en la interfaz de usuario pueden producirse cuando cambia el foco o cuando se invoca, selecciona o tiene un cambio de estado o propiedad.

**AccEvent** se instala con el kit de desarrollo Windows software (SDK). Se encuentra en la carpeta bin version platform> de la ruta de instalación del \\ \\ <  > \\ <  SDK (Accevent.exe).

> [!NOTE]
> **AccEvent** es una herramienta heredada. Se recomienda usar [accessibility Ideas](https://accessibilityinsights.io/) en su lugar.

## <a name="requirements"></a>Requisitos

**AccEvent** se puede usar para examinar los datos de accesibilidad en sistemas que no tienen Automatización de la interfaz de usuario, se escribió originalmente para Microsoft Active Accessibility. Para examinar Automatización de la interfaz de usuario, Automatización de la interfaz de usuario debe estar presente en el sistema. Para obtener más información, vea la sección "Requisitos" [de Automatización de la interfaz de usuario](entry-uiauto-win32.md).

**AccEvent** se instala como parte del conjunto general de herramientas del SDK de Windows, no se distribuye como una descarga de exe independiente. El SDK Windows incluye todas las herramientas relacionadas con la accesibilidad documentadas en esta sección. [Obtenga el SDK Windows.](https://developer.microsoft.com/) (También hay un archivo de descarga del SDK vinculado desde esa página, si necesita una versión anterior).

Para ejecutar **AccEvent,** busque AccEvent.exe en la carpeta bin version platform> y ejecute (normalmente no tiene que ejecutar \\ \\ <  > \\ <  como administrador).

## <a name="the-accessible-event-watcher-window"></a>Ventana De Event Watcher accesible

Al iniciar **AccEvent**, se muestra la ventana principal. La ventana **accEvent** principal muestra los eventos Automatización de la interfaz de usuario o Microsoft Active Accessibility eventos producidos por las aplicaciones que se ejecutan. La ventana principal tiene las siguientes partes principales:

- Barra de título. Muestra el estado y el modo de funcionamiento actuales.
- Barra de menús. Proporciona acceso a **la funcionalidad AccEvent.**
- Vista de datos. Muestra información sobre cada evento, incluidos el identificador de evento y las propiedades seleccionadas del elemento de interfaz de usuario que ha producido el evento.

**AccEvent** solo tiene una interfaz gráfica de usuario; no hay argumentos de línea de comandos para esta herramienta, pero podría usar otras herramientas para procesar el registro de salida como texto.

En la imagen siguiente se muestra la ventana **principal de AccEvent.**

![la interfaz de usuario de la herramienta de control de eventos accesible](images/accevent.png)

## <a name="accessible-event-watcher-tasks"></a>Tareas accesibles de Event Watcher

En esta sección se incluye información sobre las tareas **de AccEvent que** se usan habitualmente.

### <a name="configuring-the-operating-mode"></a>Configuración del modo operativo

Use el menú **Modo** para configurar el modo **operativo AccEvent** y seleccione la configuración que controla el comportamiento de la herramienta. Puede seleccionar las siguientes opciones.



| Cuando se selecciona esta opción | **AccEvent** hace esto                                                                                                                                                                                                                           |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Siempre en la parte superior                | Aparece encima de cualquier otra interfaz de usuario en la pantalla.                                                                                                                                                                                    |
| Eventos de UIA                   | Muestra información sobre Automatización de la interfaz de usuario eventos.                                                                                                                                                                                             |
| WinEvents (en contexto)       | Muestra información sobre Microsoft Active Accessibility eventos (WinEvents) pasados para enlazar funciones que residen en el espacio de direcciones del servidor. Para obtener más información, vea [Funciones de enlace en contexto](in-context-hook-functions.md).         |
| WinEvents (fuera de contexto)   | Muestra información sobre Microsoft Active Accessibility eventos (WinEvents) pasados para enlazar funciones que residen en el espacio de direcciones del cliente. Para obtener más información, vea [Funciones de enlace](out-of-context-hook-functions.md)fuera de contexto . |
| Mostrar rectángulo resaltado     | Resalta un rectángulo alrededor del elemento de interfaz de usuario que ha producido el evento seleccionado.                                                                                                                                                                 |
| Mostrar información sobre herramientas     | Muestra información de eventos en una información sobre herramientas.                                                                                                                                                                                                        |
| Configuración                     | Muestra el **cuadro de diálogo Configuración** evento **UIA Configuración WinEvent.**                                                                                                                                                                     |



 

### <a name="filtering-ui-automation-events"></a>Filtrado de Automatización de la interfaz de usuario eventos

Para configurar los Automatización de la interfaz de usuario y las propiedades que se muestran en  la ventana **AccEvent,** haga clic en el menú Modo, seleccione **Eventos UIA** y, a continuación, **Configuración**. Se muestra el cuadro de diálogo Configuración evento **UIA.** También puede usar este cuadro de diálogo para filtrar por eventos.

El cuadro de diálogo Configuración evento **UIA** contiene los paneles siguientes:

- **Eventos globales**

    Active la **casilla FocusChangedEvent** para mostrar información sobre los eventos globales modificados por el foco.

- **Tipo de evento**

    Seleccione los eventos que le interesen.

- **Ámbito**

    Seleccione el elemento de interfaz de usuario en el que **desea que AccEvent** escuche eventos.

- **Incluir eventos de**

    Seleccione **Elementos secundarios inmediatos** si desea ver eventos de los elementos secundarios inmediatos del elemento de interfaz de usuario seleccionado en el **panel** Ámbito. Si desea ver eventos de todos los elementos **descendientes, seleccione Todos los descendientes.**

- **Propiedades de informe**

    Seleccione las propiedades que desea que se muestren después de cada evento en la ventana principal. Si **la opción Mostrar información sobre** herramientas está seleccionada en el **menú** Modo, las propiedades seleccionadas también se muestran en una información sobre herramientas.

### <a name="filtering-active-accessibility-events"></a>Filtrado de Active Accessibility eventos

Para configurar los eventos y propiedades de Microsoft Active Accessibility que se muestran  en la ventana **AccEvent,** haga clic en el menú Modo, seleccione **WinEvents (en contexto)** o **WinEvents (fuera** de contexto) y, a continuación, **Configuración**. Se **muestra el Configuración** cuadro de diálogo de Configuración WinEvent. También puede usar este cuadro de diálogo para filtrar por eventos.

El **cuadro de Configuración** winevent contiene los siguientes paneles:

- **Objects**

    Seleccione los objetos a los que **desea que AccEvent** escuche eventos. **AccEvent** puede escuchar eventos que se origina en ventanas, desde el cursor o desde el cursor. **La** ventana está seleccionada de forma predeterminada.

- **Eventos**

    Seleccione los eventos que le interesen. Todos los eventos se muestran de forma predeterminada.

- **Información de eventos**

    Seleccione la información que desea mostrar después del nombre de cada evento en la ventana principal.

- **Propiedades de objeto**

    Seleccione las propiedades que desea que se muestren después de cada evento en la ventana principal. Si **la opción Mostrar información sobre** herramientas está seleccionada en el **menú** Modo, las propiedades seleccionadas también se muestran en una información sobre herramientas. **El** nombre , **el** rol y **el estado** están seleccionados de forma predeterminada.

- **Filtros**

    Seleccione uno de los botones de radio de la sección de filtrado para filtrar los eventos producidos por las ventanas especificadas en el **campo hWNDs.** El **botón de radio** No filtrar está seleccionado de forma predeterminada.

    - Seleccione el **botón** de radio Excluir para mostrar solo los eventos que se han producido desde objetos distintos de las ventanas especificadas.
    - Seleccione el **botón de radio Incluir** solo y especifique uno o varios identificadores de ventana para mostrar solo los eventos que se han producido desde esas ventanas.
    - Active la **casilla y Descendants (Descendientes)** para incluir los eventos que han producido los descendientes de las ventanas especificadas.

- **Opciones**

    Seleccione cualquiera de las siguientes opciones:

    

    | Cuando se selecciona esta opción                                  | **AccEvent** hace esto                                                                                                                                                                                 |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Uso de Invoke                                                    | Usa [IDispatch::Invoke para](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) recuperar propiedades de objeto en lugar de usar [**métodos IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)                               |
    | Obtener siempre el objeto (incluso si no hay ninguna propiedad de objeto seleccionada)     | Recupera el objeto asociado al evento incluso si no hay elementos seleccionados en el panel Propiedades del objeto .                                                                                        |
    | Mostrar la propiedad predeterminada (además de las propiedades seleccionadas) | Muestra la propiedad predeterminada, si la hay, para el objeto asociado al evento, junto con los elementos seleccionados en el panel Propiedades del objeto .                                                      |
    | Mostrar información de eventos desde ventanas invisibles o ocultas       | Muestra los elementos seleccionados en el panel Información de eventos para todos los objetos, incluidos los de ventanas invisibles u ocultas.                                                                       |
    | Mostrar información completa del evento desde ventanas invisibles o ocultas  | Muestra los elementos seleccionados en el panel Información de eventos y los elementos seleccionados (o predeterminados) del panel Propiedades del objeto para todos los objetos, incluidos los de ventanas invisibles u ocultas. |
    | DebugBreak en el siguiente evento                                      | Hace que se produzca una excepción de punto de interrupción en el proceso que origina el siguiente WinEvent. Esto indica al depurador que controle la excepción.                                                        |

### <a name="using-the-event-menu"></a>Uso del menú Evento

Use el **menú** Evento para realizar las siguientes tareas:

| Cuando se selecciona esta opción | **AccEvent** hace esto                                    |
|------------------------------|-------------------------------------------------------|
| Iniciar escucha              | Comienza a mostrar información de eventos en la vista Datos. |
| Detener escuchas               | Deja de mostrar información de eventos en la vista Datos.  |
| Borrar historial de eventos          | Borra el contenido de la vista Datos.                 |
| Seleccionar todos los eventos            | Selecciona todos los eventos enumerados en la vista Datos.           |
| Copiar eventos seleccionados         | Copia los eventos seleccionados en el Portapapeles.          |

### <a name="saving-active-accessibility-events"></a>Guardar Active Accessibility eventos

Para empezar a guardar eventos en un archivo de texto, abra el **menú** Archivo y seleccione **Iniciar registro en archivo.** **AccEvent** comienza a escribir eventos en el archivo especificado hasta que selecciona **Detener registro** en el **menú** Archivo. El archivo de texto puede ser útil para solucionar problemas y revisar los eventos más adelante.

## <a name="related-topics"></a>Temas relacionados

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Herramientas de prueba](testing-tools.md)
- [UI Accessibility Checker](ui-accessibility-checker.md)
- [Información general sobre eventos de UI Automation](uiauto-eventsoverview.md)
- [UI Automation Verify](ui-automation-verify.md)
- [WinEvents](winevents-infrastructure.md)