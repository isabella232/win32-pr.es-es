---
description: Empaquetar los datos de la partición de malla en un Atlas.
ms.assetid: 4da85626-c36c-44d9-990b-0db80ed04423
title: Función D3DXUVAtlasPack (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPack
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31de326160120fe14a71841cb5f2d18e1c8d4e57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717725"
---
# <a name="d3dxuvatlaspack-function"></a>D3DXUVAtlasPack función)

Empaquetar los datos de la partición de malla en un Atlas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXUVAtlasPack(
  _In_       LPD3DXMESH      pMesh,
  _In_       UINT            dwWidth,
  _In_       UINT            dwHeight,
  _In_       FLOAT           fGutter,
  _In_       DWORD           dwTextureIndex,
       const DWORD           *pdwPartitionResultAdjacency,
  _In_       LPD3DXUVATLASCB pCallback,
  _In_       FLOAT           fCallbackFrequency,
  _In_       LPVOID          pUserContent,
  _In_       DWORD           dwOptions,
  _In_       LPD3DXBUFFER    pFacePartitioning
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pmesh* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a una malla de entrada (vea [**ID3DXMesh**](id3dxmesh.md)) que contiene la geometría del objeto para calcular el Atlas. Como mínimo, la malla debe contener datos de posición y coordenadas de textura 2D.

</dd> <dt>

*dwWidth* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ancho de la textura.

</dd> <dt>

*dwHeight* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Alto de textura.

</dd> <dt>

*fGutter* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Distancia mínima, en textura, entre dos gráficos en el Atlas. El margen se escala siempre por el ancho; por lo tanto, si se usa un medianil de 2,5 en una textura 512 x 512, la distancia mínima entre dos gráficos es 2,5/512,0 textura.

</dd> <dt>

*dwTextureIndex* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice de coordenadas de textura basado en cero que identifica el conjunto de coordenadas de textura que se va a usar.

</dd> <dt>

*pdwPartitionResultAdjacency* 
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla. Debe derivarse del ppPartitionResultAdjacency devuelto desde [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md). Este valor no puede ser **null** porque Pack debe saber dónde se han cortado los gráficos en el paso de partición para encontrar los bordes de cada gráfico.

</dd> <dt>

*pCallback* \[ de\]
</dt> <dd>

Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Un puntero a una función de devolución de llamada (vea [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) que es útil para supervisar el progreso.

</dd> <dt>

*fCallbackFrequency* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Especificar la frecuencia con la que D3DX llamará a la devolución de llamada; un valor predeterminado razonable es 0,0001 f.

</dd> <dt>

*pUserContent* \[ de\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntero void que se va a devolver a la función de devolución de llamada.

</dd> <dt>

*dwOptions* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Este parámetro de opciones está actualmente reservado.

</dd> <dt>

*pFacePartitioning* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

Un puntero a un [**ID3DXBuffer**](id3dxbuffer.md) que contiene la matriz de la creación de particiones de caras final. Cada elemento contiene un valor DWORD por cada tipo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK; de lo contrario, el valor es D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> </dl>

 

 
