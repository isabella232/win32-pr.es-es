---
title: Indexer (objeto)
description: Indexer (objeto)
ms.assetid: 652e04a5-ed6e-4e92-acf4-55ed82f77ef1
keywords:
- SDK de Windows Media Format, objetos de indexador
- Advanced Systems Format (ASF), objetos de indexador
- ASF (formato de sistemas avanzados), objetos de indexador
- objetos, objetos de indexador
- objetos de indexador
- índices, objetos de indexador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c9aa8c1c3ff694ae8e125e17dc0190451c7f21
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "104077429"
---
# <a name="indexer-object"></a><span data-ttu-id="85980-109">Indexer (objeto)</span><span class="sxs-lookup"><span data-stu-id="85980-109">Indexer Object</span></span>

<span data-ttu-id="85980-110">El objeto indexador crea un índice en un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="85980-110">The indexer object creates an index in an ASF file.</span></span> <span data-ttu-id="85980-111">Un índice es una parte estándar de un archivo ASF que equipara las muestras de vídeo con las horas, los números de fotogramas o, si procede, la sociedad de las marcas de tiempo estándar de las imágenes de movimiento y los ingenieros de televisión (SMPTE).</span><span class="sxs-lookup"><span data-stu-id="85980-111">An index is a standard part of an ASF file that equates video samples with times, frame numbers, or (if applicable) Society of Motion Picture and Television Engineers (SMPTE) standard time stamps.</span></span> <span data-ttu-id="85980-112">Sin un índice, ni el objeto lector ni el objeto lector sincrónico pueden buscar un punto en medio de un archivo.</span><span class="sxs-lookup"><span data-stu-id="85980-112">Without an index, neither the reader object nor the synchronous reader object can seek to a point in the middle of a file.</span></span>

<span data-ttu-id="85980-113">Los índices creados por este objeto solo son necesarios si el archivo contiene una o varias secuencias de vídeo.</span><span class="sxs-lookup"><span data-stu-id="85980-113">Indexes created by this object are only necessary if the file contains one or more video streams.</span></span> <span data-ttu-id="85980-114">Esto se debe a que los datos de audio no se comprimen temporalmente, lo que facilita la búsqueda de un tiempo determinado en una secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="85980-114">This is because audio data is not temporally compressed, making it easy to find a given time in an audio stream.</span></span>

<span data-ttu-id="85980-115">El objeto de indexador se crea mediante la función [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) , que establece un puntero a una interfaz **IWMIndexer** .</span><span class="sxs-lookup"><span data-stu-id="85980-115">The indexer object is created by the [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) function, which sets a pointer to an **IWMIndexer** interface.</span></span> <span data-ttu-id="85980-116">Las demás interfaces del objeto indexador se pueden obtener llamando al método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="85980-116">The other interfaces of the indexer object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="85980-117">El objeto de indexador admite las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="85980-117">The following interfaces are supported by the indexer object.</span></span>



| <span data-ttu-id="85980-118">Interfaz</span><span class="sxs-lookup"><span data-stu-id="85980-118">Interface</span></span>                          | <span data-ttu-id="85980-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="85980-119">Description</span></span>                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="85980-120">**IWMIndexer**</span><span class="sxs-lookup"><span data-stu-id="85980-120">**IWMIndexer**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)   | <span data-ttu-id="85980-121">Inicia y detiene el proceso de indización.</span><span class="sxs-lookup"><span data-stu-id="85980-121">Starts and stops the indexing process.</span></span>                                              |
| [<span data-ttu-id="85980-122">**IWMIndexer2**</span><span class="sxs-lookup"><span data-stu-id="85980-122">**IWMIndexer2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer2) | <span data-ttu-id="85980-123">Configura el indexador, habilitando la indexación por fotograma, por hora o por código de tiempo de SMPTE.</span><span class="sxs-lookup"><span data-stu-id="85980-123">Configures the indexer, enabling indexing by frame, by time, or by SMPTE time code.</span></span> |



 

<span data-ttu-id="85980-124">La aplicación debe implementar la siguiente interfaz de devolución de llamada para poder usar el objeto de indexador.</span><span class="sxs-lookup"><span data-stu-id="85980-124">The following callback interface must be implemented by the application in order to use the indexer object.</span></span>



| <span data-ttu-id="85980-125">Interfaz</span><span class="sxs-lookup"><span data-stu-id="85980-125">Interface</span></span>                                      | <span data-ttu-id="85980-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="85980-126">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="85980-127">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="85980-127">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="85980-128">Recibe mensajes de estado de los procesos que se ejecutan en un subproceso independiente.</span><span class="sxs-lookup"><span data-stu-id="85980-128">Receives status messages from processes that execute in a separate thread.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="85980-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="85980-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85980-130">**de la empresa**</span><span class="sxs-lookup"><span data-stu-id="85980-130">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="85980-131">**Trabajar con índices**</span><span class="sxs-lookup"><span data-stu-id="85980-131">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




