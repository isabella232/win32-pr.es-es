---
description: Convierta el subconjunto de malla especificado en una serie de franjas.
ms.assetid: 4f005383-6a5a-4393-ac88-202e45946d3d
title: Función D3DXConvertMeshSubsetToStrips (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToStrips
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 345c80305f42df410f42cf255f1b9e0d8f353b448134779b416d686db4b40c05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526793"
---
# <a name="d3dxconvertmeshsubsettostrips-function"></a>Función D3DXConvertMeshSubsetToStrips

Convierta el subconjunto de malla especificado en una serie de franjas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXConvertMeshSubsetToStrips(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices,
  _Out_ LPD3DXBUFFER           *ppStripLengths,
  _Out_ DWORD                  *pNumStrips
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*MeshIn* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Puntero a una [**interfaz ID3DXBaseMesh,**](id3dxbasemesh.md) que representa la malla que se convertirá en una franja.

</dd> <dt>

*AttribId* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Identificador de atributo del subconjunto de malla que se convertirá en franjas.

</dd> <dt>

*IBOptions* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de una o varias marcas de la enumeración [**D3DXMESH,**](./d3dxmesh.md) especificando las opciones para crear el búfer de índice. No puede ser D3DXMESH \_ de 32 BITS. El búfer de índice se creará con índices de 32 o 16 bits en función del formato del búfer de índice de la malla especificado por el *parámetro MeshIn.*

</dd> <dt>

*ppIndexBuffer* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***

Puntero a una [**interfaz IDirect3DIndexBuffer9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) que representa el búfer de índice que contiene la franja.

</dd> <dt>

*pNumIndices* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Número de índices en el búfer devueltos en el *parámetro ppIndexBuffer.*

</dd> <dt>

*ppStripLengths* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Búfer que contiene una matriz de un DWORD por franja, que especifica el número de triángulos de esa franja.

</dd> <dt>

*pNumStrips* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Número de franjas individuales en el búfer de índice y la matriz de longitud de franja correspondiente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Antes de ejecutar esta función, llame a [**Optimize**](id3dxmesh--optimize.md) o [**D3DXOptimizeFaces**](d3dxoptimizefaces.md), con la marca D3DXMESHOPT \_ ATTRSORT establecida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
