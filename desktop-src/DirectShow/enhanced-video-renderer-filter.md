---
description: El filtro de representador de vídeo mejorado (EVR) es un representador y mezclador de vídeo de 16 canales. Tiene la misma funcionalidad principal y el mismo modelo de complemento que el Media Foundation receptor de medios EVR.
ms.assetid: ead99cb3-2be2-42c6-ac22-be0c2ddf28d5
title: Filtro de representador de vídeo mejorado
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ba6e7c14386ea37424364274263859844182ed7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079978"
---
# <a name="enhanced-video-renderer-filter"></a>Filtro de representador de vídeo mejorado

> [!Note]  
> Este tema se aplica a Windows Vista y versiones posteriores.

 

El filtro de representador de vídeo mejorado (EVR) es un representador y mezclador de vídeo de 16 canales. Tiene la misma funcionalidad principal y el mismo modelo de complemento que el Media Foundation receptor de medios EVR.

El filtro EVR de DirectShow se documenta en la documentación del SDK de Media Foundation; para obtener más información, vea [representador de vídeo mejorado](../medfound/enhanced-video-renderer.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro (a través de <strong>QueryInterface</strong>)</td>
<td>Interfaces de DirectShow:
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li>
<li><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>IMediaEventSink</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></li>
</ul>
Interfaces de Media Foundation:<br/>
<ul>
<li><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a></li>
<li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></li>
<li><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a></li>
<li><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de entrada</td>
<td>Variable, dependiendo del controlador de gráficos.</td>
</tr>
<tr class="odd">
<td>Interfaces de PIN de entrada (a través de <strong>QueryInterface</strong>)</td>
<td>Interfaces de DirectShow:
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li>
</ul>
Interfaces de Media Foundation:<br/>
<ul>
<li><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a></li>
<li><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a></li>
<li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de salida</td>
<td>No es aplicable.</td>
</tr>
<tr class="odd">
<td>Interfaces de clavija de salida</td>
<td>No es aplicable.</td>
</tr>
<tr class="even">
<td>Identificador CLSID</td>
<td>CLSID_EnhancedVideoRenderer</td>
</tr>
<tr class="odd">
<td>Executable</td>
<td>evr.dll</td>
</tr>
<tr class="even">
<td><a href="merit.md">Fundament</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="odd">
<td><a href="filter-categories.md">Categoría de filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Además de las interfaces expuestas a través de **QueryInterface**, el EVR expone otras interfaces a través del método [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) . Algunas de estas interfaces las implementa el presentador EVR o el mezclador EVR, en lugar del propio EVR. Si la aplicación establece un presentador o mezclador personalizado en EVR, las versiones personalizadas podrían exponer un conjunto de interfaces diferente.



| Object     | Identificador de servicio                                              | Interfaces                                                                                                                                                                                                                                                                                                     |
|------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtro de EVR | \_ \_ \_ Servicio de representación de vídeo Mr (consultas EVR o Presenter)<br/> | [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)<br/> [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)<br/>                                                          |
| Filtro de EVR | \_Servicio de aceleración de vídeo Mr \_ \_ (presentador de consultas)<br/>  | [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)                                                                                                                                                                                                                                                      |
| Filtro de EVR | \_Servicio de mezclador de vídeo Mr \_ \_ (mezclador de consultas)<br/>             | [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)<br/> [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)<br/> [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)<br/> |
| Clavijas de entrada | \_servicio de \_ aceleración de vídeo Mr \_                                | [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                                                                                                                                                                                                    |



 

EVR puede mezclar hasta 16 secuencias de vídeo. El primer flujo de entrada (pin 0) se denomina *flujo de referencia*. El flujo de referencia siempre aparece primero en el orden z. Los flujos adicionales se denominan subsecuencias y se mezclan en la parte superior de la secuencia de referencia. La aplicación puede cambiar el orden z de las subsecuencias, pero no puede haber ningún subflujo en primer lugar en el orden z.

El controlador de gráficos determina qué formatos de vídeo se admiten, pero normalmente se limitan a lo siguiente:

-   Secuencia de referencia: YUV progresivo o entrelazado sin alfa por píxel (como NV12 o YUY2); o RGB progresivo.
-   Subsecuencias: YUV progresivo con alfa por píxel, como AYUV o AI44.

Los formatos de subflujo disponibles pueden depender del formato del flujo de referencia.

EVR reenvía los comandos de búsqueda hacia arriba a través del PIN 0. Los pin de subsecuencia no reenvían los comandos de búsqueda. Es responsabilidad del filtro de origen o divisor mantener las subsecuencias sincronizadas con la secuencia de referencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

