---
description: En este tutorial se muestra cómo escribir una aplicación de DirectShow que reproduce un archivo multimedia.
ms.assetid: 88f4762a-e6e6-4b1e-9951-a409d9d80da9
title: Reproducción de audio y vídeo en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca3d681386d85eafc4f32b4e688b920253a51a7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659269"
---
# <a name="audiovideo-playback-in-directshow"></a><span data-ttu-id="32d01-103">Reproducción de audio y vídeo en DirectShow</span><span class="sxs-lookup"><span data-stu-id="32d01-103">Audio/Video Playback in DirectShow</span></span>

<span data-ttu-id="32d01-104">En este tutorial se muestra cómo escribir una aplicación de DirectShow que reproduce un archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="32d01-104">This tutorial shows how to write a DirectShow application that plays a media file.</span></span>

<span data-ttu-id="32d01-105">Antes de leer este tutorial, puede que desee leer los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="32d01-105">Before reading this tutorial, you might want to read the following topics:</span></span>

-   [<span data-ttu-id="32d01-106">Introducción a la programación de aplicaciones de DirectShow</span><span class="sxs-lookup"><span data-stu-id="32d01-106">Introduction to DirectShow Application Programming</span></span>](introduction-to-directshow-application-programming.md)
-   [<span data-ttu-id="32d01-107">Cómo reproducir un archivo</span><span class="sxs-lookup"><span data-stu-id="32d01-107">How To Play a File</span></span>](how-to-play-a-file.md)
-   [<span data-ttu-id="32d01-108">Acerca de los filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="32d01-108">About DirectShow Filters</span></span>](about-directshow-filters.md)
-   [<span data-ttu-id="32d01-109">Acerca del administrador de gráficos de filtros</span><span class="sxs-lookup"><span data-stu-id="32d01-109">About the Filter Graph Manager</span></span>](about-the-filter-graph-manager.md)

## <a name="in-this-section"></a><span data-ttu-id="32d01-110">En esta sección</span><span class="sxs-lookup"><span data-stu-id="32d01-110">In this section</span></span>

-   [<span data-ttu-id="32d01-111">Paso 1: declarar la clase DShowPlayer</span><span class="sxs-lookup"><span data-stu-id="32d01-111">Step 1: Declare the DShowPlayer Class</span></span>](step-1--declare-the-dshowplayer-class.md)
-   [<span data-ttu-id="32d01-112">Paso 2: declarar CVideoRenderer y clases derivadas</span><span class="sxs-lookup"><span data-stu-id="32d01-112">Step 2: Declare CVideoRenderer and Derived Classes</span></span>](step-2--declare-cvideorenderer-and-derived-classes.md)
-   [<span data-ttu-id="32d01-113">Paso 3: compilar el gráfico de filtro</span><span class="sxs-lookup"><span data-stu-id="32d01-113">Step 3: Build the Filter Graph</span></span>](step-3--build-the-filter-graph.md)
-   [<span data-ttu-id="32d01-114">Paso 4: agregar el representador de vídeo</span><span class="sxs-lookup"><span data-stu-id="32d01-114">Step 4: Add the Video Renderer</span></span>](step-4--add-the-video-renderer.md)
-   [<span data-ttu-id="32d01-115">Paso 5: agregar funcionalidad de vídeo</span><span class="sxs-lookup"><span data-stu-id="32d01-115">Step 5: Add Video Functionality</span></span>](step-5--add-video-functionality.md)
-   [<span data-ttu-id="32d01-116">Paso 6: control de eventos de gráfico</span><span class="sxs-lookup"><span data-stu-id="32d01-116">Step 6: Handle Graph Events</span></span>](step-6--handle-graph-events.md)
-   [<span data-ttu-id="32d01-117">Paso 7: controles de transporte</span><span class="sxs-lookup"><span data-stu-id="32d01-117">Step 7: Transport Controls</span></span>](step-7--transport-controls.md)
-   [<span data-ttu-id="32d01-118">Ejemplo de reproducción de DirectShow</span><span class="sxs-lookup"><span data-stu-id="32d01-118">DirectShow Playback Example</span></span>](directshow-playback-example.md)

## <a name="related-topics"></a><span data-ttu-id="32d01-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="32d01-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32d01-120">Usar DirectShow</span><span class="sxs-lookup"><span data-stu-id="32d01-120">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



