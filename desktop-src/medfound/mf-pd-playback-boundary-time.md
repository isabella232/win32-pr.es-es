---
description: Almacena la hora (en unidades de 100 nanosegundos) a la que debe comenzar la presentación, con respecto al inicio del origen multimedia.
ms.assetid: 7a3dddad-067b-46af-9ed9-4ccc65f9d772
title: MF_PD_PLAYBACK_BOUNDARY_TIME atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22abadb4e0148a2079a9a7387e43599f4f79b8bb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257796"
---
# <a name="mf_pd_playback_boundary_time-attribute"></a>Atributo MF \_ PD \_ PLAYBACK BOUNDARY \_ \_ TIME

Almacena la hora (en unidades de 100 nanosegundos) a la que debe comenzar la presentación, con respecto al inicio del origen multimedia.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Se aplica a

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Observaciones

El atributo MF \_ PD PLAYBACK BOUNDARY TIME es opcional para los orígenes multimedia de una lista de \_ \_ \_ reproducción. Este valor indica la hora de inicio real de la presentación. Considere una lista de reproducción que incluya los orígenes *multimedia Element1,* *Element2* y *Element3* en una secuencia. 15 segundos después de que *element1* empiece a reproducirse, se produce un cambio de flujo dinámico. La nueva secuencia debe empezar a reproducirse 15 segundos en la presentación. Sin embargo, el fotograma clave más cercano al tiempo de presentación de 15 segundos es de 12 segundos para la nueva secuencia. Para iniciar la nueva presentación en 15 segundos, se requiere un markin para que las muestras descodificadas se desasocien de 12 segundos a 15 segundos.

Antes de la transición, el origen multimedia genera el evento [MENewPresentation.](menewpresentation.md) Esto devuelve el descriptor de presentación que contiene el atributo [MF PD PLAYBACK ELEMENT \_ \_ \_ \_ ID](mf-pd-playback-element-id.md) para *Element1*. Además, contiene el atributo MF PD PLAYBACK BOUNDARY TIME establecido en 15 segundos para indicar la hora a la que se produjo \_ \_ la \_ \_ transición. El origen multimedia realiza el markin a los 15 segundos después de la decodación, lo que impide que se muestren los fotogramas de 12 a 15 segundos.

Este valor solo afecta a la hora markin y no afecta a cómo la sesión multimedia ajusta las marcas de tiempo. Este atributo se omite a menos que el origen multimedia indique a través del atributo [MF PD PLAYBACK ELEMENT \_ \_ \_ \_ ID](mf-pd-playback-element-id.md) que esta presentación es el mismo elemento de reproducción que el anterior.

El atributo MF PD PLAYBACK BOUNDARY TIME es similar al atributo \_ \_ MF \_ \_ [ \_ TOPONODE \_ MEDIASTART](mf-toponode-mediastart-attribute.md) que se establece en el nodo de topología. Para las aplicaciones que se ejecutan en Windows Vista, los orígenes multimedia que implementan [**MFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) deben usar **MF \_ TOPONODE \_ MEDIASTART** en lugar de MF \_ PD PLAYBACK BOUNDARY \_ \_ \_ TIME.

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

 

 




