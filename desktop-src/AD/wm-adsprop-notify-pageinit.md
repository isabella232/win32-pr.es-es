---
title: Mensaje de WM_ADSPROP_NOTIFY_PAGEINIT (Adsprop. h)
description: Una Active Directory extensión de la hoja de propiedades llama a ADsPropGetInitInfo para obtener datos sobre el objeto de directorio al que se aplica la extensión de la hoja de propiedades.
ms.assetid: 473c5a75-d0d9-4d12-b855-63683e8cdf3f
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_PAGEINIT Active Directory de mensaje
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
ms.openlocfilehash: a2718ee30cdbecec7c4e0954636aa14c75f13027
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533987"
---
# <a name="wm_adsprop_notify_pageinit-message"></a>\_Mensaje de \_ PAGEINIT de notificación de ADSPROP de WM \_

Una Active Directory extensión de la hoja de propiedades llama a [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) para obtener datos sobre el objeto de directorio al que se aplica la extensión de la hoja de propiedades. La función **ADsPropGetInitInfo** envía el mensaje de ADSPROP de notificación de **\_ \_ \_ PAGEINIT de WM** al objeto de notificación para lograr este resultado.


```C++
WM_ADSPROP_NOTIFY_PAGEINIT

    WPARAM wParam
    LPARAM pADsPropInitParams
    
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador* 
</dt> <dd>

Identificador del objeto de notificación. Este es el parámetro *hNotifyObject* obtenido mediante una llamada a [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

No se utiliza.

</dd> <dt>

*pADsPropInitParams* 
</dt> <dd>

Puntero a una estructura [**ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) que recibe la información del objeto de directorio. Este es el parámetro *pInitParams* pasado a [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no tiene ningún valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Adsprop. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mensajes en Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> <dt>

[**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo)
</dt> <dt>

[**ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams)
</dt> </dl>

 

 





