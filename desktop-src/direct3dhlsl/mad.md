---
title: mad (función)
description: Realiza una operación aritmética de multiplicación y adición en tres valores.
ms.assetid: 2e58229d-2387-4319-adc6-2d66eda88bd1
keywords:
- función loca HLSL
topic_type:
- apiref
api_name:
- mad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 52e0e4819e4c78f092ee99c78403ace5d0205037db3096dfe45865c2216d486d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788825"
---
# <a name="mad-function"></a>mad (función)

Realiza una operación aritmética de multiplicación y adición en tres valores.

## <a name="syntax"></a>Sintaxis

``` syntax
numeric mad(
  in numeric mvalue,
  in numeric avalue,
  in numeric bvalue
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*mvalue* \[ En\]
</dt> <dd>

Tipo: **numérico**

Valor de multiplicación.

</dd> <dt>

*avalue* \[ En\]
</dt> <dd>

Tipo: **numérico**

Primer valor de suma.

</dd> <dt>

*bvalue* \[ En\]
</dt> <dd>

Tipo: **numérico**

Segundo valor de suma.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **numérico**

Resultado de *mvalue* \* *avalue*  +  *bvalue*.

## <a name="remarks"></a>Comentarios

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores | Sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

Los autores de  sombreadores pueden usar la instrinsía loca para dirigirse explícitamente a la instrucción de **hardware** loca en la salida del sombreador compilada, lo que resulta especialmente útil con sombreadores que marcan los resultados con la palabra clave [precisa.](dx-graphics-hlsl-appendix-keywords.md) La **instrucción loca** se puede implementar en hardware como "fusionada", lo que ofrece una precisión mayor que la implementación de una instrucción **mul** seguida de una instrucción **add,** o como una instrucción **mul**  +  **add**.

Si los autores del sombreador usan la instrinsía loca para calcular un resultado que el  sombreador ha marcado como preciso, indican al hardware que  use cualquier implementación válida de la instrucción loca (fusionada o no), siempre y cuando la implementación sea coherente para todos los usos de ese intrínseco en cualquier sombreador de ese hardware.  A continuación, los sombreadores pueden aprovechar las posibles mejoras de rendimiento mediante una instrucción **loca** nativa (frente a **mul**  +  **add)** en algún hardware. El resultado de realizar una instrucción **de** hardware loca nativa podría ser o no diferente de realizar una **mula** seguida de una **adición de**. Sin embargo, sea cual sea el resultado, el resultado debe ser coherente para que la misma operación se produzca en varios sombreadores o en distintas partes de un sombreador.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




