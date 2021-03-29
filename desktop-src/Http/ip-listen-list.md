---
title: Lista de escucha de IP
description: Las API de servidor HTTP no se enlazan a ninguna dirección IP ni a pares de puertos TCP hasta que un usuario registra un UrlPrefix.
ms.assetid: f2f51e6c-9114-4ba9-a37c-1d1d1f0b444f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba085112c800d7845c76467c4dd2fdc3f5f0b00a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994552"
---
# <a name="ip-listen-list"></a><span data-ttu-id="832f2-103">Lista de escucha de IP</span><span class="sxs-lookup"><span data-stu-id="832f2-103">IP Listen List</span></span>

<span data-ttu-id="832f2-104">Las API de servidor HTTP no se enlazan a ninguna dirección IP ni a pares de puertos TCP hasta que un usuario registra un UrlPrefix.</span><span class="sxs-lookup"><span data-stu-id="832f2-104">The HTTP Server APIs do not bind to any IP address and TCP port pairs until a user registers a UrlPrefix.</span></span> <span data-ttu-id="832f2-105">De forma predeterminada, una vez que se escribe un registro en la cola de solicitudes, la API del servidor HTTP enlaza con el puerto especificado en el UrlPrefix (por ejemplo, el puerto 80) para todas las direcciones IP (inaddress \_ any o INADDR6 \_ any) disponibles en la máquina.</span><span class="sxs-lookup"><span data-stu-id="832f2-105">By default, once a registration is entered in the request queue, the HTTP Server API binds to the port specified in the UrlPrefix (for example port 80) for all IP addresses (INADDR\_ANY or INADDR6\_ANY) available on the machine.</span></span> <span data-ttu-id="832f2-106">Los problemas surgen cuando las aplicaciones de terceros (que no usan las API de servidor HTTP) se enlazan a los pares de dirección IP y puerto 80 en la máquina.</span><span class="sxs-lookup"><span data-stu-id="832f2-106">Problems arise when third party applications (not using the HTTP Server APIs) bind to IP address and port 80 pairs on the machine.</span></span> <span data-ttu-id="832f2-107">La API del servidor HTTP proporciona una manera de configurar la lista de direcciones IP que enlaza y resuelve este problema de coexistencia.</span><span class="sxs-lookup"><span data-stu-id="832f2-107">The HTTP Server API provides a way to configure the list of IP addresses that it binds and solves this coexistence issue.</span></span> <span data-ttu-id="832f2-108">El administrador del sistema llama a la función [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) con el parámetro *ConfigId* establecido en el valor HttpServiceConfigIPListenList para especificar la lista de escucha de IP.</span><span class="sxs-lookup"><span data-stu-id="832f2-108">The system administrator calls the [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) function with the *ConfigId* parameter set to the HttpServiceConfigIPListenList value to specify the IP listen list.</span></span> <span data-ttu-id="832f2-109">Las direcciones IPv4 e IPv6 se pueden agregar a la lista.</span><span class="sxs-lookup"><span data-stu-id="832f2-109">Both IPv4 and IPv6 addresses can be added to the list.</span></span> <span data-ttu-id="832f2-110">Las direcciones IP especificadas se aplican a todas las aplicaciones del equipo mediante la API del servidor HTTP y se conservan a lo largo de los reinicios de la máquina.</span><span class="sxs-lookup"><span data-stu-id="832f2-110">The IP addresses entered apply to all applications on the machine using the HTTP Server API and persist across reboots of the machine.</span></span> <span data-ttu-id="832f2-111">Sin embargo, los cambios en la configuración de la lista de escucha de IP no tienen lugar de forma dinámica. en la mayoría de los casos, es posible que sea necesario reiniciar el sistema.</span><span class="sxs-lookup"><span data-stu-id="832f2-111">However, any changes to the IP listen list configuration do not take place dynamically; in most cases, a system reboot may be necessary.</span></span>

 

 




