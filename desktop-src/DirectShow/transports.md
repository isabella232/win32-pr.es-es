---
description: Transportes
ms.assetid: 63c5ff5b-293d-4a80-92e8-3ece41321095
title: Transportes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3d87ffacc871fc45ef1e8e645849afc956fb1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687726"
---
# <a name="transports"></a><span data-ttu-id="ee937-103">Transportes</span><span class="sxs-lookup"><span data-stu-id="ee937-103">Transports</span></span>

<span data-ttu-id="ee937-104">Para poder trasladar los datos multimedia a través del gráfico de filtro, un filtro DirectShow debe admitir uno de varios protocolos posibles.</span><span class="sxs-lookup"><span data-stu-id="ee937-104">In order to move media data through the filter graph, a DirectShow filter must support one of several possible protocols.</span></span> <span data-ttu-id="ee937-105">Estos protocolos se denominan transportes.</span><span class="sxs-lookup"><span data-stu-id="ee937-105">These protocols are called transports.</span></span> <span data-ttu-id="ee937-106">Cuando dos filtros se conectan, deben admitir el mismo transporte. en caso contrario, no pueden intercambiar datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="ee937-106">When two filters connect, they must support the same transport; otherwise they cannot exchange media data.</span></span> <span data-ttu-id="ee937-107">Normalmente, un transporte requiere que uno de los pin admita una interfaz determinada.</span><span class="sxs-lookup"><span data-stu-id="ee937-107">Typically, a transport requires that one of the pins support a particular interface.</span></span> <span data-ttu-id="ee937-108">Cuando los filtros se conectan, un PIN consulta el otro para la interfaz.</span><span class="sxs-lookup"><span data-stu-id="ee937-108">When the filters connect, one pin queries the other for the interface.</span></span>

<span data-ttu-id="ee937-109">La mayoría de los filtros de DirectShow contienen datos multimedia en la memoria principal y los entregan a otros filtros a través de conexiones de PIN.</span><span class="sxs-lookup"><span data-stu-id="ee937-109">Most DirectShow filters hold media data in main memory, and deliver it to other filters across pin connections.</span></span> <span data-ttu-id="ee937-110">Este tipo de transporte se denomina transporte de memoria local.</span><span class="sxs-lookup"><span data-stu-id="ee937-110">This type of transport is called local memory transport.</span></span> <span data-ttu-id="ee937-111">Aunque el transporte de memoria local es el transporte más común en DirectShow, no todos los filtros lo usan.</span><span class="sxs-lookup"><span data-stu-id="ee937-111">Although local memory transport is the most common transport in DirectShow, not all filters use it.</span></span> <span data-ttu-id="ee937-112">Por ejemplo, algunos filtros envían datos multimedia a lo largo de una ruta de hardware y usan PIN solo para proporcionar información de control.</span><span class="sxs-lookup"><span data-stu-id="ee937-112">For example, some filters send media data along a hardware path, and use pins only to deliver control information.</span></span> <span data-ttu-id="ee937-113">Por ejemplo, vea la interfaz [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) .</span><span class="sxs-lookup"><span data-stu-id="ee937-113">For example, see the [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) interface.</span></span>

<span data-ttu-id="ee937-114">DirectShow define dos mecanismos para el transporte de memoria local, el modelo de inserción y el modelo de extracción.</span><span class="sxs-lookup"><span data-stu-id="ee937-114">DirectShow defines two mechanisms for local memory transport, the push model and the pull model.</span></span> <span data-ttu-id="ee937-115">En el modelo de insertar, un filtro de origen genera datos y los entrega al siguiente filtro de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="ee937-115">In the push model, a source filter generates data and delivers it to the next filter downstream.</span></span> <span data-ttu-id="ee937-116">Ese filtro recibe los datos de forma pasiva, los procesa y los envía más abajo.</span><span class="sxs-lookup"><span data-stu-id="ee937-116">That filter passively receives the data, processes it, and sends it further downstream.</span></span> <span data-ttu-id="ee937-117">En el modelo de extracción, el filtro de origen se conecta a un filtro de analizador.</span><span class="sxs-lookup"><span data-stu-id="ee937-117">In the pull model, the source filter is connected to a parser filter.</span></span> <span data-ttu-id="ee937-118">El filtro del analizador solicita datos del filtro de origen.</span><span class="sxs-lookup"><span data-stu-id="ee937-118">The parser filter requests data from the source filter.</span></span> <span data-ttu-id="ee937-119">El filtro de origen responde a las solicitudes mediante la entrega de datos.</span><span class="sxs-lookup"><span data-stu-id="ee937-119">The source filter responds to the requests by delivering data.</span></span> <span data-ttu-id="ee937-120">El modelo de inserción usa la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) y el modelo de extracción usa la interfaz [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="ee937-120">The push model uses the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface, and the pull model uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

<span data-ttu-id="ee937-121">El modelo de inserción es más común que el modelo de extracción.</span><span class="sxs-lookup"><span data-stu-id="ee937-121">The push model is more common than the pull model.</span></span> <span data-ttu-id="ee937-122">Por lo tanto, los artículos siguientes suponen un modelo de inserciones.</span><span class="sxs-lookup"><span data-stu-id="ee937-122">Therefore, the articles that follow assume a push model.</span></span> <span data-ttu-id="ee937-123">El último artículo de esta sección, [modelo de extracción](pull-model.md), describe el modo en que la interfaz **IAsyncReader** difiere de **IMemInputPin**.</span><span class="sxs-lookup"><span data-stu-id="ee937-123">The last article in this section, [Pull Model](pull-model.md), describes how the **IAsyncReader** interface differs from **IMemInputPin**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee937-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ee937-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee937-125">Flujo de datos en el gráfico de filtros</span><span class="sxs-lookup"><span data-stu-id="ee937-125">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



