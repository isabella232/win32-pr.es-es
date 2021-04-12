---
title: Mensaje de WM_MOUSELEAVE (Winuser. h)
description: Se envía a una ventana cuando el cursor abandona el área cliente de la ventana especificada en una llamada anterior a TrackMouseEvent.
ms.assetid: b23d24ff-531a-4b6d-8848-f82ac5568995
keywords:
- Entrada de mouse y teclado de mensaje de WM_MOUSELEAVE
topic_type:
- apiref
api_name:
- WM_MOUSELEAVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc96022e94df7f518b21b1c9a46895fc9204b08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490036"
---
# <a name="wm_mouseleave-message"></a>Mensaje de WM \_ MOUSELEAVE

Se envía a una ventana cuando el cursor abandona el área cliente de la ventana especificada en una llamada anterior a [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_MOUSELEAVE                   0x02A3
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza y debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza y debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Todo el seguimiento solicitado por [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) se cancela cuando se genera este mensaje. La aplicación debe llamar a **TrackMouseEvent** cuando el mouse vuelva a entrar en su ventana si requiere un seguimiento adicional del comportamiento de desplazamiento del mouse.

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

[**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[**NCMOUSELEAVE de WM \_**](wm-ncmouseleave.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Entrada del mouse](mouse-input.md)
</dt> </dl>

 

