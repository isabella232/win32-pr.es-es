---
description: Contiene un puntero al descriptor de flujo para el origen de medios.
ms.assetid: 5acafbc1-823f-4b6d-8737-04b3a6a0cf87
title: MF_TOPONODE_STREAM_DESCRIPTOR atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f074a1c1ffde3671779362724676f884c3b6b0b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705793"
---
# <a name="mf_toponode_stream_descriptor-attribute"></a>\_Atributo de \_ descriptor de secuencia MF TOPONODE \_

Contiene un puntero al descriptor de flujo para el origen de medios.

## <a name="data-type"></a>Tipo de datos

**IUnknown \** _

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los nodos de origen (_ * MF \_ Topology \_ SOURCESTREAM \_ node * *).

El valor del atributo es un puntero a la interfaz [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) del descriptor de flujo. Este atributo es necesario.

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

[**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes:: Setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> </dl>

 

 




