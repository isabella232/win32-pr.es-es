---
title: FRC-PS
description: Devuelve la parte fraccionaria de cada componente de entrada. | FRC-PS
ms.assetid: 378bc516-c81e-4538-8d6f-987536b19467
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a16dd518333efa1dce878c1418547bc0527d1d64
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362282"
---
# <a name="frc---ps"></a>FRC-PS

Devuelve la parte fraccionaria de cada componente de entrada.

## <a name="syntax"></a>Sintaxis



| FRC DST, src |
|--------------|



 

, donde

-   DST es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| frc                   |      |      |      |      | x    | x    | x     | x    | x     |



 

En el fragmento de código siguiente se muestra conceptualmente cómo funciona la instrucción.


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



La función Floor convierte el argumento que se pasa al entero más grande que es menor o igual que el argumento. Esto se convierte en un valor float y, a continuación, se resta pantalla el valor original. El valor fraccionario resultante oscila entre 0,0 y 1,0.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




