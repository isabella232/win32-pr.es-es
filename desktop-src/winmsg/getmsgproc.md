---
UID: ''
title: Función de devolución de llamada GetMsgProc
description: El sistema llama a esta función cuando una función de mensaje obtiene un mensaje de una cola de mensajes de aplicación.
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
ms.openlocfilehash: e5c51f2abe8b3660ae40bae05c13428e0622fd4d5c4b8020fea8caa924a35681
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200797"
---
# <a name="getmsgproc-function"></a>Función GetMsgProc

## <a name="-description"></a>-description

Función de devolución de llamada definida por la aplicación o definida por la biblioteca que se usa con la [función SetWindowsHookEx.](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) El sistema llama a esta función cada vez que la función [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) [o PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) ha recuperado un mensaje de una cola de mensajes de aplicación.
Antes de devolver el mensaje recuperado al autor de la llamada, el sistema pasa el mensaje al procedimiento de enlace.

El **tipo HOOKPROC** define un puntero a esta función de devolución de llamada.
**GetMsgProc es** un marcador de posición para el nombre de función definido por la aplicación o definido por la biblioteca.

```cpp
LRESULT CALLBACK GetMsgProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="-parameters"></a>-parameters

### <a name="code-in"></a>code [in]

Tipo: **int**

Especifica si el procedimiento de enlace debe procesar el mensaje.
Si *el* código **HC_ACTION**, el procedimiento de enlace debe procesar el mensaje.
Si *el* código es menor que cero, el procedimiento de enlace debe pasar el mensaje a la función [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sin más procesamiento y debe devolver el valor devuelto por **CallNextHookEx**.

### <a name="wparam-in"></a>wParam [in]

Tipo: **WPARAM**

Especifica si el mensaje se ha quitado de la cola.
Este parámetro puede ser uno de los valores siguientes.

| Valor | Significado |
|-------|---------|
| **PM_NOREMOVE** 0x0000 | El mensaje no se ha quitado de la cola. (Una aplicación denominada función **PeekMessage,** que especifica la **marca PM_NOREMOVE).** |
| **PM_REMOVE** 0x0001 | El mensaje se ha quitado de la cola. (Una aplicación denominada **GetMessage** o la función  **PeekMessage,** especificando el **PM_REMOVE** marca).|

### <a name="lparam-in"></a>lParam [in]

Tipo: **LPARAM**

Puntero a una [estructura MSG](/windows/desktop/api/winuser/ns-winuser-msg) que contiene detalles sobre el mensaje.

## <a name="-returns"></a>-returns

Si *el* código es menor que cero, el procedimiento de enlace debe devolver el valor devuelto por [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex).

Si *el* código es mayor o igual que cero, se recomienda encarecidamente llamar a **CallNextHookEx** y devolver el valor que devuelve. De lo contrario, otras aplicaciones que tienen instalados [WH_GETMESSAGE](about-hooks.md) de enlace no recibirán notificaciones de enlace y pueden comportarse incorrectamente como resultado.
Si el procedimiento de enlace no llama a **CallNextHookEx**, el valor devuelto debe ser cero.

## <a name="-remarks"></a>-remarks

El **procedimiento de enlace GetMsgProc** puede examinar o modificar el mensaje.
Una vez que el procedimiento de enlace devuelve el control al sistema, la función **GetMessage** o **PeekMessage** devuelve el mensaje, junto con las modificaciones, a la aplicación que lo llamó originalmente.

Una aplicación instala este procedimiento de  enlace especificando WH_GETMESSAGE tipo de enlace y un puntero al procedimiento de enlace en una llamada a la **función SetWindowsHookEx.**

## <a name="see-also"></a>Consulte también

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[Msg](/windows/desktop/api/winuser/ns-winuser-msg)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Enlaces](hooks.md)
