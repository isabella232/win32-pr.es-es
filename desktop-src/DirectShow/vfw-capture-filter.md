---
description: Filtro de captura vfw
ms.assetid: 663b6b3b-2a50-4586-9506-600a59869abe
title: Filtro de captura vfw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eadc2c8a22ed6e00ff76d79a0b7ce2db012abb4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160090"
---
# <a name="vfw-capture-filter"></a>Filtro de captura vfw

Este filtro funciona con hardware de captura de vídeo anterior que usa Video For Windows.

Este filtro tiene dos pines de salida. Una se denomina Captura y la otra se denomina Vista previa o Superposición.



| Etiqueta | Value |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | **IPersistPropertyBag**, [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs), [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **ISpecifyPropertyPages**, [**IOverlayNotify**](/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Tipos de medios de pin de entrada                    | No aplicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Interfaces de pin de entrada                     | No aplicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Tipos de medios de pin de salida                   | Captura: MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL, FORMAT \_ VideoInfoOverlay: MEDIATYPE \_ Video, MEDIASUBTYPE \_ Overlay, FORMAT \_ VideoInfo<br/> Versión preliminar: MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL, FORMAT \_ VideoInfo<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Interfaces de pin de salida                    | Pin de captura: [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation), [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes), [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource), [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IKsPropertySet**](ikspropertyset.md), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)Overlay Pin: [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IKsPropertySet**](ikspropertyset.md), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> Pin de vista previa: [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource), [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IKsPropertySet**](ikspropertyset.md), [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> |
| Filtrar CLSID                             | CLSID \_ VfwCapture                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| CLSID de la página de propiedades                      | CLSID \_ CaptureProperties                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Executable                               | qcap.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Mérito](merit.md)                       | NO USE EL VALOR DE NO \_ \_ \_ USE.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [Categoría de filtro](filter-categories.md) | CLSID \_ VideoInputDeviceCategory                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a>Observaciones

Aunque el pin de captura expone la [**interfaz IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) solo se implementan los métodos **SetFormat** y **GetFormat** para esta interfaz.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 




