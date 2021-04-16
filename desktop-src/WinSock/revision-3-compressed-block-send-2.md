---
description: En esta versión de la aplicación, se usa un bloque comprimido que envía los datos. Este cambio produce una mejora significativa del rendimiento.
ms.assetid: 3f0a129b-5b67-4334-a0aa-cd80ee7018b9
title: 'Revisión 3: envío de bloque comprimido'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657579406ed31fce08239c518a6910f525219fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706188"
---
# <a name="revision-three-compressed-block-send"></a><span data-ttu-id="689ea-104">Revisión 3: envío de bloque comprimido</span><span class="sxs-lookup"><span data-stu-id="689ea-104">Revision Three: Compressed Block Send</span></span>

<span data-ttu-id="689ea-105">En esta versión de la aplicación, se usa un bloque comprimido que envía los datos.</span><span class="sxs-lookup"><span data-stu-id="689ea-105">In this version of the application, a compressed block send of the data is used.</span></span> <span data-ttu-id="689ea-106">Este cambio produce una mejora significativa del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="689ea-106">This change results in significant performance improvement.</span></span>


```C++
BYTE tmp[3*ROWS*COLS];
FIELD Old = Map;
ComputeNext( Map );
n=Compact(Map,Old,tmp);
bind( s, ... );
connect( s, ... );
send( s, tmp, 3*n );
//can't do recv(s,tmp,n)
for(int i=0; i < n; )
    recv( s, tmp+i, n-i );
closesocket( s );
```



## <a name="changes-in-this-version"></a><span data-ttu-id="689ea-107">Cambios en esta versión</span><span class="sxs-lookup"><span data-stu-id="689ea-107">Changes in this Version</span></span>

<span data-ttu-id="689ea-108">Esta versión refleja los cambios siguientes:</span><span class="sxs-lookup"><span data-stu-id="689ea-108">This version reflects the following changes:</span></span>

-   <span data-ttu-id="689ea-109">Las actualizaciones de celda ya no se serializan.</span><span class="sxs-lookup"><span data-stu-id="689ea-109">Cell updates are no longer serialized.</span></span>
-   <span data-ttu-id="689ea-110">Dado que se usa un bloque de envío, la aplicación ya no está conversando.</span><span class="sxs-lookup"><span data-stu-id="689ea-110">Since a block send is used, the application is no longer chatty.</span></span>
-   <span data-ttu-id="689ea-111">Se utiliza la compresión de datos, lo que da lugar a una aplicación menos FAT.</span><span class="sxs-lookup"><span data-stu-id="689ea-111">Data compression is used, resulting in a less fat application.</span></span>

<span data-ttu-id="689ea-112">Todavía hay un problema con esta versión de la aplicación; el riesgo de interbloqueo existe porque se usa un envío grande sin recibir.</span><span class="sxs-lookup"><span data-stu-id="689ea-112">There is still an issue with this version of the application; the risk of deadlock exists since a large send is used with no receives.</span></span> <span data-ttu-id="689ea-113">El servidor envía un byte por cada 3 bytes recibidos.</span><span class="sxs-lookup"><span data-stu-id="689ea-113">The server sends one byte for every 3 bytes received.</span></span> <span data-ttu-id="689ea-114">Esto podría producir un interbloqueo si el tamaño del búfer de recepción es inferior a 1000 bytes para esta aplicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="689ea-114">This could cause a deadlock if the receive buffer size is less than 1000 bytes for this sample application.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="689ea-115">Métricas de rendimiento clave</span><span class="sxs-lookup"><span data-stu-id="689ea-115">Key Performance Metrics</span></span>

<span data-ttu-id="689ea-116">Las siguientes métricas de rendimiento se expresan en tiempo de ida y vuelta (RTT), Goodput y sobrecarga del protocolo.</span><span class="sxs-lookup"><span data-stu-id="689ea-116">The following performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="689ea-117">Consulte el tema [terminología de red](network-terminology-2.md) para obtener una explicación de estos términos.</span><span class="sxs-lookup"><span data-stu-id="689ea-117">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

<span data-ttu-id="689ea-118">Esta versión refleja las siguientes métricas de rendimiento:</span><span class="sxs-lookup"><span data-stu-id="689ea-118">This version reflects the following performance metrics:</span></span>

-   <span data-ttu-id="689ea-119">Hora de la celda:. 002 \* RTT</span><span class="sxs-lookup"><span data-stu-id="689ea-119">Cell Time — .002\*RTT</span></span>
-   <span data-ttu-id="689ea-120">Goodput: 2 kilobytes/RTT</span><span class="sxs-lookup"><span data-stu-id="689ea-120">Goodput — 2 Kilobytes/RTT</span></span>
-   <span data-ttu-id="689ea-121">Sobrecarga de protocolos: 14%</span><span class="sxs-lookup"><span data-stu-id="689ea-121">Protocol Overhead — 14%</span></span>

<span data-ttu-id="689ea-122">En el 14% de la sobrecarga, el 6% se deriva de los encabezados Ethernet y el otro 8% proviene del inicio y el desmontaje de la conexión.</span><span class="sxs-lookup"><span data-stu-id="689ea-122">Of the 14% overhead, 6% is from the Ethernet headers and the other 8% is from the connection startup and teardown.</span></span>

## <a name="related-topics"></a><span data-ttu-id="689ea-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="689ea-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="689ea-124">Mejora de una aplicación lenta</span><span class="sxs-lookup"><span data-stu-id="689ea-124">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="689ea-125">Terminología de red</span><span class="sxs-lookup"><span data-stu-id="689ea-125">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="689ea-126">La versión de línea base: una aplicación con un rendimiento muy deficiente</span><span class="sxs-lookup"><span data-stu-id="689ea-126">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="689ea-127">Revisión 1: limpieza del manifiesto</span><span class="sxs-lookup"><span data-stu-id="689ea-127">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="689ea-128">Revisión 2: rediseño para menos conexiones</span><span class="sxs-lookup"><span data-stu-id="689ea-128">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="689ea-129">Mejoras futuras</span><span class="sxs-lookup"><span data-stu-id="689ea-129">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



