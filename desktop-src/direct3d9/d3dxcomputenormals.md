---
description: Calcula las normales de unidad para cada vértice de una malla. Proporcionado para admitir aplicaciones heredadas. Use D3DXComputeTangentFrameEx para obtener mejores resultados.
ms.assetid: 7c879149-2c4c-4824-9604-e88696cc6ddc
title: Función D3DXComputeNormals (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormals
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f95e5e353c318429f5340d1a831f9ca3050ba3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003868"
---
# <a name="d3dxcomputenormals-function"></a>D3DXComputeNormals función)

Calcula las normales de unidad para cada vértice de una malla. Proporcionado para admitir aplicaciones heredadas. Use [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) para obtener mejores resultados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXComputeNormals(
  _Inout_       LPD3DXBASEMESH pMesh,
  _In_    const DWORD          *pAdjacency
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pmesh* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Puntero a una interfaz [**ID3DXBaseMesh**](id3dxbasemesh.md) que representa el objeto de malla normalizado.

</dd> <dt>

*pAdjacency* \[ de\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla progresiva creada. Este parámetro es opcional y debe establecerse en **null** si no se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

La malla de entrada debe tener la marca [D3DFVF \_ normal](d3dfvf.md) especificada en su formato de vértice flexible (FVF).

La normalización de un vértice se genera al calcular el promedio de las normales de todas las caras que comparten dicho vértice.

Si se proporciona adyacencia, se omiten los vértices replicados y se "suavizan". Si no se proporciona la adyacencia, los vértices replicados tendrán un promedio de normalización de solo los rostros a los que se hace referencia explícitamente.

Esta función simplemente llama a [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) con los siguientes parámetros de entrada:


```
D3DXComputeTangentFrameEx( pMesh,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DDECLUSAGE_NORMAL,
                           0,
                           D3DXTANGENT_GENERATE_IN_PLACE | D3DXTANGENT_CALCULATE_NORMALS,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
