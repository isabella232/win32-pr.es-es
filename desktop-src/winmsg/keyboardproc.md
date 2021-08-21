---
UID: ''
title: Función de devolución de llamada KeyboardProc
description: El sistema llama a esta función para obtener una función de mensaje y hay un mensaje de teclado para procesar.
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
ms.openlocfilehash: ed2f3943667d09f42a7bc843adac69eaa4043454d93b409b193513b8ab43fd63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437161"
---
# <a name="keyboardproc-function"></a>Función KeyboardProc

## <a name="description"></a>Descripción

Función de devolución de llamada definida por la aplicación o definida por la biblioteca que se usa con la [función SetWindowsHookEx.](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)
El sistema llama a esta función cada vez que una aplicación llama a la función [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) o [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) y hay un mensaje de teclado[(WM_KEYUP](/windows/desktop/inputdev/wm-keyup) [o WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)) que se va a procesar.

El **tipo HOOKPROC** define un puntero a esta función de devolución de llamada.
**KeyboardProc es** un marcador de posición para el nombre de función definido por la aplicación o definido por la biblioteca.

```cpp
LRESULT CALLBACK KeyboardProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parámetros

### <a name="code-in"></a>código [in]

Tipo: **int**

Código que el procedimiento de enlace usa para determinar cómo procesar el mensaje.
Si *el* código es menor que cero, el procedimiento de enlace debe pasar el mensaje a la función [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sin procesarlo más y debe devolver el valor devuelto por **CallNextHookEx**.
Este parámetro puede ser uno de los valores siguientes.

| Valor | Significado |
|-------|---------|
| **HC_ACTION** 0 | Los *parámetros wParam* *y lParam* contienen información sobre un mensaje de pulsación de tecla. |
| **HC_NOREMOVE** 3 | Los *parámetros wParam* y *lParam* contienen información sobre un mensaje de pulsación de tecla y el mensaje de pulsación de tecla no se ha quitado de la cola de mensajes. (Una aplicación denominada función **PeekMessage,** que especifica la **PM_NOREMOVE** marca). |

### <a name="wparam-in"></a>wParam [in]

Tipo: **WPARAM**

Código [de clave virtual de](/windows/desktop/inputdev/virtual-key-codes) la clave que generó el mensaje de pulsación de tecla.

### <a name="lparam-in"></a>lParam [in]

Tipo: **LPARAM**

Recuento de repeticiones, código de examen, marca de clave extendida, código de contexto, marca de estado de clave anterior y marca de estado de transición.
Para obtener más información sobre el *parámetro lParam,* vea [Marcas de mensajes de pulsación de teclas](/windows/desktop/inputdev/about-keyboard-input).
En la tabla siguiente se describen los bits de este valor.

| Bits | Descripción |
|-------|---------|
| 0-15 | Recuento de repeticiones. El valor es el número de veces que se repite la pulsación de tecla como resultado de que el usuario mantiene presionada la tecla. |
| 16-23 | Código de examen. El valor depende del OEM. |
| 24 | Indica si la clave es una clave extendida, como una clave de función o una clave en el teclado numérico. El valor es 1 si la clave es una clave extendida; de lo contrario, es 0. |
| 25-28 | Reservado. |
| 29 | Código de contexto. El valor es 1 si la tecla ALT está presionada; De lo contrario, es 0. |
| 30 | Estado de la clave anterior. El valor es 1 si la clave está abajo antes de que se envíe el mensaje; es 0 si la clave está arriba. |
| 31 | Estado de transición. El valor es 0 si se presiona la tecla y 1 si se va a liberar. |

## <a name="returns"></a>Devoluciones

Tipo: **LRESULT**

Si *el* código es menor que cero, el procedimiento de enlace debe devolver el valor devuelto por **CallNextHookEx**.

Si *el* código es mayor o igual que cero y el procedimiento de enlace no procesó el mensaje, se recomienda encarecidamente llamar a **CallNextHookEx** y devolver el valor que devuelve. De lo contrario, otras aplicaciones que [WH_KEYBOARD](about-hooks.md) enlaces no recibirán notificaciones de enlace y pueden comportarse incorrectamente como resultado.
Si el procedimiento de enlace procesó el mensaje, puede devolver un valor distinto de cero para evitar que el sistema pase el mensaje al resto de la cadena de enlace o al procedimiento de ventana de destino.

## <a name="remarks"></a>Comentarios

Una aplicación instala el procedimiento de  enlace especificando el tipo de enlace WH_KEYBOARD y un puntero al procedimiento de enlace en una llamada a la función **SetWindowsHookEx.**

Se puede llamar a este enlace en el contexto del subproceso que lo instaló.
La llamada se realiza mediante el envío de un mensaje al subproceso que instaló el enlace.
Por lo tanto, el subproceso que instaló el enlace debe tener un bucle de mensajes.

## <a name="see-also"></a>Consulte también

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_KEYUP](/windows/desktop/inputdev/wm-keyup)

[WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)

[Enlaces](hooks.md)
