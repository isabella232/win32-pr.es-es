---
title: frc - vs
description: Devuelve la parte fraccionera de cada componente de entrada. | frc - vs
ms.assetid: 6b6a4475-b665-4de0-9423-88ea8103e606
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2ecc6a1c903f78fb7c03442809f792e3ddb984d04975d3f5ecb0b5c918f7ab4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117907648"
---
# <a name="frc---vs"></a>frc - vs

Devuelve la parte fraccionera de cada componente de entrada.

## <a name="syntax"></a>Syntax



| frc dst, src |
|--------------|



 

where

-   dst es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Frc                    | x    | x    | x    | x     | x    | x     |



 

El fragmento de código siguiente muestra conceptualmente cómo funciona la instrucción.


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



La función floor convierte el argumento pasado en el entero mayor que es menor (o igual que) el argumento. Esto se convierte en un valor float y, a continuación, se resta el valor original. El valor fraccionrio resultante oscila entre 0,0 y 1,0.

Para la versión 1 1, las máscaras de escritura permitidas son \_ .y y .xy (no se permite .x).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




