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
ms.openlocfilehash: 8c5cdf4e0a71430d6375fd75ca553f92ca9539b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966872"
---
# <a name="callshader-function"></a>Función CallShader

Invoca otro sombreador desde dentro de un sombreador.

## <a name="syntax"></a>Sintaxis
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

## <a name="remarks"></a>Observaciones

Se puede llamar a esta función desde los siguientes tipos de sombreador de raytracción:

* [**Sombreador al que se puede llamar**](callable-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de errores**](miss-shader.md)
* [**Sombreador de generación de rayos**](ray-generation-shader.md)



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




