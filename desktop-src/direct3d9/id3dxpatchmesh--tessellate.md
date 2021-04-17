---
description: Realiza una teselación uniforme basada en el nivel de teselación.
ms.assetid: 0fc701b4-0636-450e-b8e0-e7a490871316
title: 'ID3DXPatchMesh:: dividirlas (método) (D3DX9Mesh. h)'
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670264"
---
# <a name="id3dxpatchmeshtessellate-method"></a>ID3DXPatchMesh:: dividirlas (método)

Realiza una teselación uniforme basada en el nivel de teselación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Tessellate(
  [in] FLOAT      fTessLevel,
  [in] LPD3DXMESH pMesh
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fTessLevel* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Nivel de teselación. Es el número de vértices introducidos entre los vértices existentes. El intervalo de este parámetro Float es 0 < fTessLevel <= 32.

</dd> <dt>

*pmesh* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Malla teselada resultante. Vea [**ID3DXMesh**](id3dxmesh.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Esta función se ejecutará de forma más eficaz si la malla de revisión se ha optimizado mediante [**ID3DXPatchMesh:: Optimize**](id3dxpatchmesh--optimize.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
