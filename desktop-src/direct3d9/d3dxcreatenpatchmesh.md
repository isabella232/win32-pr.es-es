---
description: Crea una malla de N revisiones a partir de una malla de triángulo.
ms.assetid: f565ed0b-72fc-4184-b423-f68b0acfafb0
title: Función D3DXCreateNPatchMesh (D3DX9Mesh.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270220"
---
# <a name="d3dxcreatenpatchmesh-function"></a>Función D3DXCreateNPatchMesh

Crea una malla de N revisiones a partir de una malla de triángulo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateNPatchMesh(
  _In_    LPD3DXMESH      pMeshSysMem,
  _Inout_ LPD3DXPATCHMESH *pPatchMesh
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMeshSysMem* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Dirección de un puntero a una [**interfaz ID3DXMesh**](id3dxmesh.md) que representa el objeto de malla de triángulo.

</dd> <dt>

*pPatchMesh* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

Dirección de un puntero a una [**interfaz ID3DXPatchMesh**](id3dxpatchmesh.md) que representa el objeto de malla de revisión creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




