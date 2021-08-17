---
title: Modelo de sombreador HLSL 6.4
description: Describe los intrínsecos de aprendizaje automático agregados al modelo de sombreador HLSL 6.4.
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 5e161d77439eef63547d92fcc4f47e3185ac798141d20017d7e7102ee86a38cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511839"
---
# <a name="hlsl-shader-model-64"></a>Modelo de sombreador HLSL 6.4

Describe los intrínsecos de aprendizaje automático agregados al modelo de sombreador HLSL 6.4.

## <a name="shader-model-64"></a>Modelo de sombreador 6.4
Estos intrínsecos son una característica obligatoria o compatible del modelo de sombreador 6.4. Por lo tanto, no se requiere ninguna comprobación de bits de funcionalidad independiente, más allá de asegurar el uso del modelo de sombreador 6.4. El cliente mínimo admitido para estas rutinas es Windows 10, versión 1903.

## <a name="shading-language-intrinsics"></a>Funciones intrínsecas del lenguaje de sombreado

### <a name="unsigned-integer-dot-product-of-4-elements-and-accumulate"></a>Número entero sin signo Dot-Product de 4 elementos y Acumulación
```syntax
uint32 dot4add_u8packed(uint32 a, uint32 b, uint32 acc); // ubyte4 a, b;
```
 
Entero de 4 dimensiones sin signo dot-product con add. Multiplica juntos cada par correspondiente de bytes int de 8 bits sin signo en los dos DWORD de entrada y suma los resultados en el acumulador entero de 32 bits sin signo. Esta instrucción funciona dentro de un único camino SIMD de 32 bits de ancho. También se supone que las entradas son cantidades de 32 bits.
 
### <a name="signed-integer-dot-product-of-4-elements-and-accumulate"></a>Número entero Dot-Product con signo de 4 elementos y Accumulate
```syntax
int32 dot4add_i8packed(uint32 a, uint32 b, int32 acc); // signed byte4 a, b;
```

Un entero de 4 dimensiones con signo dot-product con add. Multiplica juntos cada par correspondiente de bytes int de 8 bits con signo en los dos DWORD de entrada y suma los resultados en el acumulador entero de 32 bits con signo. Esta instrucción funciona dentro de un único camino SIMD de 32 bits de ancho. También se supone que las entradas son cantidades de 32 bits.
 
### <a name="single-precision-floating-point-2-element-dot-product-and-accumulate"></a>Punto flotante de precisión sencilla: 2 elementos Dot-Product y Accumulate
```syntax
float dot2add( half2 a, half2 b, float acc );
```

Producto de punto flotante bidimensional de half2 vectores con add. Multiplica los elementos de los dos vectores de entrada float de precisión media juntos y suma los resultados en el acumulador float de 32 bits. Estas instrucciones funcionan dentro de un único camino SIMD de 32 bits de ancho. Las entradas son cantidades de 16 bits empaquetadas en el mismo camino.

Esto se trata en el bit de la característica de baja precisión (lo que indica que hay compatibilidad nativa media y corta).

### <a name="sv_shadingrate"></a>SV_ShadingRate
```syntax
uint shadingRate : SV_ShadingRate
```

Entero sin signo que representa cuántos píxeles de destino escribe cada invocación del sombreador de píxeles. Los valores válidos pertenecen al conjunto de valores de [enumeración D3D12_SHADING_RATE](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate).

Este valor del sistema está disponible en plataformas que [D3D12_VARIABLE_SHADING_RATE_TIER_2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) o superior. Se puede escribir a partir como máximo de una de las fases del sombreador de vértices o geometría. Se puede leer desde la fase del sombreador de píxeles. Para obtener más información, vea El sombreado [de velocidad variable](../direct3d12/vrs.md).