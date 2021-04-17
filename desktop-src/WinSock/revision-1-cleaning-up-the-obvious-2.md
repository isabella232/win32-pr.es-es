---
description: En esta versión del programa de ejemplo, se han realizado algunos cambios obvios que tomarán los progresos iniciales al mejorar el rendimiento.
ms.assetid: ef9d594c-31fe-44c0-b707-47c01e2c5bf0
title: 'Revisión 1: limpieza del'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 631bea7395000531cce542b41ace3b3aab9afff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715867"
---
# <a name="revision-one-cleaning-up-the-obvious"></a><span data-ttu-id="64b3a-103">Revisión 1: limpieza del</span><span class="sxs-lookup"><span data-stu-id="64b3a-103">Revision One: Cleaning up the Obvious</span></span>

<span data-ttu-id="64b3a-104">En esta versión del programa de ejemplo, se han realizado algunos cambios obvios que tomarán los progresos iniciales al mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="64b3a-104">In this version of the example program, a few obvious changes have been made that will take initial strides at improving performance.</span></span> <span data-ttu-id="64b3a-105">Esta versión del código está lejos del rendimiento, pero es un buen paso incremental que permite examinar los efectos de métodos más incrementales.</span><span class="sxs-lookup"><span data-stu-id="64b3a-105">This version of the code is far from performance-tuned, but it is a good incremental step that enables examination of the effects of incrementally better approaches.</span></span>

> [!WARNING]
> <span data-ttu-id="64b3a-106">Este ejemplo de la aplicación proporciona un rendimiento insuficiente intencionadamente, con el fin de mostrar las mejoras de rendimiento posibles con los cambios en el código.</span><span class="sxs-lookup"><span data-stu-id="64b3a-106">This example of the application provides intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="64b3a-107">No use este ejemplo de código en la aplicación; solo es para fines ilustrativos.</span><span class="sxs-lookup"><span data-stu-id="64b3a-107">Do not use this code sample in your application; it is for illustration purposes only.</span></span>

 


