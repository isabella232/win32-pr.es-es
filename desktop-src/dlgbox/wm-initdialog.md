---
title: WM_INITDIALOG mensaje (Winuser.h)
description: Se envía al procedimiento del cuadro de diálogo inmediatamente antes de que se muestre un cuadro de diálogo. Los procedimientos de cuadro de diálogo suelen usar este mensaje para inicializar controles y llevar a cabo cualquier otra tarea de inicialización que afecte a la apariencia del cuadro de diálogo.
ms.assetid: bc4f4718-1dab-48db-ae3b-5a81a7be2644
keywords:
- WM_INITDIALOG de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_INITDIALOG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e272ac93514fb60069a9217c3100318f95b1e9a8c77d9e75af56e2e7fbfbf66e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117775"
---
# <a name="wm_initdialog-message"></a>Mensaje \_ WM INITDIALOG

Se envía al procedimiento del cuadro de diálogo inmediatamente antes de que se muestre un cuadro de diálogo. Los procedimientos de cuadro de diálogo suelen usar este mensaje para inicializar controles y llevar a cabo cualquier otra tarea de inicialización que afecte a la apariencia del cuadro de diálogo.


```C++
#define WM_INITDIALOG                   0x0110
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del control para recibir el foco de teclado predeterminado. El sistema asigna el foco de teclado predeterminado solo si el procedimiento del cuadro de diálogo devuelve **TRUE**.

</dd> <dt>

*lParam* 
</dt> <dd>

Datos de inicialización adicionales. Estos datos se pasan al sistema como el parámetro *lParam* en una llamada a la función [**CreateDialogIndirectParam,**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama) [**CreateDialogParam,**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama) [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)o [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) utilizada para crear el cuadro de diálogo. Para las hojas de propiedades, este parámetro es un puntero a la [**estructura PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) utilizada para crear la página. Este parámetro es cero si se usa cualquier otra función de creación de cuadro de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El procedimiento del cuadro de diálogo debe devolver **TRUE** para dirigir el sistema para establecer el foco del teclado en el control especificado por *wParam*. De lo contrario, debe devolver **FALSE para** evitar que el sistema ajuste el foco de teclado predeterminado.

El procedimiento del cuadro de diálogo debe devolver el valor directamente. Se omite el valor **\_ MSGRESULT** de DWL establecido por la función [**SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)

## <a name="remarks"></a>Comentarios

El control para recibir el foco de teclado predeterminado siempre es el primer control del cuadro de diálogo que está visible, no deshabilitado, y que tiene el estilo **\_ TABSTOP de WS.** Cuando el procedimiento del cuadro de diálogo **devuelve TRUE,** el sistema comprueba el control para asegurarse de que el procedimiento no lo ha deshabilitado. Si se ha deshabilitado, el sistema establece el foco del teclado en el siguiente control que está visible, no deshabilitado, y tiene **el \_ control TABSTOP de WS.**

Una aplicación solo puede devolver **FALSE** si ha establecido el foco del teclado en uno de los controles del cuadro de diálogo.

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

[**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)
</dt> <dt>

[**Setfocus**](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Cuadros de diálogo](dialog-boxes.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2)
</dt> </dl>

 

