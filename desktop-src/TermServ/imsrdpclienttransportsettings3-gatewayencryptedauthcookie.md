---
title: Propiedad IMsRdpClientTransportSettings3 GatewayEncryptedAuthCookie
description: Cookie de autenticación cifrada.
ms.assetid: c9ab6667-327c-44f8-a10e-b048ea91980c
ms.tgt_platform: multiple
keywords:
- Propiedad GatewayEncryptedAuthCookie Servicios de Escritorio remoto
- Propiedad GatewayEncryptedAuthCookie Servicios de Escritorio remoto , interfaz IMsRdpClientTransportSettings3
- Interfaz IMsRdpClientTransportSettings3 Servicios de Escritorio remoto , propiedad GatewayEncryptedAuthCookie
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayEncryptedAuthCookie
- IMsRdpClientTransportSettings3.get_GatewayEncryptedAuthCookie
- IMsRdpClientTransportSettings3.put_GatewayEncryptedAuthCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c05a83d3b6891bfb8173a45935dcd73ad9ad65db5643d093306eda6e5d1cb20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000885"
---
# <a name="imsrdpclienttransportsettings3gatewayencryptedauthcookie-property"></a>Propiedad IMsRdpClientTransportSettings3::GatewayEncryptedAuthCookie

Cookie de autenticación cifrada. El tamaño de la propiedad se especifica mediante la [**propiedad GatewayEncryptedAuthCookieSize.**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayEncryptedAuthCookie(
  [in]          BSTR bstrEncryptedAuthCookie
);

HRESULT get_GatewayEncryptedAuthCookie(
  [out, retval] BSTR *pbstrEncryptedAuthCookie
);
```



## <a name="property-value"></a>Valor de propiedad

Nueva cookie de autenticación cifrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GatewayEncryptedAuthCookieSize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)
</dt> <dt>

[**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





