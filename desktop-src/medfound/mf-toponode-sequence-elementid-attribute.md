---
description: Especifica el elemento que contiene este nodo de origen.
ms.assetid: f5fa5c10-8f30-43bd-8054-a39996f807a3
title: MF_TOPONODE_SEQUENCE_ELEMENTID atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3cd2c66c40a0bc3776d2fd2b7d78535cf24b6c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572769"
---
# <a name="mf_toponode_sequence_elementid-attribute"></a>Atributo ELEMENTID DE \_ MF TOPONODE \_ SEQUENCE \_

Especifica el elemento que contiene este nodo de origen.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los nodos de origen **(MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE).**

La canalización de medios usa este atributo para detectar cuándo los orígenes multimedia forman parte del mismo elemento. La canalización trata todos los nodos de origen que forman parte del mismo elemento que tener el mismo reloj.

Cuando la canalización pone en cola una nueva topología que contiene nodos de origen que forman parte de un elemento que está presente en la topología anterior, la canalización trata estos nodos de origen como que tienen el mismo reloj que los nodos de origen de ese elemento en la topología anterior.

> [!Note]  
> La canalización de medios no corrige las marcas de tiempo para los nodos de origen con velocidades de reloj diferentes.

 

Un origen de medios que pueda proporcionar topologías debe implementar la interfaz [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) o [**la interfaz DESEQUENcerSource.**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) Un origen multimedia que proporciona topologías debe establecer el atributo **MF \_ TOPONODE \_ SEQUENCE \_ ELEMENTID** en cada nodo de origen que cree.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
</dt> <dt>

[**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)
</dt> <dt>

[**NODETopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> <dt>

[Origen del secuenciador](sequencer-source.md)
</dt> </dl>

 

 




