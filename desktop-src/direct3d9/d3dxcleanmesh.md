---
description: Limpia una malla y la prepara para simplificarla.
ms.assetid: 2b586ecc-db87-4b20-a4fc-c8b547bebf65
title: Función D3DXCleanMesh (D3DX9Mesh. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649423"
---
# <a name="d3dxcleanmesh-function"></a>D3DXCleanMesh función)

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

*CleanType* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXCLEANTYPE**](./d3dxcleantype.md)**

Operaciones de vértices que se deben realizar como preparación para la limpieza de malla. Vea [**D3DXCLEANTYPE**](./d3dxcleantype.md).

</dd> <dt>

*pMeshIn* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla que se va a limpiar.

</dd> <dt>

*pAdjacencyIn* \[ de\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos de cada una de las caras de la malla que se van a limpiar.

</dd> <dt>

*ppMeshOut* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Dirección de un puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla limpiada devuelta. Se devuelve la misma malla que se pasó si no se necesita ninguna limpieza.

</dd> <dt>

*pAdjacencyOut* \[ enuncia\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla de salida.

</dd> <dt>

*ppErrorsAndWarnings* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Devuelve un búfer que contiene una cadena de errores y advertencias, que explican los problemas encontrados en la malla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Esta función limpia una malla mediante el método de limpieza y las opciones especificadas en el parámetro CleanType. Vea la enumeración [**D3DXCLEANTYPE**](./d3dxcleantype.md) para obtener una descripción de las opciones disponibles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
