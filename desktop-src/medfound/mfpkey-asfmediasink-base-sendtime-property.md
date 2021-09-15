---
description: Tiempo de envío base para el receptor de medios de ASF, en milisegundos.
ms.assetid: 1b99845e-751a-4ec6-bd2d-e4644cd6863e
title: MFPKEY_ASFMEDIASINK_BASE_SENDTIME propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f9bc7f9d92a598a723e3eeee733f63b59d27d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474103"
---
# <a name="mfpkey_asfmediasink_base_sendtime-property"></a>Propiedad MFPKEY \_ ASFMEDIASINK \_ BASE \_ SENDTIME

Tiempo de envío base para el receptor de medios de ASF, en milisegundos.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Observaciones

La hora de envío es la hora a la que se envía un paquete asf a través de la red. No se corresponde directamente con el tiempo de presentación de los datos del paquete.

Puede usar esta propiedad para configurar el receptor de medios de ASF. El uso depende de la función a la que llame para crear el receptor de medios de ASF:

-   [**MFCreateASFMediaSink:**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)consulta el puntero [**DECIMMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) recuperado para la **interfaz IPropertyStore.**

-   [**MFCreateASFMediaSinkActivate:**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)llame a [**MFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) en el puntero [**DEFFContentInfo especificado**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) en el *parámetro pContentInfo.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




