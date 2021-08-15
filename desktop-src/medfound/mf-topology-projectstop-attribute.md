---
description: Especifica la hora de inicio de una topología, en relación con el inicio de la primera topología de la secuencia.
ms.assetid: 1ca3709e-88ea-40ca-8da4-c2259365122b
title: MF_TOPOLOGY_PROJECTSTOP atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ab227f1fdcda99148be3106b2ea724578f30bd9fd83756cd3b9d16f46ef993
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875402"
---
# <a name="mf_topology_projectstop-attribute"></a>Atributo \_ MF TOPOLOGY \_ PROJECTSTOP

Especifica la hora de inicio de una topología, en relación con el inicio de la primera topología de la secuencia.

## <a name="data-type"></a>Tipo de datos

**UINT64**

Tratar como **un valor LONGLONG.**

## <a name="remarks"></a>Comentarios

El valor se da en unidades de 100 nanosegundos.

Si la sesión multimedia se creó con el atributo [**MF \_ SESSION GLOBAL \_ \_ TIME**](mf-session-global-time-attribute.md) igual a **TRUE,** todas las topologías deben contener el atributo **MF \_ TOPOLOGY \_ PROJECTSTOP.** De lo contrario, las topologías no deben contener el atributo **MF \_ TOPOLOGY \_ PROJECTSTOP.** Para obtener más información, vea [Sequence Presentation Times](sequence-presentation-times.md).

Este atributo es un valor con firma, aunque se almacena como **UINT64**.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Tiempos de presentación de secuencia](sequence-presentation-times.md)
</dt> <dt>

[Atributos de topología](topology-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**MF \_ TOPOLOGY \_ PROJECTSTART**](mf-topology-projectstart-attribute.md)
</dt> </dl>

 

 




