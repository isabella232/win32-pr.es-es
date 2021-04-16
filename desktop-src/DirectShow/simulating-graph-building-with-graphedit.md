---
description: Simular la compilación de gráficos con GraphEdit
ms.assetid: 3f7d3079-3d3d-4b93-9ab7-4c03def7c4be
title: Simular la compilación de gráficos con GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76878997c873c74d454979ccda689a9c241489d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495227"
---
# <a name="simulating-graph-building-with-graphedit"></a><span data-ttu-id="83c6e-103">Simular la compilación de gráficos con GraphEdit</span><span class="sxs-lookup"><span data-stu-id="83c6e-103">Simulating Graph Building with GraphEdit</span></span>

<span data-ttu-id="83c6e-104">DirectShow proporciona una utilidad de depuración denominada GraphEdit, que puede usar para crear y probar gráficos de filtros.</span><span class="sxs-lookup"><span data-stu-id="83c6e-104">DirectShow provides a debugging utility called GraphEdit, which you can use to create and test filter graphs.</span></span>

<span data-ttu-id="83c6e-105">GraphEdit es una herramienta visual para crear gráficos de filtros.</span><span class="sxs-lookup"><span data-stu-id="83c6e-105">GraphEdit is a visual tool for building filter graphs.</span></span> <span data-ttu-id="83c6e-106">Con GraphEdit, puede experimentar con un gráfico de filtros antes de escribir código de aplicación.</span><span class="sxs-lookup"><span data-stu-id="83c6e-106">With GraphEdit, you can experiment with a filter graph before you write any application code.</span></span> <span data-ttu-id="83c6e-107">También puede cargar un gráfico de filtro que cree la aplicación, para comprobar que la aplicación está compilando el gráfico correcto.</span><span class="sxs-lookup"><span data-stu-id="83c6e-107">You can also load a filter graph that your application creates, to verify that your application is building the correct graph.</span></span> <span data-ttu-id="83c6e-108">Si desarrolla un filtro personalizado, GraphEdit proporciona una forma rápida de probarla: simplemente cargue un grafo con el filtro personalizado y pruebe a ejecutar el gráfico.</span><span class="sxs-lookup"><span data-stu-id="83c6e-108">If you develop a custom filter, GraphEdit provides a quick way to test it: Simply load a graph with your custom filter and try running the graph.</span></span> <span data-ttu-id="83c6e-109">Si no está familiarizado con DirectShow, GraphEdit es una buena manera de familiarizarse con los gráficos de filtro y la arquitectura de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="83c6e-109">If you are new to DirectShow, GraphEdit is a good way to become familiar with filter graphs and the DirectShow architecture.</span></span>

<span data-ttu-id="83c6e-110">En la ilustración siguiente se muestra cómo GraphEdit representa un gráfico de filtro simple.</span><span class="sxs-lookup"><span data-stu-id="83c6e-110">The following illustration shows how GraphEdit represents a simple filter graph.</span></span>

![gráfico de filtro simple en GraphEdit](images/gedit09.png)

<span data-ttu-id="83c6e-112">Cada filtro se representa como un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="83c6e-112">Each filter is represented as a rectangle.</span></span> <span data-ttu-id="83c6e-113">Los cuadrados más pequeños a lo largo de los bordes de los filtros representan PIN.</span><span class="sxs-lookup"><span data-stu-id="83c6e-113">Smaller squares along the edges of the filters represent pins.</span></span> <span data-ttu-id="83c6e-114">Los pines de entrada están en el lado izquierdo del filtro y los pin de salida están en el lado derecho.</span><span class="sxs-lookup"><span data-stu-id="83c6e-114">Input pins are on the left side of the filter, and output pins are on the right side.</span></span> <span data-ttu-id="83c6e-115">Las flechas representan las conexiones entre los pines.</span><span class="sxs-lookup"><span data-stu-id="83c6e-115">The arrows represent the connections between pins.</span></span>

<span data-ttu-id="83c6e-116">Con GraphEdit, puede:</span><span class="sxs-lookup"><span data-stu-id="83c6e-116">With GraphEdit, you can:</span></span>

-   <span data-ttu-id="83c6e-117">Cree y modifique gráficos de filtro con una interfaz visual, de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="83c6e-117">Create and modify filter graphs using a visual, drag-and-drop interface.</span></span>
-   <span data-ttu-id="83c6e-118">Simular llamadas mediante programación para compilar un grafo.</span><span class="sxs-lookup"><span data-stu-id="83c6e-118">Simulate programmatic calls to build a graph.</span></span>
-   <span data-ttu-id="83c6e-119">Ejecutar, pausar, detener y buscar un grafo.</span><span class="sxs-lookup"><span data-stu-id="83c6e-119">Run, pause, stop, and seek a graph.</span></span>
-   <span data-ttu-id="83c6e-120">Vea qué filtros están registrados en el equipo y vea la información del registro para cada filtro.</span><span class="sxs-lookup"><span data-stu-id="83c6e-120">See what filters are registered on your computer, and view registry information for each filter.</span></span>
-   <span data-ttu-id="83c6e-121">Ver las páginas de propiedades de filtro.</span><span class="sxs-lookup"><span data-stu-id="83c6e-121">View filter property pages.</span></span>
-   <span data-ttu-id="83c6e-122">Ver los tipos de medios de las conexiones del PIN.</span><span class="sxs-lookup"><span data-stu-id="83c6e-122">View the media types of pin connections.</span></span>

<span data-ttu-id="83c6e-123">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="83c6e-123">This section contains the following topics:</span></span>

-   [<span data-ttu-id="83c6e-124">Usar GraphEdit</span><span class="sxs-lookup"><span data-stu-id="83c6e-124">Using GraphEdit</span></span>](using-graphedit.md)
-   [<span data-ttu-id="83c6e-125">Cargar un grafo desde un proceso externo</span><span class="sxs-lookup"><span data-stu-id="83c6e-125">Loading a Graph From an External Process</span></span>](loading-a-graph-from-an-external-process.md)
-   [<span data-ttu-id="83c6e-126">Guardar un gráfico de filtro en un archivo GraphEdit</span><span class="sxs-lookup"><span data-stu-id="83c6e-126">Saving a Filter Graph to a GraphEdit File</span></span>](saving-a-filter-graph-to-a-graphedit-file.md)
-   [<span data-ttu-id="83c6e-127">Cargar un archivo GraphEdit mediante programación</span><span class="sxs-lookup"><span data-stu-id="83c6e-127">Loading a GraphEdit File Programmatically</span></span>](loading-a-graphedit-file-programmatically.md)
-   [<span data-ttu-id="83c6e-128">Formato de archivo GraphEdit</span><span class="sxs-lookup"><span data-stu-id="83c6e-128">GraphEdit File Format</span></span>](graphedit-file-format.md)

## <a name="related-topics"></a><span data-ttu-id="83c6e-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="83c6e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83c6e-130">Usar DirectShow</span><span class="sxs-lookup"><span data-stu-id="83c6e-130">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



