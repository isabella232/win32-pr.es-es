---
description: Hospedar directamente un DMO
ms.assetid: 10fb99cf-78d9-4519-9aec-23b0daeca9e2
title: Hospedar directamente un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3c933cf4eb946abb9ffefd5186159595480887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806895"
---
# <a name="directly-hosting-a-dmo"></a><span data-ttu-id="21851-103">Hospedar directamente un DMO</span><span class="sxs-lookup"><span data-stu-id="21851-103">Directly Hosting a DMO</span></span>

<span data-ttu-id="21851-104">En esta sección se describe cómo una aplicación puede actuar como cliente directo de DMO.</span><span class="sxs-lookup"><span data-stu-id="21851-104">This section describes how an application can act as the direct client of a DMO.</span></span> <span data-ttu-id="21851-105">La aplicación entrega la entrada a DMO, el DMO crea la salida y la aplicación utiliza la salida para la representación, el procesamiento posterior o cualquier otra cosa.</span><span class="sxs-lookup"><span data-stu-id="21851-105">The application delivers input to the DMO, the DMO creates output, and the application uses the output for rendering, further processing, or anything else.</span></span> <span data-ttu-id="21851-106">La aplicación es responsable de los problemas, como la asignación de memoria, el control de tiempo y la sincronización, y el subprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="21851-106">The application is responsible for issues such as memory allocation, timing and synchronization, and threading.</span></span> <span data-ttu-id="21851-107">Estos requisitos dependerán de la naturaleza de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="21851-107">These requirements will depend on the nature of the application.</span></span>

<span data-ttu-id="21851-108">La información de esta sección también se aplica si está escribiendo un componente que actúa como una capa entre una aplicación y un DMO (por ejemplo, un control ActiveX que hospeda un DMO).</span><span class="sxs-lookup"><span data-stu-id="21851-108">The information in this section also applies if you are writing a component that acts as a layer between an application and a DMO (for example, an ActiveX Control that hosts a DMO).</span></span> <span data-ttu-id="21851-109">Además, debe leer esta sección si está escribiendo un DMO, ya que describe la funcionalidad que debe implementar DMO.</span><span class="sxs-lookup"><span data-stu-id="21851-109">In addition, you should read this section if you are writing a DMO, because it describes the functionality that your DMO must implement.</span></span>

<span data-ttu-id="21851-110">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="21851-110">This section contains the following topics:</span></span>

-   [<span data-ttu-id="21851-111">Establecimiento de tipos de medios en DMO</span><span class="sxs-lookup"><span data-stu-id="21851-111">Setting Media Types on a DMO</span></span>](setting-media-types-on-a-dmo.md)
-   [<span data-ttu-id="21851-112">Procesamiento de datos en una DMO</span><span class="sxs-lookup"><span data-stu-id="21851-112">Processing Data in a DMO</span></span>](processing-data-in-a-dmo.md)
-   [<span data-ttu-id="21851-113">Procesamiento en contexto</span><span class="sxs-lookup"><span data-stu-id="21851-113">In-Place Processing</span></span>](in-place-processing.md)
-   [<span data-ttu-id="21851-114">Flujos opcionales</span><span class="sxs-lookup"><span data-stu-id="21851-114">Optional Streams</span></span>](optional-streams.md)
-   [<span data-ttu-id="21851-115">Implementación de IMediaBuffer</span><span class="sxs-lookup"><span data-stu-id="21851-115">Implementing IMediaBuffer</span></span>](implementing-imediabuffer.md)

## <a name="related-topics"></a><span data-ttu-id="21851-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="21851-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21851-117">Usar DMOs</span><span class="sxs-lookup"><span data-stu-id="21851-117">Using DMOs</span></span>](using-dmos.md)
</dt> </dl>

 

 



