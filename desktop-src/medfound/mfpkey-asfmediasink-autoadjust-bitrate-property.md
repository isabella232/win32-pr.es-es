---
description: Especifica si el receptor de medios de ASF ajusta automáticamente la velocidad de bits.
ms.assetid: 0a6f4dd4-4ad7-4aab-a33d-14b4716f9902
title: MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d22463f477eb5abc1bb84254ad312427ecef52
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474104"
---
# <a name="mfpkey_asfmediasink_autoadjust_bitrate-property"></a>Propiedad MFPKEY \_ ASFMEDIASINK \_ AUTOADJUST \_ BITRATE

Especifica si el receptor de medios de ASF ajusta automáticamente la velocidad de bits.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**VARIANT \_ BOOL**

VT \_ BOOL

**boolVal**



## <a name="remarks"></a>Observaciones

Si el valor de esta propiedad es VARIANT TRUE, el receptor de medios de ASF ajusta automáticamente la velocidad de bits del contenido de ASF en respuesta a las características de las secuencias que se \_ multiplexan.

Esta propiedad afecta a cómo se comporta el receptor de medios de ASF cuando una secuencia desborda los parámetros de "cubo de pérdida" del receptor:



| Value              | Comportamiento                                                                                                                                      |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **VARIANT \_ TRUE**  | El receptor de medios de ASF ajusta automáticamente la velocidad de bits del contenido de ASF en respuesta a las características de las secuencias que se multiplexa. |
| **VARIANT \_ FALSE** | El receptor de medios de ASF usa el valor de velocidad de bits de flujo proporcionado por la aplicación.                                                                |



 

El valor predeterminado es **VARIANT \_ FALSE.**

Establezca esta propiedad al configurar el receptor de medios de ASF. El uso depende de la función a la que llame para crear el receptor de medios de ASF:

-   [**MFCreateASFMediaSink:**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)consulta el puntero [**DE TIPO MFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) recuperado para la **interfaz IPropertyStore.**

-   [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): llame a [**MFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) en el puntero [**MFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) especificado en el *parámetro pContentInfo.*

Al establecer esta propiedad en VARIANT TRUE, el receptor de medios de ASF establece la marca \_ **MFASF \_ \_ MULTIPLEXER AUTOADJUST \_ BITRATE** en el multiplexor de ASF. Vea [**ALFMultiplexer::SetFlags.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags)

Para obtener más información sobre el concepto de cubo filtrado, vea el tema "The Leaky Bucket Buffer Model" en la documentación del SDK Windows Media Format.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> <dt>

[**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




