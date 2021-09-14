---
title: Control de flujo
description: La mayoría del hardware está diseñado para ejecutar el código del sombreador línea a línea, ejecutando cada instrucción HLSL una vez.
ms.assetid: 94f22e39-8e71-424b-8ca1-bafc843f843f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 70bb7706e520818c86286947acfba6cae0759b4d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964652"
---
# <a name="flow-control"></a>Control de flujo

La mayoría del hardware está diseñado para ejecutar el código del sombreador línea a línea, ejecutando cada instrucción HLSL una vez. Una instrucción de control de flujo determina en tiempo de ejecución qué bloque de instrucciones HLSL se ejecutará a continuación. Con una instrucción de control de flujo, un sombreador puede recorrer un conjunto de instrucciones o saltar (rama) a una instrucción que no sea la de la línea siguiente. Algunas instrucciones de control de flujo admiten el control estático que se especifica en tiempo de compilación; Otros ofrecen control predicado, que es una decisión por componente tomada en tiempo de ejecución, y otros admiten el control dinámico, que es una decisión tomada en tiempo de ejecución en función del contenido de una variable.

HLSL admite las siguientes instrucciones de control de flujo.

-   [break](dx-graphics-hlsl-break.md)
-   [continue](dx-graphics-hlsl-continue.md)
-   [Deseche](dx-graphics-hlsl-discard.md)
-   [do](dx-graphics-hlsl-do.md)
-   [for](dx-graphics-hlsl-for.md)
-   [if](dx-graphics-hlsl-if.md)
-   [switch](dx-graphics-hlsl-switch.md)
-   [while](dx-graphics-hlsl-while.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sintaxis del lenguaje (HLSL de DirectX)](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




