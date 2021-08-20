---
title: frc - ps
description: Devuelve la parte fraccionera de cada componente de entrada. | frc - ps
ms.assetid: 378bc516-c81e-4538-8d6f-987536b19467
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a9db28773ef5473a4b4b574f3feb32c9623c95863adcb4cb31a717e8f8c541d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117907658"
---
# <a name="frc---ps"></a>frc - ps

Devuelve la parte fraccionera de cada componente de entrada.

## <a name="syntax"></a>Syntax



| frc dst, src |
|--------------|



 

where

-   dst es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Frc                   |      |      |      |      | x    | x    | x     | x    | x     |



 

El siguiente fragmento de código muestra conceptualmente cómo funciona la instrucción.


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



La función floor convierte el argumento pasado en el entero mayor que es menor (o igual que) el argumento. Esto se convierte en un valor float y, a continuación, se resta el valor original. El valor fraccionrio resultante oscila entre 0,0 y 1,0.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




