---
description: Especifica la plantilla de conformidad de dispositivos que desea usar para la codificación de vídeo.
ms.assetid: cd2c068a-dbbc-42c5-bc92-bbb73f0259d1
title: MFPKEY_DECODERCOMPLEXITYREQUESTED propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e017361d7e8267d33ecb2cfdbce2a6e79758fac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257615"
---
# <a name="mfpkey_decodercomplexityrequested-property"></a>Propiedad \_ DECODERCOMPLEXITYREQUESTED de MFPKEY

Especifica la plantilla de conformidad de dispositivos que desea usar para la codificación de vídeo.

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

## <a name="remarks"></a>Observaciones

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
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




