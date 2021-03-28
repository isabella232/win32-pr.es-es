---
title: Modelo de sombreador HLSL 6,4
description: Describe los intrínsecos de machine learning agregados al modelo de sombreador de HLSL 6,4.
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 10e74b268243ab059c2d0945887a6d429d40bb53
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "103914262"
---
# <a name="hlsl-shader-model-64"></a>Modelo de sombreador HLSL 6,4

Describe los intrínsecos de machine learning agregados al modelo de sombreador de HLSL 6,4.

## <a name="shader-model-64"></a>Modelo de sombreador 6,4
Estos intrínsecos son una característica necesaria o compatible del modelo de sombreador 6,4. Por consiguiente, no se requiere ninguna comprobación de bits de funcionalidad independiente, más allá de garantizar el uso del modelo de sombreador 6,4. El cliente mínimo admitido para estas rutinas es Windows 10, versión 1903.

## <a name="shading-language-intrinsics"></a>Intrínsecos del lenguaje de sombreado

### <a name="unsigned-integer-dot-product-of-4-elements-and-accumulate"></a>Entero sin signo Dot-Product de 4 elementos y acumular
```syntax
uint32 dot4add_u8packed(uint32 a, uint32 b, uint32 acc); // ubyte4 a, b;
```
 
Entero sin signo de 4 dimensiones-producto con agregar. Multiplica cada par correspondiente de bytes int sin signo de 8 bits en los dos DWORDs de entrada y suma los resultados en el acumulador de enteros de 32 bits sin signo. Esta instrucción funciona en una única calle de SIMD de 32 bits. También se supone que las entradas son cantidades de 32 bits.
 
### <a name="signed-integer-dot-product-of-4-elements-and-accumulate"></a>Entero con signo Dot-Product de 4 elementos y acumular
```syntax
int32 dot4add_i8packed(uint32 a, uint32 b, int32 acc); // signed byte4 a, b;
```

Entero de cuatro dimensiones con signo de un producto con agregar. Multiplica juntos cada par correspondiente de bytes int con signo de 8 bits en los dos DWORDs de entrada y suma los resultados en el acumulador de enteros con signo de 32 bits. Esta instrucción funciona en una única calle de SIMD de 32 bits. También se supone que las entradas son cantidades de 32 bits.
 
### <a name="single-precision-floating-point-2-element-dot-product-and-accumulate"></a>Punto flotante de precisión simple de 2 elementos Dot-Product y acumulado
```syntax
float dot2add( half2 a, half2 b, float acc );
```

Producto de punto flotante de 2 dimensiones de vectores half2 con Add. Multiplica los elementos de los dos vectores de entrada Float de media precisión y suma los resultados en el acumulador de punto flotante de 32 bits. Estas instrucciones operan en una única calle de SIMD de 32 bits. Las entradas son cantidades de 16 bits empaquetadas en la misma calle.

Esto se trata en el bit de características de baja precisión (lo que indica que la compatibilidad media y corta nativa está presente).

### <a name="sv_shadingrate"></a>SV_ShadingRate
```syntax
uint shadingRate : SV_ShadingRate
```

Entero sin signo que representa el número de píxeles de destino escritos por cada invocación del sombreador de píxeles. Los valores válidos pertenecen al conjunto de valores de enumeración [D3D12_SHADING_RATE](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate).

Este valor del sistema está disponible en plataformas [D3D12_VARIABLE_SHADING_RATE_TIER_2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) o superior. Se puede escribir como máximo una de las fases del sombreador de vértices o de geometría. Se puede leer desde la fase del sombreador de píxeles. Para obtener más información, vea el [sombreado de velocidad variable](../direct3d12/vrs.md).