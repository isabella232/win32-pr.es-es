---
description: Tessellates la malla determinada mediante el esquema de teselación de N-patch.
ms.assetid: e804905d-ee0b-484f-a621-58b197bd370b
title: Función D3DXTessellateNPatches (D3DX9Mesh. h)
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
ms.openlocfilehash: 9c8811816447deb858b5c8b42d651d219f06fef5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717701"
---
# <a name="d3dxtessellatenpatches-function"></a>D3DXTessellateNPatches función)

Tessellates la malla determinada mediante el esquema de teselación de N-patch.

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

*pMeshIn* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla a dividirlas.

</dd> <dt>

*pAdjacencyIn* \[ de\]
</dt> <dd>

Tipo: **CONST const DWORD \***

Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla de origen. Este parámetro puede ser **null**.

</dd> <dt>

*NumSegs* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Número de segmentos por borde a dividirlas.

</dd> <dt>

*QuadraticInterpNormals* \[ de\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Establézcalo en **true** para usar la interpolación cuadrática para las normales; establézcalo en **false** para la interpolación lineal.

</dd> <dt>

*ppMeshOut* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Dirección de un puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla teselada devuelta.

</dd> <dt>

*ppAdjacencyOut* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) . Si el valor de este parámetro no se establece en **null**, este búfer contendrá una matriz de tres valores DWORD por cada tipo que especifique los tres vecinos para cada una de las caras de la malla de salida. Este parámetro puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Esta función tessellates con el algoritmo N-patch.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
