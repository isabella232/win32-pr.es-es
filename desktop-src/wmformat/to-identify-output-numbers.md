---
title: Para identificar los números de salida
description: Para identificar los números de salida
ms.assetid: a2135a71-52e6-4f62-8be8-b9886be9b37c
keywords:
- SDK de Windows Media Format, identificar números de salida
- Advanced Systems Format (ASF), identificar números de salida
- ASF (formato de sistemas avanzados), identificar números de salida
- Formato de sistemas avanzados (ASF), números y formatos de salida
- ASF (formato de sistemas avanzados), números y formatos de salida
- números y formatos de salida, identificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c08f8e9a49d672efe7c04ecdde11ca4ef297d552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105714327"
---
# <a name="to-identify-output-numbers"></a><span data-ttu-id="4d3a5-109">Para identificar los números de salida</span><span class="sxs-lookup"><span data-stu-id="4d3a5-109">To Identify Output Numbers</span></span>

<span data-ttu-id="4d3a5-110">Para identificar los números de salida de un archivo cargado, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="4d3a5-110">To identify the output numbers for a loaded file, perform the following steps.</span></span> <span data-ttu-id="4d3a5-111">Estos procedimientos son idénticos para el lector asincrónico y el lector sincrónico.</span><span class="sxs-lookup"><span data-stu-id="4d3a5-111">These procedures are identical for both the asynchronous reader and the synchronous reader.</span></span> <span data-ttu-id="4d3a5-112">Si los nombres de interfaz varían, los métodos de lectura sincrónicos se enumeran entre paréntesis después de los métodos del lector asincrónico.</span><span class="sxs-lookup"><span data-stu-id="4d3a5-112">Where interface names vary, the synchronous reader methods are listed in parentheses after the methods of the asynchronous reader.</span></span>

