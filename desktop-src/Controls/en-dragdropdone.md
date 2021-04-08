---
title: Código de notificación de EN_DRAGDROPDONE (RichEdit. h)
description: Notifica a la ventana primaria de un control Rich Edit que se ha completado la operación de arrastrar y colocar. Un control Rich Edit envía este código de notificación en forma de mensaje de \_ notificación de WM.
ms.assetid: 3c8b95cc-86ef-4aec-b551-11dca50ea5c5
keywords:
- EN_DRAGDROPDONE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_DRAGDROPDONE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a10b6718122791bcc862866fbaf17ed43e8bfd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995979"
---
# <a name="en_dragdropdone-notification-code"></a>\_Código de notificación en DRAGDROPDONE

Notifica a la ventana primaria de un control Rich Edit que se ha completado la operación de arrastrar y colocar. Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
EN_DRAGDROPDONE

    pnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este código de notificación no devuelve un valor.

## <a name="remarks"></a>Observaciones

Para recibir un \_ código de notificación en DRAGDROPDONE, especifique la marca [**\_ DRAGDROPDONE de ENM**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**una \_ SETEVENTMASK**](em-seteventmask.md)
</dt> </dl>

 

 





