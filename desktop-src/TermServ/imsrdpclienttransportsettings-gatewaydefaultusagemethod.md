---
title: Propiedad GatewayDefaultUsageMethod de IMsRdpClientTransportSettings
description: El método de uso predeterminado para la puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 7014538d-550a-4246-ad32-406ef67fb112
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayDefaultUsageMethod
- Propiedad GatewayDefaultUsageMethod Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings, propiedad GatewayDefaultUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayDefaultUsageMethod
- IMsRdpClientTransportSettings.get_GatewayDefaultUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b8417da30f9a692e6e233174a33f4b03682a5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685898"
---
# <a name="imsrdpclienttransportsettingsgatewaydefaultusagemethod-property"></a>IMsRdpClientTransportSettings:: GatewayDefaultUsageMethod (propiedad)

El método de uso predeterminado para la puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_GatewayDefaultUsageMethod(
  [out] ULONG *pulProxyDefaultUsageMethod
);
```



## <a name="property-value"></a>Valor de propiedad

Un puntero al método de uso predeterminado para la puerta de enlace de escritorio remoto. Devuelve una Unión de la configuración de usuario establecida por [**Put \_ GatewayUsageMethod ()**](imsrdpclienttransportsettings-gatewayusagemethod.md)y la configuración de directiva de grupo. Si no se estableció ninguna configuración de usuario en **Put \_ GatewayUsageMethod ()**, **Get \_ GatewayDefaultUsageMethod ()** devolverá el valor predeterminado de la **\_ \_ \_ detección del modo proxy de TSC**.

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

 

 





