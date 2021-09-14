---
description: Contiene la hora de inicio a la que se reinicia un origen multimedia desde su posición actual.
ms.assetid: b598b4d1-40e1-4282-b312-5aa6ca3a6733
title: MF_EVENT_SOURCE_ACTUAL_START atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0132fd8fc50f4e71a3b5bb334bc528d86c04e50c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127364078"
---
# <a name="mf_event_source_actual_start-attribute"></a>Atributo MF \_ EVENT \_ SOURCE REAL \_ \_ START

Contiene la hora de inicio a la que se reinicia un origen multimedia desde su posición actual.

## <a name="data-type"></a>Tipo de datos

**UINT64**

Tratar como un **valor LONGLONG.**

## <a name="remarks"></a>Observaciones

Este atributo se usa con el [evento MESourceStarted.](mesourcestarted.md) El atributo es relevante cuando los datos del evento están vacíos **(VT \_ EMPTY),** lo que indica que el origen multimedia se inició desde la posición de reproducción actual. En ese caso, el atributo **MF EVENT SOURCE ACTUAL \_ \_ \_ \_ START** especifica la hora de inicio real. Si los datos del evento **son VT \_ EMPTY** y este atributo no está establecido, se supone que la hora de inicio es cero.

Cuando los datos del evento [MESourceStarted](mesourcestarted.md) contienen la hora de inicio **(VT \_ I8),** no se debe establecer este atributo.

Este atributo es un valor con firma, aunque se almacena como **UINT64.**

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

 

 




