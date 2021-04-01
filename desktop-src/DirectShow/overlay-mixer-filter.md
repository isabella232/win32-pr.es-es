---
description: Filtro de mezclador de superposición
ms.assetid: e80938b7-31f0-467b-a3fa-c4511d14758d
title: Filtro de mezclador de superposición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26ad8ba8a41a1cdb94eec0f4406c4845f25cda5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906330"
---
# <a name="overlay-mixer-filter"></a>Filtro de mezclador de superposición

El filtro de mezclador de superposición es un representador de vídeo diseñado específicamente para reproducción de DVD y transmisión por secuencias de vídeo con subtítulos (CC) de línea 21. El mezclador de superposición también admite extensiones de puerto de vídeo (VPEs), lo que permite que funcione con descodificadores de hardware MPEG-2 o sintonizadores de TV analógicos que envían vídeo directamente a la tarjeta de gráficos, en lugar de a través del bus PCI.

> [!Note]  
> Ahora se prefiere el [procesador de mezcla de vídeo 9](video-mixing-renderer-filter-9.md) sobre el filtro de mezclador de superposición, excepto en escenarios VPE.

 

El mezclador de superposición utiliza DirectDraw para la representación. Requiere una superficie de superposición en la tarjeta gráfica. La secuencia de vídeo principal debe estar conectada al pin 0. Las secuencias secundarias (gráficos de subtítulos (CC) o de DVD) están conectadas a los pin 1 y superiores. El mezclador de superposición blits los flujos secundarios directamente en el superficie principal; no mezcla ni mezcla alfa.

El mezclador de superposición usa el representador de vídeo para la administración de ventanas. El representador de vídeo se conecta al pin de salida del mezclador de superposición.

Este filtro se agrega automáticamente al gráfico de filtros cuando las aplicaciones utilizan las interfaces [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) y [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) para crear el gráfico. El administrador de gráficos de filtro no agregará automáticamente el mezclador de superposición al gráfico.

> [!Note]  
> En la tabla siguiente, los subtipos de medios aceptados en el PIN de entrada 0 dependen del hardware. El mezclador de superposición no puede determinar si se admite un subtipo determinado hasta que cree la superficie de DirectDraw. Por lo tanto, la única forma de un filtro de nivel superior para determinar si se admite un subtipo es intentar una conexión con ese subtipo.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a>, <a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>, <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de entrada</td>
<td>Tipo principal: MEDIATYPE_Video<br/> Subtipos<br/>
<ul>
<li>MEDIASUBTYPE_Overlay (solo pin 0)</li>
<li>Formatos YUV de DirectDraw (solo pin 0)</li>
<li>Formatos de aceleración de vídeo de DirectDraw (solo pin 0)</li>
<li>Formatos RGB de DirectDraw (todos los pin de entrada)</li>
</ul>
Tipos de formato:<br/>
<ul>
<li>Format_VIDEOINFO</li>
<li>Format_VIDEOINFO2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de PIN de entrada</td>
<td><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="ikspin.md"><strong>IKsPin</strong></a>, <a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig"><strong>IMixerPinConfig</strong></a>, <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (solo pin 0), <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>, <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de salida</td>
<td>MEDIATYPE_Video, MEDIASUBTYPE_Overlay</td>
</tr>
<tr class="odd">
<td>Interfaces de clavija de salida</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Identificador CLSID</td>
<td>CLSID_OverlayMixer</td>
</tr>
<tr class="odd">
<td>CLSID de la página de propiedades</td>
<td>Ninguna página de propiedades.</td>
</tr>
<tr class="even">
<td>Executable</td>
<td>qdvd.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Fundament</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoría de filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

### <a name="remarks"></a>Observaciones

El mezclador de superposición usa la clave de color de destino para mezclar las superficies de vídeo con las superposiciones. Blits la clave de color y el vídeo secundario en la superficie primaria y envía el vídeo principal a la superficie de superposición. A continuación, la tarjeta de gráficos compone las dos superficies en su búfer de fotogramas.

Para probar si el controlador de gráficos admite la superposición de hardware, llame a **IDirectDraw7:: GetCaps**. Si el campo **dwMaxVisibleOverlays** de la estructura **DDCAPS** es mayor que cero, el controlador admite la superposición de hardware.

Las aplicaciones pueden controlar algunos comportamientos en el mezclador de superposición a través de la interfaz [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2) . Los desarrolladores de juegos pueden usar el mezclador de superposición para mostrar vídeo en modo exclusivo de DirectDraw, como se describe más adelante en esta sección. El [filtro de representador de mezcla de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9) ahora proporciona una mejor compatibilidad con el vídeo en juegos. Para obtener más información, vea [usar el representador de mezcla de vídeo](using-the-video-mixing-renderer.md).

La siguiente información se proporciona para la ventaja de los desarrolladores de filtros y los desarrolladores de juegos que desean usar el mezclador de superposición en el modo exclusivo de DirectDraw.

**Operaciones internas del mezclador de superposición**

