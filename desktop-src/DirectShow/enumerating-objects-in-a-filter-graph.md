---
description: Enumerar objetos en un gráfico de filtros
ms.assetid: 04a3dbc8-33c4-4b70-930e-686be2f8301f
title: Enumerar objetos en un gráfico de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369cd3400d3b7fc9944662ed6d32fd67234af90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152298"
---
# <a name="enumerating-objects-in-a-filter-graph"></a><span data-ttu-id="29e1e-103">Enumerar objetos en un gráfico de filtros</span><span class="sxs-lookup"><span data-stu-id="29e1e-103">Enumerating Objects in a Filter Graph</span></span>

<span data-ttu-id="29e1e-104">Es posible que una aplicación necesite buscar un filtro determinado en el gráfico de filtros, o incluso un PIN determinado en un filtro.</span><span class="sxs-lookup"><span data-stu-id="29e1e-104">An application might need to locate a particular filter in the filter graph, or even a particular pin on a filter.</span></span> <span data-ttu-id="29e1e-105">Por ejemplo, podría utilizar una interfaz que expone un filtro determinado.</span><span class="sxs-lookup"><span data-stu-id="29e1e-105">For example, it might use an interface that a particular filter exposes.</span></span> <span data-ttu-id="29e1e-106">O bien, puede crear un gráfico de filtros especializado y tener que llamar a métodos en PIN individuales para conectar los filtros.</span><span class="sxs-lookup"><span data-stu-id="29e1e-106">Or, it might construct a specialized filter graph and need to call methods on individual pins to connect the filters.</span></span> <span data-ttu-id="29e1e-107">Para este propósito, DirectShow proporciona varios métodos para enumerar los objetos de un gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="29e1e-107">For this purpose, DirectShow provides several methods for enumerating objects in a filter graph.</span></span>

<span data-ttu-id="29e1e-108">Los enumeradores descritos en esta sección siguen el formato estándar que utilizan las interfaces de enumeración COM.</span><span class="sxs-lookup"><span data-stu-id="29e1e-108">The enumerators discussed in this section follow the standard form used by COM enumeration interfaces.</span></span> <span data-ttu-id="29e1e-109">Para obtener más información, vea el tema "IEnumXXXX" en el SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="29e1e-109">For more information, see the "IEnumXXXX" topic in the Platform SDK.</span></span> <span data-ttu-id="29e1e-110">Para obtener información sobre la enumeración de filtros que están registrados en el equipo del usuario, pero que aún no están en el gráfico de filtros, consulte [enumeración de dispositivos y filtros](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="29e1e-110">For information on enumerating filters that are registered on the user's computer, but aren't yet in the filter graph, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>

<span data-ttu-id="29e1e-111">Ese artículo contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="29e1e-111">This article contains the following topics:</span></span>

-   [<span data-ttu-id="29e1e-112">Enumerar filtros</span><span class="sxs-lookup"><span data-stu-id="29e1e-112">Enumerating Filters</span></span>](enumerating-filters.md)
-   [<span data-ttu-id="29e1e-113">Enumerar PIN</span><span class="sxs-lookup"><span data-stu-id="29e1e-113">Enumerating Pins</span></span>](enumerating-pins.md)
-   [<span data-ttu-id="29e1e-114">Enumerar tipos de medios</span><span class="sxs-lookup"><span data-stu-id="29e1e-114">Enumerating Media Types</span></span>](enumerating-media-types.md)

## <a name="related-topics"></a><span data-ttu-id="29e1e-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="29e1e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29e1e-116">Tareas básicas de DirectShow</span><span class="sxs-lookup"><span data-stu-id="29e1e-116">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 



