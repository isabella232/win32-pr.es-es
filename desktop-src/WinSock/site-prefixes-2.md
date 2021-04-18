---
description: especifica un prefijo que está en el vínculo a la interfaz \# 4.
ms.assetid: cc3aa99d-cf45-460c-bdc1-3e9a19806fe4
title: Prefijos de sitio IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed8a21c59f9b6727c98ccb7fdacf4e9ec6ea5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715112"
---
# <a name="ipv6-site-prefixes"></a><span data-ttu-id="8f041-103">Prefijos de sitio IPv6</span><span class="sxs-lookup"><span data-stu-id="8f041-103">IPv6 Site Prefixes</span></span>

<span data-ttu-id="8f041-104">El comando RTU de IPv6 permite configurar prefijos en vínculo publicados con una longitud de prefijo de sitio.</span><span class="sxs-lookup"><span data-stu-id="8f041-104">The ipv6 rtu command allows published on-link prefixes to be configured with a site prefix length.</span></span> <span data-ttu-id="8f041-105">Si se especifica, la longitud del prefijo del sitio se coloca en una opción de información de prefijo en anuncios de enrutador.</span><span class="sxs-lookup"><span data-stu-id="8f041-105">If specified, the site prefix length is put into a prefix information option in router advertisements.</span></span> <span data-ttu-id="8f041-106">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8f041-106">For example:</span></span>

``` syntax
ipv6 rtu 2002:836b:9820:2::/64 4 pub life 1800 spl 48
```

<span data-ttu-id="8f041-107">especifica un prefijo que está en el vínculo a la interfaz \# 4.</span><span class="sxs-lookup"><span data-stu-id="8f041-107">specifies a prefix that is on-link to interface \#4.</span></span> <span data-ttu-id="8f041-108">El prefijo está publicado, lo que significa que se incluye en los anuncios de enrutador si la interfaz \# 4 es una interfaz de publicidad.</span><span class="sxs-lookup"><span data-stu-id="8f041-108">The prefix is published, meaning that it is included in router advertisements if interface \#4 is an advertising interface.</span></span> <span data-ttu-id="8f041-109">La duración de la opción de información de prefijo es de 1800 segundos (30 minutos).</span><span class="sxs-lookup"><span data-stu-id="8f041-109">The lifetime in the prefix information option is 1800 seconds (30 minutes).</span></span> <span data-ttu-id="8f041-110">La longitud del prefijo del sitio en la opción información de prefijo es 48.</span><span class="sxs-lookup"><span data-stu-id="8f041-110">The site prefix length in the prefix information option is 48.</span></span>

<span data-ttu-id="8f041-111">La recepción de una opción de información de prefijo que especifica un prefijo de sitio hace que se cree una entrada en la tabla de prefijos de sitio, que se puede mostrar mediante el comando de acceso a través de IPv6.</span><span class="sxs-lookup"><span data-stu-id="8f041-111">The receipt of a prefix information option that specifies a site prefix causes an entry to be created in the site prefix table, which can be displayed by using the ipv6 spt command.</span></span> <span data-ttu-id="8f041-112">La tabla de prefijos de sitio se usa para quitar las direcciones locales de sitio inadecuadas de las devueltas por [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) y las funciones relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8f041-112">The site prefix table is used to remove inappropriate site-local addresses from those returned by the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and related functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f041-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8f041-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f041-114">Dirección local de vínculo IPv6 y direcciones locales de sitio</span><span class="sxs-lookup"><span data-stu-id="8f041-114">IPv6 Link-local and Site-local Addresses</span></span>](link-local-and-site-local-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="8f041-115">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="8f041-115">Netsh.exe</span></span>](netsh-exe.md)
</dt> </dl>

 

 



