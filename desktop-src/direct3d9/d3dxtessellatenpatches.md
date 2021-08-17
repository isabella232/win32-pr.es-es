---
description: Suaviza la malla dada mediante el esquema de teselación de N revisiones.
ms.assetid: e804905d-ee0b-484f-a621-58b197bd370b
title: Función D3DXTessellateNPatches (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateNPatches
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1df63068f3eef608f797f8048231e744412c32f9e01a31a089c50f8a46465a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122727"
---
# <a name="d3dxtessellatenpatches-function"></a>Función D3DXTessellateNPatches

Suaviza la malla dada mediante el esquema de teselación de N revisiones.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXTessellateNPatches(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const CONST DWORD  *pAdjacencyIn,
  _In_        FLOAT        NumSegs,
  _In_        BOOL         QuadraticInterpNormals,
  _Out_       LPD3DXMESH   *ppMeshOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMeshIn* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a una [**interfaz ID3DXMesh,**](id3dxmesh.md) que representa la malla que se debe tesentar.

</dd> <dt>

*pAdjacencyIn* \[ En\]
</dt> <dd>

Tipo: **const CONST \* DWORD**

Puntero a una matriz de tres DWORD por cara que especifican los tres vecinos de cada cara de la malla de origen. Este parámetro puede ser **NULL.**

</dd> <dt>

*NumSegs* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Número de segmentos por borde a tessentar.

</dd> <dt>

*QuadraticInterpNormals* \[ En\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Establezca en **TRUE** para usar la interpolación cuadrática para las normales; se establece **en FALSE** para la interpolación lineal.

</dd> <dt>

*ppMeshOut* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Dirección de un puntero a una [**interfaz ID3DXMesh,**](id3dxmesh.md) que representa la malla teselada devuelta.

</dd> <dt>

*ppAdjacencyOut* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Dirección de un puntero a una [**interfaz ID3DXBuffer.**](id3dxbuffer.md) Si el valor de este parámetro no se establece en **NULL,** este búfer contendrá una matriz de tres DWORD por cara que especifican los tres vecinos para cada cara de la malla de salida. Este parámetro puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Esta función se tesenta mediante el algoritmo N-patch.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
