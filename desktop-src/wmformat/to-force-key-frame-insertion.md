---
title: Para forzar la inserción de Key-Frame
description: Para forzar la inserción de Key-Frame
ms.assetid: 456482da-aaa2-41f8-93f7-c0fa5abe7dd2
keywords:
- Advanced Systems Format (ASF), forzar inserciones de fotogramas clave
- ASF (formato de sistemas avanzados), forzar inserciones de fotogramas clave
- Advanced Systems Format (ASF), inserciones de fotogramas clave
- ASF (formato de sistemas avanzados), inserciones de fotogramas clave
- fotogramas clave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23006eef1e51d8bc63f2d55cac22e09a2052d83e
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104487358"
---
# <a name="to-force-key-frame-insertion"></a><span data-ttu-id="6b5ae-108">Para forzar la inserción de Key-Frame</span><span class="sxs-lookup"><span data-stu-id="6b5ae-108">To Force Key-Frame Insertion</span></span>

<span data-ttu-id="6b5ae-109">El códec Windows Media Video 9 admite la inserción de fotogramas clave forzada.</span><span class="sxs-lookup"><span data-stu-id="6b5ae-109">The Windows Media Video 9 codec supports forced key-frame insertion.</span></span> <span data-ttu-id="6b5ae-110">Al pasar un ejemplo al escritor, puede especificar que se debe codificar como un [*fotograma clave*](wmformat-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="6b5ae-110">When you pass a sample to the writer, you can specify that it must be encoded as a [*key frame*](wmformat-glossary.md).</span></span>

<span data-ttu-id="6b5ae-111">Para forzar la inserción de fotogramas clave para un ejemplo, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="6b5ae-111">To force key-frame insertion for a sample, perform the following steps.</span></span>

1.  <span data-ttu-id="6b5ae-112">Asigne un búfer para contener el ejemplo y recupere un puntero a la interfaz [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) que contiene el búfer mediante una llamada a [**IWMWriter:: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).</span><span class="sxs-lookup"><span data-stu-id="6b5ae-112">Allocate a buffer to hold the sample, and retrieve a pointer to the [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) interface containing the buffer by calling [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).</span></span>
2.  <span data-ttu-id="6b5ae-113">Recupere la ubicación y el tamaño del búfer creado en el paso 1 mediante una llamada a [**INSSBuffer:: GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength).</span><span class="sxs-lookup"><span data-stu-id="6b5ae-113">Retrieve the location and size of the buffer created in step 1 by calling [**INSSBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength).</span></span>
3.  <span data-ttu-id="6b5ae-114">Copie los datos de ejemplo en la ubicación del búfer, asegurándose de que el ejemplo que se ha pasado quepa en el búfer asignado.</span><span class="sxs-lookup"><span data-stu-id="6b5ae-114">Copy your sample data to the buffer location, making sure that the sample passed will fit in the allocated buffer.</span></span> <span data-ttu-id="6b5ae-115">Dependiendo del origen de los ejemplos, puede usar diversas funciones para copiar los datos.</span><span class="sxs-lookup"><span data-stu-id="6b5ae-115">Depending upon the source of your samples, you can use a variety of functions to copy the data.</span></span> <span data-ttu-id="6b5ae-116">Por ejemplo, si va a copiar una secuencia desde un archivo AVI, puede usar la función AVI, **AVIStreamRead**.</span><span class="sxs-lookup"><span data-stu-id="6b5ae-116">For example, if you are copying a stream from an AVI file, you can use the AVI function, **AVIStreamRead**.</span></span>
4.  <span data-ttu-id="6b5ae-117">Actualice la cantidad de datos que se usan en el búfer para reflejar el tamaño real del ejemplo llamando a [**INSSBuffer:: SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).</span><span class="sxs-lookup"><span data-stu-id="6b5ae-117">Update the amount of data used in the buffer to reflect the actual size of the sample by calling [**INSSBuffer::SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).</span></span>
5.  <span data-ttu-id="6b5ae-118">Obtenga un puntero a la interfaz [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) llamando a **INSSBuffer:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="6b5ae-118">Obtain a pointer to the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface by calling **INSSBuffer::QueryInterface**.</span></span>
6.  <span data-ttu-id="6b5ae-119">Establezca el ejemplo como un fotograma clave forzado llamando al método [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) para establecer la \_ propiedad WM SampleExtensionGUID \_ OutputCleanPoint.</span><span class="sxs-lookup"><span data-stu-id="6b5ae-119">Set the sample as a forced key frame by calling the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method to set the WM\_SampleExtensionGUID\_OutputCleanPoint property.</span></span> <span data-ttu-id="6b5ae-120">Esta propiedad es un valor booleano; establézcalo en **true**.</span><span class="sxs-lookup"><span data-stu-id="6b5ae-120">This property is a Boolean value; set it to **TRUE**.</span></span>
7.  <span data-ttu-id="6b5ae-121">Pase la interfaz de búfer al escritor junto con el número de entrada y el tiempo de muestra mediante el método [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) .</span><span class="sxs-lookup"><span data-stu-id="6b5ae-121">Pass the buffer interface to the writer along with the input number and sample time by using the [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b5ae-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6b5ae-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b5ae-123">**IWMWriter::WriteSample**</span><span class="sxs-lookup"><span data-stu-id="6b5ae-123">**IWMWriter::WriteSample**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)
</dt> <dt>

[<span data-ttu-id="6b5ae-124">**Para escribir ejemplos**</span><span class="sxs-lookup"><span data-stu-id="6b5ae-124">**To Write Samples**</span></span>](to-write-samples.md)
</dt> <dt>

[<span data-ttu-id="6b5ae-125">**Codificación de velocidad de bits variable (VBR)**</span><span class="sxs-lookup"><span data-stu-id="6b5ae-125">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="6b5ae-126">**Escribir archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="6b5ae-126">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




