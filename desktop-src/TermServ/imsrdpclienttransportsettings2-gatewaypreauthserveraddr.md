---
title: Propiedad IMsRdpClientTransportSettings2 GatewayPreAuthServerAddr
description: Especifica o recupera la dirección web del servidor de autenticación previa, que se usa para la característica de contraseña única (OTP) de puerta de enlace de Escritorio remoto (puerta de enlace de Escritorio remoto).
ms.assetid: 14edad82-ab19-46fe-b878-d34298763c56
ms.tgt_platform: multiple
keywords:
- Propiedad GatewayPreAuthServerAddr Servicios de Escritorio remoto
- Propiedad GatewayPreAuthServerAddr Servicios de Escritorio remoto , interfaz IMsRdpClientTransportSettings2
- Interfaz IMsRdpClientTransportSettings2 Servicios de Escritorio remoto , propiedad GatewayPreAuthServerAddr
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.get_GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.put_GatewayPreAuthServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89fa3df8431f829c0dd85cd3a448965e98b4e6d5e6285ae75d18c76257ddbb00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000915"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthserveraddr-property"></a>Propiedad IMsRdpClientTransportSettings2::GatewayPreAuthServerAddr

Especifica o recupera la dirección web del servidor de autenticación previa, que se usa para la característica de contraseña única (OTP) de puerta de enlace de Escritorio remoto (puerta de enlace de Escritorio remoto).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayPreAuthServerAddr(
  [in]  BSTR bstrProxyPreAuthServerAddr
);

HRESULT get_GatewayPreAuthServerAddr(
  [out] BSTR *pbstrProxyPreAuthServerAddr
);
```



## <a name="property-value"></a>Valor de propiedad

Dirección web del servidor de autenticación previa; por ejemplo, la dirección web del servidor de Seguridad y aceleración de Internet (ISA) de Microsoft. Especifique la dirección web con el formato "https://*HostName*. *DomainName*.com/*WebsiteName*" o "https://*HostName*. *DomainName*.com/*WebsiteName*".

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

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
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





