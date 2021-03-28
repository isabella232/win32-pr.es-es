---
title: DP3-PS
description: Calcula el producto de tres componentes de los registros de origen. | DP3-PS
ms.assetid: a365acd1-89c0-4340-8f51-8e478f84ddc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09e4178f6aedbfb5242f4c545d624f1d07796008
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986363"
---
# <a name="dp3---ps"></a>DP3-PS

Calcula el producto de tres componentes de los registros de origen.

## <a name="syntax"></a>Sintaxis



| DP3 DST, src0, SRC1 |
|---------------------|



 

, donde

-   DST es el registro de destino.
-   src0 es un registro de origen.
-   SRC1 es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp3                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

En el fragmento de código siguiente se muestran las operaciones realizadas:


```
dest.x = dest.y = dest.z = dest.w = 
  (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
```



Esta instrucción se ejecuta en la canalización de vectores, escribiendo siempre en los canales de color. En el caso de \_ la versión 4, esta instrucción todavía utiliza la canalización de vectores, pero puede escribir en cualquier canal.

Una instrucción con una máscara de escritura de Register. RGB (. XYZ) de destino puede coexistir con DP3, como se muestra a continuación.


```
dp3 r0.rgb, t0, v0            // Copy scalar result to color components
+mov r2.a, t0                 // Copy alpha component from t0 in parallel 
```



La instrucción DP3 se puede modificar mediante el uso del modificador de argumento de entrada de [ajuste de escala firmado del registro de origen](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) aplicado a sus argumentos de entrada si aún no se han expandido al intervalo dinámico con firma. En el caso de un sombreador de iluminación, el modificador de instrucciones saturadas ( \_ SAT) suele usarse para fijar los valores negativos a negro, como se muestra en el ejemplo siguiente.


```
dp3_sat r0, t0_bx2, v0_bx2    // t0 is a bump map, v0 contains the light direction
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




