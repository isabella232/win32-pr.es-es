---
description: Crea una malla a partir de una malla de revisión de control.
ms.assetid: 50e4f7aa-a6b8-4a2b-9813-a9448f408d06
title: Función D3DXCreatePatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 375052e240973f56af32825f74caccf6f9411d75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362771"
---
# <a name="d3dxcreatepatchmesh-function"></a>D3DXCreatePatchMesh función)

Crea una malla a partir de una malla de revisión de control.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreatePatchMesh(
  _In_  const D3DXPATCHINFO     *pInfo,
  _In_        DWORD             dwNumPatches,
  _In_        DWORD             dwNumVertices,
  _In_        DWORD             dwOptions,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXPATCHMESH   *pPatchMesh
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pinfo* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXPATCHINFO**](d3dxpatchinfo.md) \***

Estructura de información de revisión. Para obtener más información, vea [**D3DXPATCHINFO**](d3dxpatchinfo.md).

</dd> <dt>

*dwNumPatches* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de revisiones.

</dd> <dt>

*dwNumVertices* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de vértices de control de la revisión.

</dd> <dt>

*dwOptions* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Sin usar. Reservado para su uso posterior.

</dd> <dt>

*pDecl* \[ de\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , que describe el formato de vértice de la malla devuelta.

</dd> <dt>

*pD3DDevice* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero el dispositivo que crea la malla de revisión. Vea [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).

</dd> <dt>

*pPatchMesh* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

Puntero al objeto [**ID3DXPatchMesh**](id3dxpatchmesh.md) que se crea.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Este método toma una malla de revisión de entrada y la convierte en una malla teselada. Las mallas de revisión utilizan búferes de índice de 16 bits. Por lo tanto, los índices de [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md) son de 16 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXPATCHINFO**](d3dxpatchinfo.md)
</dt> </dl>

 

 
