---
description: Resolver una cadena de host en su dirección IP
ms.assetid: 32d70f10-803b-484d-a9e0-d4c61a8d897f
title: dnsResolveEx función)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716646"
---
# <a name="dnsresolveex-function"></a><span data-ttu-id="7129a-103">dnsResolveEx función)</span><span class="sxs-lookup"><span data-stu-id="7129a-103">dnsResolveEx function</span></span>

<span data-ttu-id="7129a-104">Resolver una cadena de host en su dirección IP</span><span class="sxs-lookup"><span data-stu-id="7129a-104">Resolve a host string to its IP address</span></span>

## <a name="parameters"></a><span data-ttu-id="7129a-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7129a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7129a-106">*host*</span><span class="sxs-lookup"><span data-stu-id="7129a-106">*host*</span></span> 
</dt> <dd>

<span data-ttu-id="7129a-107">Cadena que contiene el host HTTP que se proporciona a FindProxyForUrl.</span><span class="sxs-lookup"><span data-stu-id="7129a-107">A string containing the HTTP host that is supplied to FindProxyForUrl.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7129a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7129a-108">Return value</span></span>

<span data-ttu-id="7129a-109">Cadena delimitada por signos de punto y coma que contiene direcciones IPv6 e IPv4, o una cadena vacía si el host no se pueda resolver.</span><span class="sxs-lookup"><span data-stu-id="7129a-109">A semi-colon delimited string containing IPv6 and IPv4 addresses or an empty string if host is not resolvable.</span></span>

## <a name="remarks"></a><span data-ttu-id="7129a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7129a-110">Remarks</span></span>

<span data-ttu-id="7129a-111">Los implementadores de FindProxyforURLEx deben agregar código que interrumpa la cadena de direcciones IP delimitadas por punto y coma en direcciones independientes.</span><span class="sxs-lookup"><span data-stu-id="7129a-111">FindProxyforURLEx implementers should add code that breaks the string of semi-colon delimited IP addresses into separate addresses.</span></span>

## <a name="examples"></a><span data-ttu-id="7129a-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7129a-112">Examples</span></span>

``` syntax
dnsResolveEx("testmachine1");
    returns the string "fe80::380c:2e71:f5b9:a3b5%15;fe80::982d:a3b3:97ad:7dd0%9;2001:4898:28:7:982d:a3b3:97ad:7dd0;2001:4898:28:7:adfe:a643:8130:2fdc;fe80::5efe:10.70.92.74%13;3ffe:8311:ffff:f70f:0:5efe:10.70.92.74;10.70.92.74;3ffe:831f:4136:e37e:380c:2e71
```

## <a name="see-also"></a><span data-ttu-id="7129a-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="7129a-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7129a-114">Definiciones de API de aplicación auxiliar de proxy compatible con IPv6</span><span class="sxs-lookup"><span data-stu-id="7129a-114">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="7129a-115">Extensiones IPv6 para el formato de archivo de configuración automática de navegador</span><span class="sxs-lookup"><span data-stu-id="7129a-115">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



