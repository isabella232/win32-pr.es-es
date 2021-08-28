---
description: Especifica cómo el cargador de topologías conecta este nodo de topología y si este nodo es opcional.
ms.assetid: 8d70e1af-607b-47c3-9808-091c95fd05b7
title: MF_TOPONODE_CONNECT_METHOD atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acace030331821b9ca4030c058aabda3160183de80323b32e792de372afd182b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875355"
---
# <a name="mf_toponode_connect_method-attribute"></a>Atributo MF \_ TOPONODE \_ CONNECT \_ METHOD

Especifica cómo el cargador de topologías conecta este nodo de topología y si este nodo es opcional.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Este atributo se aplica a todos los tipos de nodo.

El valor del atributo es un **OR** bit a bit de marcas de la [**enumeración MF \_ CONNECT \_ METHOD.**](/windows/desktop/api/mfidl/ne-mfidl-mf_connect_method) Si no se establece este atributo, el valor predeterminado es **MF \_ CONNECT ALLOW \_ \_ DECODER**.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

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

 

 




