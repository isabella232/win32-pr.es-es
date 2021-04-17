---
description: Genera una reasignación de caras optimizada para una lista de triángulos.
ms.assetid: 428c2af8-43e7-4cf7-8b9b-04ba5cff82c8
title: Función D3DXOptimizeFaces (D3DX9Mesh. h)
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
ms.openlocfilehash: 6c56dec04e01b542d2c760852a58826a8186c213
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698178"
---
# <a name="d3dxoptimizefaces-function"></a>D3DXOptimizeFaces función)

Genera una reasignación de caras optimizada para una lista de triángulos.

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

*pIndices* \[ de\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero a los índices de la lista de triángulos que se van a usar para ordenar vértices.

</dd> <dt>

*NumFaces* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de caras en la lista de triángulos. En el caso de las mallas de 16 bits, esto está limitado a 2 ^ 16-1 (65535) o a menos caras.

</dd> <dt>

*NumVertices* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de vértices a los que hace referencia la lista de triángulos.

</dd> <dt>

*Indices32Bit* \[ de\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Marca que indica el tipo de índice: **true** si los índices son de 32 bits (más de 65535 índices), **false** si los índices son de 16 bits (65535 o menos índices).

</dd> <dt>

*pFaceRemap* \[ in, out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero a la superficie de la malla original que se ha dividido para generar la superficie actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

El procedimiento de optimización de esta función es funcionalmente equivalente a llamar a [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) con la \_ marca DEVICEINDEPENDENT de D3DXMESHOPT, pero esta función hace un uso más eficaz de las memorias caché de vértices.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
