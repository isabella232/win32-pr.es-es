---
description: Paso 5.
ms.assetid: b7d878ab-523f-4b52-b98d-c9d4fa18ce8a
title: Paso 5. Transformar la imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609acb626d00dbceea8b6f5bca6af012d8158b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278286"
---
# <a name="step-5-transform-the-image"></a>Paso 5. Transformar la imagen

Este es el paso 5 del tutorial de [escritura de filtros de transformación](writing-transform-filters.md).

El filtro de nivel superior proporciona muestras de medios al filtro de transformación mediante una llamada al método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) en el PIN de entrada del filtro de transformación. Para procesar los datos, el filtro de transformación llama al método de **transformación** , que es virtual puro. Las clases **CTransformFilter** y **CTransInPlaceFilter** usan dos versiones diferentes de este método:

-   [**CTransformFilter:: transform**](ctransformfilter-transform.md) toma un puntero al ejemplo de entrada y un puntero al ejemplo de salida. Antes de que el filtro llame al método, copia las propiedades de ejemplo del ejemplo de entrada en el ejemplo de salida, incluidas las marcas de tiempo.
-   [**CTransInPlaceFilter:: transform**](ctransinplacefilter-transform.md) toma un puntero al ejemplo de entrada. El filtro modifica los datos en su lugar.

Si el método **Transform** devuelve S \_ OK, el filtro entrega el ejemplo de nivel inferior. Para omitir un marco, devuelve S \_ false. Si se produce un error de streaming, devuelva un código de error.

En el ejemplo siguiente se muestra cómo el codificador RLE podría implementar este método. Su propia implementación podría diferir considerablemente en función de lo que hace el filtro.


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



En este ejemplo se da por supuesto que EncodeFrame es un método privado que implementa la codificación RLE. El algoritmo de codificación en sí no se describe aquí. para obtener más información, vea el tema "compresión de mapa de bits" en la documentación de Platform SDK.

En primer lugar, el ejemplo llama a [**IMediaSample:: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) para recuperar las direcciones de los búferes subyacentes. Los pasa al método privado EncoderFrame. A continuación, llama a [**IMediaSample:: SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) para especificar la longitud de los datos codificados. El filtro de nivel inferior necesita esta información para que pueda administrar el búfer correctamente. Por último, el método llama a [**IMediaSample:: SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) para establecer la marca de fotograma clave en **true**. La codificación de longitud de ejecución no usa ningún fotograma Delta, por lo que cada fotograma es un fotograma clave. En el caso de los fotogramas Delta, establezca el valor en **false**.

Otros problemas que debe tener en cuenta son:

-   Marcas de tiempo. La clase **CTransformFilter** marca las marcas de tiempo en el ejemplo de salida antes de llamar al método **Transform** . Copia los valores de la marca de tiempo de la muestra de entrada, sin modificarlos. Si el filtro debe cambiar las marcas de tiempo, llame a [**IMediaSample:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) en el ejemplo de salida.
-   Cambios de formato. El filtro de nivel superior puede cambiar el formato de la secuencia intermedia adjuntando un tipo de medio al ejemplo. Antes de hacerlo, llama a [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) en el PIN de entrada del filtro. En la clase **CTransformFilter** , esto da como resultado una llamada a **CheckInputType** seguida de **CheckTransform**. El filtro de nivel inferior también puede cambiar los tipos de medios mediante el mismo mecanismo. En su propio filtro, hay dos aspectos que se deben tener en cuenta:

    -   Asegúrese de que **QueryAccept** no devuelva la aceptación falsa.
    -   Si el filtro acepta cambios de formato, compruébelos en el método de **transformación** mediante una llamada a [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype). Si el método devuelve S \_ correcto, el filtro debe responder al cambio de formato.

    Para obtener más información, consulte [Dynamic Format Changes](dynamic-format-changes.md).

-   Subprocesos. En **CTransformFilter** y **CTransInPlaceFilter**, el filtro de transformación entrega los ejemplos de salida sincrónicamente dentro del método **Receive** . El filtro no crea ningún subproceso de trabajo para procesar los datos. Normalmente, no hay ningún motivo para que un filtro de transformación cree subprocesos de trabajo.

Siguiente: [paso 6. Agregar compatibilidad para COM](step-6--add-support-for-com.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



