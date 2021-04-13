---
title: Propiedad GatewayPreAuthRequirement de IMsRdpClientTransportSettings2
description: Especifica o recupera la configuración de si la característica de contraseña de un solo tiempo (OTP) de Escritorio remoto puerta de enlace de escritorio remoto está habilitada.
ms.assetid: cc8f7ebb-16ba-45ed-ba66-de4a339946d0
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayPreAuthRequirement
- Propiedad GatewayPreAuthRequirement Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings2, propiedad GatewayPreAuthRequirement
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
ms.openlocfilehash: 058ca92237a4f9729f526030f5f8a836ce1c739c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535326"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthrequirement-property"></a>IMsRdpClientTransportSettings2:: GatewayPreAuthRequirement (propiedad)

Especifica o recupera la configuración de si la característica de contraseña de un solo tiempo (OTP) de Escritorio remoto puerta de enlace de escritorio remoto está habilitada.

Cuando OTP está habilitado, **GatewayPreAuthRequirement** intenta consultar la cookie de OTP desde el almacén de cookies de Internet mediante la propiedad [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md) . Si se realiza correctamente, **GatewayPreAuthRequirement** envía la cookie de OTP al servidor de Firewall (como Microsoft Internet Security and Acceleration \[ ISA \] Server) para la autenticación previa.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


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

Devuelve **S \_ correcto** si se realiza correctamente.

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

 

 





