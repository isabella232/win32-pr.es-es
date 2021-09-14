---
description: Permite que la aplicación invalide la configuración predeterminada en varias propiedades del DSP de captura de voz.
ms.assetid: 1c11e817-36bd-4a5d-9c2b-6a91e86f623f
title: MFPKEY_WMAAECMA_FEATURE_MODE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a47ef86a2acf83131800e9cb55b86de2cd3d98
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360688"
---
# <a name="mfpkey_wmaaecma_feature_mode-property"></a>Propiedad MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE

Permite que la aplicación invalide la configuración predeterminada en varias propiedades del DSP de captura de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ BOOL

## <a name="default-value"></a>Valor predeterminado

VARIANT \_ FALSE

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Observaciones

Si esta propiedad es VARIANT \_ TRUE, la aplicación puede establecer las siguientes propiedades en el DSP:

-   [MFPKEY \_ WMAAECMA \_ FEATR \_ AES](mfpkey-wmaaecma-featr-aesproperty.md)
-   [MFPKEY \_ WMAAECMA \_ FEATR \_ AGC](mfpkey-wmaaecma-featr-agcproperty.md)
-   [CLIP DEL CENTRO MFPKEY \_ WMAAECMA \_ FEATR \_ \_](mfpkey-wmaaecma-featr-center-clipproperty.md)
-   [LONGITUD DE ECO DE MFPKEY \_ WMAAECMA \_ FEATR \_ \_](mfpkey-wmaaecma-featr-echo-lengthproperty.md)
-   [TAMAÑO DEL MARCO MFPKEY \_ WMAAECMA \_ FEATR \_ \_](mfpkey-wmaaecma-featr-frame-sizeproperty.md)
-   [MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ MODE](mfpkey-wmaaecma-featr-micarr-modeproperty.md)
-   [MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ PREPROC](mfpkey-wmaaecma-featr-micarr-preprocproperty.md)
-   [RELLENO DE RUIDO DE MFPKEY \_ WMAAECMA \_ FEATR \_ \_](mfpkey-wmaaecma-featr-noise-fillproperty.md)
-   [MFPKEY \_ WMAAECMA \_ FEATR \_ NS](mfpkey-wmaaecma-featr-nsproperty.md)
-   [MFPKEY \_ WMAAECMA \_ FEATR \_ VAD](mfpkey-wmaaecma-featr-vadproperty.md)

Si esta propiedad es VARIANT \_ FALSE, el DSP omite estas propiedades y usa su configuración predeterminada. El valor predeterminado de esta propiedad es VARIANT \_ FALSE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
