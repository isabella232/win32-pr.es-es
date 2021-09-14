---
description: Hora de inicio de la presentación, en unidades de 100 nanosegundos, medida por el reloj de presentación.
ms.assetid: d19d851c-ab4a-4a9d-bcc4-8dd4e993fa2c
title: MF_EVENT_START_PRESENTATION_TIME atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65bf6142ce12a7bf921fd26373ea5d10ab384560
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257879"
---
# <a name="mf_event_start_presentation_time-attribute"></a>Atributo MF \_ EVENT \_ START PRESENTATION \_ \_ TIME

Hora de inicio de la presentación, en unidades de 100 nanosegundos, medida por el reloj de presentación.

## <a name="data-type"></a>Tipo de datos

**UINT64**

Tratar como un **valor LONGLONG.**

## <a name="remarks"></a>Observaciones

Este atributo se usa con el [evento MESessionNotifyPresentationTime.](mesessionnotifypresentationtime.md)

Este atributo es un valor con firma, aunque se almacena como **UINT64**.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de eventos](event-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




