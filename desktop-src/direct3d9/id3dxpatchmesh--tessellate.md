---
description: Realiza una teselación uniforme en función del nivel de teselación.
ms.assetid: 0fc701b4-0636-450e-b8e0-e7a490871316
title: Método ID3DXPatchMesh::Tessellate (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Tessellate
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b94b79a9decd2f44fa1675e257a2401e2ae8f7a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060530"
---
# <a name="id3dxpatchmeshtessellate-method"></a>Método ID3DXPatchMesh::Tessellate

Realiza una teselación uniforme en función del nivel de teselación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Tessellate(
  [in] FLOAT      fTessLevel,
  [in] LPD3DXMESH pMesh
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fTessLevel* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Nivel de teselación. Este es el número de vértices introducidos entre los vértices existentes. El intervalo de este parámetro float es 0 < fTessLevel <= 32.

</dd> <dt>

*pMesh* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Malla teselada resultante. Vea [**ID3DXMesh.**](id3dxmesh.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Esta función funcionará de forma más eficaz si la malla de revisión se ha optimizado mediante [**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
