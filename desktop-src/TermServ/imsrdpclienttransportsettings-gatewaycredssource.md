---
title: Propiedad IMsRdpClientTransportSettings GatewayCredsSource
description: Especifica o recupera el método de autenticación Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).
ms.assetid: 3b05edcb-f678-4d80-99fd-b76d27c80c68
ms.tgt_platform: multiple
keywords:
- Propiedad GatewayCredsSource Servicios de Escritorio remoto
- Propiedad GatewayCredsSource Servicios de Escritorio remoto , interfaz IMsRdpClientTransportSettings
- Interfaz IMsRdpClientTransportSettings Servicios de Escritorio remoto , propiedad GatewayCredsSource
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
ms.openlocfilehash: 0270d7123176161b2b90b423cde3d3945e15a179c3ffd5aa2335e079542c1098
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870875"
---
# <a name="imsrdpclienttransportsettingsgatewaycredssource-property"></a>Propiedad IMsRdpClientTransportSettings::GatewayCredsSource

Especifica o recupera el método de autenticación Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a>Valor de propiedad

Variable **ULONG que** especifica el método de autenticación de puerta de enlace de Escritorio remoto. Este parámetro puede ser uno de los valores siguientes.

<dt>

USERPASS EN MODO CREDS DEL PROXY TSC \_ \_ \_ \_ (0)
</dt> <dd>

Use una contraseña (NTLM) como método de autenticación para la puerta de enlace de Escritorio remoto.

</dd> <dt>

TARJETA INTELIGENTE \_ DE MODO \_ CREDS DE PROXY TSC \_ \_ (1)
</dt> <dd>

Use una tarjeta inteligente como método de autenticación para puerta de enlace de Escritorio remoto.

</dd> <dt>

TSC \_ PROXY \_ CREDS \_ MODE ANY \_ (4)
</dt> <dd>

Use cualquier método de autenticación para puerta de enlace de Escritorio remoto.

</dd> </dl>

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

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

 

 





