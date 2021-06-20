---
description: Use este ejemplo para comprender cómo el codificador RLE podría implementar el método como parte de la escritura de un filtro de transformación.
ms.assetid: b7d878ab-523f-4b52-b98d-c9d4fa18ce8a
title: Paso 5. Transformación de la imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac9d32e48ba438f8bde2d8d4d9aca3b827ebc0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406788"
---
# <a name="step-5-transform-the-image"></a>Paso 5. Transformación de la imagen

Este es el paso 5 del tutorial Escribir [filtros de transformación](writing-transform-filters.md).

El filtro ascendente entrega ejemplos multimedia al filtro de transformación mediante una llamada al método [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) en el pin de entrada del filtro de transformación. Para procesar los datos, el filtro de transformación llama al **método Transform,** que es virtual puro. Las **clases CTransformFilter** y **CTransInPlaceFilter** usan dos versiones diferentes de este método:

-   [**CTransformFilter::Transform**](ctransformfilter-transform.md) toma un puntero al ejemplo de entrada y un puntero al ejemplo de salida. Antes de que el filtro llame al método , copia las propiedades de ejemplo del ejemplo de entrada en el ejemplo de salida, incluidas las marcas de tiempo.
-   [**CTransInPlaceFilter::Transform**](ctransinplacefilter-transform.md) toma un puntero al ejemplo de entrada. El filtro modifica los datos en su lugar.

Si el **método Transform** devuelve S \_ OK, el filtro entrega el ejemplo de nivel inferior. Para omitir un marco, devuelva S \_ FALSE. Si se produce un error de streaming, devuelva un código de error.

En el ejemplo siguiente se muestra cómo el codificador RLE podría implementar este método. Su propia implementación puede diferir considerablemente, en función de lo que haga el filtro.


```C++
HRESULT CRleFilter::Transform(IMediaSample *pSource, IMediaSample *pDest)
{
    // Get pointers to the underlying buffers.
    BYTE *pBufferIn, *pBufferOut;
    hr = pSource->GetPointer(&pBufferIn);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pDest->GetPointer(&pBufferOut);
    if (FAILED(hr))
    {
        return hr;
    }
    // Process the data.
    DWORD cbDest = EncodeFrame(pBufferIn, pBufferOut);
    KASSERT((long)cbDest <= pDest->GetSize());

    pDest->SetActualDataLength(cbDest);
    pDest->SetSyncPoint(TRUE);
    return S_OK;
}
```



En este ejemplo se supone que EncodeFrame es un método privado que implementa la codificación RLE. El propio algoritmo de codificación no se describe aquí; Para obtener más información, consulte el tema "Bitmap Compression" (Compresión de mapa de bits) en la documentación de Platform SDK.

En primer lugar, el ejemplo llama [**a IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) para recuperar las direcciones de los búferes subyacentes. Los pasa al método EncoderFrame privado. A continuación, [**llama a IMediaSample::SetActualDataLength para**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) especificar la longitud de los datos codificados. El filtro de nivel inferior necesita esta información para poder administrar el búfer correctamente. Por último, el método llama [**a IMediaSample::SetSyncPoint para**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) establecer la marca de fotograma clave en **TRUE.** La codificación de longitud de ejecución no usa ningún fotograma delta, por lo que cada fotograma es un fotograma clave. En el caso de los marcos delta, establezca el valor en **FALSE.**

Otros problemas que debe tener en cuenta son:

-   Marcas de tiempo. La **clase CTransformFilter marca** de tiempo el ejemplo de salida antes de llamar al método **Transform.** Copia los valores de marca de tiempo del ejemplo de entrada, sin modificarlos. Si el filtro necesita cambiar las marcas de tiempo, llame a [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) en el ejemplo de salida.
-   Cambios de formato. El filtro ascendente puede cambiar los formatos de la secuencia media adjuntando un tipo de medio al ejemplo. Antes de hacerlo, llama a [**IPin::QueryAccept en**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) el pin de entrada del filtro. En la **clase CTransformFilter,** esto da como resultado una llamada a **CheckInputType** seguida de **CheckTransform**. El filtro de nivel inferior también puede cambiar los tipos de medios con el mismo mecanismo. En su propio filtro, hay dos cosas que debe tener en cuenta:

    -   Asegúrese de que **QueryAccept** no devuelve aceptaciones falsas.
    -   Si el filtro acepta cambios de formato, comprórrelos dentro del **método Transform** llamando a [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype). Si ese método devuelve S \_ OK, el filtro debe responder al cambio de formato.

    Para obtener más información, vea [Cambios de formato dinámico.](dynamic-format-changes.md)

-   Subprocesos. En **CTransformFilter y** **CTransInPlaceFilter,** el filtro de transformación entrega muestras de salida sincrónicamente dentro del **método Receive.** El filtro no crea ningún subproceso de trabajo para procesar los datos. Normalmente, no hay ninguna razón para que un filtro de transformación cree subprocesos de trabajo.

Siguiente: [Paso 6. Agregue compatibilidad con COM.](step-6--add-support-for-com.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



