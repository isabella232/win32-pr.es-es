---
title: Propiedad IMsRdpClientTransportSettings3 GatewayCredSourceCookie
description: Especifica si el origen de credenciales se basa en cookies.
ms.assetid: 039459a3-7a83-444c-a0b4-46ef0dc5ddd0
ms.tgt_platform: multiple
keywords:
- Propiedad GatewayCredSourceCookie Servicios de Escritorio remoto
- Propiedad GatewayCredSourceCookie Servicios de Escritorio remoto interfaz , IMsRdpClientTransportSettings3
- Interfaz IMsRdpClientTransportSettings3 Servicios de Escritorio remoto , propiedad GatewayCredSourceCookie
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.get_GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.put_GatewayCredSourceCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fae89a3b7694d1ab73c076464b7ac62e6b18bcac6b4877d6156731135ee47a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606950"
---
# <a name="imsrdpclienttransportsettings3gatewaycredsourcecookie-property"></a>IMsRdpClientTransportSettings3::GatewayCredSourceCookie, propiedad

Especifica si el origen de credenciales se basa en cookies. Contiene uno si el origen de credenciales está basado en cookies o cero en caso contrario.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_GatewayCredSourceCookie(
  [in]          ULONG ulProxyCredSourceCookie
);

HRESULT get_GatewayCredSourceCookie(
  [out, retval] ULONG *pulProxyCredSourceCookie
);
```



## <a name="property-value"></a>Valor de propiedad

Valor **ULONG** que especifica si el origen de credenciales se basa en cookies.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





