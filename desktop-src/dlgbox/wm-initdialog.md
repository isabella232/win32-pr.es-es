---
title: Mensaje de WM_INITDIALOG (Winuser. h)
description: Se envía al procedimiento del cuadro de diálogo inmediatamente antes de que se muestre un cuadro de diálogo. Los procedimientos del cuadro de diálogo suelen usar este mensaje para inicializar controles y realizar cualquier otra tarea de inicialización que afecte a la apariencia del cuadro de diálogo.
ms.assetid: bc4f4718-1dab-48db-ae3b-5a81a7be2644
keywords:
- WM_INITDIALOG cuadros de diálogo de mensaje
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
ms.openlocfilehash: 64646075bc3d5c90076d6c1ca0d61f80111c90ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105720226"
---
# <a name="wm_initdialog-message"></a>Mensaje de INITDIALOG de WM \_

Se envía al procedimiento del cuadro de diálogo inmediatamente antes de que se muestre un cuadro de diálogo. Los procedimientos del cuadro de diálogo suelen usar este mensaje para inicializar controles y realizar cualquier otra tarea de inicialización que afecte a la apariencia del cuadro de diálogo.


```C++
#define WM_INITDIALOG                   0x0110
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del control que va a recibir el foco de teclado predeterminado. El sistema asigna el foco de teclado predeterminado solo si el procedimiento de cuadro de diálogo devuelve **true**.

</dd> <dt>

*lParam* 
</dt> <dd>

Datos de inicialización adicionales. Estos datos se pasan al sistema como el parámetro *lParam* en una llamada a la función [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)o [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) utilizada para crear el cuadro de diálogo. En las hojas de propiedades, este parámetro es un puntero a la estructura [**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) utilizada para crear la página. Este parámetro es cero si se utiliza cualquier otra función de creación de cuadros de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El procedimiento de cuadro de diálogo debe devolver **true** para indicar al sistema que establezca el foco de teclado en el control especificado por *wParam*. De lo contrario, debería devolver **false** para evitar que el sistema establezca el foco de teclado predeterminado.

El procedimiento del cuadro de diálogo debe devolver el valor directamente. Se omite el valor de **DWL \_ MSGRESULT** establecido por la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .

## <a name="remarks"></a>Observaciones

El control para recibir el foco de teclado predeterminado siempre es el primer control del cuadro de diálogo que es visible, no deshabilitado y que tiene el estilo **WS \_ TABSTOP** . Cuando el procedimiento del cuadro de diálogo devuelve **true**, el sistema comprueba el control para asegurarse de que el procedimiento no lo ha deshabilitado. Si se ha deshabilitado, el sistema establece el foco de teclado en el siguiente control que es visible, no deshabilitado y que tiene el **WS \_ TABSTOP**.

Una aplicación solo puede devolver **false** si ha establecido el foco de teclado en uno de los controles del cuadro de diálogo.

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

[**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)
</dt> <dt>

[**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

**Vista**
</dt> <dt>

[Cuadros de diálogo](dialog-boxes.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2)
</dt> </dl>

 

