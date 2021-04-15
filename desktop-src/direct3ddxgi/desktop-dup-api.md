---
description: Windows 8 deshabilita los controladores de reflejo estándar del modelo de controladores de pantalla de Windows 2000 (XDDM) y ofrece en su lugar la API de duplicado de escritorio.
ms.assetid: 523FBFAD-5D78-4EE3-A3B7-8FD5BA39DC46
title: API de duplicación de escritorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad27f545318254404beb6372344d8dd0cdfdf604
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494561"
---
# <a name="desktop-duplication-api"></a><span data-ttu-id="af420-103">API de duplicación de escritorio</span><span class="sxs-lookup"><span data-stu-id="af420-103">Desktop Duplication API</span></span>

<span data-ttu-id="af420-104">Windows 8 deshabilita los controladores de reflejo estándar del modelo de controladores de pantalla de Windows 2000 (XDDM) y ofrece en su lugar la API de duplicado de escritorio.</span><span class="sxs-lookup"><span data-stu-id="af420-104">Windows 8 disables standard Windows 2000 Display Driver Model (XDDM) mirror drivers and offers the desktop duplication API instead.</span></span> <span data-ttu-id="af420-105">La API de duplicación de escritorio proporciona acceso remoto a una imagen de escritorio para escenarios de colaboración.</span><span class="sxs-lookup"><span data-stu-id="af420-105">The desktop duplication API provides remote access to a desktop image for collaboration scenarios.</span></span> <span data-ttu-id="af420-106">Las aplicaciones pueden usar la API de duplicación de escritorio para tener acceso a las actualizaciones de fotogramas fotogramas en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="af420-106">Apps can use the desktop duplication API to access frame-by-frame updates to the desktop.</span></span> <span data-ttu-id="af420-107">Dado que las aplicaciones reciben actualizaciones de la imagen de escritorio en una superficie de DXGI, las aplicaciones pueden usar toda la capacidad de la GPU para procesar las actualizaciones de la imagen.</span><span class="sxs-lookup"><span data-stu-id="af420-107">Because apps receive updates to the desktop image in a DXGI surface, the apps can use the full power of the GPU to process the image updates.</span></span>

