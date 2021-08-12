---
description: Una función es el bloque de creación de un sombreador creado en el lenguaje de alto nivel. Si prefiere escribir sombreadores en un lenguaje de estilo C en lugar de en lenguaje de ensamblado, querrá escribir funciones.
ms.assetid: vs|directx_sdk|~\functions.htm
title: Sintaxis de función de efecto (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b9de680f2f892e59f49e1dfd0850a128ca9ba34e2588e416059251d5058c44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118297113"
---
# <a name="effect-function-syntax-direct3d-9"></a>Sintaxis de función de efecto (Direct3D 9)

Una función es el bloque de creación de un sombreador creado en el lenguaje de alto nivel. Si prefiere escribir sombreadores en un lenguaje de estilo C en lugar de en lenguaje de ensamblado, querrá escribir funciones.

## <a name="syntax"></a>Syntax


```
type id ( [ parameters ] )  
    { body }
```



Las funciones no cambian los valores de parámetro en un efecto.

-   type: cualquier referencia [válida para el tipo HLSL.](../direct3dhlsl/dx-graphics-hlsl-reference.md)
-   id: un nombre único.
-   parameters: parámetros de función.
-   body: el cuerpo de la función.

Las funciones se construyen a partir del lenguaje de alto nivel. Vea [Referencia de HLSL.](../direct3dhlsl/dx-graphics-hlsl-reference.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
