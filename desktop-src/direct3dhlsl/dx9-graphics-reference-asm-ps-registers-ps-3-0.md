---
title: ps_3_0 registros
description: Este artículo contiene información de referencia para los registros de entrada y salida implementados por la versión 3_0 del sombreador de píxeles.
ms.assetid: 01bee50a-c1b7-4b15-9df8-1dd52d9ff163
keywords:
- vPos
- Registro de posición, sombreador de píxeles
- 'Registros: ps_3_0'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e1cd0173beabc8fbe21ad15e88e23fc1b6e84892
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263927"
---
# <a name="ps_3_0-registers"></a>ps \_ 3 \_ 0 Registros

Los sombreadores de píxeles dependen de los registros para obtener datos de vértices, generar datos de píxeles, contener resultados temporales durante los cálculos e identificar las fases de muestreo de textura. Hay varios tipos de registros, cada uno con una funcionalidad única. Esta sección contiene información de referencia para los registros de entrada y salida implementados por la versión 3 0 del sombreador de \_ píxeles.

## <a name="new-registers"></a>Nuevos registros

### <a name="input-register"></a>Registro de entrada

Los registros de entrada (v ) ahora son de punto flotante completo y los registros de coordenadas de textura \# (t) se han consolidado en [](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) \# él. La [semántica de dcl \_ (sm3 - ps asm)](dcl-usage---ps.md) en la parte superior del sombreador se usa para describir lo que contiene un registro de entrada \_ determinado. Se introduce una semántica para los tipos de píxeles (análoga al lado del vértice) para este modelo. No se realiza ninguna fijación cuando los registros de entrada se definen como colores (como coordenadas de textura). La evaluación de los registros definidos como color difiere de las coordenadas de textura cuando se multimuestreo.

### <a name="face-register"></a>Face Register

El registro facial (vFace) es nuevo para este modelo. Se trata de un registro escalar de punto flotante que con el tiempo contendrá el área primitiva. Sin \_ embargo, en ps \_ 3 0, solo el signo de este registro es válido. Por lo tanto, si el valor es menor que cero (el bit de signo se establece en negativo), la primitiva es la cara posterior (el área es negativa, en sentido contrario a las agujas del reloj). Por lo tanto, en ps 3 0 solo tiene sentido comparar este registro con \_ \_ 0 (> 0 o < 0). Dentro del sombreador de píxeles, la aplicación puede tomar una decisión sobre qué técnica de iluminación usar. La iluminación en dos lados se puede lograr de esta manera. Este registro requiere una declaración, por lo que el uso no declarado se marcará como un error. Para las líneas y las primitivas de punto, este registro es indefinido. El registro facial solo se puede usar como condición con las siguientes instrucciones: [setp \_ comp - ps](setp-comp---ps.md), if comp - [ \_ ps](if-comp---ps.md)o [break comp - \_ ps](break-comp---ps.md).

### <a name="loop-counter-register"></a>Registro de contadores de bucles

El [registro de contadores de](dx9-graphics-reference-asm-ps-registers-loop-counter.md) bucles (aL) es nuevo para este modelo. Se incrementa automáticamente en cada ejecución del [bucle - ps](loop---ps.md) / [endloop - ps](endloop---ps.md) block. Se puede usar en el bloque para el direccionamiento relativo si es necesario. No es válido usar el registro de contadores de bucles fuera del bucle.

### <a name="position-register"></a>Registro de posición

El registro de posición (vPos) es nuevo para este modelo. Contiene los píxeles actuales (x, y) en los canales correspondientes. Los canales (z, w) no están definidos. Este registro requiere una declaración, por lo que el uso no declarado se marcará como un error. Cuando se declara, este registro debe tener exactamente una de las siguientes máscaras: .x, .y, .xy.

## <a name="input-register-types"></a>Tipos de registro de entrada



| Registrarse | Nombre                                                                                      | Count | L/E | \# Lectura de puertos | \# Lecturas/inst | Dimensión | RelAddr | Valores predeterminados   | Requiere DCL |
|----------|-------------------------------------------------------------------------------------------|-------|-----|---------------|---------------|-----------|---------|------------|--------------|
| V\#      | [Registro de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md)                 | 10    | R   | 1             | Sin límite     | 4         | aL      | None       | Sí          |
| R\#      | [Registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md)               | 32    | L/E | 3             | Sin límite     | 4         | No      | None       | No           |
| c\#      | [Registro flotante constante](dx9-graphics-reference-asm-ps-registers-constant-float.md)     | 224   | R   | 1             | Sin límite     | 4         | No      | 0000       | No           |
| i\#      | [Registro de enteros constantes](dx9-graphics-reference-asm-ps-registers-constant-integer.md) | 16    | R   | 1             | 1             | 4         | No      | 0000       | No           |
| b\#      | [Registro booleano constante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md) | 16    | R   | 1             | 1             | 1         | No      | FALSE      | No           |
| p0       | [Registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md)               | 1     | R   | 1             | 1             | 1         | No      | None       | No           |
| s\#      | [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md)        | 16    | R   | 1             | 1             | 4         | No      | Consulte la nota 1 | Sí          |
| vFace    | Face \_ Register                                                                            | 1     | R   | 1             | Sin límite     | 1         | No      | None       | Sí          |
| vPos     | Registro de \_ posición                                                                        | 1     | R   | 1             | Sin límite     | 4         | No      | None       | Sí          |
| aL       | Registro \_ de contador de \_ bucles                                                                   | 1     | R   | 1             | Sin límite     | 1         | N/D     | Ninguno       | No           |



 

Notas:

-   Existen valores predeterminados para las búsquedas de muestreador, pero los valores dependen del formato de textura.

El número de puertos de lectura es el número de registros diferentes (para cada tipo de registro) que se pueden leer en una sola instrucción.

## <a name="output-register-types"></a>Tipos de registro de salida



| Registrarse | Nombre                                                                              | Count                                                                             | L/E | Dimensión | RelAddr | Valores predeterminados | Requiere DCL |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| Oc #     | [Registro de color de salida](dx9-graphics-reference-asm-ps-registers-output-color.md) | Consulte [Texturas de varios elementos (Direct3D 9)](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | No      | None     | No           |
| oDepth   | [Registro de profundidad de salida](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | No      | None     | No           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 