---
UID: ''
title: Función de devolución de llamada SysMsgProc
description: El sistema llama a esta función después de que se produzca un evento de entrada en un cuadro de diálogo, un cuadro de mensaje, un menú o una barra de desplazamiento. | Función de devolución de llamada SysMsgProc
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
ms.openlocfilehash: 0d5c7fc116b74dada141e88116ba67209da4a103
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105707711"
---
# <a name="sysmsgproc-function"></a>SysMsgProc función)

## <a name="description"></a>Descripción

Función de devolución de llamada definida por la aplicación o definida por la biblioteca que se usa con la función [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
El sistema llama a esta función después de que se produzca un evento de entrada en un cuadro de diálogo, un cuadro de mensaje, un menú o una barra de desplazamiento, pero antes de que se procese el mensaje generado por el evento de entrada.
La función puede supervisar los mensajes de cualquier cuadro de diálogo, cuadro de mensaje, menú o barra de desplazamiento del sistema.

El tipo **HOOKPROC** define un puntero a esta función de devolución de llamada.
**SysMsgProc** es un marcador de posición para el nombre de la función definida por la aplicación o por la biblioteca.

```cpp
LRESULT CALLBACK SysMsgProc(
  _In_ int    nCode,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parámetros

### <a name="ncode-in"></a>nCode [in]

Tipo: **int**

El tipo de evento de entrada que generó el mensaje.
Si *nCode* es menor que cero, el procedimiento de enlace debe pasar el mensaje a la función [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sin más procesamiento y debe devolver el valor devuelto por **CallNextHookEx**.
Este parámetro puede ser uno de los valores siguientes.

| Valor | Significado |
|-------|---------|
| **MSGF_DIALOGBOX** 0 | El evento de entrada se produjo en un cuadro de mensaje o en un cuadro de diálogo. |
| **MSGF_MENU** 2 | El evento de entrada se produjo en un menú. |
| **MSGF_SCROLLBAR** 5 | El evento de entrada se produjo en una barra de desplazamiento. |

### <a name="wparam"></a>wParam

Tipo: **wParam**

Este parámetro no se utiliza.

### <a name="lparam-in"></a>lParam [in]

Tipo: **lParam**

Puntero a una estructura de mensaje [MSG](/windows/desktop/api/winuser/ns-winuser-msg) .

## <a name="returns"></a>Devoluciones

Tipo: **LRESULT**

Si *nCode* es menor que cero, el procedimiento de enlace debe devolver el valor devuelto por **CallNextHookEx**.

Si *nCode* es mayor o igual que cero y el procedimiento de enlace no procese el mensaje, se recomienda encarecidamente llamar a **CallNextHookEx** y devolver el valor que devuelve; de lo contrario, otras aplicaciones que tengan instalado [WH_SYSMSGFILTER](about-hooks.md) enlaces no recibirán notificaciones de enlace y se comportarán de forma incorrecta como resultado.
Si el procedimiento de enlace ha procesado el mensaje, es posible que devuelva un valor distinto de cero para evitar que el sistema pase el mensaje al procedimiento de ventana de destino.

## <a name="remarks"></a>Observaciones

Una aplicación instala el procedimiento de enlace especificando el tipo de enlace de **WH_SYSMSGFILTER** y un puntero al procedimiento de enlace en una llamada a la función **SetWindowsHookEx** .

## <a name="see-also"></a>Vea también

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[MENSAJE](/windows/desktop/api/winuser/ns-winuser-msg)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Enlaces](hooks.md)
