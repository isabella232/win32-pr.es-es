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
# <a name="isinnetex-function"></a><span data-ttu-id="346b8-103">isInNetEx función)</span><span class="sxs-lookup"><span data-stu-id="346b8-103">isInNetEx function</span></span>

<span data-ttu-id="346b8-104">Determina si una dirección IP se encuentra en una subred específica.</span><span class="sxs-lookup"><span data-stu-id="346b8-104">Determines if an IP address is in a specific subnet.</span></span>

## <a name="parameters"></a><span data-ttu-id="346b8-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="346b8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="346b8-106">*DirIP*</span><span class="sxs-lookup"><span data-stu-id="346b8-106">*IPaddress*</span></span> 
</dt> <dd>

<span data-ttu-id="346b8-107">Una cadena que contiene direcciones IPv6/IPv4.</span><span class="sxs-lookup"><span data-stu-id="346b8-107">A string containing IPv6/IPv4 addresses.</span></span>

</dd> <dt>

<span data-ttu-id="346b8-108">*IPprefix*</span><span class="sxs-lookup"><span data-stu-id="346b8-108">*IPprefix*</span></span> 
</dt> <dd>

<span data-ttu-id="346b8-109">Cadena que contiene el prefijo de IP delimitado por dos puntos con los n bits superiores especificados en el campo de bits (es decir, 3ffe: 8311: ffff::/48 o 123.112.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="346b8-109">A string containing colon delimited IP prefix with top n bits specified in the bit field (i.e. 3ffe:8311:ffff::/48 or 123.112.0.0/16).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="346b8-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="346b8-110">Return value</span></span>

<span data-ttu-id="346b8-111">TRUE si el host está en la misma subred; en caso contrario, FALSE.</span><span class="sxs-lookup"><span data-stu-id="346b8-111">TRUE if the host is in the same subnet; otherwise, FALSE.</span></span>

<span data-ttu-id="346b8-112">También devuelve FALSE si el prefijo no tiene el formato correcto o si se usan direcciones y prefijos de tipos diferentes en la comparación (es decir, el prefijo IPv4 y una dirección IPv6).</span><span class="sxs-lookup"><span data-stu-id="346b8-112">Also returns FALSE if the prefix is not in the correct format or if addresses and prefixes of different types are used in the comparison (i.e. IPv4 prefix and an IPv6 address).</span></span>

## <a name="examples"></a><span data-ttu-id="346b8-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="346b8-113">Examples</span></span>

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

## <a name="see-also"></a><span data-ttu-id="346b8-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="346b8-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="346b8-115">Definiciones de API de aplicación auxiliar de proxy compatible con IPv6</span><span class="sxs-lookup"><span data-stu-id="346b8-115">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="346b8-116">Extensiones IPv6 para el formato de archivo de configuración automática de navegador</span><span class="sxs-lookup"><span data-stu-id="346b8-116">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



