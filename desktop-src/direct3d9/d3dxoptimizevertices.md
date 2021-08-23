---
description: Genera una nueva distribución de vértices optimizada para una lista de triángulos. Esta función se usa normalmente después de aplicar el remapping facial generado por D3DXOptimizeFaces.
ms.assetid: a3b9cb68-204e-4e8f-a985-738d1cea1e29
title: Función D3DXOptimizeVertices (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeVertices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a60d7d47e78cd197a7bfcf6285509c9187e32e074347f63f8e76ef9ef866adfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044803"
---
# <a name="d3dxoptimizevertices-function"></a>Función D3DXOptimizeVertices

Genera una nueva distribución de vértices optimizada para una lista de triángulos. Esta función se usa normalmente después de aplicar el remapping facial generado por [**D3DXOptimizeFaces**](d3dxoptimizefaces.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXOptimizeVertices(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pVertexRemap
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pIndices* \[ En\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero a índices de lista de triángulos que se usarán para ordenar los vértices.

</dd> <dt>

*NumFaces* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de caras en la lista de triángulos.

</dd> <dt>

*NumVertices* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de vértices a los que hace referencia la lista de triángulos.

</dd> <dt>

*Índices32Bit* \[ En\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Marca que indica el tipo de índice: **TRUE** si los índices son de 32 bits (más de 65535 vértices), **FALSE** si los índices son de 16 bits (65535 o menos vértices).

</dd> <dt>

*pVertexRemap* \[ in, out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero a un búfer de destino que contendrá el nuevo índice para cada vértice. El valor almacenado en *pVertexRemap para* un elemento determinado es la ubicación del vértice de origen en la nueva ordenación de vértices.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

De forma predeterminada, una malla usa índices de 16 bits cuando se crea a menos que la aplicación especifique lo contrario. Para comprobar si una malla existente usa índices de 16 o 32 bits, llame a [**ID3DXBaseMesh::GetOptions**](id3dxbasemesh--getoptions.md) y compruebe la marca D3DXMESH \_ de 32 BITS.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
