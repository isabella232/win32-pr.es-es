---
description: Ordena una lista de direcciones IP.
ms.assetid: 1266d6f3-e9f5-4e6b-9431-7329df156f0a
title: Función sortIpAddressList
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
ms.openlocfilehash: 3144ecf044f832a49dd6aa4d9fabf76ce8e81c79c195ec101d294c432a8081e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562460"
---
# <a name="sortipaddresslist-function"></a>Función sortIpAddressList

Ordena una lista de direcciones IP.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*IpAddressList* 
</dt> <dd>

Cadena delimitada por punto y coma que contiene direcciones IP.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Lista de direcciones IP delimitadas por punto y coma ordenadas o una cadena vacía si no se puede ordenar la lista de direcciones IP.

## <a name="remarks"></a>Observaciones

Los implementadores FindProxyforURLEx deben agregar código que divide la cadena de direcciones IP delimitadas por punto y coma en direcciones independientes.

## <a name="examples"></a>Ejemplos

``` syntax
sortIpAddressList(2001:4898:28:3:201:2ff:feea:fc14; 
                  157.59.139.22; 
                  fe80::5efe:157.59.139.22");
    returns "fe80::5efe:157.59.139.22;2001:4898:28:3:201:2ff:feea:fc14;157.59.139.22" 
    A list of sorted IP addresses. If there both IPv6 and IPv4 IP addresses are passed as input to this function, then the sorted IPv6 addresses are followed by sorted IPv4 addresses
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Definiciones de API del asistente de proxy compatibles con IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Extensiones IPv6 para el formato de archivo de configuración automática del navegador](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



