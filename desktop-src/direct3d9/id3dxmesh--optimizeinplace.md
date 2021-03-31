---
description: Genera una malla con caras y vértices reordenados para optimizar el rendimiento del dibujo. Este método reordena la malla existente.
ms.assetid: 2cdaf627-d1d3-44f0-a5ae-9023d4b0de45
title: 'ID3DXMesh:: OptimizeInplace (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.OptimizeInplace
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f889e0d3754cc1321ffa59eba294038b87991489
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821426"
---
# <a name="id3dxmeshoptimizeinplace-method"></a>ID3DXMesh:: OptimizeInplace (método)

Genera una malla con caras y vértices reordenados para optimizar el rendimiento del dibujo. Este método reordena la malla existente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OptimizeInplace(
  [in]        DWORD        Flags,
  [in]  const DWORD        *pAdjacencyIn,
  [out]       DWORD        *pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de una o varias marcas [**D3DXMESHOPT**](./d3dxmeshopt.md) , especificando el tipo de optimización que se va a realizar.

</dd> <dt>

*pAdjacencyIn* \[ de\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla de origen. Si el borde no tiene caras adyacentes, el valor es 0xFFFFFFFF.

</dd> <dt>

*pAdjacencyOut* \[ enuncia\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla optimizada. Si el borde no tiene caras adyacentes, el valor es 0xFFFFFFFF. Si el valor proporcionado para este argumento es **null**, no se devuelven los datos de adyacencia.

</dd> <dt>

*pFaceRemap* \[ enuncia\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Matriz de DWORDs, una por cada tipo, que identifica la superficie de la malla original que corresponde a cada una de las caras de la malla optimizada. Si el valor proporcionado para este argumento es **null**, no se devuelven los datos de reasignación de caras.

</dd> <dt>

*ppVertexRemap* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) , que contiene un valor DWORD para cada vértice que especifica cómo se asignan los nuevos vértices a los vértices anteriores. Esta reasignación es útil si necesita modificar los datos externos en función de la nueva asignación de vértices. Si el valor proporcionado para este argumento es **null**, no se devuelven los datos de reasignación de vértices.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ CANNOTATTRSORT, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Antes de ejecutar **ID3DXMesh:: OptimizeInplace**, una aplicación debe generar un búfer de adyacencia llamando a [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md). El búfer de adyacencia contiene datos de adyacencias, como una lista de bordes y las caras adyacentes entre sí.

> [!Note]  
> Este método producirá un error si la malla comparte su búfer de vértice con otra malla, a menos que el \_ IGNOREVERTS de D3DXMESHOPT se establezca en marcas.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md)
</dt> </dl>

 

 
