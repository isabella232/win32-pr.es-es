---
description: Contiene un puntero a los atributos de flujo de la secuencia conectada en una transformación de Media Foundation hardware (MFT).
ms.assetid: 7e14a02e-4cbf-45aa-a6f5-2c53b2437127
title: MFT_CONNECTED_STREAM_ATTRIBUTE atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b182cbed78f5f9851b621de72bf691bf698b70
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468599"
---
# <a name="mft_connected_stream_attribute-attribute"></a>Atributo MFT \_ CONNECTED \_ STREAM \_ ATTRIBUTE

Contiene un puntero a los atributos de flujo de la secuencia conectada en una transformación de Media Foundation hardware (MFT).

## <a name="data-type"></a>Tipo de datos

**ATTRIBUTEAttributes \* *_ almacenados como _* IUnknown\***

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para establecer este atributo, llame [**a IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Observaciones

Normalmente, las aplicaciones no usan este atributo.

Este atributo se usa para las MTA que actúan como servidores proxy en un dispositivo de hardware. Para obtener más información, vea [Hardware MFT](hardware-mfts.md).

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFT \_ CONECTADO A HW \_ \_ \_ STREAM](mft-connected-to-hw-stream.md)
</dt> <dt>

[MTA de hardware](hardware-mfts.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




