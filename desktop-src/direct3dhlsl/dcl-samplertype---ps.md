---
title: dcl_samplerType (SM2, SM3-PS ASM)
description: Declare una muestra de sombreador de píxeles.
ms.assetid: c90ff5b6-f89a-4993-8a5d-dbbc4a7896b0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 934931d6063ac264a2e6685104f8ed6fbdaaa64e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077129"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a>DCL \_ samplerType (SM2, SM3-PS ASM)

Declare una muestra de sombreador de píxeles.

## <a name="syntax"></a>Sintaxis



|                      |
|----------------------|
| DCL \_ samplerType s\# |



 

donde:

-   \_samplerType define el tipo de datos de muestra. Esto determina el número de coordenadas que requiere cada coordenada de textura al realizar el muestreo. Se definen las siguientes dimensiones de coordenadas de textura.
    -   \_2D
    -   \_BD
    -   \_cantidad
-   s \# identifica una muestra donde s es una abreviatura de la muestra y \# es el número de muestra. Los ejemplos son pseudo registros porque no se pueden leer ni escribir directamente en ellos.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| samplerType de DCL \_      |      |      |      |      | x    | x    | x     | x    | x     |



 

Todas \_ las instrucciones samplerType de DCL deben aparecer antes de la primera instrucción ejecutable.

## <a name="example"></a>Ejemplo


```
dcl_cube t0.rgb;  // Define a 3D texture map.

add r0, r0, t0;   // Perturb texture coordinates. 
texld r0, s0, r0; // Load r0 with a color sampled from stage0
                  //   at perturbed texture coordinates r0.
                  // This is a dependent texture read.
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




