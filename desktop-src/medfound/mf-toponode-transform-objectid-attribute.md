---
description: Identificador de clase (CLSID) de la transformación Media Foundation transformación (MFT) asociada a este nodo de topología.
ms.assetid: 6aa6e649-d23d-4d8d-be80-2b8814b07a57
title: MF_TOPONODE_TRANSFORM_OBJECTID atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b5013bc43f07e08e1a2c26530e9325595e62666986516029ef9d76e2c72ffe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244319"
---
# <a name="mf_toponode_transform_objectid-attribute"></a>Atributo OBJECTID MF \_ TOPONODE \_ TRANSFORM \_

Identificador de clase (CLSID) de la transformación Media Foundation transformación (MFT) asociada a este nodo de topología.

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Comentarios

Este atributo se aplica a los nodos de transformación (**MF \_ TOPOLOGY \_ TRANSFORM \_ NODE**).

Las aplicaciones pueden usar este atributo para inicializar un nodo transfrom. Si establece este atributo, no tiene que llamar a [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) con un puntero a un objeto MFT o de activación. Por el contrario, si llama a **SetObject**, no es necesario establecer este atributo. Para obtener más información, vea [Crear topologías.](creating-topologies.md)

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

[**ATTRIBUTEAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**ATTRIBUTEAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> <dt>

[Creación de topologías](creating-topologies.md)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> </dl>

 

 




