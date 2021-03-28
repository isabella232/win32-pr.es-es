---
title: CRS-PS
description: Calcula un producto cruzado mediante la regla de la derecha. | CRS-PS
ms.assetid: 602fa7cc-4e2b-4d90-90d8-df00d5812c81
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b6098c8bf01bf0d8cce886276c1d1081720ea667
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362112"
---
# <a name="crs---ps"></a>CRS-PS

Calcula un producto cruzado mediante la regla de la derecha.

## <a name="syntax"></a>Sintaxis



| CRS DST, src0, SRC1 |
|---------------------|



 

, donde

-   DST es el registro de destino.
-   src0 es un registro de origen.
-   SRC1 es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| CRS                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Esta instrucción funciona como se muestra aquí.


```
dest.x = src0.y * src1.z - src0.z * src1.y;
dest.y = src0.z * src1.x - src0.x * src1.z;
dest.z = src0.x * src1.y - src0.y * src1.x;
```



Algunas restricciones en el uso:

-   src0 no puede ser el mismo registro que dest.
-   SRC1 no puede ser el mismo registro que dest.
-   src0 no puede tener ningún swizzle que no sea el swizzle predeterminado (. xyzw).
-   SRC1 no puede tener ningún swizzle que no sea el swizzle predeterminado (. xyzw).
-   dest debe tener exactamente una de las siete máscaras siguientes:. x \| . y \| . z \| . XY \| . XZ. \| YZ. \| XYZ.
-   dest debe ser un registro temporal.
-   dest no debe ser el mismo registro que src0 o SRC1

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




