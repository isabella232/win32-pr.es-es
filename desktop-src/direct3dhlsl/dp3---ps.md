---
title: 'dp3: ps'
description: 'Calcula el producto de puntos de tres componentes de los registros de origen. | dp3: ps'
ms.assetid: a365acd1-89c0-4340-8f51-8e478f84ddc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49e957078832f11885ea82baf8438d712394133eb77ad8eeaba705ff0d32a9d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024635"
---
# <a name="dp3---ps"></a>dp3: ps

Calcula el producto de puntos de tres componentes de los registros de origen.

## <a name="syntax"></a>Syntax



| dp3 dst, src0, src1 |
|---------------------|



 

where

-   dst es el registro de destino.
-   src0 es un registro de origen.
-   src1 es un registro de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp3                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

El fragmento de código siguiente muestra las operaciones realizadas:


```
dest.x = dest.y = dest.z = dest.w = 
  (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
```



Esta instrucción se ejecuta en la canalización de vectores, escribiendo siempre en los canales de color. Para la versión 1 \_ 4, esta instrucción todavía usa la canalización de vectores, pero puede escribir en cualquier canal.

Se puede emitir una instrucción con una máscara de escritura .rgb (.xyz) de registro de destino con dp3 como se muestra a continuación.


```
dp3 r0.rgb, t0, v0            // Copy scalar result to color components
+mov r2.a, t0                 // Copy alpha component from t0 in parallel 
```



La instrucción dp3 se puede modificar mediante el modificador de argumento de entrada Source [Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) (bx2) aplicado a sus argumentos de entrada si aún no se han expandido al intervalo dinámico \_ firmado. En el caso de un sombreador de iluminación, el modificador de instrucción saturada (sat) se usa a menudo para fijar los valores negativos en negro, como se muestra \_ en el ejemplo siguiente.


```
dp3_sat r0, t0_bx2, v0_bx2    // t0 is a bump map, v0 contains the light direction
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




