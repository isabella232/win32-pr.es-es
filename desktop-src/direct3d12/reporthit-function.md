---
description: Lo llama un sombreador de intersección para notificar una intersección de rayo.
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
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705365"
---
# <a name="reporthit-function"></a>Función ReportHit

Lo llama un [sombreador de intersección](intersection-shader.md) para notificar una intersección de rayo.

## <a name="syntax"></a>Sintaxis
Esta definición de función intrínseca es equivalente a la siguiente plantilla de función:

```
template<attr_t>
bool ReportHit(float THit, uint HitKind, attr_t Attributes);
```



## <a name="parameters"></a>Parámetros

`THit`

Un valor de tipo float que especifica la distancia paramétrica de la intersección.

`HitKind`

Entero sin signo que identifica el tipo de acierto que se ha producido.  Este es un valor especificado por el usuario en el intervalo de 0-127.  El valor se puede leer en [cualquier](any-hit-shader.md) sombreado de posicionamiento o de [posicionamiento más cercano](closest-hit-shader.md) con el intrínseco **HitKind** .

`Attributes`

Estructura del atributo de [**intersección**](intersection-attributes.md) definido por el usuario que especifica los atributos de intersección.  

## <a name="return-value"></a>Valor devuelto

**booleano** True si se aceptó el acierto.  Se rechaza una visita si *THit* está fuera del intervalo de rayo actual, o el sombreador de aciertos llama a [**IgnoreHit**](ignorehit-function.md).  El intervalo de rayo actual está definido por **RayTMin** y **RayTCurrent**.

## <a name="remarks"></a>Observaciones

Se puede llamar a esta función desde los siguientes tipos de sombreador raytracing:

* [**Sombreador de intersección**](intersection-shader.md)





## <a name="see-also"></a>Vea también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




