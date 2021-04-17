---
title: Propiedad GatewayCredsSource de IMsRdpClientTransportSettings
description: Especifica o recupera el método de autenticación de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 3b05edcb-f678-4d80-99fd-b76d27c80c68
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayCredsSource
- Propiedad GatewayCredsSource Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings, propiedad GatewayCredsSource
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayCredsSource
- IMsRdpClientTransportSettings.get_GatewayCredsSource
- IMsRdpClientTransportSettings.put_GatewayCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2771998ddc7c53d05c5d0db452f34a734a7c3e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422071"
---
# <a name="imsrdpclienttransportsettingsgatewaycredssource-property"></a>IMsRdpClientTransportSettings:: GatewayCredsSource (propiedad)

Especifica o recupera el método de autenticación de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_GatewayCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a>Valor de propiedad

Variable **ULong** que especifica el método de autenticación de puerta de enlace de escritorio remoto. Este parámetro puede ser uno de los valores siguientes.

<dt>

\_Modo de credenciales de proxy de TSC \_ \_ \_ USERPASS (0)
</dt> <dd>

Use una contraseña (NTLM) como método de autenticación para la puerta de enlace de escritorio remoto.

</dd> <dt>

\_ \_ Tarjeta inteligente del modo de credenciales de proxy de TSC \_ \_ (1)
</dt> <dd>

Usar una tarjeta inteligente como método de autenticación para la puerta de enlace de escritorio remoto.

</dd> <dt>

\_Modo de \_ credenciales de proxy TSC \_ \_ any (4)
</dt> <dd>

Use cualquier método de autenticación para la puerta de enlace de escritorio remoto.

</dd> </dl>

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ correcto** si se realiza correctamente.

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

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





