---
title: WM_ADSPROP_NOTIFY_EXIT mensaje (Adsprop.h)
description: Una Active Directory de hoja de propiedades envía el mensaje WM ADSPROP NOTIFY EXIT al objeto de notificación cuando el objeto de notificación \_ \_ ya no es \_ necesario.
ms.assetid: b0f58c73-8953-412d-b801-bf34967fe0b4
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_EXIT mensaje Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_EXIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e144bb0b24112cabe1a806d4c746aac07708443665c0f457df8756be36d80b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181969"
---
# <a name="wm_adsprop_notify_exit-message"></a>Mensaje \_ DE SALIDA DE WM ADSPROP \_ NOTIFY \_

Una Active Directory de hoja de propiedades envía el mensaje **\_ WM ADSPROP NOTIFY \_ \_ EXIT** al objeto de notificación cuando el objeto de notificación ya no es necesario.


```C++
WM_ADSPROP_NOTIFY_EXIT

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Identificador del objeto de notificación. Para obtener este identificador, llame [**a ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

No se usa.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no tiene ningún valor devuelto.

## <a name="remarks"></a>Comentarios

El objeto de notificación se eliminará en respuesta a este mensaje. Cuando se ha enviado este mensaje, el identificador del objeto de notificación debe considerarse no válido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                       |
| Header<br/>                   | <dl> <dt>Adsprop.h</dt> </dl> |



## <a name="see-also"></a>Consulta también

<dl> <dt>

[**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[Mensajes en Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





