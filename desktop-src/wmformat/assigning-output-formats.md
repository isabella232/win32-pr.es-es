---
title: Asignar formatos de salida
description: Asignar formatos de salida
ms.assetid: 47697ffb-51cb-44cd-a0b0-7d85625a38f9
keywords:
- SDK de Windows Media Format, asignar formatos de salida
- Advanced Systems Format (ASF), asignar formatos de salida
- ASF (formato de sistemas avanzados), asignar formatos de salida
- Formato de sistemas avanzados (ASF), números y formatos de salida
- ASF (formato de sistemas avanzados), números y formatos de salida
- números y formatos de salida, asignar
- códecs, números de salida y formatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633673053a2b34a2f7aed5ed3f6ae66457a7ee13
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "105656315"
---
# <a name="assigning-output-formats"></a><span data-ttu-id="aad08-110">Asignar formatos de salida</span><span class="sxs-lookup"><span data-stu-id="aad08-110">Assigning Output Formats</span></span>

<span data-ttu-id="aad08-111">Algunos códecs pueden descomprimir los datos multimedia digitales en varios formatos sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="aad08-111">Some codecs can decompress digital media data into several uncompressed formats.</span></span> <span data-ttu-id="aad08-112">Puede buscar todos los formatos admitidos para una salida específica mediante el lector asincrónico o el lector sincrónico.</span><span class="sxs-lookup"><span data-stu-id="aad08-112">You can find all of the supported formats for a specific output using either the asynchronous reader or the synchronous reader.</span></span>

<span data-ttu-id="aad08-113">Para examinar todos los formatos disponibles para una salida, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="aad08-113">To examine all of the available formats for an output, perform the following steps.</span></span> <span data-ttu-id="aad08-114">Estos procedimientos son idénticos para el lector asincrónico y el lector sincrónico.</span><span class="sxs-lookup"><span data-stu-id="aad08-114">These procedures are identical for both the asynchronous reader and the synchronous reader.</span></span> <span data-ttu-id="aad08-115">Si los nombres de interfaz varían, los métodos de lectura sincrónicos se enumeran entre paréntesis después de los métodos del lector asincrónico.</span><span class="sxs-lookup"><span data-stu-id="aad08-115">Where interface names vary, the synchronous reader methods are listed in parentheses after the methods of the asynchronous reader.</span></span>

