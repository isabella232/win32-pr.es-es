---
title: Código de notificación de EN_REQUESTRESIZE (RichEdit. h)
description: Notifica a la ventana primaria de un control Rich Edit que el contenido del control es menor o mayor que el tamaño de la ventana del control. Un control Rich Edit envía este código de notificación en forma de mensaje de \_ notificación de WM.
ms.assetid: 708c23b1-7b81-46f1-9595-46230693855d
keywords:
- EN_REQUESTRESIZE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60214d8902297eb7cd77ded481b0604929e7adb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150558"
---
# <a name="en_requestresize-notification-code"></a>\_Código de notificación en REQUESTRESIZE

Notifica a la ventana primaria de un control Rich Edit que el contenido del control es menor o mayor que el tamaño de la ventana del control. Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
EN_REQUESTRESIZE

    pReqResize = (REQRESIZE *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Una estructura [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) que recibe el tamaño solicitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este código de notificación no devuelve un valor.

## <a name="remarks"></a>Observaciones

Para admitir el comportamiento sin límite de un control Rich Edit, la ventana primaria debe cambiar el tamaño del control cuando recibe este código de notificación.

Para recibir los \_ códigos de notificación en REQUESTRESIZE, especifique [**ENM \_ REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .

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

[**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize)
</dt> <dt>

[**\_notificaciones de WM**](wm-notify.md)
</dt> </dl>

 

 





