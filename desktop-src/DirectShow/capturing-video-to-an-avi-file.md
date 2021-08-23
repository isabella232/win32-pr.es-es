---
description: Captura de vídeo en un archivo AVI
ms.assetid: 0f5f4a82-4a2e-4c48-b201-bda641cb8619
title: Captura de vídeo en un archivo AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5ec58c021c5f37fed992959b33965efddb5603798ff756909879d307bca1f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689045"
---
# <a name="capturing-video-to-an-avi-file"></a>Captura de vídeo en un archivo AVI

En la ilustración siguiente se muestra el gráfico más sencillo posible para capturar vídeo en un archivo AVI.

![Gráfico de captura de vídeo avi](images/vidcap02.png)

El [filtro AVI Mux](avi-mux-filter.md) toma la secuencia de vídeo del pin de captura y la empaqueta en una secuencia AVI. También se podría conectar una secuencia de audio al filtro avi Mux, en cuyo caso el mux intercalaría las dos secuencias. El [filtro Escritor de](file-writer-filter.md) archivos escribe la secuencia AVI en el disco.

Para compilar el gráfico, empiece por llamar al [**método ICaptureGraphBuilder2::SetOutputFileName,**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) como se muestra a continuación:


```C++
IBaseFilter *pMux;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Avi,  // Specifies AVI for the target file.
    L"C:\\Example.avi", // File name.
    &pMux,              // Receives a pointer to the mux.
    NULL);              // (Optional) Receives a pointer to the file sink.
```



El primer parámetro especifica el tipo de archivo; en este caso, AVI. El segundo parámetro proporciona el nombre de archivo. Para AVI, el método SetOutputFileName crea el filtro Mux avi y el filtro File Writer y los agrega al gráfico. También establece el nombre de archivo en el filtro escritor de archivos, llamando al método [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) y conecta los dos filtros. El método devuelve un puntero al Mux avi en el tercer parámetro. Opcionalmente, devuelve un puntero a la [**interfaz IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) en el cuarto parámetro. Si no necesita esta interfaz, puede establecer este parámetro en **NULL,** como se muestra en el ejemplo anterior.

A continuación, llame [**al método ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar el filtro de captura al Mux avi, como se muestra a continuación:


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



El primer parámetro proporciona la categoría pin, que es PIN \_ CATEGORY CAPTURE para la \_ captura. El segundo parámetro proporciona el tipo de medio. El tercer parámetro es un puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro de captura. El cuarto parámetro es opcional; permite enrutar la secuencia de vídeo a través de un filtro intermedio, como un codificador, antes de pasarla al filtro mux. De lo contrario, establezca este parámetro **en NULL,** como se muestra en el ejemplo anterior. El quinto parámetro es el puntero al filtro mux. Este puntero se obtiene llamando al método SetOutputFileName.

Para capturar audio, llame a RenderStream con el tipo de medio MEDIATYPE \_ Audio. Si va a capturar audio y vídeo desde dos dispositivos independientes, es una buena idea convertir la secuencia de audio en la secuencia maestra. Esto ayuda a evitar el desajuste entre las dos secuencias, ya que el filtro avi Mux ajusta la velocidad de reproducción de la secuencia de vídeo para que coincida con la secuencia de audio. Para establecer la secuencia maestra, llame al método [**IConfigAviMux::SetMasterStream**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) en el filtro avi Mux:


```C++
IConfigAviMux *pConfigMux = NULL;
hr = pMux->QueryInterface(IID_IConfigAviMux, (void**)&pConfigMux);
if (SUCCEEDED(hr))
{
    pConfigMux->SetMasterStream(1);
    pConfigMux->Release();
}
```



El parámetro para SetMasterStream es el número de secuencia, que viene determinado por el orden en el que se llama a RenderStream. Por ejemplo, si llama a RenderStream primero para vídeo y, a continuación, para audio, el vídeo es stream 0 y el audio es stream 1.

También puede establecer cómo el filtro AVI Mux intercala las secuencias de audio y vídeo mediante una llamada al método [**IConfigInterleaving::p ut \_ Mode.**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode)


```C++
IConfigInterleaving *pInterleave = NULL;
hr = pMux->QueryInterface(IID_IConfigInterleaving, (void**)&pInterleave);
if (SUCCEEDED(hr))
{
    pInterleave->put_Mode(INTERLEAVE_CAPTURE);
    pInterleave->Release();
}
```



Con la marca INTERLEAVE CAPTURE, avi Mux realiza la intercalación a una velocidad adecuada para \_ la captura de vídeo. También puede usar INTERLEAVE NONE, lo que significa que no hay intercalación: avi Mux simplemente escribirá los datos en el orden en que \_ llegan. La marca INTERLEAVE FULL significa que AVI Mux realiza el intercalado completo; sin embargo, este modo es menos adecuado para la captura de vídeo porque requiere el más \_ sobresalido.

Codificación del flujo de vídeo

Puede codificar la secuencia de vídeo insertando un filtro de codificador entre el filtro de captura y el filtro avi Mux. Use el [Enumerador de dispositivos del sistema](system-device-enumerator.md) o [el Asignador de filtros](filter-mapper.md) para seleccionar un filtro de codificador. (Para obtener más información, [vea Enumerar dispositivos y filtros).](enumerating-devices-and-filters.md)

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



El filtro del codificador puede admitir [**IAMVideoCompression u**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) otras interfaces para establecer los parámetros de codificación. Para obtener una lista de las interfaces posibles, vea [File Encoding and Decoding Interfaces](file-encoding-and-decoding-interfaces.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Capturar vídeo en un archivo](capturing-video-to-a-file.md)
</dt> </dl>

 

 



