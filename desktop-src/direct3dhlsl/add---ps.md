---
title: Agregar-PS
description: Agrega dos vectores. | Agregar-PS
ms.assetid: f7d29a66-879b-4160-82fd-0a1b2076559a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8c6ef7c14ac54610301f283d076751b0c4d4a5e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986222"
---
# <a name="add---ps"></a>Agregar-PS

Agrega dos vectores.

## <a name="syntax"></a>Sintaxis



| Agregar DST, src0, SRC1 |
|---------------------|



 

, donde

-   DST es el registro de destino.
-   src0 es un registro de origen.
-   SRC1 es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| add                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

En el fragmento de código siguiente se muestran las operaciones realizadas.


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="instruction-information"></a>Información de instrucciones



|                          |            |
|--------------------------|------------|
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




