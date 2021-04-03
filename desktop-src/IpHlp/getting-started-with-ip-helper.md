---
description: A continuación se facilita una guía paso a paso para empezar a programar con la interfaz de programación de aplicaciones (API) auxiliar de IP. Está diseñado para proporcionar una descripción de las funciones básicas de la aplicación auxiliar de IP y las estructuras de datos, y de cómo funcionan conjuntamente.
ms.assetid: 3280d6cf-2741-40fe-8aa5-9f5be96d9fb8
title: Introducción con la aplicación auxiliar de IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 566ed4503c9bbafaee846aebf30c31993f7ce7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913686"
---
# <a name="getting-started-with-ip-helper"></a><span data-ttu-id="3af0d-104">Introducción con la aplicación auxiliar de IP</span><span class="sxs-lookup"><span data-stu-id="3af0d-104">Getting Started with IP Helper</span></span>

<span data-ttu-id="3af0d-105">A continuación se facilita una guía paso a paso para empezar a programar con la interfaz de programación de aplicaciones (API) auxiliar de IP.</span><span class="sxs-lookup"><span data-stu-id="3af0d-105">The following is a step-by-step guide to getting started programming using the IP Helper application programming interface (API).</span></span> <span data-ttu-id="3af0d-106">Está diseñado para proporcionar una descripción de las funciones básicas de la aplicación auxiliar de IP y las estructuras de datos, y de cómo funcionan conjuntamente.</span><span class="sxs-lookup"><span data-stu-id="3af0d-106">It is designed to provide an understanding of basic IP Helper functions and data structures, and how they work together.</span></span>

<span data-ttu-id="3af0d-107">La aplicación que se usa para la ilustración es una aplicación auxiliar de IP muy básica.</span><span class="sxs-lookup"><span data-stu-id="3af0d-107">The application that is used for illustration is a very basic IP Helper application.</span></span> <span data-ttu-id="3af0d-108">En los ejemplos incluidos en el kit de desarrollo de software (SDK) de Microsoft Windows se incluyen ejemplos de código más avanzados.</span><span class="sxs-lookup"><span data-stu-id="3af0d-108">More advanced code examples are included in the samples included with the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="3af0d-109">El primer paso es el mismo para la mayoría de las aplicaciones auxiliares de IP.</span><span class="sxs-lookup"><span data-stu-id="3af0d-109">The first step is the same for most IP Helper applications.</span></span>

-   [<span data-ttu-id="3af0d-110">Creación de una aplicación auxiliar de IP básica</span><span class="sxs-lookup"><span data-stu-id="3af0d-110">Creating a Basic IP Helper Application</span></span>](creating-a-basic-ip-helper-application.md)

<span data-ttu-id="3af0d-111">En las secciones siguientes se describen los pasos restantes para crear esta aplicación auxiliar de IP básica.</span><span class="sxs-lookup"><span data-stu-id="3af0d-111">The following sections describe the remaining steps for creating this basic IP Helper application.</span></span>

-   [<span data-ttu-id="3af0d-112">Recuperación de información mediante GetNetworkParams</span><span class="sxs-lookup"><span data-stu-id="3af0d-112">Retrieving Information Using GetNetworkParams</span></span>](retrieving-information-using-getnetworkparams.md)
-   [<span data-ttu-id="3af0d-113">Administración de adaptadores de red con GetAdaptersInfo</span><span class="sxs-lookup"><span data-stu-id="3af0d-113">Managing Network Adapters Using GetAdaptersInfo</span></span>](managing-network-adapters-using-getadaptersinfo.md)
-   [<span data-ttu-id="3af0d-114">Administrar interfaces mediante GetInterfaceInfo</span><span class="sxs-lookup"><span data-stu-id="3af0d-114">Managing Interfaces Using GetInterfaceInfo</span></span>](managing-interfaces-using-getinterfaceinfo.md)
-   [<span data-ttu-id="3af0d-115">Administración de direcciones IP mediante GetIpAddrTable</span><span class="sxs-lookup"><span data-stu-id="3af0d-115">Managing IP Addresses Using GetIpAddrTable</span></span>](managing-ip-addresses-using-getipaddrtable.md)
-   [<span data-ttu-id="3af0d-116">Administrar concesiones DHCP mediante IpReleaseAddress y IpRenewAddress</span><span class="sxs-lookup"><span data-stu-id="3af0d-116">Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress</span></span>](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)
-   [<span data-ttu-id="3af0d-117">Administración de direcciones IP mediante AddIPAddress y DeleteIPAddress</span><span class="sxs-lookup"><span data-stu-id="3af0d-117">Managing IP Addresses Using AddIPAddress and DeleteIPAddress</span></span>](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)
-   [<span data-ttu-id="3af0d-118">Recuperación de información mediante GetIpStatistics</span><span class="sxs-lookup"><span data-stu-id="3af0d-118">Retrieving Information Using GetIpStatistics</span></span>](retrieving-information-using-getipstatistics.md)
-   [<span data-ttu-id="3af0d-119">Recuperación de información mediante GetTcpStatistics</span><span class="sxs-lookup"><span data-stu-id="3af0d-119">Retrieving Information Using GetTcpStatistics</span></span>](retrieving-information-using-gettcpstatistics.md)

