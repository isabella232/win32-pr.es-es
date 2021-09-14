---
title: Propiedad de pantalla completa IMsTscSecuredSettings
description: Especifica el estado de pantalla completa del control de cliente.
ms.assetid: f65c2fa3-b2d0-4e64-bf1e-08394c91eda8
ms.tgt_platform: multiple
keywords:
- Propiedades de pantalla completa Servicios de Escritorio remoto
- Propiedad de pantalla Servicios de Escritorio remoto , interfaz IMsTscSecuredSettings
- Interfaz IMsTscSecuredSettings Servicios de Escritorio remoto , propiedad Fullscreen
- Propiedad de pantalla Servicios de Escritorio remoto , interfaz IMsRdpClientSecuredSettings
- Interfaz IMsRdpClientSecuredSettings Servicios de Escritorio remoto , propiedad Fullscreen
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168714"
---
# <a name="imstscsecuredsettingsfullscreen-property"></a>Propiedad IMsTscSecuredSettings::Fullscreen

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

Establezca este parámetro en **TRUE si** el control debe usar el modo de pantalla completa y **FALSE en** caso contrario.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Observaciones

Para obtener más información sobre este método, vea [Proporcionar seguridad de cliente RDP.](providing-for-rdp-client-security.md)

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

Tenga en cuenta que aunque el uso de esta propiedad está restringido a las zonas de seguridad de url de Internet Explorer permitidas, [](terminal-services-shortcut-keys.md) un usuario siempre puede cambiar al modo de pantalla completa una vez establecida la conexión presionando la combinación de teclas de método abreviado de modo de pantalla completa (CTRL+ALT+BREAK).

Se puede llamar a este método mientras se establece la conexión de cliente.

Debe llamar al método [**IMsRdpClientNonScriptable3::p ut \_ ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) antes de llamar al método **IMsTscSecuredSettings::p ut \_ Fullscreen** o al método [**IMsRdpClient::p ut \_ Fullscreen.**](imsrdpclient-fullscreen.md)

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

 

 





