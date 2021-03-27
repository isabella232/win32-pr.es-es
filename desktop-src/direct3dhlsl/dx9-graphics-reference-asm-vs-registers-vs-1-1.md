---
title: 'Registros: vs_1_1'
description: Esta sección contiene información de referencia de los registros de entrada y salida implementados por la versión 1 del sombreador de vértices \_ .
ms.assetid: 8b19a0da-1561-450f-a36a-35ac7ea6e17a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e6776fef206f9ced0608e86cbf596585399d4a12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903691"
---
# <a name="registers---vs_1_1"></a>Registros-vs \_ 1 \_ 1

Esta sección contiene información de referencia de los registros de entrada y salida implementados por la versión 1 del sombreador de vértices \_ .

## <a name="input-registers"></a>Registros de entrada



| Registrarse | Nombre                                                                                  | Count      | L/E | \# Leer puertos | \# Lecturas/inst. | Dimensión  | RelAddr | Valores predeterminados     | Requiere DCL |
|----------|---------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|------------|---------|--------------|--------------|
| a0       | [Registro de direcciones](dx9-graphics-reference-asm-vs-registers-address.md)               | 1          | L/E | 1             | Sin límite       | Vea la nota 3 | No      | None         | No           |
| c\#      | [Registro Float constante](dx9-graphics-reference-asm-vs-registers-constant-float.md) | Consulte la nota 2. | R   | 1             | Sin límite       | 4          | a0. x    | (0, 0, 0, 0) | No           |
| v\#      | [Registro de entrada](dx9-graphics-reference-asm-vs-registers-input.md)                   | 16         | R   | 1             | Sin límite       | 4          | No      | Vea la nota 1   | Sí          |
| c\#      | [Registro temporal](dx9-graphics-reference-asm-vs-registers-temporary.md)           | 12         | L/E | 3             | Sin límite       | 4          | No      | None         | No           |



 

Notas:

1.  Partial (0, 0, 0, 1): si solo se actualiza un subconjunto de canales, los canales restantes tendrán como valor predeterminado (0, 0, 0, 1).
2.  Igual a D3DCAPS9. MaxVertexShaderConst (al menos 96 para vs \_ 1 \_ 1).
3.  Solo está disponible el canal. x.

## <a name="output-registers"></a>Registros de salida



| Registrarse | Nombre                        | Count | L/E | Dimensión | RelAddr | Valores predeterminados | Requiere DCL |
|----------|-----------------------------|-------|-----|-----------|---------|----------|--------------|
| oPos     | Registro de posición           | 1     | W   | 4         | No      | None     | No           |
| oFog     | Registro de niebla                | 1     | W   | 1         | No      | None     | No           |
| Aporta     | Registro de tamaño de punto         | 1     | W   | 1         | No      | None     | No           |
| DP\#     | Registro de color; Vea la nota 1  | 2     | W   | 4         | No      | None     | No           |
| OTR\#     | Registro de coordenadas de textura | 8     | W   | 4         | No      | None     | No           |



 

Notas:

-   oD0 es la salida de color difuso; oD1 es la salida del color especular.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




