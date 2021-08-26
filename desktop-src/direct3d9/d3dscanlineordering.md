---
description: Marcas que indican el método que usa el rasterizador para crear una imagen en una superficie.
ms.assetid: 55cf790e-ebe9-4791-a2be-a90fc76bae57
title: Enumeración D3DSCANLINEORDERING (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSCANLINEORDERING
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: e5265387973c3c1605ac0022d88df3afa676dda614d7cc238e29a1ddd4a73f5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987235"
---
# <a name="d3dscanlineordering-enumeration"></a>D3DSCANLINEORDERING (enumeración)

Marcas que indican el método que usa el rasterizador para crear una imagen en una superficie.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DSCANLINEORDERING { 
  D3DSCANLINEORDERING_PROGRESSIVE  = 1,
  D3DSCANLINEORDERING_INTERLACED   = 2
} D3DSCANLINEORDERING, *LPD3DSCANLINEORDERING;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DSCANLINEORDERING_PROGRESSIVE"></span><span id="d3dscanlineordering_progressive"></span>**D3DSCANLINEORDERING \_ PROGRESSIVE**
</dt> <dd>

La imagen se crea desde la primera línea de exploración hasta la última sin omitir ninguna.

</dd> <dt>

<span id="D3DSCANLINEORDERING_INTERLACED"></span><span id="d3dscanlineordering_interlaced"></span>**D3DSCANLINEORDERING \_ ENTRELAZADO**
</dt> <dd>

La imagen se crea mediante el método entrelazado en el que las líneas con números impares se dibujan en pases impares e incluso las líneas se dibujan en pases con números pares.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta enumeración se usa como miembro en [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) y [**D3DDISPLAYMODEEX.**](d3ddisplaymodeex.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




