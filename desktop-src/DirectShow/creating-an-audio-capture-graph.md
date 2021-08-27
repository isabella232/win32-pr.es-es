---
description: Creación de una captura de audio Graph
ms.assetid: 2302bb40-a5db-473a-afeb-71905ac41f47
title: Creación de una captura de audio Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ff89cff8662bb5da81860053221596b18e89ab2300134cf2ff8826ae99b787
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108225"
---
# <a name="creating-an-audio-capture-graph"></a>Creación de una captura de audio Graph

El primer paso para una aplicación de captura de audio es crear un gráfico de filtro. La configuración del gráfico depende del tipo de archivo que quiera crear.

-   Archivo AVI de solo audio: filtro de captura de audio al filtro [Mux](avi-mux-filter.md) de AVI y filtro de Mux a [escritor de](file-writer-filter.md) archivos de AVI.
-   Archivo WAV: filtro de captura de audio a [ejemplo de filtro WavDest](wavdest-filter-sample.md) a filtro de escritor de archivos
-   Windows Archivo de audio multimedia (.wma): filtro de captura de audio para [el filtro WM ASF Writer.](wm-asf-writer-filter.md)

El filtro WavDest se proporciona como ejemplo de SDK. Para usarlo, debe compilar y registrar el filtro.

Para usar el filtro ASF Writer, debe instalar el SDK de Windows Media y obtener una clave de software para desbloquear el filtro. Para obtener más información, vea [Using Windows Media in DirectShow](using-windows-media-in-directshow.md).

Puede compilar el gráfico de filtros mediante el objeto [Capture Graph Builder,](capture-graph-builder.md) o bien puede compilar el gráfico "manualmente". Es decir, haga que la aplicación agregue y conecte cada filtro mediante programación. En este artículo se describe el enfoque manual. Para obtener más información sobre el uso de Capture Graph Builder, vea [Captura de vídeo.](video-capture.md) Gran parte de la información de ese artículo se aplica a los gráficos de solo audio.

Agregar el dispositivo de captura de audio

Dado que el filtro de captura de audio se comunica con un dispositivo de hardware específico, no puede llamar simplemente a **CoCreateInstance** para crear el filtro. En su [](system-device-enumerator.md) lugar, use el enumerador de dispositivos del sistema para enumerar todos los dispositivos de la categoría "Orígenes de captura de audio", que se identifica mediante el identificador de clase CLSID \_ AudioInputDeviceCategory.

El enumerador de dispositivos del sistema devuelve una lista de monikers para los dispositivos. El nombre descriptivo de cada moniker corresponde al nombre del dispositivo. Elija uno de los monikers devueltos y úselo para crear una instancia del filtro de captura de audio para ese dispositivo. Agregue el filtro al gráfico de filtros. El dispositivo de grabación de audio preferido del usuario aparece primero en la lista de moniker. (El usuario selecciona un dispositivo preferido haciendo clic en Sonidos y multimedia en Panel de control).

Para obtener más información, [vea Usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).

Para especificar de qué entrada se va a capturar, obtenga la interfaz [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) del filtro Audio Capture y llame al método **put \_ Enable** para especificar la entrada. Sin embargo, una limitación de este método es que los distintos dispositivos de hardware pueden usar cadenas diferentes para identificar sus entradas. Por ejemplo, una tarjeta puede usar "Micrófono" para identificar la entrada del micrófono y otra tarjeta puede usar "Micrófono". Para determinar el identificador de cadena de una entrada determinada, use las funciones multimedia [**waveOutOpen,**](/previous-versions//dd743866(v=vs.85)) [**mixerOpen**](/previous-versions//dd757308(v=vs.85))y [**mixerGetLineInfo**](/previous-versions//dd757303(v=vs.85))de Windows Multimedia. Consulte el tema de MSDN [Mixer Device Queries](/windows/desktop/Multimedia/mixer-device-queries) para obtener más información.

Agregar el multiplexor y el escritor de archivos

Un gráfico de captura de audio debe contener un multiplexor y un escritor de archivos.

Un *multiplexor* es un filtro que combina una o varias secuencias en una sola secuencia con un formato determinado. Por ejemplo, el filtro avi Mux combina secuencias de audio y vídeo en una secuencia AVI intercalada. Para la captura de audio, normalmente solo hay una secuencia de audio, pero los datos de audio deben empaquetarse en un formato que se pueda guardar en el disco, lo que requiere un multiplexor. La elección del multiplexor depende del formato de destino:

-   AVI: Multiplexor de AVI
-   WAV: WavDest
-   WMA: ASF Writer

Un *escritor de* archivos es un filtro que escribe datos entrantes en un archivo. En el caso de los archivos AVI o WAV, use el filtro [de escritor de archivos](file-writer-filter.md). En el caso de los archivos WMA, ASF Writer actúa como multiplexador y escritor de archivos.

Después de crear los filtros y agregarlos al gráfico, conecte el pin de salida del filtro de captura de audio al pin de entrada del multiplexor y conecte el pin de salida del multiplexador al pin de entrada del escritor de filtros (suponiendo que se trata de filtros independientes). Para especificar el nombre de archivo, consulte el escritor de archivos para la interfaz [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) y llame al [**método IFileSinkFilter::SetFileName.**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename)

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



En este ejemplo se usa la función descrita en Agregar un filtro por `AddFilterByCLSID` [CLSID](add-a-filter-by-clsid.md)y la función descrita en Conectar `ConnectFilters` [dos filtros](connect-two-filters.md). Ninguno de ellos es una API DirectShow.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de audio](audio-capture.md)
</dt> </dl>

 

 
