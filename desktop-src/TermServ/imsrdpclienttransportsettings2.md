---
title: Interfaz IMsRdpClientTransportSettings2
description: Administra la configuración de transporte de cliente para el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto). | Interfaz IMsRdpClientTransportSettings2
ms.assetid: 4f9f1905-2693-4666-9f6f-6e00b1eb6a0f
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings2, descrito
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
ms.openlocfilehash: 7f2f4887c6a4f55f3b9c97c389e9afd702d2ffab
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689738"
---
# <a name="imsrdpclienttransportsettings2-interface"></a>Interfaz IMsRdpClientTransportSettings2

Administra la configuración de transporte de cliente para el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).

## <a name="members"></a>Miembros

La interfaz **IMsRdpClientTransportSettings2** hereda de [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md). **IMsRdpClientTransportSettings2** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IMsRdpClientTransportSettings2** tiene estas propiedades.



| Propiedad                                                                                                    | Tipo de acceso           | Descripción                                                                                       |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------|
| [**GatewayCredSharing**](imsrdpclienttransportsettings2-gatewaycredsharing.md)<br/>                  | Lectura/escritura<br/> | Indica si la característica de inicio de sesión único para la puerta de enlace de escritorio remoto está habilitada.<br/>                |
| [**GatewayDomain**](imsrdpclienttransportsettings2-gatewaydomain.md)<br/>                            | Lectura/escritura<br/> | El nombre de dominio que proporciona un usuario para conectarse al servidor de puerta de enlace de escritorio remoto.<br/>              |
| [**GatewayEncryptedOtpCookie**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>     | Lectura/escritura<br/> | Cookie de OTP cifrada.<br/>                                                              |
| [**GatewayEncryptedOtpCookieSize**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/> | Lectura/escritura<br/> | Tamaño, en bytes, de la cookie de OTP cifrada.<br/>                                       |
| [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md)<br/>                        | Solo escritura<br/> | La contraseña que un usuario proporciona para conectarse al servidor de puerta de enlace de escritorio remoto.<br/>                 |
| [**GatewayPreAuthRequirement**](imsrdpclienttransportsettings2-gatewaypreauthrequirement.md)<br/>    | Lectura/escritura<br/> | Indica si la característica de contraseña de un solo tiempo (OTP) de puerta de enlace de escritorio remoto está habilitada.<br/>           |
| [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>      | Lectura/escritura<br/> | Dirección web del servidor de autenticación previa.<br/>                                      |
| [**GatewaySupportUrl**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>             | Lectura/escritura<br/> | Dirección web del sitio que proporciona soporte técnico para el servidor de puerta de enlace de escritorio remoto.<br/> |
| [**GatewayUsername**](imsrdpclienttransportsettings2-gatewayusername.md)<br/>                        | Lectura/escritura<br/> | El nombre de usuario que proporciona un usuario para conectarse al servidor de puerta de enlace de escritorio remoto.<br/>                |



 

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

 

 





