---
description: Se envía para cancelar determinados modos, como la captura del mouse.
ms.assetid: c801233a-c4d8-4fd9-aaf0-3d4503bbce26
title: Mensaje de WM_CANCELMODE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23b842dfdfde7dc550d8ec6d942bcc83ea25f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706674"
---
# <a name="wm_cancelmode-message"></a>Mensaje de CANCELMODE de WM \_

Se envía para cancelar determinados modos, como la captura del mouse. Por ejemplo, el sistema envía este mensaje a la ventana activa cuando se muestra un cuadro de diálogo o un cuadro de mensaje. Ciertas funciones también envían este mensaje explícitamente a la ventana especificada independientemente de si se trata de la ventana activa. Por ejemplo, la función [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) envía este mensaje al deshabilitar la ventana especificada.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_CANCELMODE                   0x001F
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

Cuando se envía el mensaje de **\_ CANCELMODE de WM** , la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) cancela el procesamiento interno de la entrada de la barra de desplazamiento estándar, cancela el procesamiento interno del menú y libera la captura del mouse.

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

[**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

[**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
