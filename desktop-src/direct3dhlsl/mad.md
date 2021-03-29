---
title: mad (función)
description: Realiza una operación aritmética de multiplicación/suma con tres valores.
ms.assetid: 2e58229d-2387-4319-adc6-2d66eda88bd1
keywords:
- HLSL de la función de Mad
topic_type:
- apiref
api_name:
- mad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 208b1bbc87c430ca5a58a70fb3c86f9edae762bf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104487166"
---
# <a name="mad-function"></a>mad (función)

Realiza una operación aritmética de multiplicación/suma con tres valores.

## <a name="syntax"></a>Sintaxis

``` syntax
numeric mad(
  in numeric mvalue,
  in numeric avalue,
  in numeric bvalue
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*mvalue* \[ de\]
</dt> <dd>

Tipo: **Numeric**

Valor de multiplicación.

</dd> <dt>

*un valorque* \[ de\]
</dt> <dd>

Tipo: **Numeric**

Primer valor de suma.

</dd> <dt>

*bValue* \[ de\]
</dt> <dd>

Tipo: **Numeric**

Segundo valor de suma.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **Numeric**

Resultado de *mvalue* \* *un valorque*  +  *bValue*.

## <a name="remarks"></a>Observaciones

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores | sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

Los autores del sombreador pueden usar el intrínsecas de **Mad** para dirigirse explícitamente a la instrucción de hardware de **Mad** en el resultado del sombreador compilado, lo que es especialmente útil con los sombreadores que marcan los resultados con la palabra clave [precisa](dx-graphics-hlsl-appendix-keywords.md) . La instrucción de **Mad** se puede implementar en hardware como "fusionada", que ofrece mayor precisión que la implementación de una instrucción **mul** seguida de una instrucción **Add** o como un tipo **mul**  +  **Add**.

Si los autores del sombreador usan el intrínsecas de **Mad** para calcular un resultado que el sombreador marcó como preciso, indican al hardware que use cualquier implementación válida de la instrucción de **Mad** (fusionada o no), siempre que la implementación sea coherente para todos los usos de la función intrínseca de **Mad** en cualquier sombreador de ese hardware. Los sombreadores pueden aprovechar mejor las posibles mejoras de rendimiento mediante el uso de una instrucción nativa de **Mad** (frente a la   +  **adición** de Mul) en algún hardware. El resultado de realizar una instrucción de hardware de **Mad** nativa puede ser o no diferente de la realización de un **mul** seguido de una **adición**. Sin embargo, en cualquier caso, el resultado debe ser coherente para que se produzca la misma operación en varios sombreadores o en partes diferentes de un sombreador.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




