---
description: Marcas que indican el método que el rasterizador utiliza para crear una imagen en una superficie.
ms.assetid: 55cf790e-ebe9-4791-a2be-a90fc76bae57
title: Enumeración D3DSCANLINEORDERING (D3d9types. h)
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
ms.openlocfilehash: 2eaed36577f881266c12b0a927cfcdc2494f0d57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718536"
---
# <a name="d3dscanlineordering-enumeration"></a>Enumeración D3DSCANLINEORDERING

Marcas que indican el método que el rasterizador utiliza para crear una imagen en una superficie.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DSCANLINEORDERING { 
  D3DSCANLINEORDERING_PROGRESSIVE  = 1,
  D3DSCANLINEORDERING_INTERLACED   = 2
} D3DSCANLINEORDERING, *LPD3DSCANLINEORDERING;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DSCANLINEORDERING_PROGRESSIVE"></span><span id="d3dscanlineordering_progressive"></span>**\_Progresiva D3DSCANLINEORDERING**
</dt> <dd>

La imagen se crea desde la primera Scanline hasta la última sin omitir ninguna.

</dd> <dt>

<span id="D3DSCANLINEORDERING_INTERLACED"></span><span id="d3dscanlineordering_interlaced"></span>**D3DSCANLINEORDERING \_ entrelazado**
</dt> <dd>

La imagen se crea mediante el método entrelazado, en el que las líneas impares se dibujan en las pasadas con números impares y las líneas pares se dibujan en pasos con número par.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración se usa como miembro en [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) y [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




