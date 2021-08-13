---
title: CDN_FOLDERCHANGE de notificación (Commdlg.h)
description: Enviado por un cuadro de diálogo Abrir o Guardar como de estilo explorador cuando se abre una nueva carpeta.
ms.assetid: 864ab80d-cd99-4dd6-8aff-49beed246e53
keywords:
- CDN_FOLDERCHANGE de diálogo del código de notificación
topic_type:
- apiref
api_name:
- CDN_FOLDERCHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 085d7d0131608ce70a1e023130159b270a679c968a548062645b32cd5cd10204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786145"
---
# <a name="cdn_folderchange-notification-code"></a>\_CDN Código de notificación FOLDERCHANGE

\[A partir Windows Vista,  los  cuadros de diálogo Abrir y Guardar como comunes se han reemplazado por el [cuadro de diálogo Elemento común](../shell/common-file-dialog.md). Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca común de cuadros de diálogo.\]

Enviado por un cuadro de **diálogo** Abrir o Guardar **como** de estilo explorador cuando se abre una nueva carpeta.

El [*procedimiento de enlace OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje WM [**\_ NOTIFY.**](../controls/wm-notify.md)


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FOLDERCHANGE        (CDN_FIRST - 0x0002)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) La **estructura OFNOTIFY contiene** una  estructura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) cuyo miembro de código indica el **CDN notificación \_ FOLDERCHANGE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

El sistema envía esta notificación solo si el cuadro de diálogo se creó con el **valor OFN \_ EXPLORER.**

Para obtener la ruta de acceso de la carpeta recién abierta, el procedimiento de enlace puede enviar el mensaje [**\_ GETFOLDERPATH**](cdm-getfolderpath.md) de CDM al cuadro de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**GETFOLDERPATH de CDM \_**](cdm-getfolderpath.md)
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Biblioteca común de cuadros de diálogo](common-dialog-box-library.md)
</dt> </dl>

