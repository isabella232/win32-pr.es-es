---
title: Código de notificación de CDN_FILEOK (commdlg. h)
description: Enviado por un cuadro de diálogo abrir o guardar como del explorador cuando el usuario especifica un nombre de archivo y hace clic en el botón Aceptar.
ms.assetid: 7f3de96f-68d8-4f40-b74f-304835f9def2
keywords:
- CDN_FILEOK cuadros de diálogo código de notificación
topic_type:
- apiref
api_name:
- CDN_FILEOK
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5aef63d531b603c94369936374bc10531639254
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676909"
---
# <a name="cdn_fileok-notification-code"></a>\_Código de notificación FILEOK de CDN

Enviado por un cuadro de diálogo **abrir** o **Guardar como** del explorador cuando el usuario especifica un nombre de archivo y hace clic en el botón **Aceptar** .

El procedimiento de enlace de [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje de [**\_ notificación de WM**](../controls/wm-notify.md) .


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FILEOK              (CDN_FIRST - 0x0005)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**imnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .

La estructura [**imnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) contiene una estructura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) cuyo miembro de **código** indica el mensaje de notificación FILEOK de la **red CDN \_** .

La estructura [**imnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) también contiene un puntero a una estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) cuyo miembro **lpstrFile** especifica la dirección del nombre de archivo seleccionado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el procedimiento de enlace devuelve cero, el cuadro de diálogo acepta el nombre de archivo especificado y se cierra.

Para rechazar el nombre de archivo especificado y forzar que el cuadro de diálogo permanezca abierto, devuelve un valor distinto de cero del procedimiento de enlace y llama a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para establecer un valor **\_ MSGRESULT de DWL** distinto de cero.

## <a name="remarks"></a>Observaciones

El sistema envía esta notificación solo si el cuadro de diálogo se creó con el valor del **\_ Explorador OFN** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[**No NOTIFICAr**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

**Vista**
</dt> <dt>

[Biblioteca de cuadros de diálogo comunes](common-dialog-box-library.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**\_notificaciones de WM**](../controls/wm-notify.md)
</dt> </dl>

 

