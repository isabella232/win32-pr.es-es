---
title: Enmascaramiento de registros de destino
description: El enmascaramiento especifica qué componentes del registro de destino se actualizarán con el resultado de una instrucción. Los registros de textura tienen un conjunto de reglas y los registros sin texto tienen otro conjunto de reglas.
ms.assetid: 989ebe55-1f80-4063-b116-4284520f52cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7ce15f75f424cb7796ef7db7a8b89bd5bcbfa9cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974683"
---
# <a name="destination-register-masking"></a>Enmascaramiento de registros de destino

El enmascaramiento especifica qué componentes del registro de destino se actualizarán con el resultado de una instrucción. Los registros de textura tienen un conjunto de reglas y los registros sin texto tienen otro conjunto de reglas.

-   Enmascaramiento de modificadores de referencia de gráficos dx9 frente a modificadores de registros: esta sección contiene reglas para aplicar \_ \_ \_ \_ \_ \_ \_ máscaras a los registros de destino.
-   Máscaras \_ de \_ registro de textura: los registros de textura tienen algunas reglas únicas.

## <a name="destination-register-masking"></a>Enmascaramiento de registros de destino

Como se muestra en la tabla siguiente, el enmascaramiento (donde es uno de los registros válidos del sombreador de [vértices)](dx9-graphics-reference-asm-vs-registers.md)se puede aplicar a los componentes individuales de los datos vectoriales.



| Modificador de componente | Descripción      |
|--------------------|------------------|
| r.{x}{y}{z}{w}     | Máscara de destino |



 

-   En general, especificar máscaras de escritura de registro de destino es un buen estilo de codificación. Facilita la lectura y el mantenimiento del código.
-   Se puede especificar cualquier combinación de componentes (incluido ninguno) siempre que x preceda a y, y precede a z y z precede a w.
-   Los registros de salida oPts y oFog solo deben usar una máscara.
-   Algunas instrucciones requieren que el registro de destino use una sola máscara de escritura: exp, expp, log, logp, pow, rcp y rsq.
-   En la versión 1.0, la instrucción frc requería una de las siguientes combinaciones de máscara: .x, .y o .xy. La versión 2.0 no tiene ninguna restricción de máscara.
-   sincos requiere una de las siguientes combinaciones de máscara: .x, .y o .xyz.
-   m3x2 requiere la máscara de escritura .xy.
-   m3x3 y m4x3 requieren la máscara de escritura .xyz.
-   m3x4 y m4x4 requieren la máscara de escritura .xyz o la máscara de escritura predeterminada (xyzw).

## <a name="texture-register-masks"></a>Máscaras de registro de textura

Las reglas de validación para usar modificadores en registros de coordenadas de textura son más estrictas que las reglas de validación para otros registros.

-   Si se escribe oTn, también se deben escribir todos los registros anteriores (oTn-1 ~ oT0).
-   La máscara de escritura "combinada" para cualquier registro de oT \# debe ser exactamente una de las siguientes:
    -   .x
    -   .xy
    -   .xyz
    -   .xyzw (que equivale a no usar modificadores de componente)

Por ejemplo, un sombreador de vértices puede generar registros de textura en instrucciones independientes.


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

 

 




