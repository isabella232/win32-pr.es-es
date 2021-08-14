---
description: Especifica cómo se debe aplicar el receptor de medios de ASF Windows DRM multimedia.
ms.assetid: 5f81294b-859a-4325-98dd-6267c736e1f1
title: MFPKEY_ASFMEDIASINK_DRMACTION propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ed62f62a5d03d7fe938101d9837bd8ed9bccefe69b2bf30e0566ea0b471e37f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874349"
---
# <a name="mfpkey_asfmediasink_drmaction-property"></a>Propiedad \_ DRMACTION de ASFMEDIASINK de MFPKEY \_

Especifica cómo se debe aplicar el receptor de medios de ASF Windows DRM multimedia.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Comentarios

El valor de esta propiedad es un miembro de la enumeración [**\_ MFSINK WMDRMACTION.**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction)

Puede usar este atributo para configurar el receptor de medios de ASF. El uso depende de la función a la que llame para crear el receptor de medios de ASF:

-   [**MFCreateASFMediaSink:**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)consulta el puntero [**DECIMMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) recuperado para la **interfaz IPropertyStore.**

-   [**MFCreateASFMediaSinkActivate:**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)llame a [**MFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) en el puntero [**DEFFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) especificado en el *parámetro pContentInfo.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
