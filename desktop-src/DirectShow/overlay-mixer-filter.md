---
description: Filtro de mezclador de superposición
ms.assetid: e80938b7-31f0-467b-a3fa-c4511d14758d
title: Filtro de mezclador de superposición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475726607f282ce4b7885ec6c5aea562c0380cb0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476991"
---
# <a name="overlay-mixer-filter"></a>Filtro de mezclador de superposición

El filtro overlay Mixer es un representador de vídeo diseñado específicamente para la reproducción de DVD y la difusión de secuencias de vídeo con subtítulos de línea 21. Overlay Mixer también admite extensiones de puerto de vídeo (VPN), lo que le permite trabajar con descodificadores MPEG-2 de hardware o de tv análoga que envían vídeo directamente a la tarjeta gráfica, en lugar de a través del bus PCI.

> [!Note]  
> El [representador de mezcla de vídeo 9](video-mixing-renderer-filter-9.md) ahora es preferible al filtro overlay Mixer, excepto en escenarios de VPE.

 

El cuadro de Mixer usa DirectDraw para la representación. Requiere una superficie superpuesta en la tarjeta gráfica. La secuencia de vídeo principal debe estar conectada al pin 0. Las secuencias secundarias (gráficos de subtítulos o subpicturas de DVD) están conectadas a los pines 1 y superiores. El objeto Overlay Mixer blits the secondary streams directly onto the primary suface; no los mezcla ni los mezcla alfa.

El objeto Overlay Mixer el representador de vídeo para la administración de ventanas. El representador de vídeo se conecta a la Mixer de salida de La superposición.

Este filtro se agrega automáticamente al gráfico de filtros cuando las aplicaciones usan las interfaces [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) e [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) para crear el gráfico. El Administrador de Graph filtros no agregará automáticamente el elemento Overlay Mixer al gráfico.

> [!Note]  
> En la tabla siguiente, los subtipos de medios aceptados en el pin de entrada 0 dependen del hardware. El objeto Overlay Mixer puede determinar si se admite un subtipo determinado hasta que crea la superficie de DirectDraw. Por lo tanto, la única manera de que un filtro ascendente determine si se admite un subtipo es intentar una conexión con ese subtipo.

 




| | | Filtrar interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a>, <a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>, <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a> | | Tipos de medios de pin de entrada | Tipo principal: MEDIATYPE_Video<br /> Subtipos:<br /><ul><li>MEDIASUBTYPE_Overlay (solo pin 0)</li><li>Formatos YUV de DirectDraw (solo pin 0)</li><li>Formatos de aceleración de vídeo de DirectDraw (solo pin 0)</li><li>Formatos RGB de DirectDraw (todos los pines de entrada)</li></ul>Tipos de formato:<br /><ul><li>Format_VIDEOINFO</li><li>Format_VIDEOINFO2</li></ul> | | Interfaces de pin de entrada | <a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="ikspin.md"><strong>IKsPin</strong></a>, <a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig"><strong>IMixerPinConfig,</strong></a> <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (solo pin 0), <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>, <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a> | | Tipos de medios de pin de salida | MEDIATYPE_Video, MEDIASUBTYPE_Overlay | | Interfaces de pin de salida | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrar clsid | CLSID_OverlayMixer | | Página de propiedades CLSID | No hay ninguna página de propiedades. | | Archivos ejecutables | qdvd.dll | | <a href="merit.md">|</a> MERIT_DO_NOT_USE | | <a href="filter-categories.md">Categoría de</a> filtro | CLSID_LegacyAmFilterCategory | 




 

### <a name="remarks"></a>Comentarios

El cuadro de Mixer utiliza la clave de color de destino para mezclar superficies de vídeo con superposiciones. Corta la clave de color y el vídeo secundario a la superficie principal y envía el vídeo principal a la superficie superpuesta. A continuación, la tarjeta gráfica compone las dos superficies en su búfer de fotogramas.

Para probar si el controlador de gráficos admite la superposición de hardware, llame **a IDirectDraw7::GetCaps**. Si el **campo dwMaxVisibleOverlays** de la estructura **DDCAPS** es mayor que cero, el controlador admite la superposición de hardware.

Las aplicaciones pueden controlar algunos comportamientos en la interfaz Overlay Mixer a través de [**la interfaz IMixerPinConfig2.**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2) Los desarrolladores de juegos pueden usar el Mixer superposición para mostrar vídeo en el modo exclusivo de DirectDraw, como se describe más adelante en esta sección. Sin embargo, el filtro [de representador de](video-mixing-renderer-filter-9.md) mezcla de vídeo 9 (VMR-9) ahora proporciona una mejor compatibilidad con el vídeo en juegos. Para obtener más información, [vea Usar el representador de mezcla de vídeo.](using-the-video-mixing-renderer.md)

La siguiente información se proporciona en beneficio de los desarrolladores de filtros y los desarrolladores de juegos que desean usar el Mixer overlay en el modo exclusivo de DirectDraw.

**Operaciones internas Mixer superposición**

