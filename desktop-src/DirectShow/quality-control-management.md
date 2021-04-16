---
description: Administración de Quality-Control
ms.assetid: b1def588-6c9c-4853-a69b-1ba5df8b5ba2
title: Administración de Quality-Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c68aff4f8c054f9f649801e1b9829ccd7daaff35
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686270"
---
# <a name="quality-control-management"></a><span data-ttu-id="ea3bc-103">Administración de Quality-Control</span><span class="sxs-lookup"><span data-stu-id="ea3bc-103">Quality-Control Management</span></span>

<span data-ttu-id="ea3bc-104">Control de calidad es un mecanismo para ajustar la velocidad del flujo de datos a través del gráfico de filtro en respuesta al rendimiento en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ea3bc-104">Quality control is a mechanism for adjusting the rate of data flow through the filter graph in response to run-time performance.</span></span> <span data-ttu-id="ea3bc-105">Si un filtro de representador recibe demasiados datos o demasiado pocos, puede enviar un *mensaje de calidad*.</span><span class="sxs-lookup"><span data-stu-id="ea3bc-105">If a renderer filter is receiving too much data or too little data, it can send a *quality message*.</span></span> <span data-ttu-id="ea3bc-106">El mensaje de calidad solicita un ajuste en la velocidad de datos.</span><span class="sxs-lookup"><span data-stu-id="ea3bc-106">The quality message requests an adjustment in the data rate.</span></span> <span data-ttu-id="ea3bc-107">De forma predeterminada, los mensajes de calidad viajan hacia arriba desde el representador hasta que llegan a un filtro que puede responder (si lo hubiera).</span><span class="sxs-lookup"><span data-stu-id="ea3bc-107">By default, quality messages travel upstream from the renderer until they reach a filter that can respond (if any).</span></span> <span data-ttu-id="ea3bc-108">Una aplicación también puede implementar un administrador de calidad personalizado.</span><span class="sxs-lookup"><span data-stu-id="ea3bc-108">An application can also implement a custom quality manager.</span></span> <span data-ttu-id="ea3bc-109">En ese caso, el representador pasa los mensajes de calidad directamente al administrador de calidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ea3bc-109">In that case, the renderer passes quality messages directly to the application's quality manager.</span></span>

<span data-ttu-id="ea3bc-110">Este artículo contiene los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="ea3bc-110">This article contains the following topics.</span></span>

-   [<span data-ttu-id="ea3bc-111">Mensajes de calidad</span><span class="sxs-lookup"><span data-stu-id="ea3bc-111">Quality Messages</span></span>](quality-messages.md)
-   [<span data-ttu-id="ea3bc-112">Control de calidad predeterminado</span><span class="sxs-lookup"><span data-stu-id="ea3bc-112">Default Quality Control</span></span>](default-quality-control.md)

## <a name="related-topics"></a><span data-ttu-id="ea3bc-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ea3bc-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea3bc-114">Flujo de datos para desarrolladores de filtros</span><span class="sxs-lookup"><span data-stu-id="ea3bc-114">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
</dt> <dt>

[<span data-ttu-id="ea3bc-115">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="ea3bc-115">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



