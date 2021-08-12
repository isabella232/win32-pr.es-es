---
title: Propiedad IMsRdpClientTransportSettings GatewayDefaultUsageMethod
description: Método de uso predeterminado para Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).
ms.assetid: 7014538d-550a-4246-ad32-406ef67fb112
ms.tgt_platform: multiple
keywords:
- Propiedad GatewayDefaultUsageMethod Servicios de Escritorio remoto
- Propiedad GatewayDefaultUsageMethod Servicios de Escritorio remoto , interfaz IMsRdpClientTransportSettings
- Interfaz IMsRdpClientTransportSettings Servicios de Escritorio remoto , propiedad GatewayDefaultUsageMethod
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
ms.openlocfilehash: 6403f319eaa79b9d140a3d75f9dd4f7625eced916ee907755c017d3e58a1767f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118607426"
---
# <a name="imsrdpclienttransportsettingsgatewaydefaultusagemethod-property"></a>Propiedad IMsRdpClientTransportSettings::GatewayDefaultUsageMethod

Método de uso predeterminado para Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_GatewayDefaultUsageMethod(
  [out] ULONG *pulProxyDefaultUsageMethod
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero al método de uso predeterminado para puerta de enlace de Escritorio remoto. Devuelve una unión de la configuración de usuario establecida por [**put \_ GatewayUsageMethod() y**](imsrdpclienttransportsettings-gatewayusagemethod.md)la configuración de directiva de grupo. Si no se estableció ninguna configuración de usuario mediante **put \_ GatewayUsageMethod(),** **get \_ GatewayDefaultUsageMethod()** devolverá el valor predeterminado de **TSC \_ PROXY MODE \_ \_ DETECT**.

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

 

 





