---
description: Búferes de vídeo sin comprimir
ms.assetid: be5ec8a8-2d0b-401b-9d05-fdb87ad8c864
title: Búferes de vídeo sin comprimir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24eda19136bf2dd7bc77f95d0efa6c48ca96e79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696867"
---
# <a name="uncompressed-video-buffers"></a><span data-ttu-id="2c435-103">Búferes de vídeo sin comprimir</span><span class="sxs-lookup"><span data-stu-id="2c435-103">Uncompressed Video Buffers</span></span>

<span data-ttu-id="2c435-104">En este artículo se describe cómo trabajar con búferes multimedia que contienen fotogramas de vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="2c435-104">This article describes how to work with media buffers that contain uncompressed video frames.</span></span> <span data-ttu-id="2c435-105">En orden de preferencia, están disponibles las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="2c435-105">In order of preference, the following options are available.</span></span> <span data-ttu-id="2c435-106">No todos los búferes multimedia admiten cada opción.</span><span class="sxs-lookup"><span data-stu-id="2c435-106">Not every media buffer supports each option.</span></span>

1.  <span data-ttu-id="2c435-107">Usar la superficie de Direct3D subyacente.</span><span class="sxs-lookup"><span data-stu-id="2c435-107">Use the underlying Direct3D surface.</span></span> <span data-ttu-id="2c435-108">(Se aplica solo a fotogramas de vídeo almacenados en superficies de Direct3D).</span><span class="sxs-lookup"><span data-stu-id="2c435-108">(Applies only to video frames stored in Direct3D surfaces.)</span></span>
2.  <span data-ttu-id="2c435-109">Use la interfaz [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="2c435-109">Use the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>
3.  <span data-ttu-id="2c435-110">Use la interfaz [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="2c435-110">Use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span>

## <a name="use-the-underlying-direct3d-surface"></a><span data-ttu-id="2c435-111">Usar la superficie de Direct3D subyacente</span><span class="sxs-lookup"><span data-stu-id="2c435-111">Use the Underlying Direct3D Surface</span></span>

<span data-ttu-id="2c435-112">El fotograma de vídeo puede almacenarse dentro de una superficie de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2c435-112">The video frame might be stored inside a Direct3D surface.</span></span> <span data-ttu-id="2c435-113">Si es así, puede obtener un puntero a la superficie llamando a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) o [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) en el objeto de búfer de multimedia.</span><span class="sxs-lookup"><span data-stu-id="2c435-113">If so, you can get a pointer to the surface by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) or [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) on the media buffer object.</span></span> <span data-ttu-id="2c435-114">Use el servicio de búfer del identificador de servicio MR \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2c435-114">Use the service identifier MR\_BUFFER\_SERVICE.</span></span> <span data-ttu-id="2c435-115">Se recomienda este enfoque cuando el componente que tiene acceso al fotograma de vídeo está diseñado para usar Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2c435-115">This approach is recommended when the component accessing the video frame is designed to use Direct3D.</span></span> <span data-ttu-id="2c435-116">Por ejemplo, un descodificador de vídeo compatible con la aceleración de vídeo de DirectX debe utilizar este enfoque.</span><span class="sxs-lookup"><span data-stu-id="2c435-116">For example, a video decoder that supports DirectX Video Acceleration should use this approach.</span></span>

<span data-ttu-id="2c435-117">En el código siguiente se muestra cómo obtener el puntero **IDirect3DSurface9** desde un búfer multimedia.</span><span class="sxs-lookup"><span data-stu-id="2c435-117">The following code shows how to get the **IDirect3DSurface9** pointer from a media buffer.</span></span>


```C++
IDirect3DSurface9 *pSurface = NULL;

hr = MFGetService(
    pBuffer, 
    MR_BUFFER_SERVICE,
    __uuidof(IDirect3DSurface9), 
    (void**)&pSurface
    );

if (SUCCEEDED(hr))
{
    // Call IDirect3DSurface9 methods.
}
```



<span data-ttu-id="2c435-118">Los objetos siguientes admiten el servicio de **\_ \_ servicio de búfer Mr** :</span><span class="sxs-lookup"><span data-stu-id="2c435-118">The following objects support the **MR\_BUFFER\_SERVICE** service:</span></span>

-   [<span data-ttu-id="2c435-119">Búfer de superficie de DirectX</span><span class="sxs-lookup"><span data-stu-id="2c435-119">DirectX Surface Buffer</span></span>](directx-surface-buffer.md)
-   [<span data-ttu-id="2c435-120">Ejemplos de vídeo</span><span class="sxs-lookup"><span data-stu-id="2c435-120">Video Samples</span></span>](video-samples.md)

## <a name="use-the-imf2dbuffer-interface"></a><span data-ttu-id="2c435-121">Uso de la interfaz IMF2DBuffer</span><span class="sxs-lookup"><span data-stu-id="2c435-121">Use the IMF2DBuffer Interface</span></span>

<span data-ttu-id="2c435-122">Si el fotograma de vídeo no se almacena en una superficie de Direct3D, o el componente no está diseñado para usar Direct3D, la siguiente manera recomendada de acceder al fotograma de vídeo es consultar el búfer para la interfaz [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="2c435-122">If the video frame is not stored inside a Direct3D surface, or the component is not designed to use Direct3D, the next recommended way to access the video frame is to query the buffer for the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span> <span data-ttu-id="2c435-123">Esta interfaz está diseñada específicamente para los datos de imagen.</span><span class="sxs-lookup"><span data-stu-id="2c435-123">This interface is designed specifically for image data.</span></span> <span data-ttu-id="2c435-124">Para obtener un puntero a esta interfaz, llame a **QueryInterface** en el búfer multimedia.</span><span class="sxs-lookup"><span data-stu-id="2c435-124">To get a pointer to this interface, call **QueryInterface** on the media buffer.</span></span> <span data-ttu-id="2c435-125">No todos los objetos de búfer multimedia exponen esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="2c435-125">Not all media buffer objects expose this interface.</span></span> <span data-ttu-id="2c435-126">Pero si un búfer multimedia expone la interfaz **IMF2DBuffer** , debe usar esa interfaz para tener acceso a los datos, si es posible, en lugar de usar [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer).</span><span class="sxs-lookup"><span data-stu-id="2c435-126">But if a media buffer does expose the **IMF2DBuffer** interface, you should use that interface to access the data, if possible, rather than using [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer).</span></span> <span data-ttu-id="2c435-127">Todavía puede usar la interfaz **IMFMediaBuffer** , pero podría ser menos eficaz.</span><span class="sxs-lookup"><span data-stu-id="2c435-127">You can still use the **IMFMediaBuffer** interface, but it might be less efficient.</span></span>

1.  <span data-ttu-id="2c435-128">Llame a **QueryInterface** en el búfer multimedia para obtener la interfaz [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="2c435-128">Call **QueryInterface** on the media buffer to get the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>
2.  <span data-ttu-id="2c435-129">Llame a [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) para tener acceso a la memoria del búfer.</span><span class="sxs-lookup"><span data-stu-id="2c435-129">Call [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) to access the memory for the buffer.</span></span> <span data-ttu-id="2c435-130">Este método devuelve un puntero al primer byte de la fila superior de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2c435-130">This method returns a pointer to the first byte of the top row of pixels.</span></span> <span data-ttu-id="2c435-131">También devuelve el paso de la imagen, que es el número de bytes desde el inicio de una fila de píxeles hasta el inicio de la siguiente fila.</span><span class="sxs-lookup"><span data-stu-id="2c435-131">It also returns the image stride, which is the number of bytes from the start of a row of pixels to the start of the next row.</span></span> <span data-ttu-id="2c435-132">El búfer puede contener bytes de relleno después de cada fila de píxeles, por lo que el intervalo puede ser más ancho que el ancho de la imagen en bytes.</span><span class="sxs-lookup"><span data-stu-id="2c435-132">The buffer might contain padding bytes after each row of pixels, so the stride might be wider than the image width in bytes.</span></span> <span data-ttu-id="2c435-133">STRIDE también puede ser negativo si la imagen está orientada en orden ascendente en la memoria.</span><span class="sxs-lookup"><span data-stu-id="2c435-133">Stride can also be negative if the image is oriented bottom-up in memory.</span></span> <span data-ttu-id="2c435-134">Para obtener más información, consulte [STRIDE](image-stride.md)de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2c435-134">For more information, see [Image Stride](image-stride.md).</span></span>
3.  <span data-ttu-id="2c435-135">Mantenga el búfer bloqueado solo mientras necesite tener acceso a la memoria.</span><span class="sxs-lookup"><span data-stu-id="2c435-135">Keep the buffer locked only while you need to access the memory.</span></span> <span data-ttu-id="2c435-136">Desbloquee el búfer mediante una llamada a [**IMF2DBuffer:: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d).</span><span class="sxs-lookup"><span data-stu-id="2c435-136">Unlock the buffer by calling [**IMF2DBuffer::Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d).</span></span>

<span data-ttu-id="2c435-137">No todos los búferes multimedia implementan la interfaz [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="2c435-137">Not every media buffer implements the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span> <span data-ttu-id="2c435-138">Si el búfer multimedia no implementa esta interfaz (es decir, el objeto de búfer devuelve E \_ nointerface en el paso 1), debe usar la interfaz de la interfaz [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) , que se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="2c435-138">If the media buffer does not implement this interface (that is, the buffer object returns E\_NOINTERFACE in step 1), you must use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface interface, described next.</span></span>

## <a name="use-the-imfmediabuffer-interface"></a><span data-ttu-id="2c435-139">Uso de la interfaz IMFMediaBuffer</span><span class="sxs-lookup"><span data-stu-id="2c435-139">Use the IMFMediaBuffer Interface</span></span>

<span data-ttu-id="2c435-140">Si un búfer multimedia no expone la interfaz [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , use la interfaz [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="2c435-140">If a media buffer does not expose the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface, use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span> <span data-ttu-id="2c435-141">La semántica general de esta interfaz se describe en el tema [trabajar con búferes multimedia](working-with-media-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="2c435-141">The general semantics of this interface are described in the topic [Working with Media Buffers](working-with-media-buffers.md).</span></span>

1.  <span data-ttu-id="2c435-142">Llame a **QueryInterface** en el búfer multimedia para obtener la interfaz [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="2c435-142">Call **QueryInterface** on the media buffer to get the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span>
2.  <span data-ttu-id="2c435-143">Llame a [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para tener acceso a la memoria del búfer.</span><span class="sxs-lookup"><span data-stu-id="2c435-143">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to access the buffer memory.</span></span> <span data-ttu-id="2c435-144">Este método devuelve un puntero a la memoria del búfer.</span><span class="sxs-lookup"><span data-stu-id="2c435-144">This method returns a pointer to the buffer memory.</span></span> <span data-ttu-id="2c435-145">Cuando se usa el método de **bloqueo** , el intervalo es siempre el intervalo mínimo para el formato de vídeo en cuestión, sin bytes adicionales de relleno.</span><span class="sxs-lookup"><span data-stu-id="2c435-145">When the **Lock** method is used, the stride is always the minimum stride for the video format in question, with no extra padding bytes.</span></span>
3.  <span data-ttu-id="2c435-146">Mantenga el búfer bloqueado solo mientras necesite tener acceso a la memoria.</span><span class="sxs-lookup"><span data-stu-id="2c435-146">Keep the buffer locked only while you need to access the memory.</span></span> <span data-ttu-id="2c435-147">Desbloquee el búfer mediante una llamada a [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span><span class="sxs-lookup"><span data-stu-id="2c435-147">Unlock the buffer by calling [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span></span>

<span data-ttu-id="2c435-148">Siempre debe evitar llamar a [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) si el búfer expone [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer), ya que el método **Lock** puede forzar el objeto de búfer al fotograma de vídeo en un bloque de memoria contiguo y después volver de nuevo.</span><span class="sxs-lookup"><span data-stu-id="2c435-148">You should always avoid calling [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) if the buffer exposes [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer), because the **Lock** method can force the buffer object to the video frame into a contiguous memory block and then back again.</span></span> <span data-ttu-id="2c435-149">Por otro lado, si el búfer no es compatible con **IMF2DBuffer**, probablemente **IMFMediaBuffer:: Lock** no producirá una copia.</span><span class="sxs-lookup"><span data-stu-id="2c435-149">On the other hand, if the buffer does not support **IMF2DBuffer**, then **IMFMediaBuffer::Lock** will probably not result in a copy.</span></span>

<span data-ttu-id="2c435-150">Calcule el intervalo mínimo del tipo de medio como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="2c435-150">Calculate the minimum stride from the media type as follows:</span></span>

-   <span data-ttu-id="2c435-151">El intervalo mínimo puede almacenarse en el atributo de [**\_ \_ \_ intervalo MF MT predeterminado**](mf-mt-default-stride-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="2c435-151">The minimum stride might be stored in the [**MF\_MT\_DEFAULT\_STRIDE**](mf-mt-default-stride-attribute.md) attribute.</span></span>
-   <span data-ttu-id="2c435-152">Si no se ha establecido el atributo de **\_ \_ \_ intervalo MF MT predeterminado** , llame a la función [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) para calcular el intervalo para los formatos de vídeo más comunes.</span><span class="sxs-lookup"><span data-stu-id="2c435-152">If the **MF\_MT\_DEFAULT\_STRIDE** attribute is not set, call the [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) function to calculate the stride for most common video formats.</span></span>
-   <span data-ttu-id="2c435-153">Si la función [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) no reconoce el formato, debe calcular el intervalo en función de la definición del formato.</span><span class="sxs-lookup"><span data-stu-id="2c435-153">If the [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) function does not recognize the format, you must calculate the stride based on the definition of the format.</span></span> <span data-ttu-id="2c435-154">En ese caso, no hay ninguna regla general; necesita conocer los detalles de la definición de formato.</span><span class="sxs-lookup"><span data-stu-id="2c435-154">In that case, there is no general rule; you need to know the details of the format definition.</span></span>

<span data-ttu-id="2c435-155">En el código siguiente se muestra cómo obtener el intervalo predeterminado para los formatos de vídeo más comunes.</span><span class="sxs-lookup"><span data-stu-id="2c435-155">The following code shows how to get the default stride for the most common video formats.</span></span>


```C++
HRESULT GetDefaultStride(IMFMediaType *pType, LONG *plStride)
{
    LONG lStride = 0;

    // Try to get the default stride from the media type.
    HRESULT hr = pType->GetUINT32(MF_MT_DEFAULT_STRIDE, (UINT32*)&lStride);
    if (FAILED(hr))
    {
        // Attribute not set. Try to calculate the default stride.

        GUID subtype = GUID_NULL;

        UINT32 width = 0;
        UINT32 height = 0;

        // Get the subtype and the image size.
        hr = pType->GetGUID(MF_MT_SUBTYPE, &subtype);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetStrideForBitmapInfoHeader(subtype.Data1, width, &lStride);
        if (FAILED(hr))
        {
            goto done;
        }

        // Set the attribute for later reference.
        (void)pType->SetUINT32(MF_MT_DEFAULT_STRIDE, UINT32(lStride));
    }

    if (SUCCEEDED(hr))
    {
        *plStride = lStride;
    }

done:
    return hr;
}
```



<span data-ttu-id="2c435-156">En función de la aplicación, puede saber de antemano si un búfer multimedia determinado admite [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) (por ejemplo, si ha creado el búfer).</span><span class="sxs-lookup"><span data-stu-id="2c435-156">Depending on your application, you might know in advance whether a given media buffer supports [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) (for example, if you created the buffer).</span></span> <span data-ttu-id="2c435-157">De lo contrario, debe estar preparado para usar cualquiera de las dos interfaces de búfer.</span><span class="sxs-lookup"><span data-stu-id="2c435-157">Otherwise, you must be prepared to use either of the two buffer interfaces.</span></span>

<span data-ttu-id="2c435-158">En el ejemplo siguiente se muestra una clase auxiliar que oculta algunos de estos detalles.</span><span class="sxs-lookup"><span data-stu-id="2c435-158">The following example shows a helper class that hides some of these details.</span></span> <span data-ttu-id="2c435-159">Esta clase tiene un método LockBuffer que llama a [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) o [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) y devuelve un puntero al principio de la primera fila de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2c435-159">This class has a LockBuffer method that calls either [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) or [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) and returns a pointer to the start of the first row of pixels.</span></span> <span data-ttu-id="2c435-160">(Este comportamiento coincide con el método **Lock2D** ). El método LockBuffer toma el intervalo predeterminado como parámetro de entrada y devuelve el intervalo real como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="2c435-160">(This behavior matches the **Lock2D** method.) The LockBuffer method takes the default stride as an input parameter and returns the actual stride as an output parameter.</span></span>


```C++
class CBufferLock
{
public:
    CBufferLock(IMFMediaBuffer *pBuffer) : m_p2DBuffer(NULL), m_bLocked(FALSE)
    {
        m_pBuffer = pBuffer;
        m_pBuffer->AddRef();

        m_pBuffer->QueryInterface(IID_IMF2DBuffer, (void**)&m_p2DBuffer);
    }

    ~CBufferLock()
    {
        UnlockBuffer();
        SafeRelease(&m_pBuffer);
        SafeRelease(&m_p2DBuffer);
    }

    HRESULT LockBuffer(
        LONG  lDefaultStride,    // Minimum stride (with no padding).
        DWORD dwHeightInPixels,  // Height of the image, in pixels.
        BYTE  **ppbScanLine0,    // Receives a pointer to the start of scan line 0.
        LONG  *plStride          // Receives the actual stride.
        )
    {
        HRESULT hr = S_OK;

        // Use the 2-D version if available.
        if (m_p2DBuffer)
        {
            hr = m_p2DBuffer->Lock2D(ppbScanLine0, plStride);
        }
        else
        {
            // Use non-2D version.
            BYTE *pData = NULL;

            hr = m_pBuffer->Lock(&pData, NULL, NULL);
            if (SUCCEEDED(hr))
            {
                *plStride = lDefaultStride;
                if (lDefaultStride < 0)
                {
                    // Bottom-up orientation. Return a pointer to the start of the
                    // last row *in memory* which is the top row of the image.
                    *ppbScanLine0 = pData + abs(lDefaultStride) * (dwHeightInPixels - 1);
                }
                else
                {
                    // Top-down orientation. Return a pointer to the start of the
                    // buffer.
                    *ppbScanLine0 = pData;
                }
            }
        }

        m_bLocked = (SUCCEEDED(hr));

        return hr;
    }
    
    void UnlockBuffer()
    {
        if (m_bLocked)
        {
            if (m_p2DBuffer)
            {
                (void)m_p2DBuffer->Unlock2D();
            }
            else
            {
                (void)m_pBuffer->Unlock();
            }
            m_bLocked = FALSE;
        }
    }

private:
    IMFMediaBuffer  *m_pBuffer;
    IMF2DBuffer     *m_p2DBuffer;

    BOOL            m_bLocked;
};
```



## <a name="related-topics"></a><span data-ttu-id="2c435-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2c435-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c435-162">Intervalo de imagen</span><span class="sxs-lookup"><span data-stu-id="2c435-162">Image Stride</span></span>](image-stride.md)
</dt> <dt>

[<span data-ttu-id="2c435-163">Búferes multimedia</span><span class="sxs-lookup"><span data-stu-id="2c435-163">Media Buffers</span></span>](media-buffers.md)
</dt> </dl>

 

 



