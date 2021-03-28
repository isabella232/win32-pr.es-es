---
title: Modificadores de registro de origen del sombreador de píxeles
description: Utilice modificadores de registro de origen para cambiar el valor leído de un registro antes de que se ejecute una instrucción.
ms.assetid: b45d0919-7878-4184-ad4a-5623aae9d1f1
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 12cfee533a71408a445d97a63bbd8b76b281236b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357757"
---
# <a name="pixel-shader-source-register-modifiers"></a>Modificadores de registro de origen del sombreador de píxeles

Utilice modificadores de registro de origen para cambiar el valor leído de un registro antes de que se ejecute una instrucción. El contenido de un registro de origen se deja sin cambios. Los modificadores son útiles para ajustar el intervalo de datos de registro como preparación para la instrucción. Un conjunto de modificadores denominados selectores copia o replica los datos de un canal único (r, g, b, a) en los otros canales.

## <a name="ps_1_1---ps_1_4"></a>PS \_ 1 \_ 1-PS \_ 1 \_ 4

En esta tabla se identifican las versiones que admiten cada modificador:



| Modificadores de registro de origen                                                                                    | Sintaxis         | Versión |      |      |      |     |     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|-----|-----|
|                                                                                                              |                | 1\_1    | 1\_2 | 1 \_ 3 | 1\_4 |     |     |
| [parcial](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | \_desviar registro | X       | X    | X    | X    |     |     |
| [triángulo](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | 1-registro   | X       | X    | X    | X    |     |     |
| [negate](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | \- el    | X       | X    | X    | X    |     |     |
| [escalar por 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | registrar \_ x2   |         |      |      | X    |     |     |
| [escalado con signo](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | registrar \_ BX2  | X       | X    | X    | X    |     |     |
| [modificadores texld y texcrd](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | Registro \_ d\*  | X       | X    | X    | X    |     |     |
| [registro de origen permutación](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | registro. xyzw  | X       | X    | X    | X    |     |     |



 

Los modificadores de registro de origen solo se pueden usar en Instrucciones aritméticas. No se pueden usar en instrucciones de dirección de textura. La excepción es el modificador [Scale by 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) . En el caso de la versión 1 \_ , se puede usar la escala con signo en el argumento de origen de cualquier \* instrucción texm. En el caso de la versión 1 \_ 2 o 1 \_ 3, la escala firmada se puede utilizar en el argumento de origen de cualquier instrucción de dirección de textura.

Algunas restricciones específicas del modificador:

-   Niega puede combinarse con el modificador Bias, escalado con signo o scalex2. Cuando se combina, la ejecución de la negación es la última.
-   La inversión no se puede combinar con ningún otro modificador.
-   Invert, Negate, Bias, escala firmada y scalex2 se pueden combinar con cualquiera de los selectores.
-   Los modificadores de registro de origen no se deben usar en registros constantes porque producirán resultados no definidos. En el caso de la versión \_ 4, no se permiten modificadores en constantes y se producirá un error en la validación.

## <a name="ps_2_0-and-above"></a>PS \_ 2 \_ 0 y versiones posteriores

En el caso de la versión PS \_ 2 \_ 0 y versiones más arriba, se ha simplificado el número de modificadores.

### <a name="negate"></a>Negate

Niega el contenido del registro de origen.



| Modificador de componente | Descripción     |
|--------------------|-----------------|
| \- c               | Negación de origen |



 

No se puede usar el modificador Negate en el segundo registro de código fuente de estas instrucciones: [m3x2-PS](m3x2---ps.md), [M3x3-PS](m3x3---ps.md), [M3x4-PS](m3x4---ps.md), [m4x3-PS](m4x3---ps.md)y [M4x4-PS](m4x4---ps.md).



| Versiones del sombreador de píxeles | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|-------|------|-------|
| \-                    | x    | x    | x     | x    | x     |



 

### <a name="absolute-value"></a>Valor absoluto

Tome el valor absoluto del registro.



| Versiones del sombreador de píxeles | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|-------|------|-------|
| abs                   |      |      |       | x    | x     |



 

Si cualquier sombreador de la versión 3 Lee de uno o más registros Float constantes (c \# ), debe cumplirse una de las siguientes condiciones.

-   Todos los registros de punto flotante constantes deben usar el modificador ABS.
-   Ninguno de los registros de punto flotante constantes puede usar el modificador ABS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