El mezclador de superposición expone un PIN de entrada para cada flujo entrante. Normalmente, hay tres clavijas de entrada: pin 0 para los datos de vídeo y los pin 1 y 2 para los datos de la línea 21 y el DVD. Internamente, el mezclador de superposición crea un objeto DirectDraw con una superficie primaria que incluye todo el escritorio, además de una superficie superpuesta cuyo rectángulo se define por el tamaño de la secuencia de vídeo en el pin 0. Si el descodificador no especifica una clave de color, el mezclador de superposición usa las teclas de color predeterminadas: gris oscuro para tarjetas gráficas más recientes y magenta para tarjetas de 256 colores anteriores.

> [!Note]  
> Los resultados son indefinidos si el descodificador entrega dos secuencias de vídeo secundarias simultáneamente en el mismo lugar en la superficie de superposición. (En ocasiones, esto ocurre con los DVDs que contienen secuencias de subimagen y de línea 21). El vídeo puede parpadear o mostrar solo una de las secuencias.

 

En Windows Vista o posterior, el mezclador de superposición deshabilita la composición Administrador de ventanas de escritorio (DWM) si el controlador de pantalla admite la superposición de hardware. Las aplicaciones deben evitar el uso del filtro de mezclador de superposición. en su lugar, use VMR-9 o el representador de vídeo mejorado (EVR).

**Conexión ascendente con el descodificador de vídeo**

Normalmente, los pines de entrada del mezclador de superposición se conectan a un descodificador de vídeo de nivel superior. La secuencia de vídeo principal debe conectarse al pin 0. La línea 21 o las secuencias de subimagen se conectan al pin 1 o superior. Si el descodificador es un descodificador de software que usa la CPU del host exclusivamente, la conexión entre el descodificador y el pin 0 es una conexión de [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) . Si el descodificador utiliza la aceleración de hardware, la conexión al pin 0 debe utilizar el [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) interfaz. Estos dos tipos de conexiones se excluyen mutuamente.

Si el descodificador dibuja directamente en la superficie de superposición, debe usar la interfaz [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) en el pin 0 e implementar la interfaz [**IOverlayNotify**](/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify) .

Los filtros que ajustan un descodificador de hardware y se conectan al mezclador de superposición a través de un puerto de vídeo deben implementar la interfaz [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) . El mezclador de superposición implementa la interfaz [**IVPNotify**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) . Estas dos interfaces permiten al descodificador especificar las superficies superpuestas que requiere y permiten que el mezclador de superposición informe al descodificador de la ubicación de esas superficies en la memoria de vídeo.

El mezclador de superposición también garantiza que el rectángulo de vídeo se escale correctamente. La captura de vídeo implica determinados problemas con respecto a la escala de la imagen de vista previa y la captura de fotogramas de vídeo intercalados. Si va a desarrollar un filtro o un controlador WDM para un dispositivo de captura de vídeo de hardware, consulte las páginas de referencia de [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) y [**IVPNotify**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) para obtener más información sobre estos temas.

El mezclador de superposición no se utiliza en los escenarios de captura de 1394 o USB. Se usa en la captura de vídeo a través del bus PCI.

**Conexión de nivel inferior con el representador de vídeo**

El mezclador de superposición tiene un PIN de salida que se conecta al filtro de [representador de vídeo](video-renderer-filter.md) . En este caso, el representador de vídeo no representa el vídeo; simplemente administra la ventana de vídeo.

La conexión de PIN usa la interfaz [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) en lugar de la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) . El representador de vídeo pasa el identificador de ventana a través del mezclador de superposición a DirectDraw, que administra el recorte del rectángulo. Las aplicaciones pueden controlar el representador de vídeo a través de las interfaces [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) y [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2) en el administrador de gráficos de filtro.

**Modo exclusivo de DirectDraw**

El modo exclusivo de DirectDraw del mezclador de superposición permite que los juegos muestren vídeo en alguna parte de la pantalla. En este modo, el mezclador de superposición representa el vídeo directamente en una superficie de DirectDraw creada por la aplicación de juego, en lugar de hacerlo en una ventana proporcionada por el representador de vídeo. Esto permite a los juegos controlar la clave del color. El mezclador de superposición solo expone un PIN de entrada en modo exclusivo de DirectDraw, lo que significa que no se puede realizar ninguna mezcla de subimagen de línea 21 o DVD en este modo.

Para usar el mezclador de superposición en modo exclusivo de DirectDraw, cree una instancia del mezclador de superposición y consulte la interfaz [**IDDrawExclModeVideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo) antes de generar el gráfico de filtro. A continuación, llame a [**IDDrawExclModeVideo:: SetDDrawSurface**](/windows/desktop/api/Strmif/nf-strmif-iddrawexclmodevideo-setddrawsurface) para especificar la superficie de DirectDraw para la representación. Una limitación importante de este modo es que el juego no obtiene acceso a los bits de vídeo reales. Si usa **IDDrawExclModeVideo**, la aplicación crea la superficie principal y el mezclador de superposición crea la superficie de superposición.

También puede usar el modo exclusivo de DirectDraw para realizar la representación sin ventana (por ejemplo, en una página web), pero no se recomienda porque el mezclador de superposición no realiza ninguna combinación en este modo. Esto significa que no se pueden mostrar los datos de la línea 21 o de la subimagen.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 




