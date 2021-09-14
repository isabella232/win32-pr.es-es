---
title: crs- vs
description: Calcula un producto cruzado mediante la regla de la derecha. | crs- vs
ms.assetid: 102108f5-acc8-49ce-a84b-b8060decbaa7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fee30fab91b4f491efd4311919245ec2cb98b555
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264351"
---
# <a name="crs---vs"></a>crs- vs

Calcula un producto cruzado mediante la regla de la derecha.

## <a name="syntax"></a>Sintaxis



| crs dst, src0, src1 |
|---------------------|



 

, donde

-   dst es el registro de destino.
-   src0 es un registro de origen.
-   src1 es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Crs                    |      | x    | x    | x     | x    | x     |



 

Esta instrucción funciona como se muestra aquí.


```
dest.x = src0.y * src1.z - src0.z * src1.y;
dest.y = src0.z * src1.x - src0.x * src1.z;
dest.z = src0.x * src1.y - src0.y * src1.x;
```



Algunas restricciones de uso:

-   src0 no puede ser el mismo registro que dest.
-   src1 no puede ser el mismo registro que dest.
-   src0 no puede tener ningún swzzle que no sea el swzzle predeterminado (.xyzw).
-   src1 no puede tener ningún swzzle que no sea el swzzle predeterminado (.xyzw).
-   dest tiene que tener exactamente una de las siete máscaras siguientes: .x \| \| .x .y .z \| \| .xy .xz \| .yz \| .xyz.
-   dest debe ser un registro temporal.
-   dest no debe ser el mismo registro que src0 o src1

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