<span data-ttu-id="3af0d-120">El código fuente completo de este ejemplo de aplicación auxiliar de IP básica.</span><span class="sxs-lookup"><span data-stu-id="3af0d-120">The complete source code for this basic IP Helper example.</span></span>

-   [<span data-ttu-id="3af0d-121">Código fuente completo de la aplicación auxiliar IP</span><span class="sxs-lookup"><span data-stu-id="3af0d-121">Complete IP Helper Application Source Code</span></span>](complete-ip-helper-application-source-code.md)

## <a name="advanced-ip-helper-samples"></a><span data-ttu-id="3af0d-122">Ejemplos de aplicaciones auxiliares de IP avanzadas</span><span class="sxs-lookup"><span data-stu-id="3af0d-122">Advanced IP Helper Samples</span></span>

<span data-ttu-id="3af0d-123">En el kit de desarrollo de software (SDK) de Microsoft Windows se incluyen varios ejemplos de aplicación auxiliar de IP más avanzados.</span><span class="sxs-lookup"><span data-stu-id="3af0d-123">Several more advanced IP Helper samples are included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3af0d-124">De forma predeterminada, el Windows SDK publicado para Windows 7 en el siguiente directorio instala el código fuente de ejemplo de la aplicación auxiliar IP.</span><span class="sxs-lookup"><span data-stu-id="3af0d-124">By default, the IP Helper sample source code is installed by the Windows SDK released for Windows 7 in the following directory:</span></span>

<span data-ttu-id="3af0d-125">*C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ NetDs \\ IPHelp*</span><span class="sxs-lookup"><span data-stu-id="3af0d-125">*C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\NetDs\\IPHelp*</span></span>

<span data-ttu-id="3af0d-126">Los ejemplos más avanzados que se enumeran a continuación se encuentran en los siguientes directorios:</span><span class="sxs-lookup"><span data-stu-id="3af0d-126">The more advanced samples listed below are found in the following directories:</span></span>

-   <span data-ttu-id="3af0d-127">EnableRouter</span><span class="sxs-lookup"><span data-stu-id="3af0d-127">EnableRouter</span></span>

    <span data-ttu-id="3af0d-128">Este directorio contiene un ejemplo que muestra cómo usar las funciones auxiliares de IP [**EnableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) y [**UnenableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) para habilitar y deshabilitar el reenvío IPv4 en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="3af0d-128">This directory contains a sample that demonstrates how to use the [**EnableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) and [**UnenableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) IP Helper functions to enable and disable IPv4 forwarding on the local computer.</span></span>

-   <span data-ttu-id="3af0d-129">iparp</span><span class="sxs-lookup"><span data-stu-id="3af0d-129">iparp</span></span>

    <span data-ttu-id="3af0d-130">Este directorio contiene un programa de ejemplo que muestra cómo utilizar las funciones auxiliares de IP para mostrar y manipular entradas en la tabla ARP de IPv4 en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="3af0d-130">This directory contains a sample program that demonstrates how to use the IP Helper functions to display and manipulate entries in the IPv4 ARP table on the local computer.</span></span>

-   <span data-ttu-id="3af0d-131">ipchange</span><span class="sxs-lookup"><span data-stu-id="3af0d-131">ipchange</span></span>

    <span data-ttu-id="3af0d-132">Este directorio contiene un programa de ejemplo que muestra cómo usar las funciones auxiliares de IP para cambiar mediante programación una dirección IP para un adaptador de red específico de la máquina.</span><span class="sxs-lookup"><span data-stu-id="3af0d-132">This directory contains a sample program that demonstrates how to use IP Helper functions to programmatically change an IP address for a specific network adapter on your machine.</span></span> <span data-ttu-id="3af0d-133">Este programa también muestra cómo recuperar la información de configuración IP del adaptador de red existente.</span><span class="sxs-lookup"><span data-stu-id="3af0d-133">This program also demonstrates how to retrieve existing network adapter IP configuration information.</span></span>

