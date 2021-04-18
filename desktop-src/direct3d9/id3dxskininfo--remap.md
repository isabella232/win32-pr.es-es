---
description: Actualiza la información de influencia del hueso para que coincida con los vértices después de reordenar. Se debe llamar a este método si el búfer de vértices de destino se ha reordenado externamente.
ms.assetid: bff5229f-e547-4ab3-84c6-58b15a7825e9
title: 'ID3DXSkinInfo:: reasignar (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Remap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 657cf0977592a8e19e68b8aeb950c62d404e7cdb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698174"
---
# <a name="id3dxskininforemap-method"></a>ID3DXSkinInfo:: reasignar (método)

Actualiza la información de influencia del hueso para que coincida con los vértices después de reordenar. Se debe llamar a este método si el búfer de vértices de destino se ha reordenado externamente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Remap(
  [in] DWORD NumVertices,
  [in] DWORD *pVertexRemap
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NumVertices* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de vértices que se van a reasignar.

</dd> <dt>

*pVertexRemap* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Matriz de DWORD cuya longitud se especifica mediante NumVertices.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Cada elemento de pVertexRemap especifica el índice de vértice anterior para esa posición. Por ejemplo, si un vértice estaba en la posición 3 pero se ha reasignado a la posición 5, el quinto elemento de pVertexRemap debe contener 3. Se puede usar la matriz de reasignación de vértices devuelta por [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
