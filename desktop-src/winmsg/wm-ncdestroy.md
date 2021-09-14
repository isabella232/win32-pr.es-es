---
description: Notifica a una ventana que se está destruyendo su área no cliente. La función DestroyWindow envía el mensaje \_ WM NCDESTROY a la ventana que sigue al mensaje WM \_ DESTROY.
ms.assetid: 64ab268d-0e90-4401-81d3-a4da64196001
title: WM_NCDESTROY mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a462f679a29f471638299e037749adaf32a85dea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251672"
---
# <a name="wm_ncdestroy-message"></a>Mensaje \_ WM NCDESTROY

Notifica a una ventana que se está destruyendo su área no cliente. La [**función DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) envía el mensaje **WM \_ NCDESTROY** a la ventana que sigue al [**mensaje WM \_ DESTROY.**](wm-destroy.md) [**WM \_ DESTROY**](wm-destroy.md) se usa para liberar el objeto de memoria asignado asociado a la ventana.

El **mensaje \_ WM NCDESTROY** se envía después de que se hayan destruido las ventanas secundarias. En cambio, [**WM \_ DESTROY**](wm-destroy.md) se envía antes de que se destruyan las ventanas secundarias.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCDESTROY                    0x0082
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

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Este mensaje libera cualquier memoria asignada internamente para la ventana.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**WM \_ DESTROY**](wm-destroy.md)
</dt> <dt>

[**WM \_ NCCREATE**](wm-nccreate.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
