---
title: Registro temporal (referencia de HLSL PS)
description: Los registros temporales de entrada del sombreador de píxeles se usan para contener los resultados intermedios.
ms.assetid: e61daaa1-0a9b-4b1c-b91c-56573be59ed9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47ac2d76c1197349fee9fc5c993d4268e69495367ce3f121b4a59004bff1b3a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118090020"
---
# <a name="temporary-register-hlsl-ps-reference"></a>Registro temporal (referencia de HLSL PS)

Los registros temporales de entrada del sombreador de píxeles se usan para contener los resultados intermedios.

Syntax


```
no declaration is required
```





| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Registro temporal    |      |      |      |      | x    | x     | x    | x    | x     |



 

-   Hay 12 registros temporales de sombreador de píxeles: de r0 a r11.
-   Estos registros se usan para almacenar los resultados intermedios durante los cálculos.
-   Si un registro temporal usa componentes que no están definidos en el código anterior, se producirá un error en la validación del sombreador.
-   Son al menos de precisión de punto flotante.
-   Se puede usar un máximo de tres en una sola instrucción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




