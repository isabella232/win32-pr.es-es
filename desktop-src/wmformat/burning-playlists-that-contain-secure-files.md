---
title: Grabación de listas de reproducción que contienen archivos seguros
description: Grabación de listas de reproducción que contienen archivos seguros
ms.assetid: 0d9415a1-a154-4fe4-af4c-cce4cb05ade5
keywords:
- SDK de Windows Media Format, grabar listas de reproducción con archivos seguros
- SDK de Windows Media Format, listas de reproducción con archivos seguros
- Advanced Systems Format (ASF), grabar listas de reproducción con archivos seguros
- ASF (formato de sistemas avanzados), grabación de listas de reproducción con archivos seguros
- Advanced Systems Format (ASF), listas de reproducción con archivos seguros
- ASF (formato de sistemas avanzados), listas de reproducción con archivos seguros
- Administración de derechos digitales (DRM), grabar listas de reproducción con archivos seguros
- DRM (administración de derechos digitales), grabar listas de reproducción con archivos seguros
- Administración de derechos digitales (DRM), listas de reproducción con archivos seguros
- DRM (administración de derechos digitales), listas de reproducción con archivos seguros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214c1dbd4ee08f90b3e5e8aa6186508af5044f29
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "105714345"
---
# <a name="burning-playlists-that-contain-secure-files"></a><span data-ttu-id="61ee5-113">Grabación de listas de reproducción que contienen archivos seguros</span><span class="sxs-lookup"><span data-stu-id="61ee5-113">Burning Playlists That Contain Secure Files</span></span>

<span data-ttu-id="61ee5-114">Las licencias creadas con los objetos del SDK de Windows Media Rights Manager 10 pueden especificar el derecho para copiar un archivo en un disco compacto como parte de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="61ee5-114">Licenses created by using the objects of the Windows Media Rights Manager 10 SDK can specify the right to copy a file to compact disc as part of a playlist.</span></span> <span data-ttu-id="61ee5-115">Esta característica, denominada grabación de listas de reproducción, requiere que compruebe las licencias de todos los archivos de la lista de reproducción antes de empezar a copiar los datos.</span><span class="sxs-lookup"><span data-stu-id="61ee5-115">This feature, called playlist burning, requires that you verify the licenses of all of the files in the playlist before starting to copy data.</span></span> <span data-ttu-id="61ee5-116">El SDK de Windows Media Format proporciona la interfaz [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) para realizar la comprobación de archivos.</span><span class="sxs-lookup"><span data-stu-id="61ee5-116">The Windows Media Format SDK provides the [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) interface to perform file verification for you.</span></span>

<span data-ttu-id="61ee5-117">Para implementar la grabación de listas de reproducción, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="61ee5-117">To implement playlist burning, perform the following steps:</span></span>

1.  <span data-ttu-id="61ee5-118">Cree una instancia del objeto lector o el objeto lector sincrónico.</span><span class="sxs-lookup"><span data-stu-id="61ee5-118">Create an instance of the reader object, or the synchronous reader object.</span></span> <span data-ttu-id="61ee5-119">Para obtener más información, consulte [leer archivos ASF](reading-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="61ee5-119">For more information, see [Reading ASF Files](reading-asf-files.md).</span></span>
2.  <span data-ttu-id="61ee5-120">Llame al método **QueryInterface** de la interfaz del lector ([**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) o [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)) para obtener un puntero a la interfaz [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) .</span><span class="sxs-lookup"><span data-stu-id="61ee5-120">Call the **QueryInterface** method of the reader interface ([**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) or [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)) to obtain a pointer to the [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) interface.</span></span>
3.  <span data-ttu-id="61ee5-121">Copie los nombres de archivo de la lista de reproducción en una matriz de cadenas de caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="61ee5-121">Copy the file names from the playlist into an array of wide-character strings.</span></span> <span data-ttu-id="61ee5-122">Los nombres de archivo de la matriz deben estar en el mismo orden en que aparecen en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="61ee5-122">The file names in the array must be in the same order as they appear in the playlist.</span></span>
4.  <span data-ttu-id="61ee5-123">Llame al método [**IWMReaderPlaylistBurn:: InitPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) , pasando un puntero a la matriz creada en el paso 3, para inicializar la comprobación de la licencia para los archivos.</span><span class="sxs-lookup"><span data-stu-id="61ee5-123">Call the [**IWMReaderPlaylistBurn::InitPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) method, passing in a pointer to the array created in step 3, to initialize the license verification for the files.</span></span>
5.  <span data-ttu-id="61ee5-124">Cuando se completa la comprobación de la licencia, el objeto de lector envía un \_ \_ \_ mensaje de grabación de la lista de reproducción WMT init a la implementación del método de devolución de llamada [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) .</span><span class="sxs-lookup"><span data-stu-id="61ee5-124">When the license verification is completed, the reader object sends a WMT\_INIT\_PLAYLIST\_BURN message to your implementation of the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method.</span></span> <span data-ttu-id="61ee5-125">Cuando la devolución de llamada reciba este mensaje, llame al método [**IWMReaderPlaylistBurn:: GetInitResults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) para obtener los resultados de la comprobación de licencia.</span><span class="sxs-lookup"><span data-stu-id="61ee5-125">When your callback receives this message, call the [**IWMReaderPlaylistBurn::GetInitResults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) method to get the results of the license check.</span></span> <span data-ttu-id="61ee5-126">Este método toma una matriz de variables **HRESULT** que corresponden a los nombres de archivo de la matriz que se pasa a **InitPlaylistBurn**.</span><span class="sxs-lookup"><span data-stu-id="61ee5-126">This method takes an array of **HRESULT** variables that correspond to the file names in the array passed to **InitPlaylistBurn**.</span></span> <span data-ttu-id="61ee5-127">Si todos los valores de la matriz de resultados son iguales a S \_ correcto, puede continuar.</span><span class="sxs-lookup"><span data-stu-id="61ee5-127">If all of the values in the result array are equal to S\_OK, you can continue.</span></span> <span data-ttu-id="61ee5-128">Si algún resultado es un código de error, no se debe copiar la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="61ee5-128">If any result is an error code, the playlist must not be copied.</span></span>
6.  <span data-ttu-id="61ee5-129">Con la misma instancia del lector, abra y Lea cada archivo.</span><span class="sxs-lookup"><span data-stu-id="61ee5-129">Using the same instance of the reader, open and read each file.</span></span> <span data-ttu-id="61ee5-130">Debe abrir los archivos en el orden en que aparecen los nombres de archivo en la matriz de nombres de archivo que se pasó a **InitPlaylistBurn**.</span><span class="sxs-lookup"><span data-stu-id="61ee5-130">You must open the files in the order in which the file names appeared in the file name array passed to **InitPlaylistBurn**.</span></span>
7.  <span data-ttu-id="61ee5-131">Una vez copiados todos los archivos de la lista de reproducción, llame a [**IWMReaderPlaylistBurn:: EndPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) para completar el proceso de grabación de la lista de reproducción y liberar los recursos utilizados por el lector.</span><span class="sxs-lookup"><span data-stu-id="61ee5-131">When you have copied all of the files in the playlist, call the [**IWMReaderPlaylistBurn::EndPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) to complete the playlist burn process and free the resources used by the reader.</span></span>

> [!Note]  
> <span data-ttu-id="61ee5-132">DRM no es compatible con la versión basada en x64 de este SDK.</span><span class="sxs-lookup"><span data-stu-id="61ee5-132">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="61ee5-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="61ee5-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61ee5-134">**Habilitar la compatibilidad con DRM**</span><span class="sxs-lookup"><span data-stu-id="61ee5-134">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




