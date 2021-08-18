---
title: Interfaz IMsRdpClientTransportSettings2
description: Administra la configuración de transporte de cliente para el Escritorio remoto Gateway (puerta de enlace de Escritorio remoto). | Interfaz IMsRdpClientTransportSettings2
ms.assetid: 4f9f1905-2693-4666-9f6f-6e00b1eb6a0f
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpClientTransportSettings2 Servicios de Escritorio remoto
- Interfaz IMsRdpClientTransportSettings2 Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479fdceee0a1fc168725ef9b5acccb471e1b32b8c13a0e0ff6b12096f14ff0ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000955"
---
# <a name="imsrdpclienttransportsettings2-interface"></a>Interfaz IMsRdpClientTransportSettings2

Administra la configuración de transporte de cliente para el Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).

## <a name="members"></a>Miembros

La **interfaz IMsRdpClientTransportSettings2** hereda de [**IMsRdpClientTransportSettings.**](imsrdpclienttransportsettings.md) **IMsRdpClientTransportSettings2** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpClientTransportSettings2** tiene estas propiedades.



| Propiedad                                                                                                    | Tipo de acceso           | Descripción                                                                                       |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------|
| [**GatewayCredSharing**](imsrdpclienttransportsettings2-gatewaycredsharing.md)<br/>                  | Lectura/escritura<br/> | Indica si la característica de inicio de sesión único para puerta de enlace de Escritorio remoto está habilitada.<br/>                |
| [**GatewayDomain**](imsrdpclienttransportsettings2-gatewaydomain.md)<br/>                            | Lectura/escritura<br/> | Nombre de dominio que proporciona un usuario para conectarse al servidor de puerta de enlace de Escritorio remoto.<br/>              |
| [**GatewayEncryptedOtpCookie**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>     | Lectura/escritura<br/> | Cookie de OTP cifrada.<br/>                                                              |
| [**GatewayEncryptedOtpCookieSize**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/> | Lectura/escritura<br/> | Tamaño, en bytes, de la cookie de OTP cifrada.<br/>                                       |
| [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md)<br/>                        | Solo escritura<br/> | Contraseña que proporciona un usuario para conectarse al servidor de puerta de enlace de Escritorio remoto.<br/>                 |
| [**GatewayPreAuthRequirement**](imsrdpclienttransportsettings2-gatewaypreauthrequirement.md)<br/>    | Lectura/escritura<br/> | Indica si la característica de contraseña única (OTP) de puerta de enlace de Escritorio remoto está habilitada.<br/>           |
| [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>      | Lectura/escritura<br/> | Dirección web del servidor de autenticación previa.<br/>                                      |
| [**GatewaySupportUrl**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>             | Lectura/escritura<br/> | Dirección web del sitio que proporciona soporte técnico para el servidor de puerta de enlace de Escritorio remoto.<br/> |
| [**GatewayUsername**](imsrdpclienttransportsettings2-gatewayusername.md)<br/>                        | Lectura/escritura<br/> | Nombre de usuario que proporciona un usuario para conectarse al servidor de puerta de enlace de Escritorio remoto.<br/>                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista con SP1<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings2 se define como 67341688-D606-4c73-A5D2-2E0489009319<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





