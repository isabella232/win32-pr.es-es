---
title: Formato de efecto (Direct3D 11)
ms.assetid: c425f57b-fc14-46a5-bb65-a0a2305bd406
description: 'Más información sobre: formato de efectos (Direct3D 11)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c08589fcb041591591d033b88e4fafe597e98520
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274940"
---
# <a name="effect-format-direct3d-11"></a>Formato de efecto (Direct3D 11)

Un efecto (que suele almacenarse en un archivo con una extensión de archivo. FX) declara el estado de la canalización establecido por un efecto. El estado del efecto puede dividirse aproximadamente en tres categorías:

-   [Variables](d3d11-effect-variable-syntax.md), que se declaran normalmente en la parte superior de un efecto.
-   [Funciones](d3d11-effect-function-syntax.md), que implementan código de sombreador o que otras funciones usan como funciones auxiliares.
-   Las [técnicas](d3d11-effect-technique-syntax.md), que se pueden organizar en grupos de efectos, e implementan secuencias de representación mediante una o varias fases de efecto. Cada paso establece uno o más [grupos de Estados](d3d11-effect-states.md) y llama a las funciones de sombreador.

![diagrama de las categorías de declaraciones de efectos, incluidas las variables en la parte superior, las funciones del centro y las técnicas de la parte inferior.](images/d3d10-effect-intro.png)

En el diagrama anterior se muestran las categorías de estado de efecto.

La definición del formato binario de efectos se puede encontrar en el archivo binario \\ EffectBinaryFormat. h en el código fuente de los efectos.


## <a name="in-this-section"></a>En esta sección



| Tema                                                                   | Descripción                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Sintaxis de variables de efectos](d3d11-effect-variable-syntax.md)<br/>   | Una variable de efecto se declara con la sintaxis descrita en esta sección.<br/>                                 |
| [Sintaxis de anotación](d3d11-effect-annotation-syntax.md)<br/>      | Una anotación es una parte de la información definida por el usuario, declarada con la sintaxis descrita en esta sección.<br/> |
| [Sintaxis de la función Effect](d3d11-effect-function-syntax.md)<br/>   | Una función Effect se escribe en HLSL y se declara con la sintaxis descrita en esta sección.<br/>          |
| [Sintaxis de la técnica de efectos](d3d11-effect-technique-syntax.md)<br/> | Una técnica de efecto se declara con la sintaxis descrita en esta sección.<br/>                                |
| [Grupos de Estados de efecto](d3d11-effect-states.md)<br/>               | Los Estados de efecto son pares de nombre y valor en forma de expresión.<br/>                                          |
| [Sintaxis de grupo de efectos](d3d11-effect-group-syntax.md)<br/>         | Un grupo de efectos se declara con la sintaxis descrita en esta sección.<br/>                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Effects 11](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





