---
UID: ''
title: Función de devolución de llamada ShellProc
description: La función recibe notificaciones de eventos de Shell del sistema.
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 4add84011745aeb61659c39775b94fed91028d83
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/11/2020
ms.locfileid: "105704929"
---
# <a name="shellproc-function"></a>ShellProc función)

## <a name="description"></a>Descripción

Función de devolución de llamada definida por la aplicación o definida por la biblioteca que se usa con la función [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
La función recibe notificaciones de eventos de Shell del sistema.

El tipo **HOOKPROC** define un puntero a esta función de devolución de llamada.
**ShellProc** es un marcador de posición para el nombre de la función definida por la aplicación o por la biblioteca.

```cpp
LRESULT CALLBACK ShellProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parámetros

### <a name="ncode-in"></a>nCode [in]

Tipo: **int**

Código de enlace.
Si *nCode* es menor que cero, el procedimiento de enlace debe pasar el mensaje a la función [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sin más procesamiento y debe devolver el valor devuelto por **CallNextHookEx**.
Este parámetro puede ser uno de los valores siguientes.

| Valor | Significado |
|-------|---------|
| **HSHELL_ACCESSIBILITYSTATE** 11 | El estado de accesibilidad ha cambiado. |
| **HSHELL_ACTIVATESHELLWINDOW** 3 | El shell debe activar su ventana principal. |
| **HSHELL_APPCOMMAND** 12 | El usuario completó un evento de entrada (por ejemplo, presionó un botón de comando de la aplicación en el mouse o una tecla de comando de la aplicación en el teclado) y la aplicación no controló el mensaje de [WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand) generado por dicha entrada. Si el procedimiento de Shell controla el mensaje de [WM_COMMAND](/windows/desktop/menurc/wm-command) , no debe llamar a **CallNextHookEx**. Vea la sección valor devuelto para obtener más información. |
| **HSHELL_GETMINRECT** 5 | Una ventana está minimizada o maximizada. El sistema necesita las coordenadas del rectángulo minimizado para la ventana. |
| **HSHELL_LANGUAGE** 8 | El idioma del teclado ha cambiado o se ha cargado una nueva distribución del teclado. |
| **HSHELL_REDRAW** 6 | Se ha redibujado el título de una ventana en la barra de tareas. |
| **HSHELL_TASKMAN** 7 | El usuario ha seleccionado la lista de tareas. Una aplicación de Shell que proporciona una lista de tareas debe devolver **true** para impedir que Windows inicie su lista de tareas. |
| **HSHELL_WINDOWACTIVATED** 4 | La activación ha cambiado a otra ventana sin propiedad de nivel superior. |
| **HSHELL_WINDOWCREATED** 1 | Se ha creado una ventana sin propiedad de nivel superior. La ventana existe cuando el sistema llama a este enlace. |
| **HSHELL_WINDOWDESTROYED** 2 | Una ventana sin propiedad de nivel superior está a punto de ser destruida. La ventana todavía existe cuando el sistema llama a este enlace. |
| **HSHELL_WINDOWREPLACED** 13 | Se está reemplazando una ventana de nivel superior. La ventana existe cuando el sistema llama a este enlace. |

### <a name="wparam-in"></a>wParam [in]

Tipo: **wParam**

Este parámetro depende del valor del parámetro *nCode* , tal y como se muestra en la tabla siguiente.

| nCode | wParam |
|-------|---------|
| **HSHELL_ACCESSIBILITYSTATE** | Indica qué característica de accesibilidad ha cambiado de estado. Este valor es uno de los siguientes: **ACCESS_FILTERKEYS**, **ACCESS_MOUSEKEYS** o **ACCESS_STICKYKEYS**. |
| **HSHELL_APPCOMMAND** | Indica dónde se envió originalmente el mensaje de **WM_APPCOMMAND** ; por ejemplo, el identificador de una ventana. Para obtener más información, vea el parámetro cmd en **WM_APPCOMMAND**. |
| **HSHELL_GETMINRECT** | Identificador de la ventana minimizada o maximizada. |
| **HSHELL_LANGUAGE** | Identificador de la ventana. |
| **HSHELL_REDRAW** | Identificador de la ventana redibujada. |
| **HSHELL_WINDOWACTIVATED** | Identificador de la ventana activa. |
| **HSHELL_WINDOWCREATED** | Identificador de la ventana creada. |
| **HSHELL_WINDOWDESTROYED** | Identificador de la ventana destruida. |
| **HSHELL_WINDOWREPLACED** | Identificador de la ventana que se va a reemplazar. Windows 2000: no compatible. |

### <a name="lparam-in"></a>lParam [in]

Tipo: **lParam**

Este parámetro depende del valor del parámetro *nCode* , tal y como se muestra en la tabla siguiente.

| nCode | lParam |
|-------|---------|
| **HSHELL_APPCOMMAND** | `GET_APPCOMMAND_LPARAM(lParam)` es el comando de aplicación correspondiente al evento de entrada. `GET_DEVICE_LPARAM(lParam)` indica qué generó el evento de entrada; por ejemplo, el mouse o el teclado. Para obtener más información, vea la descripción del parámetro *uDevice* en **WM_APPCOMMAND**. `GET_FLAGS_LPARAM(lParam)` depende del valor de *cmd* en **WM_APPCOMMAND**. Por ejemplo, podría indicar qué teclas virtuales se mantuvieron presionadas cuando el mensaje de **WM_APPCOMMAND** se envió originalmente. Para obtener más información, consulte el parámetro *dwCmdFlags* Description en **WM_APPCOMMAND**. |
| **HSHELL_GETMINRECT** | Puntero a una estructura [Rect](/previous-versions/dd162897(v=vs.85)) . |
| **HSHELL_LANGUAGE** | Identificador de una distribución del teclado. |
| **HSHELL_MONITORCHANGED** | Identificador de la ventana que se ha desplace a otro monitor. |
| **HSHELL_REDRAW** | El valor es **true** si la ventana parpadea o **false** en caso contrario. |
| **HSHELL_WINDOWACTIVATED** | El valor es TRUE si la ventana está en modo de pantalla completa o **false** en caso contrario. |
| **HSHELL_WINDOWREPLACED** | Identificador de la nueva ventana. Windows 2000: no compatible. |

## <a name="returns"></a>Devoluciones

Tipo: **LRESULT**

El valor devuelto debe ser cero a menos que el valor de nCode sea **HSHELL_APPCOMMAND** y el procedimiento de Shell controle el mensaje de **WM_COMMAND** .
En este caso, el valor devuelto debe ser distinto de cero.

## <a name="remarks"></a>Observaciones

Instale este procedimiento de enlace especificando el tipo de enlace de [WH_SHELL](about-hooks.md) y un puntero al procedimiento de enlace en una llamada a la función **SetWindowsHookEx** .

## <a name="see-also"></a>Vea también

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand)

[WM_COMMAND](/windows/desktop/menurc/wm-command)

[Enlaces](hooks.md)
