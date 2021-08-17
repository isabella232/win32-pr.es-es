---
description: Valida una malla de revisión y devuelve el número de vértices y revisiones degenerados.
ms.assetid: a95ff9d9-d476-42ac-8d7e-1dc42418f763
title: Función D3DXValidPatchMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c3b7b28c763691af83dbb1ed0fe406fa6d370c82f9d8ffa702afa69566f2597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523821"
---
# <a name="d3dxvalidpatchmesh-function"></a>Función D3DXValidPatchMesh

Valida una malla de revisión y devuelve el número de vértices y revisiones degenerados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXValidPatchMesh(
  _In_  LPD3DXPATCHMESH pMeshIn,
  _Out_ DWORD           *pNumDegenerateVertices,
  _Out_ DWORD           *pNumDegeneratePatches,
  _Out_ LPD3DXBUFFER    *ppErrorsAndWarnings
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMeshIn* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)**

Puntero a una [**interfaz ID3DXPatchMesh,**](id3dxpatchmesh.md) que representa la malla de revisión que se va a probar.

</dd> <dt>

*pNumDegenerateVertices* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Devuelve el número de vértices degenerados en la malla de revisión.

</dd> <dt>

*pNumDegeneratePatches* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Devuelve el número de revisiones degeneradas en la malla de revisión.

</dd> <dt>

*ppErrorsAndWarnings* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Devuelve un puntero a un búfer que contiene una cadena de errores y advertencias que explican los problemas encontrados en la malla de revisión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Este método valida la malla mediante la comprobación de índices no válidos. La información de error está disponible en la salida del depurador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
