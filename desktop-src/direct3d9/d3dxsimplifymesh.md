---
description: Genera una malla simplificada con los pesos proporcionados que se acercan lo más posible al valor MinValue determinado.
ms.assetid: 589356a9-f272-4851-92ae-54dbecc0b234
title: Función D3DXSimplifyMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSimplifyMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3cc0bfe18afef7b91dbdf887500b485a446b154cb5775cbf950a7e712a332a9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749785"
---
# <a name="d3dxsimplifymesh-function"></a>Función D3DXSimplifyMesh

Genera una malla simplificada con los pesos proporcionados que se acercan lo más posible al valor MinValue determinado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXSimplifyMesh(
  _In_        LPD3DXMESH           pMesh,
  _In_  const DWORD                *pAdjacency,
  _In_  const D3DXATTRIBUTEWEIGHTS *pVertexAttributeWeights,
  _In_  const FLOAT                *pVertexWeights,
  _In_        DWORD                MinValue,
  _In_        DWORD                Options,
  _Out_       LPD3DXMESH           *ppMesh
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMesh* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a una [**interfaz ID3DXMesh,**](id3dxmesh.md) que representa la malla de origen.

</dd> <dt>

*pAdjacency* \[ En\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a una matriz de tres DWORD por cara que especifican los tres vecinos de cada cara de la malla que se va a simplificar.

</dd> <dt>

*pVertexAttributeWeights* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) \***

Puntero a una [**estructura D3DXATTRIBUTEWEIGHTS,**](d3dxattributeweights.md) que contiene el peso de cada componente de vértice. Si este parámetro se establece en **NULL,** se usa una estructura predeterminada. Vea la sección Comentarios.

</dd> <dt>

*pVertexWeights* \[ En\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Puntero a una matriz de ponderaciones de vértices. Si este parámetro se establece en **NULL,** todos los pesos de vértice se establecen en 1,0.

</dd> <dt>

*MinValue* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de vértices o caras, en función de la marca establecida en el parámetro *Options,* por el que se va a simplificar la malla de origen.

</dd> <dt>

*Opciones* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica opciones de simplificación para la malla. Se puede establecer una de las [**marcas de D3DXMESHSIMP.**](./d3dxmeshsimp.md)

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Dirección de un puntero a una [**interfaz ID3DXMesh,**](id3dxmesh.md) que representa la malla de simplificación devuelta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Esta función genera una malla que tiene vértices o caras *MinValue.*

Si el proceso de simplificación no puede reducir la malla a *MinValue,* la llamada se realiza correctamente porque *MinValue* es un mínimo deseado, no un mínimo absoluto.

Si *pVertexAttributeWeights* se establece en **NULL,** se asignan los valores siguientes a la estructura [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) predeterminada.


```
D3DXATTRIBUTEWEIGHTS AttributeWeights;
    
AttributeWeights.Position  = 1.0;
AttributeWeights.Boundary =  1.0;
AttributeWeights.Normal   =  1.0;
AttributeWeights.Diffuse  =  0.0;
AttributeWeights.Specular =  0.0;
AttributeWeights.Tex[8]   =  {0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0};
```



Esta estructura predeterminada es la que la mayoría de las aplicaciones deben usar porque solo tiene en cuenta el ajuste geométrico y normal. Solo en casos especiales se deben modificar los demás campos de miembro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
