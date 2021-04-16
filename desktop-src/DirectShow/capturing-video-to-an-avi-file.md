---
description: Capturar vídeo en un archivo AVI
ms.assetid: 0f5f4a82-4a2e-4c48-b201-bda641cb8619
title: Capturar vídeo en un archivo AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86504e9ce149f495e1ea31664f56382340d33887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104558888"
---
# <a name="capturing-video-to-an-avi-file"></a>Capturar vídeo en un archivo AVI

En la ilustración siguiente se muestra el gráfico más sencillo posible para capturar vídeo en un archivo AVI.

![gráfico de captura de vídeo AVI](images/vidcap02.png)

El filtro de [AVI-MUX](avi-mux-filter.md) toma el flujo de vídeo del PIN de captura y lo empaqueta en una secuencia AVI. También se puede conectar una secuencia de audio al filtro de AVI, en cuyo caso el MUX intercalaría las dos secuencias. El filtro del [escritor de archivos](file-writer-filter.md) escribe el flujo AVI en el disco.

Para compilar el gráfico, empiece por llamar al método [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) , como se indica a continuación:


```C++
IBaseFilter *pMux;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Avi,  // Specifies AVI for the target file.
    L"C:\\Example.avi", // File name.
    &pMux,              // Receives a pointer to the mux.
    NULL);              // (Optional) Receives a pointer to the file sink.
```



El primer parámetro especifica el tipo de archivo; en este caso, AVI. El segundo parámetro proporciona el nombre de archivo. Para AVI, el método SetOutputFileName crea el filtro de AVI y el filtro de escritor de archivos y los agrega al gráfico. También establece el nombre de archivo en el filtro del escritor de archivos, llamando al método [**IFileSinkFilter:: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) y conecta los dos filtros. El método devuelve un puntero a AVI MUX en el tercer parámetro. Opcionalmente, devuelve un puntero a la interfaz [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) en el cuarto parámetro. Si no necesita esta interfaz, puede establecer este parámetro en **null**, como se muestra en el ejemplo anterior.

A continuación, llame al método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar el filtro de captura a AVI MUX, como se indica a continuación:


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                  // Capture filter.
    NULL,                  // Intermediate filter (optional).
    pMux);                 // Mux or file sink filter.

// Release the mux filter.
pMux->Release();
```



El primer parámetro proporciona la categoría PIN, que es la \_ \_ captura de categoría PIN para la captura. El segundo parámetro proporciona el tipo de medio. El tercer parámetro es un puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro de captura. El cuarto parámetro es opcional. permite enrutar el flujo de vídeo a través de un filtro intermedio, como un codificador, antes de pasarlo al filtro Mux. De lo contrario, establezca este parámetro en **null**, como se muestra en el ejemplo anterior. El quinto parámetro es el puntero al filtro Mux. Este puntero se obtiene llamando al método SetOutputFileName.

Para capturar audio, llame a RenderStream con el tipo de archivo multimedia MEDIATYPE \_ audio. Si va a capturar audio y vídeo desde dos dispositivos independientes, es una buena idea convertir la secuencia de audio en la secuencia maestra. Esto ayuda a evitar el desplazamiento entre los dos flujos, ya que el filtro de AVI MUX ajusta la velocidad de reproducción en el flujo de vídeo para que coincida con la secuencia de audio. Para establecer la secuencia maestra, llame al método [**IConfigAviMux:: SetMasterStream**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) en el filtro de AVI MUX:


```C++
IConfigAviMux *pConfigMux = NULL;
hr = pMux->QueryInterface(IID_IConfigAviMux, (void**)&pConfigMux);
if (SUCCEEDED(hr))
{
    pConfigMux->SetMasterStream(1);
    pConfigMux->Release();
}
```



El parámetro para SetMasterStream es el número de secuencia, que viene determinado por el orden en el que se llama a RenderStream. Por ejemplo, si llama primero a RenderStream para el vídeo y luego para audio, el vídeo es el flujo 0 y el audio es el flujo 1.

También puede establecer el modo en que el filtro de AVI MUX intercala las secuencias de audio y vídeo, llamando al método [**IConfigInterleaving::p \_ UT**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode) .


```C++
IConfigInterleaving *pInterleave = NULL;
hr = pMux->QueryInterface(IID_IConfigInterleaving, (void**)&pInterleave);
if (SUCCEEDED(hr))
{
    pInterleave->put_Mode(INTERLEAVE_CAPTURE);
    pInterleave->Release();
}
```



Con la marca de captura de intercalación \_ , AVI MUX realiza la intercalación a una velocidad adecuada para la captura de vídeo. También puede usar la intercalación \_ None, lo que significa que no hay intercalación: AVI MUX simplemente escribirá los datos en el orden en que llegan. La marca de intercalación \_ completa significa que AVI MUX realiza una intercalación completa; sin embargo, este modo es menos adecuado para la captura de vídeo porque requiere el mayor nivel de rendimiento.

Codificar la secuencia de vídeo

Puede codificar el flujo de vídeo insertando un filtro de codificador entre el filtro de captura y el filtro de AVI. Use el [enumerador de dispositivos del sistema](system-device-enumerator.md) o el [asignador de filtros](filter-mapper.md) para seleccionar un filtro de codificador. (Para obtener más información, consulte [enumeración de dispositivos y filtros](enumerating-devices-and-filters.md)).

Especifique el filtro del codificador como cuarto parámetro en RenderStream, que se muestra en negrita en el ejemplo siguiente:


```C++
IBaseFilter *pEncoder;
/* Create the encoder filter (not shown). */
// Add it to the filter graph.
pGraph->AddFilter(pEncoder, L"Encoder");

/* Call SetOutputFileName as shown previously. */

// Render the stream.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, 
    pCap, 
pEncoder, pMux);
pEncoder->Release();
```



El filtro del codificador podría admitir [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) u otras interfaces para establecer los parámetros de codificación. Para obtener una lista de interfaces posibles, vea [interfaces de codificación y descodificación de archivos](file-encoding-and-decoding-interfaces.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Capturar vídeo en un archivo](capturing-video-to-a-file.md)
</dt> </dl>

 

 



