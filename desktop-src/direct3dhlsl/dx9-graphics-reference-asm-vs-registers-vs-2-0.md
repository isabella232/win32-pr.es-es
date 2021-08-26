---
title: 'Registros: vs_2_0'
description: Esta sección contiene información de referencia para los registros de entrada y salida implementados por la versión 2 0 del sombreador de \_ vértices.
ms.assetid: e5ef015e-1e4d-41b3-95da-3b44ef0bd73e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fd31f4ce5cac538624fe736642b30cbee9ba54579ee50da9a2ccd027847e9ecc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067975"
---
# <a name="registers---vs_2_0"></a>Registros: vs \_ 2 \_ 0

Esta sección contiene información de referencia para los registros de entrada y salida implementados por la versión 2 0 del sombreador de \_ vértices.

## <a name="input-registers"></a>Registros de entrada



| Registrarse | Nombre                                                                                      | Count      | L/E | \# Puertos de lectura | \# Reads/inst | Dimensión | RelAddr | Valores predeterminados     | Requiere DCL |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| V\#      | [Registro de entrada](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | ilimitadas       | 4         | No      | Consulte la nota 1   | Sí          |
| R\#      | [Registro temporal](dx9-graphics-reference-asm-vs-registers-temporary.md)               | 12         | L/E | 3             | ilimitadas       | 4         | No      | Ninguno         | No           |
| c\#      | [Registro flotante constante](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | Consulte la nota 2. | R   | 1             | 2               | 4         | a0/aL | (0, 0, 0, 0) | No           |
| a0       | [Registro de direcciones](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | L/E | 1             | 2               | 4         | No      | Ninguno         | No           |
| b\#      | [Registro booleano constante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | No      | FALSE        | No           |
| i\#      | [Registro de enteros constantes](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | No      | (0, 0, 0, 0) | No           |
| aL       | [Registro de contadores de bucles](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | 2               | 1         | No      | Ninguno         | No           |



 

Notas:

1.  Parcial (0, 0, 0, 1): si solo se actualiza un subconjunto de canales, el valor predeterminado de los canales restantes será (0, 0, 0, 1).
2.  Igual a D3DCAPS9. MaxVertexShaderConst (al menos 256 para frente \_ a 2 \_ 0).

## <a name="output-registers"></a>Registros de salida



| Registrarse | Nombre                                                                                          | Count | L/E | Dimensión | RelAddr | Valores predeterminados | Requiere DCL |
|----------|-----------------------------------------------------------------------------------------------|-------|-----|-----------|---------|----------|--------------|
| Opos     | [Registro de posición](dx9-graphics-reference-asm-vs-registers-position.md)                     | 1     | W   | 4         | No      | Ninguno     | No           |
| oFog     | [Registro de Registrar](dx9-graphics-reference-asm-vs-registers-fog.md)                               | 1     | W   | 1         | No      | Ninguno     | No           |
| Opta     | [Registro de tamaño de punto](dx9-graphics-reference-asm-vs-registers-point-size.md)                 | 1     | W   | 1         | No      | Ninguno     | No           |
| Od\#     | [Registro de color](dx9-graphics-reference-asm-vs-registers-color.md); Consulte la nota 1.               | 2     | W   | 4         | No      | Ninguno     | No           |
| Ot\#     | [Registro de coordenadas de textura](dx9-graphics-reference-asm-vs-registers-texture-coordinate.md) | 8     | W   | 4         | No      | Ninguno     | No           |



 

Notas:

-   oD0 es la salida de color difuso; oD1 es la salida de color especular.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




