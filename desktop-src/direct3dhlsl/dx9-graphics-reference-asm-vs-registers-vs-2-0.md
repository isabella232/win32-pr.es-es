---
title: 'Registros: vs_2_0'
description: Esta sección contiene información de referencia de los registros de entrada y salida implementados por el sombreador de vértices versión 2 \_ 0.
ms.assetid: e5ef015e-1e4d-41b3-95da-3b44ef0bd73e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 156367ec08a5f1ecd94181be56558f4ba07005b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075569"
---
# <a name="registers---vs_2_0"></a>Registros-vs \_ 2 \_ 0

Esta sección contiene información de referencia de los registros de entrada y salida implementados por el sombreador de vértices versión 2 \_ 0.

## <a name="input-registers"></a>Registros de entrada



| Registrarse | Nombre                                                                                      | Count      | L/E | \# Leer puertos | \# Lecturas/inst. | Dimensión | RelAddr | Valores predeterminados     | Requiere DCL |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| v\#      | [Registro de entrada](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | Sin límite       | 4         | No      | Vea la nota 1   | Sí          |
| c\#      | [Registro temporal](dx9-graphics-reference-asm-vs-registers-temporary.md)               | 12         | L/E | 3             | Sin límite       | 4         | No      | None         | No           |
| c\#      | [Registro Float constante](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | Consulte la nota 2. | R   | 1             | 2               | 4         | a0/aL | (0, 0, 0, 0) | No           |
| a0       | [Registro de direcciones](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | L/E | 1             | 2               | 4         | No      | None         | No           |
| b\#      | [Registro booleano constante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | No      | FALSE        | No           |
| Configur\#      | [Registro de entero constante](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | No      | (0, 0, 0, 0) | No           |
| Alabama       | [Registro de contador de bucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | 2               | 1         | No      | None         | No           |



 

Notas:

1.  Partial (0, 0, 0, 1): si solo se actualiza un subconjunto de canales, los canales restantes tendrán como valor predeterminado (0, 0, 0, 1).
2.  Igual a D3DCAPS9. MaxVertexShaderConst (al menos 256 para vs \_ 2 \_ 0).

## <a name="output-registers"></a>Registros de salida



| Registrarse | Nombre                                                                                          | Count | L/E | Dimensión | RelAddr | Valores predeterminados | Requiere DCL |
|----------|-----------------------------------------------------------------------------------------------|-------|-----|-----------|---------|----------|--------------|
| oPos     | [Registro de posición](dx9-graphics-reference-asm-vs-registers-position.md)                     | 1     | W   | 4         | No      | None     | No           |
| oFog     | [Registro de niebla](dx9-graphics-reference-asm-vs-registers-fog.md)                               | 1     | W   | 1         | No      | None     | No           |
| Aporta     | [Registro de tamaño de punto](dx9-graphics-reference-asm-vs-registers-point-size.md)                 | 1     | W   | 1         | No      | None     | No           |
| DP\#     | [Registro de color](dx9-graphics-reference-asm-vs-registers-color.md); Vea la nota 1               | 2     | W   | 4         | No      | None     | No           |
| OTR\#     | [Registro de coordenadas de textura](dx9-graphics-reference-asm-vs-registers-texture-coordinate.md) | 8     | W   | 4         | No      | None     | No           |



 

Notas:

-   oD0 es la salida de color difuso; oD1 es la salida del color especular.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




