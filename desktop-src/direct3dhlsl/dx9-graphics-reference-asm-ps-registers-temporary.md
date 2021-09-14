---
title: Registro temporal (referencia de HLSL PS)
description: Los registros temporales de entrada del sombreador de píxeles se usan para contener resultados intermedios.
ms.assetid: e61daaa1-0a9b-4b1c-b91c-56573be59ed9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7aebee99a693ac629d9cc8a372fba7589a9e29ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263919"
---
# <a name="temporary-register-hlsl-ps-reference"></a>Registro temporal (referencia de HLSL PS)

Los registros temporales de entrada del sombreador de píxeles se usan para contener resultados intermedios.

Sintaxis


```
no declaration is required
```





| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Registro temporal    |      |      |      |      | x    | x     | x    | x    | x     |



 

-   Hay 12 registros temporales de sombreador de píxeles: de r0 a r11.
-   Estos registros se usan para almacenar resultados intermedios durante los cálculos.
-   Si un registro temporal usa componentes que no están definidos en el código anterior, se producirá un error en la validación del sombreador.
-   Se trata de al menos una precisión de punto flotante.
-   Se puede usar un máximo de tres en una sola instrucción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




