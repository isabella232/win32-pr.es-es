---
description: Mida el rendimiento de la tasa de aciertos de caché para texturas y vértices indexados.
ms.assetid: 70bc4e93-0a34-485b-bdcc-028c24b52f62
title: D3DDEVINFO_D3D9CACHEUTILIZATION estructura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9CACHEUTILIZATION
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 01f0521ca7833cd74c3cb45b5a650fbd12aae485e36a153b57e6d9b10b49d1f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733076"
---
# <a name="d3ddevinfo_d3d9cacheutilization-structure"></a>D3DDEVINFO \_ D3D9CACHEUTILIZATION (estructura)

Mida el rendimiento de la tasa de aciertos de caché para texturas y vértices indexados.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DDEVINFO_D3D9CACHEUTILIZATION {
  FLOAT TextureCacheHitRate;
  FLOAT PostTransformVertexCacheHitRate;
} D3DDEVINFO_D3D9CACHEUTILIZATION, *LPD3DDEVINFO_D3D9CACHEUTILIZATION;
```



## <a name="members"></a>Miembros

<dl> <dt>

**TextureCacheHitRate**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Tasa de aciertos para buscar una textura en la caché de texturas. Esto supone que hay una caché de texturas. Aumentar el sesgo de nivel de detalle para usar la textura más detallada, usar muchas texturas grandes o generar un patrón de acceso de textura casi aleatorio en texturas grandes con código de sombreador personalizado puede afectar drásticamente a la tasa de aciertos de la caché de texturas.

</dd> <dt>

**PostTransformVertexCacheHitRate**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Velocidad de aciertos para buscar vértices transformados en la caché de vértices. La GPU está diseñada para transformar vértices indexados y puede almacenarlos en una caché de vértices. Si usa [**mallas, D3DXOptimizeFaces**](d3dxoptimizefaces.md) o [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) pueden dar lugar a un mejor uso de la caché de vértices.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una caché eficaz suele estar más cerca de una tasa de aciertos del 90 %, y una caché ineficaz suele estar más cerca de una tasa de aciertos del 10 % (aunque un porcentaje bajo no es necesariamente un problema).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
