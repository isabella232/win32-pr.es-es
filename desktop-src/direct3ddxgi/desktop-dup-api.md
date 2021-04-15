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
# <a name="desktop-duplication-api"></a>API de duplicación de escritorio

Windows 8 deshabilita los controladores de reflejo estándar del modelo de controladores de pantalla de Windows 2000 (XDDM) y ofrece en su lugar la API de duplicado de escritorio. La API de duplicación de escritorio proporciona acceso remoto a una imagen de escritorio para escenarios de colaboración. Las aplicaciones pueden usar la API de duplicación de escritorio para tener acceso a las actualizaciones de fotogramas fotogramas en el escritorio. Dado que las aplicaciones reciben actualizaciones de la imagen de escritorio en una superficie de DXGI, las aplicaciones pueden usar toda la capacidad de la GPU para procesar las actualizaciones de la imagen.

-   [Actualización de los datos de imagen de escritorio](#updating-the-desktop-image-data)
-   [Girar la imagen de escritorio](#rotating-the-desktop-image)
-   [Actualizar el puntero de escritorio](#updating-the-desktop-pointer)
-   [Temas relacionados](#related-topics)

## <a name="updating-the-desktop-image-data"></a>Actualización de los datos de imagen de escritorio

DXGI proporciona una superficie que contiene una imagen de escritorio actual a través del nuevo método [**IDXGIOutputDuplication:: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) . El formato de la imagen de escritorio siempre es el [**formato de DXGI \_ \_ B8G8R8A8 \_ UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) , independientemente del modo de presentación actual. Junto con esta superficie, estos métodos [**IDXGIOutputDuplication**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) devuelven los tipos de información indicados que le ayudarán a determinar qué píxeles de la superficie debe procesar:

-   [**IDXGIOutputDuplication:: GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) devuelve regiones desfasadas, que son rectángulos no superpuestos que indican las áreas de la imagen de escritorio que el sistema operativo ha actualizado desde que se procesó la imagen de escritorio anterior.
-   [**IDXGIOutputDuplication:: GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) devuelve regiones de movimiento, que son rectángulos de píxeles de la imagen de escritorio que el sistema operativo ha movido a otra ubicación dentro de la misma imagen. Cada región de movimiento consta de un rectángulo de destino y un punto de origen. El punto de origen especifica la ubicación desde la que el sistema operativo ha copiado la región y el rectángulo de destino especifica el lugar en el que el sistema operativo ha despasado esa región. Las regiones de movimiento siempre son regiones no estiradas, por lo que el origen siempre tiene el mismo tamaño que el destino.

Supongamos que la imagen de escritorio se ha transmitido a través de una conexión lenta a la aplicación cliente remota. La cantidad de datos que se envían a través de la conexión se reduce recibiendo solo datos sobre cómo la aplicación cliente debe trasladar regiones de píxeles en lugar de datos de píxeles reales. Para procesar los movimientos, la aplicación cliente debe haber almacenado la última imagen completa.

Aunque el sistema operativo acumula actualizaciones de imágenes de escritorio no procesadas, podría quedarse sin espacio para almacenar de forma precisa las regiones de actualización. En esta situación, el sistema operativo comienza a acumular las actualizaciones mediante la combinación de las regiones de actualización existentes para cubrir todas las actualizaciones nuevas. Como resultado, el sistema operativo cubre los píxeles que todavía no se han actualizado en ese marco. Sin embargo, esta situación no genera problemas visuales en la aplicación cliente porque recibe la imagen de escritorio completa y no solo los píxeles actualizados.

Para reconstruir la imagen de escritorio correcta, la aplicación cliente debe procesar primero todas las regiones de movimiento y, a continuación, procesar todas las regiones desfasadas. Cualquiera de estas listas de regiones desfasadas y de movimiento puede estar completamente vacía. El código de ejemplo del [ejemplo de duplicación de escritorio](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) muestra cómo procesar las regiones desfasadas y de movimiento en un solo fotograma:


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



## <a name="rotating-the-desktop-image"></a>Girar la imagen de escritorio

Debe agregar código explícito a la aplicación cliente de duplicación de escritorio para admitir modos girados. En un modo girado, la superficie que recibe de [**IDXGIOutputDuplication:: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) siempre está en la orientación no girada y la imagen del escritorio se gira dentro de la superficie. Por ejemplo, si el escritorio se establece en 768x1024 con una rotación de 90 grados, **AcquireNextFrame** devuelve una superficie de 1024x768 con la imagen de escritorio girada dentro de ella. Estos son algunos ejemplos de rotación.



| Modo de presentación establecido en Mostrar panel de control | Modo de presentación devuelto por GDI o DXGI | Superficie devuelta por [ **AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)                |
|---------------------------------------------|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| vertical 1024x768                          | rotación de 0 grados 1024x768           | \[nueva línea 1024x768\] ![escritorio remoto no girado](images/dxgi-outdupl-0-rotate.png)<br/>            |
| 1024x768 vertical                           | rotación de 768x1024 90 grados          | \[nueva línea 1024x768\] ![escritorio remoto girado 90 grados](images/dxgi-outdupl-90-rotate.png)<br/>   |
| 1024x768 horizontalmente (volteado)                | rotación de grado de 1024x768 180         | \[nueva línea 1024x768\] ![escritorio remoto girado 180 grados](images/dxgi-outdupl-180-rotate.png)<br/> |
| 1024x768 vertical (volteado)                 | rotación de 768x1024 270 grados         | \[nueva línea 1024x768\] ![escritorio remoto girado 270 grados](images/dxgi-outdupl-270-rotate.png)<br/> |



 

El código de la aplicación cliente de duplicación de escritorio debe girar la imagen de escritorio correctamente antes de mostrar la imagen de escritorio.

> [!Note]  
> En escenarios de varios monitores, puede girar la imagen de escritorio de cada monitor de manera independiente.

 

## <a name="updating-the-desktop-pointer"></a>Actualizar el puntero de escritorio

Debe usar la API de duplicación de escritorio para determinar si la aplicación cliente debe dibujar la forma del puntero del mouse en la imagen del escritorio. Ya se ha dibujado el puntero del mouse en la imagen de escritorio que [**IDXGIOutputDuplication:: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) proporciona o el puntero del mouse es independiente de la imagen del escritorio. Si el puntero del mouse se dibuja en la imagen del escritorio, los datos de la posición del puntero informados por **AcquireNextFrame** (en el miembro **PointerPosition** de la  [**\_ \_ \_ información de fotogramas de DXGI OUTDUPL**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) al que apunta el parámetro pFrameInfo) indican que un puntero independiente no está visible. Si el adaptador de gráficos superpone el puntero del mouse encima de la imagen del escritorio, **AcquireNextFrame** informa de que hay un puntero independiente visible. Por lo tanto, la aplicación cliente debe dibujar la forma puntero del mouse en la imagen de escritorio para representar con precisión lo que el usuario actual verá en su monitor.

Para dibujar el puntero del mouse del escritorio, use el miembro **PointerPosition** de la [**\_ \_ \_ información de fotogramas de DXGI OUTDUPL**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) del parámetro *pFrameInfo* de [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) para determinar dónde ubicar la esquina superior izquierda del puntero del mouse en la imagen de escritorio. Al dibujar el primer fotograma, debe usar el método [**IDXGIOutputDuplication:: GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) para obtener información sobre la forma del puntero del mouse. Cada llamada a **AcquireNextFrame** para obtener el fotograma siguiente también proporciona la posición actual del puntero para ese marco. Por otro lado, debe volver a usar **GetFramePointerShape** solo si la forma cambia. Por lo tanto, mantenga una copia de la última imagen de puntero y Úsela para dibujar en el escritorio a menos que cambie la forma del puntero del mouse.

> [!Note]  
> Junto con la imagen de la forma de puntero, [**GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) proporciona el tamaño de la ubicación de la zona activa. La zona activa solo se proporciona con fines informativos. La ubicación donde se dibuja la imagen del puntero es independiente de la zona activa.

 

Este código de ejemplo del [ejemplo de duplicación del escritorio](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) muestra cómo obtener la forma del puntero del mouse:


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejoras en DXGI 1,2](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
