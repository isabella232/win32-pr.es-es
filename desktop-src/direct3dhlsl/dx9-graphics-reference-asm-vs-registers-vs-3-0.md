---
title: 'Registros: vs_3_0'
description: Esta sección contiene información de referencia para los registros de entrada y salida implementados por la versión 3 0 del sombreador de \_ vértices.
ms.assetid: af81f1c4-9c11-455e-a565-1b80f1ee8683
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d658d2d14d149d5d83d673269f2a414d7feaa22f13f1b32f57c4b80500fb1398
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673105"
---
# <a name="registers---vs_3_0"></a>Registros: vs \_ 3 \_ 0

Esta sección contiene información de referencia para los registros de entrada y salida implementados por la versión 3 0 del sombreador de \_ vértices.

## <a name="input-registers"></a>Registros de entrada



| Registrarse | Nombre                                                                                      | Count      | L/E | \# Lectura de puertos | \# Lecturas/inst | Dimensión | RelAddr | Valores predeterminados     | Requiere DCL |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| V\#      | [Registro de entrada](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | ilimitadas       | 4         | a0/aL   | Vea la nota 1.   | Sí          |
| R\#      | [Registro temporal](dx9-graphics-reference-asm-vs-registers-temporary.md)               | 32         | L/E | 3             | ilimitadas       | 4         | No      | Ninguno         | No           |
| c\#      | [Registro flotante constante](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | Consulte la nota 2. | R   | 1             | ilimitadas       | 4         | a0/aL   | (0, 0, 0, 0) | No           |
| a0       | [Registro de direcciones](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | L/E | 1             | ilimitadas       | 4         | No      | Ninguno         | No           |
| b\#      | [Registro booleano constante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | No      | FALSE        | No           |
| i\#      | [Registro de enteros constantes](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | No      | (0, 0, 0, 0) | No           |
| aL       | [Registro de contador de bucles](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | ilimitadas       | 1         | No      | Ninguno         | No           |
| p0       | [Registro de predicado](dx9-graphics-reference-asm-vs-registers-predicate.md)               | 1          | L/E | 1             | 1               | 4         | No      | ninguno         | No           |
| s\#      | [Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)        | 4          | R   | 1             | 1               | 4         | No      | Vea la nota 3.   | Sí          |



 

Notas:

1.  Parcial (0, 0, 0, 1): si solo se actualiza un subconjunto de canales, el valor predeterminado de los canales restantes será (0, 0, 0, 1).
2.  Igual a D3DCAPS9. MaxVertexShaderConst (al menos 256 para frente \_ a 3 \_ 0).
3.  Existen valores predeterminados para la búsqueda del muestreador, pero los valores dependen del formato de textura.

## <a name="output-registers"></a>Registros de salida

Los registros de salida se han contraído en 12 \# registros (salida). Se pueden usar para cualquier cosa que el usuario quiera interpolar para el sombreador de píxeles: coordenadas de textura, colores, color, etc.



| Registrarse | Nombre            | Count | L/E | Dimensión | RelAddr | Valores predeterminados | Requiere DCL |
|----------|-----------------|-------|-----|-----------|---------|----------|--------------|
| o\#      | Registro de salida | 12    | W   | 4         | aL      | Ninguno     | Sí          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




