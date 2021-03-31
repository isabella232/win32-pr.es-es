---
title: Código de notificación de CDN_SELCHANGE (commdlg. h)
description: Enviado por un cuadro de diálogo para abrir o guardar como del explorador cuando la selección cambia en el cuadro de lista que muestra el contenido de la carpeta o el directorio abiertos actualmente.
ms.assetid: e622babf-7024-45c5-a8db-f80896f69140
keywords:
- CDN_SELCHANGE cuadros de diálogo código de notificación
topic_type:
- apiref
api_name:
- CDN_SELCHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e2f0f5a7860c7d729340a84bd80bc4e5713c733
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490570"
---
# <a name="cdn_selchange-notification-code"></a>\_Código de notificación SELCHANGE de CDN

\[A partir de Windows Vista, los cuadros de diálogo **abrir** y **Guardar como** común se han sustituido por el [cuadro de diálogo de elementos comunes](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)). Se recomienda usar la API de cuadros de diálogo de elementos comunes en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo comunes.\]

Enviado por un cuadro de diálogo para **abrir** o **Guardar como** del explorador cuando la selección cambia en el cuadro de lista que muestra el contenido de la carpeta o el directorio abiertos actualmente.

El procedimiento de enlace de [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje de [**\_ notificación de WM**](../controls/wm-notify.md) .


```C++
#define CDN_SELCHANGE           (CDN_FIRST - 0x0001)
#define CDN_FIRST               (0U-601U)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**imnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) . La estructura **imnotify** contiene una estructura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) cuyo miembro de **código** indica el mensaje de notificación SELCHANGE de la **red CDN \_** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

El sistema envía esta notificación solo si el cuadro de diálogo se creó con el valor del **\_ Explorador OFN** .

Para obtener el nombre del archivo o carpeta recién seleccionado, el procedimiento de enlace puede enviar el mensaje [**CDM \_ GETFILEPATH**](cdm-getfilepath.md) o [**CDM \_ GETSPEC**](cdm-getspec.md) al cuadro de diálogo.

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

[**CDM \_ GETFILEPATH**](cdm-getfilepath.md)
</dt> <dt>

[**CDM \_ GETSPEC**](cdm-getspec.md)
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[**No NOTIFICAr**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

**Vista**
</dt> <dt>

[Biblioteca de cuadros de diálogo comunes](common-dialog-box-library.md)
</dt> </dl>

 

