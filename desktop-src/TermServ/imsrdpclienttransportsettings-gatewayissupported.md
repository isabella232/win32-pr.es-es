---
title: Propiedad GatewayIsSupported de IMsRdpClientTransportSettings
description: Especifica si se admite la puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 31edd35b-251d-404d-bec8-e082bb2427b3
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayIsSupported
- Propiedad GatewayIsSupported Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings, propiedad GatewayIsSupported
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayIsSupported
- IMsRdpClientTransportSettings.get_GatewayIsSupported
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de79033c2ab9bae73aae4213e72a54590170a184
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421926"
---
# <a name="imsrdpclienttransportsettingsgatewayissupported-property"></a>IMsRdpClientTransportSettings:: GatewayIsSupported (propiedad)

Especifica si se admite la puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_GatewayIsSupported(
  [out] BOOL *pfProxyIsSupported
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica si se admite la puerta de enlace de escritorio remoto.

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

 

 





