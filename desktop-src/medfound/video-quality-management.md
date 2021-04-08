---
description: Administración de calidad de vídeo
ms.assetid: 3617adf2-ed7b-4788-abce-58bc22a14511
title: Administración de calidad de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233ccd54cfcb98742abef9a91241e903c07ba549
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001439"
---
# <a name="video-quality-management"></a>Administración de calidad de vídeo

En este tema se describen algunas mejoras de la canalización de vídeo en Windows 7, tanto para Microsoft Media Foundation como para Microsoft DirectShow.

En un mundo perfecto, el vídeo nunca se encontraría sin problemas, independientemente de la resolución de vídeo o la carga de CPU/GPU. En realidad, por supuesto, la canalización de vídeo debe ser capaz de hacer frente a los recursos de hardware finitos y debe adaptar de modo adaptable la reproducción al entorno del sistema. Los objetivos de administración de calidad de vídeo son:

-   Reduzca los problemas (fotogramas descartados o de última hora).
-   Reduzca el uso de memoria, especialmente en la GPU.
-   Reduzca el consumo de energía, especialmente en equipos portátiles que funcionen con batería.
-   Obtenga la mejor calidad de imagen posible, dadas las restricciones de recursos.
-   Mantenga el vídeo sincronizado con audio.

Algunos de estos objetivos son contrario, especialmente en los sistemas de low-end. Por lo general, hay un equilibrio entre la velocidad y la calidad. El problema es más objeción que las reducciones moderadas en la calidad visual. La importancia relativa del consumo de energía varía en función del entorno; en un portátil que funciona con batería, es muy importante.

En Windows 7, el representador de vídeo mejorado (EVR) ofrece una mejor compatibilidad con la administración de calidad de vídeo. Tanto la canalización de Media Foundation como la canalización de DirectShow se han actualizado para aprovechar estas capacidades. Se usa un enfoque de dos puntas:

-   Antes de que se inicie la reproducción, la canalización puede realizar optimizaciones estáticas, en función de la configuración de la administración de energía del usuario y de la información sobre el hardware.
-   Una vez iniciada la reproducción, la canalización puede aplicar optimizaciones dinámicas en función del rendimiento en tiempo de ejecución.

## <a name="quality-management-in-media-foundation"></a>Administración de calidad en Media Foundation

Para habilitar las optimizaciones estáticas, establezca el atributo de [ \_ \_ \_ \_ optimizaciones de reproducción estática de la topología MF](mf-topology-static-playback-optimizations.md) en la topología parcial antes de resolver la topología. El cargador de topología consulta este atributo en su método [**IMFTopoLoader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) .

Si habilita las optimizaciones estáticas, debe establecer otros dos atributos en la topología:



| Atributo                                                                                                                                      | Descripción                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="MF_TOPOLOGY_PLAYBACK_MAX_DIMS"></span><span id="mf_topology_playback_max_dims"></span>\_DiMS de reproducción de topologías \_ \_ máx \_ .<br/>   | Especifica el tamaño máximo de la ventana de reproducción de vídeo.<br/> |
| <span id="MF_TOPOLOGY_PLAYBACK_FRAMERATE"></span><span id="mf_topology_playback_framerate"></span>velocidad de reproducción de \_ topología MF \_ \_<br/> | Especifica la frecuencia de actualización del monitor.<br/>                      |



 

Estos dos atributos ayudan a la canalización a calcular el valor más eficaz para la administración de calidad.

El administrador de calidad realiza las optimizaciones dinámicas. No es necesario hacer nada para habilitar el administrador de calidad. se habilita automáticamente. El administrador de calidad existía en Windows Vista; en Windows 7, EVR puede responder mejor a los mensajes del administrador de calidad.

## <a name="quality-management-in-directshow"></a>Administración de calidad en DirectShow

DirectShow admite las optimizaciones estáticas y dinámicas para la reproducción de DVD. Para habilitar estas optimizaciones en una aplicación de reproducción de DVD, establezca las marcas siguientes en el parámetro *dwFlags* del método **IDvdGraphBuilder:: RenderDvdVideoVolume** :



| Marca                  | Descripción                    |
|-----------------------|--------------------------------|
| gráfico de la \_ adaptación del DVD \_ \_ | Habilita las optimizaciones estáticas.  |
| \_ \_ QoS EVR de \_ DVD     | Habilita las optimizaciones dinámicas. |



 

Otras aplicaciones de DirectShow pueden habilitar las optimizaciones dinámicas llamando al método [**IEVRFilterConfigEx:: SetConfigPrefs**](/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-setconfigprefs) directamente en el filtro EVR. Especifique la **marca \_ EnableQoS de EVRFilterConfigPrefs** .

> [!Note]  
> Las optimizaciones estáticas en DirectShow se limitan a la reproducción de DVD.

 

## <a name="quality-management-in-the-evr"></a>Administración de calidad en EVR

EVR admite algunas nuevas marcas de configuración para la administración de la calidad. Si habilita las optimizaciones de administración de calidad descritas anteriormente, no es necesario establecer estas marcas directamente. Sin embargo, están documentadas para las aplicaciones que quieren un control más granular sobre el EVR.

Establezca las marcas siguientes en el mezclador EVR llamando al método [**IMFVideoMixerControl2:: SetMixingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs) :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Marcas</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><strong>MFVideoMixPrefs_ForceHalfInterlace</strong></li>
<li><strong>MFVideoMixPrefs_AllowDropToHalfInterlace</strong></li>
</ul></td>
<td>Omitir el segundo campo de cada fotograma entrelazado.</td>
</tr>
<tr class="even">
<td><ul>
<li><strong>MFVideoMixPrefs_AllowDropToBob</strong></li>
<li><strong>MFVideoMixPrefs_ForceBob</strong></li>
</ul></td>
<td>Use el desentrelazado de Bob, incluso si el controlador admite un modo de desentrelazado de mayor calidad.</td>
</tr>
</tbody>
</table>



 

Establezca las marcas siguientes en el presentador EVR llamando al método [**IMFVideoDisplayControl:: SetRenderingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs) :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Marcas</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><strong>MFVideoRenderPrefs_ForceOutputThrottling</strong></li>
<li><strong>MFVideoRenderPrefs_AllowOutputThrottling</strong></li>
</ul></td>
<td>Limite la salida para que coincida con el ancho de banda de GPU.</td>
</tr>
<tr class="even">
<td><ul>
<li><strong>MFVideoRenderPrefs_ForceBatching</strong></li>
<li><strong>MFVideoRenderPrefs_AllowBatching</strong></li>
</ul></td>
<td>Llamadas presentes de Direct3D por lotes. Esta optimización permite al sistema entrar en Estados inactivos con más frecuencia, lo que puede reducir el consumo de energía.</td>
</tr>
<tr class="odd">
<td><ul>
<li>MFVideoRenderPrefs_ForceScaling</li>
<li>MFVideoRenderPrefs_AllowScaling</li>
</ul></td>
<td>Realice la combinación de vídeo con un rectángulo más pequeño que el rectángulo de salida. Escale el resultado al tamaño de salida correcto.</td>
</tr>
</tbody>
</table>



 

Además, el receptor de medios EVR admite atributos de configuración que se corresponden con cada una de estas marcas:

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

Antes de que se inicie la reproducción, puede establecer estos atributos directamente en el receptor de medios EVR, como alternativa a la llamada a los métodos [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2) y [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) . Para establecer estos atributos, consulte el receptor de medios EVR para [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesión de medios](media-session.md)
</dt> </dl>

 

 




