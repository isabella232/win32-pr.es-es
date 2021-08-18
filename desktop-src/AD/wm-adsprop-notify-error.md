---
title: WM_ADSPROP_NOTIFY_ERROR mensaje (Adsprop.h)
description: El mensaje WM ADSPROP NOTIFY ERROR agrega un mensaje de error a una lista de mensajes de error que se muestran mediante una llamada a la función \_ \_ \_ ADsPropShowErrorDialog.
ms.assetid: 7abf1b3d-5abe-42cd-baeb-1bf863c7f04d
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_ERROR mensaje Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_ERROR
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52f88cd4c60dcfcceed60ca644f7c59f65bee16e344cc17664e8b4be1ee18fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024293"
---
# <a name="wm_adsprop_notify_error-message"></a>Mensaje DE ERROR \_ WM ADSPROP \_ NOTIFY \_

El **mensaje \_ WM ADSPROP NOTIFY \_ \_ ERROR** agrega un mensaje de error a una lista de mensajes de error que se muestran mediante una llamada a la función [**ADsPropShowErrorDialog.**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)


```C++
WM_ADSPROP_NOTIFY_ERROR

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Identificador del objeto de notificación. Este es el *parámetro hNotifyObject* obtenido por [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

No se usa.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura ADSPROPERROR que**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror) contiene datos de mensaje de error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no tiene ningún valor devuelto.

## <a name="remarks"></a>Comentarios

La [**función ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) es el método preferido para enviar este mensaje.

Los mensajes de error agregados por el mensaje **DE ERROR NOTIFY \_ \_ \_ DE WM ADSPROP** se acumulan hasta que se llama [**a ADsPropShowErrorDialog.**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) **ADsPropShowErrorDialog** combina y muestra los mensajes de error acumulados. Cuando se descarta el cuadro de diálogo de error, se eliminan los mensajes de error acumulados.

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

[**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror)
</dt> <dt>

[**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage)
</dt> <dt>

[**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)
</dt> </dl>

 

 





