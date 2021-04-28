---
description: 'Método ID3DXMesh::Optimize: genera una nueva malla con caras y vértices reordenados para optimizar el rendimiento del dibujo.'
ms.assetid: 6a9bf7b9-2cb9-4b42-92d9-2a121ff79284
title: Método ID3DXMesh::Optimize (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: debec1c0ee54e612ab0de832dbc5c2481dcefad8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093313"
---
# <a name="id3dxmeshoptimize-method"></a>Método ID3DXMesh::Optimize

Genera una nueva malla con caras y vértices reordenados para optimizar el rendimiento del dibujo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Optimize(
  [in]            DWORD        Flags,
  [in]      const DWORD        *pAdjacencyIn,
  [in, out]       DWORD        *pAdjacencyOut,
  [in, out]       DWORD        *pFaceRemap,
  [out]           LPD3DXBUFFER *ppVertexRemap,
  [out]           LPD3DXMESH   *ppOptMesh
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica el tipo de optimización que se debe realizar. Este parámetro se puede establecer en una combinación de una o varias marcas de [**D3DXMESHOPT**](./d3dxmeshopt.md) y [**D3DXMESH**](./d3dxmesh.md) (excepto D3DXMESH \_ 32BIT, D3DXMESH \_ IB WRITEONLY y \_ D3DXMESH \_ WRITEONLY).

</dd> <dt>

*pAdjacencyIn* \[ En\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a una matriz de tres DWORD por cara que especifica los tres vecinos de cada cara de la malla de origen. Si el borde no tiene caras adyacentes, el valor se 0xffffffff. Vea la sección Comentarios.

</dd> <dt>

*pAdjacencyOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero a una matriz de tres DWORD por cara que especifica los tres vecinos de cada cara de la malla optimizada. Si el borde no tiene caras adyacentes, el valor se 0xffffffff.

</dd> <dt>

*pFaceRemap* \[ in, out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Matriz de DWORD, una por cara, que identifica la cara de malla original que corresponde a cada cara de la malla optimizada. Si el valor proporcionado para este argumento es **NULL,** no se devuelven los datos de reasignación de caras.

</dd> <dt>

*ppVertexRemap* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Dirección de un puntero a una [**interfaz ID3DXBuffer,**](id3dxbuffer.md) que contiene un DWORD para cada vértice que especifica cómo se asignan los nuevos vértices a los vértices antiguos. Esta reasignación es útil si necesita modificar los datos externos en función de la nueva asignación de vértices.

</dd> <dt>

*ppOptMesh* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Dirección de un puntero a una [**interfaz ID3DXMesh,**](id3dxmesh.md) que representa la malla optimizada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Este método genera una nueva malla. Antes de ejecutar Optimize, una aplicación debe generar un búfer de adyacencia llamando a [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md). El búfer de adyacencia contiene datos de adyacencia, como una lista de bordes y las caras adyacentes entre sí.

Este método es muy similar al método [**ID3DXBaseMesh::CloneMesh,**](id3dxbasemesh--clonemesh.md) salvo que puede realizar la optimización al generar el nuevo clon de la malla. La malla de salida hereda todos los parámetros de creación de la malla de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh::OptimizeInplace**](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
