---
title: Mensaje de WM_ADSPROP_NOTIFY_EXIT (Adsprop. h)
description: Una Active Directory extensión de la hoja de propiedades envía el mensaje de salida de notificación de WM \_ ADSPROP \_ \_ al objeto de notificación cuando ya no se necesita el objeto de notificación.
ms.assetid: b0f58c73-8953-412d-b801-bf34967fe0b4
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_EXIT Active Directory de mensaje
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
ms.openlocfilehash: 32d74ef4b7dfa525cfb77a6d89499837cbfac8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996936"
---
# <a name="wm_adsprop_notify_exit-message"></a>\_Mensaje de \_ salida de notificación de ADSPROP de WM \_

Una Active Directory extensión de la hoja de propiedades envía el mensaje de **\_ \_ \_ salida** de notificación de WM ADSPROP al objeto de notificación cuando ya no se necesita el objeto de notificación.


```C++
WM_ADSPROP_NOTIFY_EXIT

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador* 
</dt> <dd>

Identificador del objeto de notificación. Para obtener este identificador, llame a [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

No se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

El objeto de notificación se eliminará en respuesta a este mensaje. Cuando se envía este mensaje, el identificador del objeto de notificación debe considerarse no válido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Adsprop. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[Mensajes en Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





