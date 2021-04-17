---
description: Contiene el identificador del elemento de lista de reproducción en la presentación.
ms.assetid: 355818cf-1e00-46ad-9ce1-ab3a178164f9
title: MF_PD_PLAYBACK_ELEMENT_ID atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 744a1d164c71cbd7eb8bb47ef12be68d47b8351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659981"
---
# <a name="mf_pd_playback_element_id-attribute"></a>\_Atributo de \_ \_ \_ ID. de elemento de reproducción MF PD

Contiene el identificador del elemento de lista de reproducción en la presentación.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Observaciones

Los orígenes multimedia que ofrecen listas de reproducción pueden establecer opcionalmente este atributo en los descriptores de presentación.

Cuando un origen multimedia entrega una lista de reproducción, envía un evento [MENewPresentation](menewpresentation.md) para cada elemento de lista de reproducción después de la primera. Este evento contiene un descriptor de presentación para el nuevo elemento de lista de reproducción. El origen multimedia puede asignar identificadores a los elementos mediante el establecimiento del \_ \_ \_ atributo ID del elemento de reproducción MF PD \_ en cada descriptor de presentación, incluido el creado por [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).

Un origen multimedia también puede enviar el evento [MENewPresentation](menewpresentation.md) debido a un cambio de flujo dinámico o un cambio en el número de secuencias. En esa situación, el valor del \_ identificador de elemento de reproducción MF PD \_ \_ \_ debe permanecer igual en ambas presentaciones para indicar que ambas presentaciones representan el mismo elemento de lista de reproducción. Si dos presentaciones consecutivas tienen el mismo valor para este atributo, la canalización Microsoft Media Foundation espera que las marcas de tiempo sigan siendo continuas en la transición. Por lo tanto, el origen multimedia no debe usar el atributo de [ \_ \_ \_ \_ Inicio real del origen de eventos MF](mf-event-source-actual-start-attribute.md) cuando realiza la transición a la siguiente presentación.

Los orígenes de medios que implementan [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) deben usar el atributo de la [secuencia de MF \_ \_ \_ TOPONODE](mf-toponode-sequence-elementid-attribute.md) en lugar del \_ atributo de identificador de elemento de reproducción MF PD \_ \_ \_ .

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de descriptor de presentación](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




