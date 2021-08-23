---
description: Contiene un puntero al origen de medios asociado a un nodo de topología.
ms.assetid: 73b84ab6-bdc2-4b22-9ce4-b79b954476e5
title: MF_TOPONODE_SOURCE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce77b001cdfb5bad982de09c3d58cf1a717a5e841cc148d98967e82a60b088a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600105"
---
# <a name="mf_toponode_source-attribute"></a>Atributo MF \_ TOPONODE \_ SOURCE

Contiene un puntero al origen de medios asociado a un nodo de topología.

## <a name="data-type"></a>Tipo de datos

**IUnknown\***

## <a name="remarks"></a>Comentarios

Este atributo se aplica a los nodos de origen **(MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE**).

El valor del atributo es un puntero a la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) del origen multimedia. Este atributo es necesario.

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

[**ATTRIBUTEAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> </dl>

 

 




