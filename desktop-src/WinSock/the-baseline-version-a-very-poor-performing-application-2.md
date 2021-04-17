---
description: Versión de línea de base de una aplicación con un rendimiento muy deficiente en Windows Sockets (Winsock).
ms.assetid: 923884c4-f1bd-4f72-983e-6158f368e0dd
title: 'La versión de línea base: una aplicación con un rendimiento muy deficiente'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c094be5fd5cf6e3b9eaeb07c7ff38880e651dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706481"
---
# <a name="the-baseline-version-a-very-poor-performing-application"></a><span data-ttu-id="8b639-103">La versión de línea base: una aplicación con un rendimiento muy deficiente</span><span class="sxs-lookup"><span data-stu-id="8b639-103">The Baseline Version: A Very Poor Performing Application</span></span>

<span data-ttu-id="8b639-104">La siguiente muestra de código de bajo rendimiento que se usa para calcular las actualizaciones es como sigue:</span><span class="sxs-lookup"><span data-stu-id="8b639-104">The initial, poor performing code sample used to calculate the updates is as follows:</span></span>

> [!Note]  
> <span data-ttu-id="8b639-105">Para simplificar, no hay ningún control de errores en los ejemplos siguientes.</span><span class="sxs-lookup"><span data-stu-id="8b639-105">For simplicity, there is no error handling in the following examples.</span></span> <span data-ttu-id="8b639-106">Cualquier aplicación de producción siempre comprueba los valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="8b639-106">Any production application always checks return values.</span></span>

 

> [!WARNING]
> <span data-ttu-id="8b639-107">Los primeros ejemplos de la aplicación proporcionan un rendimiento insuficiente intencionadamente, con el fin de mostrar las mejoras de rendimiento posibles con los cambios en el código.</span><span class="sxs-lookup"><span data-stu-id="8b639-107">The first few examples of the application provide intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="8b639-108">No use estos ejemplos de código en la aplicación; solo tienen fines ilustrativos.</span><span class="sxs-lookup"><span data-stu-id="8b639-108">Do not use these code samples in your application; they are for illustration purposes only.</span></span>

 


