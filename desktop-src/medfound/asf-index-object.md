---
description: Indexador ASF
ms.assetid: 3f95b0ac-d70f-4bc2-8524-c7de1df34afa
title: Indexador ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c729b547339149ee578a90283c570ec8460b0c57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696186"
---
# <a name="asf-indexer"></a><span data-ttu-id="7e981-103">Indexador ASF</span><span class="sxs-lookup"><span data-stu-id="7e981-103">ASF Indexer</span></span>

<span data-ttu-id="7e981-104">El *indexador* ASF es un componente de nivel WMContainer que se usa para leer o escribir objetos de índice en un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="7e981-104">The ASF *indexer* is a WMContainer layer component that is used to read or write Index Objects in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="7e981-105">Para obtener información acerca de la estructura de un archivo ASF, consulte [ASF File Structure](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="7e981-105">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="7e981-106">Una aplicación puede utilizar el indexador para realizar búsquedas en función del tiempo de presentación o para generar nuevas entradas de índice para un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="7e981-106">An application can use the indexer to perform seeking based on presentation time or to generate new index entries for an ASF file.</span></span> <span data-ttu-id="7e981-107">El indizador ASF implementa la interfaz [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) .</span><span class="sxs-lookup"><span data-stu-id="7e981-107">The ASF indexer implements the [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) interface.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7e981-108">Tipo de índice</span><span class="sxs-lookup"><span data-stu-id="7e981-108">Index type</span></span></th>
<th><span data-ttu-id="7e981-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e981-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7e981-110">Índice basado en tiempo de presentación</span><span class="sxs-lookup"><span data-stu-id="7e981-110">Presentation time-based Index</span></span></td>
<td><span data-ttu-id="7e981-111">Proporciona una indización basada en el tiempo de presentación para secuencias de audio y vídeo en bloques de índice para que la indización tenga más espacio eficaz.</span><span class="sxs-lookup"><span data-stu-id="7e981-111">Provides presentation time-based indexing for audio and video streams in index blocks to make indexing more space efficient.</span></span> <span data-ttu-id="7e981-112">Cada bloque de índice hace referencia a las entradas de índice que contienen un desplazamiento de bytes.</span><span class="sxs-lookup"><span data-stu-id="7e981-112">Each index block references index entries that contain a byte offset.</span></span> <br/> <span data-ttu-id="7e981-113">El desplazamiento es la posición del paquete de datos en el que se realiza la búsqueda, en relación con el inicio del objeto de datos ASF.</span><span class="sxs-lookup"><span data-stu-id="7e981-113">The offset is the position of the data packet being seeked, relative to the start of the ASF Data Object.</span></span><br/> <span data-ttu-id="7e981-114">GUID_NULL debe usarse como el tipo GUID para el identificador de índice.</span><span class="sxs-lookup"><span data-stu-id="7e981-114">GUID_NULL must be used as the GUID type for the index identifier.</span></span> <span data-ttu-id="7e981-115">Para obtener más información, consulte <a href="using-the-indexer-to-write-a-new-index.md">uso del indexador para escribir un nuevo índice</a>.</span><span class="sxs-lookup"><span data-stu-id="7e981-115">For more information; see <a href="using-the-indexer-to-write-a-new-index.md">Using the Indexer to Write a New Index</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e981-116">Índice de código de tiempo</span><span class="sxs-lookup"><span data-stu-id="7e981-116">Timecode Index</span></span></td>
<td><span data-ttu-id="7e981-117">Facilita la búsqueda por código de tiempo en secuencias que contienen metadatos de código de tiempo.</span><span class="sxs-lookup"><span data-stu-id="7e981-117">Facilitates seeking by timecode in streams which contain timecode metadata.</span></span> <span data-ttu-id="7e981-118">Los códigos de tiempo se ajustan a un formato SMPTE (<em>horas: minutos: segundos: fotogramas</em>).</span><span class="sxs-lookup"><span data-stu-id="7e981-118">The timecodes conform to a SMPTE format (<em>Hours:Minutes:Seconds:Frames</em>).</span></span> <span data-ttu-id="7e981-119">Cada bloque de índice hace referencia a las entradas de índice que contienen un desplazamiento de bytes.</span><span class="sxs-lookup"><span data-stu-id="7e981-119">Each index block references index entries that contain a byte offset.</span></span> <br/> <span data-ttu-id="7e981-120">El desplazamiento es la posición del paquete de datos en el que se realiza la búsqueda, en relación con el inicio del objeto de datos ASF.</span><span class="sxs-lookup"><span data-stu-id="7e981-120">The offset is the position of the data packet being seeked, relative to the start of the ASF Data Object.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7e981-121">Los objetos de índice de código de tiempo no se admiten actualmente.</span><span class="sxs-lookup"><span data-stu-id="7e981-121">Timecode index objects are not currently supported.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e981-122">Índice basado en marco</span><span class="sxs-lookup"><span data-stu-id="7e981-122">Frame-based Index</span></span></td>
<td><span data-ttu-id="7e981-123">Proporciona índices basados en marcos para las secuencias de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7e981-123">Provides frame-based indexing for video streams.</span></span> <span data-ttu-id="7e981-124">Los índices en el índice basado en fotogramas están en términos de números de fotogramas, con el primer fotograma de una secuencia en el archivo ASF correspondiente a la entrada 0 en el objeto de índice basado en marco.</span><span class="sxs-lookup"><span data-stu-id="7e981-124">Indexes into the frame-based index are in terms of frame numbers, with the first frame for a stream in the ASF file corresponding to entry 0 in the frame-based index object.</span></span> <span data-ttu-id="7e981-125">Cada bloque de índice hace referencia a las entradas de índice que contienen un desplazamiento de bytes.</span><span class="sxs-lookup"><span data-stu-id="7e981-125">Each index block references index entries that contain a byte offset.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7e981-126">Actualmente no se admiten objetos de índice basados en marcos.</span><span class="sxs-lookup"><span data-stu-id="7e981-126">Frame-based index objects are not currently supported.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7e981-127">Esta sección contiene los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="7e981-127">This section contains the following topics.</span></span>



| <span data-ttu-id="7e981-128">Tema</span><span class="sxs-lookup"><span data-stu-id="7e981-128">Topic</span></span>                                                                                | <span data-ttu-id="7e981-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e981-129">Description</span></span>                                                                                                                      |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e981-130">Creación y configuración de indexador</span><span class="sxs-lookup"><span data-stu-id="7e981-130">Indexer Creation and Configuration</span></span>](indexer-creation-and-configuration.md)         | <span data-ttu-id="7e981-131">Cómo crear un objeto de indexador y configurarlo para leer un índice existente o para escribir un nuevo objeto de índice ASF para un archivo.</span><span class="sxs-lookup"><span data-stu-id="7e981-131">How to create an indexer object and configure it for reading an existing index or for writing a new ASF Index Object for a file.</span></span> |
| [<span data-ttu-id="7e981-132">Usar el indexador para buscar en un archivo</span><span class="sxs-lookup"><span data-stu-id="7e981-132">Using the Indexer to Seek in a File</span></span>](using-the-indexer-to-seek.md)                 | <span data-ttu-id="7e981-133">Cómo usar el indizador para buscar en un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="7e981-133">How to use the indexer to seek within an ASF file.</span></span>                                                                               |
| [<span data-ttu-id="7e981-134">Usar el indexador para escribir un nuevo índice</span><span class="sxs-lookup"><span data-stu-id="7e981-134">Using the Indexer to Write a New Index</span></span>](using-the-indexer-to-write-a-new-index.md) | <span data-ttu-id="7e981-135">Cómo usar el indexador para generar entradas de índice y escribir un nuevo objeto index para un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="7e981-135">How to use the indexer to generate index entries and write a new Index Object for an ASF file.</span></span>                                   |



 

## <a name="related-topics"></a><span data-ttu-id="7e981-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7e981-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e981-137">Componentes de WMContainer ASF</span><span class="sxs-lookup"><span data-stu-id="7e981-137">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="7e981-138">Compatibilidad con ASF en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7e981-138">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




