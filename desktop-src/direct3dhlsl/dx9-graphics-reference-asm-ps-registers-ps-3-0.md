---
title: ps_3_0 registros
description: Los sombreadores de píxeles dependen de los registros para obtener datos de vértices, de salida de datos de píxeles, para conservar los resultados temporales durante los cálculos y para identificar las fases de muestreo de textura.
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
ms.openlocfilehash: ef4eef435857968246ab0413841ef072b5391a5e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420864"
---
# <a name="ps_3_0-registers"></a>Registros de PS \_ 3 \_ 0

Los sombreadores de píxeles dependen de los registros para obtener datos de vértices, de salida de datos de píxeles, para conservar los resultados temporales durante los cálculos y para identificar las fases de muestreo de textura. Hay varios tipos de registros, cada uno con una funcionalidad única. Esta sección contiene información de referencia de los registros de entrada y salida implementados por el sombreador de píxeles versión 3 \_ 0.

## <a name="new-registers"></a>Nuevos registros

### <a name="input-register"></a>Registro de entrada

Los registros de entrada (v \# ) son ahora de punto flotante y el [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)(t) se ha \# consolidado en él. La [semántica de DCL \_ (SM3-PS ASM)](dcl-usage---ps.md) en la parte superior del sombreador se usa para describir lo que se contenía en un registro de entrada determinado \_ . Se introduce una semántica para los tipos de píxeles (análogo al lado del vértice) de este modelo. No se realiza ninguna fijación cuando los registros de entrada se definen como colores (como coordenadas de textura). La evaluación de los registros definidos como color difiere de las coordenadas de textura en el muestreo múltiple.

### <a name="face-register"></a>Registro facial

El registro facial (vFace) es nuevo para este modelo. Se trata de un registro escalar de punto flotante que finalmente contendrá el área primitiva. En \_ el PS 3 \_ 0, sin embargo, solo el signo de este registro es válido. Por lo tanto, si el valor es menor que cero (el bit de signo está establecido como negativo), el primitivo es la parte trasera (el área es negativa, en sentido contrario a las agujas del reloj). Por lo tanto, en PS \_ 3 \_ 0 solo tiene sentido comparar este registro con 0 (> 0 o < 0). Dentro del sombreador de píxeles, la aplicación puede tomar una decisión sobre la técnica de iluminación que se va a usar. La iluminación a dos caras puede lograrse de esta manera. Este registro requiere una declaración, por lo que el uso no declarado se marcará como un error. En el caso de las líneas y los primitivos de punto, este registro es indefinido. El registro facial solo se puede usar como condición con las siguientes instrucciones: [SETP \_ COMP-PS](setp-comp---ps.md), [If \_ COMP-PS](if-comp---ps.md)o [break \_ COMP-PS](break-comp---ps.md).

### <a name="loop-counter-register"></a>Registro de contador de bucle

El [registro de contador de bucle](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al) es nuevo para este modelo. Se incrementa automáticamente en cada ejecución del bloque [Loop-PS](loop---ps.md) / [ENDLOOP-PS](endloop---ps.md) . Se puede usar en el bloque para el direccionamiento relativo si es necesario. No es válido usar el registro de contador de bucle fuera del bucle.

### <a name="position-register"></a>Registro de posición

El registro de posición (vPos) es nuevo para este modelo. Contiene los píxeles actuales (x, y) en los canales correspondientes. Los canales (z, w) no están definidos. Este registro requiere una declaración, por lo que el uso no declarado se marcará como un error. Cuando se declara, este registro debe tener exactamente una de las siguientes máscaras:. x,. y,. XY.

## <a name="input-register-types"></a>Tipos de registro de entrada



| Registrarse | Nombre                                                                                      | Count | L/E | \# Leer puertos | \# Lecturas/inst. | Dimensión | RelAddr | Valores predeterminados   | Requiere DCL |
|----------|-------------------------------------------------------------------------------------------|-------|-----|---------------|---------------|-----------|---------|------------|--------------|
| v\#      | [Registro de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md)                 | 10    | R   | 1             | Sin límite     | 4         | Alabama      | Ninguno       | Sí          |
| c\#      | [Registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md)               | 32    | L/E | 3             | Sin límite     | 4         | No      | None       | No           |
| c\#      | [Registro Float constante](dx9-graphics-reference-asm-ps-registers-constant-float.md)     | 224   | R   | 1             | Sin límite     | 4         | No      | 0000       | No           |
| Configur\#      | [Registro de entero constante](dx9-graphics-reference-asm-ps-registers-constant-integer.md) | 16    | R   | 1             | 1             | 4         | No      | 0000       | No           |
| b\#      | [Registro booleano constante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md) | 16    | R   | 1             | 1             | 1         | No      | FALSE      | No           |
| P0       | [Registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md)               | 1     | R   | 1             | 1             | 1         | No      | None       | No           |
| s\#      | [Muestra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md)        | 16    | R   | 1             | 1             | 4         | No      | Vea la nota 1 | Sí          |
| vFace    | \_Registro facial                                                                            | 1     | R   | 1             | Sin límite     | 1         | No      | None       | Sí          |
| vPos     | Registro de posición \_                                                                        | 1     | R   | 1             | Sin límite     | 4         | No      | None       | Sí          |
| Alabama       | \_Registro de contador de bucle \_                                                                   | 1     | R   | 1             | Sin límite     | 1         | N/D     | Ninguno       | No           |



 

Notas:

-   Existen valores predeterminados para las búsquedas de muestra, pero los valores dependen del formato de textura.

El número de readports es el número de registros diferentes (para cada tipo de registro) que se pueden leer en una única instrucción.

## <a name="output-register-types"></a>Tipos de registro de salida



| Registrarse | Nombre                                                                              | Count                                                                             | L/E | Dimensión | RelAddr | Valores predeterminados | Requiere DCL |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| Opcional #     | [Registro de color de salida](dx9-graphics-reference-asm-ps-registers-output-color.md) | Ver [texturas de varios elementos (Direct3D 9)](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | No      | None     | No           |
| oDepth   | [Registro de profundidad de salida](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | No      | None     | No           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registra](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 