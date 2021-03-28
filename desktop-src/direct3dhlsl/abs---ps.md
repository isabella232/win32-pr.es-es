---
title: ABS-PS
description: Calcula el valor absoluto. | ABS-PS
ms.assetid: e97db550-2a03-421a-86f4-a6fc5f8e0bca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 070a513aaa0d336d5ac404b1748fdd162edfd532
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362030"
---
# <a name="abs---ps"></a>ABS-PS

Calcula el valor absoluto.

## <a name="syntax"></a>Sintaxis



|              |
|--------------|
| ABS DST, src |



 

, donde

-   DST es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Observaciones



|                       |      |      |      |      |      |      |       |      |       |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
| abs                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Esta instrucción funciona como se muestra aquí.


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="instruction-information"></a>Información de instrucciones



|                          |            |
|--------------------------|------------|
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




