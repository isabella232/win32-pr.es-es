---
title: WM_ADSPROP_NOTIFY_PAGEINIT mensaje (Adsprop.h)
description: Una Active Directory de hoja de propiedades llama a ADsPropGetInitInfo para obtener datos sobre el objeto de directorio al que se aplica la extensión de hoja de propiedades.
ms.assetid: 473c5a75-d0d9-4d12-b855-63683e8cdf3f
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_PAGEINIT mensaje Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEINIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcad6ed359edf195b2355920b08d6010597f33dbc0f4e3b1e4c2438c3841ca47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024213"
---
# <a name="wm_adsprop_notify_pageinit-message"></a>Mensaje \_ \_ \_ PAGEINIT de WM ADSPROP NOTIFY

Una Active Directory de hoja de propiedades llama [**a ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) para obtener datos sobre el objeto de directorio al que se aplica la extensión de hoja de propiedades. La **función ADsPropGetInitInfo** envía el mensaje **\_ \_ \_ PAGEINIT DE WM ADSPROP NOTIFY** al objeto de notificación para lograr este resultado.


```C++
WM_ADSPROP_NOTIFY_PAGEINIT

    WPARAM wParam
    LPARAM pADsPropInitParams
    
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Identificador del objeto de notificación. Este es el *parámetro hNotifyObject* obtenido por una llamada a [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

No se usa.

</dd> <dt>

*pADsPropInitParams* 
</dt> <dd>

Puntero a una [**estructura ADSPROPIICIOPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) que recibe la información del objeto de directorio. Este es el *parámetro pInitParams* pasado [**a ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no tiene ningún valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                       |
| Header<br/>                   | <dl> <dt>Adsprop.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mensajes en Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> <dt>

[**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo)
</dt> <dt>

[**ADSPROPIICIOPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams)
</dt> </dl>

 

 





