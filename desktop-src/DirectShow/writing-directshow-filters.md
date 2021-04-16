---
description: Escribir filtros de DirectShow
ms.assetid: ffbc92b2-4f45-439b-b140-49a66fc4d914
title: Escribir filtros de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2b266f3bbb9781dddcd2d0fb065b63d895a732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687154"
---
# <a name="writing-directshow-filters"></a><span data-ttu-id="623af-103">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="623af-103">Writing DirectShow Filters</span></span>

<span data-ttu-id="623af-104">Si va a desarrollar un filtro para usarlo en un gráfico de filtros de Microsoft DirectShow, lea los artículos de esta sección.</span><span class="sxs-lookup"><span data-stu-id="623af-104">If you are developing a filter for use in a Microsoft DirectShow filter graph, read the articles in this section.</span></span> <span data-ttu-id="623af-105">En general, no tiene que leer esta sección si está escribiendo una aplicación de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="623af-105">In general, you do not have to read this section if you are writing a DirectShow application.</span></span> <span data-ttu-id="623af-106">La mayoría de las aplicaciones no tienen acceso a los filtros ni al gráfico de filtros en el nivel descrito en esta sección.</span><span class="sxs-lookup"><span data-stu-id="623af-106">Most applications do not access filters or the filter graph at the level discussed in this section.</span></span>

-   [<span data-ttu-id="623af-107">Introducción al desarrollo de filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="623af-107">Introduction to DirectShow Filter Development</span></span>](introduction-to-directshow-filter-development.md)
-   [<span data-ttu-id="623af-108">Compilar filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="623af-108">Building DirectShow Filters</span></span>](building-directshow-filters.md)
-   [<span data-ttu-id="623af-109">Cómo se conectan los filtros</span><span class="sxs-lookup"><span data-stu-id="623af-109">How Filters Connect</span></span>](how-filters-connect.md)
-   [<span data-ttu-id="623af-110">Flujo de datos para desarrolladores de filtros</span><span class="sxs-lookup"><span data-stu-id="623af-110">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
-   [<span data-ttu-id="623af-111">Subprocesos y secciones críticas</span><span class="sxs-lookup"><span data-stu-id="623af-111">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
-   [<span data-ttu-id="623af-112">Administración de control de calidad</span><span class="sxs-lookup"><span data-stu-id="623af-112">Quality-Control Management</span></span>](quality-control-management.md)
-   [<span data-ttu-id="623af-113">DirectShow y COM</span><span class="sxs-lookup"><span data-stu-id="623af-113">DirectShow and COM</span></span>](directshow-and-com.md)
-   [<span data-ttu-id="623af-114">Escribir filtros de origen</span><span class="sxs-lookup"><span data-stu-id="623af-114">Writing Source Filters</span></span>](writing-source-filters.md)
-   [<span data-ttu-id="623af-115">Escribir filtros de transformación</span><span class="sxs-lookup"><span data-stu-id="623af-115">Writing Transform Filters</span></span>](writing-transform-filters.md)
-   [<span data-ttu-id="623af-116">Escritura de representadores de vídeo</span><span class="sxs-lookup"><span data-stu-id="623af-116">Writing Video Renderers</span></span>](writing-video-renderers.md)
-   [<span data-ttu-id="623af-117">Escribir filtros de captura</span><span class="sxs-lookup"><span data-stu-id="623af-117">Writing Capture Filters</span></span>](writing-capture-filters.md)
-   [<span data-ttu-id="623af-118">Exponer los formatos de captura y compresión</span><span class="sxs-lookup"><span data-stu-id="623af-118">Exposing Capture and Compression Formats</span></span>](exposing-capture-and-compression-formats.md)
-   [<span data-ttu-id="623af-119">Registro de un tipo de archivo personalizado</span><span class="sxs-lookup"><span data-stu-id="623af-119">Registering a Custom File Type</span></span>](registering-a-custom-file-type.md)
-   [<span data-ttu-id="623af-120">Crear una página de propiedades de filtro</span><span class="sxs-lookup"><span data-stu-id="623af-120">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)

 

 



