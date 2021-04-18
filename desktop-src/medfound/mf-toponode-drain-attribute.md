---
description: Especifica cuándo se purga una transformación.
ms.assetid: 68332106-d1fe-467b-8baa-1e592b9cc243
title: MF_TOPONODE_DRAIN atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679b87d626738b82f4504673392bd0fe159e2722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715390"
---
# <a name="mf_toponode_drain-attribute"></a>\_Atributo de \_ purga MF TOPONODE

Especifica cuándo se purga una transformación.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los nodos de transformación (**\_ nodo de \_ transformación \_ de topología MF**).

El valor del atributo es un miembro de la enumeración del [**\_ modo de \_ purga \_ MF TOPONODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_drain_mode) . Si no se establece este atributo, el valor predeterminado es **MF \_ TOPONODE \_ \_ valor predeterminado de Drain**.

La purga se realiza mediante una llamada a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) en la transformación con el mensaje de [**\_ agotamiento del \_ comando \_ de mensaje MFT**](mft-message-command-drain.md) . Para obtener más información, consulte enumeración de [**\_ \_ tipo de mensaje de MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) .

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

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> </dl>

 

 




