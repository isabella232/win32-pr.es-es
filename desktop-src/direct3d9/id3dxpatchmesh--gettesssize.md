---
description: Obtiene el tamaño de la malla teselada, dado un nivel de teselación.
ms.assetid: 86d1d1a0-1934-40e9-bff9-6c435d1e5183
title: 'ID3DXPatchMesh:: GetTessSize (método) (D3DX9Mesh. h)'
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083814"
---
# <a name="id3dxpatchmeshgettesssize-method"></a>ID3DXPatchMesh:: GetTessSize (método)

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

*fTessLevel* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Nivel de teselación.

</dd> <dt>

*Adaptable* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Teselación adaptable. En el caso de la teselación adaptativa, establezca este valor en **true** y establezca fTessLevel en el valor de teselación máxima. Esto producirá el tamaño de malla máximo necesario para la teselación adaptable.

</dd> <dt>

*NumTriangles* \[ enuncia\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero al número de triángulos generado por la malla de teselación.

</dd> <dt>

*NumVertices* \[ enuncia\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero al número de vértices generado por la malla teselada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Este método presupone la teselación uniforme.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
