---
description: Contiene la hora de inicio en la que un origen multimedia se reinicia desde su posición actual.
ms.assetid: b598b4d1-40e1-4282-b312-5aa6ca3a6733
title: MF_EVENT_SOURCE_ACTUAL_START atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0132fd8fc50f4e71a3b5bb334bc528d86c04e50c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423824"
---
# <a name="mf_event_source_actual_start-attribute"></a>\_Atributo de \_ \_ Inicio real del origen de eventos MF \_

Contiene la hora de inicio en la que un origen multimedia se reinicia desde su posición actual.

## <a name="data-type"></a>Tipo de datos

**UINT64**

Trata como un valor de **LONGLONG** .

## <a name="remarks"></a>Observaciones

Este atributo se usa con el evento [MESourceStarted](mesourcestarted.md) . El atributo es relevante cuando los datos de evento están vacíos (**VT \_ vacío**), lo que indica que el origen de medios se inició desde la posición de reproducción actual. En ese caso, el atributo de **\_ \_ \_ \_ Inicio real del origen de eventos MF** especifica la hora de inicio real. Si los datos de evento **están \_ vacíos en VT** y este atributo no está establecido, se supone que la hora de inicio es cero.

Cuando los datos del evento [MESourceStarted](mesourcestarted.md) contienen la hora de inicio (**VT \_ i8**), no se debe establecer este atributo.

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

 

 




