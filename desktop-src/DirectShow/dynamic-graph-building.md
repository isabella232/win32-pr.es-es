---
description: Creación de gráficos dinámicos
ms.assetid: 13fed430-979b-40f7-91ba-aff2d811bd92
title: Creación de gráficos dinámicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710bf5f648fc91e8db6bf62d81b41327f874ddf7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677125"
---
# <a name="dynamic-graph-building"></a><span data-ttu-id="b29d5-103">Creación de gráficos dinámicos</span><span class="sxs-lookup"><span data-stu-id="b29d5-103">Dynamic Graph Building</span></span>

<span data-ttu-id="b29d5-104">Si tiene que modificar un gráfico de filtros existente, puede detener el gráfico, realizar los cambios y reiniciar el gráfico.</span><span class="sxs-lookup"><span data-stu-id="b29d5-104">If you need to modify an existing filter graph, you can stop the graph, make the changes, and restart the graph.</span></span> <span data-ttu-id="b29d5-105">Este suele ser el mejor enfoque.</span><span class="sxs-lookup"><span data-stu-id="b29d5-105">This is usually the best approach.</span></span> <span data-ttu-id="b29d5-106">Sin embargo, en algunas circunstancias, es posible que desee modificar un gráfico mientras se sigue ejecutando.</span><span class="sxs-lookup"><span data-stu-id="b29d5-106">However, under some circumstances, you might want to alter a graph while it is still running.</span></span> <span data-ttu-id="b29d5-107">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="b29d5-107">For example:</span></span>

-   <span data-ttu-id="b29d5-108">La aplicación inserta un filtro de efectos de vídeo durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="b29d5-108">The application inserts a video effects filter during playback.</span></span>
-   <span data-ttu-id="b29d5-109">Un filtro de origen cambia el flujo medio de tipos de medios, posiblemente requiriendo un nuevo filtro de descompresión.</span><span class="sxs-lookup"><span data-stu-id="b29d5-109">A source filter switches media types midstream, possibly requiring a new decompression filter.</span></span>
-   <span data-ttu-id="b29d5-110">La aplicación agrega una nueva secuencia de vídeo al gráfico.</span><span class="sxs-lookup"><span data-stu-id="b29d5-110">The application adds a new video stream to the graph.</span></span>

<span data-ttu-id="b29d5-111">Estos son algunos ejemplos de *creación de gráficos dinámicos*, un término que cubre cualquier tipo de cambio en un gráfico de filtro mientras el gráfico continúa ejecutándose.</span><span class="sxs-lookup"><span data-stu-id="b29d5-111">These are all examples of *dynamic graph building*, a term that covers any kind of change to a filter graph while the graph continues to run.</span></span> <span data-ttu-id="b29d5-112">Una aplicación o un filtro del gráfico pueden iniciar la creación de gráficos dinámicos.</span><span class="sxs-lookup"><span data-stu-id="b29d5-112">Dynamic graph building can be initiated by an application or by a filter in the graph.</span></span> <span data-ttu-id="b29d5-113">Se pueden realizar tres escenarios distintos:</span><span class="sxs-lookup"><span data-stu-id="b29d5-113">Three distinct scenarios are possible:</span></span>

-   <span data-ttu-id="b29d5-114">[Cambios en el formato dinámico](dynamic-format-changes.md): un filtro puede cambiar los formatos de la secuencia en el nivel más bajo, sin necesidad de quitar o reemplazar ningún filtro.</span><span class="sxs-lookup"><span data-stu-id="b29d5-114">[Dynamic Format Changes](dynamic-format-changes.md): A filter can change formats midstream, without the need to remove or replace any filters.</span></span>
-   <span data-ttu-id="b29d5-115">[Reconexión dinámica](dynamic-reconnection.md): cambiar el gráfico agregando o quitando filtros.</span><span class="sxs-lookup"><span data-stu-id="b29d5-115">[Dynamic Reconnection](dynamic-reconnection.md): Changing the graph by adding or removing filters.</span></span>
-   <span data-ttu-id="b29d5-116">[Cadenas de filtro](filter-chains.md): agregar, quitar y controlar cadenas de filtros.</span><span class="sxs-lookup"><span data-stu-id="b29d5-116">[Filter Chains](filter-chains.md): Adding, removing, and controlling chains of filters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b29d5-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b29d5-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b29d5-118">Acerca de DirectShow</span><span class="sxs-lookup"><span data-stu-id="b29d5-118">About DirectShow</span></span>](about-directshow.md)
</dt> </dl>

 

 



