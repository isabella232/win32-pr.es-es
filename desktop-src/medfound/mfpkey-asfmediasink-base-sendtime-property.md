---
description: Tiempo de envío base para el receptor de medios de ASF, en milisegundos.
ms.assetid: 1b99845e-751a-4ec6-bd2d-e4644cd6863e
title: MFPKEY_ASFMEDIASINK_BASE_SENDTIME propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23ece9ef06a7253c016557609c344db09f96bcd32ddef44272c2ce5ffa77672a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874582"
---
# <a name="mfpkey_asfmediasink_base_sendtime-property"></a>Propiedad MFPKEY \_ ASFMEDIASINK \_ BASE \_ SENDTIME

Tiempo de envío base para el receptor de medios de ASF, en milisegundos.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Comentarios

La hora de envío es la hora a la que se envía un paquete asf a través de la red. No se corresponde directamente con el tiempo de presentación de los datos del paquete.

Puede usar esta propiedad para configurar el receptor de medios de ASF. El uso depende de la función a la que llame para crear el receptor de medios de ASF:

-   [**MFCreateASFMediaSink:**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)consulta el puntero [**DECIMMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) recuperado para la **interfaz IPropertyStore.**

-   [**MFCreateASFMediaSinkActivate:**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)llame a [**MFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) en el puntero [**DEFFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) especificado en el *parámetro pContentInfo.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




