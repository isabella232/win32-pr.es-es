---
description: Se envía una vez a una ventana después de entrar en el bucle modal de movimiento o tamaño.
ms.assetid: fe09db71-2c79-47f2-b575-516e960915d4
title: WM_ENTERSIZEMOVE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0ffbd3ac8c65b68998a37e64df2593c183b61adb3f8eba1fa140251174b503d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118436260"
---
# <a name="wm_entersizemove-message"></a>Mensaje \_ DE WM ENTERSIZEMOVE

Se envía una vez a una ventana después de entrar en el bucle modal de movimiento o tamaño. La ventana entra en el bucle modal de movimiento o tamaño cuando el usuario hace clic en la barra de título o el borde de tamaño de la ventana, o cuando la ventana pasa el mensaje [**\_ SYSCOMMAND**](../menurc/wm-syscommand.md) de WM a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) y el parámetro *wParam* del mensaje especifica el valor **SC \_ MOVE** **o SC \_ SIZE.** La operación se completa cuando [**se devuelve DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

El sistema envía el **mensaje \_ WM ENTERSIZEMOVE** independientemente de si está habilitado el arrastre de ventanas completa.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_ENTERSIZEMOVE                0x0231
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

[**WM \_ EXITSIZEMOVE**](wm-exitsizemove.md)
</dt> <dt>

[**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
