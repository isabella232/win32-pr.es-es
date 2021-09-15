---
description: Crea una malla de máscara a partir de otra malla.
ms.assetid: 4c69377e-61ef-42b8-8864-c116164d4b22
title: Función D3DXCreateSkinInfoFromBlendedMesh (D3DX9Mesh.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575228"
---
# <a name="d3dxcreateskininfofromblendedmesh-function"></a>Función D3DXCreateSkinInfoFromBlendedMesh

Crea una malla de máscara a partir de otra malla.

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

*pMesh* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Puntero a un [**objeto ID3DXBaseMesh,**](id3dxbasemesh.md) la malla a partir de la que se va a crear la malla de máscara.

</dd> <dt>

*NumBones* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Longitud de la matriz asociada aId Desapegado. Vea [**D3DXCCICOMBINATION**](d3dxbonecombination.md).

</dd> <dt>

*pCombinationTable* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXCCICOMBINATION**](d3dxbonecombination.md) \***

Puntero a una matriz de combinaciones de teclas. Vea [**D3DXCCICOMBINATION**](d3dxbonecombination.md).

</dd> <dt>

*ppSkinInfo* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Dirección de un puntero a una [**interfaz ID3DXSkinInfo**](id3dxskininfo.md) que representa el objeto de malla de máscara creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser el siguiente: E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
