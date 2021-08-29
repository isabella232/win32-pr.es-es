---
description: Especifica el nivel de mezcla, en decibelios (dB), en una secuencia de audio Dolby Digital. Esta propiedad se aplica a los codificadores de audio Dolby Digital.
ms.assetid: fcb16d02-af4f-4626-99ee-2831172e5280
title: Propiedad AVEncDProductionMixLevel (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f73f2c9db1a4ddf1b1354ec0354f77b8f87d8a81b3c98dec7a74a45025e67550
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873215"
---
# <a name="avencddproductionmixlevel-property"></a>Propiedad AVEncDDProductionMixLevel

Especifica el nivel de mezcla, en decibelios (dB), en una secuencia de audio Dolby Digital. Esta propiedad se aplica a los codificadores de audio Dolby Digital.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncDDProductionMixLevel**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad tiene un intervalo lineal de valores. Para obtener el intervalo admitido, llame a [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Comentarios

Si establece esta propiedad, establezca la [**propiedad AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) en **TRUE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




