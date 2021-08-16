---
description: Se envía una vez a una ventana, después de salir del bucle modal de movimiento o tamaño.
ms.assetid: 3466bfb5-c38d-49d8-a4ab-bf23d09c454c
title: WM_EXITSIZEMOVE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f451e846f2a262a30ccc73121d52c3732dbdfb160fe529535dcf353f077c351
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849257"
---
# <a name="wm_exitsizemove-message"></a>Mensaje \_ EXITSIZEMOVE de WM

Se envía una vez a una ventana, después de salir del bucle modal de movimiento o tamaño. La ventana entra en el bucle modal de movimiento o tamaño cuando el usuario hace clic en la barra de título o el borde de tamaño de la ventana, o cuando la ventana pasa el mensaje [**\_ SYSCOMMAND**](../menurc/wm-syscommand.md) wm a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) y el parámetro *wParam* del mensaje especifica el valor **SC \_ MOV** E **o SC \_ SIZE.** La operación se completa cuando [**se devuelve DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_EXITSIZEMOVE                 0x0232
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ ENTERSIZEMOVE**](wm-entersizemove.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
