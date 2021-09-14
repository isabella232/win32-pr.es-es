---
title: WM_NCMOUSELEAVE mensaje (Winuser.h)
description: Se publica en una ventana cuando el cursor sale del área no cliente de la ventana especificada en una llamada anterior a TrackMouseEvent.
ms.assetid: b3ada6db-93ce-45d7-b408-d08692328aeb
keywords:
- WM_NCMOUSELEAVE entrada de teclado y mouse
topic_type:
- apiref
api_name:
- WM_NCMOUSELEAVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cf7f9d0931c2623d2e92010abfca96f391107b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360090"
---
# <a name="wm_ncmouseleave-message"></a>Mensaje \_ DE WM NCMOUSELEAVE

Se publica en una ventana cuando el cursor sale del área no cliente de la ventana especificada en una llamada anterior a [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCMOUSELEAVE                 0x02A2
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa y debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa y debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Todo el seguimiento solicitado [**por TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) se cancela cuando se genera este mensaje. La aplicación debe llamar a **TrackMouseEvent** cuando el mouse vuelva a entrar en su ventana si requiere un seguimiento adicional del comportamiento del mouse.

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

[**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[**WM \_ MOUSELEAVE**](wm-mouseleave.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Entrada del mouse](mouse-input.md)
</dt> </dl>

 

