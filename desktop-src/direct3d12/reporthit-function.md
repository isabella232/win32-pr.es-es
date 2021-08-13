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
ms.openlocfilehash: 8714cabc02f70ca12bcc78493de3a61482ba5aed5490087d309f6ec091cecf75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528113"
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

Entero sin signo que identifica el tipo de impacto que se produjo.  Se trata de un valor especificado por el usuario en el intervalo de 0 a 127.  El valor se puede leer [](closest-hit-shader.md) mediante [cualquier sombreador de](any-hit-shader.md) impacto o más cercano con el **intrínseco HitKind.**

`Attributes`

Estructura de atributo de [**intersección**](intersection-attributes.md) definida por el usuario que especifica los atributos de intersección.  

## <a name="return-value"></a>Valor devuelto

**bool** True si se aceptó la pulsación.  Se rechaza una pulsación si *THit* está fuera del intervalo de rayos actual o cualquier sombreador de llamadas llama [**a IgnoreHit**](ignorehit-function.md).  **RayTMin** y **RayTCurrent** definen el intervalo de rayo actual.

## <a name="remarks"></a>Observaciones

Se puede llamar a esta función desde los siguientes tipos de sombreador de raytracción:

* [**Sombreador de intersección**](intersection-shader.md)





## <a name="see-also"></a>Vea también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




