---
description: Especifica si las topologías tienen una hora de inicio y de detenerse global.
ms.assetid: 6810a22c-f091-423c-97dd-c04fdabdb9bb
title: MF_SESSION_GLOBAL_TIME atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b930ed47c5f314b12aba0075cdc9120d2179325
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572785"
---
# <a name="mf_session_global_time-attribute"></a>Atributo MF \_ SESSION \_ GLOBAL \_ TIME

Especifica si las topologías tienen una hora de inicio y de detenerse global.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como un valor booleano.

## <a name="remarks"></a>Observaciones

Puede establecer este atributo al crear la sesison multimedia mediante el parámetro *pConfiguration* de la función [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) o [**MFCreatePMPMediaSession.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)

Si este atributo está presente y es distinto de cero, todas las topologías que se pasan a la sesión multimedia deben tener los atributos [**MF \_ TOPOLOGY \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) y [**MF \_ TOPOLOGY \_ PROJECTSTOP.**](mf-topology-projectstop-attribute.md) Estos atributos especifican las horas de inicio y de detección de la topología en relación con toda la presentación.

Si este atributo no está presente o **es FALSE,** las topologías no deben tener el atributo [**MF \_ TOPOLOGY \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) o [**MF \_ TOPOLOGY \_ PROJECTSTOP.**](mf-topology-projectstop-attribute.md)

Use este atributo para crear secuencias de edición. Para obtener más información, vea [Tiempos de presentación de secuencia.](sequence-presentation-times.md)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de sesión multimedia](media-session-attributes.md)
</dt> <dt>

[Tiempos de presentación de secuencia](sequence-presentation-times.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**MF \_ TOPOLOGY \_ PROJECTSTART**](mf-topology-projectstart-attribute.md)
</dt> <dt>

[**PROYECTOS \_ DE TOPOLOGÍA \_ MFTOP**](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




