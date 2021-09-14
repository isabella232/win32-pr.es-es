---
description: Contiene el identificador del elemento de lista de reproducción de la presentación.
ms.assetid: 355818cf-1e00-46ad-9ce1-ab3a178164f9
title: MF_PD_PLAYBACK_ELEMENT_ID atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 744a1d164c71cbd7eb8bb47ef12be68d47b8351d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263284"
---
# <a name="mf_pd_playback_element_id-attribute"></a>Atributo MF \_ PD \_ PLAYBACK ELEMENT \_ \_ ID

Contiene el identificador del elemento de lista de reproducción de la presentación.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Observaciones

Los orígenes multimedia que entregan listas de reproducción pueden establecer opcionalmente este atributo en sus descriptores de presentación.

Cuando un origen multimedia entrega una lista de reproducción, envía un evento [MENewPresentation](menewpresentation.md) para cada elemento de lista de reproducción después del primero. Este evento contiene un descriptor de presentación para el nuevo elemento de lista de reproducción. El origen de medios puede asignar identificadores a los elementos estableciendo el atributo MF PD PLAYBACK ELEMENT ID en cada descriptor de presentación, incluido el creado por \_ \_ \_ \_ [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).

Un origen multimedia también podría enviar el evento [MENewPresentation](menewpresentation.md) debido a un modificador de flujo dinámico o a un cambio en el número de secuencias. En esa situación, el valor de MF PD PLAYBACK ELEMENT ID debe ser el mismo en ambas presentaciones, para indicar que ambas presentaciones representan el mismo elemento de lista \_ \_ de \_ \_ reproducción. Si dos presentaciones consecutivas tienen el mismo valor para este atributo, la canalización Microsoft Media Foundation espera que las marcas de tiempo permanezcan continuas durante la transición. Por lo tanto, el origen de medios no debe usar el atributo [MF EVENT SOURCE ACTUAL \_ \_ \_ \_ START](mf-event-source-actual-start-attribute.md) cuando se pasa a la siguiente presentación.

Los orígenes multimedia que implementan [**MFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) deben usar el atributo [MF \_ TOPONODE \_ SEQUENCE \_ ELEMENTID](mf-toponode-sequence-elementid-attribute.md) en lugar del atributo MF \_ PD PLAYBACK ELEMENT \_ \_ \_ ID.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del descriptor de presentación](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




