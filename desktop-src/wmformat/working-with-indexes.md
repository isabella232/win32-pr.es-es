---
title: Trabajar con índices
description: Trabajar con índices
ms.assetid: 7daa4b29-0597-462d-ad65-135d0ef7362d
keywords:
- Windows Media Format SDK, índices
- Advanced Systems Format (ASF), índices
- ASF (formato de sistemas avanzados), índices
- índices, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34057046223daf2e16950e0e38b1b0db5df32c4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903284"
---
# <a name="working-with-indexes"></a><span data-ttu-id="6e981-107">Trabajar con índices</span><span class="sxs-lookup"><span data-stu-id="6e981-107">Working with Indexes</span></span>

<span data-ttu-id="6e981-108">El SDK de Windows Media Format admite la búsqueda y el progresado a través del contenido.</span><span class="sxs-lookup"><span data-stu-id="6e981-108">The Windows Media Format SDK supports seeking and striding through content.</span></span> <span data-ttu-id="6e981-109">La búsqueda le permite especificar un lugar en la escala de tiempo del archivo para comenzar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="6e981-109">Seeking enables you to specify a place on the file's timeline to begin playback.</span></span> <span data-ttu-id="6e981-110">El avance le permite avanzar y rebobinar la salida de un archivo de forma rápida.</span><span class="sxs-lookup"><span data-stu-id="6e981-110">Striding enables you to fast-forward and rewind the output of a file.</span></span> <span data-ttu-id="6e981-111">Los archivos se deben indizar para aprovechar las ventajas de estas características.</span><span class="sxs-lookup"><span data-stu-id="6e981-111">Files must be indexed to take advantage of these features.</span></span> <span data-ttu-id="6e981-112">Un índice es una serie de valores que representan las posiciones del archivo (tiempos de presentación, números de marco o códigos de tiempo de SMTP) con los desplazamientos correspondientes en la sección de datos del archivo para cada uno.</span><span class="sxs-lookup"><span data-stu-id="6e981-112">An index is a series of values representing positions in the file (either presentation times, frame numbers, or SMTPE time codes) with corresponding offsets into the data section of the file for each.</span></span> <span data-ttu-id="6e981-113">La indexación es más importante para las secuencias de vídeo, ya que el tiempo de presentación de la secuencia de audio se puede estimar fácilmente.</span><span class="sxs-lookup"><span data-stu-id="6e981-113">Indexing is most important for video streams, as audio stream presentation time can be easily estimated.</span></span> <span data-ttu-id="6e981-114">Sin embargo, algunas secuencias de audio también pueden requerir índices.</span><span class="sxs-lookup"><span data-stu-id="6e981-114">However, some audio streams may require indexes as well.</span></span> <span data-ttu-id="6e981-115">De forma predeterminada, el escritor indexará cada nuevo archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="6e981-115">By default, the writer will index every new ASF file.</span></span> <span data-ttu-id="6e981-116">Si se realizan cambios en el contenido de un archivo, debe actualizar el índice mediante el objeto indexador.</span><span class="sxs-lookup"><span data-stu-id="6e981-116">If changes are made to the content of a file, you must refresh the index yourself using the indexer object.</span></span>

<span data-ttu-id="6e981-117">El indexador admite la indexación temporal y la basada en tramas, así como la indexación basada en códigos de tiempo de SMPTE (si existen).</span><span class="sxs-lookup"><span data-stu-id="6e981-117">The indexer supports both temporal and frame-based indexing as well as indexing based on SMPTE time codes (if present).</span></span> <span data-ttu-id="6e981-118">El escritor creará un índice temporal de forma predeterminada para cada nueva secuencia de vídeo codificada en un archivo.</span><span class="sxs-lookup"><span data-stu-id="6e981-118">The writer will create a temporal index by default for every new video stream encoded to a file.</span></span> <span data-ttu-id="6e981-119">Debe configurar y llamar explícitamente al indexador para crear un índice de código de tiempo basado en marco o SMPTE.</span><span class="sxs-lookup"><span data-stu-id="6e981-119">You must explicitly configure and call the indexer to create a frame-based or SMPTE time code index.</span></span>

<span data-ttu-id="6e981-120">Cuando se realizan cambios en el contenido de un archivo ASF, se debe volver a indexar.</span><span class="sxs-lookup"><span data-stu-id="6e981-120">When changes are made to the content of an ASF file, it must be indexed again.</span></span>

<span data-ttu-id="6e981-121">En las secciones siguientes se muestra código de ejemplo para realizar tareas de indexación comunes.</span><span class="sxs-lookup"><span data-stu-id="6e981-121">The following sections present example code for performing common indexing tasks.</span></span>

-   [<span data-ttu-id="6e981-122">Para deshabilitar la indexación automática</span><span class="sxs-lookup"><span data-stu-id="6e981-122">To Disable Automatic Indexing</span></span>](to-disable-automatic-indexing.md)
-   [<span data-ttu-id="6e981-123">Para configurar el indexador</span><span class="sxs-lookup"><span data-stu-id="6e981-123">To Configure the Indexer</span></span>](to-configure-the-indexer.md)
-   [<span data-ttu-id="6e981-124">Para indexar un archivo ASF</span><span class="sxs-lookup"><span data-stu-id="6e981-124">To Index an ASF File</span></span>](to-index-an-asf-file.md)
-   [<span data-ttu-id="6e981-125">Para detener la indización en curso</span><span class="sxs-lookup"><span data-stu-id="6e981-125">To Stop Indexing in Progress</span></span>](to-stop-indexing-in-progress.md)

<span data-ttu-id="6e981-126">Además, la aplicación de ejemplo DSCopy muestra el uso del indexador.</span><span class="sxs-lookup"><span data-stu-id="6e981-126">In addition, the DSCopy sample application illustrates the use of the indexer.</span></span> <span data-ttu-id="6e981-127">Para obtener más información, vea [aplicaciones de ejemplo](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="6e981-127">For more information, see [Sample Applications](sample-applications.md).</span></span>

 

 




