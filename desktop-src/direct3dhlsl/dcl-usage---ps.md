---
title: dcl_semantics (SM3-PS ASM)
description: Declare la asociación entre la salida del sombreador de vértices y la entrada del sombreador de píxeles.
ms.assetid: 4f4dc6fe-0efa-4d84-aefd-583e90ab9a61
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 944ddd2b581c6179ac4a3fe22f2b687f85aecfdc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149432"
---
# <a name="dcl_semantics-sm3---ps-asm"></a>\_semántica de DCL (SM3-PS ASM)

Declare la asociación entre la salida del sombreador de vértices y la entrada del sombreador de píxeles.

## <a name="syntax"></a>Sintaxis



|                                                   |
|---------------------------------------------------|
| \_semántica de DCL \[ \_ centroide \] DST \[ . Write \_ Mask\] |



 

Donde:

-   \_semántica: identifica el uso de datos previsto y puede ser cualquiera de los valores de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (sin el \_ prefijo D3DDECLUSAGE). Además, se puede anexar un índice de entero a la semántica para distinguir los parámetros que utilizan una semántica similar.
-   \[\_[Centroide](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md) \] es un modificador de instrucción opcional. Es compatible con \_ las instrucciones de uso de DCL que declaran los registros de entrada y las instrucciones de búsqueda de texturas. El centroide se anexa sin espacio.
-   DST: registro de destino. Vea [registros de PS \_ 3 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).
-   escribir \_ máscara: el mismo registro de salida se puede declarar varias veces, cada vez con una máscara de escritura única (por lo que se pueden aplicar diferentes semánticas a componentes individuales). Sin embargo, no se puede usar la misma semántica varias veces en una declaración. Esto significa que los vectores deben tener cuatro componentes o menos y no pueden pasar por los límites de registro de cuatro componentes (registros de salida individuales). Cuando \_ se usa la semántica psize, debe tener una máscara de escritura completa porque se considera un escalar. Cuando \_ se usa la semántica de posición, debe tener una máscara de escritura completa porque se deben escribir los cuatro componentes.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| uso de DCL \_            |      |      |      |      |      |      |       | x    | x     |



 

Todas \_ las instrucciones de uso de DCL deben aparecer antes de la primera instrucción ejecutable.

## <a name="declaration-examples"></a>Ejemplos de declaraciones


```
ps_3_0

; Declaring inputs
dcl_normal      v0.xyz
dcl_blendweight v0.w ; Must be same reg# as normal, matching vshader packing
dcl_texcoord1   v1.y ; Mask can be any subset of mask from vshader semantic
dcl_texcoord0   v1.zw; Has to be same reg# as texcoord1, to match vshader

; Declaring samplers
dcl_2d s0
dcl_2d s1

def c0, 0, 0, 0, 0

mov r0.x, v1.y ; texcoord1
mov r0.y, c0
texld r0, r0, s0

texld r1, v1.zw, s1
...
(output regs in ps_3_0 are same as ps_2_0: oC0-oC3, oDepth)
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[Ejemplo antialias](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)
</dt> </dl>

 

 