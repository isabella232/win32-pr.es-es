---
description: En esta revisión, se rediseña la aplicación de ejemplo para eliminar las conexiones innecesarias.
ms.assetid: 0db6ded4-0a59-454e-824e-8cd7f0dc9fec
title: 'Revisión 2: rediseño para menos conexiones'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8d5a8c8648f43f9ddac93c9d17f667b4b97011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155873"
---
# <a name="revision-two-redesigning-for-fewer-connects"></a><span data-ttu-id="aa8b4-103">Revisión 2: rediseño para menos conexiones</span><span class="sxs-lookup"><span data-stu-id="aa8b4-103">Revision Two: Redesigning for Fewer Connects</span></span>

<span data-ttu-id="aa8b4-104">En esta revisión, se rediseña la aplicación de ejemplo para eliminar las conexiones innecesarias.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-104">In this revision, the sample application is redesigned to eliminate unnecessary connects.</span></span>

> [!WARNING]
> <span data-ttu-id="aa8b4-105">En este ejemplo de la aplicación también se proporciona un rendimiento insuficiente intencionadamente, con el fin de mostrar las mejoras de rendimiento posibles con los cambios en el código.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-105">This examples of the application also provide intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="aa8b4-106">No use este ejemplo de código en la aplicación; solo es para fines ilustrativos.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-106">Do not use this code sample in your application; it is for illustration purposes only.</span></span>

 


```C++
ComputeNext( Map );
bind( s, ... );
connect( s, ... );
for(int i=0 ; i < ROWS ; ++i)
  for(int j=0 ; j < COLS ; ++j)
  {
    BYTE tmp[3];
    tmp[0] = i;
    tmp[1] = j;
    tmp[2] = Map[i][j];
    send( s, tmp, 3 );
    recv( s, &byRet, 1 );
  }
closesocket( s );
```



## <a name="remaining-problems"></a><span data-ttu-id="aa8b4-107">Problemas restantes</span><span class="sxs-lookup"><span data-stu-id="aa8b4-107">Remaining Problems</span></span>

<span data-ttu-id="aa8b4-108">Los cambios en la revisión dos rediseñaron la aplicación para realizar solo una conexión por actualización.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-108">The changes in Revision Two redesigned the application to make only one connect per update.</span></span> <span data-ttu-id="aa8b4-109">La aplicación todavía incluye los siguientes problemas de rendimiento:</span><span class="sxs-lookup"><span data-stu-id="aa8b4-109">The application still includes the following performance issues:</span></span>

-   <span data-ttu-id="aa8b4-110">La aplicación todavía se serializa y conversa.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-110">The application is still serialized and chatty.</span></span>
-   <span data-ttu-id="aa8b4-111">La aplicación todavía tiene un diseño FAT; Hay muchos envíos que no requieren ninguna operación en este diseño.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-111">The application still has a fat design; there are many sends that require no operation in this design.</span></span>
-   <span data-ttu-id="aa8b4-112">Los envíos siguen siendo solo 3 bytes, que es un flujo deficiente.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-112">The sends are still only 3 bytes, which is poor streaming.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="aa8b4-113">Métricas de rendimiento clave</span><span class="sxs-lookup"><span data-stu-id="aa8b4-113">Key Performance Metrics</span></span>

<span data-ttu-id="aa8b4-114">Las siguientes métricas de rendimiento se expresan en tiempo de ida y vuelta (RTT), Goodput y sobrecarga del protocolo.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-114">The following performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="aa8b4-115">Consulte el tema [terminología de red](network-terminology-2.md) para obtener una explicación de estos términos.</span><span class="sxs-lookup"><span data-stu-id="aa8b4-115">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

<span data-ttu-id="aa8b4-116">Esta versión refleja las siguientes métricas de rendimiento:</span><span class="sxs-lookup"><span data-stu-id="aa8b4-116">This version reflects the following performance metrics:</span></span>

-   <span data-ttu-id="aa8b4-117">Tiempo de la celda: 1 \* RTT</span><span class="sxs-lookup"><span data-stu-id="aa8b4-117">Cell Time — 1\*RTT</span></span>
-   <span data-ttu-id="aa8b4-118">Goodput: 4 bytes/RTT</span><span class="sxs-lookup"><span data-stu-id="aa8b4-118">Goodput — 4 bytes/RTT</span></span>
-   <span data-ttu-id="aa8b4-119">Sobrecarga de protocolo: 96,8%</span><span class="sxs-lookup"><span data-stu-id="aa8b4-119">Protocol Overhead — 96.8%</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa8b4-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aa8b4-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa8b4-121">Mejora de una aplicación lenta</span><span class="sxs-lookup"><span data-stu-id="aa8b4-121">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="aa8b4-122">Terminología de red</span><span class="sxs-lookup"><span data-stu-id="aa8b4-122">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="aa8b4-123">La versión de línea base: una aplicación con un rendimiento muy deficiente</span><span class="sxs-lookup"><span data-stu-id="aa8b4-123">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="aa8b4-124">Revisión 1: limpieza del manifiesto</span><span class="sxs-lookup"><span data-stu-id="aa8b4-124">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="aa8b4-125">Revisión 3: envío de bloque comprimido</span><span class="sxs-lookup"><span data-stu-id="aa8b4-125">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> <dt>

[<span data-ttu-id="aa8b4-126">Mejoras futuras</span><span class="sxs-lookup"><span data-stu-id="aa8b4-126">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



