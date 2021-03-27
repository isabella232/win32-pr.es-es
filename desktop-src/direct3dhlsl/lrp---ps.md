---
title: LRP-PS
description: Interpola linealmente entre el segundo y tercer registro de origen mediante una proporción especificada en el primer registro de origen. | LRP-PS
ms.assetid: b360f28e-cb2a-4403-a020-180524df6549
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aec1ac23cc6c86f768d435e4c8169117c1bbe899
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083686"
---
# <a name="lrp---ps"></a>LRP-PS

Interpola linealmente entre el segundo y tercer registro de origen mediante una proporción especificada en el primer registro de origen.

## <a name="syntax"></a>Sintaxis



| LRP DST, src0, SRC1, src2 |
|---------------------------|



 

, donde

-   DST es el registro de destino.
-   src0 es un registro de origen.
-   SRC1 es un registro de origen.
-   src2 es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| lrp                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Esta instrucción realiza la interpolación lineal basada en la fórmula siguiente.


```
 
dest = src0 * src1 + (1-src0) * src2
// which is the same as
dest = src2 + src0 * (src1 - src2)
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




