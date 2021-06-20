---
title: ps_2_x registros
description: Este artículo contiene información de referencia para los registros de entrada y salida implementados por la versión del sombreador de píxeles 2_x.
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
ms.openlocfilehash: be0e7f282978ada28c2dd71dc7c16dd317ddce42
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406708"
---
# <a name="ps_2_x-registers"></a>ps \_ 2 \_ x Registros

Los sombreadores de píxeles dependen de los registros para obtener datos de vértices, generar datos de píxeles, contener resultados temporales durante los cálculos e identificar fases de muestreo de textura. Hay varios tipos de registros, cada uno con una funcionalidad única. Esta sección contiene información de referencia para los registros de entrada y salida implementados por el sombreador de píxeles versión 2 \_ x.

## <a name="input-register-types"></a>Tipos de registro de entrada



| Registrarse | Nombre                                                                                          | Count      | L/E        | \# Lectura de puertos | \# Lecturas/inst | Dimensión | RelAddr | Valores predeterminados                  | Requiere DCL |
|----------|-----------------------------------------------------------------------------------------------|------------|------------|---------------|---------------|-----------|---------|---------------------------|--------------|
| V\#      | [Registro de color de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md)               | 2          | R          | 1             | Sin límite     | 4         | No       | Partial(0001). Consulte la nota 4 | esté            |
| R\#      | [Registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md)                   | Consulte la nota 1 | L/E        | 3             | Sin límite     | 4         | No       | Ninguno                      | No            |
| c\#      | [Registro flotante constante](dx9-graphics-reference-asm-ps-registers-constant-float.md)         | 32         | R          | 1             | 2             | 4         | No       | 0000                      | No            |
| i\#      | [Registro de enteros constantes](dx9-graphics-reference-asm-ps-registers-constant-integer.md)     | 16         | Consulte la nota 2. | 1             | 1             | 4         | No       | 0000                      | No            |
| b\#      | [Registro booleano constante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md)     | 16         | Consulte la nota 2. | 1             | 1             | 1         | No       | FALSE                     | No            |
| p0       | [Registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md)                   | 1          | Consulte la nota 2. | 1             | 1             | 1         | No       | Ninguno                      | esté            |
| s\#      | [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md)            | 16         | Vea la nota 3. | 1             | 1             | 4         | No       | Consulte la nota 5                | esté            |
| T\#      | [Registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) | 8          | R          | 1             | 1             | 4         | No       | Ninguno                      | esté            |



 

Notas:

1.  12 min/32 max: el número de registros de r viene determinado por \# D3DPSHADERCAPS2 \_ 0.NumTemps (que va de 12 a 32).
2.  Solo se puede usar mediante una instrucción de control de flujo.
3.  Solo se puede usar mediante una instrucción de muestreo de textura.
4.  partial(x, y, z, w): si solo se actualiza un subconjunto de canales en el registro, los canales restantes tendrán como valor predeterminado los valores especificados (x, y, z, w).
5.  Existen valores predeterminados para las búsquedas de muestreador, pero los valores dependen del formato de textura.

El número de puertos de lectura es el número de registros diferentes (para cada tipo de registro) que se pueden leer en una sola instrucción.

## <a name="output-register-types"></a>Tipos de registro de salida



| Registrarse | Nombre                                                                              | Count                                                                             | L/E | Dimensión | RelAddr | Valores predeterminados | Requiere DCL |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| Oc #     | [Registro de color de salida](dx9-graphics-reference-asm-ps-registers-output-color.md) | Consulte [Texturas de varios elementos (Direct3D 9)](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | No       | Ninguno     | No            |
| oDepth   | [Registro de profundidad de salida](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | No       | Ninguno     | No            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 