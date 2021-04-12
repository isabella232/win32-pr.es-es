---
title: Negociación del formato de vídeo en el complemento DSP de vídeo de ejemplo
description: Negociación del formato de vídeo en el complemento DSP de vídeo de ejemplo
ms.assetid: 3e92ce10-2b9b-4689-a181-f56c33472fea
keywords:
- Complementos de Windows Media Player, DSP de vídeo
- complementos, DSP de vídeo
- Complementos de procesamiento de señal digital, negociación de formato de vídeo
- Complementos DSP, negociación de formato de vídeo
- Complementos de DSP de vídeo, negociación de formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c287a38fbfcf11f1b9d74087a91c5825b22f1243
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357165"
---
# <a name="video-format-negotiation-in-the-sample-video-dsp-plug-in"></a>Negociación del formato de vídeo en el complemento DSP de vídeo de ejemplo

Antes de que Windows Media Player Inserte un complemento de DSP de vídeo en la cadena de señales, el reproductor debe determinar si el complemento puede procesar el vídeo que se está reproduciendo. El proceso por el que el complemento y el reproductor se comunican sobre los formatos de vídeo admitidos se denomina negociación de formato.

## <a name="providing-the-supported-input-and-output-types"></a>Proporcionar los tipos de entrada y salida admitidos

Si el complemento de DSP está actuando como un objeto multimedia de DirectX (DMO), el reproductor consulta el complemento sobre los formatos admitidos mediante la realización de una secuencia de llamadas a **IMediaObject:: GetInputType** y **IMediaObject:: GetOutputType**.

Si el complemento de DSP actúa como una transformación de Media Foundation (MFT), el reproductor consulta el complemento sobre los formatos admitidos realizando una secuencia de llamadas a **IMFTransform:: GetInputAvailableType** y **IMFTransform:: GetOutputAvailableType**.

El complemento de vídeo de ejemplo generado por el Asistente para complementos de Windows Media Player almacena la lista de formatos de vídeo compatibles como una matriz de GUID. El código siguiente procede del archivo main. cpp:


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



El reproductor puede llamar a **IMediaObject:: GetInputType** y **IMediaObject:: GetOutputType** en cualquier orden, por lo que el código del complemento debe anticiparse. De igual forma, el reproductor puede llamar a **IMFTransform:: GetInputAvailableType** y **IMFTransform:: GetOutputAvailableType** en cualquier orden. Las implementaciones de ejemplo de **GetOutputType** y **GetOutputAvailableType** prueban si el tipo de entrada ya se ha definido. Si es así, el complemento responde que solo admite ese tipo. De lo contrario, el complemento devuelve el tipo que corresponde al índice proporcionado, como se muestra en el código siguiente:


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



## <a name="setting-the-input-and-output-types"></a>Establecer los tipos de entrada y salida

Si el complemento DSP actúa como DMO, Windows Media Player establece el tipo de medio mediante una llamada a **IMediaObject:: SetInputType** y **IMediaObject:: SetOutputType**, pasando a cada función un puntero a una estructura **de \_ \_ tipo de medio DMO** que representa el tipo de medio solicitado.

Si el complemento de DSP actúa como MFT, Windows Media Player establece el tipo de medio mediante una llamada a **IMFTransform:: SetInputType** y **IMFTransform:: SetOutputType**, pasando a cada función un puntero a una interfaz **IMFMediaType** que representa el tipo de medio solicitado.

No hay ninguna garantía de que el reproductor llame a los métodos de negociación de formato en un orden determinado, por lo que el código de complemento debe controlar cualquier caso. Por ejemplo, si el reproductor llama a **SetOutputType** antes de llamar a **SetInputType**, es un curso de acción válido para que el complemento rechace el tipo de medio de salida propuesto. El siguiente código de la implementación de ejemplo de **IMediaObject:: SetOutputType** muestra esto:


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



Las implementaciones de complementos de ejemplo de **SetInputType** y **SetOutputType** llaman a la función personalizada denominada **ValidateMediaType**. Esta función de complemento realiza una serie de pruebas en el tipo de medio propuesto diseñado para asegurarse de que el tipo de medio tiene el formato correcto y es compatible con el complemento. **ValidateMediaType** realiza las siguientes pruebas:

-   Comprueba que los miembros **majortype** y **formatType** contienen los valores correctos.
-   Comprueba que el miembro del **subtipo** coincide con uno de los formatos admitidos.
-   Comprueba que la información de las estructuras **BITMAPINFOHEADER** y **VIDEOINFOHEADER** o **VIDEOINFOHEADER2** contiene valores válidos.
-   Comprueba si los tipos de medios de entrada y salida coinciden porque el complemento no convierte los formatos de entrada a salida.

Si el tipo de medio propuesto pasa las pruebas de validación, se almacena en una variable miembro: **m \_ mtInput** para el tipo de medio de entrada, **m \_ mtOutput** para el tipo de medio de salida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de un complemento DSP de vídeo**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 




