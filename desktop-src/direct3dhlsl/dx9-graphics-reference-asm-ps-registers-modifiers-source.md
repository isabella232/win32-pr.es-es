---
title: Modificadores de registro de origen del sombreador de píxeles
description: Use modificadores de registro de origen para cambiar el valor leído de un registro antes de que se ejecute una instrucción.
ms.assetid: b45d0919-7878-4184-ad4a-5623aae9d1f1
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0626449e0a38cb695f5f3c9402969df3a25c192ad7a16ef3311053c7843e0667
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673315"
---
# <a name="pixel-shader-source-register-modifiers"></a>Modificadores de registro de origen del sombreador de píxeles

Use modificadores de registro de origen para cambiar el valor leído de un registro antes de que se ejecute una instrucción. El contenido de un registro de origen se deja sin cambios. Los modificadores son útiles para ajustar el intervalo de datos de registro como preparación para la instrucción. Un conjunto de modificadores denominado selectores copia o replica los datos de un único canal (r,g,b,a) en los demás canales.

## <a name="ps_1_1---ps_1_4"></a>ps \_ 1 \_ 1 - ps \_ 1 \_ 4

Esta tabla identifica las versiones que admiten cada modificador:



| Modificadores de registro de origen                                                                                    | Syntax         | Versión 1 \_ 1 | Versión 1 \_ 2     | Versión 1 \_ 3     | Versión 1 \_ 4     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|
| [predisposición](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | registro \_ de sesgo | X       | X    | X    | X    |
| [Invertir](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | 1: registro   | X       | X    | X    | X    |
| [Negar](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | \- Registro    | X       | X    | X    | X    |
| [escala en 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | register \_ x2   |         |      |      | X    |
| [escalado firmado](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | register \_ bx2  | X       | X    | X    | X    |
| [modificadores texld y texcrd](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | register \_ d\*  | X       | X    | X    | X    |
| [swling del registro de origen](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | register.xyzw  | X       | X    | X    | X    |



 

Los modificadores de registro de origen solo se pueden usar en instrucciones aritméticas. No se pueden usar en instrucciones de dirección de textura. La excepción a esto es el [modificador de escala por 2.](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) Para la versión \_ 1 1, se puede usar la escala con firma en el argumento de origen de cualquier instrucción \* texm. Para la versión 1 \_ 2 o 1 3, la escala con firma se puede usar en el argumento de origen \_ de cualquier instrucción de dirección de textura.

Algunas restricciones específicas de modificador:

-   Negate se puede combinar con el sesgo, el escalado firmado o el modificador scalex2. Cuando se combina, negate se ejecuta en último lugar.
-   La inversión no se puede combinar con ningún otro modificador.
-   Invert, negate, bias, signed scaling y scalex2 se pueden combinar con cualquiera de los selectores.
-   Los modificadores de registro de origen no deben usarse en registros constantes porque provocarán resultados no definidos. Para la versión 1 4, no se permiten modificadores en constantes \_ y se producirá un error en la validación.

## <a name="ps_2_0-and-above"></a>ps \_ 2 \_ 0 y superiores

Para la versión ps 2 0 y versiones arriba, se ha simplificado el número \_ \_ de modificadores.

### <a name="negate"></a>Negate

Nega el contenido del registro de origen.



| Modificador de componente | Descripción     |
|--------------------|-----------------|
| \- R               | Negación de origen |



 

El modificador negate no se puede usar en el segundo registro de origen de estas instrucciones: [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md)y [m4x4 - ps](m4x4---ps.md).



| Versiones del sombreador de píxeles | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|-------|------|-------|
| \-                    | x    | x    | x     | x    | x     |



 

### <a name="absolute-value"></a>Valor absoluto

Tome el valor absoluto del registro.



| Versiones del sombreador de píxeles | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|-------|------|-------|
| abs                   |      |      |       | x    | x     |



 

Si algún sombreador de la versión 3 lee de uno o varios registros float constantes \# (c), debe cumplirse una de las siguientes condiciones.

-   Todos los registros de punto flotante constantes deben usar el modificador abs.
-   Ninguno de los registros de punto flotante constantes puede usar el modificador abs.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