-   [<span data-ttu-id="af420-108">Actualización de los datos de imagen de escritorio</span><span class="sxs-lookup"><span data-stu-id="af420-108">Updating the desktop image data</span></span>](#updating-the-desktop-image-data)
-   [<span data-ttu-id="af420-109">Girar la imagen de escritorio</span><span class="sxs-lookup"><span data-stu-id="af420-109">Rotating the desktop image</span></span>](#rotating-the-desktop-image)
-   [<span data-ttu-id="af420-110">Actualizar el puntero de escritorio</span><span class="sxs-lookup"><span data-stu-id="af420-110">Updating the desktop pointer</span></span>](#updating-the-desktop-pointer)
-   [<span data-ttu-id="af420-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="af420-111">Related topics</span></span>](#related-topics)

## <a name="updating-the-desktop-image-data"></a><span data-ttu-id="af420-112">Actualización de los datos de imagen de escritorio</span><span class="sxs-lookup"><span data-stu-id="af420-112">Updating the desktop image data</span></span>

<span data-ttu-id="af420-113">DXGI proporciona una superficie que contiene una imagen de escritorio actual a través del nuevo método [**IDXGIOutputDuplication:: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) .</span><span class="sxs-lookup"><span data-stu-id="af420-113">DXGI provides a surface that contains a current desktop image through the new [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) method.</span></span> <span data-ttu-id="af420-114">El formato de la imagen de escritorio siempre es el [**formato de DXGI \_ \_ B8G8R8A8 \_ UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) , independientemente del modo de presentación actual.</span><span class="sxs-lookup"><span data-stu-id="af420-114">The format of the desktop image is always [**DXGI\_FORMAT\_B8G8R8A8\_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) no matter what the current display mode is.</span></span> <span data-ttu-id="af420-115">Junto con esta superficie, estos métodos [**IDXGIOutputDuplication**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) devuelven los tipos de información indicados que le ayudarán a determinar qué píxeles de la superficie debe procesar:</span><span class="sxs-lookup"><span data-stu-id="af420-115">Along with this surface, these [**IDXGIOutputDuplication**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) methods return the indicated types of info that help you determine which pixels within the surface you need to process:</span></span>

-   <span data-ttu-id="af420-116">[**IDXGIOutputDuplication:: GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) devuelve regiones desfasadas, que son rectángulos no superpuestos que indican las áreas de la imagen de escritorio que el sistema operativo ha actualizado desde que se procesó la imagen de escritorio anterior.</span><span class="sxs-lookup"><span data-stu-id="af420-116">[**IDXGIOutputDuplication::GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) returns dirty regions, which are non-overlapping rectangles that indicate the areas of the desktop image that the operating system updated since you processed the previous desktop image.</span></span>
-   <span data-ttu-id="af420-117">[**IDXGIOutputDuplication:: GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) devuelve regiones de movimiento, que son rectángulos de píxeles de la imagen de escritorio que el sistema operativo ha movido a otra ubicación dentro de la misma imagen.</span><span class="sxs-lookup"><span data-stu-id="af420-117">[**IDXGIOutputDuplication::GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) returns move regions, which are rectangles of pixels in the desktop image that the operating system moved to another location within the same image.</span></span> <span data-ttu-id="af420-118">Cada región de movimiento consta de un rectángulo de destino y un punto de origen.</span><span class="sxs-lookup"><span data-stu-id="af420-118">Each move region consists of a destination rectangle and a source point.</span></span> <span data-ttu-id="af420-119">El punto de origen especifica la ubicación desde la que el sistema operativo ha copiado la región y el rectángulo de destino especifica el lugar en el que el sistema operativo ha despasado esa región.</span><span class="sxs-lookup"><span data-stu-id="af420-119">The source point specifies the location from where the operating system copied the region and the destination rectangle specifies to where the operating system moved that region.</span></span> <span data-ttu-id="af420-120">Las regiones de movimiento siempre son regiones no estiradas, por lo que el origen siempre tiene el mismo tamaño que el destino.</span><span class="sxs-lookup"><span data-stu-id="af420-120">Move regions are always non-stretched regions so the source is always the same size as the destination.</span></span>

<span data-ttu-id="af420-121">Supongamos que la imagen de escritorio se ha transmitido a través de una conexión lenta a la aplicación cliente remota.</span><span class="sxs-lookup"><span data-stu-id="af420-121">Suppose the desktop image was transmitted over a slow connection to your remote client app.</span></span> <span data-ttu-id="af420-122">La cantidad de datos que se envían a través de la conexión se reduce recibiendo solo datos sobre cómo la aplicación cliente debe trasladar regiones de píxeles en lugar de datos de píxeles reales.</span><span class="sxs-lookup"><span data-stu-id="af420-122">The amount of data that is sent over the connection is reduced by receiving only data about how your client app must move regions of pixels rather than actual pixel data.</span></span> <span data-ttu-id="af420-123">Para procesar los movimientos, la aplicación cliente debe haber almacenado la última imagen completa.</span><span class="sxs-lookup"><span data-stu-id="af420-123">To process the moves, your client app must have stored the complete last image.</span></span>

<span data-ttu-id="af420-124">Aunque el sistema operativo acumula actualizaciones de imágenes de escritorio no procesadas, podría quedarse sin espacio para almacenar de forma precisa las regiones de actualización.</span><span class="sxs-lookup"><span data-stu-id="af420-124">While the operating system accumulates unprocessed desktop image updates, it might run out of space to accurately store the update regions.</span></span> <span data-ttu-id="af420-125">En esta situación, el sistema operativo comienza a acumular las actualizaciones mediante la combinación de las regiones de actualización existentes para cubrir todas las actualizaciones nuevas.</span><span class="sxs-lookup"><span data-stu-id="af420-125">In this situation, the operating system starts to accumulate the updates by coalescing them with existing update regions to cover all new updates.</span></span> <span data-ttu-id="af420-126">Como resultado, el sistema operativo cubre los píxeles que todavía no se han actualizado en ese marco.</span><span class="sxs-lookup"><span data-stu-id="af420-126">As a result, the operating system covers pixels that it has not actually updated in that frame yet.</span></span> <span data-ttu-id="af420-127">Sin embargo, esta situación no genera problemas visuales en la aplicación cliente porque recibe la imagen de escritorio completa y no solo los píxeles actualizados.</span><span class="sxs-lookup"><span data-stu-id="af420-127">But this situation doesn’t produce visual issues on your client app because you receive the entire desktop image and not just the updated pixels.</span></span>

<span data-ttu-id="af420-128">Para reconstruir la imagen de escritorio correcta, la aplicación cliente debe procesar primero todas las regiones de movimiento y, a continuación, procesar todas las regiones desfasadas.</span><span class="sxs-lookup"><span data-stu-id="af420-128">To reconstruct the correct desktop image, your client app must first process all the move regions and then process all the dirty regions.</span></span> <span data-ttu-id="af420-129">Cualquiera de estas listas de regiones desfasadas y de movimiento puede estar completamente vacía.</span><span class="sxs-lookup"><span data-stu-id="af420-129">Either of these lists of dirty and move regions can be completely empty.</span></span> <span data-ttu-id="af420-130">El código de ejemplo del [ejemplo de duplicación de escritorio](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) muestra cómo procesar las regiones desfasadas y de movimiento en un solo fotograma:</span><span class="sxs-lookup"><span data-stu-id="af420-130">The example code from the [Desktop Duplication Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) shows how to process both the dirty and move regions in a single frame:</span></span>


```C++
//
// Get next frame and write it into Data
//
HRESULT DUPLICATIONMANAGER::GetFrame(_Out_ FRAME_DATA* Data)
{
    HRESULT hr = S_OK;

    IDXGIResource* DesktopResource = NULL;
    DXGI_OUTDUPL_FRAME_INFO FrameInfo;

    //Get new frame
    hr = DeskDupl->AcquireNextFrame(500, &FrameInfo, &DesktopResource);
    if (FAILED(hr))
    {
        if ((hr != DXGI_ERROR_ACCESS_LOST) && (hr != DXGI_ERROR_WAIT_TIMEOUT))
        {
            DisplayErr(L"Failed to acquire next frame in DUPLICATIONMANAGER", L"Error", hr);
        }
        return hr;
    }

    // If still holding old frame, destroy it
    if (AcquiredDesktopImage)
    {
        AcquiredDesktopImage->Release();
        AcquiredDesktopImage = NULL;
    }

    // QI for IDXGIResource
    hr = DesktopResource->QueryInterface(__uuidof(ID3D11Texture2D), reinterpret_cast<void **>(&AcquiredDesktopImage));
    DesktopResource->Release();
    DesktopResource = NULL;
    if (FAILED(hr))
    {
        DisplayErr(L"Failed to QI for ID3D11Texture2D from acquired IDXGIResource in DUPLICATIONMANAGER", L"Error", hr);
        return hr;
    }

    // Get metadata
    if (FrameInfo.TotalMetadataBufferSize)
    {
        // Old buffer too small
        if (FrameInfo.TotalMetadataBufferSize > MetaDataSize)
        {
            if (MetaDataBuffer)
            {
                delete [] MetaDataBuffer;
                MetaDataBuffer = NULL;
            }
            MetaDataBuffer = new (std::nothrow) BYTE[FrameInfo.TotalMetadataBufferSize];
            if (!MetaDataBuffer)
            {
                DisplayErr(L"Failed to allocate memory for metadata in DUPLICATIONMANAGER", L"Error", E_OUTOFMEMORY);
                MetaDataSize = 0;
                Data->MoveCount = 0;
                Data->DirtyCount = 0;
                return E_OUTOFMEMORY;
            }
            MetaDataSize = FrameInfo.TotalMetadataBufferSize;
        }

        UINT BufSize = FrameInfo.TotalMetadataBufferSize;

        // Get move rectangles
        hr = DeskDupl->GetFrameMoveRects(BufSize, reinterpret_cast<DXGI_OUTDUPL_MOVE_RECT*>(MetaDataBuffer), &BufSize);
        if (FAILED(hr))
        {
            if (hr != DXGI_ERROR_ACCESS_LOST)
            {
                DisplayErr(L"Failed to get frame move rects in DUPLICATIONMANAGER", L"Error", hr);
            }
            Data->MoveCount = 0;
            Data->DirtyCount = 0;
            return hr;
        }
        Data->MoveCount = BufSize / sizeof(DXGI_OUTDUPL_MOVE_RECT);

        BYTE* DirtyRects = MetaDataBuffer + BufSize;
        BufSize = FrameInfo.TotalMetadataBufferSize - BufSize;

        // Get dirty rectangles
        hr = DeskDupl->GetFrameDirtyRects(BufSize, reinterpret_cast<RECT*>(DirtyRects), &BufSize);
        if (FAILED(hr))
        {
            if (hr != DXGI_ERROR_ACCESS_LOST)
            {
                DisplayErr(L"Failed to get frame dirty rects in DUPLICATIONMANAGER", L"Error", hr);
            }
            Data->MoveCount = 0;
            Data->DirtyCount = 0;
            return hr;
        }
        Data->DirtyCount = BufSize / sizeof(RECT);

        Data->MetaData = MetaDataBuffer;
    }

    Data->Frame = AcquiredDesktopImage;
    Data->FrameInfo = FrameInfo;

    return hr;
}

//
// Release frame
//
HRESULT DUPLICATIONMANAGER::DoneWithFrame()
{
    HRESULT hr = S_OK;

    hr = DeskDupl->ReleaseFrame();
    if (FAILED(hr))
    {
        DisplayErr(L"Failed to release frame in DUPLICATIONMANAGER", L"Error", hr);
        return hr;
    }

    if (AcquiredDesktopImage)
    {
        AcquiredDesktopImage->Release();
        AcquiredDesktopImage = NULL;
    }

    return hr;
}
```



## <a name="rotating-the-desktop-image"></a><span data-ttu-id="af420-131">Girar la imagen de escritorio</span><span class="sxs-lookup"><span data-stu-id="af420-131">Rotating the desktop image</span></span>

<span data-ttu-id="af420-132">Debe agregar código explícito a la aplicación cliente de duplicación de escritorio para admitir modos girados.</span><span class="sxs-lookup"><span data-stu-id="af420-132">You must add explicit code to your desktop duplication client app to support rotated modes.</span></span> <span data-ttu-id="af420-133">En un modo girado, la superficie que recibe de [**IDXGIOutputDuplication:: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) siempre está en la orientación no girada y la imagen del escritorio se gira dentro de la superficie.</span><span class="sxs-lookup"><span data-stu-id="af420-133">In a rotated mode, the surface that you receive from [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) is always in the un-rotated orientation, and the desktop image is rotated within the surface.</span></span> <span data-ttu-id="af420-134">Por ejemplo, si el escritorio se establece en 768x1024 con una rotación de 90 grados, **AcquireNextFrame** devuelve una superficie de 1024x768 con la imagen de escritorio girada dentro de ella.</span><span class="sxs-lookup"><span data-stu-id="af420-134">For example, if the desktop is set to 768x1024 at 90 degrees rotation, **AcquireNextFrame** returns a 1024x768 surface with the desktop image rotated within it.</span></span> <span data-ttu-id="af420-135">Estos son algunos ejemplos de rotación.</span><span class="sxs-lookup"><span data-stu-id="af420-135">Here are some rotation examples.</span></span>



| <span data-ttu-id="af420-136">Modo de presentación establecido en Mostrar panel de control</span><span class="sxs-lookup"><span data-stu-id="af420-136">Display mode set from display control panel</span></span> | <span data-ttu-id="af420-137">Modo de presentación devuelto por GDI o DXGI</span><span class="sxs-lookup"><span data-stu-id="af420-137">Display mode returned by GDI or DXGI</span></span> | <span data-ttu-id="af420-138">Superficie devuelta por [ **AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)</span><span class="sxs-lookup"><span data-stu-id="af420-138">Surface returned from [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)</span></span>                |
|---------------------------------------------|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af420-139">vertical 1024x768</span><span class="sxs-lookup"><span data-stu-id="af420-139">1024x768 landscape</span></span>                          | <span data-ttu-id="af420-140">rotación de 0 grados 1024x768</span><span class="sxs-lookup"><span data-stu-id="af420-140">1024x768 0 degree rotation</span></span>           | <span data-ttu-id="af420-141">\[nueva línea 1024x768\]</span><span class="sxs-lookup"><span data-stu-id="af420-141">1024x768\[newline\]</span></span> ![escritorio remoto no girado](images/dxgi-outdupl-0-rotate.png)<br/>            |
| <span data-ttu-id="af420-143">1024x768 vertical</span><span class="sxs-lookup"><span data-stu-id="af420-143">1024x768 portrait</span></span>                           | <span data-ttu-id="af420-144">rotación de 768x1024 90 grados</span><span class="sxs-lookup"><span data-stu-id="af420-144">768x1024 90 degree rotation</span></span>          | <span data-ttu-id="af420-145">\[nueva línea 1024x768\]</span><span class="sxs-lookup"><span data-stu-id="af420-145">1024x768\[newline\]</span></span> ![escritorio remoto girado 90 grados](images/dxgi-outdupl-90-rotate.png)<br/>   |
| <span data-ttu-id="af420-147">1024x768 horizontalmente (volteado)</span><span class="sxs-lookup"><span data-stu-id="af420-147">1024x768 landscape (flipped)</span></span>                | <span data-ttu-id="af420-148">rotación de grado de 1024x768 180</span><span class="sxs-lookup"><span data-stu-id="af420-148">1024x768 180 degree rotation</span></span>         | <span data-ttu-id="af420-149">\[nueva línea 1024x768\]</span><span class="sxs-lookup"><span data-stu-id="af420-149">1024x768\[newline\]</span></span> ![escritorio remoto girado 180 grados](images/dxgi-outdupl-180-rotate.png)<br/> |
| <span data-ttu-id="af420-151">1024x768 vertical (volteado)</span><span class="sxs-lookup"><span data-stu-id="af420-151">1024x768 portrait (flipped)</span></span>                 | <span data-ttu-id="af420-152">rotación de 768x1024 270 grados</span><span class="sxs-lookup"><span data-stu-id="af420-152">768x1024 270 degree rotation</span></span>         | <span data-ttu-id="af420-153">\[nueva línea 1024x768\]</span><span class="sxs-lookup"><span data-stu-id="af420-153">1024x768\[newline\]</span></span> ![escritorio remoto girado 270 grados](images/dxgi-outdupl-270-rotate.png)<br/> |



 

<span data-ttu-id="af420-155">El código de la aplicación cliente de duplicación de escritorio debe girar la imagen de escritorio correctamente antes de mostrar la imagen de escritorio.</span><span class="sxs-lookup"><span data-stu-id="af420-155">The code in your desktop duplication client app must rotate the desktop image appropriately before you display the desktop image.</span></span>

> [!Note]  
> <span data-ttu-id="af420-156">En escenarios de varios monitores, puede girar la imagen de escritorio de cada monitor de manera independiente.</span><span class="sxs-lookup"><span data-stu-id="af420-156">In multi-monitor scenarios, you can rotate the desktop image for each monitor independently.</span></span>

 

## <a name="updating-the-desktop-pointer"></a><span data-ttu-id="af420-157">Actualizar el puntero de escritorio</span><span class="sxs-lookup"><span data-stu-id="af420-157">Updating the desktop pointer</span></span>

<span data-ttu-id="af420-158">Debe usar la API de duplicación de escritorio para determinar si la aplicación cliente debe dibujar la forma del puntero del mouse en la imagen del escritorio.</span><span class="sxs-lookup"><span data-stu-id="af420-158">You need to use the desktop duplication API to determine if your client app must draw the mouse pointer shape onto the desktop image.</span></span> <span data-ttu-id="af420-159">Ya se ha dibujado el puntero del mouse en la imagen de escritorio que [**IDXGIOutputDuplication:: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) proporciona o el puntero del mouse es independiente de la imagen del escritorio.</span><span class="sxs-lookup"><span data-stu-id="af420-159">Either the mouse pointer is already drawn onto the desktop image that [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) provides or the mouse pointer is separate from the desktop image.</span></span> <span data-ttu-id="af420-160">Si el puntero del mouse se dibuja en la imagen del escritorio, los datos de la posición del puntero informados por **AcquireNextFrame** (en el miembro **PointerPosition** de la  [**\_ \_ \_ información de fotogramas de DXGI OUTDUPL**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) al que apunta el parámetro pFrameInfo) indican que un puntero independiente no está visible.</span><span class="sxs-lookup"><span data-stu-id="af420-160">If the mouse pointer is drawn onto the desktop image, the pointer position data that is reported by **AcquireNextFrame** (in the **PointerPosition** member of [**DXGI\_OUTDUPL\_FRAME\_INFO**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) that the *pFrameInfo* parameter points to) indicates that a separate pointer isn’t visible.</span></span> <span data-ttu-id="af420-161">Si el adaptador de gráficos superpone el puntero del mouse encima de la imagen del escritorio, **AcquireNextFrame** informa de que hay un puntero independiente visible.</span><span class="sxs-lookup"><span data-stu-id="af420-161">If the graphics adapter overlays the mouse pointer on top of the desktop image, **AcquireNextFrame** reports that a separate pointer is visible.</span></span> <span data-ttu-id="af420-162">Por lo tanto, la aplicación cliente debe dibujar la forma puntero del mouse en la imagen de escritorio para representar con precisión lo que el usuario actual verá en su monitor.</span><span class="sxs-lookup"><span data-stu-id="af420-162">So, your client app must draw the mouse pointer shape onto the desktop image to accurately represent what the current user will see on their monitor.</span></span>

<span data-ttu-id="af420-163">Para dibujar el puntero del mouse del escritorio, use el miembro **PointerPosition** de la [**\_ \_ \_ información de fotogramas de DXGI OUTDUPL**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) del parámetro *pFrameInfo* de [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) para determinar dónde ubicar la esquina superior izquierda del puntero del mouse en la imagen de escritorio.</span><span class="sxs-lookup"><span data-stu-id="af420-163">To draw the desktop’s mouse pointer, use the **PointerPosition** member of [**DXGI\_OUTDUPL\_FRAME\_INFO**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) from the *pFrameInfo* parameter of [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) to determine where to locate the top left hand corner of the mouse pointer on the desktop image.</span></span> <span data-ttu-id="af420-164">Al dibujar el primer fotograma, debe usar el método [**IDXGIOutputDuplication:: GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) para obtener información sobre la forma del puntero del mouse.</span><span class="sxs-lookup"><span data-stu-id="af420-164">When you draw the first frame, you must use the [**IDXGIOutputDuplication::GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) method to obtain info about the shape of the mouse pointer.</span></span> <span data-ttu-id="af420-165">Cada llamada a **AcquireNextFrame** para obtener el fotograma siguiente también proporciona la posición actual del puntero para ese marco.</span><span class="sxs-lookup"><span data-stu-id="af420-165">Each call to **AcquireNextFrame** to get the next frame also provides the current pointer position for that frame.</span></span> <span data-ttu-id="af420-166">Por otro lado, debe volver a usar **GetFramePointerShape** solo si la forma cambia.</span><span class="sxs-lookup"><span data-stu-id="af420-166">On the other hand, you need to use **GetFramePointerShape** again only if the shape changes.</span></span> <span data-ttu-id="af420-167">Por lo tanto, mantenga una copia de la última imagen de puntero y Úsela para dibujar en el escritorio a menos que cambie la forma del puntero del mouse.</span><span class="sxs-lookup"><span data-stu-id="af420-167">So, keep a copy of the last pointer image and use it to draw on the desktop unless the shape of the mouse pointer changes.</span></span>

> [!Note]  
> <span data-ttu-id="af420-168">Junto con la imagen de la forma de puntero, [**GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) proporciona el tamaño de la ubicación de la zona activa.</span><span class="sxs-lookup"><span data-stu-id="af420-168">Together with the pointer shape image, [**GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) provides the size of the hot spot location.</span></span> <span data-ttu-id="af420-169">La zona activa solo se proporciona con fines informativos.</span><span class="sxs-lookup"><span data-stu-id="af420-169">The hot spot is given for informational purposes only.</span></span> <span data-ttu-id="af420-170">La ubicación donde se dibuja la imagen del puntero es independiente de la zona activa.</span><span class="sxs-lookup"><span data-stu-id="af420-170">The location of where to draw the pointer image is independent to the hotspot.</span></span>

 

<span data-ttu-id="af420-171">Este código de ejemplo del [ejemplo de duplicación del escritorio](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) muestra cómo obtener la forma del puntero del mouse:</span><span class="sxs-lookup"><span data-stu-id="af420-171">This example code from the [Desktop Duplication Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) shows how to get the mouse pointer shape:</span></span>


```C++
//
// Retrieves mouse info and write it into PtrInfo
//
HRESULT DUPLICATIONMANAGER::GetMouse(_Out_ PTR_INFO* PtrInfo, _In_ DXGI_OUTDUPL_FRAME_INFO* FrameInfo, INT OffsetX, INT OffsetY)
{
    HRESULT hr = S_OK;

    // A non-zero mouse update timestamp indicates that there is a mouse position update and optionally a shape change
    if (FrameInfo->LastMouseUpdateTime.QuadPart == 0)
    {
        return hr;
    }

    bool UpdatePosition = true;

    // Make sure we don't update pointer position wrongly
    // If pointer is invisible, make sure we did not get an update from another output that the last time that said pointer
    // was visible, if so, don't set it to invisible or update.
    if (!FrameInfo->PointerPosition.Visible && (PtrInfo->WhoUpdatedPositionLast != OutputNumber))
    {
        UpdatePosition = false;
    }

    // If two outputs both say they have a visible, only update if new update has newer timestamp
    if (FrameInfo->PointerPosition.Visible && PtrInfo->Visible && (PtrInfo->WhoUpdatedPositionLast != OutputNumber) && (PtrInfo->LastTimeStamp.QuadPart > FrameInfo->LastMouseUpdateTime.QuadPart))
    {
        UpdatePosition = false;
    }

    // Update position
    if (UpdatePosition)
    {
        PtrInfo->Position.x = FrameInfo->PointerPosition.Position.x + OutputDesc.DesktopCoordinates.left - OffsetX;
        PtrInfo->Position.y = FrameInfo->PointerPosition.Position.y + OutputDesc.DesktopCoordinates.top - OffsetY;
        PtrInfo->WhoUpdatedPositionLast = OutputNumber;
        PtrInfo->LastTimeStamp = FrameInfo->LastMouseUpdateTime;
        PtrInfo->Visible = FrameInfo->PointerPosition.Visible != 0;
    }

    // No new shape
    if (FrameInfo->PointerShapeBufferSize == 0)
    {
        return hr;
    }

    // Old buffer too small
    if (FrameInfo->PointerShapeBufferSize > PtrInfo->BufferSize)
    {
        if (PtrInfo->PtrShapeBuffer)
        {
            delete [] PtrInfo->PtrShapeBuffer;
            PtrInfo->PtrShapeBuffer = NULL;
        }
        PtrInfo->PtrShapeBuffer = new (std::nothrow) BYTE[FrameInfo->PointerShapeBufferSize];
        if (!PtrInfo->PtrShapeBuffer)
        {
            DisplayErr(L"Failed to allocate memory for pointer shape in DUPLICATIONMANAGER", L"Error", E_OUTOFMEMORY);
            PtrInfo->BufferSize = 0;
            return E_OUTOFMEMORY;
        }

        // Update buffer size
        PtrInfo->BufferSize = FrameInfo->PointerShapeBufferSize;
    }

    UINT BufferSizeRequired;
    // Get shape
    hr = DeskDupl->GetFramePointerShape(FrameInfo->PointerShapeBufferSize, reinterpret_cast<VOID*>(PtrInfo->PtrShapeBuffer), &BufferSizeRequired, &(PtrInfo->ShapeInfo));
    if (FAILED(hr))
    {
        if (hr != DXGI_ERROR_ACCESS_LOST)
        {
            DisplayErr(L"Failed to get frame pointer shape in DUPLICATIONMANAGER", L"Error", hr);
        }
        delete [] PtrInfo->PtrShapeBuffer;
        PtrInfo->PtrShapeBuffer = NULL;
        PtrInfo->BufferSize = 0;
        return hr;
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="af420-172">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="af420-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af420-173">Mejoras en DXGI 1,2</span><span class="sxs-lookup"><span data-stu-id="af420-173">DXGI 1.2 Improvements</span></span>](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
