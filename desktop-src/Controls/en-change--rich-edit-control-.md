---
title: EN_CHANGE (edición enriquecte) de código de notificación (Winuser.h)
description: Notifica a la ventana host de un control rich edit sin ventana que se ha producido un cambio. Un control de edición enriquecido envía este código de notificación en forma de mensaje WM \_ NOTIFY.
ms.assetid: 97C0D9F1-7D4E-409D-A4F6-E645475A8EEF
keywords:
- EN_CHANGE (edición enriquecte) de código de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_CHANGE (rich edit control)
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea615234aba881b2a8938b8e502b36acfa565fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062040"
---
# <a name="en_change-rich-edit-notification-code"></a>Código de notificación EN \_ CHANGE (rich edit)

Notifica a la ventana host de un control rich edit sin ventana que se ha producido un cambio. Un control de edición enriquecido envía este código de notificación en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_CHANGE

    penChangeNotify = (CHANGENOTIFY *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Estructura [**CHANGENOTIFY**](/windows/desktop/api/Textserv/ns-textserv-changenotify) que especifica el cambio realizado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este código de notificación no devuelve un valor.

## <a name="remarks"></a>Observaciones

Para recibir códigos de notificación EN \_ CHANGE, especifique [**ENM \_ CHANGE**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**\_ EM SETEVENTMASK.**](em-seteventmask.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify)
</dt> </dl>

 

 





