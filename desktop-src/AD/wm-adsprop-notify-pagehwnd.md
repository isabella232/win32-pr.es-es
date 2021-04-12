---
title: Mensaje de WM_ADSPROP_NOTIFY_PAGEHWND (Adsprop. h)
description: Una extensión de la hoja de propiedades del servicio de directorio de Active Directory llama a ADsPropSetHwnd para informar al objeto de notificación del identificador de la ventana de la página de propiedades.
ms.assetid: eb8bf525-cd7f-44d0-a0f9-43178a29c443
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_PAGEHWND Active Directory de mensaje
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
ms.openlocfilehash: d74ef2db993d2a3daf10f69687b8f3525ef80a87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150931"
---
# <a name="wm_adsprop_notify_pagehwnd-message"></a>\_Mensaje de \_ PAGEHWND de notificación de ADSPROP de WM \_

Una extensión de la hoja de propiedades del servicio de directorio de Active Directory llama a [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) para informar al objeto de notificación del identificador de la ventana de la página de propiedades. La función **ADsPropSetHwnd** envía el mensaje **WM \_ ADSPROP \_ Notify \_ PAGEHWND** al objeto de notificación, que informa al objeto de notificación del identificador de la ventana de la página de propiedades.


```C++
WM_ADSPROP_NOTIFY_PAGEHWND

    WPARAM hPage
    LPARAM ptzTitle
    
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hNotifyObj* 
</dt> <dd>

Identificador del objeto de notificación. Para obtener este identificador, llame a [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*hPage* 
</dt> <dd>

Identificador de ventana de la página de propiedades.

</dd> <dt>

*ptzTitle* 
</dt> <dd>

Puntero a un búfer **WCHAR** terminado en null que contiene el título de la página de propiedades.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

Una Active Directory extensión de la hoja de propiedades normalmente llama a la función [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) mientras procesa el mensaje [**\_ INITDIALOG de WM**](../dlgbox/wm-initdialog.md) .

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

[**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd)
</dt> <dt>

[**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[**INITDIALOG de WM \_**](../dlgbox/wm-initdialog.md)
</dt> </dl>

 

