---
description: 'Función D3DXUVAtlasCreate: cree un atlas UV para una malla.'
ms.assetid: 70256990-b177-451e-b42a-84799fdc2a17
title: Función D3DXUVAtlasCreate (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasCreate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f382e7d59f3a5b5db8ba3cfd65ba6cc1a11e86d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566081"
---
# <a name="d3dxuvatlascreate-function"></a>Función D3DXUVAtlasCreate

Cree un atlas UV para una malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXUVAtlasCreate(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        UINT            dwWidth,
  _In_        UINT            dwHeight,
  _In_        FLOAT           fGutter,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContext,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    *ppFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
  _Out_       FLOAT           *pfMaxStretchOut,
  _Out_       UINT            *pdwNumChartsOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMesh* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a una malla de entrada [**(vea ID3DXMesh)**](id3dxmesh.md)que contiene la geometría del objeto para calcular el atlas. Como mínimo, la malla debe contener datos de posición y coordenadas de textura 2D.

</dd> <dt>

*dwMaxChartNumber* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número máximo de gráficos en los que se particiona la malla. Vea comentarios sobre los modos de creación de particiones. Use 0 para decir a D3DX que el atlas debe parametrizarse en función de stretch.

</dd> <dt>

*fMaxStretch* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Cantidad de extensión permitida. 0 significa que no se permite ningún stretching, 1 significa que se puede usar cualquier cantidad de stretching.

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

*pdwAdjacency* \[ En\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a una matriz de datos de adyacencia. con 3 DWORD por cara, lo que indica qué triángulos son adyacentes entre sí (vea [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).

</dd> <dt>

*pdwFalseEdges* 
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Matriz con 3 DWORDS por cara. Cada cara indica si un borde es false o no. Un borde no falso se indica mediante -1, un borde falso se indica mediante cualquier otro valor. Esto permite parametrizar una malla de cuádros donde no se cortarán los bordes del centro de cada cuatro.

</dd> <dt>

*pfIMTArray* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a una matriz de tensores de métricas integrados que describe cómo extender un triángulo (vea [IntegratedMetricTensor](using-uvatlas.md)).

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

Puntero a un valor definido por el usuario que se pasa a la función de devolución de llamada; normalmente lo usa una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.

</dd> <dt>

*dwOptions* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifique la calidad de los gráficos generados. Vea [**D3DVATVATLAS**](./d3dxuvatlas.md).

</dd> <dt>

*ppMeshOut* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Puntero a la malla creada con el atlas [**(vea ID3DXMesh).**](id3dxmesh.md)

</dd> <dt>

*ppFacePartitioning* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntero a una matriz de los datos finales de partición de caras. Cada elemento contiene un DWORD por cara (vea [**ID3DXBuffer).**](id3dxbuffer.md)

</dd> <dt>

*ppVertexRemapArray* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntero a una matriz de vértices remapped. Cada elemento de matriz identifica el vértice original del que provenía cada vértice final (si el vértice se dividió durante la remapping). Cada elemento de matriz contiene un DWORD por vértice.

</dd> <dt>

*pfMaxStretchOut* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero al valor de stretch máximo generado por el algoritmo atlas. El intervalo está entre 0,0 y 1,0.

</dd> <dt>

*pdwNumChartsOut* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntero al número de gráficos creados por el algoritmo atlas. Si dwMaxChartNumber es demasiado bajo, este parámetro devolverá el número mínimo de gráficos necesarios para crear un atlas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK; de lo contrario, el valor es D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

D3DXUVAtlasCreate puede particionar la geometría de malla de dos maneras:

-   En función del número de gráficos
-   En función del límite máximo permitido. Si el stretch máximo permitido es 0, es probable que cada triángulo esté en su propio gráfico.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Uv Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)
</dt> </dl>

 

 
