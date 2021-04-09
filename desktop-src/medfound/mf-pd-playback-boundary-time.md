---
description: Almacena el tiempo (en unidades 100-nanosegundos) en el que debe comenzar la presentación, en relación con el inicio del origen del medio.
ms.assetid: 7a3dddad-067b-46af-9ed9-4ccc65f9d772
title: MF_PD_PLAYBACK_BOUNDARY_TIME atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22abadb4e0148a2079a9a7387e43599f4f79b8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083370"
---
# <a name="mf_pd_playback_boundary_time-attribute"></a>\_Atributo de \_ tiempo de límite de reproducción MF PD \_ \_

Almacena el tiempo (en unidades 100-nanosegundos) en el que debe comenzar la presentación, en relación con el inicio del origen del medio.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Se aplica a

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Observaciones

El \_ atributo de tiempo de límite de reproducción MF PD \_ \_ \_ es opcional para los orígenes multimedia de una lista de reproducción. Este valor indica la hora de inicio real de la presentación. Considere una lista de reproducción que incluye los orígenes de medios *Element1*, *elemento2* y *Element3* en una secuencia. 15 segundos después de que se reproduzca *elemento1* , se produce un cambio de flujo dinámico. La nueva secuencia debe empezar a reproducir 15 segundos en la presentación. Sin embargo, el fotograma clave más cercano al tiempo de presentación de 15 segundos es de 12 segundos para la nueva secuencia. Para iniciar la nueva presentación en 15 segundos, se requiere un signo para que las muestras descodificadas se quiten de 12 segundos a 15 segundos.

Antes de la transición, el origen del medio genera el evento [MENewPresentation](menewpresentation.md) . Esto devuelve el descriptor de presentación que contiene el atributo de ID. de [ \_ elemento de \_ reproducción \_ \_ MF PD](mf-pd-playback-element-id.md) para Element1. Además, contiene el atributo de \_ tiempo de límite de reproducción MF PD \_ \_ \_ que se establece en 15 segundos para indicar el momento en que se produjo la transición. El origen multimedia realiza el marcado en 15 segundos después de la descodificación, lo que evita que se muestren los fotogramas de 12 segundos a 15 segundos.

Este valor solo afecta a Marking Time y no afecta al modo en que la sesión multimedia ajusta las marcas de tiempo. Este atributo se omite a menos que el origen de medios indique a través del atributo de [ \_ \_ \_ \_ ID. de elemento de reproducción MF PD](mf-pd-playback-element-id.md) que esta presentación es el mismo elemento de reproducción que el anterior.

El \_ atributo de tiempo de límite de reproducción MF PD \_ \_ \_ es similar al atributo [MF \_ TOPONODE \_ MEDIASTART](mf-toponode-mediastart-attribute.md) que se establece en el nodo de la topología. En el caso de las aplicaciones que se ejecutan en Windows Vista, los orígenes multimedia que implementan [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) deben usar **MF \_ TOPONODE \_ MEDIASTART** en lugar del tiempo de límite de reproducción de MF \_ PD \_ \_ \_ .

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

 

 




