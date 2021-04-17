---
description: Se envía una vez a una ventana una vez que entra en el bucle modal de movimiento o de ajuste de tamaño.
ms.assetid: fe09db71-2c79-47f2-b575-516e960915d4
title: Mensaje de WM_ENTERSIZEMOVE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfaf27c888311991b88278a9d4e69482efd06111
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706671"
---
# <a name="wm_entersizemove-message"></a>Mensaje de ENTERSIZEMOVE de WM \_

Se envía una vez a una ventana una vez que entra en el bucle modal de movimiento o de ajuste de tamaño. La ventana entra en el bucle modal de movimiento o cambio de tamaño cuando el usuario hace clic en la barra de título o en el borde de tamaño de la ventana, o cuando la ventana pasa el mensaje de [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) y el parámetro *wParam* del mensaje especifica el valor **SC \_ Move** o **SC \_ size** . La operación se completa cuando [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve.

El sistema envía el mensaje de **WM \_ ENTERSIZEMOVE** independientemente de si está habilitada la opción de arrastrar ventanas completas.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**EXITSIZEMOVE de WM \_**](wm-exitsizemove.md)
</dt> <dt>

[**SYSCOMMAND de WM \_**](../menurc/wm-syscommand.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
