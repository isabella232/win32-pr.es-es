---
description: Filtro de captura de audio
ms.assetid: f76d5c82-33b2-4579-9420-8f97eca53ede
title: Filtro de captura de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a630452565fafad3c4a4420154efd8fe6b282f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162221"
---
# <a name="audio-capture-filter"></a>Filtro de captura de audio

El filtro Captura de audio representa un dispositivo de captura de audio. Tiene un pin de salida de captura y varios pines de entrada (uno para cada tipo de entrada en la tarjeta, como Entrada de línea, Micrófono, CD y MIDI).

Este filtro puede funcionar con más de un dispositivo de hardware, por lo que llamar a CoCreateInstance para crear el filtro no funciona. En su lugar, use [el enumerador de dispositivos del sistema](system-device-enumerator.md). El enumerador de dispositivos del sistema devuelve un moniker único para cada dispositivo. El nombre descriptivo del moniker corresponde al nombre del dispositivo. (Este es el nombre que aparece en GraphEdit). Para obtener más información, [vea Enumerar dispositivos y filtros.](enumerating-devices-and-filters.md)



| Etiqueta | Value |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMAudioInputMixer,**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) [**IAMFilterMiscFlags,**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)IPersistPropertyBag, ISpecifyPropertyPages                                                               |
| Tipos de medios de pin de entrada                    | MEDIATYPE \_ AnalogAudio, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                                                                         |
| Interfaces de pin de entrada                     | [**IAMAudioInputMixer,**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                           |
| Tipos de medios de pin de salida                   | MEDIATYPE \_ Audio, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                                                                               |
| Interfaces de pin de salida                    | [**IAMBufferNegotiation,**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation) [**IAMPushSource,**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IKsPropertySet**](ikspropertyset.md), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtrar CLSID                             | No aplicable                                                                                                                                                                                                                                                                                     |
| CLSID de la página de propiedades                      | CLSID \_ AudioInputMixerProperties                                                                                                                                                                                                                                                                   |
| Executable                               | qcap.dll                                                                                                                                                                                                                                                                                           |
| [Mérito](merit.md)                       | NO USE EL VALOR DE NO \_ \_ \_ USE.                                                                                                                                                                                                                                                                                |
| [Categoría de filtro](filter-categories.md) | CLSID \_ AudioInputDeviceCategory                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Observaciones

Los pines de entrada representan conexiones de hardware físico y nunca se conectan a otros filtros de DirectShow.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Captura de audio](audio-capture.md)
</dt> </dl>

 

 