El objeto Overlay Mixer expone un pin de entrada para cada secuencia entrante. Normalmente, hay tres pines de entrada: pin 0 para los datos de vídeo y pins 1 y 2 para los datos de subimagen de DVD y línea 21. Internamente, el objeto Overlay Mixer crea un objeto DirectDraw con una superficie principal que comprende todo el escritorio, además de una superficie superpuesta cuyo rectángulo está definido por el tamaño de la secuencia de vídeo en el pin 0. Si el descodificador no especifica una clave de color, el Mixer de superposición usa claves de color predeterminadas: gris oscuro para tarjetas gráficas más recientes y rojo para tarjetas antiguas de 256 colores.

> [!Note]  
> Los resultados no están definidos si el descodificador entrega dos secuencias de vídeo secundarias simultáneamente en el mismo lugar en la superficie superpuesta. (Esto sucede a veces con DVD que contienen secuencias de subimagen y línea 21). El vídeo podría parpadear o mostrar solo una de las secuencias.

 

En Windows Vista o versiones posteriores, el Mixer superposición deshabilita la Administrador de ventanas de escritorio (DWM) si el controlador de pantalla admite la superposición de hardware. Las aplicaciones deben evitar el uso del filtro overlay Mixer; use vmr-9 o representador de vídeo mejorado (EVR) en su lugar.

**Conexión ascendente con el descodificador de vídeo**

Normalmente, las Mixer de entrada de overlay se conectan a un descodificador de vídeo ascendente. La secuencia de vídeo principal debe conectarse al pin 0. Las secuencias de línea 21 o subpicture se conectan al pin 1 o superior. Si el descodificador es un descodificador de software que usa exclusivamente la CPU del host, la conexión entre el descodificador y el pin 0 es una [**conexión IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) Si el descodificador usa la aceleración de hardware, la conexión al pin 0 debe usar el inferir [**IAMVideoAccelerator.**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) Estos dos tipos de conexiones son mutuamente excluyentes.

Si el descodificador dibuja directamente en la superficie superpuesta, debe usar la interfaz [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) en el pin 0 e implementar la [**interfaz IOverlayNotify.**](/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify)

Los filtros que encapsulan un descodificador de hardware y se conectan a la interfaz overlay Mixer a través de un puerto de vídeo deben implementar la [**interfaz IVPConfig.**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) La interfaz Overlay Mixer implementa la [**interfaz IVPNotify.**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) Estas dos interfaces permiten al descodificador especificar las superficies superpuestas que necesita y habilitan el Mixer de superposición para informar al descodificador de la ubicación de esas superficies en la memoria de vídeo.

La propiedad Overlay Mixer garantiza que el rectángulo de vídeo se escale correctamente. La captura de vídeo implica ciertos problemas con respecto al escalado de la imagen de vista previa y la captura de fotogramas de vídeo intercalados. Si está desarrollando un filtro o un controlador WDM para un dispositivo de captura de vídeo de hardware, consulte las páginas de referencia [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) e [**IVPNotify**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) para obtener más información sobre estos temas.

El archivo overlay Mixer no se usa en escenarios de captura USB o 1394. Se usa en la captura de vídeo a través del bus PCI.

**Conexión de nivel inferior con el representador de vídeo**

El panel Mixer superposición tiene un pin de salida que se conecta al filtro [Representador de](video-renderer-filter.md) vídeo. En este caso, el representador de vídeo no representa el vídeo; simplemente administra la ventana de vídeo.

La conexión de pin usa [**la interfaz IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) en lugar de [**la interfaz IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) El representador de vídeo pasa su identificador de ventana a Mixer a DirectDraw, que administra el recorte del rectángulo. Las aplicaciones pueden controlar el representador de vídeo a través de las interfaces [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2) en filter Graph Manager.

**Modo exclusivo de DirectDraw**

El modo exclusivo DirectDraw Mixer overlay permite que los juegos muestren vídeo en alguna parte de la pantalla. En este modo, el elemento Overlay Mixer representa el vídeo directamente en una superficie de DirectDraw creada por la aplicación de juego, en lugar de en una ventana proporcionada por el representador de vídeo. Esto permite a los juegos controlar la clave de color. El Mixer superposición expone solo un pin de entrada en modo exclusivo de DirectDraw, lo que significa que no se puede realizar ninguna combinación de subpicura de línea 21 o DVD en este modo.

Para usar el Mixer superposición en modo exclusivo de DirectDraw, cree una instancia de overlay Mixer y consulte la interfaz [**IDDrawExclModeVideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo) antes de compilar el gráfico de filtros. A [**continuación, llame a IDDrawExclModeVideo::SetDDrawSurface para**](/windows/desktop/api/Strmif/nf-strmif-iddrawexclmodevideo-setddrawsurface) especificar la superficie de DirectDraw para la representación. Una limitación significativa de este modo es que el juego no obtiene acceso a los bits de vídeo reales. Si usa **IDDrawExclModeVideo,** la aplicación crea la superficie principal y el objeto Overlay Mixer la superficie superpuesta.

También puede usar el modo exclusivo de DirectDraw para realizar la representación sin ventanas (por ejemplo, en una página web), pero esto no se recomienda, ya que el Mixer de superposición no realiza ninguna combinación en este modo. Esto significa que no se puede mostrar ningún dato de línea 21 ni subimagen.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




