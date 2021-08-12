---
title: IMsRdpClientTransportSettings3 (interfaz)
description: Define propiedades adicionales para el servidor Escritorio remoto Gateway (puerta de enlace de Escritorio remoto). | IMsRdpClientTransportSettings3 (interfaz)
ms.assetid: c0bdfe23-9a26-4feb-b9b7-e52f04f23aa1
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpClientTransportSettings3 Servicios de Escritorio remoto
- Interfaz IMsRdpClientTransportSettings3 Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a7680e27b0d67c9273e4f47da4725c0acab6d173c560bb5b288a30a96931d7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606930"
---
# <a name="imsrdpclienttransportsettings3-interface"></a>IMsRdpClientTransportSettings3 (interfaz)

Define propiedades adicionales para el servidor Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).

## <a name="members"></a>Miembros

La **interfaz IMsRdpClientTransportSettings3** hereda de [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md). **IMsRdpClientTransportSettings3** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpClientTransportSettings3** tiene estas propiedades.



| Propiedad                                                                                                           | Tipo de acceso           | Descripción                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GatewayAuthCookieServerAddr**](imsrdpclienttransportsettings3-gatewayauthcookieserveraddr.md)<br/>       | Lectura/escritura<br/> | Dirección del servidor para la autenticación basada en cookies.<br/>                                                                                       |
| [**GatewayAuthLoginPage**](imsrdpclienttransportsettings3-gatewayauthloginpage.md)<br/>                     | Lectura/escritura<br/> | Dirección de la página web de inicio de sesión que se usará para autenticar a un usuario.<br/>                                                                           |
| [**GatewayCredSourceCookie**](imsrdpclienttransportsettings3-gatewaycredsourcecookie.md)<br/>               | Lectura/escritura<br/> | Especifica si el origen de credenciales se basa en cookies.<br/>                                                                                       |
| [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md)<br/>         | Lectura/escritura<br/> | Cookie de autenticación cifrada.<br/>                                                                                                      |
| [**GatewayEncryptedAuthCookieSize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)<br/> | Lectura/escritura<br/> | Tamaño, en caracteres, de la [**propiedad GatewayEncryptedAuthCookie.**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md)<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings3 se define como 3D5B21AC-748D-41DE-8F30-E15169586BD4<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





