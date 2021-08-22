---
UID: ''
title: Función de devolución de llamada LowLevelMouseProc
description: El sistema llama a esta función cada vez que un nuevo evento de entrada del mouse está a punto de publicarse en una cola de entrada de subprocesos.
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
ms.openlocfilehash: 53f75d14395388ce22ce86ef73f8819892c3fe7285909b1f38c801af476636a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705791"
---
# <a name="lowlevelmouseproc-function"></a>Función LowLevelMouseProc

## <a name="description"></a>Descripción

Función de devolución de llamada definida por la aplicación o definida por la biblioteca que se usa con la [función SetWindowsHookEx.](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)
El sistema llama a esta función cada vez que un nuevo evento de entrada del mouse está a punto de publicarse en una cola de entrada de subprocesos.

El **tipo HOOKPROC** define un puntero a esta función de devolución de llamada.
**LowLevelMouseProc es** un marcador de posición para el nombre de función definido por la aplicación o definido por la biblioteca.

```cpp
LRESULT CALLBACK LowLevelMouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parámetros

### <a name="ncode-in"></a>nCode [in]

Tipo: **int**

Código que el procedimiento de enlace usa para determinar cómo procesar el mensaje.
Si *nCode* es menor que cero, el procedimiento de enlace debe pasar el mensaje a la función [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sin más procesamiento y debe devolver el valor devuelto por **CallNextHookEx**.
Este parámetro puede ser uno de los valores siguientes.

| Valor | Significado |
|-------|---------|
| **HC_ACTION** 0 | Los *parámetros wParam* *y lParam* contienen información sobre un mensaje del mouse. |

### <a name="wparam-in"></a>wParam [in]

Tipo: **WPARAM**

Identificador del mensaje del mouse.
Este parámetro puede ser uno de los siguientes mensajes: [WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown), [WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup), [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove), [WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel), [WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown) [o WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup).

### <a name="lparam-in"></a>lParam [in]

Tipo: **LPARAM**

Puntero a una [estructura MSLLHOOKSTRUCT.](/windows/desktop/api/winuser/ns-winuser-msllhookstruct)

## <a name="returns"></a>Devoluciones

Tipo: **LRESULT**

Si *nCode* es menor que cero, el procedimiento de enlace debe devolver el valor devuelto por **CallNextHookEx**.

Si *nCode* es mayor o igual que cero y el procedimiento de enlace no procesó el mensaje, se recomienda encarecidamente llamar a **CallNextHookEx** y devolver el valor que devuelve. De lo contrario, otras aplicaciones que [WH_MOUSE_LL](about-hooks.md) enlaces no recibirán notificaciones de enlace y pueden comportarse incorrectamente como resultado.
Si el procedimiento de enlace procesó el mensaje, puede devolver un valor distinto de cero para evitar que el sistema pase el mensaje al resto de la cadena de enlace o al procedimiento de ventana de destino.

## <a name="remarks"></a>Comentarios

Una aplicación instala el procedimiento de  enlace especificando WH_MOUSE_LL tipo de enlace y un puntero al procedimiento de enlace en una llamada a la **función SetWindowsHookEx.**

Se llama a este enlace en el contexto del subproceso que lo instaló.
La llamada se realiza mediante el envío de un mensaje al subproceso que instaló el enlace.
Por lo tanto, el subproceso que instaló el enlace debe tener un bucle de mensajes.

La entrada del mouse puede procede del controlador del mouse local o de las llamadas [a](/windows/desktop/api/winuser/nf-winuser-mouse_event) mouse_event función.
Si la entrada procede de una llamada a **mouse_event**, la entrada se "inyectó".
Sin embargo, **WH_MOUSE_LL** enlace no se inserta en otro proceso.
En su lugar, el contexto vuelve al proceso que instaló el enlace y se llama a él en su contexto original.
A continuación, el contexto vuelve a la aplicación que generó el evento.

El procedimiento de enlace debe procesar un mensaje en menos tiempo que la entrada de datos especificada en el valor **LowLevelHooksTimeout** en la siguiente clave del **Registro:HKEY_CURRENT_USER\Control Panel\Desktop**.

El valor se expresa en milisegundos.
Si se supera el tiempo de espera del procedimiento de enlace, el sistema pasa el mensaje al siguiente enlace.
Sin embargo, en Windows 7 y versiones posteriores, el enlace se quita en modo silencioso sin que se llame a .
No hay ninguna manera de que la aplicación sepa si se quita el enlace.

**Nota:**  Los enlaces de depuración no pueden realizar un seguimiento de este tipo de enlaces de mouse de bajo nivel.
Si la aplicación debe usar enlaces de bajo nivel, debe ejecutar los enlaces en un subproceso dedicado que pase el trabajo a un subproceso de trabajo y, a continuación, vuelva inmediatamente.
En la mayoría de los casos en los que la aplicación necesita usar enlaces de bajo nivel, debe supervisar la entrada sin procesar en su lugar.
Esto se debe a que la entrada sin procesar puede supervisar de forma asincrónica los mensajes del mouse y el teclado destinados a otros subprocesos de forma más eficaz que los enlaces de bajo nivel.
Para obtener más información sobre la entrada sin procesar, vea [Raw Input](/windows/desktop/inputdev/raw-input).

## <a name="see-also"></a>Consulte también

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event)

[KBDLDLOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[MSLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-msllhookstruct)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown)

[WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup)

[WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove)

[WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel)

[WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown)

[WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup)

[Enlaces](hooks.md)

[Acerca de los enlaces](about-hooks.md)
