---
description: Uso de los controles de Mixer vídeo
ms.assetid: 475996c6-a205-4133-8882-f55beaf9f8fd
title: Uso de los controles de Mixer vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8a062c6f984e0eac0128bd67c72bf691c95af6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363690"
---
# <a name="using-the-video-mixer-controls"></a>Uso de los controles de Mixer vídeo

El mezclador EVR proporciona varias interfaces que una aplicación puede usar para controlar cómo procesa el vídeo el mezclador. Estas interfaces se pueden usar en DirectShow o Media Foundation.



| Interfaz                                                      | Descripción                                                                                                                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INTERFAZ DE MAPADEMEDAMeserBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)   | Combina alfa una imagen de mapa de bits estática en el vídeo.                                                                                                                                                                                          |
| [**INTERFAZ DE CONTROL DEVIDEOVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol) | Controla cómo la EVR combina substreams de vídeo.                                                                                                                                                                                                |
| [**Interfaz DEPROCESSORVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)       | Controla el ajuste de color, los filtros de imagen y otras funcionalidades de procesamiento de vídeo. Esta interfaz proporciona acceso a la funcionalidad implementada por el controlador de gráficos, por lo que las funcionalidades exactas dependerán del controlador de gráficos del usuario. |



 

La manera correcta de obtener punteros a estas interfaces depende de si usa la versión DirectShow de la EVR o la Media Foundation anterior. Para la Media Foundation EVR, también depende de si usa la EVR directamente o mediante la [sesión multimedia](media-session.md). (Normalmente, una aplicación usará la EVR a través de la sesión multimedia, no directamente).

Para obtener un puntero a cualquiera de estas interfaces, haga lo siguiente:

1.  Obtenga un puntero a la [**interfaz IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) en la EVR.

    -   Si usa el filtro DirectShow EVR, llame a **QueryInterface** en el filtro.

    -   Si usa el receptor de medios EVR directamente, llame a **QueryInterface** en el receptor de medios.

    -   Si usa la sesión multimedia, llame a **QueryInterface** en la sesión multimedia.

2.  Si usa la sesión multimedia, espere a que la sesión multimedia envíe el evento [MESessionTopologyStatus](mesessiontopologystatus.md) con un valor de estado DE MF \_ TOPOSTATUS \_ READY. (Omita este paso si no usa la sesión multimedia).

3.  Llame [**a IMFGetService::GetService para**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) obtener la interfaz mezcladora. Use el identificador de servicio MR \_ VIDEO \_ MIXER \_ SERVICE.

## <a name="alpha-blending-a-bitmap-onto-the-video"></a>Combinación alfa de un mapa de bits en el vídeo

Puede usar la interfaz [**IMFVideoMixerBitmap para**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) combinar alfamente un mapa de bits estático en el vídeo durante la reproducción. Puede almacenar el mapa de bits en una superficie de Direct3D, especificada como puntero **IDirect3DSurface9,** o usar un mapa de bits GDI.

Si usa una superficie de Direct3D para el mapa de bits, la superficie puede contener datos alfa por píxel, que se usarán cuando el mezclador combine alfa la imagen. Como alternativa, puede definir una clave de color, es decir, un único color que será transparente dondequiera que aparezca en el mapa de bits. Además, puede especificar un valor alfa que se aplicará a toda la imagen. También puede establecer un rectángulo de origen para recortar el mapa de bits y un rectángulo de destino para colocar el mapa de bits dentro del marco de vídeo.

Para establecer el mapa de bits, llame [**a IMFVideoMixerBitmap::SetAlphaBitmap**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-setalphabitmap). Este método toma un puntero a una [**estructura MFVideoAlphaBitmap**](/windows/desktop/api/evr9/ns-evr9-mfvideoalphabitmap) que especifica el mapa de bits y los parámetros de combinación alfa. Para obtener código de ejemplo, vea el tema de referencia del **método SetAlphaBitmap.**

Después de establecer el mapa de bits, puede actualizar los parámetros de combinación, incluidos los recangles de origen y destino, mediante una llamada a [**IMFVideoMixerBitmap::UpdateAlphaBitmapParameters**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-updatealphabitmapparameters). La actualización tiene efecto en el siguiente fotograma de vídeo. El vídeo debe reproducirse para que se produzca la actualización. Puede usar este método para realizar animaciones simples en el mapa de bits. (Si necesita efectos más sofisticados, considere la posibilidad de escribir un mezclador EVR personalizado).

Para borrar el mapa de bits, llame [**a IMFVideoMixerBitmap::ClearAlphaBitmap**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-clearalphabitmap).

## <a name="controlling-substreams"></a>Control de substreams

La EVR puede mezclar una o varias secuencias de vídeo en la secuencia de vídeo principal. Para controlar la combinación de substream, use la [**interfaz IMFVideo MixerControl.**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)

-   Llame [**a IMFVideoMixerControl::SetStreamOutputRect**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol-setstreamoutputrect) para establecer la posición de una subsección dentro del fotograma de vídeo compuesto.

-   Llame [**a IMFVideoMixerControl::SetStreamZOrder**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol-setstreamzorder) para establecer el orden z de las substreams. La EVR dibuja las secuencias de vídeo en el orden de sus valores de orden Z, empezando por cero. La secuencia de vídeo principal siempre es la primera en el orden Z.

## <a name="video-processor-settings"></a>Procesador de vídeo Configuración

