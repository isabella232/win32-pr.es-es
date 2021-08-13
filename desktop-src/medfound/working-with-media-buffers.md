---
description: Trabajar con búferes multimedia
ms.assetid: c7e079e0-99f3-4bff-9163-1c5a022c14ae
title: Trabajar con búferes multimedia (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c559e54d38c5a601a51bf3d6a879cbfe5b8403e1df48117e15d23f6264554437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736616"
---
# <a name="working-with-media-buffers-microsoft-media-foundation"></a>Trabajar con búferes multimedia (Microsoft Media Foundation)

En este tema se describe cómo usar la interfaz [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) para tener acceso a los datos de un búfer multimedia. Todos los búferes multimedia exponen **EL BÚFER DEMEDIAMEDIA,** que está diseñado para cualquier tipo de datos. Los fotogramas de vídeo sin comprimir son un caso especial, que se describe en el tema [Búferes de vídeo sin comprimir.](uncompressed-video-buffers.md)

## <a name="buffer-size"></a>Tamaño del búfer

Un búfer multimedia tiene dos tamaños asociados:

-   La *longitud máxima* es el tamaño físico de la memoria que se asigna para el búfer. Este valor se establece cuando se crea el búfer y no cambia durante la vigencia del búfer. La longitud máxima indica cuántos datos se pueden almacenar en el búfer. Para buscar el tamaño máximo, llame [**a IMFMediaBuffer::GetMaxLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength).

-   La *longitud actual* es la cantidad de datos válidos que se encuentran actualmente en el búfer. Cuando se asigna por primera vez el búfer, la longitud actual es cero, porque no hay datos válidos en el búfer. Si escribe datos en el búfer, debe actualizar la longitud actual mediante una llamada a [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength). Por ejemplo, si escribe 100 bytes de datos en el búfer, llame a **SetCurrentLength** con el valor 100. Si lee datos de un búfer de medios, llame a [**LAMEDIABUFFER::GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) para averiguar cuántos datos hay actualmente en el búfer. No lea más allá de la longitud actual. La longitud actual nunca puede superar la longitud máxima del búfer.

## <a name="accessing-the-buffer-memory"></a>Acceso a la memoria del búfer

Para acceder a la memoria en el búfer, llame [**a IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). Este método devuelve un puntero al inicio del bloque de memoria. También devuelve la longitud máxima y la longitud actual. Cuando haya terminado de usar el puntero, llame [**a IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).

Para escribir datos en un búfer multimedia:

1.  Llame [**a IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para obtener un puntero a la memoria. El método también devuelve la longitud máxima del búfer.
2.  Escriba los datos en la memoria, hasta la longitud máxima del búfer.
3.  Llame [**aBUFFERMediaBuffer::SetCurrentLength para**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) actualizar la longitud actual. Establezca la longitud actual igual a la cantidad de datos que escribió en el paso 2.
4.  Llame [**a IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) para desbloquear el búfer.

Para leer datos de un búfer multimedia:

1.  Llame [**a IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para obtener un puntero a la memoria. El método también devuelve la longitud actual del búfer (la cantidad de datos válidos en el búfer).
2.  Lea el contenido de la memoria, hasta la longitud actual.
3.  Llame [**a IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) para desbloquear el búfer.

## <a name="creating-system-memory-buffers"></a>Crear búferes de memoria del sistema

El búfer de memoria del sistema es un búfer multimedia que administra un bloque de memoria del sistema. Para crear una instancia de este objeto, llame a [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) o [**MFCreateAlignedMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer) y especifique un tamaño de búfer. Ambas funciones asignan un bloque de memoria y devuelven un [**puntero DE LUGARMediaBuffer.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) La memoria se libera automáticamente cuando el recuento de referencias del búfer multimedia alcanza cero y se destruye el objeto.

En el ejemplo siguiente se muestra cómo crear un búfer de memoria del sistema y escribir en el búfer.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes multimedia](media-buffers.md)
</dt> <dt>

[Media Foundation API de plataforma de aplicaciones](media-foundation-platform-apis.md)
</dt> </dl>

 

 



