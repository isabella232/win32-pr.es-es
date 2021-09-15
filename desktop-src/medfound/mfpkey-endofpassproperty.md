---
description: Especifica el final de un paso de codificación.
ms.assetid: 8a7e6e09-766c-4346-8893-eea5614b2aa4
title: MFPKEY_ENDOFPASS propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a38e03867e11cde944bf902ae52f98cda7b8313
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468648"
---
# <a name="mfpkey_endofpass-property"></a>Propiedad MFPKEY \_ ENDOFPASS

Especifica el final de un paso de codificación.

## <a name="data-type"></a>Tipo de datos

**VT \_ BOOL**

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCEndOfPass

## <a name="data-type-for-ipropertybag"></a>Tipo de datos para IPropertyBag

No se requiere ningún tipo de datos. Para establecer esta propiedad, pase una variant no **inicializada.**

## <a name="remarks"></a>Observaciones

Esta propiedad no es una propiedad normal porque tiene el mismo efecto independientemente de si el valor es VARIANT \_ TRUE o VARIANT \_ FALSE. Debe establecer esta propiedad después de procesar los últimos ejemplos de entrada para un paso de preprocesamiento. Si está realizando varios pases, debe establecer esta propiedad al final de cada paso de preprocesamiento (en la actualidad, ninguno de los códecs admite más de uno). Si no establece esta propiedad, el códec supondrá que sigue pasando ejemplos para el preprocesamiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




