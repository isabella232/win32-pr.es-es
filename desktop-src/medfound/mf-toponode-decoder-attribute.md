---
description: Especifica si un objeto subyacente de nodos de topología es un descodificador.
ms.assetid: b6d576dc-b12f-49bf-b938-db2c629df400
title: MF_TOPONODE_DECODER atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8946e9de4131ce62a7ab76119b4a409cea03b1d05000a5c28c3cbab4bdcf3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875189"
---
# <a name="mf_toponode_decoder-attribute"></a>Atributo MF \_ TOPONODE \_ DECODER

Especifica si el objeto subyacente de un nodo de topología es un descodificador.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como un valor booleano.

## <a name="remarks"></a>Comentarios

Este atributo se aplica a todos los tipos de nodo.

Si el valor de este atributo es distinto de cero, el objeto subyacente del nodo es un descodificador.

El cargador de topologías establece este atributo cuando crea un nodo descodificador. Una aplicación debe establecer este atributo si la aplicación agrega manualmente un descodificador a la topología.

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

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> </dl>

 

 




