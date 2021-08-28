---
description: Usar el solucionador de origen
ms.assetid: 94e2a411-96b8-4506-8491-78f4f5f286ce
title: Usar el solucionador de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81265f2edeb573ccdfb2b4ea8f2664d08f9bca8a2170459c9c53890ecd3b52cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887154"
---
# <a name="using-the-source-resolver"></a>Usar el solucionador de origen

La resolución del origen usa una URL o una secuencia de bytes y crea el origen multimedia adecuado para el contenido en cuestión. Para crear la resolución de origen, llame [**a MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver). Esta función devuelve un puntero [**de interfaz IMFSourceResolver.**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)

La resolución de origen tiene métodos sincrónicos y asincrónicos. Si usa la resolución de origen del subproceso de aplicación principal, los métodos asincrónicos harán que la interfaz de usuario tenga más capacidad de respuesta. Los métodos sincrónicos pueden bloquearse durante un período de tiempo perceptible, especialmente si el solucionador de origen debe abrir un recurso de red.

Los métodos sincrónicos son:

-   [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)
-   [**IMFSourceResolver::CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream)

Los métodos asincrónicos son:

-   [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)
-   [**IMFSourceResolver::BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream)

Para los métodos asincrónicos, cada método tiene un método **End...** correspondiente para completar la solicitud asincrónica y un método **Cancel...** para cancelar una solicitud pendiente. Para obtener más información sobre los métodos asincrónicos Media Foundation, vea [Métodos de devolución de llamada asincrónicos.](asynchronous-callback-methods.md)

En el ejemplo de código siguiente se crea un origen multimedia a partir de una dirección URL. En este ejemplo se usa el método sincrónico .


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solucionador de origen](source-resolver.md)
</dt> </dl>

 

 



