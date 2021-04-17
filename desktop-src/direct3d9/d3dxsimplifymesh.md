---
description: Genera una malla simplificada usando los pesos proporcionados lo más cerca posible del MinValue dado.
ms.assetid: 589356a9-f272-4851-92ae-54dbecc0b234
title: Función D3DXSimplifyMesh (D3DX9Mesh. h)
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
ms.openlocfilehash: 0258047631a41e31d108ba45531988e4cb6a35ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717735"
---
# <a name="d3dxsimplifymesh-function"></a>D3DXSimplifyMesh función)

Genera una malla simplificada usando los pesos proporcionados lo más cerca posible del MinValue dado.

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

*pmesh* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla de origen.

</dd> <dt>

*pAdjacency* \[ de\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla que se van a simplificar.

</dd> <dt>

*pVertexAttributeWeights* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) \***

Puntero a una estructura [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) , que contiene el peso de cada componente de vértice. Si este parámetro se establece en **null**, se usa una estructura predeterminada. Vea la sección Comentarios.

</dd> <dt>

*pVertexWeights* \[ de\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Puntero a una matriz de pesos de vértice. Si este parámetro se establece en **null**, todos los pesos de vértice se establecen en 1,0.

</dd> <dt>

*MinValue* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de vértices o caras, dependiendo del marcador establecido en el parámetro *Options* , por el que se va a simplificar la malla de origen.

</dd> <dt>

*Opciones* \[ de de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica las opciones de simplificación para la malla. Se puede establecer una de las marcas de [**D3DXMESHSIMP**](./d3dxmeshsimp.md) .

</dd> <dt>

*ppMesh* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Dirección de un puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla de simplificación devuelta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Esta función genera una malla que tiene vértices o caras *MinValue* .

Si el proceso de simplificación no puede reducir la malla a *MinValue*, la llamada todavía se realiza correctamente porque *MinValue* es un mínimo deseado, no un mínimo absoluto.

Si *pVertexAttributeWeights* se establece en **null**, los valores siguientes se asignan a la estructura [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) predeterminada.


```
D3DXATTRIBUTEWEIGHTS AttributeWeights;
    
AttributeWeights.Position  = 1.0;
AttributeWeights.Boundary =  1.0;
AttributeWeights.Normal   =  1.0;
AttributeWeights.Diffuse  =  0.0;
AttributeWeights.Specular =  0.0;
AttributeWeights.Tex[8]   =  {0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0};
```



Esta estructura predeterminada es lo que la mayoría de las aplicaciones deben usar porque solo tiene en cuenta el ajuste geométrico y normal. Solo en casos especiales, los demás campos de miembro deben modificarse.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
