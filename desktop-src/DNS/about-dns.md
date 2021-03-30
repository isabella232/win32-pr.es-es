---
title: Acerca de DNS
description: El sistema de nombres de dominio (DNS) es un protocolo estándar del sector que se usa para buscar equipos en una red basada en IP. Los usuarios pueden recordar nombres para mostrar, como www.microsoft.com más fácilmente que las direcciones basadas en números, como 207.46.131.137.
ms.assetid: 3a899ba4-4338-4119-aa68-a969d196c4f5
keywords:
- Acerca del DNS del sistema de nombres de dominio
- Sistema de nombres de dominio DNS, acerca de
- DNS del sistema de nombres de dominio, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98573e72db645d96c263efd479135807274c18a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104280212"
---
# <a name="about-dns"></a><span data-ttu-id="45db4-107">Acerca de DNS</span><span class="sxs-lookup"><span data-stu-id="45db4-107">About DNS</span></span>

<span data-ttu-id="45db4-108">El sistema de nombres de dominio (DNS) es un protocolo estándar del sector que se usa para buscar equipos en una red basada en IP.</span><span class="sxs-lookup"><span data-stu-id="45db4-108">Domain Name System (DNS) is an industry-standard protocol used to locate computers on an IP-based network.</span></span> <span data-ttu-id="45db4-109">Los usuarios pueden recordar los nombres para mostrar, como `www.microsoft.com` más sencillo que las direcciones basadas en números, como 207.46.131.137.</span><span class="sxs-lookup"><span data-stu-id="45db4-109">Users can remember display names, such as `www.microsoft.com` easier than number-based addresses, such as 207.46.131.137.</span></span>

<span data-ttu-id="45db4-110">Las redes IP, como las redes de Internet y Windows, dependen de direcciones basadas en números para transmitir datos a través de la red. por lo tanto, es necesario traducir los nombres para mostrar (como `www.microsoft.com` ) en direcciones numéricas que la red pueda reconocer (como 207.46.131.137).</span><span class="sxs-lookup"><span data-stu-id="45db4-110">IP networks, such as the Internet and Windows networks, rely on number-based addresses to transmit data throughout the network; therefore, it is necessary to translate display names (such as `www.microsoft.com`) into numeric addresses that the network can recognize (such as 207.46.131.137).</span></span> <span data-ttu-id="45db4-111">DNS es el servicio preferido en Windows para localizar estos recursos y traducirlos en direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="45db4-111">DNS is the service of choice in Windows to locate such resources and translate them into IP addresses.</span></span>

<span data-ttu-id="45db4-112">DNS es el servicio de localizador principal para Active Directory y, por tanto, el DNS se puede considerar como un servicio base para Windows y para Active Directory.</span><span class="sxs-lookup"><span data-stu-id="45db4-112">DNS is the primary locator service for Active Directory, and therefore, DNS can be considered a base service for both Windows and Active Directory.</span></span> <span data-ttu-id="45db4-113">Windows proporciona funciones que permiten a los programadores de aplicaciones usar funciones de DNS, como la realización de consultas de DNS mediante programación, la comparación de registros y la búsqueda de nombres.</span><span class="sxs-lookup"><span data-stu-id="45db4-113">Windows provides functions that enable application programmers to use DNS functions such as programmatically making DNS queries, comparing records, and looking up names.</span></span>

<span data-ttu-id="45db4-114">Muchas funciones de DNS son realmente tipos de función, en que hay un nombre base para la función, pero su uso depende de la codificación de caracteres.</span><span class="sxs-lookup"><span data-stu-id="45db4-114">Many DNS functions are actually function types, in that there is a base name for the function, but its use depends on character encoding.</span></span> <span data-ttu-id="45db4-115">Por ejemplo, la función [**dnsquery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) aparece en la referencia de funciones de la interfaz de programación de aplicaciones (API) DNS como **DnsQuery**. pero su uso en las aplicaciones depende de si la codificación de caracteres es ANSI (designada mediante la anexión de \_ un al nombre de tipo de función), Unicode (designado mediante anexando \_ W al nombre de tipo de función) o UTF-8 (designado mediante la anexión de \_ UTF al nombre de tipo de función).</span><span class="sxs-lookup"><span data-stu-id="45db4-115">For example, the [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) function is listed in the function reference of the DNS Application Programming Interface (API) as **DnsQuery**, but its use in applications depends on whether the character encoding is ANSI (designated by appending \_A to the function type name), Unicode (designated by appending \_W to the function type name), or UTF-8 (designated by appending \_UTF to the function type name).</span></span> <span data-ttu-id="45db4-116">Por lo tanto, la llamada de función para la función **DnsQuery** sería realmente una de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="45db4-116">Therefore, the function call for the **DnsQuery** function would actually be one of the following:</span></span>

<span data-ttu-id="45db4-117">DnsQuery \_ a ( \_ para la codificación ANSI)</span><span class="sxs-lookup"><span data-stu-id="45db4-117">DnsQuery\_A (\_A for ANSI encoding)</span></span>

<span data-ttu-id="45db4-118">DnsQuery \_ w ( \_ w para codificación Unicode)</span><span class="sxs-lookup"><span data-stu-id="45db4-118">DnsQuery\_W (\_W for Unicode encoding)</span></span>

<span data-ttu-id="45db4-119">DnsQuery \_ UTF8 ( \_ UTF8 para la codificación UTF-8)</span><span class="sxs-lookup"><span data-stu-id="45db4-119">DnsQuery\_UTF8 (\_UTF8 for UTF-8 encoding)</span></span>

<span data-ttu-id="45db4-120">Todas las funciones que requieren esta Convención indican claramente este requisito en las primeras oraciones de la definición de función.</span><span class="sxs-lookup"><span data-stu-id="45db4-120">All functions that require this convention clearly state this requirement within the first few sentences of their function definition.</span></span> <span data-ttu-id="45db4-121">Use el nombre de función adecuado; por ejemplo, no puede llamar simplemente a [**dnsquery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) en lugar de a dnsquery \_ a.</span><span class="sxs-lookup"><span data-stu-id="45db4-121">Use the proper function name; for example, you cannot simply call [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) instead of DnsQuery\_A.</span></span>

 

 




