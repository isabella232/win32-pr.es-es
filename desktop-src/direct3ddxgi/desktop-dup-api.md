---
description: Windows 8 deshabilita los controladores reflejados Windows modelo de controlador de pantalla (XDDM) estándar y ofrece la API de duplicación de escritorio en su lugar.
ms.assetid: 523FBFAD-5D78-4EE3-A3B7-8FD5BA39DC46
title: API de duplicación de escritorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c1960d064d7fd1e34748dcc2efb3c86459b498df91b52c1384ef8698a37c01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518501"
---
# <a name="desktop-duplication-api"></a>API de duplicación de escritorio

Windows 8 deshabilita los controladores reflejados Windows modelo de controlador de pantalla (XDDM) estándar y ofrece la API de duplicación de escritorio en su lugar. La API de duplicación de escritorio proporciona acceso remoto a una imagen de escritorio para escenarios de colaboración. Las aplicaciones pueden usar la API de duplicación de escritorio para acceder a las actualizaciones fotograma a fotograma en el escritorio. Dado que las aplicaciones reciben actualizaciones de la imagen de escritorio en una superficie DXGI, las aplicaciones pueden usar toda la potencia de la GPU para procesar las actualizaciones de la imagen.

-   [Actualización de los datos de la imagen de escritorio](#updating-the-desktop-image-data)
-   [Rotación de la imagen de escritorio](#rotating-the-desktop-image)
-   [Actualización del puntero de escritorio](#updating-the-desktop-pointer)
-   [Temas relacionados](#related-topics)

## <a name="updating-the-desktop-image-data"></a>Actualización de los datos de la imagen de escritorio

DXGI proporciona una superficie que contiene una imagen de escritorio actual a través del nuevo [**método IDXGIOutputDuplication::AcquireNextFrame.**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) El formato de la imagen de escritorio siempre es [**DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) independientemente del modo de presentación actual. Junto con esta superficie, estos métodos [**IDXGIOutputDuplication**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) devuelven los tipos de información indicados que le ayudan a determinar qué píxeles de la superficie necesita procesar:

-   [**IDXGIOutputDuplication::GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) devuelve regiones desfasadas, que son rectángulos no superpuestos que indican las áreas de la imagen de escritorio que el sistema operativo actualizó desde que procesó la imagen de escritorio anterior.
-   [**IDXGIOutputDuplication::GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) devuelve regiones de movimiento, que son rectángulos de píxeles en la imagen de escritorio que el sistema operativo movió a otra ubicación dentro de la misma imagen. Cada región de movimiento consta de un rectángulo de destino y un punto de origen. El punto de origen especifica la ubicación desde la que el sistema operativo copió la región y el rectángulo de destino especifica dónde se movió el sistema operativo esa región. Las regiones de movimiento siempre son regiones no elásticas, por lo que el origen siempre tiene el mismo tamaño que el destino.

Supongamos que la imagen de escritorio se transmitió a través de una conexión lenta a la aplicación cliente remota. La cantidad de datos que se envían a través de la conexión se reduce al recibir solo datos sobre cómo la aplicación cliente debe mover regiones de píxeles en lugar de datos de píxeles reales. Para procesar los movimientos, la aplicación cliente debe haber almacenado la última imagen completa.

Aunque el sistema operativo acumula actualizaciones de imágenes de escritorio sin procesar, puede que se queme espacio para almacenar con precisión las regiones de actualización. En esta situación, el sistema operativo comienza a acumular las actualizaciones mediante la conjunción de ellas con las regiones de actualización existentes para cubrir todas las actualizaciones nuevas. Como resultado, el sistema operativo cubre píxeles que aún no se han actualizado en ese marco. Pero esta situación no genera problemas visuales en la aplicación cliente porque recibe toda la imagen de escritorio y no solo los píxeles actualizados.

Para reconstruir la imagen de escritorio correcta, la aplicación cliente debe procesar primero todas las regiones de movimiento y, a continuación, procesar todas las regiones desapreociadas. Cualquiera de estas listas de regiones desnuciados y de movimiento puede estar completamente vacía. El código de ejemplo del [ejemplo de duplicación de](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) escritorio muestra cómo procesar las regiones desduplicadas y de movimiento en un solo fotograma:


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



## <a name="rotating-the-desktop-image"></a>Rotación de la imagen de escritorio

Debe agregar código explícito a la aplicación cliente de duplicación de escritorio para admitir los modos girados. En un modo girado, la superficie que recibe de [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) siempre está en la orientación sin girar y la imagen de escritorio gira dentro de la superficie. Por ejemplo, si el escritorio está establecido en 768 x 1024 a 90 grados de rotación, **AcquireNextFrame** devuelve una superficie de 1024 x 768 con la imagen de escritorio girada dentro de ella. Estos son algunos ejemplos de rotación.



| Modo de visualización establecido desde el panel de control de pantalla | Modo de presentación devuelto por GDI o DXGI | Surface devuelta desde [ **AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)                |
|---------------------------------------------|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| Horizontal de 1024 x 768                          | Rotación de 0 grados de 1024 x 768           | Nueva línea 1024x768 \[\] ![Escritorio remoto no arrobado](images/dxgi-outdupl-0-rotate.png)<br/>            |
| Vertical de 1024 x 768                           | Rotación de 90 grados de 768x1024          | Nueva línea 1024x768 \[\] ![Escritorio remoto girado a 90 grados](images/dxgi-outdupl-90-rotate.png)<br/>   |
| Horizontal de 1024 x 768 (volteado)                | Rotación de 180 grados de 1024 x 768         | Nueva línea 1024x768 \[\] ![Escritorio remoto girado a 180 grados](images/dxgi-outdupl-180-rotate.png)<br/> |
| Vertical de 1024 x 768 (volteado)                 | Rotación de 768x1024 270 grados         | Nueva línea 1024x768 \[\] ![Escritorio remoto girado a 270 grados](images/dxgi-outdupl-270-rotate.png)<br/> |



 

El código de la aplicación cliente de duplicación de escritorio debe rotar la imagen de escritorio correctamente antes de mostrar la imagen de escritorio.

> [!Note]  
> En escenarios de varios monitores, puede rotar la imagen de escritorio de cada monitor de forma independiente.

 

## <a name="updating-the-desktop-pointer"></a>Actualización del puntero de escritorio

Debe usar la API de duplicación de escritorio para determinar si la aplicación cliente debe dibujar la forma del puntero del mouse en la imagen de escritorio. El puntero del mouse ya está dibujado en la imagen de escritorio que [**proporciona IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) o el puntero del mouse es independiente de la imagen de escritorio. Si el puntero del mouse se dibuja en la imagen de escritorio, los datos de posición del puntero notificados por **AcquireNextFrame** (en el miembro **PointerPosition** de [**DXGI \_ OUTDUPL \_ FRAME \_ INFO**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) al que apunta el parámetro *pFrameInfo)* indican que un puntero independiente no está visible. Si el adaptador de gráficos superpone el puntero del mouse en la parte superior de la imagen de escritorio, **AcquireNextFrame** informa de que hay un puntero independiente visible. Por lo tanto, la aplicación cliente debe dibujar la forma del puntero del mouse en la imagen de escritorio para representar con precisión lo que el usuario actual verá en su monitor.

Para dibujar el puntero del mouse del escritorio, use el miembro **PointerPosition** de [**DXGI \_ OUTDUPL \_ FRAME \_ INFO**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) desde el *parámetro pFrameInfo* [**de AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) para determinar dónde buscar la esquina superior izquierda del puntero del mouse en la imagen de escritorio. Al dibujar el primer fotograma, debe usar el método [**IDXGIOutputDuplication::GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) para obtener información sobre la forma del puntero del mouse. Cada llamada a **AcquireNextFrame para** obtener el marco siguiente también proporciona la posición del puntero actual para ese marco. Por otro lado, solo debe usar **GetFramePointerShape** si cambia la forma. Por lo tanto, mantenga una copia de la última imagen de puntero y úsela para dibujarla en el escritorio a menos que cambie la forma del puntero del mouse.

> [!Note]  
> Junto con la imagen de forma de puntero, [**GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) proporciona el tamaño de la ubicación del punto de acceso rápido. El punto de acceso se proporciona solo con fines informativos. La ubicación en la que se va a dibujar la imagen de puntero es independiente de la zona activa.

 

Este código de ejemplo del ejemplo [de duplicación de escritorio](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) muestra cómo obtener la forma del puntero del mouse:


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

[Mejoras de DXGI 1.2](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
