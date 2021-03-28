---
title: Enmascaramiento del registro de destino
description: Enmascaramiento especifica qué componentes del registro de destino se actualizarán con el resultado de una instrucción. Los registros de textura tienen un conjunto de reglas y los registros que no son de textura tienen otro conjunto de reglas.
ms.assetid: 989ebe55-1f80-4063-b116-4284520f52cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7ce15f75f424cb7796ef7db7a8b89bd5bcbfa9cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418913"
---
# <a name="destination-register-masking"></a>Enmascaramiento del registro de destino

Enmascaramiento especifica qué componentes del registro de destino se actualizarán con el resultado de una instrucción. Los registros de textura tienen un conjunto de reglas y los registros que no son de textura tienen otro conjunto de reglas.

-   DX9 \_ Graphics \_ referencia \_ ASM \_ vs \_ registros \_ modificadores \_ masking: esta sección contiene reglas para aplicar máscaras a los registros de destino.
-   \_ \_ Máscaras de registro de textura: los registros de textura tienen algunas reglas únicas.

## <a name="destination-register-masking"></a>Enmascaramiento del registro de destino

Como se muestra en la tabla siguiente, el enmascaramiento (donde es uno de los [registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)válidos del sombreador de vértices) se puede aplicar a los componentes individuales de los datos vectoriales.



| Modificador de componente | Descripción      |
|--------------------|------------------|
| r. {x} {y} {z} {w}     | Máscara de destino |



 

-   En general, la especificación de las máscaras de escritura del registro de destino es un buen estilo de codificación. Facilita la lectura y el mantenimiento del código.
-   Se puede especificar cualquier combinación de componentes (incluido ninguno) siempre y cuando x preceda a y, y preceda a z, y z preceda a w.
-   Los registros de salida OPC y oFog deben usar solo una máscara.
-   Algunas instrucciones requieren que el registro de destino use una sola máscara de escritura: EXP, EXPP, log, logP, pow, RCP y RSQ.
-   En la versión 1,0, la instrucción FRC requería una de las siguientes combinaciones de máscara:. x o. y o. XY. La versión 2,0 no tiene ninguna restricción de máscara.
-   sincos (requiere una de las siguientes combinaciones de máscara:. x o. y o. XYZ.
-   m3x2 requiere la máscara de escritura. XY.
-   M3x3 y m4x3 requieren la máscara de escritura. XYZ.
-   M3x4 y M4x4 requieren la máscara de escritura. XYZ o la máscara de escritura predeterminada (xyzw).

## <a name="texture-register-masks"></a>Máscaras de registro de textura

Las reglas de validación para usar modificadores en los registros de coordenadas de textura son más estrictas que las reglas de validación para otros registros.

-   Si se escribe oTn, también se deben escribir todos los registros anteriores (oTn-1 ~ oT0).
-   La máscara de escritura "combinada" para cualquier \# registro de OT debe ser exactamente una de las siguientes:
    -   .x
    -   . XY
    -   . XYZ
    -   . xyzw (que equivale a no usar modificadores de componente)

Por ejemplo, un sombreador de vértices puede generar los registros de textura en instrucciones independientes.


```
    oT1.y  
    oT0.y  
    oT2  
    oT0.xz  
    oT1.x
```



O bien, se pueden combinar las instrucciones.


```
    oT0.xyz  
    oT1.xy  
    oT2.xyzw    
```



Estas restricciones solo se aplican a los registros de coordenadas de textura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




