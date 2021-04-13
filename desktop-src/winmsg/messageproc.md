---
UID: ''
title: Función de devolución de llamada MessageProc
description: El sistema llama a esta función después de que se produzca un evento de entrada en un cuadro de diálogo, un cuadro de mensaje, un menú o una barra de desplazamiento. | Función de devolución de llamada MessageProc
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
ms.openlocfilehash: 00a1d1c52d50d0d9a028829181c886a813112a15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362313"
---
# <a name="messageproc-function"></a>MessageProc función)

## <a name="description"></a>Descripción

Función de devolución de llamada definida por la aplicación o definida por la biblioteca que se usa con la función [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
El sistema llama a esta función después de que se produzca un evento de entrada en un cuadro de diálogo, un cuadro de mensaje, un menú o una barra de desplazamiento, pero antes de que se procese el mensaje generado por el evento de entrada.
El procedimiento de enlace puede supervisar los mensajes de un cuadro de diálogo, un cuadro de mensaje, un menú o una barra de desplazamiento creados por una aplicación determinada o por todas las aplicaciones.

El tipo **HOOKPROC** define un puntero a esta función de devolución de llamada.
**MessageProc** es un marcador de posición para el nombre de la función definida por la aplicación o por la biblioteca.

```cpp
LRESULT CALLBACK MessageProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parámetros

### <a name="code-in"></a>código [in]

Tipo: **int**

El tipo de evento de entrada que generó el mensaje.
Si el *código* es menor que cero, el procedimiento de enlace debe pasar el mensaje a la función [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sin más procesamiento y devolver el valor devuelto por **CallNextHookEx**.
Este parámetro puede ser uno de los valores siguientes.

| Valor | Significado |
|-------|---------|
| **MSGF_DDEMGR** 0x8001 | El evento de entrada se produjo mientras la biblioteca de administración de Intercambio dinámico de datos (DDEML) estaba esperando a que finalizara una transacción sincrónica. Para obtener más información acerca de DDEML, consulte [biblioteca de administración de intercambio dinámico de datos](../dataxchg/dynamic-data-exchange-management-library.md). |
| **MSGF_DIALOGBOX** 0 | El evento de entrada se produjo en un cuadro de mensaje o en un cuadro de diálogo. |
| **MSGF_MENU** 2 | El evento de entrada se produjo en un menú. |
| **MSGF_SCROLLBAR** 5 | El evento de entrada se produjo en una barra de desplazamiento. |

### <a name="wparam"></a>wParam

Tipo: **wParam**

Este parámetro no se utiliza.

### <a name="lparam-in"></a>lParam [in]

Tipo: **lParam**

Puntero a una estructura [MSG](/windows/win32/api/winuser/ns-winuser-msg) .

## <a name="returns"></a>Devoluciones

Tipo: **LRESULT**

Si el *código* es menor que cero, el procedimiento de enlace debe devolver el valor devuelto por **CallNextHookEx**.

Si el *código* es mayor o igual que cero y el procedimiento de enlace no procese el mensaje, se recomienda encarecidamente llamar a **CallNextHookEx** y devolver el valor que devuelve; de lo contrario, otras aplicaciones que tengan instalado [WH_MSGFILTER](about-hooks.md) enlaces no recibirán notificaciones de enlace y se comportarán de forma incorrecta como resultado.
Si el procedimiento de enlace ha procesado el mensaje, es posible que devuelva un valor distinto de cero para evitar que el sistema pase el mensaje al resto de la cadena de enlace o al procedimiento de ventana de destino.

## <a name="remarks"></a>Observaciones

Una aplicación instala el procedimiento de enlace especificando el tipo de enlace de **WH_MSGFILTER** y un puntero al procedimiento de enlace en una llamada a la función **SetWindowsHookEx** .

Si una aplicación que usa DDEML y realiza transacciones sincrónicas debe procesar los mensajes antes de que se envíen, debe usar el **WH_MSGFILTER** enlace.

## <a name="see-also"></a>Vea también

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[MENSAJE](/windows/win32/api/winuser/ns-winuser-msg)

[Enlaces](hooks.md)
