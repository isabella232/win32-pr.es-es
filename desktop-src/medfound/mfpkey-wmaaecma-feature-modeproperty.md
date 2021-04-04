---
description: Permite que la aplicación invalide la configuración predeterminada en varias propiedades del DSP de captura de voz.
ms.assetid: 1c11e817-36bd-4a5d-9c2b-6a91e86f623f
title: Propiedad MFPKEY_WMAAECMA_FEATURE_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a47ef86a2acf83131800e9cb55b86de2cd3d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811618"
---
# <a name="mfpkey_wmaaecma_feature_mode-property"></a>\_Propiedad del \_ modo de característica MFPKEY WMAAECMA \_

Permite que la aplicación invalide la configuración predeterminada en varias propiedades del DSP de captura de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ bool

## <a name="default-value"></a>Valor predeterminado

VARIANTE \_ false

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Observaciones

Si esta propiedad es VARIANT \_ true, la aplicación puede establecer las siguientes propiedades en el DSP:

-   [MFPKEY \_ WMAAECMA \_ feat \_ AES](mfpkey-wmaaecma-featr-aesproperty.md)
-   [MFPKEY \_ WMAAECMA \_ feat \_ AGC](mfpkey-wmaaecma-featr-agcproperty.md)
-   [\_clip del \_ \_ Centro \_ de MFPKEY WMAAECMA](mfpkey-wmaaecma-featr-center-clipproperty.md)
-   [\_longitud del \_ eco del funcdor de MFPKEY WMAAECMA \_ \_](mfpkey-wmaaecma-featr-echo-lengthproperty.md)
-   [\_tamaño de \_ \_ marco \_ del MFPKEY de WMAAECMA](mfpkey-wmaaecma-featr-frame-sizeproperty.md)
-   [\_ \_ \_ modo MICARR MFPKEY WMAAECMA feat \_](mfpkey-wmaaecma-featr-micarr-modeproperty.md)
-   [MFPKEY \_ WMAAECMA \_ feat \_ MICARR \_ preproc](mfpkey-wmaaecma-featr-micarr-preprocproperty.md)
-   [\_relleno de \_ \_ ruido \_ de MFPKEY WMAAECMA](mfpkey-wmaaecma-featr-noise-fillproperty.md)
-   [MFPKEY \_ WMAAECMA \_ feat \_](mfpkey-wmaaecma-featr-nsproperty.md)
-   [MFPKEY \_ WMAAECMA \_ feat \_ VAD](mfpkey-wmaaecma-featr-vadproperty.md)

Si esta propiedad es VARIANT \_ false, el DSP omite estas propiedades y usa su configuración predeterminada. El valor predeterminado de esta propiedad es VARIANT \_ false.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
