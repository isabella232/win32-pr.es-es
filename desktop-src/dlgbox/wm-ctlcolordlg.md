---
title: WM_CTLCOLORDLG mensaje (Winuser.h)
description: Se envía a un cuadro de diálogo antes de que el sistema dibuje el cuadro de diálogo. Al responder a este mensaje, el cuadro de diálogo puede establecer sus colores de texto y fondo mediante el identificador de contexto del dispositivo de presentación especificado.
ms.assetid: 5b90ab3f-b751-486f-a0fa-33f791c31a26
keywords:
- WM_CTLCOLORDLG cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_CTLCOLORDLG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5b7ab11bbb2cfd402888f930d5bcf2afa08b7ba83f74252fb3e443fd9e9309a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503418"
---
# <a name="wm_ctlcolordlg-message"></a>Mensaje \_ WM CTLCOLORDLG

Se envía a un cuadro de diálogo antes de que el sistema dibuje el cuadro de diálogo. Al responder a este mensaje, el cuadro de diálogo puede establecer sus colores de texto y fondo mediante el identificador de contexto del dispositivo de presentación especificado.


```C++
#define WM_CTLCOLORDLG                  0x0136
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del contexto del dispositivo para el cuadro de diálogo.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del cuadro de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver un identificador a un pincel. El sistema usa el pincel para pintar el fondo del cuadro de diálogo.

## <a name="remarks"></a>Comentarios

De forma predeterminada, [**la función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) selecciona los colores predeterminados del sistema para el cuadro de diálogo.

El sistema no destruye automáticamente el pincel devuelto. Es responsabilidad de la aplicación destruir el pincel cuando ya no se necesita.

El **mensaje \_ WM CTLCOLORDLG** nunca se envía entre subprocesos. Solo se envía dentro de un subproceso.

Tenga en cuenta que el mensaje **\_ WM CTLCOLORDLG** se envía al propio cuadro de diálogo; todos los demás mensajes **wm \_ CTLCOLOR \*** se envían al propietario del control.

Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado en **int \_ PTR** y devolver el valor directamente. Si el procedimiento del cuadro de diálogo **devuelve FALSE**, se realiza el control de mensajes predeterminado. Se **omite el valor \_ MSGRESULT** de DWL establecido por la función [**SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)

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

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Cuadros de diálogo](dialog-boxes.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SeleccionePalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

