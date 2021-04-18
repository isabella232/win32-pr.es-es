---
description: Crea una malla de N revisiones a partir de una malla triangular.
ms.assetid: f565ed0b-72fc-4184-b423-f68b0acfafb0
title: Función D3DXCreateNPatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateNPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ab73d1254700808bbd56b7b46f7781b27b188b7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698402"
---
# <a name="d3dxcreatenpatchmesh-function"></a>D3DXCreateNPatchMesh función)

Crea una malla de N revisiones a partir de una malla triangular.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateNPatchMesh(
  _In_    LPD3DXMESH      pMeshSysMem,
  _Inout_ LPD3DXPATCHMESH *pPatchMesh
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMeshSysMem* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Dirección de un puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa el objeto de malla de triángulo.

</dd> <dt>

*pPatchMesh* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

Dirección de un puntero a una interfaz [**ID3DXPatchMesh**](id3dxpatchmesh.md) que representa el objeto de malla de revisión creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