El mezclador EVR usa la aceleración de vídeo de DirectX (DXVA) para realizar el procesamiento de vídeo en los flujos de entrada. Las funcionalidades de procesamiento exactas dependen del controlador de gráficos. Las funcionalidades de procesamiento de vídeo se describen mediante [**la estructura \_ VideoProcessorCaps de DXVA2.**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) Un conjunto determinado de funcionalidades se denomina modo *de procesamiento de vídeo,* y cada modo se identifica mediante un GUID. Para obtener una lista de GUID predefinidos, vea [**IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids). El controlador podría definir GUID adicionales específicos del proveedor, que representan diferentes combinaciones de funcionalidades.

Para buscar los modos admitidos y las funcionalidades de cada modo, haga lo siguiente:

1.  Llame [**a IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obtener un puntero a la interfaz [**DEL PROCESADOR DEL MEZCLADOR.**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)

2.  Llame [**a IMFVideoProcessor::GetAvailableVideoProcessorModes**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getavailablevideoprocessormodes). Este método devuelve una matriz de GUID, que identifican los modos de procesador de vídeo disponibles. La lista se devuelve en orden de calidad descendente, el modo con la calidad más alta aparece primero en la lista. La lista puede cambiar en función del formato del vídeo.

3.  Para cada GUID de la lista, llame [**a IMFVideoProcessor::GetVideoProcessorCaps**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps) para encontrar las funcionalidades del modo de procesador de vídeo correspondiente. El método rellena una [**estructura \_ DxVA2 VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) con una descripción de las funcionalidades.

4.  Para seleccionar un modo, llame a [**IMFVideoProcessor::SetVideoProcessorMode**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setvideoprocessormode). De lo contrario, evr selecciona automáticamente un modo cuando comienza el streaming. En ese caso, puede llamar a [**IMFVideoProcessor::GetVideoProcessorMode**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessormode) para buscar qué modo se seleccionó.

La mayoría de los campos de la [**estructura \_ VideoProcessorCaps de DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) describen el comportamiento del controlador de bajo nivel y no son de interés en una aplicación típica. Es más probable que los campos siguientes sean de interés:

-   **DeviceCaps**. Este campo indica si el procesamiento de vídeo se realiza en hardware o software, y si el controlador de gráficos es un controlador DXVA 1.0 anterior.

-   **DeinterlaceTechnology**. Este campo proporciona alguna indicación de qué nivel de calidad de desenlazamiento puede esperar si el vídeo de origen está entrelazado.

-   **ProcAmpControlCaps**. Este campo especifica qué controles de ajuste de color están disponibles. Para obtener una lista de posibles ajustes de color, vea [ProcAmp Configuración](procamp-settings.md). Si el controlador no puede realizar el ajuste de color, este campo es cero.

-   **VideoProcessorOperations**. Este campo contiene marcas que describen varias funcionalidades de procesamiento de vídeo. Dos marcas de especial importancia son la marca DXVA2 VideoProcess SubStreams y la marca \_ \_ DXVA2 \_ VideoProcess \_ SubStreams. Al menos una de estas marcas debe estar presente para que la EVR mezcle substreams en la secuencia de vídeo de referencia. Si no hay ninguna marca, la EVR se limita a una secuencia de vídeo.

-   **NoiseFilterTechnology**. Este campo indica qué filtros de ruido son compatibles con el controlador de gráficos. Si el controlador no admite el filtrado de ruido, el valor es DXVA2 \_ NoiseFilterTech \_ No compatible.

-   **DetailFilterTechnology**. Este campo indica qué filtros de detalles son compatibles con el controlador de gráficos. Si el controlador no admite el filtrado de ruido, el valor es DXVA2 \_ DetailFilterTech \_ No compatible.

## <a name="color-adjustment-and-image-filtering"></a>Ajuste de color y filtrado de imágenes

El controlador de gráficos puede admitir el ajuste de color (también denominado *amplificación del proceso* o simplemente *ProcAmp)* y el filtrado de imágenes. Cuando lo realiza la GPU, el ajuste de color y el filtrado de imágenes se pueden realizar en tiempo real sin sobrecarga de CPU.

Para usar estas características, realice los pasos siguientes:

1.  Seleccione un modo de procesamiento de vídeo como se describe en la sección anterior.

2.  Llame [**a IMFVideoProcessor::GetVideoProcessorCaps**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps) para encontrar las funcionalidades de procesamiento de vídeo como se describe en la sección anterior. El método rellena una estructura [**\_ DxVA2 VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) que describe las funcionalidades, incluido si el controlador admite el ajuste de color y el filtro de imagen.

3.  Para cada ajuste de color que sea compatible con el controlador, llame a [**IMFVideoProcessor::GetProcAmpRange**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getprocamprange) para encontrar el posible intervalo de valor para esa configuración. Este método también devuelve el valor predeterminado de la configuración. Llame [**a IMFVideoProcessor::GetProcAmpValues**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getprocampvalues) para buscar el valor actual de la configuración. Los valores no tienen unidades especificadas. Es el controlador el que define el intervalo de valores.

4.  Llame [**a IMFVideoProcessor::SetFilteringValue para**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setfilteringvalue) establecer un valor de ajuste de color.

5.  Si el controlador admite el filtrado de imágenes, cada tipo de filtro (ruido y detalles) admite tres configuraciones(nivel, radio y umbral) tanto en el sonido como en el luma. (Vea [Filtro de imagen DXVA Configuración](dxva-image-filter-settings.md)). Para cada configuración, llame [**a IMFVideoProcessor::GetFilteringRange**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getfilteringrange) para obtener el intervalo de valores posibles y llame a [**IMFVideoProcessor::GetFilteringValue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getfilteringvalue) para obtener el valor actual.

6.  Para cambiar la configuración de un filtro de imagen, llame [**a IMFVideoProcessor::SetFilteringValue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setfilteringvalue).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representador de vídeo mejorado](enhanced-video-renderer.md)
</dt> </dl>

 

 



