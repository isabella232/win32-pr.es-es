---
title: Propiedad IMsTscSecuredSettings Fullscreen
description: Especifica el estado de pantalla completa del control de cliente.
ms.assetid: f65c2fa3-b2d0-4e64-bf1e-08394c91eda8
ms.tgt_platform: multiple
keywords:
- Propiedad fullScreen Servicios de Escritorio remoto
- Propiedad fullScreen Servicios de Escritorio remoto, interfaz IMsTscSecuredSettings
- Interfaz IMsTscSecuredSettings Servicios de Escritorio remoto, propiedad fullScreen
- Propiedad fullScreen Servicios de Escritorio remoto, interfaz IMsRdpClientSecuredSettings
- Interfaz IMsRdpClientSecuredSettings Servicios de Escritorio remoto, propiedad fullScreen
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.Fullscreen
- IMsTscSecuredSettings.get_Fullscreen
- IMsTscSecuredSettings.put_Fullscreen
- IMsRdpClientSecuredSettings.Fullscreen
- IMsRdpClientSecuredSettings.get_Fullscreen
- IMsRdpClientSecuredSettings.put_Fullscreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c3b3208edf3476fcd110d7729d97d9817cb929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676927"
---
# <a name="imstscsecuredsettingsfullscreen-property"></a>IMsTscSecuredSettings:: Fullscreen (propiedad)

Especifica el estado de pantalla completa del control de cliente.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Fullscreen(
  [in]  BOOL fFullScreen
);

HRESULT get_Fullscreen(
  [out] BOOL *pfFullScreen
);
```



## <a name="property-value"></a>Valor de propiedad

Establezca este parámetro en **true** si el control debe usar el modo de pantalla completa y **false** en caso contrario.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ correcto** si se realiza correctamente.

## <a name="remarks"></a>Observaciones

Para obtener más información acerca de este método, consulte [proporcionar seguridad de cliente RDP](providing-for-rdp-client-security.md).

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

Tenga en cuenta que aunque el uso de esta propiedad está restringido a las zonas de seguridad de direcciones URL permitidas de Internet Explorer, un usuario siempre puede cambiar al modo de pantalla completa después de que se haya establecido la conexión presionando la combinación de [teclas de método abreviado](terminal-services-shortcut-keys.md) del modo de pantalla completa (Ctrl + Alt + inter).

Se puede llamar a este método mientras se establece la conexión de cliente.

Debe llamar al método [**IMsRdpClientNonScriptable3::p UT \_ ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) antes de llamar al método de **\_ pantalla completa IMsTscSecuredSettings::p UT** o al método de [**\_ pantalla completa IMsRdpClient::p UT**](imsrdpclient-fullscreen.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsTscSecuredSettings se define como c9d65442-a0f9-45b2-8f73-d61d2db8cbb6<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





