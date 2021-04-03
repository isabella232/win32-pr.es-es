---
description: Trabajar con búferes multimedia
ms.assetid: c7e079e0-99f3-4bff-9163-1c5a022c14ae
title: Trabajar con búferes multimedia (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db63843ded32be6b1baa9c62e21a33f6563a43d5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914162"
---
# <a name="working-with-media-buffers-microsoft-media-foundation"></a><span data-ttu-id="77b24-103">Trabajar con búferes multimedia (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="77b24-103">Working with Media Buffers (Microsoft Media Foundation)</span></span>

<span data-ttu-id="77b24-104">En este tema se describe cómo utilizar la interfaz [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) para tener acceso a los datos de un búfer multimedia.</span><span class="sxs-lookup"><span data-stu-id="77b24-104">This topic describes how to use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface to access the data in a media buffer.</span></span> <span data-ttu-id="77b24-105">Todos los búferes multimedia exponen **IMFMediaBuffer**, que está diseñado para cualquier tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="77b24-105">All media buffers expose **IMFMediaBuffer**, which is designed for any type of data.</span></span> <span data-ttu-id="77b24-106">Los fotogramas de vídeo sin comprimir son un caso especial, que se describe en el tema [búferes de vídeo sin comprimir](uncompressed-video-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="77b24-106">Uncompressed video frames are a special case, described in the topic [Uncompressed Video Buffers](uncompressed-video-buffers.md).</span></span>

## <a name="buffer-size"></a><span data-ttu-id="77b24-107">Tamaño del búfer</span><span class="sxs-lookup"><span data-stu-id="77b24-107">Buffer Size</span></span>

<span data-ttu-id="77b24-108">Un búfer multimedia tiene dos tamaños asociados:</span><span class="sxs-lookup"><span data-stu-id="77b24-108">A media buffer has two sizes associated with it:</span></span>

-   <span data-ttu-id="77b24-109">La *longitud máxima* es el tamaño físico de la memoria asignada para el búfer.</span><span class="sxs-lookup"><span data-stu-id="77b24-109">The *maximum length* is the physical size of the memory that is allocated for the buffer.</span></span> <span data-ttu-id="77b24-110">Este valor se establece cuando se crea el búfer y no cambia durante la vigencia del búfer.</span><span class="sxs-lookup"><span data-stu-id="77b24-110">This value is set when the buffer is created and does not change during the lifetime of the buffer.</span></span> <span data-ttu-id="77b24-111">La longitud máxima indica la cantidad de datos que se pueden almacenar en el búfer.</span><span class="sxs-lookup"><span data-stu-id="77b24-111">The maximum length indicates how much data can be stored in the buffer.</span></span> <span data-ttu-id="77b24-112">Para encontrar el tamaño máximo, llame a [**IMFMediaBuffer:: GetMaxLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength).</span><span class="sxs-lookup"><span data-stu-id="77b24-112">To find the maximum size, call [**IMFMediaBuffer::GetMaxLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength).</span></span>

-   <span data-ttu-id="77b24-113">La *longitud actual* es la cantidad de datos válidos que se encuentran actualmente en el búfer.</span><span class="sxs-lookup"><span data-stu-id="77b24-113">The *current length* is the amount of valid data that is currently in the buffer.</span></span> <span data-ttu-id="77b24-114">Cuando el búfer se asigna por primera vez, la longitud actual es cero, ya que no hay datos válidos en el búfer.</span><span class="sxs-lookup"><span data-stu-id="77b24-114">When the buffer is first allocated, the current length is zero, because there is no valid data in the buffer.</span></span> <span data-ttu-id="77b24-115">Si escribe datos en el búfer, debe actualizar la longitud actual llamando a [**IMFMediaBuffer:: SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength).</span><span class="sxs-lookup"><span data-stu-id="77b24-115">If you write any data to the buffer, you must update the current length by calling [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength).</span></span> <span data-ttu-id="77b24-116">Por ejemplo, si escribe 100 bytes de datos en el búfer, llame a **SetCurrentLength** con el valor 100.</span><span class="sxs-lookup"><span data-stu-id="77b24-116">For example, if you write 100 bytes of data into the buffer, call **SetCurrentLength** with the value 100.</span></span> <span data-ttu-id="77b24-117">Si lee los datos de un búfer multimedia, llame a [**IMFMediaBuffer:: GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) para averiguar la cantidad de datos que hay actualmente en el búfer.</span><span class="sxs-lookup"><span data-stu-id="77b24-117">If you read data from a media buffer, call [**IMFMediaBuffer::GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) to find out how much data is currently in the buffer.</span></span> <span data-ttu-id="77b24-118">No lea más allá de la longitud actual.</span><span class="sxs-lookup"><span data-stu-id="77b24-118">Do not read past the current length.</span></span> <span data-ttu-id="77b24-119">La longitud actual nunca puede superar la longitud máxima del búfer.</span><span class="sxs-lookup"><span data-stu-id="77b24-119">The current length can never exceed the maximum length of the buffer.</span></span>

## <a name="accessing-the-buffer-memory"></a><span data-ttu-id="77b24-120">Obtener acceso a la memoria de búfer</span><span class="sxs-lookup"><span data-stu-id="77b24-120">Accessing the Buffer Memory</span></span>

<span data-ttu-id="77b24-121">Para tener acceso a la memoria del búfer, llame a [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span><span class="sxs-lookup"><span data-stu-id="77b24-121">To access the memory in the buffer, call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span></span> <span data-ttu-id="77b24-122">Este método devuelve un puntero al principio del bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="77b24-122">This method returns a pointer to the start of the memory block.</span></span> <span data-ttu-id="77b24-123">También devuelve la longitud máxima y la longitud actual.</span><span class="sxs-lookup"><span data-stu-id="77b24-123">It also returns the maximum length and the current length.</span></span> <span data-ttu-id="77b24-124">Cuando haya terminado de usar el puntero, llame a [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span><span class="sxs-lookup"><span data-stu-id="77b24-124">When you are done using the pointer, call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span></span>

<span data-ttu-id="77b24-125">Para escribir datos en un búfer multimedia:</span><span class="sxs-lookup"><span data-stu-id="77b24-125">To write data into a media buffer:</span></span>

1.  <span data-ttu-id="77b24-126">Llame a [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para obtener un puntero a la memoria.</span><span class="sxs-lookup"><span data-stu-id="77b24-126">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the memory.</span></span> <span data-ttu-id="77b24-127">El método también devuelve la longitud máxima del búfer.</span><span class="sxs-lookup"><span data-stu-id="77b24-127">The method also returns the buffer's maximum length.</span></span>
2.  <span data-ttu-id="77b24-128">Escriba los datos en la memoria, hasta la longitud máxima del búfer.</span><span class="sxs-lookup"><span data-stu-id="77b24-128">Write your data into the memory, up to the buffer's maximum length.</span></span>
3.  <span data-ttu-id="77b24-129">Llame a [**IMFMediaBuffer:: SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) para actualizar la longitud actual.</span><span class="sxs-lookup"><span data-stu-id="77b24-129">Call [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) to update the current length.</span></span> <span data-ttu-id="77b24-130">Establezca la longitud actual igual a la cantidad de datos que escribió en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="77b24-130">Set the current length equal to the amount of data that you wrote in step 2.</span></span>
4.  <span data-ttu-id="77b24-131">Llame a [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) para desbloquear el búfer.</span><span class="sxs-lookup"><span data-stu-id="77b24-131">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer.</span></span>

<span data-ttu-id="77b24-132">Para leer datos de un búfer multimedia:</span><span class="sxs-lookup"><span data-stu-id="77b24-132">To read data from a media buffer:</span></span>

1.  <span data-ttu-id="77b24-133">Llame a [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para obtener un puntero a la memoria.</span><span class="sxs-lookup"><span data-stu-id="77b24-133">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the memory.</span></span> <span data-ttu-id="77b24-134">El método también devuelve la longitud actual del búfer (la cantidad de datos válidos en el búfer).</span><span class="sxs-lookup"><span data-stu-id="77b24-134">The method also returns the buffer's current length (the amount of valid data in the buffer).</span></span>
2.  <span data-ttu-id="77b24-135">Lea el contenido de la memoria hasta la longitud actual.</span><span class="sxs-lookup"><span data-stu-id="77b24-135">Read the contents of the memory, up to the current length.</span></span>
3.  <span data-ttu-id="77b24-136">Llame a [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) para desbloquear el búfer.</span><span class="sxs-lookup"><span data-stu-id="77b24-136">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer.</span></span>

## <a name="creating-system-memory-buffers"></a><span data-ttu-id="77b24-137">Crear búferes de memoria del sistema</span><span class="sxs-lookup"><span data-stu-id="77b24-137">Creating System Memory Buffers</span></span>

<span data-ttu-id="77b24-138">El búfer de memoria del sistema es un búfer de medios que administra un bloque de memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="77b24-138">The system memory buffer is a media buffer that manages a block of system memory.</span></span> <span data-ttu-id="77b24-139">Para crear una instancia de este objeto, llame a [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) o [**MFCreateAlignedMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer) y especifique un tamaño de búfer.</span><span class="sxs-lookup"><span data-stu-id="77b24-139">To create an instance of this object, call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) or [**MFCreateAlignedMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer) and specify a buffer size.</span></span> <span data-ttu-id="77b24-140">Ambas funciones asignan un bloque de memoria y devuelven un puntero [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="77b24-140">Both functions allocate a block of memory and return an [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) pointer.</span></span> <span data-ttu-id="77b24-141">La memoria se libera automáticamente cuando el recuento de referencias del búfer del medio llega a cero y se destruye el objeto.</span><span class="sxs-lookup"><span data-stu-id="77b24-141">The memory is automatically released when the media buffer's reference count reaches zero and the object is destroyed.</span></span>

<span data-ttu-id="77b24-142">En el ejemplo siguiente se muestra cómo crear un búfer de memoria del sistema y escribir en el búfer.</span><span class="sxs-lookup"><span data-stu-id="77b24-142">The following example shows how to create a system memory buffer and write to the buffer.</span></span>


```C++
HRESULT CreateSystemMemoryBuffer(
    BYTE *pSrc, 
    DWORD cbData, 
    IMFMediaBuffer **ppBuffer
    )
{
    HRESULT hr = S_OK;
    BYTE *pData = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    // Create the media buffer.
    hr = MFCreateMemoryBuffer(
        cbData,   // Amount of memory to allocate, in bytes.
        &pBuffer        
        );

    // Lock the buffer to get a pointer to the memory.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }

    if (SUCCEEDED(hr))
    {
        memcpy_s(pData, cbData, pSrc, cbData);
    }

    // Update the current length.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbData);
    }

    // Unlock the buffer.
    if (pData)
    {
        hr = pBuffer->Unlock();
    }

    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)->AddRef();
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="77b24-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="77b24-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77b24-144">Búferes multimedia</span><span class="sxs-lookup"><span data-stu-id="77b24-144">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="77b24-145">API de Media Foundation Platform</span><span class="sxs-lookup"><span data-stu-id="77b24-145">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



