---
description: Especifica que el marco actual se codifica mediante uno o varios fotogramas LTR.
ms.assetid: 51FD6E36-9CDF-4005-942F-7A92CA706F38
title: CODECAPI_AVEncVideoUseLTRFrame propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c438a4e6e2656c5e952062d9e3c1c0000899f2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269199"
---
# <a name="codecapi_avencvideouseltrframe-property"></a>Propiedad CODECAPI \_ AVEncVideoUseLTRFrame

Especifica que el marco actual se codifica mediante uno o varios fotogramas LTR.

## <a name="data-type"></a>Tipo de datos

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoUseLTRFrame**

## <a name="property-value"></a>Valor de propiedad

El valor de este control incluye dos campos, donde cada campo tiene 16 bits.




| Value | Significado | 
|-------|---------|
| <span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl><dt><strong>Primer campo</strong></dt><dt>Bits[0..15]</dt></dl> | Indica qué fotogramas LTR se permiten para codificar el marco actual. <br /><strong>Codificadores H.264/AVC:</strong><br /> Se trata de un mapa de bits que indica qué fotogramas LTR se pueden usar como referencia para este marco. El bit menos significativo corresponde al índice LTR 0, el segundo bit menos significativo corresponde al índice LTR 1, etc.<br /> Este valor no debe ser 0.<br /> El índice más alto especificado por este valor no debe ser mayor que el número máximo de fotogramas LTR especificado en la <a href="codecapi-avencvideoltrbuffercontrol.md">propiedad CODECAPI_AVEncVideoLTRBufferControl</a> menos uno.<br /> | 
| <span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl><dt><strong>Segundo campo</strong></dt><dt>Bits[16..31]</dt></dl> | Marca que indica si se requieren limitaciones adicionales para codificar fotogramas posteriores. <br /><strong>Codificadores H.264/AVC:</strong><br /> 1 está en el único valor válido para este campo. Todos los demás valores no son válidos y están reservados para su uso futuro.<br /> Cuando la marca es 1, el codificador codificará los fotogramas posteriores en el orden de codificación sujeto a las restricciones siguientes:<br /><ul><li>No debe usar fotogramas de referencia a corto plazo en el orden de codificación anterior al fotograma actual o codificación futura en orden de codificación.</li><li>No usará marcos LTR no descritos por el control de CODECAPI_AVEncVideoUseLTRFrame más reciente.</li><li>Puede usar fotogramas LTR actualizados después del marco actual.</li></ul> | 




 

## <a name="remarks"></a>Observaciones

**Codificadores H.264/AVC:**

No se debe llamar a esta propiedad si se ha emitido una llamada pendiente para usar un marco LTR mediante la propiedad CODECAPI AVEncVideoUseLTRFrame y el codificador aún no ha generado un marco que haya usado \_ la LTR. En otras palabras, el codificador no debe poner en cola las solicitudes CODECAPI \_ AVEncVideoUseLTRFrame.

Si se envía una solicitud \_ CODECAPI AVEncVideoUseLTRFrame mientras hay otra solicitud CODECAPI AVEncVideoUseLTRFrame pendiente, se debe descartar la solicitud \_ anterior.

Llamar a CODECAPI AVEncVideoUseLTRFrame en un marco de capa no base es válido y se aplicará al marco de capa no base, sin retraso a un marco de \_ capa base.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| para aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




