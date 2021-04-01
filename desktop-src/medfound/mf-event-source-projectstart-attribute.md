---
description: Especifica la hora de inicio de una topología de segmento.
ms.assetid: d8902fb6-c758-4d3d-9230-e918948bda19
title: MF_EVENT_SOURCE_PROJECTSTART atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 512e2129c3104d9e7160163f03a9c28b2716273e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913734"
---
# <a name="mf_event_source_projectstart-attribute"></a>\_ \_ PROJECTSTART atributo de origen de evento MF \_

Especifica la hora de inicio de una topología de segmento.

## <a name="data-type"></a>Tipo de datos

**UINT64**

Trata como un valor de **LONGLONG** .

## <a name="remarks"></a>Observaciones

Este atributo se usa con el evento [MESourceStarted](mesourcestarted.md) . El origen del secuenciador establece este atributo cuando la topología del segmento actual tiene el atributo [**\_ \_ PROJECTSTART de la topología MF**](mf-topology-projectstart-attribute.md) . Los dos atributos tienen el mismo valor.

Este atributo es un valor con signo, aunque se almacena como **UINT64**.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de eventos](event-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




