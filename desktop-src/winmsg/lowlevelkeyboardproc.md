---
UID: ''
title: Función de devolución de llamada LowLevelKeyboardProc
description: El sistema llama a esta función cada vez que se va a publicar un nuevo evento de entrada de teclado en una cola de entrada del subproceso.
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
ms.openlocfilehash: f33acbb6888bad97a03b610c513cbaf9c3750684
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/11/2020
ms.locfileid: "104077474"
---
# <a name="lowlevelkeyboardproc-function"></a>LowLevelKeyboardProc función)

## <a name="description"></a>Descripción

Función de devolución de llamada definida por la aplicación o definida por la biblioteca que se usa con la función [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
El sistema llama a esta función cada vez que se va a publicar un nuevo evento de entrada de teclado en una cola de entrada del subproceso.

**Nota:**  Cuando se llama a esta función de devolución de llamada en respuesta a un cambio en el estado de una clave, se llama a la función de devolución de llamada antes de que se actualice el estado asincrónico de la clave.
Por consiguiente, el estado asincrónico de la clave no se puede determinar mediante una llamada a [GetAsyncKeyState](/windows/desktop/api/winuser/nf-winuser-getasynckeystate) desde dentro de la función de devolución de llamada.

El tipo **HOOKPROC** define un puntero a esta función de devolución de llamada.
**LowLevelKeyboardProc** es un marcador de posición para el nombre de la función definida por la aplicación o por la biblioteca.

```cpp
LRESULT CALLBACK LowLevelKeyboardProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parámetros

### <a name="code-in"></a>código [in]

Tipo: **int**

Código que utiliza el procedimiento de enlace para determinar cómo procesar el mensaje.
Si *nCode* es menor que cero, el procedimiento de enlace debe pasar el mensaje a la función [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sin más procesamiento y debe devolver el valor devuelto por **CallNextHookEx**.
Este parámetro puede ser uno de los valores siguientes.

| Valor | Significado |
|-------|---------|
| **HC_ACTION** 0 | Los parámetros *wParam* e *lParam* contienen información sobre un mensaje de teclado. |

### <a name="wparam-in"></a>wParam [in]

Tipo: **wParam**

Identificador del mensaje de teclado.
Este parámetro puede ser uno de los siguientes mensajes: [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown), [WM_KEYUP](/windows/desktop/inputdev/wm-keyup), [WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown)o [WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup).

### <a name="lparam-in"></a>lParam [in]

Tipo: **lParam**

Puntero a una estructura [KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct) .

## <a name="returns"></a>Devoluciones

Tipo: **LRESULT**

Si *nCode* es menor que cero, el procedimiento de enlace debe devolver el valor devuelto por **CallNextHookEx**.

Si *nCode* es mayor o igual que cero y el procedimiento de enlace no procese el mensaje, se recomienda encarecidamente llamar a **CallNextHookEx** y devolver el valor que devuelve; de lo contrario, otras aplicaciones que tengan instalado [WH_KEYBOARD_LL](about-hooks.md) enlaces no recibirán notificaciones de enlace y se comportarán de forma incorrecta como resultado.
Si el procedimiento de enlace ha procesado el mensaje, es posible que devuelva un valor distinto de cero para evitar que el sistema pase el mensaje al resto de la cadena de enlace o al procedimiento de ventana de destino.

## <a name="remarks"></a>Observaciones

Una aplicación instala el procedimiento de enlace especificando el tipo de enlace de **WH_KEYBOARD_LL** y un puntero al procedimiento de enlace en una llamada a la función **SetWindowsHookEx** .

Este enlace se llama en el contexto del subproceso que lo instaló.
La llamada se realiza mediante el envío de un mensaje al subproceso que instaló el enlace.
Por lo tanto, el subproceso que instaló el enlace debe tener un bucle de mensajes.

La entrada del teclado puede proviene del controlador de teclado local o de las llamadas a la función [keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event) .
Si la entrada procede de una llamada a **keybd_event**, la entrada se "insertó".
Sin embargo, el enlace de WH_KEYBOARD_LL no se inserta en otro proceso.
En su lugar, el contexto vuelve a cambiar al proceso que instaló el enlace y se llama en su contexto original.
A continuación, el contexto vuelve a la aplicación que generó el evento.

El procedimiento de enlace debe procesar un mensaje en menos tiempo que la entrada de datos especificada en el valor **LowLevelHooksTimeout** en la siguiente clave del registro: **HKEY_CURRENT_USER\Control Panel\Desktop**.

El valor se expresa en milisegundos.
Si el procedimiento de enlace agota el tiempo de espera, el sistema pasa el mensaje al siguiente enlace.
Sin embargo, en Windows 7 y versiones posteriores, el enlace se quita de forma silenciosa sin llamar a.
No hay ninguna manera de que la aplicación sepa si se quita el enlace.

Nota: los enlaces de depuración no pueden realizar un seguimiento de este tipo de enlaces de teclado de bajo nivel.
Si la aplicación debe usar enlaces de nivel bajo, debe ejecutar los enlaces en un subproceso dedicado que pase el trabajo a un subproceso de trabajo y, a continuación, devuelva inmediatamente.
En la mayoría de los casos en los que la aplicación necesita usar enlaces de nivel bajo, debe supervisar en su lugar la entrada sin formato.
Esto se debe a que la entrada sin formato puede supervisar de forma asincrónica los mensajes de teclado y del mouse que están destinados a otros subprocesos de forma más eficaz que los enlaces de bajo nivel.
Para obtener más información sobre la entrada sin formato, consulte [entrada sin formato](/windows/desktop/inputdev/raw-input).

## <a name="see-also"></a>Vea también

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)

[WM_KEYUP](/windows/desktop/inputdev/wm-keyup)

[WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown)

[WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup)

[Enlaces](hooks.md)

[Acerca de los enlaces](about-hooks.md)
