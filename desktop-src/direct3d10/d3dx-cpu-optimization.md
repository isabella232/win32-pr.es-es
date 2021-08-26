---
description: Especifica el conjunto de instrucciones para el que D3DX está optimizado actualmente.
ms.assetid: 5fc97028-4a9d-4bc7-9c90-236a70e570e1
title: D3DX_CPU_OPTIMIZATION enumeración (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX_CPU_OPTIMIZATION
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 7bb36b3aeb448933416148b087cb7e82619beef04186637c0bb3fa944a143da5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989545"
---
# <a name="d3dx_cpu_optimization-enumeration"></a>Enumeración D3DX \_ CPU \_ OPTIMIZATION

Especifica el conjunto de instrucciones para el que D3DX está optimizado actualmente.

## <a name="syntax"></a>Syntax


```C++
typedef enum _D3DX_CPU_OPTIMIZATION { 
  D3DX_NOT_OPTIMIZED    = 0,
  D3DX_3DNOW_OPTIMIZED  = 1,
  D3DX_SSE2_OPTIMIZED   = 2,
  D3DX_SSE_OPTIMIZED    = 3
} D3DX_CPU_OPTIMIZATION;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX_NOT_OPTIMIZED"></span><span id="d3dx_not_optimized"></span>**D3DX \_ NO \_ OPTIMIZADO**
</dt> <dd>

No optimice.

</dd> <dt>

<span id="D3DX_3DNOW_OPTIMIZED"></span><span id="d3dx_3dnow_optimized"></span>**D3DX \_ 3DNOW \_ OPTIMIZADO**
</dt> <dd>

Optimice para 3DNow. conjunto de instrucciones.

</dd> <dt>

<span id="D3DX_SSE2_OPTIMIZED"></span><span id="d3dx_sse2_optimized"></span>**D3DX \_ SSE2 \_ OPTIMIZADO**
</dt> <dd>

Optimice para un conjunto de instrucciones SSE2.

</dd> <dt>

<span id="D3DX_SSE_OPTIMIZED"></span><span id="d3dx_sse_optimized"></span>**D3DX \_ SSE \_ OPTIMIZADO**
</dt> <dd>

Optimice para un conjunto de instrucciones SSE.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




