---
description: El filtro Representador de vídeo mejorado (EVR) es un mezclador y representador de vídeo de 16 canales. Tiene la misma funcionalidad principal y el mismo modelo de complemento que el receptor Media Foundation multimedia EVR.
ms.assetid: ead99cb3-2be2-42c6-ac22-be0c2ddf28d5
title: Filtro de representador de vídeo mejorado
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96075ab9149cdf219971c5d1c321474de784aaa8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987898"
---
# <a name="enhanced-video-renderer-filter"></a>Filtro de representador de vídeo mejorado

> [!Note]  
> Este tema se aplica a Windows Vista y versiones posteriores.

 

El filtro Representador de vídeo mejorado (EVR) es un mezclador y representador de vídeo de 16 canales. Tiene la misma funcionalidad principal y el mismo modelo de complemento que el receptor Media Foundation multimedia EVR.

El DirectShow EVR se documenta en la documentación de Media Foundation SDK. Para obtener más información, vea [Representador de vídeo mejorado.](../medfound/enhanced-video-renderer.md)




| Etiqueta | Value |
|--------|-------|
| Interfaces de filtro (a través <strong>de QueryInterface)</strong> | DirectShow interfaces:<ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li><li><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>IMediaEventSink</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></li></ul>Media Foundation interfaces:<br /><ul><li><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a></li><li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></li><li><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a></li><li><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>RENDERERVideoRenderer</strong></a></li></ul> | 
| Tipos de medios de pin de entrada | Variable, según el controlador de gráficos. | 
| Interfaces de pin de entrada (a través <strong>de QueryInterface)</strong> | DirectShow interfaces:<ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li></ul>Media Foundation interfaces:<br /><ul><li><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a></li><li><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a></li><li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></li></ul> | 
| Tipos de medios de pin de salida | No es aplicable. | 
| Interfaces de pin de salida | No es aplicable. | 
| Filtrar CLSID | CLSID_EnhancedVideoRenderer | 
| Executable | evr.dll | 
| <a href="merit.md">Mérito</a> | MERIT_DO_NOT_USE | 
| <a href="filter-categories.md">Categoría de filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Observaciones

Además de las interfaces expuestas a través de **QueryInterface**, evr expone otras interfaces a través del [**método IMFGetService::GetService.**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) Algunas de estas interfaces las implementa el presentador de EVR o el mezclador de EVR, en lugar de la propia EVR. Si la aplicación establece un presentador o mezclador personalizado en la EVR, las versiones personalizadas pueden exponer un conjunto diferente de interfaces.



| Object     | Identificador de servicio                                              | Interfaces                                                                                                                                                                                                                                                                                                     |
|------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtro EVR | MR \_ VIDEO \_ RENDER \_ SERVICE(Queries EVR or presenter)<br/> | [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)<br/> [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)<br/>                                                          |
| Filtro EVR | MR \_ VIDEO \_ ACCELERATION \_ SERVICE(Queries presenter)<br/>  | [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)                                                                                                                                                                                                                                                      |
| Filtro EVR | SERVICIO MR \_ VIDEO \_ MIXER \_ (mezclador de consultas)<br/>             | [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)<br/> [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)<br/> [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**PROCESSORVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)<br/> |
| Pines de entrada | SERVICIO DE \_ \_ ACELERACIÓN DE \_ VÍDEO DE MR                                | [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                                                                                                                                                                                                    |



 

El EVR puede mezclar hasta 16 secuencias de vídeo. La primera secuencia de entrada (patilla 0) se denomina secuencia *de referencia.* La secuencia de referencia siempre aparece en primer lugar en el orden z. Las secuencias adicionales se denominan substreams y se mezclan encima de la secuencia de referencia. La aplicación puede cambiar el orden z de las substreams, pero ninguna substream puede ser la primera en el orden z.

El controlador de gráficos determina qué formatos de vídeo se admiten, pero normalmente se limitan a lo siguiente:

-   Secuencia de referencia: YUV progresiva o entrelazada sin alfa por píxel (como NV12 o YUY2); o RGB progresiva.
-   Substreams: YUV progresiva con alfa por píxel, como AYUV o AI44.

Los formatos de substream disponibles pueden depender del formato de la secuencia de referencia.

Los reenviadores EVR buscan comandos ascendentes a través del pin 0. Las patillas de substream no reenvía los comandos seek. Es responsabilidad del filtro de origen o divisor mantener las subdirecciones sincronizadas con la secuencia de referencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

