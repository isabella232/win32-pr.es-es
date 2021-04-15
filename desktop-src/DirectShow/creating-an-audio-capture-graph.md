---
description: Creación de un gráfico de captura de audio
ms.assetid: 2302bb40-a5db-473a-afeb-71905ac41f47
title: Creación de un gráfico de captura de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd3c731a7dc498fcb7180bc56ae6a7f94dbec6d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666150"
---
# <a name="creating-an-audio-capture-graph"></a>Creación de un gráfico de captura de audio

El primer paso para una aplicación de captura de audio es crear un gráfico de filtro. La configuración del gráfico depende del tipo de archivo que desea crear.

-   Archivo AVI de solo audio: filtro de captura de audio para filtro de [AVI de AVI](avi-mux-filter.md) y filtro de AVI MUX al [escritor de archivos](file-writer-filter.md) .
-   Archivo WAV: filtro de captura de audio en el [ejemplo de filtro de WavDest](wavdest-filter-sample.md) al filtro de escritura de archivos
-   Archivo de Windows Media Audio (. WMA): filtro de captura de audio para el filtro del [escritor ASF de WM](wm-asf-writer-filter.md) .

El filtro WavDest se proporciona como un ejemplo de SDK. Para usarlo, debe compilar y registrar el filtro.

Para usar el filtro del escritor ASF, debe instalar el SDK de Windows Media y obtener una clave de software para desbloquear el filtro. Para obtener más información, vea [usar Windows Media en DirectShow](using-windows-media-in-directshow.md).

Puede compilar el gráfico de filtro mediante el objeto [generador de gráficos de captura](capture-graph-builder.md) o puede compilar el gráfico "manualmente". es decir, hacer que la aplicación agregue y conecte mediante programación cada filtro. En este artículo se describe el enfoque manual. Para obtener más información sobre cómo usar el generador de gráficos de captura, consulte [captura de vídeo](video-capture.md). Gran parte de la información de ese artículo se aplica a los gráficos de solo audio.

Agregar el dispositivo de captura de audio

Dado que el filtro de captura de audio se comunica con un dispositivo de hardware específico, no se puede llamar simplemente a **CoCreateInstance** para crear el filtro. En su lugar, use el [enumerador de dispositivos del sistema](system-device-enumerator.md) para enumerar todos los dispositivos de la categoría "orígenes de captura de audio", que se identifica mediante el identificador de clase CLSID \_ AudioInputDeviceCategory.

El enumerador de dispositivos del sistema devuelve una lista de monikers para los dispositivos; el nombre descriptivo de cada moniker corresponde al nombre del dispositivo. Elija uno de los monikers devueltos y úselo para crear una instancia del filtro de captura de audio para ese dispositivo. Agregue el filtro al gráfico de filtros. El dispositivo de grabación de audio preferido del usuario aparece en primer lugar en la lista de moniker. (El usuario selecciona un dispositivo preferido haciendo clic en sonidos y multimedia en el panel de control).

Para obtener más información, vea [usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).

Para especificar la entrada que se va a capturar, obtenga la interfaz [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) del filtro de captura de audio y llame al método **Put \_ enable** para especificar la entrada. Sin embargo, una limitación de este método es que distintos dispositivos de hardware pueden usar cadenas diferentes para identificar sus entradas. Por ejemplo, una tarjeta puede usar "micrófono" para identificar la entrada del micrófono y otra tarjeta puede usar "MIC". Para determinar el identificador de cadena de una entrada determinada, use las funciones multimedia de Windows [**waveOutOpen**](/previous-versions//dd743866(v=vs.85)), [**mixerOpen**](/previous-versions//dd757308(v=vs.85))y [**mixerGetLineInfo**](/previous-versions//dd757303(v=vs.85)). Vea el tema de MSDN [consultas de dispositivo](/windows/desktop/Multimedia/mixer-device-queries) para obtener más información.

Adición del multiplexor y del escritor de archivos

Un gráfico de captura de audio debe contener un multiplexor y un escritor de archivos.

Un *multiplexor* es un filtro que combina uno o varios flujos en un solo flujo con un formato determinado. Por ejemplo, el filtro de AVI MUX combina secuencias de audio y vídeo en una secuencia AVI intercalada. Para la captura de audio, normalmente solo hay una única secuencia de audio, pero los datos de audio se deben empaquetar en un formato que se pueda guardar en el disco, lo que requiere un multiplexor. La elección del multiplexor depende del formato de destino:

-   AVI: multiplexor de AVI
-   WAV: WavDest
-   WMA: ASF Writer

Un *escritor de archivos* es un filtro que escribe los datos entrantes en un archivo. En el caso de archivos AVI o WAV, use el [filtro de escritura de archivo](file-writer-filter.md). En el caso de los archivos WMA, el escritor ASF actúa como multiplexor y escritor de archivos.

Después de crear los filtros y agregarlos al gráfico, conecte el PIN de salida del filtro de captura de audio al pin de entrada del multiplexor y conecte el PIN de salida del multiplexor al pin de entrada del escritor del filtro (suponiendo que se trata de filtros independientes). Para especificar el nombre de archivo, consulte el escritor de archivos para la interfaz [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) y llame al método [**IFileSinkFilter:: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) .

### <a name="example-code"></a>Código de ejemplo

En el ejemplo siguiente se muestra cómo crear un gráfico de captura de audio mediante el filtro WavDest. Los mismos principios se aplican a los demás tipos de archivo.


```C++
IBaseFilter *pSrc = NULL, *pWaveDest = NULL, *pWriter = NULL;
IFileSinkFilter *pSink= NULL;
IGraphBuilder *pGraph;

// Create the Filter Graph Manager.
hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void**)&pGraph);

// This example omits error handling.

// Not shown: Use the System Device Enumerator to create the 
// audio capture filter.

// Add the audio capture filter to the filter graph. 
hr = pGraph->AddFilter(pSrc, L"Capture");

// Add the WavDest and the File Writer.
hr = AddFilterByCLSID(pGraph, CLSID_WavDest, L"WavDest", &pWaveDest);
hr = AddFilterByCLSID(pGraph, CLSID_FileWriter, L"File Writer", &pWriter);

// Set the file name.
hr = pWriter->QueryInterface(IID_IFileSinkFilter, (void**)&pSink);
hr = pSink->SetFileName(L"C:\\MyWavFile.wav", NULL);

// Connect the filters.
hr = ConnectFilters(pGraph, pSrc, pWaveDest);
hr = ConnectFilters(pGraph, pWaveDest, pWriter);

// Not shown: Release interface pointers.

```



En este ejemplo se usa la `AddFilterByCLSID` función descrita en [Agregar un filtro por CLSID](add-a-filter-by-clsid.md)y la `ConnectFilters` función descrita en [conectar dos filtros](connect-two-filters.md). Ninguno de ellos es una API de DirectShow.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de audio](audio-capture.md)
</dt> </dl>

 

 