-   <span data-ttu-id="3af0d-134">IPConfig</span><span class="sxs-lookup"><span data-stu-id="3af0d-134">IPConfig</span></span>

    <span data-ttu-id="3af0d-135">Este directorio contiene un programa de ejemplo que muestra cómo recuperar mediante programación la información de configuración de IPv4 similar a la utilidad IPCONFIG.EXE.</span><span class="sxs-lookup"><span data-stu-id="3af0d-135">This directory contains a sample program that demonstrates how to programmatically retrieve IPv4 configuration information similar to the IPCONFIG.EXE utility.</span></span> <span data-ttu-id="3af0d-136">Muestra cómo usar las funciones [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) y [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) .</span><span class="sxs-lookup"><span data-stu-id="3af0d-136">It demonstrates how to use the [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) and [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) functions.</span></span> <span data-ttu-id="3af0d-137">Tenga en cuenta que la función **GetAdaptersInfo** solo recupera información de IPv4.</span><span class="sxs-lookup"><span data-stu-id="3af0d-137">Note that the **GetAdaptersInfo** function only retrieves IPv4 information.</span></span>

-   <span data-ttu-id="3af0d-138">IPRenew</span><span class="sxs-lookup"><span data-stu-id="3af0d-138">IPRenew</span></span>

    <span data-ttu-id="3af0d-139">Este directorio contiene un programa de ejemplo que muestra cómo liberar y renovar mediante programación las direcciones IPv4 obtenidas a través de DHCP.</span><span class="sxs-lookup"><span data-stu-id="3af0d-139">This directory contains a sample program that demonstrates how to programmatically release and renew IPv4 addresses obtained through DHCP.</span></span> <span data-ttu-id="3af0d-140">Este programa también muestra cómo recuperar la información de configuración del adaptador de red existente.</span><span class="sxs-lookup"><span data-stu-id="3af0d-140">This program also demonstrates how to retrieve existing network adapter configuration information.</span></span>

-   <span data-ttu-id="3af0d-141">IPRoute</span><span class="sxs-lookup"><span data-stu-id="3af0d-141">IPRoute</span></span>

    <span data-ttu-id="3af0d-142">Este directorio contiene un programa de ejemplo que muestra cómo utilizar las funciones auxiliares de IP para manipular la tabla de enrutamiento de IPv4.</span><span class="sxs-lookup"><span data-stu-id="3af0d-142">This directory contains a sample program that demonstrates how to use the IP Helper functions to manipulate the IPv4 routing table.</span></span>

-   <span data-ttu-id="3af0d-143">ipstat</span><span class="sxs-lookup"><span data-stu-id="3af0d-143">ipstat</span></span>

    <span data-ttu-id="3af0d-144">Este directorio contiene un programa de ejemplo que muestra cómo utilizar las funciones auxiliares de IP para mostrar las conexiones IPv4 para un protocolo.</span><span class="sxs-lookup"><span data-stu-id="3af0d-144">This directory contains a sample program that demonstrates how to use the IP Helper functions to show IPv4 connections for a protocol.</span></span> <span data-ttu-id="3af0d-145">De forma predeterminada, las estadísticas se muestran para IP, ICMP, TCP y UDP.</span><span class="sxs-lookup"><span data-stu-id="3af0d-145">By default, statistics are shown for IP, ICMP, TCP and UDP.</span></span>

-   <span data-ttu-id="3af0d-146">Netinfo</span><span class="sxs-lookup"><span data-stu-id="3af0d-146">Netinfo</span></span>

    <span data-ttu-id="3af0d-147">Este directorio contiene un programa de ejemplo que muestra cómo usar las nuevas API auxiliares de IP introducidas en Windows Vista y versiones posteriores para mostrar o cambiar la información de dirección e interfaz para IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="3af0d-147">This directory contains a sample program that demonstrates how to the use the new IP Helper APIs introduced on Windows Vista and later to display/change address and interface information for IPv4 and IPv6.</span></span>

 

 



