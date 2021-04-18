---
description: Crea una malla de máscara desde otra malla.
ms.assetid: 4c69377e-61ef-42b8-8864-c116164d4b22
title: Función D3DXCreateSkinInfoFromBlendedMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFromBlendedMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d81de43dde2b4f0df5913831ddfcefbab1a41855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547926"
---
# <a name="d3dxcreateskininfofromblendedmesh-function"></a>D3DXCreateSkinInfoFromBlendedMesh función)

Crea una malla de máscara desde otra malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateSkinInfoFromBlendedMesh(
  _In_        LPD3DXBASEMESH      pMesh,
  _In_        DWORD               NumBones,
  _In_  const D3DXBONECOMBINATION *pBoneCombinationTable,
  _Out_       LPD3DXSKININFO      *ppSkinInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pmesh* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Puntero a un objeto [**ID3DXBaseMesh**](id3dxbasemesh.md) , la malla desde la que se va a crear la malla de máscara.

</dd> <dt>

*NumBones* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

La longitud de la matriz asociada a BoneId. Vea [**D3DXBONECOMBINATION**](d3dxbonecombination.md).

</dd> <dt>

*pBoneCombinationTable* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXBONECOMBINATION**](d3dxbonecombination.md) \***

Puntero a una matriz de combinaciones de hueso. Vea [**D3DXBONECOMBINATION**](d3dxbonecombination.md).

</dd> <dt>

*ppSkinInfo* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Dirección de un puntero a una interfaz [**ID3DXSkinInfo**](id3dxskininfo.md) que representa el objeto de malla de máscara creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser el siguiente: E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
