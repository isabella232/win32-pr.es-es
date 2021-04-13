---
title: Herramientas de accesibilidad-AccEvent (monitor de eventos accesibles)
description: AccEvent (monitor de eventos accesibles) permite a los desarrolladores y evaluadores validar que los elementos de la interfaz de usuario de una aplicación generan la automatización de la interfaz de usuario de Microsoft y los eventos de Microsoft Active Accessibility cuando se producen cambios en la interfaz de usuario.
ms.assetid: 0077da81-7a1f-4f8b-b519-ebefcc63d264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76e6fa4896c0cfe3155536537099b1c00af8ebe5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421126"
---
# <a name="accessibility-tools---accevent-accessible-event-watcher"></a>Herramientas de accesibilidad-AccEvent (monitor de eventos accesibles)

**AccEvent (monitor de eventos accesibles)** permite a los desarrolladores y evaluadores validar que los elementos de la interfaz de usuario de una aplicación generan la automatización de la interfaz de usuario de Microsoft y los eventos de Microsoft Active Accessibility cuando se producen cambios en la interfaz de usuario. Los cambios en la interfaz de usuario pueden producirse cuando el foco cambia o cuando un elemento de la interfaz de usuario se invoca, se selecciona o tiene un cambio de estado o propiedad.

**AccEvent** se instala con el kit de desarrollo de software (SDK) de Windows. Se encuentra en la \\ carpeta bin \\ < *version* > \\ < *Platform*> de la ruta de instalación de SDK (Accevent.exe).

