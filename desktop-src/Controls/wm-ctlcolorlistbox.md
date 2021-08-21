---
title: WM_CTLCOLORLISTBOX mensaje (Winuser.h)
description: Se envía a la ventana primaria de un cuadro de lista antes de que el sistema dibuje el cuadro de lista. Al responder a este mensaje, la ventana primaria puede establecer los colores de texto y fondo del cuadro de lista mediante el identificador de contexto del dispositivo de presentación especificado.
ms.assetid: e128e77f-e966-44c4-9f0e-efcf421b6c82
keywords:
- WM_CTLCOLORLISTBOX controles de Windows mensaje
topic_type:
- apiref
api_name:
- WM_CTLCOLORLISTBOX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1713c7251dfe837d5796b708fa5b77f0aa5e372c031c251199cb871dbd7c5608
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077669"
---
# <a name="wm_ctlcolorlistbox-message"></a>Mensaje \_ CTLCOLORLISTBOX de WM

Se envía a la ventana primaria de un cuadro de lista antes de que el sistema dibuje el cuadro de lista. Al responder a este mensaje, la ventana primaria puede establecer los colores de texto y fondo del cuadro de lista mediante el identificador de contexto del dispositivo de presentación especificado.


```C++
WM_CTLCOLORLISTBOX

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del contexto del dispositivo para el cuadro de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del cuadro de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver un identificador a un pincel. El sistema usa el pincel para pintar el fondo del cuadro de lista.

## <a name="remarks"></a>Comentarios

De forma predeterminada, [**la función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) selecciona los colores predeterminados del sistema para el cuadro de lista.

El **mensaje \_ WM CTLCOLORLISTBOX** nunca se envía entre subprocesos. Solo se envía dentro de un subproceso.

Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado en **int \_ PTR** y devolver el valor directamente. Si el procedimiento del cuadro de diálogo **devuelve FALSE,** se realiza el control de mensajes predeterminado. Se omite el valor **\_ MSGRESULT** de DWL establecido por la función [**SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Otros recursos**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SeleccionarPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

