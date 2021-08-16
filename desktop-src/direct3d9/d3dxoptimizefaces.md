---
description: Genera un remapping de caras optimizado para una lista de triángulos.
ms.assetid: 428c2af8-43e7-4cf7-8b9b-04ba5cff82c8
title: Función D3DXOptimizeFaces (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeFaces
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 165f81d9b829ce7a7b22ced6fb37851f926ed861f11b79feca3a63c763dabbb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525234"
---
# <a name="d3dxoptimizefaces-function"></a>Función D3DXOptimizeFaces

Genera un remapping de caras optimizado para una lista de triángulos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXOptimizeFaces(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pFaceRemap
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

Número de caras en la lista de triángulos. Para las mallas de 16 bits, se limita a 2^16 - 1 (65535) o menos caras.

</dd> <dt>

*NumVertices* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de vértices a los que hace referencia la lista de triángulos.

</dd> <dt>

*Índices32Bit* \[ En\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Marca que indica el tipo de índice: **TRUE** si los índices son de 32 bits (más de 65535 índices), **FALSE** si los índices son de 16 bits (65535 o menos índices).

</dd> <dt>

*pFaceRemap* \[ in, out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero a la cara de malla original que se dividió para generar la cara actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

El procedimiento de optimización de esta función es funcionalmente equivalente a llamar a [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) con la marca DEVICEINDEPENDENT de D3DXMESHOPT, pero esta función hace un uso más eficaz de las cachés de \_ vértices.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
