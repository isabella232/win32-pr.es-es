---
description: Especifica el elemento que contiene este nodo de origen.
ms.assetid: f5fa5c10-8f30-43bd-8054-a39996f807a3
title: MF_TOPONODE_SEQUENCE_ELEMENTID atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3cd2c66c40a0bc3776d2fd2b7d78535cf24b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715379"
---
# <a name="mf_toponode_sequence_elementid-attribute"></a>\_ \_ Atributo ELEMENTID de secuencia MF TOPONODE \_

Especifica el elemento que contiene este nodo de origen.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los nodos de origen (**\_ \_ \_ nodo SOURCESTREAM de topología MF**).

La canalización multimedia usa este atributo para detectar cuándo los orígenes multimedia forman parte del mismo elemento. La canalización trata todos los nodos de origen que forman parte del mismo elemento que tienen el mismo reloj.

Cuando la canalización pone en cola una nueva topología que contiene nodos de origen que forman parte de un elemento que se encuentra en la topología anterior, la canalización trata estos nodos de origen como si tuvieran el mismo reloj que los nodos de origen de ese elemento en la topología anterior.

> [!Note]  
> La canalización multimedia no corrige las marcas de tiempo de los nodos de origen con diferentes velocidades de reloj.

 

Un origen multimedia que puede proporcionar topologías debe implementar la interfaz [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) o la interfaz [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) . Un origen multimedia que proporciona topologías debe establecer el atributo de la **\_ \_ secuencia \_ TOPONODE de MF** en cada nodo de origen que cree.

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

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
</dt> <dt>

[**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> <dt>

[Origen del secuenciador](sequencer-source.md)
</dt> </dl>

 

 




