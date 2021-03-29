---
description: Las métricas se utilizan para medir aspectos del rendimiento de la red y del protocolo.
ms.assetid: ee5faaf6-e230-4084-9829-e8cae8759587
title: Terminología de red (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04e84621cdaec2638762d54f67e5aca7e3d55ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809715"
---
# <a name="network-terminology-windows-sockets-2"></a><span data-ttu-id="38b4b-103">Terminología de red (Windows Sockets 2)</span><span class="sxs-lookup"><span data-stu-id="38b4b-103">Network Terminology (Windows Sockets 2)</span></span>

<span data-ttu-id="38b4b-104">Las métricas se utilizan para medir aspectos del rendimiento de la red y del protocolo.</span><span class="sxs-lookup"><span data-stu-id="38b4b-104">Metrics are used to measure aspects of network and protocol performance.</span></span> <span data-ttu-id="38b4b-105">Los valores de estas métricas en varios escenarios indican el nivel de rendimiento de una aplicación de red.</span><span class="sxs-lookup"><span data-stu-id="38b4b-105">The values for such metrics in various scenarios indicate the level of performance of a network application.</span></span> <span data-ttu-id="38b4b-106">En esta sección se definen los términos y las métricas usados en todo el sector para medir el rendimiento de las aplicaciones de red.</span><span class="sxs-lookup"><span data-stu-id="38b4b-106">This section defines terms and metrics used industry-wide for measuring network application performance.</span></span> <span data-ttu-id="38b4b-107">Estos términos se usan en el resto de esta guía.</span><span class="sxs-lookup"><span data-stu-id="38b4b-107">These terms are used throughout the rest of this guide.</span></span>

-   <span data-ttu-id="38b4b-108">Tiempo de ida y vuelta (RTT)</span><span class="sxs-lookup"><span data-stu-id="38b4b-108">Round Trip Time (RTT)</span></span>

    <span data-ttu-id="38b4b-109">Tiempo, en milisegundos, que tarda una solicitud en realizar un recorrido desde un equipo de origen a un equipo de destino y viceversa.</span><span class="sxs-lookup"><span data-stu-id="38b4b-109">Time, in milliseconds, for a request to make a trip from a source computer to a destination computer, and back again.</span></span> <span data-ttu-id="38b4b-110">Los valores menores indican un mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="38b4b-110">Lower values indicate better performance.</span></span> <span data-ttu-id="38b4b-111">Los tiempos de rutas de acceso hacia delante y devueltos no son necesariamente iguales.</span><span class="sxs-lookup"><span data-stu-id="38b4b-111">Forward and return path times are not necessarily equal.</span></span>

    <span data-ttu-id="38b4b-112">Los valores de RTT se ven afectados por la infraestructura de red, la distancia entre los nodos, las condiciones de la red y el tamaño de los paquetes.</span><span class="sxs-lookup"><span data-stu-id="38b4b-112">RTT values are affected by network infrastructure, distance between nodes, network conditions, and packet size.</span></span> <span data-ttu-id="38b4b-113">El tamaño de paquete, la congestión y la carga compresión afectan al RTT cuando se mide en vínculos de baja velocidad, como conexiones de acceso telefónico.</span><span class="sxs-lookup"><span data-stu-id="38b4b-113">Packet size, congestion and payload compressibility impact RTT when measured on slow links, such as dial-up connections.</span></span> <span data-ttu-id="38b4b-114">Otros factores afectan a RTT, incluida la corrección de errores de reenvío y la compresión de datos, que introducen búferes y colas que aumentan el RTT y, por tanto, reducen el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="38b4b-114">Other factors affect RTT, including forward error correction and data compression, which introduce buffers and queues that increase RTT, and therefore decrease performance.</span></span>

-   <span data-ttu-id="38b4b-115">Goodput</span><span class="sxs-lookup"><span data-stu-id="38b4b-115">Goodput</span></span>

    <span data-ttu-id="38b4b-116">Medida de datos de aplicación útiles procesados correctamente por el receptor, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="38b4b-116">Measure of useful application data successfully processed by the receiver, in bits-per-second.</span></span> <span data-ttu-id="38b4b-117">Goodput habilita la medición del rendimiento eficaz o útil e incluye solo los datos de la aplicación; Los encabezados de paquetes, protocolos y medios se consideran una sobrecarga y no forman parte de goodput.</span><span class="sxs-lookup"><span data-stu-id="38b4b-117">Goodput enables the measurement of effective or useful throughput and includes only application data; packet, protocol, and media headers are considered overhead, and are not part of goodput.</span></span>

-   <span data-ttu-id="38b4b-118">Sobrecarga de protocolo</span><span class="sxs-lookup"><span data-stu-id="38b4b-118">Protocol Overhead</span></span>

    <span data-ttu-id="38b4b-119">Bytes que no son de aplicación, incluidos tramas de protocolo y multimedia, divididos por el número total de bytes transmitidos.</span><span class="sxs-lookup"><span data-stu-id="38b4b-119">Nonapplication bytes, including protocol and media framing, divided by the total number of bytes transmitted.</span></span> <span data-ttu-id="38b4b-120">El valor se expresa como un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="38b4b-120">The value is expressed as a percentage.</span></span> <span data-ttu-id="38b4b-121">Los valores más altos indican un rendimiento más bajo.</span><span class="sxs-lookup"><span data-stu-id="38b4b-121">Higher values indicate poorer performance.</span></span>

    <span data-ttu-id="38b4b-122">La sobrecarga se calcula en ambas direcciones de esta guía, pero se puede calcular para cada dirección por separado.</span><span class="sxs-lookup"><span data-stu-id="38b4b-122">Overhead is calculated for both directions in this guide, but can be calculated for each direction separately.</span></span>

-   <span data-ttu-id="38b4b-123">Bandwidth-Delay producto</span><span class="sxs-lookup"><span data-stu-id="38b4b-123">Bandwidth-Delay Product</span></span>

    <span data-ttu-id="38b4b-124">Producto del ancho de banda de bits por segundo de la red y el RTT (en segundos).</span><span class="sxs-lookup"><span data-stu-id="38b4b-124">Product of the bits-per-second bandwidth of the network, and the RTT (in seconds).</span></span> <span data-ttu-id="38b4b-125">Este valor equivale al número de bits que se tarda en rellenar el ancho de banda de red disponible.</span><span class="sxs-lookup"><span data-stu-id="38b4b-125">This value equates to the number of bits it takes to fill available network bandwidth.</span></span> <span data-ttu-id="38b4b-126">Cuando el valor del producto de retraso de ancho de banda es alto, la pila TCP/IP debe administrar grandes cantidades de datos no confirmados para que la canalización esté completa.</span><span class="sxs-lookup"><span data-stu-id="38b4b-126">When the value for bandwidth-delay product is high, the TCP/IP stack must handle large amounts of unacknowledged data in order to keep the pipeline full.</span></span> <span data-ttu-id="38b4b-127">El producto de retraso de ancho de banda es una métrica de extremo a extremo de la clave para las aplicaciones de streaming.</span><span class="sxs-lookup"><span data-stu-id="38b4b-127">Bandwidth-delay product is a key end-to-end metric for streaming applications.</span></span>

 

 



