---
title: Negociación de formato de vídeo en el complemento DSP de vídeo de ejemplo
description: Negociación de formato de vídeo en el complemento DSP de vídeo de ejemplo
ms.assetid: 3e92ce10-2b9b-4689-a181-f56c33472fea
keywords:
- Reproductor de Windows Media complementos, DSP de vídeo
- complementos, DSP de vídeo
- complementos de procesamiento de señal digital, negociación de formato de vídeo
- Complementos DE DSP, negociación de formato de vídeo
- complementos de DSP de vídeo, negociación de formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c287a38fbfcf11f1b9d74087a91c5825b22f1243
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070824"
---
# <a name="video-format-negotiation-in-the-sample-video-dsp-plug-in"></a>Negociación de formato de vídeo en el complemento DSP de vídeo de ejemplo

Antes Reproductor de Windows Media insertar un complemento DSP de vídeo en la cadena de señales, el reproductor debe determinar si el complemento puede procesar el vídeo que se reproduce. El proceso por el que el complemento y el reproductor se comunican sobre los formatos de vídeo admitidos se denomina negociación de formato.

## <a name="providing-the-supported-input-and-output-types"></a>Proporcionar los tipos de entrada y salida admitidos

Si el complemento DSP actúa como un objeto multimedia DirectX (DMO), el reproductor consulta al complemento sobre sus formatos admitidos mediante una secuencia de llamadas a **IMediaObject::GetInputType** e **IMediaObject::GetOutputType**.

Si el complemento DSP actúa como una transformación de Media Foundation (MFT), el reproductor consulta al complemento sobre sus formatos admitidos mediante una secuencia de llamadas a **IMFTransform::GetInputAvailableType** y **ADETransform::GetOutputAvailableType.**

El complemento de vídeo de ejemplo generado por el Asistente para complementos de Reproductor de Windows Media almacena la lista de formatos de vídeo admitidos como una matriz de GUID. El código siguiente es del archivo .cpp principal:


```C++
static const GUID*    k_guidValidSubtypes[] = {
    &MEDIASUBTYPE_NV12,
    &MEDIASUBTYPE_YV12,
    &MEDIASUBTYPE_YUY2,
    &MEDIASUBTYPE_UYVY,
    &MEDIASUBTYPE_RGB32,
    &MEDIASUBTYPE_RGB24,
    &MEDIASUBTYPE RGB555,
    &MEDIASUBTYPE RGB565
};

```



El reproductor puede llamar **a IMediaObject::GetInputType** e **IMediaObject::GetOutputType** en cualquier orden, por lo que el código del complemento debe preverlo. De forma similar, el reproductor puede llamar **a IMFTransform::GetInputAvailableType** y **a IMFTransform::GetOutputAvailableType** en cualquier orden. Las implementaciones de ejemplo **de GetOutputType** y **GetOutputAvailableType** prueban si el tipo de entrada ya se ha definido. Si lo tiene, el complemento responde que solo admite ese tipo. De lo contrario, el complemento devuelve el tipo que corresponde al índice proporcionado, como se muestra en el código siguiente:


```C++
// If input type has been defined, then use that as output type.
if (GUID_NULL != m_mtInput.majortype)
{
    hr = ::MoCopyMediaType( pmt, &m_mtInput );
}
else // Otherwise use default for this plug-in.
{
    ::ZeroMemory( pmt, sizeof( DMO_MEDIA_TYPE ) );
    pmt->majortype = MEDIATYPE_Video;
    pmt->subtype = *k_guidValidSubtypes[dwTypeIndex];     
}

```



## <a name="setting-the-input-and-output-types"></a>Establecimiento de los tipos de entrada y salida

Si el complemento DSP actúa como un DMO, Reproductor de Windows Media establece el tipo de medio mediante una llamada a **IMediaObject::SetInputType** e **IMediaObject::SetOutputType**, pasando a cada función un puntero a una estructura **media \_ \_ TYPE** de DMO que representa el tipo de medio solicitado.

Si el complemento DSP actúa como MFT, Reproductor de Windows Media establece el tipo de medio mediante una llamada a **IMFTransform::SetInputType** y **ASETRANSFORMTransform::SetOutputType,** pasando a cada función un puntero a una interfaz **IMFMediaType que** representa el tipo de medio solicitado.

No hay ninguna garantía de que el reproductor llame a métodos de negociación de formato en un orden determinado, por lo que el código del complemento debe controlar cualquier caso. Por ejemplo, si el reproductor llama a **SetOutputType** antes de llamar a **SetInputType,** es un curso de acción válido para que el complemento rechace el tipo de medio de salida propuesto. El código siguiente de la implementación de ejemplo **de IMediaObject::SetOutputType** muestra esto:


```C++
if( GUID_NULL != m_mtInput.majortype )
{
    // Validate that the output media type matches our requirements 
    // and matches our input type (if set).
    hr = ValidateMediaType(pmt, &m_mtInput);
}
else
{
    hr = DMO_E_TYPE_NOT_ACCEPTED;
}

```



Las implementaciones de complemento de ejemplo **de SetInputType** y **SetOutputType** llaman a la función personalizada **denominada ValidateMediaType**. Esta función de complemento realiza una serie de pruebas en el tipo de medio propuesto diseñado para garantizar que el tipo de medio esté bien formado y sea compatible con el complemento. **ValidateMediaType** realiza las siguientes pruebas:

-   Comprueba que los **miembros majortype** y **formattype** contienen los valores correctos.
-   Comprueba que el **miembro de subtipo** coincide con uno de los formatos admitidos.
-   Comprueba que la información de las estructuras **BITMAPINFOHEADER** y **VIDEOINFOHEADER** o **VIDEOINFOHEADER2** contiene valores válidos.
-   Comprueba si los tipos de medios de entrada y salida coinciden porque el complemento no convierte formatos de entrada a salida.

Si el tipo de medio propuesto supera las pruebas de validación, se almacena en una variable miembro: **m \_ mtInput** para el tipo de medio de entrada, **m \_ mtOutput** para el tipo de medio de salida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de un complemento DSP de vídeo**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 




