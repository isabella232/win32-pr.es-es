---
title: Formato de efecto (Direct3D 11)
ms.assetid: c425f57b-fc14-46a5-bb65-a0a2305bd406
description: 'Más información sobre: Formato de efecto (Direct3D 11)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7644e433f6c19df20cb2417659cf575e0613f93b0d53f6494ad6ee1422a55b9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792075"
---
# <a name="effect-format-direct3d-11"></a>Formato de efecto (Direct3D 11)

Un efecto (que a menudo se almacena en un archivo con una extensión de archivo .fx) declara el estado de canalización establecido por un efecto . El estado del efecto se puede dividir aproximadamente en tres categorías:

-   [Variables](d3d11-effect-variable-syntax.md), que normalmente se declaran en la parte superior de un efecto.
-   [Funciones](d3d11-effect-function-syntax.md), que implementan código de sombreador o que otras funciones usan como funciones auxiliares.
-   Técnicas , que se pueden organizar en grupos de efectos e implementar [secuencias](d3d11-effect-technique-syntax.md)de representación mediante uno o varios pases de efecto. Cada paso establece uno o varios grupos [de estados y](d3d11-effect-states.md) llama a las funciones del sombreador.

![diagrama de las categorías de declaraciones para efectos, incluidas las variables de la parte superior, las funciones en el centro y las técnicas en la parte inferior](images/d3d10-effect-intro.png)

En el diagrama anterior se muestran las categorías de estado de efecto.

La definición del formato binario de efecto se puede encontrar en Binary \\ EffectBinaryFormat.h en el código fuente de los efectos.


## <a name="in-this-section"></a>En esta sección



| Tema                                                                   | Descripción                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Sintaxis de variable de efecto](d3d11-effect-variable-syntax.md)<br/>   | Una variable de efecto se declara con la sintaxis descrita en esta sección.<br/>                                 |
| [Sintaxis de anotación](d3d11-effect-annotation-syntax.md)<br/>      | Una anotación es un fragmento de información definido por el usuario, declarado con la sintaxis descrita en esta sección.<br/> |
| [Sintaxis de función de efecto](d3d11-effect-function-syntax.md)<br/>   | Una función de efecto se escribe en HLSL y se declara con la sintaxis descrita en esta sección.<br/>          |
| [Sintaxis de la técnica de efecto](d3d11-effect-technique-syntax.md)<br/> | Se declara una técnica de efecto con la sintaxis descrita en esta sección.<br/>                                |
| [Grupos de estados de efecto](d3d11-effect-states.md)<br/>               | Los estados de efecto son pares de valor de nombre en forma de expresión.<br/>                                          |
| [Sintaxis de grupo de efectos](d3d11-effect-group-syntax.md)<br/>         | Un grupo de efectos se declara con la sintaxis descrita en esta sección.<br/>                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de efectos 11](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