```C++
#include <windows.h>

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    BYTE tmp[3];
    tmp[0] = (BYTE)row;
    tmp[1] = (BYTE)col;
    tmp[2] = (BYTE)bAlive;
    bind( s, ... );
    connect( s, ... );
    send( s, &tmp, 3 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



## <a name="changes-in-this-version"></a><span data-ttu-id="64b3a-108">Cambios en esta versión</span><span class="sxs-lookup"><span data-stu-id="64b3a-108">Changes in this Version</span></span>

<span data-ttu-id="64b3a-109">Esta versión refleja los cambios siguientes:</span><span class="sxs-lookup"><span data-stu-id="64b3a-109">This version reflects the following changes:</span></span>

-   <span data-ttu-id="64b3a-110">Se quitó SNDBUF = 0.</span><span class="sxs-lookup"><span data-stu-id="64b3a-110">Removed SNDBUF=0.</span></span> <span data-ttu-id="64b3a-111">Se quitan los retrasos de 200 milisegundos debido a los envíos no almacenados en búfer y a las confirmaciones diferidas.</span><span class="sxs-lookup"><span data-stu-id="64b3a-111">The 200 millisecond delays due to unbuffered sends and delayed acknowledgments are removed.</span></span>
-   <span data-ttu-id="64b3a-112">Se ha quitado el comportamiento de envío y envío-recepción.</span><span class="sxs-lookup"><span data-stu-id="64b3a-112">Removed the Send-Send-Receive behavior.</span></span> <span data-ttu-id="64b3a-113">Este cambio elimina los retrasos de 200 milisegundos debido a las interacciones de Nagle y de la confirmación diferida.</span><span class="sxs-lookup"><span data-stu-id="64b3a-113">This change eliminates 200-millisecond delays due to Nagle and delayed ACK interactions.</span></span>
-   <span data-ttu-id="64b3a-114">Se quitó la hipótesis Little-Endian.</span><span class="sxs-lookup"><span data-stu-id="64b3a-114">Removed little-endian assumption.</span></span> <span data-ttu-id="64b3a-115">Los bytes están ahora en orden.</span><span class="sxs-lookup"><span data-stu-id="64b3a-115">The bytes are now in order.</span></span>

## <a name="remaining-problems"></a><span data-ttu-id="64b3a-116">Problemas restantes</span><span class="sxs-lookup"><span data-stu-id="64b3a-116">Remaining Problems</span></span>

<span data-ttu-id="64b3a-117">En esta versión, quedan los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="64b3a-117">In this version, the following problems remain:</span></span>

-   <span data-ttu-id="64b3a-118">La aplicación sigue conectándose.</span><span class="sxs-lookup"><span data-stu-id="64b3a-118">The application is still connect heavy.</span></span> <span data-ttu-id="64b3a-119">Dado que se quitan los retrasos de 600 + milisegundos, la aplicación ahora alcanza la tasa sostenida de 12 conexiones por segundo.</span><span class="sxs-lookup"><span data-stu-id="64b3a-119">Since the 600+ millisecond delays are removed, the application now hits the 12 connects-per-second sustained rate.</span></span> <span data-ttu-id="64b3a-120">Ahora muchas conexiones simultáneas se convierten en un problema.</span><span class="sxs-lookup"><span data-stu-id="64b3a-120">Many concurrent connections now becomes an issue.</span></span>
-   <span data-ttu-id="64b3a-121">La aplicación sigue siendo FAT; las celdas sin cambios se siguen propagando al servidor.</span><span class="sxs-lookup"><span data-stu-id="64b3a-121">The application is still fat; unchanged cells are still propagated to the server.</span></span>
-   <span data-ttu-id="64b3a-122">La aplicación todavía exhibe un flujo deficiente; los envíos de 3 bytes siguen siendo pequeños envíos.</span><span class="sxs-lookup"><span data-stu-id="64b3a-122">The application still exhibits poor streaming; 3-byte sends are still small sends.</span></span>
-   <span data-ttu-id="64b3a-123">La aplicación ahora envía 2 bytes/RTT, que es igual a 4 KB/s en la Ethernet conectada directamente.</span><span class="sxs-lookup"><span data-stu-id="64b3a-123">The application now sends 2 bytes/RTT, which equals 4 KB/s on directly connected Ethernet.</span></span> <span data-ttu-id="64b3a-124">Esto no es demasiado rápido, pero es probable que la espera de tiempo provoque problemas en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="64b3a-124">This is not too fast, but TIME-WAIT will likely cause problems first.</span></span>
-   <span data-ttu-id="64b3a-125">La sobrecarga está fuera del 99,3%, que sigue sin ser un buen porcentaje de sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="64b3a-125">The overhead is down to 99.3%, which is still not a good overhead percentage.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="64b3a-126">Métricas de rendimiento clave</span><span class="sxs-lookup"><span data-stu-id="64b3a-126">Key Performance Metrics</span></span>

<span data-ttu-id="64b3a-127">Las siguientes métricas clave de rendimiento se expresan en tiempo de ida y vuelta (RTT), Goodput y sobrecarga del protocolo.</span><span class="sxs-lookup"><span data-stu-id="64b3a-127">The following key performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="64b3a-128">Consulte el tema [terminología de red](network-terminology-2.md) para obtener una explicación de estos términos.</span><span class="sxs-lookup"><span data-stu-id="64b3a-128">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

<span data-ttu-id="64b3a-129">Esta versión refleja las siguientes métricas de rendimiento:</span><span class="sxs-lookup"><span data-stu-id="64b3a-129">This version reflect the following performance metrics:</span></span>

-   <span data-ttu-id="64b3a-130">Tiempo de celda: 2 × RTT</span><span class="sxs-lookup"><span data-stu-id="64b3a-130">Cell Time—2×RTT</span></span>
-   <span data-ttu-id="64b3a-131">Goodput: 2 bytes/RTT</span><span class="sxs-lookup"><span data-stu-id="64b3a-131">Goodput—2 bytes/RTT</span></span>
-   <span data-ttu-id="64b3a-132">Sobrecarga de protocolos: 99.3 Percent</span><span class="sxs-lookup"><span data-stu-id="64b3a-132">Protocol Overhead—99.3 percent</span></span>

## <a name="related-topics"></a><span data-ttu-id="64b3a-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="64b3a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64b3a-134">Mejora de una aplicación lenta</span><span class="sxs-lookup"><span data-stu-id="64b3a-134">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="64b3a-135">Terminología de red</span><span class="sxs-lookup"><span data-stu-id="64b3a-135">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="64b3a-136">La versión de línea base: una aplicación con un rendimiento muy deficiente</span><span class="sxs-lookup"><span data-stu-id="64b3a-136">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="64b3a-137">Revisión 2: rediseño para menos conexiones</span><span class="sxs-lookup"><span data-stu-id="64b3a-137">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="64b3a-138">Revisión 3: envío de bloque comprimido</span><span class="sxs-lookup"><span data-stu-id="64b3a-138">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> <dt>

[<span data-ttu-id="64b3a-139">Mejoras futuras</span><span class="sxs-lookup"><span data-stu-id="64b3a-139">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



