---
description: Identifica el nodo de topología para un receptor de flujo.
ms.assetid: 9aa6ca66-5122-4d05-94b9-32be194e9eb3
title: MF_EVENT_OUTPUT_NODE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b2cbcbc243c195deb1061417adb6d93271b328fa242b497a7fdb232f5f7695e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244714"
---
# <a name="mf_event_output_node-attribute"></a>Atributo MF \_ EVENT \_ OUTPUT \_ NODE

Identifica el nodo de topología para un receptor de flujo.

## <a name="data-type"></a>Tipo de datos

**UINT64**

Tratar como [**TOPOID.**](topoid.md)

## <a name="remarks"></a>Comentarios

El valor de este atributo es un identificador de nodo para un nodo de salida en la topología actual. Para obtener un puntero al nodo asociado, llame a [**IMFTopology::GetNodeByID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid) en la topología.

Este atributo se usa con los siguientes eventos:

-   [MESessionStreamSinkFormatChanged](mesessionstreamsinkformatchanged.md)
-   [MESinkInvalidated](mesinkinvalidated.md)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



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

 

 




