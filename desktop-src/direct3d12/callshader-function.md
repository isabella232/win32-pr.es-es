---
description: Invoca otro sombreador desde dentro de un sombreador.
ms.assetid: ''
title: Función CallShader
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- CallShader
api_type:
- NA
ms.openlocfilehash: e411ef61c34eafcef71f3e68f6700651e4b3073423afd40451f139f02826e504
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119280355"
---
# <a name="callshader-function"></a>Función CallShader

Invoca otro sombreador desde dentro de un sombreador.

## <a name="syntax"></a>Syntax
Esta definición de función intrínseca es equivalente a la siguiente plantilla de función:

```
template<param_t>
void CallShader(uint ShaderIndex, inout param_t Parameter);
```



## <a name="parameters"></a>Parámetros

`ShaderIndex`

Entero sin signo que representa el índice en la tabla de [sombreador](callable-shader.md) a la que se puede llamar especificada en la llamada a [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays.

`Parameter`

Parámetros definidos por el usuario que se pasan al sombreador al que se puede llamar.  Esta estructura de parámetros debe coincidir con la estructura de parámetros utilizada en el sombreador al que se puede llamar a la que se apunta en la tabla del sombreador.


## <a name="return-value"></a>Valor devuelto

**void**

## <a name="remarks"></a>Comentarios

Se puede llamar a esta función desde los siguientes tipos de sombreador de raytracción:

* [**Sombreador al que se puede llamar**](callable-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de errores**](miss-shader.md)
* [**Sombreador de generación de rayos**](ray-generation-shader.md)



## <a name="see-also"></a>Vea también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




