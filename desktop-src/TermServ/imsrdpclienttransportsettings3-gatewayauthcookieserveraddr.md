---
title: Propiedad IMsRdpClientTransportSettings3 GatewayAuthCookieServerAddr
description: Dirección del servidor para la autenticación basada en cookies.
ms.assetid: e00480cd-2133-42ff-8447-6c4234b56bf9
ms.tgt_platform: multiple
keywords:
- Propiedad GatewayAuthCookieServerAddr Servicios de Escritorio remoto
- Propiedad GatewayAuthCookieServerAddr Servicios de Escritorio remoto , interfaz IMsRdpClientTransportSettings3
- Interfaz IMsRdpClientTransportSettings3 Servicios de Escritorio remoto , propiedad GatewayAuthCookieServerAddr
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.get_GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.put_GatewayAuthCookieServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 330a1ddb15d548988c23f8140ce848f7f68be5d1deb17fc51bd88eed23b9eec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000930"
---
# <a name="imsrdpclienttransportsettings3gatewayauthcookieserveraddr-property"></a>Propiedad IMsRdpClientTransportSettings3::GatewayAuthCookieServerAddr

Dirección del servidor para la autenticación basada en cookies.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayAuthCookieServerAddr(
  [in]          BSTR bstrProxyAuthCookieServerAddr
);

HRESULT get_GatewayAuthCookieServerAddr(
  [out, retval] BSTR *pbstrProxyAuthCookieServerAddr
);
```



## <a name="property-value"></a>Valor de propiedad

Nueva dirección del servidor para la autenticación basada en cookies.

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

 

 





