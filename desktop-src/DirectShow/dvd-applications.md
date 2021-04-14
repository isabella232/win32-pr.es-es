---
description: Aplicaciones de DVD
ms.assetid: 6f41e0f1-e550-4ca6-9a80-ce4d498289e2
title: Aplicaciones de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acaddc683078acff84b7c90689f82becfb7b1d7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359969"
---
# <a name="dvd-applications"></a><span data-ttu-id="0cfb8-103">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="0cfb8-103">DVD Applications</span></span>

<span data-ttu-id="0cfb8-104">DirectShow proporciona un componente denominado filtro de origen de [DVD Navigator](dvd-navigator-filter.md) que simplifica las tareas de navegación por DVD en C++.</span><span class="sxs-lookup"><span data-stu-id="0cfb8-104">DirectShow provides a component called the [DVD Navigator](dvd-navigator-filter.md) source filter which simplifies DVD navigation tasks in C++.</span></span> <span data-ttu-id="0cfb8-105">El navegador de DVD tiene todas las capacidades que se encuentran en un reproductor de DVD independiente, además de otras funciones específicas para la reproducción de DVD en equipos personales.</span><span class="sxs-lookup"><span data-stu-id="0cfb8-105">The DVD Navigator has all the capabilities that you find on a full-featured stand-alone DVD player, plus additional capabilities specific to playing DVDs on personal computers.</span></span> <span data-ttu-id="0cfb8-106">Con el explorador de DVD, los desarrolladores de C++ y de scripting pueden crear aplicaciones de DVD completas sin hacer referencia a la especificación de DVD.</span><span class="sxs-lookup"><span data-stu-id="0cfb8-106">Using the DVD Navigator, C++ and scripting developers can create full-featured DVD applications without referring to the DVD specification.</span></span> <span data-ttu-id="0cfb8-107">El navegador del DVD, en coordinación con los filtros del descodificador, también controla la administración regional y la protección de los derechos de autor (CSS y la protección de la copia analógica), aislando a los desarrolladores de aplicaciones de estos detalles.</span><span class="sxs-lookup"><span data-stu-id="0cfb8-107">The DVD Navigator, in coordination with the decoder filters, also handles regional management and copyright protection (CSS and analog copy protection), isolating application developers from these details.</span></span>

<span data-ttu-id="0cfb8-108">El filtro del explorador de DVD funciona en todo un volumen de DVD-Video, que consta de los archivos del directorio de vídeo de \_ TS.</span><span class="sxs-lookup"><span data-stu-id="0cfb8-108">The DVD Navigator filter works across an entire DVD-Video volume, which consists of the files in the VIDEO\_TS directory.</span></span> <span data-ttu-id="0cfb8-109">A diferencia de la mayoría de los filtros de origen de DirectShow que funcionan con secuencias o archivos individuales, el navegador de DVD utiliza la estructura de DVD-Video de títulos, capítulos y códigos de hora.</span><span class="sxs-lookup"><span data-stu-id="0cfb8-109">Unlike most DirectShow source filters that work with individual streams or files, the DVD Navigator uses the DVD-Video structure of titles, chapters, and time codes.</span></span> <span data-ttu-id="0cfb8-110">Los desarrolladores que deseen reproducir archivos MPEG-2 individuales en DirectShow deben usar el [demultiplexador MPEG-2](mpeg-2-demultiplexer.md) en lugar del filtro del navegador de DVD.</span><span class="sxs-lookup"><span data-stu-id="0cfb8-110">Developers wishing to play individual MPEG-2 files in DirectShow should use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) instead of the DVD Navigator filter.</span></span> <span data-ttu-id="0cfb8-111">Para obtener más información [, consulte compatibilidad con MPEG-2 en DirectShow](mpeg-2-support-in-directshow.md) .</span><span class="sxs-lookup"><span data-stu-id="0cfb8-111">See [MPEG-2 Support in DirectShow](mpeg-2-support-in-directshow.md) for more information.</span></span>

> [!Note]  
> <span data-ttu-id="0cfb8-112">Para reproducir DVDs, el usuario debe tener un descodificador MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="0cfb8-112">To play DVDs, the user must have an MPEG-2 decoder.</span></span>

 

<span data-ttu-id="0cfb8-113">Esta sección contiene los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="0cfb8-113">This section contains the following topics.</span></span>

