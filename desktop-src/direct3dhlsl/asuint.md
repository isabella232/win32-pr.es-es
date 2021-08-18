---
title: función asuint
description: Reinterpreta el patrón de bits de un valor de 64 bits como dos enteros de 32 bits sin signo.
ms.assetid: 29671661-4fec-46e5-9b6f-56fba8e1d756
keywords:
- Función HLSL de asuint
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02f0df4d31ca978b8b58b50cd0c91710056aa9ac0f3cac1ae370a4edba6a9edf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626595"
---
# <a name="asuint-function"></a>función asuint

Reinterpreta el patrón de bits de un valor de 64 bits como dos enteros de 32 bits sin signo.

## <a name="syntax"></a>Sintaxis

``` syntax
void asuint(
  in  double value,
  out uint lowbits,
  out uint highbits
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ En\]
</dt> <dd>

Tipo: **double**

Valor de entrada.

</dd> <dt>

*lowbits* \[ out\]
</dt> <dd>

Tipo: **uint**

Patrón de 32 bits bajo de *valor*.

</dd> <dt>

*highbits* \[ out\]
</dt> <dd>

Tipo: **uint**

Patrón alto de 32 bits de *valor*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Esta función es una versión alternativa del intrínseco [**asuint**](dx-graphics-hlsl-asuint.md) que ha estado disponible en modelos de sombreador anteriores y se introdujo para El modelo de sombreador 5. La función original (reconocida en el compilador hlsl por su firma diferente) sigue estando disponible para el modelo de sombreador 5.

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelos de sombreador 5](d3d11-graphics-reference-sm5.md) y superiores | Sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




