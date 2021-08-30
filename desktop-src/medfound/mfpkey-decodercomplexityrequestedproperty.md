---
description: Especifica la plantilla de conformidad del dispositivo que desea usar para la codificación de vídeo.
ms.assetid: cd2c068a-dbbc-42c5-bc92-bbb73f0259d1
title: MFPKEY_DECODERCOMPLEXITYREQUESTED propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83330e3e413967d3b97d6531f8bbaf6ebd7809f732885849d0bf7b8f62d55ef5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954235"
---
# <a name="mfpkey_decodercomplexityrequested-property"></a>Propiedad MFPKEY \_ DECODERCOMPLEXITYREQUESTED

Especifica la plantilla de conformidad del dispositivo que desea usar para la codificación de vídeo.

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

1

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCDecoderComplexityRequested

## <a name="data-type-for-ipropertybag"></a>Tipo de datos para IPropertyBag

VT \_ BSTR

## <a name="default-value-for-ipropertybag"></a>Valor predeterminado para IPropertyBag

"MP"

## <a name="remarks"></a>Comentarios

El códec intentará codificar el contenido mediante la plantilla de conformidad del dispositivo especificada por este valor. La plantilla real a la que se ajusta el contenido codificado se puede recuperar de la propiedad [MFPKEY \_ DECODERCOMPLEXITYPROFILE](mfpkey-decodercomplexityprofileproperty.md) después de la codificación.

Esta propiedad debe ser uno de los siguientes valores.



| Valor de IPropertyStore | Valor de IPropertyBag | Descripción         |
|--------------------------|------------------------|---------------------|
| 0                        | "SP"                   | perfil simple      |
| 1                        | "MP"                   | perfil principal        |
| 2                        | "CP"                   | ya no se admite |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




