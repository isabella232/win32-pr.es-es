---
description: Flujo de datos en el gráfico de filtros
ms.assetid: 3fcfd874-39bc-42d2-9fc9-2d8945ffa8e3
title: Flujo de datos en el gráfico de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38e0e730dd78e3a42a1121e4a63a053e6016402
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906850"
---
# <a name="data-flow-in-the-filter-graph"></a><span data-ttu-id="d3653-103">Flujo de datos en el gráfico de filtros</span><span class="sxs-lookup"><span data-stu-id="d3653-103">Data Flow in the Filter Graph</span></span>

<span data-ttu-id="d3653-104">En esta sección se describe cómo se mueven los datos multimedia a través del gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="d3653-104">This section describes how media data moves through the filter graph.</span></span> <span data-ttu-id="d3653-105">Normalmente, no es necesario conocer estos detalles para escribir una aplicación de DirectShow, aunque en algunos casos puede resultar útil.</span><span class="sxs-lookup"><span data-stu-id="d3653-105">Usually, you do not need to know these details to write a DirectShow application, although in some situations you may find it helpful.</span></span> <span data-ttu-id="d3653-106">Si está escribiendo un filtro de DirectShow, debe comprender este material.</span><span class="sxs-lookup"><span data-stu-id="d3653-106">If you are writing a DirectShow filter, you will need to understand this material.</span></span>

<span data-ttu-id="d3653-107">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="d3653-107">This section contains the following topics:</span></span>

-   [<span data-ttu-id="d3653-108">Información general sobre el flujo de datos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="d3653-108">Overview of Data Flow in DirectShow</span></span>](overview-of-data-flow-in-directshow.md)
-   [<span data-ttu-id="d3653-109">Transportes</span><span class="sxs-lookup"><span data-stu-id="d3653-109">Transports</span></span>](transports.md)
-   [<span data-ttu-id="d3653-110">Muestras y asignadores</span><span class="sxs-lookup"><span data-stu-id="d3653-110">Samples and Allocators</span></span>](samples-and-allocators.md)
-   [<span data-ttu-id="d3653-111">Estados de filtro</span><span class="sxs-lookup"><span data-stu-id="d3653-111">Filter States</span></span>](filter-states.md)
-   [<span data-ttu-id="d3653-112">Modelo de extracción</span><span class="sxs-lookup"><span data-stu-id="d3653-112">Pull Model</span></span>](pull-model.md)

## <a name="related-topics"></a><span data-ttu-id="d3653-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d3653-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3653-114">Flujo de datos para desarrolladores de filtros</span><span class="sxs-lookup"><span data-stu-id="d3653-114">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
</dt> </dl>

 

 



