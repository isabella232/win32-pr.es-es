---
description: Especifica cuándo se vacía una transformación.
ms.assetid: 1e87f58f-546f-4dd4-b218-1458ff17db53
title: MF_TOPONODE_FLUSH atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67e02c297efa68c6e6c585837675a46b729ec2382be072828059fd795d1c67a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663885"
---
# <a name="mf_toponode_flush-attribute"></a>Atributo MF \_ TOPONODE \_ FLUSH

Especifica cuándo se vacía una transformación.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Este atributo se aplica a los nodos de transformación **(MF \_ TOPOLOGY \_ TRANSFORM \_ NODE**).

El valor del atributo es un miembro de la enumeración [**MF \_ TOPONODE \_ FLUSH \_ MODE.**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_flush_mode) Si no se establece este atributo, el valor predeterminado es **MF \_ TOPONODE \_ FLUSH \_ ALWAYS.**

El vaciado se realiza mediante una llamada [**a IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) en la transformación con el mensaje FLUSH del comando [**MFT \_ MESSAGE. \_ \_**](mft-message-command-flush.md) Para obtener más información, vea [**Enumeración \_ MFT MESSAGE \_ TYPE.**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)

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

[**NODETopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> </dl>

 

 




