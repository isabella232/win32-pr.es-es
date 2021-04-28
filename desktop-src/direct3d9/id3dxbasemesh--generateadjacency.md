---
description: 'Método ID3DXBaseMesh::GenerateAdjacency: genere una lista de bordes de malla, así como una lista de caras que comparten cada borde.'
ms.assetid: 9d52290f-1c9e-43a7-b239-35cd54e36466
title: Método ID3DXBaseMesh::GenerateAdjacency (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 783ed7ad61337e606793b9b467e4b17fddd7ecd2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115463"
---
# <a name="id3dxbasemeshgenerateadjacency-method"></a>Método ID3DXBaseMesh::GenerateAdjacency

Genere una lista de bordes de malla, así como una lista de caras que comparten cada borde.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT Epsilon,
  [in] DWORD *pAdjacency
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Epsilon* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Especifica que los vértices que difieren en la posición en menos de epsilon deben tratarse como coincidentes.

</dd> <dt>

*pAdjacency* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero a una matriz de tres DWORD por cara que se va a rellenar con los índices de caras adyacentes. El número de bytes de esta matriz debe ser al menos \* [**3 ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Una vez que una aplicación genera información de adyacencia para una malla, los datos de la malla se pueden optimizar para mejorar el rendimiento del dibujo.

El orden de las entradas del búfer de adyacencia viene determinado por el orden de los índices de vértice en el búfer de índice. El triángulo adyacente 0 siempre se corresponde con el borde entre los índices de las esquinas 0 y 1. El triángulo adyacente 1 siempre corresponde al borde entre los índices de las esquinas 1 y 2, mientras que el triángulo adyacente 2 corresponde al borde entre los índices de las esquinas 2 y 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**ID3DXMesh::Optimize**](id3dxmesh--optimize.md)
</dt> <dt>

[**ID3DXMesh::OptimizeInplace**](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
