---
description: Obtiene el tamaño de la malla teselada, dado un nivel de teselación.
ms.assetid: 86d1d1a0-1934-40e9-bff9-6c435d1e5183
title: Método ID3DXPatchMesh::GetTessSize (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetTessSize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ef23f46baca7e05005cee83f6ca765b9a5214b8b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060542"
---
# <a name="id3dxpatchmeshgettesssize-method"></a>Método ID3DXPatchMesh::GetTessSize

Obtiene el tamaño de la malla teselada, dado un nivel de teselación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTessSize(
  [in]  FLOAT fTessLevel,
  [in]  DWORD Adaptive,
  [out] DWORD *NumTriangles,
  [out] DWORD *NumVertices
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fTessLevel* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Nivel de teselación.

</dd> <dt>

*Adaptable* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Teselación adaptable. Para la teselación adaptable, establezca este valor en **TRUE** y establezca fTessLevel en el valor de teselación máximo. Esto dará como resultado el tamaño máximo de malla necesario para la teselación adaptable.

</dd> <dt>

*NumTriangles* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero al número de triángulos generados por la malla teselada.

</dd> <dt>

*NumVertices* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero al número de vértices generados por la malla teselada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Este método supone una teselación uniforme.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
