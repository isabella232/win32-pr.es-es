---
description: Cuando un origen multimedia solicita una nueva velocidad de reproducción, este atributo especifica si el origen también solicita el ligero. Para obtener una definición de simplificación, vea about Rate control.
ms.assetid: 42b6d0b3-e5af-4a48-969c-53628d1b7c31
title: MF_EVENT_DO_THINNING atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08807413881a13789c50dbf2d063693e7e4539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001262"
---
# <a name="mf_event_do_thinning-attribute"></a>\_Atributo de \_ \_ refinamiento de evento MF

Cuando un origen multimedia solicita una nueva velocidad de reproducción, este atributo especifica si el origen también solicita el ligero. Para obtener una definición de simplificación, vea [About Rate Control](about-rate-control.md).

## <a name="data-type"></a>Tipo de datos

**UINT32**

Trata como un valor booleano.

## <a name="remarks"></a>Observaciones

Este atributo se usa con el evento [MESourceRateChangeRequested](mesourceratechangerequested.md) . Si el valor es **true**, el origen de medios solicita un cambio a la reproducción simplificada.

El valor predeterminado es **FALSE**.

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

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




