---
description: Ventajas de DMOs
ms.assetid: 7ff3fd9c-9423-4915-8ce2-22783ed455fb
title: Ventajas de DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972b4f49ee19b271cbee970401933b6c7d6bd3ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274770"
---
# <a name="benefits-of-dmos"></a><span data-ttu-id="9d113-103">Ventajas de DMOs</span><span class="sxs-lookup"><span data-stu-id="9d113-103">Benefits of DMOs</span></span>

<span data-ttu-id="9d113-104">DMOs ofrecen las siguientes ventajas:</span><span class="sxs-lookup"><span data-stu-id="9d113-104">DMOs offer the following advantages:</span></span>

-   <span data-ttu-id="9d113-105">Suelen ser más pequeñas y más sencillas que los filtros de DirectShow, ya que admiten menos funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="9d113-105">They are generally smaller and simpler than DirectShow filters, because they support less functionality.</span></span>
-   <span data-ttu-id="9d113-106">Son más flexibles que los filtros de DirectShow porque no requieren un gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="9d113-106">They are more flexible than DirectShow filters because they do not require a filter graph.</span></span> <span data-ttu-id="9d113-107">Puede usarlos con DirectShow cuando necesite los servicios que proporciona DirectShow, como la sincronización, la conexión inteligente, el control automático del flujo de datos y la administración de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="9d113-107">You can use them with DirectShow when you need the services that DirectShow provides, such as synchronization, intelligent connection, automatic handling of data flow, and thread management.</span></span> <span data-ttu-id="9d113-108">Los clientes que no necesitan estos servicios pueden acceder a DMOs directamente.</span><span class="sxs-lookup"><span data-stu-id="9d113-108">Clients that do not need these services can access DMOs directly.</span></span>
-   <span data-ttu-id="9d113-109">DMOs siempre realiza el procesamiento de datos sincrónicos, lo que elimina muchos de los problemas de subprocesos que debe tener en cuenta si escribe un filtro.</span><span class="sxs-lookup"><span data-stu-id="9d113-109">DMOs always perform synchronous data processing, which eliminates many of the threading issues that you must consider if you write a filter.</span></span>
-   <span data-ttu-id="9d113-110">A diferencia de los códecs ACM y VCM tradicionales, los DMOs se basan en el modelo de objetos componentes (COM), por lo que se pueden extender a través de **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="9d113-110">Unlike traditional ACM and VCM codecs, DMOs are based on the Component Object Model (COM), so they can be extended through **QueryInterface**.</span></span>
-   <span data-ttu-id="9d113-111">DMOs admite un modelo de streaming más generalizado que los códecs ACM o VCM.</span><span class="sxs-lookup"><span data-stu-id="9d113-111">DMOs support a more generalized streaming model than ACM or VCM codecs.</span></span> <span data-ttu-id="9d113-112">Al igual que los filtros DirectShow, DMOs puede admitir varias entradas y varias salidas.</span><span class="sxs-lookup"><span data-stu-id="9d113-112">Like DirectShow filters, DMOs can support multiple inputs and multiple outputs.</span></span>

<span data-ttu-id="9d113-113">Por estos motivos, ahora se recomienda DMOs como solución para escribir codificadores, descodificadores y efectos de audio.</span><span class="sxs-lookup"><span data-stu-id="9d113-113">For these reasons, DMOs are now recommended as the solution for writing encoders, decoders, and audio effects.</span></span> <span data-ttu-id="9d113-114">También son posibles muchos otros escenarios, en función de las necesidades de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9d113-114">Many other scenarios are possible as well, depending on the needs of the application.</span></span>

<span data-ttu-id="9d113-115">Diferencias entre DMOs y filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="9d113-115">How DMOs Differ from DirectShow Filters</span></span>

<span data-ttu-id="9d113-116">Los filtros de DirectShow no funcionan fuera de un gráfico de filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9d113-116">DirectShow filters cannot function outside of a DirectShow filter graph.</span></span> <span data-ttu-id="9d113-117">En DirectShow, el administrador de gráficos de filtros media entre la aplicación y los filtros.</span><span class="sxs-lookup"><span data-stu-id="9d113-117">In DirectShow, the Filter Graph Manager mediates between the application and the filters.</span></span> <span data-ttu-id="9d113-118">Los filtros de DirectShow realizan la mayor parte del trabajo necesario para transmitir datos, entre los que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="9d113-118">DirectShow filters do most of the work required to stream data, including:</span></span>

-   <span data-ttu-id="9d113-119">Asignación de búferes.</span><span class="sxs-lookup"><span data-stu-id="9d113-119">Allocating buffers.</span></span>
-   <span data-ttu-id="9d113-120">Negociar tipos de medios y conexiones con otros filtros.</span><span class="sxs-lookup"><span data-stu-id="9d113-120">Negotiating media types and connections to other filters.</span></span>
-   <span data-ttu-id="9d113-121">Insertar datos a través del gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="9d113-121">Pushing data through the filter graph.</span></span>
-   <span data-ttu-id="9d113-122">Envío de eventos al administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="9d113-122">Sending events to the Filter Graph Manager.</span></span>
-   <span data-ttu-id="9d113-123">Sincronización de varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="9d113-123">Synchronizing multiple threads.</span></span>

<span data-ttu-id="9d113-124">En cambio, una DMO no realiza ninguna de estas acciones.</span><span class="sxs-lookup"><span data-stu-id="9d113-124">In contrast, a DMO does none of these things.</span></span> <span data-ttu-id="9d113-125">En su lugar, estos tipos de tareas son responsabilidad del cliente mediante DMO.</span><span class="sxs-lookup"><span data-stu-id="9d113-125">Instead, these kinds of tasks are the responsibility of the client using the DMO.</span></span> <span data-ttu-id="9d113-126">El cliente asigna búferes, los rellena con datos y los entrega a DMO.</span><span class="sxs-lookup"><span data-stu-id="9d113-126">The client allocates buffers, fills them with data, and delivers them to the DMO.</span></span> <span data-ttu-id="9d113-127">DMO procesa los datos y el cliente recupera los búferes de salida resultantes.</span><span class="sxs-lookup"><span data-stu-id="9d113-127">The DMO processes the data, and the client retrieves the resulting output buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d113-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9d113-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d113-129">Acerca de DMOs</span><span class="sxs-lookup"><span data-stu-id="9d113-129">About DMOs</span></span>](about-dmos.md)
</dt> </dl>

 

 



