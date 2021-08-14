---
title: WM_ADSPROP_NOTIFY_PAGEHWND mensaje (Adsprop.h)
description: Una Active Directory hoja de propiedades del servicio de directorio llama a ADsPropSetHwnd para informar al objeto de notificación del identificador de ventana de la página de propiedades.
ms.assetid: eb8bf525-cd7f-44d0-a0f9-43178a29c443
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_PAGEHWND mensaje Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEHWND
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2835b4e0ff878b4c747f8c34b983beb3d66c550008a82ecadb2e5a23667abc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181736"
---
# <a name="wm_adsprop_notify_pagehwnd-message"></a>MENSAJE \_ DE NOTIFICACIÓN DE ADSPROP DE WM \_ \_ PAGEHWND

Una Active Directory hoja de propiedades del servicio de directorio llama [**a ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) para informar al objeto de notificación del identificador de la ventana de la página de propiedades. La **función ADsPropSetHwnd** envía el mensaje **\_ \_ \_ PAGEHWND DE WM ADSPROP NOTIFY** al objeto de notificación, que informa al objeto de notificación del identificador de ventana de la página de propiedades.


```C++
WM_ADSPROP_NOTIFY_PAGEHWND

    WPARAM hPage
    LPARAM ptzTitle
    
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hNotifyObj* 
</dt> <dd>

Identificador del objeto de notificación. Para obtener este identificador, llame [**a ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*hPage* 
</dt> <dd>

Identificador de ventana de la página de propiedades.

</dd> <dt>

*ptzTitle* 
</dt> <dd>

Puntero a un búfer **WCHAR** terminado en NULL que contiene el título de la página de propiedades.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no tiene ningún valor devuelto.

## <a name="remarks"></a>Comentarios

Una Active Directory de hoja de propiedades normalmente llama a la función [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) mientras se procesa [**el mensaje \_ INITDIALOG de WM.**](../dlgbox/wm-initdialog.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                       |
| Header<br/>                   | <dl> <dt>Adsprop.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Mensajes en Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> <dt>

[**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd)
</dt> <dt>

[**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md)
</dt> </dl>

 

