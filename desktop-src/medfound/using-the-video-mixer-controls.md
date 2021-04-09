---
description: Usar los controles de mezclador de vídeo
ms.assetid: 475996c6-a205-4133-8882-f55beaf9f8fd
title: Usar los controles de mezclador de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8a062c6f984e0eac0128bd67c72bf691c95af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082429"
---
# <a name="using-the-video-mixer-controls"></a>Usar los controles de mezclador de vídeo

El mezclador EVR proporciona varias interfaces que una aplicación puede usar para controlar cómo el mezclador procesa vídeo. Estas interfaces se pueden utilizar en DirectShow o en Media Foundation.



| Interfaz                                                      | Descripción                                                                                                                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaz [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)   | Alfa: combina una imagen de mapa de bits estática en el vídeo.                                                                                                                                                                                          |
| Interfaz [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol) | Controla el modo en que el EVR mezcla subsecuencias de vídeo.                                                                                                                                                                                                |
| Interfaz [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)       | Controla el ajuste de color, los filtros de imagen y otras capacidades de procesamiento de vídeo. Esta interfaz proporciona acceso a la funcionalidad implementada por el controlador de gráficos, por lo que las capacidades exactas dependerán del controlador de gráficos del usuario. |



 

La manera correcta de obtener punteros a estas interfaces depende de si se usa la versión de DirectShow de EVR o la versión de Media Foundation. En el Media Foundation EVR, también depende de si usa el EVR directamente o lo usa a través de la [sesión multimedia](media-session.md). (Normalmente, una aplicación usará el EVR a través de la sesión multimedia, no directamente).

Para obtener un puntero a cualquiera de estas interfaces, haga lo siguiente:

1.  Obtiene un puntero a la interfaz [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) en EVR.

    -   Si usa el filtro EVR de DirectShow, llame a **QueryInterface** en el filtro.

    -   Si usa el receptor de medios EVR directamente, llame a **QueryInterface** en el receptor de medios.

    -   Si usa la sesión multimedia, llame a **QueryInterface** en la sesión multimedia.

2.  Si usa la sesión multimedia, espere a que la sesión multimedia envíe el evento [MESessionTopologyStatus](mesessiontopologystatus.md) con el valor de estado MF \_ TOPOSTATUS \_ listo. (Omita este paso si no está usando la sesión multimedia).

3.  Llame a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obtener la interfaz de mezclador. Use el servicio de mezclador de vídeo del identificador de servicio MR \_ \_ \_ .

## <a name="alpha-blending-a-bitmap-onto-the-video"></a>Alfa mezclar un mapa de bits en el vídeo

Puede usar la interfaz [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) para alfa mezclar un mapa de bits estático en el vídeo durante la reproducción. Puede almacenar el mapa de bits en una superficie de Direct3D, que se especifica como un puntero **IDirect3DSurface9** , o usar un mapa de bits GDI.

Si usa una superficie de Direct3D para el mapa de bits, la superficie puede contener datos alfa por píxel, que se usarán cuando el mezclador alfa mezcle la imagen. Como alternativa, puede definir una clave de color, es decir, un color único que será transparente dondequiera que aparezca en el mapa de bits. Además, puede especificar un valor alfa que se aplicará a toda la imagen. También puede establecer un rectángulo de origen para recortar el mapa de bits y un rectángulo de destino para colocar el mapa de bits dentro del fotograma de vídeo.

Para establecer el mapa de bits, llame a [**IMFVideoMixerBitmap:: SetAlphaBitmap**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-setalphabitmap). Este método toma un puntero a una estructura [**MFVideoAlphaBitmap**](/windows/desktop/api/evr9/ns-evr9-mfvideoalphabitmap) que especifica el mapa de bits y los parámetros de combinación alfa. Para ver un ejemplo de código, vea el tema de referencia para el método **SetAlphaBitmap** .

Después de establecer el mapa de bits, puede actualizar los parámetros de fusión, incluidos los recangles de origen y de destino, llamando a [**IMFVideoMixerBitmap:: UpdateAlphaBitmapParameters**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-updatealphabitmapparameters). La actualización surte efecto en el siguiente fotograma de vídeo. El vídeo debe reproducirse para que se produzca la actualización. Puede utilizar este método para realizar animaciones simples en el mapa de bits. (Si necesita efectos más sofisticados, considere la posibilidad de escribir un mezclador de EVR personalizado).

Para borrar el mapa de bits, llame a [**IMFVideoMixerBitmap:: ClearAlphaBitmap**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-clearalphabitmap).

## <a name="controlling-substreams"></a>Controlar subsecuencias

EVR puede mezclar una o más subsecuencias de vídeo en el flujo de vídeo principal. Para controlar la combinación de subflujo, use la interfaz [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol) .

-   Llame a [**IMFVideoMixerControl:: SetStreamOutputRect**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol-setstreamoutputrect) para establecer la posición de una subsecuencia en el fotograma de vídeo compuesto.

-   Llame a [**IMFVideoMixerControl:: SetStreamZOrder**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol-setstreamzorder) para establecer el orden z de las subsecuencias. El EVR dibuja las secuencias de vídeo en el orden de sus valores de orden z, empezando por cero. El flujo de vídeo principal siempre es el primero en el orden z.

## <a name="video-processor-settings"></a>Configuración del procesador de vídeo

