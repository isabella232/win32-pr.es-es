---
description: Divide una malla en mallas menores que el tamaño especificado.
ms.assetid: 55cdd82f-91fa-4805-969f-8fbe53cbde58
title: Función D3DXSplitMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSplitMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1f01cdb4ddd009f5cdf0b7f0310a492840955f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717734"
---
# <a name="d3dxsplitmesh-function"></a>D3DXSplitMesh función)

Divide una malla en mallas menores que el tamaño especificado.

## <a name="syntax"></a>Sintaxis


```C++
void D3DXSplitMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacencyIn,
  _In_  const DWORD        MaxSize,
  _In_  const DWORD        Options,
  _Out_       DWORD        *pMeshesOut,
  _Out_       LPD3DXBUFFER *ppMeshArrayOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyArrayOut,
  _Out_       LPD3DXBUFFER *ppFaceRemapArrayOut,
  _Out_       LPD3DXBUFFER *ppVertRemapArrayOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMeshIn* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla de origen.

</dd> <dt>

*pAdjacencyIn* \[ de\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla que se van a simplificar.

</dd> <dt>

*MaxSize* \[ de\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md)**

Número máximo de vértices en la malla resultante.

</dd> <dt>

*Opciones* \[ de de\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md)**

Marcas de opciones para las nuevas mallas.

</dd> <dt>

*pMeshesOut* \[ enuncia\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Número de mallas devueltas.

</dd> <dt>

*ppMeshArrayOut* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Búfer que contiene una matriz de interfaces [**ID3DXMesh**](id3dxmesh.md) para las nuevas mallas. Para una división de la malla de origen en n mallas, *ppMeshArrayOut* es una matriz de n punteros **ID3DXMesh** .

</dd> <dt>

*ppAdjacencyArrayOut* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Búfer que contiene una matriz de matrices de adyacencias (DWORDs) para las nuevas mallas. Vea [**ID3DXBuffer**](id3dxbuffer.md). Este parámetro es opcional.

</dd> <dt>

*ppFaceRemapArrayOut* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Búfer que contiene una matriz de matrices de reasignación de caras (DWORDs) para las nuevas mallas. Vea [**ID3DXBuffer**](id3dxbuffer.md). Este parámetro es opcional.

</dd> <dt>

*ppVertRemapArrayOut* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Búfer que contiene una matriz de matrices de reasignación de vértices para las nuevas mallas. Vea [**ID3DXBuffer**](id3dxbuffer.md). Este parámetro es opcional.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Un uso común de esta función es dividir una malla con índices de 32 bits (más de 65535 vértices) en más de una malla, cada una de las cuales tiene índices de 16 bits.

Las matrices de tipo adyacencia, reasignación de vértices y asignación de caras son matrices son DWORDs donde cada matriz contiene n punteros DWORD, seguidos de los datos DWORD a los que hacen referencia los punteros. Por ejemplo, para obtener la información de reasignación de caras de la esfera 3 de la malla 2, se podría usar el código siguiente, suponiendo que los datos de reasignación de caras se devolvieron en una variable denominada *ppFaceRemapArrayOut*.


```
   
const DWORD **face_remaps = 
    static_cast<DWORD **>(ppFaceRemapArrayOut->GetBufferPointer());
const DWORD remap = face_remaps[2][3];
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

 

 
