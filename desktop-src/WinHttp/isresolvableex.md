---
description: Determina si una cadena de host determinada puede resolverse en una dirección IP.
ms.assetid: 83e52ca7-2ea0-419d-b09d-9301c1982b98
title: isResolvableEx función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isResolvableEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1172aaed93a9fc6cede5ae5393c5dd430613a466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706985"
---
# <a name="isresolvableex-function"></a>isResolvableEx función)

Determina si una cadena de host determinada puede resolverse en una dirección IP.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*host* 
</dt> <dd>

Cadena que contiene el host HTTP que se proporciona a FindProxyForUrl.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

TRUE si el host se va a resolver en una dirección IPv4 o IPv6; en caso contrario, FALSE.

## <a name="examples"></a>Ejemplos

``` syntax
isResolvableEx(host);
    true if the hostname can be resolved to and IP address 
```

``` syntax
isResolvableEx(host); 
    false if the hostname cannot be resolved to an IP address 
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Definiciones de API de aplicación auxiliar de proxy compatible con IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Extensiones IPv6 para el formato de archivo de configuración automática de navegador](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



