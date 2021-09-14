---
description: Especifica cómo se debe aplicar el receptor de medios de ASF Windows DRM multimedia.
ms.assetid: 5f81294b-859a-4325-98dd-6267c736e1f1
title: MFPKEY_ASFMEDIASINK_DRMACTION propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80906a5ac6e5d12bd59dd57445d33b100fee1aef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363846"
---
# <a name="mfpkey_asfmediasink_drmaction-property"></a>Propiedad \_ DRMACTION de ASFMEDIASINK de MFPKEY \_

Especifica cómo se debe aplicar el receptor de medios de ASF Windows DRM multimedia.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Observaciones

El valor de esta propiedad es miembro de la enumeración [**\_ MFSINK WMDRMACTION.**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction)

Puede usar este atributo para configurar el receptor de medios de ASF. El uso depende de la función a la que llame para crear el receptor de medios de ASF:

-   [**MFCreateASFMediaSink:**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)consulta el puntero [**DECIMMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) recuperado para la **interfaz IPropertyStore.**

-   [**MFCreateASFMediaSinkActivate:**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)llame a [**MFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) en el puntero [**DEFFContentInfo especificado**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) en el *parámetro pContentInfo.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
