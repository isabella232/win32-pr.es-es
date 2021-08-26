---
title: Propiedad IMsRdpClientTransportSettings GatewayHostname
description: Especifica el nombre de host del servidor Escritorio remoto gateway (puerta de enlace de Escritorio remoto).
ms.assetid: 34c4b3b7-3768-4d98-b1e8-7fcb8f9c758d
ms.tgt_platform: multiple
keywords:
- Propiedad GatewayHostname Servicios de Escritorio remoto
- Propiedad GatewayHostname Servicios de Escritorio remoto , interfaz IMsRdpClientTransportSettings
- Interfaz IMsRdpClientTransportSettings Servicios de Escritorio remoto , propiedad GatewayHostname
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayHostname
- IMsRdpClientTransportSettings.get_GatewayHostname
- IMsRdpClientTransportSettings.put_GatewayHostname
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de618d31f4d0989ebce319260f0afe4548d658e3c28891a9d26dad0580d62452
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870845"
---
# <a name="imsrdpclienttransportsettingsgatewayhostname-property"></a>Propiedad IMsRdpClientTransportSettings::GatewayHostname

Especifica el nombre de host del servidor Escritorio remoto gateway (puerta de enlace de Escritorio remoto).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayHostname(
  [in]  BSTR newVal
);

HRESULT get_GatewayHostname(
  [out] BSTR *pProxyHostname
);
```



## <a name="property-value"></a>Valor de propiedad

Cadena que contiene el nombre de host del servidor de puerta de enlace de Escritorio remoto.

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

 

 





