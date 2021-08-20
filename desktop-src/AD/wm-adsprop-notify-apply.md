---
title: WM_ADSPROP_NOTIFY_APPLY mensaje (Adsprop.h)
description: Una Active Directory hoja de propiedades del servicio de directorio envía el mensaje WM ADSPROP NOTIFY APPLY al objeto de notificación si el controlador PSN APPLY de la página de \_ \_ propiedades se realiza \_ \_ correctamente.
ms.assetid: 3536054b-83ee-4cfa-ab54-c0af3a46289e
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_APPLY mensaje Active Directory
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
ms.openlocfilehash: 6cc130a83aa77021e0be512d9b2ad27914b4c6be382c0290e082e1fbd67b8b22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024303"
---
# <a name="wm_adsprop_notify_apply-message"></a>Mensaje \_ DE WM ADSPROP NOTIFY \_ \_ APPLY

Una Active Directory hoja de propiedades del servicio de directorio envía el mensaje **WM \_ ADSPROP \_ NOTIFY \_ APPLY** al objeto de notificación si el controlador PSN APPLY de la página de \_ propiedades se realiza correctamente.


```C++
WM_ADSPROP_NOTIFY_APPLY

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

Al agregar páginas al complemento MMC de Active Directory Manager Active Directory, las hojas de propiedades de MMC crean los objetos de notificación mediante una llamada a la función [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) y, a continuación, pasan el identificador de objeto de notificación a cada página de propiedades.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                       |
| Header<br/>                   | <dl> <dt>Adsprop.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[Mensajes en Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





