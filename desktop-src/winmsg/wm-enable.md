---
description: Se envía cuando una aplicación cambia el estado habilitado de una ventana.
ms.assetid: df2cf953-121f-43bb-a06c-d10e445bfb5e
title: Mensaje de WM_ENABLE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc83b84cbbf8e0c0145ef7d2730179cab54a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697374"
---
# <a name="wm_enable-message"></a>\_Mensaje de habilitación de WM

Se envía cuando una aplicación cambia el estado habilitado de una ventana. Se envía a la ventana cuyo estado habilitado está cambiando. Este mensaje se envía antes de que se devuelva la función [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) , pero después de que se haya cambiado el estado habilitado (bit de estilo [**WS \_ Disabled**](window-styles.md) ) de la ventana.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_ENABLE                       0x000A
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica si la ventana se ha habilitado o deshabilitado. Este parámetro es **true** si se ha habilitado la ventana o **false** si se ha deshabilitado la ventana.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si una aplicación procesa este mensaje, debe devolver cero.

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

[**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
