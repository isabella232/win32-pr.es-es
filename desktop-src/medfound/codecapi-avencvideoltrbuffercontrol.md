---
description: Especifica el número máximo de fotogramas de referencia a largo plazo (LTR) controlados por la aplicación.
ms.assetid: C34AD867-5F94-4414-A282-ECC392678635
title: CODECAPI_AVEncVideoLTRBufferControl propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cca2e24e8295969609ba325a2abf24be76fb07c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269271"
---
# <a name="codecapi_avencvideoltrbuffercontrol-property"></a>Propiedad CODECAPI \_ AVEncVideoLTRBufferControl

Especifica el número máximo de fotogramas de referencia a largo plazo (LTR) controlados por la aplicación.

## <a name="data-type"></a>Tipo de datos

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoLTRBufferControl**

## <a name="property-value"></a>Valor de propiedad

El valor de este control incluye dos campos, donde cada campo tiene 16 bits.




| Value | Significado | 
|-------|---------|
| <span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl><dt><strong>Primer campo</strong></dt><dt>Bits[0..15]</dt></dl> | Número de fotogramas LTR controlados por la aplicación.<br /><strong>Codificadores H.264/AVC:</strong><br /> Suponiendo que el valor es N y N es un valor distinto de cero, en cada fotograma IDR, el codificador debe marcar automáticamente los fotogramas que se deberán seguir al marco IDR (e incluir el marco IDR) como fotogramas LTR siempre y cuando se apliquen los 3 siguientes:<ul><li>El marco aún no está establecido para marcarse como marco de referencia a largo plazo.</li><li>El marco es un marco de capa base. Por ejemplo, el elemento de <strong>temporal_id</strong> es igual a 0.</li><li>El número de fotogramas marcados actualmente como LTR es menor que N.</li></ul><br /> | 
| <span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl><dt><strong>Segundo campo</strong></dt><dt>Bits[16..31]</dt></dl> | Modo de confianza del control LTR.<br /><strong>Codificadores H.264/AVC:</strong><br /> 1 (Confiar hasta) significa que el codificador puede usar un fotograma LTR a menos que la aplicación lo invalide explícitamente a través del control <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame.</a> <br /> Otros valores no son válidos y están reservados para su uso futuro.<br /> | 




 

## <a name="remarks"></a>Observaciones

Se trata de una API estática.

El valor predeterminado debe ser 0.

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

 

 




