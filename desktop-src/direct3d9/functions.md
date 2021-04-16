---
description: Una función es el bloque de creación de un sombreador creado en el lenguaje de alto nivel. Si prefiere escribir sombreadores en un lenguaje de estilo C en lugar de en lenguaje ensamblador, querrá escribir funciones.
ms.assetid: vs|directx_sdk|~\functions.htm
title: Sintaxis de la función Effect (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21e239359877813e64acea8b5f404a6ade59c992
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536832"
---
# <a name="effect-function-syntax-direct3d-9"></a>Sintaxis de la función Effect (Direct3D 9)

Una función es el bloque de creación de un sombreador creado en el lenguaje de alto nivel. Si prefiere escribir sombreadores en un lenguaje de estilo C en lugar de en lenguaje ensamblador, querrá escribir funciones.

## <a name="syntax"></a>Sintaxis


```
type id ( [ parameters ] )  
    { body }
```



Las funciones no cambian los valores de los parámetros de un efecto.

-   Type: cualquier [referencia válida para](../direct3dhlsl/dx-graphics-hlsl-reference.md) el tipo HLSL.
-   ID: un nombre único.
-   parámetros: parámetros de función.
-   cuerpo: el cuerpo de la función.

Las funciones se compilan a partir del lenguaje de alto nivel. Consulte [referencia de HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
