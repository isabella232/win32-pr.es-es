---
title: Código de notificación de EN_MSGFILTER (RichEdit. h)
description: Notifica a la ventana primaria de un control Rich Edit de un evento de teclado o del mouse en el control. Un control Rich Edit envía este código de notificación en forma de mensaje de \_ notificación de WM.
ms.assetid: 96cf0047-baae-46cd-82e8-ab6f3f353260
keywords:
- EN_MSGFILTER controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_MSGFILTER
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40ddb3e9b1d5314e2e981b00f0e0ef8e22974242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150369"
---
# <a name="en_msgfilter-notification-code"></a>\_Código de notificación en MSGFILTER

Notifica a la ventana primaria de un control Rich Edit de un evento de teclado o del mouse en el control. Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
EN_MSGFILTER

    pMsgFilter = (MSGFILTER *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Estructura [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) que contiene información sobre el mensaje del mouse o del teclado. Si la ventana primaria modifica esta estructura y devuelve un valor distinto de cero, el mensaje modificado se procesa en lugar del original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si el control debe procesar el evento de teclado o del mouse.

Devuelve un valor distinto de cero si el control debe omitir el evento de teclado o del mouse.

## <a name="remarks"></a>Observaciones

Para recibir \_ los códigos de notificación en MSGFILTER para los eventos, especifique una o varias de las siguientes marcas en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .



| Marca                                                                             | Significado                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------|
| [**ENM \_ KEYEVENTS**](rich-edit-control-event-mask-flags.md)       | Para recibir códigos de notificación para los eventos de teclado.     |
| [**ENM \_ MOUSEEVENTS**](rich-edit-control-event-mask-flags.md)   | Para recibir códigos de notificación para los eventos del mouse.        |
| [**ENM \_ SCROLLEVENTS**](rich-edit-control-event-mask-flags.md) | Para recibir los códigos de notificación de un evento de rueda del mouse. |



 

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

[**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter)
</dt> <dt>

[**\_notificaciones de WM**](wm-notify.md)
</dt> </dl>

 

 





