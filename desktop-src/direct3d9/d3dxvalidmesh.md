---
description: Valida una malla.
ms.assetid: e5bec2f3-e914-4677-8114-77c71b8a586e
title: Función D3DXValidMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 469b9b32072107885417266266f804a955301668
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060712"
---
# <a name="d3dxvalidmesh-function"></a>Función D3DXValidMesh

Valida una malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXValidMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacency,
  _Out_       LPD3DXBUFFER *ppErrorsAndWarnings
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMeshIn* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a una [**interfaz ID3DXMesh,**](id3dxmesh.md) que representa la malla que se va a probar.

</dd> <dt>

*pAdjacency* \[ En\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a una matriz de tres DWORD por cara que especifican los tres vecinos de cada cara de la malla que se va a probar.

</dd> <dt>

*ppErrorsAndWarnings* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Devuelve un búfer que contiene una cadena de errores y advertencias, que explican los problemas encontrados en la malla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DXERR \_ INVALIDMESH, D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

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

 

 
