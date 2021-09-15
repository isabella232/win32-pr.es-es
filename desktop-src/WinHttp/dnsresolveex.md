---
description: Resolución de una cadena de host en su dirección IP
ms.assetid: 32d70f10-803b-484d-a9e0-d4c61a8d897f
title: Función dnsResolveEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1c63ba3e20653c41864394d9c563c851f2aab5e6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580669"
---
# <a name="dnsresolveex-function"></a>Función dnsResolveEx

Resolución de una cadena de host en su dirección IP

## <a name="parameters"></a>Parámetros

<dl> <dt>

*host* 
</dt> <dd>

Cadena que contiene el host HTTP que se proporciona a FindProxyForUrl.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Cadena delimitada por punto y coma que contiene direcciones IPv6 e IPv4 o una cadena vacía si el host no se puede resolver.

## <a name="remarks"></a>Observaciones

Los implementadores FindProxyforURLEx deben agregar código que divide la cadena de direcciones IP delimitadas por punto y coma en direcciones independientes.

## <a name="examples"></a>Ejemplos

``` syntax
dnsResolveEx("testmachine1");
    returns the string "fe80::380c:2e71:f5b9:a3b5%15;fe80::982d:a3b3:97ad:7dd0%9;2001:4898:28:7:982d:a3b3:97ad:7dd0;2001:4898:28:7:adfe:a643:8130:2fdc;fe80::5efe:10.70.92.74%13;3ffe:8311:ffff:f70f:0:5efe:10.70.92.74;10.70.92.74;3ffe:831f:4136:e37e:380c:2e71
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Definiciones de API del asistente de proxy compatibles con IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Extensiones IPv6 para el formato de archivo de configuración automática del navegador](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



