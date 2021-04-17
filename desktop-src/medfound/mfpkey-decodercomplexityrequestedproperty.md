---
description: Especifica la plantilla de conformidad del dispositivo que desea usar para la codificación de vídeo.
ms.assetid: cd2c068a-dbbc-42c5-bc92-bbb73f0259d1
title: Propiedad MFPKEY_DECODERCOMPLEXITYREQUESTED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e017361d7e8267d33ecb2cfdbce2a6e79758fac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696950"
---
# <a name="mfpkey_decodercomplexityrequested-property"></a>\_Propiedad DECODERCOMPLEXITYREQUESTED de MFPKEY

Especifica la plantilla de conformidad del dispositivo que desea usar para la codificación de vídeo.

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

1

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCDecoderComplexityRequested

## <a name="data-type-for-ipropertybag"></a>Tipo de datos de IPropertyBag

VT \_ BSTR

## <a name="default-value-for-ipropertybag"></a>Valor predeterminado de IPropertyBag

MP

## <a name="remarks"></a>Observaciones

El códec intentará codificar el contenido mediante la plantilla de conformidad del dispositivo especificada por este valor. La plantilla real a la que se ajusta el contenido codificado se puede recuperar de la propiedad [MFPKEY \_ DECODERCOMPLEXITYPROFILE](mfpkey-decodercomplexityprofileproperty.md) después de la codificación.

Esta propiedad debe ser uno de los valores siguientes.



| Valor de IPropertyStore | Valor de IPropertyBag | Descripción         |
|--------------------------|------------------------|---------------------|
| 0                        | DAÑADO                   | Perfil simple      |
| 1                        | MP                   | Perfil principal        |
| 2                        | CP                   | ya no se admite |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




