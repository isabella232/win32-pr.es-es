---
description: Especifica el final de una fase de codificación.
ms.assetid: 8a7e6e09-766c-4346-8893-eea5614b2aa4
title: Propiedad MFPKEY_ENDOFPASS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a38e03867e11cde944bf902ae52f98cda7b8313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908781"
---
# <a name="mfpkey_endofpass-property"></a>\_Propiedad ENDOFPASS de MFPKEY

Especifica el final de una fase de codificación.

## <a name="data-type"></a>Tipo de datos

**VT \_ bool**

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCEndOfPass

## <a name="data-type-for-ipropertybag"></a>Tipo de datos de IPropertyBag

No se requiere ningún tipo de datos. Para establecer esta propiedad, pase una **variante** no inicializada.

## <a name="remarks"></a>Observaciones

Esta propiedad no es una propiedad normal porque tiene el mismo efecto sin tener en cuenta si el valor es VARIANT \_ true o Variant \_ false. Debe establecer esta propiedad después de procesar los últimos ejemplos de entrada para un paso de preprocesamiento. Si va a realizar varias fases, debe establecer esta propiedad al final de cada paso de preprocesamiento (en la actualidad ninguno de los códecs admite más de una). Si no establece esta propiedad, el códec asumirá que sigue pasando ejemplos para el preprocesamiento.

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

 

 




