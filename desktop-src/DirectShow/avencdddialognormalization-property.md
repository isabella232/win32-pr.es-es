---
description: Especifica el nivel de normalización del cuadro de diálogo, en decibelios (dB), en una secuencia de audio Dolby Digital. Esta propiedad se aplica a los codificadores de audio Dolby Digital.
ms.assetid: c347f8b2-5132-45d6-af66-43d3c409b0d7
title: Propiedad AVEncDDDialogNormalization (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f050147b0de889c9bb12f4e66964f16b8705c4883fa66c0f5cbba9c82338c30f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690195"
---
# <a name="avencdddialognormalization-property"></a>Propiedad AVEncDDDialogNormalization

Especifica el nivel de normalización del cuadro de diálogo, en decibelios (dB), en una secuencia de audio Dolby Digital. Esta propiedad se aplica a los codificadores de audio Dolby Digital.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncDDDialogNormalization**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad tiene un intervalo lineal de valores. Para obtener el intervalo admitido, llame a [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 




