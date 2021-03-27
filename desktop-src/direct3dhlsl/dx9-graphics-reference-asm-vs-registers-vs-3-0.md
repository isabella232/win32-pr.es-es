---
title: 'Registros: vs_3_0'
description: Esta sección contiene información de referencia de los registros de entrada y salida implementados por el sombreador de vértices versión 3 \_ 0.
ms.assetid: af81f1c4-9c11-455e-a565-1b80f1ee8683
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47353a3f312a2abbd6f4fe5ea1dcd1ed9495a9d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778312"
---
# <a name="registers---vs_3_0"></a>Registros-vs \_ 3 \_ 0

Esta sección contiene información de referencia de los registros de entrada y salida implementados por el sombreador de vértices versión 3 \_ 0.

## <a name="input-registers"></a>Registros de entrada



| Registrarse | Nombre                                                                                      | Count      | L/E | \# Leer puertos | \# Lecturas/inst. | Dimensión | RelAddr | Valores predeterminados     | Requiere DCL |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| v\#      | [Registro de entrada](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | Sin límite       | 4         | a0/aL   | Vea la nota 1   | Sí          |
| c\#      | [Registro temporal](dx9-graphics-reference-asm-vs-registers-temporary.md)               | 32         | L/E | 3             | Sin límite       | 4         | No      | None         | No           |
| c\#      | [Registro Float constante](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | Consulte la nota 2. | R   | 1             | Sin límite       | 4         | a0/aL   | (0, 0, 0, 0) | No           |
| a0       | [Registro de direcciones](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | L/E | 1             | Sin límite       | 4         | No      | None         | No           |
| b\#      | [Registro booleano constante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | No      | FALSE        | No           |
| Configur\#      | [Registro de entero constante](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | No      | (0, 0, 0, 0) | No           |
| Alabama       | [Registro de contador de bucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | Sin límite       | 1         | No      | None         | No           |
| P0       | [Registro de predicado](dx9-graphics-reference-asm-vs-registers-predicate.md)               | 1          | L/E | 1             | 1               | 4         | no      | ninguno         | no           |
| s\#      | [Muestra (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)        | 4          | R   | 1             | 1               | 4         | No      | Vea la nota 3   | Sí          |



 

Notas:

1.  Partial (0, 0, 0, 1): si solo se actualiza un subconjunto de canales, los canales restantes tendrán como valor predeterminado (0, 0, 0, 1).
2.  Igual a D3DCAPS9. MaxVertexShaderConst (al menos 256 para vs \_ 3 \_ 0).
3.  Existen valores predeterminados para la búsqueda de muestra, pero los valores dependen del formato de textura.

## <a name="output-registers"></a>Registros de salida

Los registros de salida se han contraer en 12 \# registros o (salida). Se pueden usar para cualquier elemento que el usuario quiera interpolar para el sombreador de píxeles: coordenadas de textura, colores, niebla, etc.



| Registrarse | Nombre            | Count | L/E | Dimensión | RelAddr | Valores predeterminados | Requiere DCL |
|----------|-----------------|-------|-----|-----------|---------|----------|--------------|
| aceptar\#      | Registro de salida | 12    | W   | 4         | Alabama      | Ninguno     | Sí          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




