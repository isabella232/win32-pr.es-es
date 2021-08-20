---
description: Especifica la hora de inicio de las presentaciones que se ponen en cola después de la primera presentación.
ms.assetid: 087f5d61-b3e6-4fdf-98e6-b018de7b237f
title: MF_TOPOLOGY_START_TIME_ON_PRESENTATION_SWITCH atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67c691871593705f29875a7cfca9675e236bed329c81c6d886a37646bd6208dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875365"
---
# <a name="mf_topology_start_time_on_presentation_switch-attribute"></a>HORA \_ DE INICIO DE LA TOPOLOGÍA MF EN EL atributo PRESENTATION \_ \_ \_ \_ \_ SWITCH

Especifica la hora de inicio de las presentaciones que se ponen en cola después de la primera presentación.

## <a name="data-type"></a>Tipo de datos

**INT64 almacenado** como **UINT64**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Se aplica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Comentarios

Cuando la aplicación pone en cola la primera presentación en la sesión multimedia, la aplicación especifica la hora de inicio en el *parámetro pvarStartPosition* del método [**IMFMediaSession::Start.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) Sin embargo, para las presentaciones posteriores, la hora de inicio la asigna el atributo MF \_ TOPOLOGY \_ START TIME ON PRESENTATION SWITCH en la \_ \_ \_ \_ topología. La hora de inicio se especifica en unidades de 100 nanosegundos, con respecto al principio de la presentación. Por ejemplo, si el valor es 500000000, la reproducción comienza en 5 segundos en la presentación. Si no se establece este atributo, la hora de inicio predeterminada es cero.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de topología](topology-attributes.md)
</dt> </dl>

 

 




