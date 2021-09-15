---
description: Una función es el bloque de creación de un sombreador creado en el lenguaje de alto nivel. Si prefiere escribir sombreadores en un lenguaje de estilo C en lugar de en el lenguaje de ensamblado, querrá escribir funciones.
ms.assetid: vs|directx_sdk|~\functions.htm
title: Sintaxis de función de efecto (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21e239359877813e64acea8b5f404a6ade59c992
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127565985"
---
# <a name="effect-function-syntax-direct3d-9"></a>Sintaxis de función de efecto (Direct3D 9)

Una función es el bloque de creación de un sombreador creado en el lenguaje de alto nivel. Si prefiere escribir sombreadores en un lenguaje de estilo C en lugar de en el lenguaje de ensamblado, querrá escribir funciones.

## <a name="syntax"></a>Sintaxis


```
type id ( [ parameters ] )  
    { body }
```



Las funciones no cambian los valores de parámetro en un efecto.

-   type: cualquier referencia [válida para el tipo HLSL.](../direct3dhlsl/dx-graphics-hlsl-reference.md)
-   id: un nombre único.
-   parameters: parámetros de función.
-   body: cuerpo de la función.

Las funciones se han creado a partir del lenguaje de alto nivel. Vea [Referencia de HLSL.](../direct3dhlsl/dx-graphics-hlsl-reference.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
