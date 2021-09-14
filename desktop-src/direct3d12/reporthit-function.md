---
description: Lo llama un sombreador de intersección para notificar una intersección de rayos.
ms.assetid: ''
title: Función ReportHit
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportHit
api_type:
- NA
ms.openlocfilehash: 58d109f184974f76c533aaeee055f1ebf21d10eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072891"
---
# <a name="reporthit-function"></a>Función ReportHit

Lo llama un [sombreador de intersección](intersection-shader.md) para notificar una intersección de rayos.

## <a name="syntax"></a>Sintaxis
Esta definición de función intrínseca es equivalente a la siguiente plantilla de función:

```
template<attr_t>
bool ReportHit(float THit, uint HitKind, attr_t Attributes);
```



## <a name="parameters"></a>Parámetros

`THit`

Valor float que especifica la distancia paramétrica de la intersección.

`HitKind`

Entero sin signo que identifica el tipo de impacto que se produjo.  Se trata de un valor especificado por el usuario en el intervalo de 0 a 127.  Cualquier sombreador de [impactos o](any-hit-shader.md) más cercanos puede leer el valor con el [](closest-hit-shader.md) **intrínseco HitKind.**

`Attributes`

Estructura de atributo de intersección definida por el [**usuario**](intersection-attributes.md) que especifica los atributos de intersección.  

## <a name="return-value"></a>Valor devuelto

**bool** True si se aceptó la pulsación.  Se rechaza una pulsación si *THit* está fuera del intervalo de rayos actual o cualquier sombreador de llamadas llama [**a IgnoreHit**](ignorehit-function.md).  **RayTMin** y RayTCurrent definen el intervalo de **rayos actual.**

## <a name="remarks"></a>Observaciones

Se puede llamar a esta función desde los siguientes tipos de sombreador:

* [**Sombreador de intersección**](intersection-shader.md)





## <a name="see-also"></a>Consulte también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




