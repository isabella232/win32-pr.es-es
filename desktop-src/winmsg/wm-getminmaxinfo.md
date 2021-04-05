---
description: Se envía a una ventana cuando el tamaño o la posición de la ventana está a punto de cambiar. Una aplicación puede usar este mensaje para invalidar el tamaño maximizado y la posición predeterminados de la ventana, o el tamaño de seguimiento máximo o mínimo predeterminado.
ms.assetid: af2295e0-2d0b-4ac0-b689-16138022f4b7
title: Mensaje de WM_GETMINMAXINFO (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29cbca97d38f7fca90c93ef7bf0606ea49306da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911377"
---
# <a name="wm_getminmaxinfo-message"></a>Mensaje de GETMINMAXINFO de WM \_

Se envía a una ventana cuando el tamaño o la posición de la ventana está a punto de cambiar. Una aplicación puede usar este mensaje para invalidar el tamaño maximizado y la posición predeterminados de la ventana, o el tamaño de seguimiento máximo o mínimo predeterminado.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_GETMINMAXINFO                0x0024
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**minmaxinfo (**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) que contiene las dimensiones y la posición maximizadas predeterminadas, y los tamaños de seguimiento mínimo y máximo predeterminados. Una aplicación puede invalidar los valores predeterminados estableciendo los miembros de esta estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

El tamaño máximo de seguimiento es el tamaño de ventana más grande que se puede generar mediante el uso de los bordes para ajustar el tamaño de la ventana. El tamaño mínimo de seguimiento es el tamaño de ventana más pequeño que se puede generar mediante el uso de los bordes para ajustar el tamaño de la ventana.

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

[**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**MINMAXINFO (**](/windows/win32/api/winuser/ns-winuser-minmaxinfo)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
