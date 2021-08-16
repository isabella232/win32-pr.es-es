---
description: Se envía para cancelar determinados modos, como la captura del mouse.
ms.assetid: c801233a-c4d8-4fd9-aaf0-3d4503bbce26
title: WM_CANCELMODE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae26cef4919ed93bb2a1c60376ab450560cd2142cef7b3040032f791c45ab09f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849304"
---
# <a name="wm_cancelmode-message"></a>Mensaje \_ CANCELMODE de WM

Se envía para cancelar determinados modos, como la captura del mouse. Por ejemplo, el sistema envía este mensaje a la ventana activa cuando se muestra un cuadro de diálogo o un cuadro de mensaje. Algunas funciones también envían este mensaje explícitamente a la ventana especificada, independientemente de si es la ventana activa. Por ejemplo, la [**función EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) envía este mensaje al deshabilitar la ventana especificada.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

## <a name="remarks"></a>Comentarios

Cuando se envía el mensaje **\_ CANCELMODE** de WM, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) cancela el procesamiento interno de la entrada de la barra de desplazamiento estándar, cancela el procesamiento de menú interno y libera la captura del mouse.

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

[**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

[**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