-   [<span data-ttu-id="0cfb8-114">Características de compatibilidad con DVD en DirectShow</span><span class="sxs-lookup"><span data-stu-id="0cfb8-114">DVD Support Features in DirectShow</span></span>](dvd-support-features-in-directshow.md)
-   [<span data-ttu-id="0cfb8-115">Conceptos básicos de DVD</span><span class="sxs-lookup"><span data-stu-id="0cfb8-115">DVD Basics</span></span>](dvd-basics.md)
-   [<span data-ttu-id="0cfb8-116">Creación del gráfico de filtros de DVD</span><span class="sxs-lookup"><span data-stu-id="0cfb8-116">Building the DVD Filter Graph</span></span>](building-the-dvd-filter-graph.md)
-   [<span data-ttu-id="0cfb8-117">Obtener los punteros de interfaz de DVD</span><span class="sxs-lookup"><span data-stu-id="0cfb8-117">Obtaining the DVD Interface Pointers</span></span>](obtaining-the-dvd-interface-pointers.md)
-   [<span data-ttu-id="0cfb8-118">Comandos de DVD</span><span class="sxs-lookup"><span data-stu-id="0cfb8-118">DVD Commands</span></span>](dvd-commands.md)
-   [<span data-ttu-id="0cfb8-119">Identificación de las operaciones de DVD válidas</span><span class="sxs-lookup"><span data-stu-id="0cfb8-119">Identifying Valid DVD Operations</span></span>](identifying-valid-dvd-operations.md)
-   [<span data-ttu-id="0cfb8-120">Sincronizar comandos de DVD</span><span class="sxs-lookup"><span data-stu-id="0cfb8-120">Synchronizing DVD Commands</span></span>](synchronizing-dvd-commands.md)
-   [<span data-ttu-id="0cfb8-121">Flujo de datos en el navegador de DVD</span><span class="sxs-lookup"><span data-stu-id="0cfb8-121">Data Flow in the DVD Navigator</span></span>](data-flow-in-the-dvd-navigator.md)
-   [<span data-ttu-id="0cfb8-122">Control de las notificaciones de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="0cfb8-122">Handling DVD Event Notifications</span></span>](handling-dvd-event-notifications.md)
-   [<span data-ttu-id="0cfb8-123">Trabajar con menús de DVD</span><span class="sxs-lookup"><span data-stu-id="0cfb8-123">Working With DVD Menus</span></span>](working-with-dvd-menus.md)
-   [<span data-ttu-id="0cfb8-124">Secuencias de audio y subimagen</span><span class="sxs-lookup"><span data-stu-id="0cfb8-124">Audio and Subpicture Streams</span></span>](audio-and-subpicture-streams.md)
-   [<span data-ttu-id="0cfb8-125">Aplicar niveles de administración parental</span><span class="sxs-lookup"><span data-stu-id="0cfb8-125">Enforcing Parental Management Levels</span></span>](enforcing-parental-management-levels.md)
-   [<span data-ttu-id="0cfb8-126">Guardar y restaurar objetos DvdState</span><span class="sxs-lookup"><span data-stu-id="0cfb8-126">Saving and Restoring DvdState Objects</span></span>](saving-and-restoring-dvdstate-objects.md)
-   [<span data-ttu-id="0cfb8-127">Trabajar con cadenas de texto de DVD</span><span class="sxs-lookup"><span data-stu-id="0cfb8-127">Working with DVD Text Strings</span></span>](working-with-dvd-text-strings.md)
-   [<span data-ttu-id="0cfb8-128">Reproducir flujos de audio de karaoke</span><span class="sxs-lookup"><span data-stu-id="0cfb8-128">Playing Karaoke Audio Streams</span></span>](playing-karaoke-audio-streams.md)
-   [<span data-ttu-id="0cfb8-129">Control de expulsaciones de disco</span><span class="sxs-lookup"><span data-stu-id="0cfb8-129">Handling Disc Ejections</span></span>](handling-disc-ejections.md)
-   [<span data-ttu-id="0cfb8-130">Mejoras en la reproducción de DVD en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0cfb8-130">DVD Playback Enhancements in Windows Vista</span></span>](dvd-playback-enhancements-in-windows-vista.md)
-   [<span data-ttu-id="0cfb8-131">Configuración del gráfico de filtros de DVD</span><span class="sxs-lookup"><span data-stu-id="0cfb8-131">DVD Filter Graph Configuration</span></span>](dvd-filter-graph-configuration.md)
-   [<span data-ttu-id="0cfb8-132">Accesos directos a páginas de referencia de DVD de C++</span><span class="sxs-lookup"><span data-stu-id="0cfb8-132">Shortcuts to C++ DVD Reference Pages</span></span>](shortcuts-to-c-dvd-reference-pages.md)

<span data-ttu-id="0cfb8-133">Para obtener referencias sobre el desarrollo de descodificadores de DVD/MPEG2, consulte [desarrollo de descodificadores de DVD en DirectShow](dvd-decoder-development-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="0cfb8-133">For references on DVD/MPEG2 decoder development, see [DVD Decoder Development in DirectShow](dvd-decoder-development-in-directshow.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cfb8-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0cfb8-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cfb8-135">Usar DirectShow</span><span class="sxs-lookup"><span data-stu-id="0cfb8-135">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



