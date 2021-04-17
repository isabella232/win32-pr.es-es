---
UID: ''
title: Función de devolución de llamada MouseProc
description: El sistema llama a esta función cuando una aplicación llama a una función de mensaje y hay un mensaje de mouse que se va a procesar.
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
ms.openlocfilehash: abdd74b5fed93e2c2ddbc8d037a657b779a62a05
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/11/2020
ms.locfileid: "105704927"
---
# <a name="mouseproc-function"></a>MouseProc función)

## <a name="description"></a>Descripción

Función de devolución de llamada definida por la aplicación o definida por la biblioteca que se usa con la función [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
El sistema llama a esta función cada vez que una aplicación llama a la función [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) o [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) y hay un mensaje del mouse que se va a procesar.

El tipo **HOOKPROC** define un puntero a esta función de devolución de llamada.
**MouseProc** es un marcador de posición para el nombre de la función definida por la aplicación o por la biblioteca.

```cpp
LRESULT CALLBACK MouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parámetros

### <a name="ncode-in"></a>nCode [in]

Tipo: **int**

Código que utiliza el procedimiento de enlace para determinar cómo procesar el mensaje.
Si *nCode* es menor que cero, el procedimiento de enlace debe pasar el mensaje a la función [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sin más procesamiento y debe devolver el valor devuelto por **CallNextHookEx**.
Este parámetro puede ser uno de los valores siguientes.

| Valor | Significado |
|-------|---------|
| **HC_ACTION** 0 | Los parámetros *wParam* e *lParam* contienen información sobre un mensaje del mouse. |
| **HC_NOREMOVE** 3 | Los parámetros *wParam* e *lParam* contienen información sobre un mensaje del mouse y el mensaje del mouse no se ha quitado de la cola de mensajes. (Una aplicación llamada la función **PeekMessage** , que especifica la marca **PM_NOREMOVE** ). |

### <a name="wparam-in"></a>wParam [in]

Tipo: **wParam**

Identificador del mensaje del mouse.

### <a name="lparam-in"></a>lParam [in]

Tipo: **lParam**

Puntero a una estructura [MOUSEHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-mousehookstruct) .

## <a name="returns"></a>Devoluciones

Tipo: **LRESULT**

Si *nCode* es menor que cero, el procedimiento de enlace debe devolver el valor devuelto por **CallNextHookEx**.

Si *nCode* es mayor o igual que cero y el procedimiento de enlace no procese el mensaje, se recomienda encarecidamente llamar a **CallNextHookEx** y devolver el valor que devuelve; de lo contrario, otras aplicaciones que tengan instalado [WH_MOUSE](about-hooks.md) enlaces no recibirán notificaciones de enlace y se comportarán de forma incorrecta como resultado.
Si el procedimiento de enlace ha procesado el mensaje, es posible que devuelva un valor distinto de cero para evitar que el sistema pase el mensaje al procedimiento de ventana de destino.

## <a name="remarks"></a>Observaciones

Una aplicación instala el procedimiento de enlace especificando el tipo de enlace de WH_MOUSE y un puntero al procedimiento de enlace en una llamada a la función **SetWindowsHookEx** .

El procedimiento de enlace no debe instalar una función de devolución de llamada [WH_JOURNALPLAYBACK](about-hooks.md) .

Este enlace se puede llamar en el contexto del subproceso que lo instaló.
La llamada se realiza mediante el envío de un mensaje al subproceso que instaló el enlace.
Por lo tanto, el subproceso que instaló el enlace debe tener un bucle de mensajes.

## <a name="see-also"></a>Vea también

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[MOUSEHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-mousehookstruct)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Enlaces](hooks.md)

[Acerca de los enlaces](about-hooks.md)
