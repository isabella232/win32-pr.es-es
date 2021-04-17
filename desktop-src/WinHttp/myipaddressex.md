---
description: Busca todas las direcciones IP del host local.
ms.assetid: 47f7d03e-c1a1-4395-9889-01891208fe0f
title: myIPAddressEx función)
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
ms.openlocfilehash: 88c205dbd5ce071a809cf87f4f97bb6d42120dcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706610"
---
# <a name="myipaddressex-function"></a><span data-ttu-id="59d4b-103">myIPAddressEx función)</span><span class="sxs-lookup"><span data-stu-id="59d4b-103">myIPAddressEx function</span></span>

<span data-ttu-id="59d4b-104">Busca todas las direcciones IP del host local.</span><span class="sxs-lookup"><span data-stu-id="59d4b-104">Finds all the IP addresses for localhost.</span></span>

## <a name="parameters"></a><span data-ttu-id="59d4b-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59d4b-105">Parameters</span></span>

<span data-ttu-id="59d4b-106">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="59d4b-106">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59d4b-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59d4b-107">Return value</span></span>

<span data-ttu-id="59d4b-108">Una cadena delimitada por punto y coma que contiene todas las direcciones IP para localhost (IPv6 o IPv4) o una cadena vacía si no puede resolver localhost en una dirección IP.</span><span class="sxs-lookup"><span data-stu-id="59d4b-108">A semi-colon delimited string containing all IP addresses for localhost (IPv6 and/or IPv4), or an empty string if unable to resolve localhost to an IP address.</span></span>

## <a name="remarks"></a><span data-ttu-id="59d4b-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59d4b-109">Remarks</span></span>

<span data-ttu-id="59d4b-110">Los implementadores de FindProxyforURLEx deben agregar código que interrumpa la cadena de direcciones IP delimitadas por punto y coma en direcciones independientes.</span><span class="sxs-lookup"><span data-stu-id="59d4b-110">FindProxyforURLEx implementers should add code that breaks the string of semi-colon delimited IP addresses into separate addresses.</span></span>

## <a name="examples"></a><span data-ttu-id="59d4b-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="59d4b-111">Examples</span></span>

``` syntax
myIpAddressEx();
    would return the string "fe80::380c:2e71:f5b9:a3b5%15;fe80::982d:a3b3:97ad:7dd0%9;2001:4898:28:7:982d:a3b3:97ad:7dd0;2001:4898:28:7:adfe:a643:8130:2fdc;fe80::5efe:10.70.92.74%13;3ffe:8311:ffff:f70f:0:5efe:10.70.92.74;10.70.92.74;3ffe:831f:4136:e37e:380c:2e71:f5b9:a3b5" 
    if you were running on that host.
```

## <a name="see-also"></a><span data-ttu-id="59d4b-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="59d4b-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59d4b-113">Definiciones de API de aplicación auxiliar de proxy compatible con IPv6</span><span class="sxs-lookup"><span data-stu-id="59d4b-113">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="59d4b-114">Extensiones IPv6 para el formato de archivo de configuración automática de navegador</span><span class="sxs-lookup"><span data-stu-id="59d4b-114">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



