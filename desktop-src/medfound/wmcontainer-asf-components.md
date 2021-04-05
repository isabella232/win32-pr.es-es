---
description: Los objetos WMContainer proporcionan un control de bajo nivel sobre el análisis y la escritura de un archivo de formato de sistema avanzado (ASF).
ms.assetid: 258ea139-581f-4b94-9655-43ecf1e77f10
title: Componentes de WMContainer ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d7d1c1b76683cfe01dc0970ab1c077580215d2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002099"
---
# <a name="wmcontainer-asf-components"></a><span data-ttu-id="350f0-103">Componentes de WMContainer ASF</span><span class="sxs-lookup"><span data-stu-id="350f0-103">WMContainer ASF Components</span></span>

<span data-ttu-id="350f0-104">Los objetos WMContainer proporcionan un control de bajo nivel sobre el análisis y la escritura de un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="350f0-104">The WMContainer objects provide low-level control over parsing and writing an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="350f0-105">Los [componentes ASF de capa de canalización](pipeline-layer-asf-components.md) usan los objetos WMContainer internamente.</span><span class="sxs-lookup"><span data-stu-id="350f0-105">The [Pipeline Layer ASF Components](pipeline-layer-asf-components.md) use the WMContainer objects internally.</span></span> <span data-ttu-id="350f0-106">La mayoría de las aplicaciones deben usar los componentes de canalización, en lugar de usar objetos WMContainer.</span><span class="sxs-lookup"><span data-stu-id="350f0-106">Most applications should use the pipeline components, rather than using WMContainer objects.</span></span> <span data-ttu-id="350f0-107">Use WMContainer solo si necesita un control de bajo nivel sobre el análisis y la escritura de un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="350f0-107">Use WMContainer only if you require low-level control over parsing and writing an ASF file.</span></span>

<span data-ttu-id="350f0-108">El nivel WMContainer incluye los siguientes objetos:</span><span class="sxs-lookup"><span data-stu-id="350f0-108">The WMContainer layer includes the following objects:</span></span>

-   [<span data-ttu-id="350f0-109">Perfil ASF</span><span class="sxs-lookup"><span data-stu-id="350f0-109">ASF Profile</span></span>](asf-profile.md)
-   [<span data-ttu-id="350f0-110">Objeto ContentInfo de ASF</span><span class="sxs-lookup"><span data-stu-id="350f0-110">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
-   [<span data-ttu-id="350f0-111">Divisor ASF</span><span class="sxs-lookup"><span data-stu-id="350f0-111">ASF Splitter</span></span>](asf-splitter.md)
-   [<span data-ttu-id="350f0-112">Multiplexor ASF</span><span class="sxs-lookup"><span data-stu-id="350f0-112">ASF Multiplexer</span></span>](asf-multiplexer.md)
-   [<span data-ttu-id="350f0-113">Indexador ASF</span><span class="sxs-lookup"><span data-stu-id="350f0-113">ASF Indexer</span></span>](asf-index-object.md)

<span data-ttu-id="350f0-114">Los temas siguientes contienen instrucciones paso a paso sobre el uso de WMContainer para leer o escribir archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="350f0-114">The following topics contain step-by-step instructions about using WMContainer to read or write ASF files.</span></span>

-   [<span data-ttu-id="350f0-115">Tutorial: lectura de un archivo ASF mediante objetos WMContainer</span><span class="sxs-lookup"><span data-stu-id="350f0-115">Tutorial: Reading an ASF File by Using WMContainer Objects</span></span>](tutorial--reading-an-asf-file.md)
-   [<span data-ttu-id="350f0-116">Tutorial: copiar secuencias ASF mediante objetos WMContainer</span><span class="sxs-lookup"><span data-stu-id="350f0-116">Tutorial: Copying ASF Streams by Using WMContainer Objects</span></span>](tutorial--copying-asf-streams-from-one-file-to-another.md)
-   [<span data-ttu-id="350f0-117">Tutorial: escribir un archivo WMA con objetos WMContainer</span><span class="sxs-lookup"><span data-stu-id="350f0-117">Tutorial: Writing a WMA File by Using WMContainer Objects</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)

## <a name="about-wm-container"></a><span data-ttu-id="350f0-118">Acerca del contenedor de WM</span><span class="sxs-lookup"><span data-stu-id="350f0-118">About WM Container</span></span>

<span data-ttu-id="350f0-119">Los objetos WMContainer interactúan directamente con los objetos de archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="350f0-119">The WMContainer objects interact directly with ASF file objects.</span></span> <span data-ttu-id="350f0-120">En el diagrama siguiente se muestra la estructura de archivos ASF y los objetos WMContainer correspondientes.</span><span class="sxs-lookup"><span data-stu-id="350f0-120">The following diagram shows the ASF file structure and the corresponding WMContainer objects.</span></span>

![diagrama que muestra la estructura de archivos ASF y los objetos de Media Foundation correspondientes](images/asf-components01.png)

<span data-ttu-id="350f0-122">A excepción del divisor y multiplexador, cada uno de estos objetos admite tanto el análisis (lectura) como la escritura de archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="350f0-122">Except for the splitter and multiplexer, each of these objects supports both parsing (reading) and writing ASF files.</span></span> <span data-ttu-id="350f0-123">El divisor solo se utiliza para leer archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="350f0-123">The splitter is used only for reading ASF files.</span></span> <span data-ttu-id="350f0-124">El multiplexor solo se usa para crear nuevos archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="350f0-124">The multiplexer is used only for authoring new ASF files.</span></span>

<span data-ttu-id="350f0-125">Todas las operaciones realizadas por objetos WMContainer son sincrónicas, lo que significa que bloquean el subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="350f0-125">All operations performed by WMContainer objects are synchronous, meaning they block the calling thread.</span></span>

## <a name="related-topics"></a><span data-ttu-id="350f0-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="350f0-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="350f0-127">Compatibilidad con ASF en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="350f0-127">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



