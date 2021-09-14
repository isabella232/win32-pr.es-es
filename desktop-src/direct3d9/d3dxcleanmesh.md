---
description: Limpia una malla y la prepara para simplificarla.
ms.assetid: 2b586ecc-db87-4b20-a4fc-c8b547bebf65
title: Función D3DXCleanMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCleanMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5565978dc1ad0e80c33718275ea65080930ce7cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174814"
---
# <a name="d3dxcleanmesh-function"></a>Función D3DXCleanMesh

Limpia una malla y la prepara para simplificarla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCleanMesh(
  _In_        D3DXCLEANTYPE CleanType,
  _In_        LPD3DXMESH    pMeshIn,
  _In_  const DWORD         *pAdjacencyIn,
  _Out_       LPD3DXMESH    *ppMeshOut,
  _Out_       DWORD         *pAdjacencyOut,
  _Out_       LPD3DXBUFFER  *ppErrorsAndWarnings
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CleanType* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXCLEANTYPE**](./d3dxcleantype.md)**

Operaciones de vértice que se realizan como preparación para la limpieza de malla. Vea [**D3DXCLEANTYPE.**](./d3dxcleantype.md)

</dd> <dt>

*pMeshIn* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a una [**interfaz ID3DXMesh,**](id3dxmesh.md) que representa la malla que se va a limpiar.

</dd> <dt>

*pAdjacencyIn* \[ En\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a una matriz de tres DWORD por cara que especifican los tres vecinos de cada cara de la malla que se va a limpiar.

</dd> <dt>

*ppMeshOut* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Dirección de un puntero a una [**interfaz ID3DXMesh,**](id3dxmesh.md) que representa la malla limpia devuelta. Se devuelve la misma malla que se pasó si no era necesaria ninguna limpieza.

</dd> <dt>

*pAdjacencyOut* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero a una matriz de tres DWORD por cara que especifican los tres vecinos de cada cara de la malla de salida.

</dd> <dt>

*ppErrorsAndWarnings* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Devuelve un búfer que contiene una cadena de errores y advertencias, que explican los problemas encontrados en la malla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Esta función limpia una malla mediante el método de limpieza y las opciones especificadas en el parámetro CleanType. Consulte la [**enumeración D3DXCLEANTYPE**](./d3dxcleantype.md) para obtener una descripción de las opciones disponibles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
