---
description: Filtro de captura de audio
ms.assetid: f76d5c82-33b2-4579-9420-8f97eca53ede
title: Filtro de captura de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73da50653a4a159d30a6ca1b83ebc1f37a6de42c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806595"
---
# <a name="audio-capture-filter"></a>Filtro de captura de audio

El filtro de captura de audio representa un dispositivo de captura de audio. Tiene un PIN de salida de captura y varios PIN de entrada (uno para cada tipo de entrada en la tarjeta, como línea en, MIC, CD y MIDI).

Este filtro puede trabajar con más de un dispositivo de hardware, por lo que llamar a CoCreateInstance para crear el filtro no funciona. En su lugar, use el [enumerador de dispositivos del sistema](system-device-enumerator.md). El enumerador de dispositivos del sistema devuelve un moniker único para cada dispositivo. El nombre descriptivo del moniker corresponde al nombre del dispositivo. (Este es el nombre que aparece en GraphEdit). Para obtener más información, vea [enumerar dispositivos y filtros](enumerating-devices-and-filters.md).



|                                          |                                                                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer), [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages                                                               |
| Tipos de medios de anclaje de entrada                    | MEDIATYPE \_ AnalogAudio, MEDIASUBTYPE \_ null                                                                                                                                                                                                                                                         |
| Interfaces de PIN de entrada                     | [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                           |
| Tipos de medios de anclaje de salida                   | MEDIATYPE \_ audio, MEDIASUBTYPE \_ null                                                                                                                                                                                                                                                               |
| Interfaces de clavija de salida                    | [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation), [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource), [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IKsPropertySet**](ikspropertyset.md), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Identificador CLSID                             | No aplicable                                                                                                                                                                                                                                                                                     |
| CLSID de la página de propiedades                      | CLSID \_ AudioInputMixerProperties                                                                                                                                                                                                                                                                   |
| Executable                               | qcap.dll                                                                                                                                                                                                                                                                                           |
| [Fundament](merit.md)                       | MÉRITO \_ \_ no se \_ usa                                                                                                                                                                                                                                                                                |
| [Categoría de filtro](filter-categories.md) | CLSID \_ AudioInputDeviceCategory                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Observaciones

Los pin de entrada representan las conexiones de hardware físico y nunca se conectan a otros filtros de DirectShow.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[Captura de audio](audio-capture.md)
</dt> </dl>

 

 



