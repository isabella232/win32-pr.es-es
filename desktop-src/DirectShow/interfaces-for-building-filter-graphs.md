---
description: Interfaces para generar gráficos de filtros
ms.assetid: 18d5217a-7f4e-49e9-ac14-2f4ba229e065
title: Interfaces para generar gráficos de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862d581f44a711cc6f2aa094210571995b15005b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805659"
---
# <a name="interfaces-for-building-filter-graphs"></a><span data-ttu-id="4a52a-103">Interfaces para generar gráficos de filtros</span><span class="sxs-lookup"><span data-stu-id="4a52a-103">Interfaces for Building Filter Graphs</span></span>

<span data-ttu-id="4a52a-104">Las aplicaciones usan estas interfaces para crear varios tipos de gráficos de filtros.</span><span class="sxs-lookup"><span data-stu-id="4a52a-104">Applications use these interfaces to build various types of filter graphs.</span></span>



| <span data-ttu-id="4a52a-105">Interfaz</span><span class="sxs-lookup"><span data-stu-id="4a52a-105">Interface</span></span>                                                  | <span data-ttu-id="4a52a-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a52a-106">Description</span></span>                                                 |
|------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="4a52a-107">**IAMFilterGraphCallback**</span><span class="sxs-lookup"><span data-stu-id="4a52a-107">**IAMFilterGraphCallback**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamfiltergraphcallback)   | <span data-ttu-id="4a52a-108">Recibir notificaciones de devolución de llamada si no se puede representar un PIN.</span><span class="sxs-lookup"><span data-stu-id="4a52a-108">Receive callback notifications if a pin cannot be rendered.</span></span> |
| [<span data-ttu-id="4a52a-109">**IAMGraphBuilderCallback**</span><span class="sxs-lookup"><span data-stu-id="4a52a-109">**IAMGraphBuilderCallback**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) | <span data-ttu-id="4a52a-110">Proporciona un mecanismo de devolución de llamada durante la creación del gráfico.</span><span class="sxs-lookup"><span data-stu-id="4a52a-110">Provides a callback mechanism during graph building.</span></span>        |
| [<span data-ttu-id="4a52a-111">**ICaptureGraphBuilder2**</span><span class="sxs-lookup"><span data-stu-id="4a52a-111">**ICaptureGraphBuilder2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)     | <span data-ttu-id="4a52a-112">Cree gráficos de filtro para la captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4a52a-112">Build filter graphs for video capture.</span></span>                      |
| [<span data-ttu-id="4a52a-113">**ICreateDevEnum**</span><span class="sxs-lookup"><span data-stu-id="4a52a-113">**ICreateDevEnum**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum)                   | <span data-ttu-id="4a52a-114">Enumerar dispositivos del sistema, como dispositivos de captura.</span><span class="sxs-lookup"><span data-stu-id="4a52a-114">Enumerate system devices, such as capture devices.</span></span>          |
| [<span data-ttu-id="4a52a-115">**IDvdGraphBuilder**</span><span class="sxs-lookup"><span data-stu-id="4a52a-115">**IDvdGraphBuilder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder)               | <span data-ttu-id="4a52a-116">Cree gráficos de filtros para la reproducción y la navegación de DVD.</span><span class="sxs-lookup"><span data-stu-id="4a52a-116">Build filter graphs for DVD navigation and playback.</span></span>        |
| [<span data-ttu-id="4a52a-117">**IEnumFilters**</span><span class="sxs-lookup"><span data-stu-id="4a52a-117">**IEnumFilters**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ienumfilters)                       | <span data-ttu-id="4a52a-118">Enumera los filtros del gráfico.</span><span class="sxs-lookup"><span data-stu-id="4a52a-118">Enumerate the filters in the graph.</span></span>                         |
| [<span data-ttu-id="4a52a-119">**IFilterGraph2**</span><span class="sxs-lookup"><span data-stu-id="4a52a-119">**IFilterGraph2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)                     | <span data-ttu-id="4a52a-120">Agregar, quitar o conectar filtros.</span><span class="sxs-lookup"><span data-stu-id="4a52a-120">Add, remove, or connect filters.</span></span>                            |
| [<span data-ttu-id="4a52a-121">**IFilterMapper2**</span><span class="sxs-lookup"><span data-stu-id="4a52a-121">**IFilterMapper2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)                   | <span data-ttu-id="4a52a-122">Enumera los filtros registrados en el sistema del usuario.</span><span class="sxs-lookup"><span data-stu-id="4a52a-122">Enumerate the filters registered on the user's system.</span></span>      |
| [<span data-ttu-id="4a52a-123">**IGraphBuilder**</span><span class="sxs-lookup"><span data-stu-id="4a52a-123">**IGraphBuilder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)                     | <span data-ttu-id="4a52a-124">Cree gráficos de filtro para la reproducción de archivos o para usos personalizados.</span><span class="sxs-lookup"><span data-stu-id="4a52a-124">Build filter graphs for file playback or for custom uses.</span></span>   |
| [<span data-ttu-id="4a52a-125">**IGraphConfig**</span><span class="sxs-lookup"><span data-stu-id="4a52a-125">**IGraphConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)                       | <span data-ttu-id="4a52a-126">Reconfigure dinámicamente un gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="4a52a-126">Dynamically reconfigure a filter graph.</span></span>                     |
| [<span data-ttu-id="4a52a-127">**IGraphVersion**</span><span class="sxs-lookup"><span data-stu-id="4a52a-127">**IGraphVersion**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphversion)                     | <span data-ttu-id="4a52a-128">Determine cuándo cambia el gráfico.</span><span class="sxs-lookup"><span data-stu-id="4a52a-128">Determine when the graph changes.</span></span>                           |



 

 

 



