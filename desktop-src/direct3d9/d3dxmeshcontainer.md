---
description: Encapsula un objeto de malla en una jerarquía de marco de transformación.
ms.assetid: 50e98230-7dc3-468a-92c4-8165e8fe242b
title: Estructura D3DXMESHCONTAINER (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHCONTAINER
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: f57daea26f42d8dd680d0259199b0df77badf510
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974333"
---
# <a name="d3dxmeshcontainer-structure"></a>D3DXMESHCONTAINER (estructura)

Encapsula un objeto de malla en una jerarquía de marco de transformación.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXMESHCONTAINER {
  LPSTR                Name;
  D3DXMESHDATA         MeshData;
  LPD3DXMATERIAL       pMaterials;
  LPD3DXEFFECTINSTANCE pEffects;
  DWORD                NumMaterials;
  DWORD                *pAdjacency;
  LPD3DXSKININFO       pSkinInfo;
  D3DXMESHCONTAINER    *pNextMeshContainer;
} D3DXMESHCONTAINER, *LPD3DXMESHCONTAINER;
```



## <a name="members"></a>Members

<dl> <dt>

**Nombre**
</dt> <dd>

Tipo: **LPSTR**

</dd> <dd>

Nombre de la malla.

</dd> <dt>

**MeshData**
</dt> <dd>

Tipo: **[ **D3DXMESHDATA**](d3dxmeshdata.md)**

</dd> <dd>

Tipo de datos de la malla. Vea [**D3DXMESHDATA**](d3dxmeshdata.md).

</dd> <dt>

**pMaterials**
</dt> <dd>

Tipo: **[ **LPD3DXMATERIAL**](d3dxmaterial.md)**

</dd> <dd>

Matriz de materiales de malla. Vea [**D3DXMATERIAL.**](d3dxmaterial.md)

</dd> <dt>

**pEffects**
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTINSTANCE**](d3dxeffectinstance.md)**

</dd> <dd>

Puntero a un conjunto de parámetros de efecto predeterminados. Vea [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).

</dd> <dt>

**NumMaterials**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de materiales de la malla.

</dd> <dt>

**pAdjacency**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

</dd> <dd>

Puntero a una matriz de tres DWORD por triángulo de la malla que contiene información de adyacencia.

</dd> <dt>

**pSkinInfo**
</dt> <dd>

Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)**

</dd> <dd>

Puntero a la interfaz de información de máscara. Vea [**ID3DXSkinInfo**](id3dxskininfo.md).

</dd> <dt>

**pNextMeshContainer**
</dt> <dd>

Tipo: *:D3DXMESHCONTAINER **\***

</dd> <dd>

Puntero al siguiente contenedor de malla.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una aplicación puede derivar de esta estructura para agregar otros datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