> [!NOTE]
> **AccEvent** es una herramienta heredada. En su lugar, se recomienda usar [información de accesibilidad](https://accessibilityinsights.io/) .

## <a name="requirements"></a>Requisitos

**AccEvent** se puede usar para examinar los datos de accesibilidad en sistemas que no tienen automatización de la interfaz de usuario, que se escribieron originalmente para Microsoft Active Accessibility. Para examinar la automatización de la interfaz de usuario, la automatización de la interfaz de usuario debe estar presente en el sistema. Para obtener más información, vea la sección "requirements" de automatización de la [interfaz de usuario](entry-uiauto-win32.md).

**AccEvent** se instala como parte del conjunto general de herramientas en el Windows SDK, no se distribuye como una descarga independiente de exe. El Windows SDK incluye todas las herramientas relacionadas con la accesibilidad que se documentan en esta sección. [Obtiene el Windows SDK.](https://developer.microsoft.com/) (También hay un archivo de descarga de SDK vinculado desde esa página, si necesita una versión anterior).

Para ejecutar **AccEvent**, busque AccEvent.exe en la \\ carpeta bin \\ < *version* > \\ < *Platform*> y ejecútela (normalmente, no tiene que ejecutar como administrador).

## <a name="the-accessible-event-watcher-window"></a>La ventana monitor de eventos accesible

Al iniciar **AccEvent**, se muestra la ventana principal. La ventana principal de **AccEvent** muestra los eventos de automatización de la interfaz de usuario o Microsoft Active Accessibility generados por las aplicaciones que se están ejecutando. La ventana principal tiene las siguientes partes principales:

- Barra de título. Muestra el modo de funcionamiento actual y el estado.
- Barra de menús. Proporciona acceso a la funcionalidad de **AccEvent** .
- Vista de datos. Muestra información sobre cada evento, incluido el identificador de evento y las propiedades seleccionadas del elemento de la interfaz de usuario que provocó el evento.

**AccEvent** solo tiene una interfaz gráfica de usuario; no hay ningún argumento de línea de comandos para esta herramienta, pero puede usar otras herramientas para procesar el registro de salida como texto.

La siguiente imagen muestra la ventana principal de **AccEvent** .

![la interfaz de usuario de la herramienta de monitor de eventos accesibles](images/accevent.png)

## <a name="accessible-event-watcher-tasks"></a>Tareas de monitor de eventos accesibles

En esta sección se incluye información sobre las tareas de **AccEvent** de uso frecuente.

### <a name="configuring-the-operating-mode"></a>Configurar el modo de funcionamiento

Use el menú **modo** para configurar el modo de funcionamiento de **AccEvent** y seleccione la configuración que controla el comportamiento de la herramienta. Puede seleccionar las opciones siguientes.



| Cuando se selecciona esta opción | **AccEvent** lo hace                                                                                                                                                                                                                           |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Siempre visible                | Aparece encima de cualquier otra interfaz de usuario de la pantalla.                                                                                                                                                                                    |
| Eventos de UIA                   | Muestra información sobre los eventos de automatización de la interfaz de usuario.                                                                                                                                                                                             |
| WinEvents (en contexto)       | Muestra información acerca de los eventos de Microsoft Active Accessibility (WinEvents) que se pasan a las funciones de enlace que residen en el espacio de direcciones del servidor. Para obtener más información, vea [funciones de enlace en contexto](in-context-hook-functions.md).         |
| WinEvents (fuera de contexto)   | Muestra información acerca de los eventos de Microsoft Active Accessibility (WinEvents) que se pasan a las funciones de enlace que residen en el espacio de direcciones del cliente. Para obtener más información, vea [funciones de enlace fuera de contexto](out-of-context-hook-functions.md). |
| Mostrar rectángulo resaltado     | Resalta un rectángulo alrededor del elemento de la interfaz de usuario que ha generado el evento seleccionado.                                                                                                                                                                 |
| Mostrar información sobre herramientas     | Muestra información de eventos en una información sobre herramientas.                                                                                                                                                                                                        |
| Configuración                     | Muestra el cuadro de diálogo Configuración de **eventos de UIA** o **configuración de WinEvent** .                                                                                                                                                                     |



 

### <a name="filtering-ui-automation-events"></a>Filtrar eventos de UI Automation

Para configurar los eventos y las propiedades de automatización de la interfaz de usuario que se muestran en la ventana de **AccEvent** , haga clic en el menú **modo** , seleccione **eventos de UIA** y, a continuación, seleccione **configuración**. Se muestra el cuadro de diálogo **configuración de eventos de UIA** . También puede utilizar este cuadro de diálogo para filtrar los eventos.

El cuadro de diálogo **configuración de eventos de UIA** contiene los siguientes paneles:

- **Eventos globales**

    Active la casilla **FocusChangedEvent** para mostrar información acerca de los eventos de cambio de foco global.

- **Tipo de evento**

    Seleccione los eventos que le interesen.

- **Ámbito**

    Seleccione el elemento de la interfaz de usuario que desea que **AccEvent** escuche para los eventos.

- **Incluir eventos de**

    Seleccione **elementos secundarios inmediatos** si desea ver los eventos de los elementos secundarios inmediatos del elemento de la interfaz de usuario seleccionado en el panel **ámbito** . Si desea ver los eventos de todos los elementos descendientes, seleccione **todos los descendientes**.

- **Propiedades de informe**

    Seleccione las propiedades que desea que se muestren después de cada evento en la ventana principal. Si la opción **Mostrar información sobre herramientas** está seleccionada en el menú **modo** , las propiedades seleccionadas también se muestran en una información sobre herramientas.

### <a name="filtering-active-accessibility-events"></a>Filtrar eventos de Active Accessibility

Para configurar los eventos y las propiedades de Microsoft Active Accessibility que se muestran en la ventana de **AccEvent** , haga clic en el menú **modo** , seleccione **WinEvents (en contexto)** o **WinEvents (fuera de contexto)** y, a continuación, seleccione **configuración**. Se muestra el cuadro de diálogo **configuración de WinEvent** . También puede utilizar este cuadro de diálogo para filtrar los eventos.

El cuadro de diálogo **configuración de WinEvent** contiene los siguientes paneles:

- **Objects**

    Seleccione los objetos que desea que **AccEvent** escuche para los eventos. **AccEvent** puede realizar escuchas de eventos que se originan en Windows, desde el cursor o desde el símbolo de intercalación. La **ventana** está seleccionada de forma predeterminada.

- **Eventos**

    Seleccione los eventos que le interesen. De forma predeterminada, se muestran todos los eventos.

- **Información del evento**

    Seleccione la información que desea que se muestre después del nombre de cada evento en la ventana principal.

- **Propiedades de objeto**

    Seleccione las propiedades que desea que se muestren después de cada evento en la ventana principal. Si la opción **Mostrar información sobre herramientas** está seleccionada en el menú **modo** , las propiedades seleccionadas también se muestran en una información sobre herramientas. **El nombre, el** **rol** y el **Estado** se seleccionan de forma predeterminada.

- **Filtros**

    Seleccione uno de los botones de radio de la sección de filtrado para filtrar los eventos generados por las ventanas especificadas en el campo **hWnd** . El botón de radio **no filtrar** está seleccionado de forma predeterminada.

    - Seleccione el botón de opción **excluir** para mostrar solo los eventos generados desde objetos distintos de las ventanas especificadas.
    - Seleccione el botón de radio **incluir solo** y especifique uno o varios identificadores de ventana para mostrar solo los eventos generados en esas ventanas.
    - Active la casilla **y los descendientes** para incluir los eventos generados por los descendientes de las ventanas especificadas.

- **Opciones**

    Seleccione cualquiera de las siguientes opciones:

    

    | Cuando se selecciona esta opción                                  | **AccEvent** lo hace                                                                                                                                                                                 |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Usar Invoke                                                    | Usa [IDispatch:: Invoke](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) para recuperar propiedades de objeto en lugar de utilizar métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .                               |
    | Obtener siempre el objeto (incluso si no se ha seleccionado ninguna propiedad de objeto)     | Recupera el objeto asociado al evento incluso si no hay elementos seleccionados en el panel Propiedades del objeto.                                                                                        |
    | Mostrar la propiedad predeterminada (además de las propiedades seleccionadas) | Muestra la propiedad predeterminada, si existe, del objeto asociado al evento, junto con los elementos seleccionados en el panel Propiedades del objeto.                                                      |
    | Mostrar información de eventos desde ventanas invisibles u ocultas       | Muestra los elementos seleccionados en el panel información de eventos para todos los objetos, incluidos los que están en ventanas no visibles u ocultas.                                                                       |
    | Mostrar información completa de eventos de ventanas ocultas u ocultas  | Muestra los elementos seleccionados en el panel información de eventos y los elementos seleccionados (o predeterminados) del panel Propiedades del objeto, para todos los objetos, incluidos los que están en ventanas no visibles u ocultas. |
    | DebugBreak en el evento siguiente                                      | Hace que se produzca una excepción de punto de interrupción en el proceso que origina el siguiente WinEvent. Esto indica al depurador que controle la excepción.                                                        |

### <a name="using-the-event-menu"></a>Usar el menú de eventos

Use el menú **evento** para realizar las siguientes tareas:

| Cuando se selecciona esta opción | **AccEvent** lo hace                                    |
|------------------------------|-------------------------------------------------------|
| Iniciar escucha              | Comienza a mostrar información de eventos en la vista de datos. |
| Detener escucha               | Deja de Mostrar información de eventos en la vista de datos.  |
| Borrar historial de eventos          | Borra el contenido de la vista de datos.                 |
| Seleccionar todos los eventos            | Selecciona todos los eventos enumerados en la vista de datos.           |
| Copiar eventos seleccionados         | Copia los eventos seleccionados en el portapapeles.          |

### <a name="saving-active-accessibility-events"></a>Guardar eventos de Active Accessibility

Para empezar a guardar eventos en un archivo de texto, abra el menú **archivo** y seleccione **Iniciar registro en archivo**. **AccEvent** comienza a escribir eventos en el archivo especificado hasta que seleccione **detener registro** en el menú **archivo** . El archivo de texto puede ser útil para solucionar problemas y revisar los eventos en otro momento.

## <a name="related-topics"></a>Temas relacionados

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Herramientas de pruebas](testing-tools.md)
- [UI Accessibility Checker](ui-accessibility-checker.md)
- [Información general sobre eventos de UI Automation](uiauto-eventsoverview.md)
- [UI Automation Verify](ui-automation-verify.md)
- [WinEvents](winevents-infrastructure.md)