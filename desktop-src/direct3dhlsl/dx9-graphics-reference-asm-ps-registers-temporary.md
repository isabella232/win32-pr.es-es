---
title: Registro temporal (referencia de PS de HLSL)
description: Los registros temporales de entrada del sombreador de píxeles se utilizan para almacenar resultados intermedios.
ms.assetid: e61daaa1-0a9b-4b1c-b91c-56573be59ed9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7aebee99a693ac629d9cc8a372fba7589a9e29ef
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "103904316"
---
# <a name="temporary-register-hlsl-ps-reference"></a>Registro temporal (referencia de PS de HLSL)

Los registros temporales de entrada del sombreador de píxeles se utilizan para almacenar resultados intermedios.

Sintaxis


```
no declaration is required
```





| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Registro temporal    |      |      |      |      | x    | x     | x    | x    | x     |



 

-   Hay 12 registros temporales del sombreador de píxeles: R0 a R11.
-   Estos registros se utilizan para almacenar resultados intermedios durante los cálculos.
-   Si un registro temporal usa componentes que no están definidos en el código anterior, se producirá un error en la validación del sombreador.
-   Se trata de una precisión de punto flotante como mínimo.
-   Se puede usar un máximo de tres en una sola instrucción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registra](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




