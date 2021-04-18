---
description: Especifica si las topologías tienen una hora de inicio y de finalización global.
ms.assetid: 6810a22c-f091-423c-97dd-c04fdabdb9bb
title: MF_SESSION_GLOBAL_TIME atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b930ed47c5f314b12aba0075cdc9120d2179325
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716417"
---
# <a name="mf_session_global_time-attribute"></a>\_Atributo de \_ hora global de sesión MF \_

Especifica si las topologías tienen una hora de inicio y de finalización global.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Trata como un valor booleano.

## <a name="remarks"></a>Observaciones

Puede establecer este atributo al crear el sesison de medios mediante el parámetro *pConfiguration* de la función [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) o [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

Si este atributo está presente y es distinto de cero, todas las topologías que se pasan a la sesión multimedia deben tener los atributos [**de \_ \_ PROJECTSTOP de topología**](mf-topology-projectstop-attribute.md) [**MF \_ \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) y MF. Estos atributos especifican las horas de inicio y detención de la topología en relación con toda la presentación.

Si este atributo no está presente o **false**, las topologías no deben tener el atributo [**MF Topology \_ \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) o [**MF \_ Topology \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) .

Use este atributo para crear secuencias de edición. Para obtener más información, vea [tiempos de presentación de secuencias](sequence-presentation-times.md).

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de la sesión multimedia](media-session-attributes.md)
</dt> <dt>

[Tiempos de presentación de secuencia](sequence-presentation-times.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**\_PROJECTSTART de topología \_ MF**](mf-topology-projectstart-attribute.md)
</dt> <dt>

[**\_PROJECTSTOP de topología \_ MF**](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




