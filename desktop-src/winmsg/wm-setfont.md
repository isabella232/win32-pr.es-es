---
description: Establece la fuente que un control va a utilizar al dibujar texto.
ms.assetid: 7db6b8af-dbec-4c29-8bf7-d7e95d9813c3
title: Mensaje de WM_SETFONT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fc334e6b8c937759555c471f00ec56254a629c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104002024"
---
# <a name="wm_setfont-message"></a>Mensaje de WM \_ SETFONT

Establece la fuente que un control va a utilizar al dibujar texto.


```C++
#define WM_SETFONT                      0x0030
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la fuente (**HFONT**). Si este parámetro es **null**, el control utiliza la fuente predeterminada del sistema para dibujar el texto.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden inferior de *lParam* especifica si el control debe volver a dibujarse inmediatamente después de establecer la fuente. Si este parámetro es **true**, el control vuelve a dibujarse.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El mensaje de **WM \_ SETFONT** se aplica a todos los controles, no solo a los de los cuadros de diálogo.

El mejor momento para que el propietario de un control de cuadro de diálogo establezca la fuente del control es cuando recibe el mensaje de [**\_ INITDIALOG de WM**](../dlgbox/wm-initdialog.md) . La aplicación debe llamar a la función [**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) para eliminar la fuente cuando ya no se necesite; por ejemplo, después de que destruya el control.

El tamaño del control no cambia como resultado de recibir este mensaje. Para evitar el recorte de texto que no cabe dentro de los límites del control, la aplicación debe corregir el tamaño de la ventana de control antes de establecer la fuente.

Cuando un cuadro de diálogo utiliza el estilo de [DS \_ SetFont](../dlgbox/about-dialog-boxes.md) para establecer el texto en sus controles, el sistema envía el mensaje de **WM \_ SetFont** al procedimiento del cuadro de diálogo antes de crear los controles. Una aplicación puede crear un cuadro de diálogo que contenga el estilo de DS \_ SETFONT mediante una llamada a cualquiera de las siguientes funciones:

-   [**CreateDialogIndirect**](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
-   [**CreateDialogIndirectParam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
-   [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
-   [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)

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

[**GETFONT de WM \_**](wm-getfont.md)
</dt> <dt>

[**INITDIALOG de WM \_**](../dlgbox/wm-initdialog.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject)
</dt> </dl>

 

 
