---
title: Propiedad IMsRdpClientTransportSettings3 GatewayEncryptedAuthCookieSize
description: Tamaño, en caracteres, de la propiedad GatewayEncryptedAuthCookie.
ms.assetid: 52e24bef-5afa-4954-b639-08ea8701404a
ms.tgt_platform: multiple
keywords:
- Propiedad GatewayEncryptedAuthCookieSize Servicios de Escritorio remoto
- Propiedad GatewayEncryptedAuthCookieSize Servicios de Escritorio remoto , interfaz IMsRdpClientTransportSettings3
- Interfaz IMsRdpClientTransportSettings3 Servicios de Escritorio remoto , propiedad GatewayEncryptedAuthCookieSize
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayEncryptedAuthCookieSize
- IMsRdpClientTransportSettings3.get_GatewayEncryptedAuthCookieSize
- IMsRdpClientTransportSettings3.put_GatewayEncryptedAuthCookieSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41e26e4d15c134bcd8a2dd5bbf74b574f38ce56627d0f7e7840547ed1d56a67a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606940"
---
# <a name="imsrdpclienttransportsettings3gatewayencryptedauthcookiesize-property"></a>Propiedad IMsRdpClientTransportSettings3::GatewayEncryptedAuthCookieSize

Tamaño, en caracteres, de la [**propiedad GatewayEncryptedAuthCookie.**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md)

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_GatewayEncryptedAuthCookieSize(
  [in]          ULONG ulEncryptedAuthCookieSize
);

HRESULT get_GatewayEncryptedAuthCookieSize(
  [out, retval] ULONG *ulEncryptedAuthCookieSize
);
```



## <a name="property-value"></a>Valor de propiedad

Valor **ULONG** que contiene el nuevo valor de tamaño.

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

 

 





