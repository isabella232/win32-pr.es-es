---
description: Administración de calidad de vídeo
ms.assetid: 3617adf2-ed7b-4788-abce-58bc22a14511
title: Administración de calidad de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d441178cd5b360bb9f8fb9bfc4d903fd9a5a3848
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479851"
---
# <a name="video-quality-management"></a>Administración de calidad de vídeo

En este tema se describen algunas mejoras en la canalización de vídeo de Windows 7, tanto para Microsoft Media Foundation como para Microsoft DirectShow.

En un mundo perfecto, el vídeo nunca tendría problemas, independientemente de la resolución de vídeo o la carga de CPU o GPU. En realidad, por supuesto, la canalización de vídeo debe ser capaz de hacer frente a recursos de hardware finitos y adaptar la reproducción de forma adaptable al entorno del sistema. Los objetivos de la administración de calidad de vídeo son:

-   Reducir problemas (fotogramas eliminados o en tiempo de retraso).
-   Reduzca el uso de memoria, especialmente en la GPU.
-   Reduzca el consumo de energía, especialmente en equipos portátiles que se ejecutan con batería.
-   Obtenga la mejor calidad de imagen posible, dadas las restricciones de recursos.
-   Mantenga el vídeo sincronizado con el audio.

Algunos de estos objetivos son contrarios, especialmente en los sistemas de gama baja. Por lo general, hay un equilibrio entre velocidad y calidad. Los problemas son más ofensivos que las reducciones moderadas de la calidad visual. La importancia relativa del consumo de energía varía con el entorno; en un portátil que se ejecuta con batería, es muy importante.

En Windows 7, el representador de vídeo mejorado (EVR) tiene una mejor compatibilidad con la administración de calidad de vídeo. Tanto la Media Foundation como la canalización DirectShow se han actualizado para aprovechar estas funcionalidades. Se usa un enfoque de dos opciones:

-   Antes de que se inicie la reproducción, la canalización puede realizar optimizaciones estáticas, en función de la configuración de administración de energía del usuario y la información sobre el hardware.
-   Una vez que se inicia la reproducción, la canalización puede aplicar optimizaciones dinámicas, en función del rendimiento en tiempo de ejecución.

## <a name="quality-management-in-media-foundation"></a>Administración de calidad en Media Foundation

Para habilitar las optimizaciones estáticas, establezca el atributo [MF \_ TOPOLOGY \_ STATIC PLAYBACK \_ \_ OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) en la topología parcial antes de resolver la topología. El cargador de topología consulta este atributo en su [**método IMFTopoLoader::Load.**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load)

Si habilita las optimizaciones estáticas, debe establecer otros dos atributos en la topología:



| Atributo                                                                                                                                      | Descripción                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="MF_TOPOLOGY_PLAYBACK_MAX_DIMS"></span><span id="mf_topology_playback_max_dims"></span>ATENUACIONES \_ MÁXIMAS DE \_ REPRODUCCIÓN DE \_ TOPOLOGÍA \_ DE MF<br/>   | Especifica el tamaño máximo de la ventana de reproducción de vídeo.<br/> |
| <span id="MF_TOPOLOGY_PLAYBACK_FRAMERATE"></span><span id="mf_topology_playback_framerate"></span>VELOCIDAD \_ DE FOTOGRAMAS DE \_ REPRODUCCIÓN DE \_ TOPOLOGÍA MF<br/> | Especifica la frecuencia de actualización del monitor.<br/>                      |



 

Estos dos atributos ayudan a la canalización a calcular la configuración más eficaz para la administración de calidad.

El administrador de calidad realiza optimizaciones dinámicas. No es necesario hacer nada para habilitar el administrador de calidad; se habilita automáticamente. El administrador de calidad existía en Windows Vista; en Windows 7, la EVR puede responder mejor a los mensajes del administrador de calidad.

## <a name="quality-management-in-directshow"></a>Administración de calidad en DirectShow

DirectShow optimizaciones estáticas y dinámicas para la reproducción de DVD. Para habilitar estas optimizaciones en una aplicación de reproducción de DVD, establezca las marcas siguientes en el parámetro *dwFlags* del método **IDvdGraphBuilder::RenderDvdVideoVolume:**



