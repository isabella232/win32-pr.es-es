---
title: Mensaje de WM_ADSPROP_NOTIFY_APPLY (Adsprop. h)
description: Una extensión de la hoja de propiedades del servicio de directorio de Active Directory envía el mensaje de notificación de ADSPROP de WM \_ \_ \_ al objeto de notificación si la página de propiedades PSN el \_ controlador de aplicación se realiza correctamente.
ms.assetid: 3536054b-83ee-4cfa-ab54-c0af3a46289e
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_APPLY Active Directory de mensaje
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_APPLY
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ccd5bb95e3f092634d54ba0534e81ded6701bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658347"
---
# <a name="wm_adsprop_notify_apply-message"></a>\_Mensaje de \_ solicitud de notificación de ADSPROP de WM \_

Una extensión de la hoja de propiedades del servicio de directorio de Active Directory envía el mensaje de notificación de **ADSPROP de WM \_ \_ \_** al objeto de notificación si la página de propiedades PSN el \_ controlador de aplicación se realiza correctamente.


```C++
WM_ADSPROP_NOTIFY_APPLY

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

Al agregar páginas al complemento MMC de Active Directory Manager, Active Directory hojas de propiedades de MMC crean los objetos de notificación mediante una llamada a la función [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) y, a continuación, pasa el identificador del objeto de notificación a cada página de propiedades.

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

 

 





