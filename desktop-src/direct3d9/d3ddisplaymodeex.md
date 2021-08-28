---
description: Información sobre las propiedades de un modo de presentación.
ms.assetid: df9d12b9-7acb-435b-9d54-0b095c871f0e
title: Estructura D3DDISPLAYMODEEX (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEEX
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1891ec67a1434700c3964f6b23fd42a9137f6e6a73a29751f566f11912c98eaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117911163"
---
# <a name="d3ddisplaymodeex-structure"></a>D3DDISPLAYMODEEX (estructura)

Información sobre las propiedades de un modo de presentación.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  UINT                Size;
  UINT                Width;
  UINT                Height;
  UINT                RefreshRate;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEEX;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Tamaño**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamaño de esta estructura. Siempre debe establecerse en sizeof(D3DDISPLAYMODEEX).

</dd> <dt>

**Width**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Ancho del modo de presentación.

</dd> <dt>

**Height**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Alto del modo de presentación.

</dd> <dt>

**RefreshRate**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Frecuencia de actualización del modo de presentación.

</dd> <dt>

**Format**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Formato del modo de presentación. Vea [D3DFORMAT](d3dformat.md).

</dd> <dt>

**ScanLineOrdering**
</dt> <dd>

Tipo: **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**

</dd> <dd>

Indica si el orden de la línea de digitalización es progresiva o entrelazada. Vea [**D3DSCANLINEORDERING.**](./d3dscanlineordering.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se usa en varios métodos para crear y administrar dispositivos Direct3D 9Ex [**(IDirect3DDevice9Ex)**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex)e cadenas de intercambio ([**IDirect3DSwapChain9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dswapchain9ex)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
