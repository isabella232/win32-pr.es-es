---
description: Monitor de red de Microsoft 3 (Netmon) es un analizador de paquetes que se utiliza para inspeccionar el tráfico de red.
ms.assetid: 015a6a6d-9e07-4f22-b931-dcce77051bef
title: Descarga de los filtros Netmon y DPWS de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47790b26164ec0ed2792d1d1e1f2ad4ba5d77d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696912"
---
# <a name="downloading-netmon-and-sample-dpws-filters"></a><span data-ttu-id="f8fa9-103">Descarga de los filtros Netmon y DPWS de ejemplo</span><span class="sxs-lookup"><span data-stu-id="f8fa9-103">Downloading Netmon and Sample DPWS Filters</span></span>

<span data-ttu-id="f8fa9-104">Monitor de red de Microsoft 3 (Netmon) es un analizador de paquetes que se utiliza para inspeccionar el tráfico de red.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-104">Microsoft Network Monitor 3 (Netmon) is a packet analyzer used to inspect network traffic.</span></span> <span data-ttu-id="f8fa9-105">Se debe descargar Netmon antes de seguir los pasos de solución de problemas que se indican en [inspeccionar seguimientos de red para UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) e [inspeccionar los seguimientos de red para el intercambio de metadatos http](inspecting-network-traces-for-http-metadata-exchange.md) .</span><span class="sxs-lookup"><span data-stu-id="f8fa9-105">Netmon must be downloaded before the troubleshooting steps given in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) and [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md) can be followed.</span></span> <span data-ttu-id="f8fa9-106">Una vez descargado Netmon, se pueden usar filtros de DPWS para ayudar a aislar el tráfico de interés.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-106">After Netmon has been downloaded, DPWS filters can be used to help isolate traffic of interest.</span></span>

## <a name="downloading-netmon"></a><span data-ttu-id="f8fa9-107">Descarga de Netmon</span><span class="sxs-lookup"><span data-stu-id="f8fa9-107">Downloading Netmon</span></span>

<span data-ttu-id="f8fa9-108">Para descargar Netmon, vaya a [monitor de red de Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) y siga las instrucciones.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-108">To download Netmon, go to [Microsoft Network Monitor](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) and follow the instructions.</span></span> <span data-ttu-id="f8fa9-109">Para obtener más información acerca de Netmon, vea "información acerca de Monitor de red 3,0" en la Knowledge base de ayuda y soporte técnico en [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .</span><span class="sxs-lookup"><span data-stu-id="f8fa9-109">For more information about Netmon, see "Information about Network Monitor 3.0" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741).</span></span>

## <a name="sample-dpws-filters"></a><span data-ttu-id="f8fa9-110">Filtros de DPWS de ejemplo</span><span class="sxs-lookup"><span data-stu-id="f8fa9-110">Sample DPWS Filters</span></span>

<span data-ttu-id="f8fa9-111">En ocasiones, la solución de problemas de WS-Discovery y de intercambio de metadatos debe realizarse en una red ocupada.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-111">Sometimes, WS-Discovery and metadata exchange troubleshooting must take place on a busy network.</span></span> <span data-ttu-id="f8fa9-112">Los filtros de ejemplo se pueden usar para limitar el resultado de Netmon al tráfico de interés.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-112">The sample filters can be used to help limit the Netmon output to traffic of interest.</span></span> <span data-ttu-id="f8fa9-113">Para obtener más información acerca del uso de filtros de Netmon, vea [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .</span><span class="sxs-lookup"><span data-stu-id="f8fa9-113">For more information about using Netmon filters, see [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741).</span></span>

<span data-ttu-id="f8fa9-114">En el ejemplo siguiente se muestra un filtro que limita la salida a todo el tráfico de WS-Discovery de difusión.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-114">The following example shows a filter that limits output to all broadcast WS-Discovery traffic.</span></span>

> [!Note]  
> <span data-ttu-id="f8fa9-115">Este filtro no captura el tráfico de pilas que no responden a los mensajes de multidifusión WS-Discovery que se originan en el puerto 3702.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-115">This filter does not capture traffic from stacks that do not respond to multicast WS-Discovery messages that originate at port 3702.</span></span> <span data-ttu-id="f8fa9-116">Si se utiliza una pila de este tipo, se debe modificar este filtro de ejemplo antes de utilizarlo.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-116">If such a stack is being used, then this sample filter must be modified before use.</span></span>

 

``` syntax
// All broadcast WS-Discovery traffic
UDP.Port == 3702
```

<span data-ttu-id="f8fa9-117">En el ejemplo siguiente se muestra un filtro que limita la salida a los mensajes HTTP enviados a las pilas de WSDAPI en el puerto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-117">The following example shows a filter that limits output to HTTP messages sent to WSDAPI stacks on the default port.</span></span>

> [!Note]  
> <span data-ttu-id="f8fa9-118">Los servicios pueden enviar mensajes HTTP relevantes de puertos distintos de 5357.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-118">Services may send relevant HTTP messages from ports other than 5357.</span></span> <span data-ttu-id="f8fa9-119">Si el tráfico procedente de otros puertos es de interés, este filtro de ejemplo debe modificarse antes de usarse.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-119">If traffic from other ports is of interest, then this sample filter must be modified before use.</span></span>

 

``` syntax
// HTTP messages sent to WSDAPI stacks on default port
TCP.Port == 5357
```

<span data-ttu-id="f8fa9-120">En el ejemplo siguiente se muestra un filtro que limita la salida al tráfico de multidifusión IPv4.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-120">The following example shows a filter that limits output to IPv4 multicast traffic.</span></span>

``` syntax
// All IPv4 multicast traffic
IPv4.DestinationAddress == 239.255.255.250
```

<span data-ttu-id="f8fa9-121">En el ejemplo siguiente se muestra un filtro que limita la salida al tráfico de multidifusión IPv6.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-121">The following example shows a filter that limits output to IPv6 multicast traffic.</span></span>

``` syntax
// All IPv6 multicast traffic
IPv6.DestinationAddress == FF02::C
```

<span data-ttu-id="f8fa9-122">Algunos filtros se pueden combinar para limitar aún más los resultados.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-122">Some filters can be combined to further limit results.</span></span> <span data-ttu-id="f8fa9-123">En el ejemplo siguiente se muestra un filtro que limita la salida al tráfico de WS-Discovery de multidifusión IPv4.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-123">The following example shows a filter that limits output to IPv4 multicast WS-Discovery traffic.</span></span>

``` syntax
// All IPv4 multicast WS-Discovery traffic
UDP.Port==3702 && IPv4.DestinationAddress=239.255.255.250
```

<span data-ttu-id="f8fa9-124">Cuando se usan estos filtros, se puede excluir el tráfico relevante de los resultados de Netmon.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-124">When these filters are used, relevant traffic may be excluded from the Netmon results.</span></span> <span data-ttu-id="f8fa9-125">La exclusión puede producirse cuando los servicios residen en puertos distintos de los puertos predeterminados (5357/5358) y cuando una pila DPWS no responde a los mensajes mediante el puerto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-125">Exclusion can occur when services reside at ports other than the default ports (5357/5358) and when a DPWS stack does not respond to messages using the default port.</span></span> <span data-ttu-id="f8fa9-126">En estos casos, los filtros deben modificarse antes de usarse.</span><span class="sxs-lookup"><span data-stu-id="f8fa9-126">In these cases, the filters must be modified before use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8fa9-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f8fa9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8fa9-128">Procedimientos de diagnóstico de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="f8fa9-128">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="f8fa9-129">Introducción con la solución de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="f8fa9-129">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