1.  <span data-ttu-id="aad08-116">Cree un objeto lector y cargue un archivo para leerlo.</span><span class="sxs-lookup"><span data-stu-id="aad08-116">Create a reader object and load a file for reading.</span></span> <span data-ttu-id="aad08-117">Para obtener más información, vea [para crear un lector y abrir un archivo](to-create-a-reader-and-open-a-file.md) (o [para crear un lector sincrónico y abrir un archivo](to-create-a-synchronous-reader-and-open-a-file.md)).</span><span class="sxs-lookup"><span data-stu-id="aad08-117">For more information, see [To Create a Reader and Open a File](to-create-a-reader-and-open-a-file.md) (or [To Create a Synchronous Reader and Open a File](to-create-a-synchronous-reader-and-open-a-file.md)).</span></span>
2.  <span data-ttu-id="aad08-118">Determine la salida para la que desea buscar los formatos disponibles.</span><span class="sxs-lookup"><span data-stu-id="aad08-118">Determine the output for which you want to find the available formats.</span></span> <span data-ttu-id="aad08-119">Si aún no sabe qué salida desea usar, puede identificar las salidas en el archivo mediante los procedimientos de [para identificar los números de salida](to-identify-output-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="aad08-119">If you don't already know which output you want to use, you can identify the outputs in the file using the procedures in [To Identify Output Numbers](to-identify-output-numbers.md).</span></span>
3.  <span data-ttu-id="aad08-120">Recupere el número total de formatos disponibles para la salida deseada llamando a [**IWMReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (o [**IWMSyncReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)).</span><span class="sxs-lookup"><span data-stu-id="aad08-120">Retrieve the total number of available formats for the desired output by calling [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (or [**IWMSyncReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)).</span></span>
4.  <span data-ttu-id="aad08-121">Recorra los formatos disponibles de uno en uno, realizando los pasos siguientes para cada uno:</span><span class="sxs-lookup"><span data-stu-id="aad08-121">Loop through the available formats one at a time, performing the following steps for each:</span></span>
    -   <span data-ttu-id="aad08-122">Recupere la interfaz [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) para el formato de salida actual llamando a [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (o [**IWMSyncReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)).</span><span class="sxs-lookup"><span data-stu-id="aad08-122">Retrieve the [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface for the current output format by calling [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (or [**IWMSyncReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)).</span></span>
    -   <span data-ttu-id="aad08-123">Recupere la estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para el formato de salida realizando dos llamadas a [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="aad08-123">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the output format by making two calls to [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span></span> <span data-ttu-id="aad08-124">Realice la primera llamada para obtener el tamaño de la estructura, después asigne memoria para ella y pase un puntero a la memoria asignada en la segunda llamada.</span><span class="sxs-lookup"><span data-stu-id="aad08-124">Make the first call to get the size of the structure, then allocate memory for it and pass a pointer to the allocated memory on the second call.</span></span>
    -   <span data-ttu-id="aad08-125">Busque el subtipo de medio del formato de salida en **tipo de medio de WM \_ \_ . subtipo**.</span><span class="sxs-lookup"><span data-stu-id="aad08-125">Find the media subtype of the output format in **WM\_MEDIA\_TYPE.subtype**.</span></span>
    -   <span data-ttu-id="aad08-126">En el caso de vídeo, si el subtipo actual es el formato que desea usar para la salida, salga del bucle.</span><span class="sxs-lookup"><span data-stu-id="aad08-126">For video, if the current subtype is the format you want to use for output, break out of the loop.</span></span> <span data-ttu-id="aad08-127">De lo contrario, vaya a la siguiente iteración.</span><span class="sxs-lookup"><span data-stu-id="aad08-127">Otherwise go to the next iteration.</span></span>

        <span data-ttu-id="aad08-128">En el caso de audio, debe comprobar los valores de la estructura **WAVEFORMATEX** en función de sus requisitos.</span><span class="sxs-lookup"><span data-stu-id="aad08-128">For audio, you must check the values in the **WAVEFORMATEX** structure against your requirements.</span></span> <span data-ttu-id="aad08-129">**WM \_ MEDIA \_ Type. pbFormat** apunta a la estructura **WAVEFORMATEX** para las salidas de audio.</span><span class="sxs-lookup"><span data-stu-id="aad08-129">**WM\_MEDIA\_TYPE.pbFormat** points to the **WAVEFORMATEX** structure for audio outputs.</span></span>

5.  <span data-ttu-id="aad08-130">Cuando haya encontrado el resultado deseado, establézcalo para usarlo con el lector mediante una llamada a [**IWMReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (o [**IWMSyncReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)).</span><span class="sxs-lookup"><span data-stu-id="aad08-130">When you have found the output desired, set it for use with the reader by calling [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (or [**IWMSyncReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)).</span></span> <span data-ttu-id="aad08-131">Debe pasar un puntero a la interfaz **IWMOutputMediaProps** obtenida en el primer paso del bucle.</span><span class="sxs-lookup"><span data-stu-id="aad08-131">You must pass a pointer to the **IWMOutputMediaProps** interface obtained in the first step of the loop.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aad08-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aad08-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aad08-133">**Interfaz IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="aad08-133">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="aad08-134">**Interfaz IWMOutputMediaProps**</span><span class="sxs-lookup"><span data-stu-id="aad08-134">**IWMOutputMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[<span data-ttu-id="aad08-135">**Interfaz IWMReader**</span><span class="sxs-lookup"><span data-stu-id="aad08-135">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="aad08-136">**Interfaz IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="aad08-136">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="aad08-137">**Trabajar con salidas**</span><span class="sxs-lookup"><span data-stu-id="aad08-137">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




