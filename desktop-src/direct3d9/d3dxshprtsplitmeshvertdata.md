---
description: D3DXSHPRTSPLITMESHVERTDATA (estructura)
ms.assetid: 8799a680-bf5f-42cc-91aa-1a6aed164ca5
title: Estructura D3DXSHPRTSPLITMESHVERTDATA (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTSPLITMESHVERTDATA
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: cc32ee70cd1685351f8cca8860d9d45ab4ea597affed2fbe7cf078d44a8ed437
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027065"
---
# <a name="d3dxshprtsplitmeshvertdata-structure"></a>D3DXSHPRTSPLITMESHVERTDATA (estructura)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXSHPRTSPLITMESHVERTDATA {
  UINT uVertRemap;
  UINT uSubCluster;
  UINT ucVertStatus;
} D3DXSHPRTSPLITMESHVERTDATA, *LPD3DXSHPRTSPLITMESHVERTDATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**uVertRemap**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Vértice de la malla original a la que corresponde.

</dd> <dt>

**uSubCluster**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Índice del clúster, en relación con el superclúster.

</dd> <dt>

**ucVertStatus**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

1 si el vértice tiene datos válidos, 0 si está "lleno".

</dd> </dl>

## <a name="remarks"></a>Comentarios

Asignado en [**D3DXSHPRTCompSplitMeshSC**](d3dxshprtcompsplitmeshsc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
