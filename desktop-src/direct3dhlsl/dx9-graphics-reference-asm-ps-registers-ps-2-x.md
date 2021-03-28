---
title: ps_2_x registros
description: Los sombreadores de píxeles dependen de los registros para obtener datos de vértices, de salida de datos de píxeles, para conservar los resultados temporales durante los cálculos y para identificar las fases de muestreo de textura.
ms.assetid: 52bb6290-46e2-4d7d-9b96-b4c3e2abfe43
keywords:
- 'Registros: ps_2_x'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 880c897aa3d812d1e94e5dc408e97ec18b5de106
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984002"
---
# <a name="ps_2_x-registers"></a>Registros de PS \_ 2 \_ x

Los sombreadores de píxeles dependen de los registros para obtener datos de vértices, de salida de datos de píxeles, para conservar los resultados temporales durante los cálculos y para identificar las fases de muestreo de textura. Hay varios tipos de registros, cada uno con una funcionalidad única. Esta sección contiene información de referencia de los registros de entrada y salida implementados por el sombreador de píxeles versión 2 \_ x.

## <a name="input-register-types"></a>Tipos de registro de entrada



| Registrarse | Nombre                                                                                          | Count      | L/E        | \# Leer puertos | \# Lecturas/inst. | Dimensión | RelAddr | Valores predeterminados                  | Requiere DCL |
|----------|-----------------------------------------------------------------------------------------------|------------|------------|---------------|---------------|-----------|---------|---------------------------|--------------|
| v\#      | [Registro del color de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md)               | 2          | R          | 1             | Sin límite     | 4         | N       | Partial (0001). Vea la nota 4 | Y            |
| c\#      | [Registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md)                   | Vea la nota 1 | L/E        | 3             | Sin límite     | 4         | N       | Ninguno                      | N            |
| c\#      | [Registro Float constante](dx9-graphics-reference-asm-ps-registers-constant-float.md)         | 32         | R          | 1             | 2             | 4         | N       | 0000                      | N            |
| Configur\#      | [Registro de entero constante](dx9-graphics-reference-asm-ps-registers-constant-integer.md)     | 16         | Consulte la nota 2. | 1             | 1             | 4         | N       | 0000                      | N            |
| b\#      | [Registro booleano constante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md)     | 16         | Consulte la nota 2. | 1             | 1             | 1         | N       | false                     | N            |
| P0       | [Registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md)                   | 1          | Consulte la nota 2. | 1             | 1             | 1         | N       | Ninguno                      | Y            |
| s\#      | [Muestra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md)            | 16         | Vea la nota 3 | 1             | 1             | 4         | N       | Vea la nota 5                | Y            |
| h\#      | [Registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) | 8          | R          | 1             | 1             | 4         | N       | Ninguno                      | Y            |



 

Notas:

1.  12 min/32 máx.: el número de \# registros de r viene determinado por D3DPSHADERCAPS2 \_ 0. NumTemps (que oscila entre 12 y 32).
2.  Solo se puede usar en una instrucción de control de flujo.
3.  Solo se puede usar mediante una instrucción de muestreo de textura.
4.  Partial (x, y, z, w): si solo se actualiza un subconjunto de canales en el registro, los canales restantes tendrán como valor predeterminado los valores especificados (x, y, z, w).
5.  Existen valores predeterminados para las búsquedas de muestra, pero los valores dependen del formato de textura.

El número de readports es el número de registros diferentes (para cada tipo de registro) que se pueden leer en una única instrucción.

## <a name="output-register-types"></a>Tipos de registro de salida



| Registrarse | Nombre                                                                              | Count                                                                             | L/E | Dimensión | RelAddr | Valores predeterminados | Requiere DCL |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| Opcional #     | [Registro de color de salida](dx9-graphics-reference-asm-ps-registers-output-color.md) | Ver [texturas de varios elementos (Direct3D 9)](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | N       | Ninguno     | N            |
| oDepth   | [Registro de profundidad de salida](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | N       | Ninguno     | N            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registra](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 