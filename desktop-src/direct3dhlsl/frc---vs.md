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
ms.openlocfilehash: 6990d5489058d217888f34caf0305badc4cab46d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361578"
---
# <a name="frc---vs"></a>frc - vs

Devuelve la parte fraccionera de cada componente de entrada.

## <a name="syntax"></a>Sintaxis



| frc dst, src |
|--------------|



 

, donde

-   dst es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Frc                    | x    | x    | x    | x     | x    | x     |



 

El siguiente fragmento de código muestra conceptualmente cómo funciona la instrucción.


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

 

 




