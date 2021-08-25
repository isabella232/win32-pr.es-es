---
title: Propiedad IMsRdpClientTransportSettings2 GatewaySupportUrl
description: Especifica o recupera la dirección web del sitio que proporciona soporte técnico para este servidor Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).
ms.assetid: e9c0f5ec-1b2f-4e09-8169-4316fd394443
ms.tgt_platform: multiple
keywords:
- Propiedad GatewaySupportUrl Servicios de Escritorio remoto
- Propiedad GatewaySupportUrl Servicios de Escritorio remoto interfaz , IMsRdpClientTransportSettings2
- Interfaz IMsRdpClientTransportSettings2 Servicios de Escritorio remoto , propiedad GatewaySupportUrl
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewaySupportUrl
- IMsRdpClientTransportSettings2.get_GatewaySupportUrl
- IMsRdpClientTransportSettings2.put_GatewaySupportUrl
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2833962f66fb6fab2597629877c5990c9234eb5b2dfe076073bedc2ceab9fd65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770695"
---
# <a name="imsrdpclienttransportsettings2gatewaysupporturl-property"></a>Propiedad IMsRdpClientTransportSettings2::GatewaySupportUrl

Especifica o recupera la dirección web del sitio que proporciona soporte técnico para este servidor Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewaySupportUrl(
  [in]  BSTR bstrProxySupportUrl
);

HRESULT get_GatewaySupportUrl(
  [out] BSTR *pbstrProxySupportUrl
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica o recupera la dirección web del sitio que proporciona soporte técnico para este servidor de puerta de enlace de Escritorio remoto.

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

 

 