El mezclador de EVR usa la aceleración de vídeo de DirectX (DXVA) para realizar el procesamiento de vídeo en los flujos de entrada. Las capacidades de procesamiento exactas dependen del controlador de gráficos. Las capacidades de procesamiento de vídeo se describen mediante el uso de la estructura [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) . Un conjunto determinado de funciones se denomina *modo de procesamiento de vídeo* y cada modo se identifica mediante un GUID. Para obtener una lista de los GUID predefinidos, vea [**IDirectXVideoProcessorService:: GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids). El controlador puede definir GUID adicionales específicos del proveedor, que representan diferentes combinaciones de funcionalidades.

Para buscar los modos admitidos y las capacidades de cada modo, haga lo siguiente:

1.  Llame a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obtener un puntero a la interfaz [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor) del mezclador.

2.  Llame a [**IMFVideoProcessor:: GetAvailableVideoProcessorModes**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getavailablevideoprocessormodes). Este método devuelve una matriz de GUID, que identifica los modos de procesador de vídeo disponibles. La lista se devuelve en orden de calidad descendente, el modo con la mayor calidad que aparece primero en la lista. La lista puede cambiar en función del formato del vídeo.

3.  Para cada GUID de la lista, llame a [**IMFVideoProcessor:: GetVideoProcessorCaps**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps) para buscar las capacidades del modo de procesador de vídeo correspondiente. El método rellena una estructura [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) con una descripción de las capacidades.

4.  Para seleccionar un modo, llame a [**IMFVideoProcessor:: SetVideoProcessorMode**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setvideoprocessormode). De lo contrario, EVR selecciona automáticamente un modo cuando comienza el streaming. En ese caso, puede llamar a [**IMFVideoProcessor:: GetVideoProcessorMode**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessormode) para buscar el modo seleccionado.

La mayoría de los campos de la estructura [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) describen el comportamiento del controlador de bajo nivel y no son de interés en una aplicación típica. Lo más probable es que los campos siguientes sean de interés:

-   **DeviceCaps**. Este campo indica si el procesamiento de vídeo se realiza en hardware o software, y si el controlador de gráficos es un controlador de DXVA 1,0 antiguo.

-   **DeinterlaceTechnology**. Este campo proporciona alguna indicación del nivel de calidad de desentrelazado que puede esperar si el vídeo de origen está entrelazado.

-   **ProcAmpControlCaps**. Este campo especifica qué controles de ajuste de color están disponibles. Para obtener una lista de posibles ajustes de color, consulte [configuración de ProcAmp](procamp-settings.md). Si el controlador no puede realizar el ajuste de color, este campo es cero.

-   **VideoProcessorOperations**. Este campo contiene marcas que describen las diversas capacidades de procesamiento de vídeo. Dos marcas de importancia concreta son la \_ \_ marca subsecuencias de DXVA2 videoprocess y la \_ marca subsecuencias de videoprocess de DXVA2 \_ . Debe haber al menos una de estas marcas para que EVR mezcle subflujos en el flujo de vídeo de referencia. Si no hay ninguna marca, la EVR se limita a una secuencia de vídeo.

-   **NoiseFilterTechnology**. Este campo indica qué filtros de ruido admite el controlador de gráficos. Si el controlador no admite el filtrado de ruido, el valor es DXVA2 \_ NoiseFilterTech no \_ compatible.

-   **DetailFilterTechnology**. Este campo indica qué filtros de detalle son compatibles con el controlador de gráficos. Si el controlador no admite el filtrado de ruido, el valor es DXVA2 \_ DetailFilterTech no \_ compatible.

## <a name="color-adjustment-and-image-filtering"></a>Ajuste de color y filtrado de imágenes

El controlador de gráficos puede admitir el ajuste de color (también denominado *amplificación de proceso* o simplemente *ProcAmp*) y el filtrado de imágenes. Cuando se realiza mediante la GPU, el ajuste de color y el filtrado de imágenes se pueden realizar en tiempo real sin sobrecarga de la CPU.

Para usar estas características, realice los pasos siguientes:

1.  Seleccione un modo de procesamiento de vídeo como se describe en la sección anterior.

2.  Llame a [**IMFVideoProcessor:: GetVideoProcessorCaps**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps) para buscar las capacidades de procesamiento de vídeo como se describe en la sección anterior. El método rellena una estructura [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) que describe las capacidades, incluido si el controlador admite el ajuste de color y el filtro de imagen.

3.  Para cada ajuste de color que sea compatible con el controlador, llame a [**IMFVideoProcessor:: GetProcAmpRange**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getprocamprange) para buscar el intervalo posible de valor para esa configuración. Este método también devuelve el valor predeterminado de la configuración. Llame a [**IMFVideoProcessor:: GetProcAmpValues**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getprocampvalues) para buscar el valor actual de la configuración. Los valores no tienen unidades especificadas. Depende del controlador definir el intervalo de valores.

4.  Llame a [**IMFVideoProcessor:: SetFilteringValue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setfilteringvalue) para establecer un valor de ajuste de color.

5.  Si el controlador admite el filtrado de imágenes, cada tipo de filtro (ruido y detalle) admite tres configuraciones: nivel, radio y umbral, tanto en croma como en luminancia. (Consulte [configuración del filtro de imagen de DXVA](dxva-image-filter-settings.md)). Para cada configuración, llame a [**IMFVideoProcessor:: GetFilteringRange**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getfilteringrange) para obtener el intervalo de valores posibles y llame a [**IMFVideoProcessor:: GetFilteringValue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getfilteringvalue) para obtener el valor actual.

6.  Para cambiar una configuración de filtro de imagen, llame a [**IMFVideoProcessor:: SetFilteringValue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setfilteringvalue).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representador de vídeo mejorado](enhanced-video-renderer.md)
</dt> </dl>

 

 



