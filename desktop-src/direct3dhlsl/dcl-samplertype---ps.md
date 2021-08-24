---
title: dcl_samplerType (sm2, sm3 - ps asm)
description: Declare un muestreador de sombreador de píxeles.
ms.assetid: c90ff5b6-f89a-4993-8a5d-dbbc4a7896b0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 764c3b992cd248a8900c3762c7c9e68abd3bed973ca4f7d44b1705122984f321
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726745"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a>dcl \_ samplerType (sm2, sm3 - ps asm)

Declare un muestreador de sombreador de píxeles.

## <a name="syntax"></a>Syntax

dcl \_ samplerType s\#



 

donde:

-   \_samplerType define el tipo de datos sampler. Esto determina cuántas coordenadas son necesarias para cada coordenada de textura al realizar el muestreo. Se definen las siguientes dimensiones de coordenadas de textura.
    -   \_2d
    -   \_Cubo
    -   \_Volumen
-   s \# identifica un muestreador donde s es una abreviatura del muestreador y \# es el número del muestreador. Los muestreadores son pseudo registros porque no se pueden leer ni escribir directamente en ellos.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dcl \_ samplerType      |      |      |      |      | x    | x    | x     | x    | x     |



 

Todas las instrucciones \_ dcl samplerType deben aparecer antes de la primera instrucción ejecutable.

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

 

 




