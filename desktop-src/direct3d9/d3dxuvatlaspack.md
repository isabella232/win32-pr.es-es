---
description: Empaquetar datos de partición de malla en un atlas.
ms.assetid: 4da85626-c36c-44d9-990b-0db80ed04423
title: Función D3DXUVAtlasPack (D3DX9Mesh.h)
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
ms.openlocfilehash: 6990d6fbc114c874b31d0035a2415d48161d3065718efce3783a041a2097e96f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749665"
---
# <a name="d3dxuvatlaspack-function"></a>Función D3DXUVAtlasPack

Empaquetar datos de partición de malla en un atlas.

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

*pMesh* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a una malla de entrada [**(vea ID3DXMesh)**](id3dxmesh.md)que contiene la geometría del objeto para calcular el atlas. Como mínimo, la malla debe contener datos de posición y coordenadas de textura 2D.

</dd> <dt>

*dwWidth* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ancho de textura.

</dd> <dt>

*dwHeight* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Alto de textura.

</dd> <dt>

*fGutter* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Distancia mínima, en texturas, entre dos gráficos en el atlas. El ancho del medianía siempre se escala; por lo tanto, si se usa un medianera de 2,5 en una textura de 512 x 512, la distancia mínima entre dos gráficos es de 2,5 / 512,0 texturas.

</dd> <dt>

*dwTextureIndex* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice de coordenadas de textura de base cero que identifica el conjunto de coordenadas de textura que se va a usar.

</dd> <dt>

*pdwPartitionResultAdjacency* 
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a una matriz de tres DWORD por cara que especifican los tres vecinos de cada cara de la malla. Debe derivarse de ppPartitionResultAdjacency devuelto desde [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md). Este valor no puede ser **NULL,** porque Pack debe saber dónde se cortaron los gráficos en el paso de partición para encontrar los bordes de cada gráfico.

</dd> <dt>

*pCallback* \[ En\]
</dt> <dd>

Tipo: **[LPD3DVATVATLASCB](lpd3dxuvatlascb.md)**

Puntero a una función de devolución de llamada [(vea LPD3DVATVATLASCB)](lpd3dxuvatlascb.md)que resulta útil para supervisar el progreso.

</dd> <dt>

*fCallbackFrequency* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Especifique la frecuencia con la que D3DX llamará a la devolución de llamada; un valor predeterminado razonable es 0,0001f.

</dd> <dt>

*pUserContent* \[ En\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntero void que se va a devolver a la función de devolución de llamada.

</dd> <dt>

*dwOptions* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Este parámetro de opciones está reservado actualmente.

</dd> <dt>

*pFacePartitioning* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

Puntero a un [**ID3DXBuffer que**](id3dxbuffer.md) contiene la matriz del particionamiento de caras final. Cada elemento contiene un DWORD por cara.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK; de lo contrario, el valor es D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> </dl>

 

 
