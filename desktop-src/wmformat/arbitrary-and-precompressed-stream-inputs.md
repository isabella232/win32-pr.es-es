---
title: Entradas de secuencias arbitrarias y precomprimidas
description: Entradas de secuencias arbitrarias y precomprimidas
ms.assetid: 6debbae5-0c54-48db-9ef8-f84f74e2f090
keywords:
- Advanced Systems Format (ASF), entradas de secuencias arbitrarias
- ASF (formato de sistemas avanzados), entradas de secuencias arbitrarias
- perfiles, entradas de secuencias arbitrarias
- códecs, entradas de secuencias arbitrarias
- Advanced Systems Format (ASF), entradas de secuencias precomprimidas
- ASF (formato de sistemas avanzados), entradas de secuencias precomprimidas
- perfiles, entradas de secuencias precomprimidas
- códecs, entradas de secuencias precomprimidas
- entradas de secuencias precomprimidas
- entradas de secuencias arbitrarias
- secuencias, entradas de secuencias arbitrarias
- secuencias, entradas de secuencias precomprimidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe1c95fe992c7638ac923ac07ce159fb5dc4126
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "105704913"
---
# <a name="arbitrary-and-precompressed-stream-inputs"></a><span data-ttu-id="c42f9-115">Entradas de secuencias arbitrarias y precomprimidas</span><span class="sxs-lookup"><span data-stu-id="c42f9-115">Arbitrary and Precompressed Stream Inputs</span></span>

<span data-ttu-id="c42f9-116">Solo las entradas que se van a comprimir con uno de los códecs de Windows Media tienen varias entradas posibles.</span><span class="sxs-lookup"><span data-stu-id="c42f9-116">Only inputs that are to be compressed by one of the Windows Media codecs have multiple possible inputs.</span></span> <span data-ttu-id="c42f9-117">Los otros tipos de entradas posibles son entradas arbitrarias y entradas precomprimidas.</span><span class="sxs-lookup"><span data-stu-id="c42f9-117">The other types of possible inputs are arbitrary inputs and precompressed inputs.</span></span> <span data-ttu-id="c42f9-118">En esta sección se describen los requisitos para los formatos de entrada de estos tipos.</span><span class="sxs-lookup"><span data-stu-id="c42f9-118">The requirements for input formats for these types are described in this section.</span></span>

## <a name="arbitrary-stream-inputs"></a><span data-ttu-id="c42f9-119">Entradas de secuencias arbitrarias</span><span class="sxs-lookup"><span data-stu-id="c42f9-119">Arbitrary Stream Inputs</span></span>

<span data-ttu-id="c42f9-120">Las entradas de tipos de flujo arbitrarios son las mismas que los formatos de secuencia descritos en el perfil.</span><span class="sxs-lookup"><span data-stu-id="c42f9-120">Inputs for arbitrary stream types are the same as the stream formats described in the profile.</span></span> <span data-ttu-id="c42f9-121">No debe tener que establecer formatos de entrada para estos tipos.</span><span class="sxs-lookup"><span data-stu-id="c42f9-121">You should not have to set input formats for these types.</span></span>

## <a name="precompressed-stream-inputs"></a><span data-ttu-id="c42f9-122">Entradas de secuencias precomprimidas</span><span class="sxs-lookup"><span data-stu-id="c42f9-122">Precompressed Stream Inputs</span></span>

<span data-ttu-id="c42f9-123">Cuando se copia una secuencia de un archivo a otro, se pasan ejemplos que ya están comprimidos.</span><span class="sxs-lookup"><span data-stu-id="c42f9-123">When copying a stream from one file to another, you pass samples that are already compressed.</span></span> <span data-ttu-id="c42f9-124">En este caso, debe establecer el objeto de propiedades de entrada en **null** para informar al escritor de que no necesita validar los datos que está pasando.</span><span class="sxs-lookup"><span data-stu-id="c42f9-124">In this case, you must set the input properties object to **NULL** to inform the writer that it does not need to validate the data you are passing in.</span></span> <span data-ttu-id="c42f9-125">Para establecer el formato de entrada en **null**, llame a [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) y pase **null** como segundo parámetro.</span><span class="sxs-lookup"><span data-stu-id="c42f9-125">To set the input format to **NULL**, call [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) and pass **NULL** as the second parameter.</span></span> <span data-ttu-id="c42f9-126">Al llamar a este método con un parámetro **null** , debe realizar la llamada antes de llamar a [**BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="c42f9-126">When calling this method with a **NULL** parameter, you must make the call before calling [**BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

<span data-ttu-id="c42f9-127">Al utilizar secuencias precomprimidas, debe copiar manualmente la información del códec en el encabezado del archivo antes de la escritura.</span><span class="sxs-lookup"><span data-stu-id="c42f9-127">When using precompressed streams, you must manually copy codec information to the file header before writing.</span></span> <span data-ttu-id="c42f9-128">Para obtener la información del códec, llame a [**IWMHeaderInfo2:: GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) y [**IWMHeaderInfo2:: GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) para enumerar los códecs asociados al archivo en el lector.</span><span class="sxs-lookup"><span data-stu-id="c42f9-128">To obtain the codec information, call [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) and [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) to enumerate the codecs associated with the file in the reader.</span></span> <span data-ttu-id="c42f9-129">Seleccione la información del códec que coincida con la configuración de la secuencia precomprimida.</span><span class="sxs-lookup"><span data-stu-id="c42f9-129">Select the codec information that matches the stream configuration of the precompressed stream.</span></span> <span data-ttu-id="c42f9-130">A continuación, establezca la información del códec en el escritor llamando a [**IWMHeaderInfo3:: AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), pasando la información obtenida del lector.</span><span class="sxs-lookup"><span data-stu-id="c42f9-130">Then set the codec information in the writer by calling [**IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passing the information obtained from the reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c42f9-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c42f9-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c42f9-132">**Trabajar con entradas**</span><span class="sxs-lookup"><span data-stu-id="c42f9-132">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




