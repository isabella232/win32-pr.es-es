---
description: Especifica el final de un paso de codificación.
ms.assetid: 8a7e6e09-766c-4346-8893-eea5614b2aa4
title: MFPKEY_ENDOFPASS (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 977c876d14c6757c5f1bc31e0d5b7cc58f6e13fad827cc23f821be8382a5e376
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738208"
---
# <a name="mfpkey_endofpass-property"></a>Propiedad MFPKEY \_ ENDOFPASS

Especifica el final de un paso de codificación.

## <a name="data-type"></a>Tipo de datos

**VT \_ BOOL**

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCEndOfPass

## <a name="data-type-for-ipropertybag"></a>Tipo de datos para IPropertyBag

No se requiere ningún tipo de datos. Para establecer esta propiedad, pase una variant sin **inicializar.**

## <a name="remarks"></a>Observaciones

Esta propiedad no es una propiedad normal porque tiene el mismo efecto independientemente de si el valor es VARIANT \_ TRUE o VARIANT \_ FALSE. Debe establecer esta propiedad después de procesar los últimos ejemplos de entrada para un paso de preprocesamiento. Si va a realizar varias pasadas, debe establecer esta propiedad al final de cada paso de preprocesamiento (actualmente ninguno de los códecs admite más de uno). Si no establece esta propiedad, el códec asumirá que sigue pasando ejemplos para el preprocesamiento.

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

 

 