1.  <span data-ttu-id="4d3a5-113">Cree un objeto lector y cargue un archivo para leerlo.</span><span class="sxs-lookup"><span data-stu-id="4d3a5-113">Create a reader object and load a file for reading.</span></span> <span data-ttu-id="4d3a5-114">Para obtener más información, vea [para crear un lector y abrir un archivo](to-create-a-reader-and-open-a-file.md) (o [para crear un lector sincrónico y abrir un archivo](to-create-a-synchronous-reader-and-open-a-file.md)).</span><span class="sxs-lookup"><span data-stu-id="4d3a5-114">For more information, see [To Create a Reader and Open a File](to-create-a-reader-and-open-a-file.md) (or [To Create a Synchronous Reader and Open a File](to-create-a-synchronous-reader-and-open-a-file.md)).</span></span>
2.  <span data-ttu-id="4d3a5-115">Recupere el número total de salidas del archivo mediante una llamada a [**IWMReader:: GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (o [**IWMSyncReader:: GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)).</span><span class="sxs-lookup"><span data-stu-id="4d3a5-115">Retrieve the total number of outputs for the file by calling [**IWMReader::GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (or [**IWMSyncReader::GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)).</span></span>
3.  <span data-ttu-id="4d3a5-116">Recorra las salidas de una en una, siguiendo estos pasos para cada una de ellas:</span><span class="sxs-lookup"><span data-stu-id="4d3a5-116">Loop through the outputs one at a time, performing the following steps for each:</span></span>
    -   <span data-ttu-id="4d3a5-117">Recupere la interfaz [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) para la salida actual con una llamada a [**IWMReader:: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) (o [**IWMSyncReader:: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)).</span><span class="sxs-lookup"><span data-stu-id="4d3a5-117">Retrieve the [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface for the current output with a call to [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) (or [**IWMSyncReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)).</span></span>
    -   <span data-ttu-id="4d3a5-118">Recupere la estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para la salida realizando dos llamadas a [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="4d3a5-118">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the output by making two calls to [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span></span> <span data-ttu-id="4d3a5-119">Realice la primera llamada para obtener el tamaño de la estructura, después asigne memoria para ella y pase un puntero a la memoria asignada en la segunda llamada.</span><span class="sxs-lookup"><span data-stu-id="4d3a5-119">Make the first call to get the size of the structure, then allocate memory for it and pass a pointer to the allocated memory on the second call.</span></span> <span data-ttu-id="4d3a5-120">Como alternativa, puede llamar a [**IWMMediaProps:: GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype), que ofrece el tipo principal sin necesidad de asignar memoria para la estructura de **\_ \_ tipo de medio de WM** .</span><span class="sxs-lookup"><span data-stu-id="4d3a5-120">Alternatively, you can call [**IWMMediaProps::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype), which delivers the major type without requiring you to allocate memory for the **WM\_MEDIA\_TYPE** structure.</span></span> <span data-ttu-id="4d3a5-121">Puede omitir las salidas del tipo principal incorrecto.</span><span class="sxs-lookup"><span data-stu-id="4d3a5-121">You can skip outputs of the wrong major type.</span></span>
    -   <span data-ttu-id="4d3a5-122">Recupere el tipo de medio principal y el subtipo de medio de la estructura de **\_ \_ tipo de medio de WM** .</span><span class="sxs-lookup"><span data-stu-id="4d3a5-122">Retrieve the major media type and media subtype from the **WM\_MEDIA\_TYPE** structure.</span></span> <span data-ttu-id="4d3a5-123">Estos valores se almacenan en miembros de datos **majortype** y **SubType** respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4d3a5-123">These values are stored in data members **majortype** and **subtype** respectively.</span></span>
    -   <span data-ttu-id="4d3a5-124">Compruebe el valor de **tipo de medio de WM \_ \_ . FormatType**.</span><span class="sxs-lookup"><span data-stu-id="4d3a5-124">Check the value of **WM\_MEDIA\_TYPE.formattype**.</span></span> <span data-ttu-id="4d3a5-125">Especifica el tipo de estructura que contiene el búfer en el **tipo de medio de WM \_ \_ . pbFormat**.</span><span class="sxs-lookup"><span data-stu-id="4d3a5-125">This specifies the type of structure contained in the buffer at **WM\_MEDIA\_TYPE.pbFormat**.</span></span> <span data-ttu-id="4d3a5-126">Para obtener más información sobre los tipos de formato, consulte [tipos de medios](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="4d3a5-126">For more information about format types, see [Media Types](media-types.md).</span></span>
    -   <span data-ttu-id="4d3a5-127">Asigne memoria para que contenga la estructura del tipo identificado en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="4d3a5-127">Allocate memory to hold the structure of the type identified in the previous step.</span></span> <span data-ttu-id="4d3a5-128">Copie la estructura en la memoria asignada.</span><span class="sxs-lookup"><span data-stu-id="4d3a5-128">Copy the structure to your allocated memory.</span></span> <span data-ttu-id="4d3a5-129">En audio y vídeo, esta estructura proporciona información esencial sobre cómo se deben representar los datos.</span><span class="sxs-lookup"><span data-stu-id="4d3a5-129">For audio and video, this structure gives you essential information about how the data should be rendered.</span></span>

<span data-ttu-id="4d3a5-130">El lector sincrónico también proporciona métodos para recuperar las asociaciones entre los números de salida y los números de flujo.</span><span class="sxs-lookup"><span data-stu-id="4d3a5-130">The synchronous reader also provides methods to retrieve associations between output numbers and stream numbers.</span></span> <span data-ttu-id="4d3a5-131">Para obtener más información, vea [para buscar números de secuencia y números de salida](to-find-stream-numbers-and-output-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="4d3a5-131">For more information, see [To Find Stream Numbers and Output Numbers](to-find-stream-numbers-and-output-numbers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d3a5-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4d3a5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d3a5-133">**Entradas, secuencias y salidas**</span><span class="sxs-lookup"><span data-stu-id="4d3a5-133">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="4d3a5-134">**Interfaz IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="4d3a5-134">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="4d3a5-135">**Interfaz IWMOutputMediaProps**</span><span class="sxs-lookup"><span data-stu-id="4d3a5-135">**IWMOutputMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[<span data-ttu-id="4d3a5-136">**Interfaz IWMReader**</span><span class="sxs-lookup"><span data-stu-id="4d3a5-136">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="4d3a5-137">**Interfaz IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="4d3a5-137">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="4d3a5-138">**Trabajar con salidas**</span><span class="sxs-lookup"><span data-stu-id="4d3a5-138">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




