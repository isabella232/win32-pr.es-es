---
title: IMsRdpClientTransportSettings (interfaz)
description: Administra la configuración de transporte de cliente para el Escritorio remoto gateway (puerta de enlace de Escritorio remoto). | IMsRdpClientTransportSettings (interfaz)
ms.assetid: d2573727-1dcc-4d4d-af5c-038e9467ba84
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpClientTransportSettings Servicios de Escritorio remoto
- Interfaz IMsRdpClientTransportSettings Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edd2cbcdaba0a4324c4501339e972f8bb967f64716d1688cef7c3c38bb22b5b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771455"
---
# <a name="imsrdpclienttransportsettings-interface"></a>IMsRdpClientTransportSettings (interfaz)

Administra la configuración de transporte de cliente para el Escritorio remoto gateway (puerta de enlace de Escritorio remoto).

## <a name="members"></a>Miembros

La **interfaz IMsRdpClientTransportSettings** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IMsRdpClientTransportSettings** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpClientTransportSettings** tiene estas propiedades.



| Propiedad                                                                                                          | Tipo de acceso           | Descripción                                                 |
|:------------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------|
| [**GatewayCredsSource**](imsrdpclienttransportsettings-gatewaycredssource.md)<br/>                         | Lectura/escritura<br/> | El método de autenticación del servidor de puerta de enlace de Escritorio remoto.<br/>     |
| [**GatewayDefaultUsageMethod**](imsrdpclienttransportsettings-gatewaydefaultusagemethod.md)<br/>           | Solo lectura<br/>  | Método de uso predeterminado de puerta de enlace de Escritorio remoto.<br/>             |
| [**GatewayHostname**](imsrdpclienttransportsettings-gatewayhostname.md)<br/>                               | Lectura/escritura<br/> | Nombre de host del servidor de puerta de enlace de Escritorio remoto.<br/>              |
| [**GatewayIsSupported**](imsrdpclienttransportsettings-gatewayissupported.md)<br/>                         | Solo lectura<br/>  | Indica si se admite la puerta de enlace de Escritorio remoto.<br/>       |
| [**GatewayProfileUsageMethod**](imsrdpclienttransportsettings-gatewayprofileusagemethod.md)<br/>           | Lectura/escritura<br/> | El método de uso del perfil de puerta de enlace de Escritorio remoto.<br/>             |
| [**GatewayUsageMethod**](imsrdpclienttransportsettings-gatewayusagemethod.md)<br/>                         | Lectura/escritura<br/> | Método de uso del servidor de puerta de enlace de Escritorio remoto.<br/>              |
| [**GatewayUserSelectedCredsSource**](imsrdpclienttransportsettings-gatewayuserselectedcredssource.md)<br/> | Lectura/escritura<br/> | Origen de credenciales de puerta de enlace de Escritorio remoto especificado por el usuario.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings se define como 720298C0-A099-46f5-9F82-96921BAE4701<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Conexión web a Escritorio remoto referencia](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

