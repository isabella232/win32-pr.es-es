---
description: Se envía una vez a una ventana, una vez que ha salido del bucle modal de movimiento o de ajuste de tamaño.
ms.assetid: 3466bfb5-c38d-49d8-a4ab-bf23d09c454c
title: Mensaje de WM_EXITSIZEMOVE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22eda44827345ef491814aab69bf0b802b924e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720608"
---
# <a name="wm_exitsizemove-message"></a>Mensaje de EXITSIZEMOVE de WM \_

Se envía una vez a una ventana, una vez que ha salido del bucle modal de movimiento o de ajuste de tamaño. La ventana especifica el bucle modal de movimiento o cambio de tamaño cuando el usuario hace clic en la barra de título o en el borde de tamaño de la ventana, o cuando la ventana pasa el mensaje de [**\_ SYSCOMMAND de WM**](../menurc/wm-syscommand.md) a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) y el parámetro *wParam* del mensaje especifica el valor de **\_ tamaño** **SC \_ MOV** E o SC. La operación se completa cuando [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

[**ENTERSIZEMOVE de WM \_**](wm-entersizemove.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
