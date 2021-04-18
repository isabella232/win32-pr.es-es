---
description: Determina si una dirección IP se encuentra en una subred específica.
ms.assetid: 2fbfad9c-86b1-44c3-860b-a5c98ac6c2e9
title: isInNetEx función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isInNetEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: d738fbf5788fbe56d8c801b6c5256e96e8d4a6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706987"
---
# <a name="isinnetex-function"></a>isInNetEx función)

Determina si una dirección IP se encuentra en una subred específica.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*DirIP* 
</dt> <dd>

Una cadena que contiene direcciones IPv6/IPv4.

</dd> <dt>

*IPprefix* 
</dt> <dd>

Cadena que contiene el prefijo de IP delimitado por dos puntos con los n bits superiores especificados en el campo de bits (es decir, 3ffe: 8311: ffff::/48 o 123.112.0.0/16).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

TRUE si el host está en la misma subred; en caso contrario, FALSE.

También devuelve FALSE si el prefijo no tiene el formato correcto o si se usan direcciones y prefijos de tipos diferentes en la comparación (es decir, el prefijo IPv4 y una dirección IPv6).

## <a name="examples"></a>Ejemplos

``` syntax
isInNetEx(host, "198.95.249.79/32");
    true if the IP address of host matches exactly 198.95.249.79
```

``` syntax
isInNetEx(host, "198.95.0.0/16");
    true if the IP address of the host matches 198.95.*.*
```

``` syntax
isInNetEx(host, "3ffe:8311:ffff::/48");
    true if the IP address of the host matches 3ffe:8311:fff:*:*:*:*:*
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Definiciones de API de aplicación auxiliar de proxy compatible con IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Extensiones IPv6 para el formato de archivo de configuración automática de navegador](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



