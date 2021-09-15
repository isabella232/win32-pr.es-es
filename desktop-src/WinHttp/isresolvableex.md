---
description: Determina si una cadena de host determinada puede resolverse en una dirección IP.
ms.assetid: 83e52ca7-2ea0-419d-b09d-9301c1982b98
title: Función isResolvableEx
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360548"
---
# <a name="isresolvableex-function"></a>Función isResolvableEx

Determina si una cadena de host determinada puede resolverse en una dirección IP.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*host* 
</dt> <dd>

Cadena que contiene el host HTTP proporcionado a FindProxyForUrl.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

TRUE si el host se puede resolver en una dirección IPv4 o IPv6; de lo contrario, FALSE.

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

[Definiciones de API auxiliares de proxy compatibles con IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Extensiones IPv6 para el formato de archivo de configuración automática del navegador](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



