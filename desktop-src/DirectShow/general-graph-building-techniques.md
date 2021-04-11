---
description: Técnicas generales de Graph-Building
ms.assetid: 66d93305-175c-4549-b825-2f3d7fd6bf09
title: Técnicas generales de Graph-Building
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c73a005f1fbf7af0a53f11d44d600852f88752
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274631"
---
# <a name="general-graph-building-techniques"></a><span data-ttu-id="c68c2-103">Técnicas generales de Graph-Building</span><span class="sxs-lookup"><span data-stu-id="c68c2-103">General Graph-Building Techniques</span></span>

<span data-ttu-id="c68c2-104">Cada aplicación de DirectShow se inicia mediante la creación de un gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="c68c2-104">Every DirectShow application starts by building a filter graph.</span></span> <span data-ttu-id="c68c2-105">A medida que lea los temas de información general de la documentación de DirectShow, encontrará que la mayor parte de los pasos es describir el tipo de gráfico de filtro que necesita.</span><span class="sxs-lookup"><span data-stu-id="c68c2-105">As you read the overview topics in the DirectShow documentation, you will find that most start by describing what kind of filter graph you need.</span></span> <span data-ttu-id="c68c2-106">En algunos casos, hay un método o un objeto auxiliar específicamente diseñados para compilar ese tipo de gráfico.</span><span class="sxs-lookup"><span data-stu-id="c68c2-106">In some cases, there is a method or a helper object specifically designed for building that type of graph.</span></span> <span data-ttu-id="c68c2-107">Por ejemplo, el objeto [generador de gráficos de DVD](dvd-graph-builder.md) crea gráficos de reproducción de DVD.</span><span class="sxs-lookup"><span data-stu-id="c68c2-107">For example, the [DVD Graph Builder](dvd-graph-builder.md) object builds DVD playback graphs.</span></span> <span data-ttu-id="c68c2-108">En otros casos, la aplicación debe construir el gráfico agregando filtros y conectándolos.</span><span class="sxs-lookup"><span data-stu-id="c68c2-108">In other cases, the application must construct the graph by adding filters and connecting them.</span></span>

<span data-ttu-id="c68c2-109">En esta sección se presentan algunas funciones auxiliares que implementan operaciones básicas de creación de gráficos.</span><span class="sxs-lookup"><span data-stu-id="c68c2-109">This section presents some helper functions that implement basic graph-building operations.</span></span> <span data-ttu-id="c68c2-110">Se pueden usar en cualquier aplicación de DirectShow que necesite crear o modificar un gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="c68c2-110">They can be used by any DirectShow application that needs to build or modify a filter graph.</span></span> <span data-ttu-id="c68c2-111">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="c68c2-111">This section contains the following topics:</span></span>

-   [<span data-ttu-id="c68c2-112">Agregar un filtro por CLSID</span><span class="sxs-lookup"><span data-stu-id="c68c2-112">Add a Filter by CLSID</span></span>](add-a-filter-by-clsid.md)
-   [<span data-ttu-id="c68c2-113">Buscar un PIN no conectado en un filtro</span><span class="sxs-lookup"><span data-stu-id="c68c2-113">Find an Unconnected Pin on a Filter</span></span>](find-an-unconnected-pin-on-a-filter.md)
-   [<span data-ttu-id="c68c2-114">Conectar dos filtros</span><span class="sxs-lookup"><span data-stu-id="c68c2-114">Connect Two Filters</span></span>](connect-two-filters.md)
-   [<span data-ttu-id="c68c2-115">Buscar una interfaz en un filtro o un PIN</span><span class="sxs-lookup"><span data-stu-id="c68c2-115">Find an Interface on a Filter or Pin</span></span>](find-an-interface-on-a-filter-or-pin.md)
-   [<span data-ttu-id="c68c2-116">Buscar el elemento del mismo nivel de un filtro</span><span class="sxs-lookup"><span data-stu-id="c68c2-116">Find a Filter's Peer</span></span>](find-a-filters-peer.md)
-   [<span data-ttu-id="c68c2-117">Quitar todos los filtros del gráfico</span><span class="sxs-lookup"><span data-stu-id="c68c2-117">Remove All the Filters in the Graph</span></span>](remove-all-the-filters-in-the-graph.md)
-   [<span data-ttu-id="c68c2-118">Generar gráficos con el generador de gráficos de captura</span><span class="sxs-lookup"><span data-stu-id="c68c2-118">Building Graphs with the Capture Graph Builder</span></span>](building-graphs-with-the-capture-graph-builder.md)

## <a name="related-topics"></a><span data-ttu-id="c68c2-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c68c2-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c68c2-120">Tareas básicas de DirectShow</span><span class="sxs-lookup"><span data-stu-id="c68c2-120">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> <dt>

[<span data-ttu-id="c68c2-121">Enumerar dispositivos y filtros</span><span class="sxs-lookup"><span data-stu-id="c68c2-121">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="c68c2-122">Enumerar objetos en un gráfico de filtros</span><span class="sxs-lookup"><span data-stu-id="c68c2-122">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="c68c2-123">Conexión inteligente</span><span class="sxs-lookup"><span data-stu-id="c68c2-123">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> </dl>

 

 



