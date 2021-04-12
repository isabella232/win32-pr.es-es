---
title: Propiedad GatewayCredSharing de IMsRdpClientTransportSettings2
description: Especifica o recupera la configuración de si está habilitada la característica de uso compartido de credenciales de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 296dc578-376d-41f6-988a-286fe744959f
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayCredSharing
- Propiedad GatewayCredSharing Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings2, propiedad GatewayCredSharing
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
ms.openlocfilehash: 329e425631b674e050f246c4105115bd4326be3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489520"
---
# <a name="imsrdpclienttransportsettings2gatewaycredsharing-property"></a>IMsRdpClientTransportSettings2:: GatewayCredSharing (propiedad)

Especifica o recupera la configuración de si está habilitada la característica de uso compartido de credenciales de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto). Cuando la característica está habilitada, el control ActiveX Escritorio remoto intenta usar las mismas credenciales para autenticarse en el servidor host de sesión Escritorio remoto (host de sesión de escritorio remoto) y en el servidor de puerta de enlace de escritorio remoto.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_GatewayCredSharing(
  [in]  ULONG ulProxyCredSharing
);

HRESULT get_GatewayCredSharing(
  [out] ULONG *pulProxyCredSharing
);
```



## <a name="property-value"></a>Valor de propiedad

Si se establece en uno, se habilita el uso compartido de credenciales. Si se establece en cero, el uso compartido de credenciales está deshabilitado.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ correcto** si se realiza correctamente.

## <a name="remarks"></a>Observaciones

El control ActiveX utiliza esta propiedad para implementar un único aviso para el uso compartido de credenciales entre el servidor host de sesión de escritorio remoto y el servidor de puerta de enlace de escritorio remoto. El uso compartido de credenciales no admite el uso compartido de contraseñas basado en Web con [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md) o [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md).

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

 

 





