---
title: Almacenamiento de contenido
description: Almacenamiento de contenido
ms.assetid: 22f4e580-43a4-48b5-8eb3-90e1346a1093
keywords:
- Windows Media Format SDK, guardar contenido
- SDK de Windows Media Format, streaming de caché rápido
- Advanced Systems Format (ASF), guardar contenido
- ASF (formato de sistemas avanzados), guardar contenido
- Advanced Systems Format (ASF), streaming de caché rápido
- ASF (formato de sistemas avanzados), streaming de caché rápido
- flujos, guardar contenido
- Streaming de caché rápido, guardar contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6c215a81accef29f8943ed52ca24264f785d94
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789208"
---
# <a name="saving-content"></a><span data-ttu-id="18161-111">Almacenamiento de contenido</span><span class="sxs-lookup"><span data-stu-id="18161-111">Saving Content</span></span>

<span data-ttu-id="18161-112">Mediante este SDK, una aplicación puede guardar el contenido descargado o transmitido en el equipo local del usuario, llamando al método [**IWMReaderAdvanced2:: saveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) en el objeto del lector.</span><span class="sxs-lookup"><span data-stu-id="18161-112">By using this SDK, an application can save downloaded or streamed content to the user's local computer, by calling the [**IWMReaderAdvanced2::SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) method on the reader object.</span></span> <span data-ttu-id="18161-113">En el caso del contenido transmitido por secuencias, el servidor debe usar el streaming de caché rápido, que se describe en la sección [habilitación del streaming de caché rápido desde el cliente](enabling-fast-cache-streaming-from-the-client.md).</span><span class="sxs-lookup"><span data-stu-id="18161-113">For streamed content, the server must be using Fast Cache streaming, which is described in the section [Enabling Fast Cache Streaming from the Client](enabling-fast-cache-streaming-from-the-client.md).</span></span> <span data-ttu-id="18161-114">En el caso del contenido transmitido por secuencias, el método **saveFileAs** crea un archivo ASX que señala a un archivo ASF que contiene el contenido guardado.</span><span class="sxs-lookup"><span data-stu-id="18161-114">For streamed content, the **SaveFileAs** method creates an ASX file that points to an ASF file containing the saved content.</span></span> <span data-ttu-id="18161-115">Si el objeto lector está transmitiendo una lista de reproducción del servidor, cada entrada se guarda como un archivo ASF independiente y el archivo ASX apunta a cada uno de los archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="18161-115">If the reader object is streaming a server-side playlist, each entry is saved as a separate ASF file, and the ASX file points to each of the ASF files.</span></span> <span data-ttu-id="18161-116">En el caso del contenido descargado, el método **saveFileAs** simplemente crea un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="18161-116">For downloaded content, the **SaveFileAs** method simply creates an ASF file.</span></span>

<span data-ttu-id="18161-117">Para guardar el contenido en un archivo local, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="18161-117">To save content to a local file, do the following:</span></span>

1.  <span data-ttu-id="18161-118">Llame a [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) con la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="18161-118">Call [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) with the URL.</span></span> <span data-ttu-id="18161-119">**Open** es una llamada asincrónica y se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="18161-119">**Open** is an asynchronous call, and returns immediately.</span></span> <span data-ttu-id="18161-120">Espere a que se complete la operación, como se describe en [para crear un lector y abrir un archivo](to-create-a-reader-and-open-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="18161-120">Wait for the operation to complete, as described in [To Create a Reader and Open a File](to-create-a-reader-and-open-a-file.md).</span></span>
2.  <span data-ttu-id="18161-121">Consulte el objeto de lector para la interfaz [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) .</span><span class="sxs-lookup"><span data-stu-id="18161-121">Query the reader object for the [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) interface.</span></span>
3.  <span data-ttu-id="18161-122">Compruebe si el contenido se puede guardar llamando al método [**IWMReaderAdvanced4:: CanSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cansavefileas) .</span><span class="sxs-lookup"><span data-stu-id="18161-122">Check whether the content can be saved by calling the [**IWMReaderAdvanced4::CanSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cansavefileas) method.</span></span> <span data-ttu-id="18161-123">Si el método devuelve false, el contenido no se puede guardar localmente.</span><span class="sxs-lookup"><span data-stu-id="18161-123">If the method returns False, the content cannot be saved locally.</span></span> <span data-ttu-id="18161-124">En caso contrario, continúe en el paso 4.</span><span class="sxs-lookup"><span data-stu-id="18161-124">Otherwise, proceed to step 4.</span></span>
4.  <span data-ttu-id="18161-125">Llame al método [**IWMReaderAdvanced4:: IsUsingFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-isusingfastcache) para determinar si el servidor usa el streaming de caché rápido.</span><span class="sxs-lookup"><span data-stu-id="18161-125">Call the [**IWMReaderAdvanced4::IsUsingFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-isusingfastcache) method to determine whether the server is using Fast Cache streaming.</span></span>
5.  <span data-ttu-id="18161-126">Llame a [**IWMReaderAdvanced2:: saveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) con un nombre de archivo para el archivo local.</span><span class="sxs-lookup"><span data-stu-id="18161-126">Call the [**IWMReaderAdvanced2::SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) with a file name for the local file.</span></span> <span data-ttu-id="18161-127">Si el método **IsUsingFastCache** devuelve true, asigne a la extensión. ASX el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="18161-127">If the **IsUsingFastCache** method returned True, give the file name an .asx extension.</span></span> <span data-ttu-id="18161-128">De lo contrario, asigne al nombre de archivo una extensión. ASF,. WMA o. wmv.</span><span class="sxs-lookup"><span data-stu-id="18161-128">Otherwise, give the file name an .asf, .wma, or .wmv extension.</span></span>

<span data-ttu-id="18161-129">La aplicación puede cancelar la operación de guardar mientras está en curso, llamando al método [**IWMReaderAdvanced4:: CancelSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cancelsavefileas) .</span><span class="sxs-lookup"><span data-stu-id="18161-129">The application can cancel the save operation while it is in progress, by calling the [**IWMReaderAdvanced4::CancelSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cancelsavefileas) method.</span></span>

<span data-ttu-id="18161-130">El contenido guardado podría estar protegido con DRM, por lo que es posible que no sea posible reproducir el archivo en otro equipo.</span><span class="sxs-lookup"><span data-stu-id="18161-130">The saved content might be protected with DRM, so it may not be possible to play the file on another computer.</span></span> <span data-ttu-id="18161-131">Para obtener más información sobre la protección de contenido, vea [características de Rights Management digital](digital-rights-management-features.md).</span><span class="sxs-lookup"><span data-stu-id="18161-131">For more information on content protection, see [Digital Rights Management Features](digital-rights-management-features.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="18161-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="18161-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18161-133">**Interfaz IWMReader**</span><span class="sxs-lookup"><span data-stu-id="18161-133">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="18161-134">**Interfaz IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="18161-134">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




