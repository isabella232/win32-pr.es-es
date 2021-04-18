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
# <a name="isresolvableex-function"></a><span data-ttu-id="8823d-103">isResolvableEx función)</span><span class="sxs-lookup"><span data-stu-id="8823d-103">isResolvableEx function</span></span>

<span data-ttu-id="8823d-104">Determina si una cadena de host determinada puede resolverse en una dirección IP.</span><span class="sxs-lookup"><span data-stu-id="8823d-104">Determines if a given host string can resolve to an IP address.</span></span>

## <a name="parameters"></a><span data-ttu-id="8823d-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8823d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8823d-106">*host*</span><span class="sxs-lookup"><span data-stu-id="8823d-106">*host*</span></span> 
</dt> <dd>

<span data-ttu-id="8823d-107">Cadena que contiene el host HTTP que se proporciona a FindProxyForUrl.</span><span class="sxs-lookup"><span data-stu-id="8823d-107">A string containing the HTTP host that is supplied to FindProxyForUrl.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8823d-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8823d-108">Return value</span></span>

<span data-ttu-id="8823d-109">TRUE si el host se va a resolver en una dirección IPv4 o IPv6; en caso contrario, FALSE.</span><span class="sxs-lookup"><span data-stu-id="8823d-109">TRUE if the host is resolvable to a IPv4 or IPv6 address; otherwise, FALSE.</span></span>

## <a name="examples"></a><span data-ttu-id="8823d-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8823d-110">Examples</span></span>

``` syntax
isResolvableEx(host);
    true if the hostname can be resolved to and IP address 
```

``` syntax
isResolvableEx(host); 
    false if the hostname cannot be resolved to an IP address 
```

## <a name="see-also"></a><span data-ttu-id="8823d-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="8823d-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8823d-112">Definiciones de API de aplicación auxiliar de proxy compatible con IPv6</span><span class="sxs-lookup"><span data-stu-id="8823d-112">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="8823d-113">Extensiones IPv6 para el formato de archivo de configuración automática de navegador</span><span class="sxs-lookup"><span data-stu-id="8823d-113">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



