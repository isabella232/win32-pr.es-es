---
title: Propiedad GatewayUserName de IMsRdpClientTransportSettings2
description: Especifica o recupera el nombre de usuario que se proporciona al servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: eb5ed12f-e650-4abb-be20-bd5fae44e604
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayUserName
- Propiedad GatewayUserName Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings2, propiedad GatewayUserName
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayUserName
- IMsRdpClientTransportSettings2.get_GatewayUserName
- IMsRdpClientTransportSettings2.put_GatewayUserName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48244c49c942c917c58bfc2790b423981f17fe98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676636"
---
# <a name="imsrdpclienttransportsettings2gatewayusername-property"></a>IMsRdpClientTransportSettings2:: GatewayUserName (propiedad)

Especifica o recupera el nombre de usuario que se proporciona al servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_GatewayUserName(
  [in]  BSTR proxyUserName
);

HRESULT get_GatewayUserName(
  [out] BSTR *pProxyUserName
);
```



## <a name="property-value"></a>Valor de propiedad

El nombre de usuario que se proporciona para conectarse al servidor de puerta de enlace de escritorio remoto.

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

 

 





