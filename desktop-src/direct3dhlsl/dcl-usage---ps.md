---
title: dcl_semantics (sm3 - ps asm)
description: Declare la asociación entre la salida del sombreador de vértices y la entrada del sombreador de píxeles.
ms.assetid: 4f4dc6fe-0efa-4d84-aefd-583e90ab9a61
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91a57ec2eabbef2cd62fec8fa95fbf9d2da47a5bfcdb339bf30ed8da5b11c9ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792934"
---
# <a name="dcl_semantics-sm3---ps-asm"></a>Semántica de dcl \_ (sm3 - ps asm)

Declare la asociación entre la salida del sombreador de vértices y la entrada del sombreador de píxeles.

## <a name="syntax"></a>Sintaxis

dcl \_ semantics \[ \_ centroid \] dst \[ .write \_ mask\]



 

Donde:

-   \_semántica: identifica el uso de datos previsto y puede ser cualquiera de los valores de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (sin el prefijo D3DDECLUSAGE). \_ Además, se puede anexar un índice entero a la semántica para distinguir los parámetros que usan una semántica similar.
-   \[\_[Centroide](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md) \] es un modificador de instrucción opcional. Se admite en las instrucciones de uso de dcl que declaran los registros de entrada \_ y en las instrucciones de búsqueda de textura. El centroide se anexa sin espacio.
-   dst: registro de destino. Consulte [ps \_ 3 \_ 0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).
-   write mask: el mismo registro de salida se puede declarar varias veces, cada vez con una máscara de escritura única (por lo que se puede aplicar una semántica diferente \_ a componentes individuales). Sin embargo, la misma semántica no se puede usar varias veces en una declaración. Esto significa que los vectores deben ser cuatro componentes o menos y no pueden pasar por los límites de registro de cuatro componentes (registros de salida individuales). Cuando se \_ usa la semántica de psize, debe tener una máscara de escritura completa porque se considera escalar. Cuando se usa la semántica de posición, debe tener máscara de escritura completa porque se deben escribir \_ los cuatro componentes.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Uso \_ de dcl            |      |      |      |      |      |      |       | x    | x     |



 

Todas las instrucciones de uso de dcl \_ deben aparecer antes de la primera instrucción ejecutable.

## <a name="declaration-examples"></a>Ejemplos de declaración


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

[Ejemplo de suavizado de contorno](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)
</dt> </dl>

 

 
