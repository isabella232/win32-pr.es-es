---
description: Con el fin de aprovechar las funciones habilitadas para IPv6, los administradores de TI deben definir dentro de su script WPAD, una función llamada FindProxyForURLEx (URL, host) que reemplazará la función FindProxyForUrl (URL, host) heredada.
ms.assetid: e531a66d-5c50-4065-a12a-783fd4d1d310
title: IPv6-Aware definiciones de API de aplicación auxiliar de proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b1ff5a0c287327593e65e29a0b03cfb59269f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688311"
---
# <a name="ipv6-aware-proxy-helper-api-definitions"></a><span data-ttu-id="920be-103">IPv6-Aware definiciones de API de aplicación auxiliar de proxy</span><span class="sxs-lookup"><span data-stu-id="920be-103">IPv6-Aware Proxy Helper API Definitions</span></span>

<span data-ttu-id="920be-104">Con el fin de aprovechar las funciones habilitadas para IPv6, los administradores de TI deben definir dentro de su script WPAD, una función llamada FindProxyForURLEx (URL, host) que reemplazará la función FindProxyForUrl (URL, host) heredada.</span><span class="sxs-lookup"><span data-stu-id="920be-104">In order to take advantage of the IPv6 enabled functions, IT administrators must define within their WPAD script, a function called FindProxyForURLEx (url, host) which will replace the legacy FindProxyForUrl (url, host) function.</span></span> <span data-ttu-id="920be-105">Solo los administradores podrán ejecutar las nuevas funciones desde la nueva función FindProxyForURLEx.</span><span class="sxs-lookup"><span data-stu-id="920be-105">Only from the new FindProxyForURLEx function will administrators be able to execute the new functions.</span></span>

<span data-ttu-id="920be-106">También intentamos simplificar el trabajo de los desarrolladores, mediante la alineación de las funciones para que devuelvan diferentes tipos de direcciones IP en el mismo orden de preferencia que otros componentes de red, específicamente direcciones IPv6 seguidas de direcciones IPv4 (es decir, el comportamiento actual de la función función getaddrinfo (..) de Winsock).</span><span class="sxs-lookup"><span data-stu-id="920be-106">We also attempted to simplify work for developers, by aligning our functions to return different types of IP addresses in the same order of preference as other networking components, specifically IPv6 addresses followed by IPv4 addresses (i.e. current behavior for Winsock’s getaddrinfo(..) function).</span></span>

<span data-ttu-id="920be-107">Las siguientes funciones son extensiones de la [especificación de formato de archivo de configuración automática de proxy (PAC) de navegador](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html) para permitir que los scripts de WPAD controlen las redes compatibles con IPv6.</span><span class="sxs-lookup"><span data-stu-id="920be-107">The following functions are extensions to the [Navigator Proxy Auto-Config (PAC) File Format specification](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html) to enable WPAD scripts to handle IPv6 capable networks.</span></span>

## <a name="predefined-functions-and-environment-for-the-javascript-function-findproxyforurlex"></a><span data-ttu-id="920be-108">Funciones y entorno predefinidos para la función de JavaScript FindProxyforURLEx</span><span class="sxs-lookup"><span data-stu-id="920be-108">Predefined Functions and Environment for the JavaScript Function FindProxyforURLEx</span></span>

<span data-ttu-id="920be-109">Condiciones basadas en el nombre de host</span><span class="sxs-lookup"><span data-stu-id="920be-109">Hostname based conditions</span></span>

<dl> <dt>

[<span data-ttu-id="920be-110">**isResolvableEx**</span><span class="sxs-lookup"><span data-stu-id="920be-110">**isResolvableEx**</span></span>](isresolvableex.md)
</dt> <dd>

<span data-ttu-id="920be-111">Determina si una cadena de host determinada puede resolverse en una dirección IP.</span><span class="sxs-lookup"><span data-stu-id="920be-111">Determines if a given host string can resolve to an IP address.</span></span>

</dd> <dt>

[<span data-ttu-id="920be-112">**isInNetEx**</span><span class="sxs-lookup"><span data-stu-id="920be-112">**isInNetEx**</span></span>](isinnetex.md)
</dt> <dd>

<span data-ttu-id="920be-113">Determina si una dirección IP se encuentra en una subred específica.</span><span class="sxs-lookup"><span data-stu-id="920be-113">Determines if an IP address is in a specific subnet.</span></span>

</dd> </dl>

<span data-ttu-id="920be-114">Funciones de utilidad relacionadas</span><span class="sxs-lookup"><span data-stu-id="920be-114">Related utility functions</span></span>

<dl> <dt>

[<span data-ttu-id="920be-115">**dnsResolveEx**</span><span class="sxs-lookup"><span data-stu-id="920be-115">**dnsResolveEx**</span></span>](dnsresolveex.md)
</dt> <dd>

<span data-ttu-id="920be-116">Resuelva una cadena de host en su dirección IP.</span><span class="sxs-lookup"><span data-stu-id="920be-116">Resolve a host string to its IP address.</span></span>

</dd> <dt>

[<span data-ttu-id="920be-117">**myIPAddressEx**</span><span class="sxs-lookup"><span data-stu-id="920be-117">**myIPAddressEx**</span></span>](myipaddressex.md)
</dt> <dd>

<span data-ttu-id="920be-118">Busca todas las direcciones IP del host local.</span><span class="sxs-lookup"><span data-stu-id="920be-118">Finds all the IP addresses for localhost.</span></span>

</dd> <dt>

[<span data-ttu-id="920be-119">**sortIpAddressList**</span><span class="sxs-lookup"><span data-stu-id="920be-119">**sortIpAddressList**</span></span>](sortipaddresslist.md)
</dt> <dd>

<span data-ttu-id="920be-120">Ordena una lista de direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="920be-120">Sorts a list of IP addresses.</span></span>

</dd> <dt>

[<span data-ttu-id="920be-121">**getClientVersion**</span><span class="sxs-lookup"><span data-stu-id="920be-121">**getClientVersion**</span></span>](getclientversion.md)
</dt> <dd>

<span data-ttu-id="920be-122">Obtiene la versión del motor de procesamiento WPAD.</span><span class="sxs-lookup"><span data-stu-id="920be-122">Gets the version of the WPAD processing engine.</span></span>

</dd> </dl>

> [!Note]  
> <span data-ttu-id="920be-123">Esta funcionalidad requiere Windows Internet Explorer 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="920be-123">This functionality requires Windows Internet Explorer 7 or greater.</span></span>

 

 

 



