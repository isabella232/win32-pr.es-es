---
title: Propiedad GatewayPreAuthRequirement de IMsRdpClientTransportSettings2
description: Especifica o recupera la configuración de si la característica de contraseña de un solo uso (OTP) Escritorio remoto Gateway (Puerta de enlace de Escritorio remoto) está habilitada.
ms.assetid: cc8f7ebb-16ba-45ed-ba66-de4a339946d0
ms.tgt_platform: multiple
keywords:
- Propiedad GatewayPreAuthRequirement Servicios de Escritorio remoto
- Propiedad GatewayPreAuthRequirement Servicios de Escritorio remoto interfaz , IMsRdpClientTransportSettings2
- Interfaz IMsRdpClientTransportSettings2 Servicios de Escritorio remoto , propiedad GatewayPreAuthRequirement
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.get_GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.put_GatewayPreAuthRequirement
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72dd588cd3280128dde654497de359a901182935035213e420831857ab5c9f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771265"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthrequirement-property"></a>Propiedad IMsRdpClientTransportSettings2::GatewayPreAuthRequirement

Especifica o recupera la configuración de si la característica de contraseña de un solo uso (OTP) Escritorio remoto Gateway (Puerta de enlace de Escritorio remoto) está habilitada.

Cuando OTP está habilitado, **GatewayPreAuthRequirement** intenta consultar la cookie de OTP desde el almacén de cookies de Internet mediante la [**propiedad GatewayPreAuthServerAddr.**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md) Si se realiza **correctamente, GatewayPreAuthRequirement** envía la cookie de OTP al servidor de firewall (como el servidor ISA de aceleración y seguridad de Internet de Microsoft) para la \[ \] autenticación previa.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayPreAuthRequirement(
  [in]  ULONG ulProxyPreAuthRequirement
);

HRESULT get_GatewayPreAuthRequirement(
  [out] ULONG *pulProxyPreAuthRequirement
);
```



## <a name="property-value"></a>Valor de propiedad

Si se establece en 1, la característica OTP está habilitada. Si se establece en 0, la característica OTP está deshabilitada.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





