---
description: Notifica a una ventana que se está destruyendo su área no cliente. La función DestroyWindow envía el mensaje de NCDESTROY de WM \_ a la ventana después del mensaje de destrucción de WM \_ .
ms.assetid: 64ab268d-0e90-4401-81d3-a4da64196001
title: Mensaje de WM_NCDESTROY (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a462f679a29f471638299e037749adaf32a85dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104002026"
---
# <a name="wm_ncdestroy-message"></a>Mensaje de NCDESTROY de WM \_

Notifica a una ventana que se está destruyendo su área no cliente. La función [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) envía el mensaje de **\_ NCDESTROY de WM** a la ventana después del mensaje de [**\_ destrucción de WM**](wm-destroy.md) .[**WM \_ Destroy**](wm-destroy.md) se usa para liberar el objeto de memoria asignado asociado a la ventana.

El mensaje de **\_ NCDESTROY de WM** se envía después de que se hayan destruido las ventanas secundarias. En cambio, [**la \_ destrucción de WM**](wm-destroy.md) se envía antes de que se destruyan las ventanas secundarias.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**destrucción de WM \_**](wm-destroy.md)
</dt> <dt>

[**NCCREATE de WM \_**](wm-nccreate.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
