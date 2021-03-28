---
title: Control de flujo
description: La mayoría del hardware está diseñado para ejecutar el código del sombreador línea a línea y ejecutar cada instrucción de HLSL una vez.
ms.assetid: 94f22e39-8e71-424b-8ca1-bafc843f843f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 70bb7706e520818c86286947acfba6cae0759b4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356917"
---
# <a name="flow-control"></a>Control de flujo

La mayoría del hardware está diseñado para ejecutar el código del sombreador línea a línea y ejecutar cada instrucción de HLSL una vez. Una instrucción de control de flujo determina en tiempo de ejecución el bloque de instrucciones de HLSL que se ejecutará a continuación. Mediante una instrucción de control de flujo, un sombreador puede recorrer en bucle un conjunto de instrucciones, o saltar (bifurcar) a una instrucción distinta de la de la línea siguiente. Algunas instrucciones de control de flujo admiten el control estático especificado en tiempo de compilación; otros ofrecen control de predicado, que es una decisión por componente tomada en tiempo de ejecución y otras admiten el control dinámico, que es una decisión tomada en tiempo de ejecución basada en el contenido de una variable.

HLSL admite las siguientes instrucciones de control de flujo.

-   [break](dx-graphics-hlsl-break.md)
-   [continue](dx-graphics-hlsl-continue.md)
-   [omiti](dx-graphics-hlsl-discard.md)
-   [do](dx-graphics-hlsl-do.md)
-   [for](dx-graphics-hlsl-for.md)
-   [if](dx-graphics-hlsl-if.md)
-   [switch](dx-graphics-hlsl-switch.md)
-   [while](dx-graphics-hlsl-while.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sintaxis del lenguaje (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




