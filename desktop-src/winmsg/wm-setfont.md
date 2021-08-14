---
description: Establece la fuente que va a usar un control al dibujar texto.
ms.assetid: 7db6b8af-dbec-4c29-8bf7-d7e95d9813c3
title: WM_SETFONT mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811bee30237a64955197588f87866d4a64af89edc640762ec16333839aee9220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199941"
---
# <a name="wm_setfont-message"></a>Mensaje \_ SETFONT de WM

Establece la fuente que va a usar un control al dibujar texto.


```C++
#define WM_SETFONT                      0x0030
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la fuente (**HFONT**). Si este parámetro es **NULL,** el control usa la fuente predeterminada del sistema para dibujar texto.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden bajo *de lParam* especifica si el control se debe volver a dibujar inmediatamente después de establecer la fuente. Si este parámetro es **TRUE,** el control se vuelve a dibujar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Comentarios

El **mensaje \_ SETFONT de WM** se aplica a todos los controles, no solo a los de los cuadros de diálogo.

El mejor momento para que el propietario de un control de cuadro de diálogo establezca la fuente del control es cuando recibe el mensaje [**WM \_ INITDIALOG.**](../dlgbox/wm-initdialog.md) La aplicación debe llamar a [**la función DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) para eliminar la fuente cuando ya no sea necesaria; por ejemplo, después de destruir el control.

El tamaño del control no cambia como resultado de recibir este mensaje. Para evitar el recorte de texto que no cabe dentro de los límites del control, la aplicación debe corregir el tamaño de la ventana de control antes de establecer la fuente.

Cuando un cuadro de diálogo usa el estilo [ \_ SETFONT](../dlgbox/about-dialog-boxes.md) de DS para establecer el texto en sus controles, el sistema envía el mensaje **WM \_ SETFONT** al procedimiento del cuadro de diálogo antes de crear los controles. Una aplicación puede crear un cuadro de diálogo que contenga el estilo SETFONT de DS llamando a \_ cualquiera de las funciones siguientes:

-   [**CreateDialogIndirect**](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
-   [**CreateDialogIndirectParam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
-   [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
-   [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)

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

[**CreateDialogIndirect**](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[**CreateDialogIndirectParam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DLGTEMPLATE**](/windows/win32/api/winuser/ns-winuser-dlgtemplate)
</dt> <dt>

[**MAKELPARAM**](/windows/win32/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**WM \_ GETFONT**](wm-getfont.md)
</dt> <dt>

[**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject)
</dt> </dl>

 

 
