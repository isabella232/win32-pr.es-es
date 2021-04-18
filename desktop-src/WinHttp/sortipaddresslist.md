---
description: Ordena una lista de direcciones IP.
ms.assetid: 1266d6f3-e9f5-4e6b-9431-7329df156f0a
title: sortIpAddressList función)
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
ms.openlocfilehash: 600d87a58248aafdef5b0a8a7f284f4094c95780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714957"
---
# <a name="sortipaddresslist-function"></a><span data-ttu-id="4051a-103">sortIpAddressList función)</span><span class="sxs-lookup"><span data-stu-id="4051a-103">sortIpAddressList function</span></span>

<span data-ttu-id="4051a-104">Ordena una lista de direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="4051a-104">Sorts a list of IP addresses.</span></span>

## <a name="parameters"></a><span data-ttu-id="4051a-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4051a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4051a-106">*IpAddressList*</span><span class="sxs-lookup"><span data-stu-id="4051a-106">*IpAddressList*</span></span> 
</dt> <dd>

<span data-ttu-id="4051a-107">Cadena delimitada por signos de punto y coma que contiene direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="4051a-107">A semi-colon delimited string containing IP addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4051a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4051a-108">Return value</span></span>

<span data-ttu-id="4051a-109">Una lista de direcciones IP delimitadas por punto y coma ordenadas o una cadena vacía si no se puede ordenar la lista de direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="4051a-109">A list of sorted semi-colon delimited IP addresses or an empty string if unable to sort the IP Address list.</span></span>

## <a name="remarks"></a><span data-ttu-id="4051a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4051a-110">Remarks</span></span>

<span data-ttu-id="4051a-111">Los implementadores de FindProxyforURLEx deben agregar código que interrumpa la cadena de direcciones IP delimitadas por punto y coma en direcciones independientes.</span><span class="sxs-lookup"><span data-stu-id="4051a-111">FindProxyforURLEx implementers should add code that breaks the string of semi-colon delimited IP addresses into separate addresses.</span></span>

## <a name="examples"></a><span data-ttu-id="4051a-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4051a-112">Examples</span></span>

``` syntax
sortIpAddressList(2001:4898:28:3:201:2ff:feea:fc14; 
                  157.59.139.22; 
                  fe80::5efe:157.59.139.22");
    returns "fe80::5efe:157.59.139.22;2001:4898:28:3:201:2ff:feea:fc14;157.59.139.22" 
    A list of sorted IP addresses. If there both IPv6 and IPv4 IP addresses are passed as input to this function, then the sorted IPv6 addresses are followed by sorted IPv4 addresses
```

## <a name="see-also"></a><span data-ttu-id="4051a-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="4051a-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4051a-114">Definiciones de API de aplicación auxiliar de proxy compatible con IPv6</span><span class="sxs-lookup"><span data-stu-id="4051a-114">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="4051a-115">Extensiones IPv6 para el formato de archivo de configuración automática de navegador</span><span class="sxs-lookup"><span data-stu-id="4051a-115">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