| Marca                  | Descripción                    |
|-----------------------|--------------------------------|
| AM \_ DVD \_ ADAPT \_ GRAPH | Habilita las optimizaciones estáticas.  |
| QOS \_ \_ DE DVD DE \_ AM     | Habilita las optimizaciones dinámicas. |



 

Otras DirectShow aplicaciones pueden habilitar optimizaciones dinámicas llamando al método [**IEVRFilterConfigEx::SetConfigPrefs**](/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-setconfigprefs) directamente en el filtro EVR. Especifique la **marca EVRFilterConfigPrefs \_ EnableQoS.**

> [!Note]  
> Las optimizaciones estáticas DirectShow se limitan a la reproducción de DVD.

 

## <a name="quality-management-in-the-evr"></a>Administración de calidad en la EVR

EvR admite algunas nuevas marcas de configuración para la administración de calidad. Si habilita las optimizaciones de administración de calidad descritas anteriormente, no tiene que establecer estas marcas directamente. Sin embargo, se documentan para las aplicaciones que desean un control más pormenorizados sobre la EVR.

Establezca las marcas siguientes en el mezclador EVR mediante una llamada al método [**IMFVideo MixerControl2::Set MixingPrefs:**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs)




| Marcas | Descripción | 
|-------|-------------|
| <ul><li><strong>MFVideoMixPrefs_ForceHalfInterlace</strong></li><li><strong>MFVideoMixPrefs_AllowDropToHalfInterlace</strong></li></ul> | Omita el segundo campo de cada fotograma entrelazado. | 
| <ul><li><strong>MFVideoMixPrefs_AllowDropToBob</strong></li><li><strong>MFVideoMixPrefs_ForceBob</strong></li></ul> | Use bob deinterlazado, incluso si el controlador admite un modo de desinterlace de mayor calidad. | 




 

Establezca las marcas siguientes en el presentador evr llamando al [**método IMFVideoDisplayControl::SetRenderingPrefs:**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs)




| Marcas | Descripción | 
|-------|-------------|
| <ul><li><strong>MFVideoRenderPrefs_ForceOutputThrottling</strong></li><li><strong>MFVideoRenderPrefs_AllowOutputThrottling</strong></li></ul> | Limite la salida para que coincida con el ancho de banda de GPU. | 
| <ul><li><strong>MFVideoRenderPrefs_ForceBatching</strong></li><li><strong>MFVideoRenderPrefs_AllowBatching</strong></li></ul> | Batch Direct3D Presenta llamadas. Esta optimización permite al sistema entrar en estados inactivos con más frecuencia, lo que puede reducir el consumo de energía. | 
| <ul><li>MFVideoRenderPrefs_ForceScaling</li><li>MFVideoRenderPrefs_AllowScaling</li></ul> | Realice la combinación de vídeo con un rectángulo más pequeño que el rectángulo de salida. Escale el resultado al tamaño de salida correcto. | 




 

Además, el receptor de medios EVR admite atributos de configuración que corresponden a cada una de estas marcas:

-   [EVRConfig \_ AllowBatching](evrconfig-allowbatching.md)
-   [EVRConfig \_ AllowDropToBob](evrconfig-allowdroptobob.md)
-   [EVRConfig \_ AllowDropToHalfInterlace](evrconfig-allowdroptohalfinterlace.md)
-   [EVRConfig \_ AllowScaling](evrconfig-allowscaling.md)
-   [EVRConfig \_ AllowDropToThrottle](evrconfig-allowdroptothrottle.md)
-   [EVRConfig \_ ForceBatching](evrconfig-forcebatching.md)
-   [EVRConfig \_ ForceBob](evrconfig-forcebob.md)
-   [EVRConfig \_ ForceHalfInterlace](evrconfig-forcehalfinterlace.md)
-   [EVRConfig \_ ForceScaling](evrconfig-forcescaling.md)
-   [EVRConfig \_ ForceThrottle](evrconfig-forcethrottle.md)

Antes de que se inicie la reproducción, puede establecer estos atributos directamente en el receptor de medios EVR, como alternativa a llamar a los métodos [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2) y [**IMFVideoDisplayControl.**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) Para establecer estos atributos, consulte el receptor de medios EVR [**paraATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesión multimedia](media-session.md)
</dt> </dl>

 

 