```C++
#include <windows.h>

BOOL Map[ROWS][COLS];

void LifeUpdate()
{
    ComputeNext( Map );
    for( int i = 0 ; i < ROWS ; ++i )     //serialized
        for( int j = 0 ; j < COLS ; ++j )
            Set( i, j, Map[i][j] );    //chatty
}

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    setsockopt( s, SO_SNDBUF, &Zero, sizeof(int) );
    bind( s, ... );
    connect( s, ... );
    send( s, &row, 1 );
    send( s, &col, 1 );
    send( s, &bAlive, 1 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



<span data-ttu-id="8b639-109">En este estado, la aplicación tiene el peor rendimiento posible de la red.</span><span class="sxs-lookup"><span data-stu-id="8b639-109">In this state, the application has the worst possible network performance.</span></span> <span data-ttu-id="8b639-110">Los problemas con esta versión de la aplicación de ejemplo incluyen:</span><span class="sxs-lookup"><span data-stu-id="8b639-110">The problems with this version of the sample application include:</span></span>

-   <span data-ttu-id="8b639-111">La aplicación está conversando.</span><span class="sxs-lookup"><span data-stu-id="8b639-111">The application is chatty.</span></span> <span data-ttu-id="8b639-112">Cada transacción es demasiado pequeña: no es necesario actualizar las celdas una por una.</span><span class="sxs-lookup"><span data-stu-id="8b639-112">Each transaction is too small — cells do not need to be updated one by one.</span></span>
-   <span data-ttu-id="8b639-113">Las transacciones se serializan estrictamente, aunque las celdas se puedan actualizar simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="8b639-113">The transactions are strictly serialized, even though the cells could be updated concurrently.</span></span>
-   <span data-ttu-id="8b639-114">El búfer de envío se establece en cero y la aplicación produce un retraso de 200 milisegundos para cada envío (tres veces por celda).</span><span class="sxs-lookup"><span data-stu-id="8b639-114">The send buffer is set to zero, and the application incurs a 200-millisecond delay for each send — three times per cell.</span></span>
-   <span data-ttu-id="8b639-115">La aplicación tiene mucha conexión y se conecta una vez para cada celda.</span><span class="sxs-lookup"><span data-stu-id="8b639-115">The application is very connect heavy, connecting once for each cell.</span></span> <span data-ttu-id="8b639-116">Las aplicaciones están limitadas por el número de conexiones por segundo para un destino determinado debido a un estado de tiempo de espera, pero esto no supone un problema aquí, ya que cada transacción tarda más de 600 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="8b639-116">Applications are limited in the number of connections per second for a given destination because of TIME-WAIT state, but that is not an issue here, since each transaction takes over 600 milliseconds.</span></span>
-   <span data-ttu-id="8b639-117">La aplicación es FAT; muchas transacciones no tienen ningún efecto en el estado del servidor, ya que muchas celdas no cambian de la actualización a la actualización.</span><span class="sxs-lookup"><span data-stu-id="8b639-117">The application is fat; many transactions have no effect on the server state, because many cells do not change from update to update.</span></span>
-   <span data-ttu-id="8b639-118">La aplicación exhibe un flujo deficiente; los envíos pequeños consumen mucha CPU y RAM.</span><span class="sxs-lookup"><span data-stu-id="8b639-118">The application exhibits poor streaming; small sends consume a lot of CPU and RAM.</span></span>
-   <span data-ttu-id="8b639-119">La aplicación asume una representación de Little-Endian para sus envíos.</span><span class="sxs-lookup"><span data-stu-id="8b639-119">The application assumes little-endian representation for its sends.</span></span> <span data-ttu-id="8b639-120">Se trata de una suposición natural para la plataforma actual de Windows, pero puede ser peligrosa para el código de larga duración.</span><span class="sxs-lookup"><span data-stu-id="8b639-120">This is a natural assumption for the current Windows platform, but can be dangerous for long-lived code.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="8b639-121">Métricas de rendimiento clave</span><span class="sxs-lookup"><span data-stu-id="8b639-121">Key Performance Metrics</span></span>

<span data-ttu-id="8b639-122">Las siguientes métricas de rendimiento se expresan en tiempo de ida y vuelta (RTT), Goodput y sobrecarga del protocolo.</span><span class="sxs-lookup"><span data-stu-id="8b639-122">The following performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="8b639-123">Consulte el tema [terminología de red](network-terminology-2.md) para obtener una explicación de estos términos.</span><span class="sxs-lookup"><span data-stu-id="8b639-123">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

-   <span data-ttu-id="8b639-124">Hora de la red, hora de la red para una actualización de una sola celda, requiere 4 \* RTT + 600 milisegundos para las interacciones de Nagle y ACK retrasada.</span><span class="sxs-lookup"><span data-stu-id="8b639-124">Cell time, network time for a single cell update, requires 4\*RTT + 600 milliseconds for Nagle and delayed ACK interactions.</span></span>
-   <span data-ttu-id="8b639-125">Goodput tiene menos de 6 bytes.</span><span class="sxs-lookup"><span data-stu-id="8b639-125">Goodput is less than 6 bytes.</span></span>
-   <span data-ttu-id="8b639-126">La sobrecarga del protocolo es del 99,6%.</span><span class="sxs-lookup"><span data-stu-id="8b639-126">Protocol Overhead is 99.6%.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b639-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8b639-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b639-128">Mejora de una aplicación lenta</span><span class="sxs-lookup"><span data-stu-id="8b639-128">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="8b639-129">Terminología de red</span><span class="sxs-lookup"><span data-stu-id="8b639-129">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="8b639-130">Revisión 1: limpieza del manifiesto</span><span class="sxs-lookup"><span data-stu-id="8b639-130">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="8b639-131">Revisión 2: rediseño para menos conexiones</span><span class="sxs-lookup"><span data-stu-id="8b639-131">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="8b639-132">Revisión 3: envío de bloque comprimido</span><span class="sxs-lookup"><span data-stu-id="8b639-132">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> <dt>

[<span data-ttu-id="8b639-133">Mejoras futuras</span><span class="sxs-lookup"><span data-stu-id="8b639-133">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



