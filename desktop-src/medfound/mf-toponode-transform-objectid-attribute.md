---
description: Identificador de clase (CLSID) de la transformación de Media Foundation (MFT) asociada a este nodo de topología.
ms.assetid: 6aa6e649-d23d-4d8d-be80-2b8814b07a57
title: MF_TOPONODE_TRANSFORM_OBJECTID atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea96e09a75374bfe048b531492fc913f764d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543251"
---
# <a name="mf_toponode_transform_objectid-attribute"></a>MF \_ TOPONODE \_ Transform \_ atributo objectId

Identificador de clase (CLSID) de la transformación de Media Foundation (MFT) asociada a este nodo de topología.

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los nodos de transformación (**\_ nodo de \_ transformación \_ de topología MF**).

Las aplicaciones pueden utilizar este atributo para inicializar un nodo transfrom. Si establece este atributo, no tiene que llamar a [**IMFTopologyNode:: SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) con un puntero a un objeto MFT o de activación. Por el contrario, si llama a **SetObject**, no es necesario establecer este atributo. Para obtener más información, consulte [crear topologías](creating-topologies.md).

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Crear topologías](creating-topologies.md)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> </dl>

 

 




