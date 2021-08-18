---
title: Propiedad GatewayCredSharing de IMsRdpClientTransportSettings2
description: Especifica o recupera la configuración de si la característica de uso compartido de credenciales Escritorio remoto Gateway (puerta de enlace de Escritorio remoto) está habilitada.
ms.assetid: 296dc578-376d-41f6-988a-286fe744959f
ms.tgt_platform: multiple
keywords:
- Propiedad GatewayCredSharing Servicios de Escritorio remoto
- Propiedad GatewayCredSharing Servicios de Escritorio remoto , interfaz IMsRdpClientTransportSettings2
- Interfaz IMsRdpClientTransportSettings2 Servicios de Escritorio remoto , propiedad GatewayCredSharing
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayCredSharing
- IMsRdpClientTransportSettings2.get_GatewayCredSharing
- IMsRdpClientTransportSettings2.put_GatewayCredSharing
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6d489678006e842a6da82f5d2f9489f84a9a20fd70bfe8f18018aaa6d412c5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974655"
---
# <a name="imsrdpclienttransportsettings2gatewaycredsharing-property"></a>Propiedad IMsRdpClientTransportSettings2::GatewayCredSharing

Especifica o recupera la configuración de si la característica de uso compartido de credenciales Escritorio remoto Gateway (puerta de enlace de Escritorio remoto) está habilitada. Cuando la característica está habilitada, el control Escritorio remoto ActiveX intenta usar las mismas credenciales para autenticarse en el servidor de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto) y en el servidor de puerta de enlace de Escritorio remoto.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayCredSharing(
  [in]  ULONG ulProxyCredSharing
);

HRESULT get_GatewayCredSharing(
  [out] ULONG *pulProxyCredSharing
);
```



## <a name="property-value"></a>Valor de propiedad

Si se establece en uno, se habilita el uso compartido de credenciales. Si se establece en cero, se deshabilita el uso compartido de credenciales.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Comentarios

Esta propiedad la usa el control ActiveX para implementar un único símbolo del sistema para el uso compartido de credenciales entre el servidor host de sesión de Escritorio remoto y el servidor de puerta de enlace de Escritorio remoto. El uso compartido de credenciales no admite el uso compartido de contraseñas basado en web [**con GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md) [**o ClearTextPassword.**](imstscnonscriptable-cleartextpassword.md)

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

 

 





