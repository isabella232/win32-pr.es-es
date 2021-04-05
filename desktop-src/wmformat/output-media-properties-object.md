---
title: Objeto de propiedades de medios de salida
description: Objeto de propiedades de medios de salida
ms.assetid: 96fa7c66-59a0-4eb3-ace4-a827b139f978
keywords:
- SDK de formato de Windows Media, objetos de propiedades de medios de salida
- Advanced Systems Format (ASF), objetos de propiedades de medios de salida
- ASF (formato de sistemas avanzados), objetos de propiedades de medios de salida
- objetos, propiedades de elementos multimedia de salida
- objetos de propiedades de medios de salida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61490464381a0b4e58be7994dfaeb0dfec2baa76
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104077448"
---
# <a name="output-media-properties-object"></a><span data-ttu-id="67d11-108">Objeto de propiedades de medios de salida</span><span class="sxs-lookup"><span data-stu-id="67d11-108">Output Media Properties Object</span></span>

<span data-ttu-id="67d11-109">Se usa un objeto de propiedades de medios de salida para recuperar y establecer una propiedad de salida.</span><span class="sxs-lookup"><span data-stu-id="67d11-109">An output media properties object is used to retrieve and set an output property.</span></span> <span data-ttu-id="67d11-110">Se crean objetos de las propiedades de los medios de salida para los formatos de salida compatibles de las secuencias en un archivo que se carga en un objeto de lector.</span><span class="sxs-lookup"><span data-stu-id="67d11-110">Output media properties objects are created for supported output formats of streams in a file that is loaded into a reader object.</span></span> <span data-ttu-id="67d11-111">En el caso de las secuencias comprimidas, las propiedades de salida se determinan mediante las posibles salidas del códec de descompresión.</span><span class="sxs-lookup"><span data-stu-id="67d11-111">For compressed streams, the output properties are determined by the possible outputs of the decompressing codec.</span></span>

<span data-ttu-id="67d11-112">[**IWMReader:: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) crea un objeto de las propiedades de los medios de salida. este método crea un objeto de propiedades de medios de salida que contiene las propiedades del formato de salida predeterminado.</span><span class="sxs-lookup"><span data-stu-id="67d11-112">An output media properties object is created by [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) This method creates an output media properties object that contains the properties of the default output format.</span></span> <span data-ttu-id="67d11-113">Es posible que se admitan otros formatos para una salida.</span><span class="sxs-lookup"><span data-stu-id="67d11-113">Other formats may be supported for an output.</span></span> <span data-ttu-id="67d11-114">Para obtener formatos de salida adicionales, puede llamar a [**IWMReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) para obtener el número de formatos de salida admitidos y, a continuación, recorra en bucle mediante llamadas a [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat).</span><span class="sxs-lookup"><span data-stu-id="67d11-114">To obtain additional output formats, you can call [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) to get the number of supported output formats and then loop through them using calls to [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat).</span></span> <span data-ttu-id="67d11-115">**GetOutputFormat** crea un objeto de propiedades de medios de salida rellenado con los datos para el formato de salida seleccionado.</span><span class="sxs-lookup"><span data-stu-id="67d11-115">**GetOutputFormat** creates an output media properties object populated with the data for the selected output format.</span></span>

<span data-ttu-id="67d11-116">Los objetos de las propiedades de los medios de salida también se pueden crear con el lector sincrónico.</span><span class="sxs-lookup"><span data-stu-id="67d11-116">Output media properties objects can also be created with the synchronous reader.</span></span> <span data-ttu-id="67d11-117">Todos los nombres de método son idénticos a los del lector y todos los exponen la interfaz [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) .</span><span class="sxs-lookup"><span data-stu-id="67d11-117">All of the method names are identical to those in the reader and they are all exposed by the [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) interface.</span></span>

<span data-ttu-id="67d11-118">**GetOutputProps** y **GetOutputFormat** establecen un puntero a una interfaz [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) .</span><span class="sxs-lookup"><span data-stu-id="67d11-118">**GetOutputProps** and **GetOutputFormat** both set a pointer to an [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface.</span></span> <span data-ttu-id="67d11-119">Las demás interfaces del objeto de propiedades de los medios de salida se pueden obtener llamando al método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="67d11-119">The other interfaces of the output media properties object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="67d11-120">Cada objeto de propiedades de medios de salida admite las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="67d11-120">The following interfaces are supported by every output media properties object.</span></span>



| <span data-ttu-id="67d11-121">Interfaz</span><span class="sxs-lookup"><span data-stu-id="67d11-121">Interface</span></span>                                          | <span data-ttu-id="67d11-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="67d11-122">Description</span></span>                                                                                                |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67d11-123">**IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="67d11-123">**IWMMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)             | <span data-ttu-id="67d11-124">Se usa como la interfaz base para las otras interfaces de propiedad de medios (entrada, salida y vídeo).</span><span class="sxs-lookup"><span data-stu-id="67d11-124">Used as the base interface for the other media-property interfaces (input, output, and video).</span></span>             |
| [<span data-ttu-id="67d11-125">**IWMOutputMediaProps**</span><span class="sxs-lookup"><span data-stu-id="67d11-125">**IWMOutputMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) | <span data-ttu-id="67d11-126">Recupera las propiedades de una salida.</span><span class="sxs-lookup"><span data-stu-id="67d11-126">Retrieves the properties of an output.</span></span>                                                                     |
| [<span data-ttu-id="67d11-127">**IWMVideoMediaProps**</span><span class="sxs-lookup"><span data-stu-id="67d11-127">**IWMVideoMediaProps**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops)   | <span data-ttu-id="67d11-128">Administra las propiedades de una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="67d11-128">Manages the properties of a video stream.</span></span> <span data-ttu-id="67d11-129">Se trata de una interfaz opcional, disponible solo para secuencias de vídeo.</span><span class="sxs-lookup"><span data-stu-id="67d11-129">This is an optional interface, available only for video streams.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="67d11-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="67d11-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67d11-131">**de la empresa**</span><span class="sxs-lookup"><span data-stu-id="67d11-131">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="67d11-132">**Objeto del lector**</span><span class="sxs-lookup"><span data-stu-id="67d11-132">**Reader Object**</span></span>](reader-object.md)
</dt> </dl>

 

 




