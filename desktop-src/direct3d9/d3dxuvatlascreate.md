---
description: Cree un Atlas UV para una malla.
ms.assetid: 70256990-b177-451e-b42a-84799fdc2a17
title: Función D3DXUVAtlasCreate (D3DX9Mesh. h)
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
ms.openlocfilehash: 814f213b0195b0922270d0548d8b5fd4c48fb3e3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717699"
---
# <a name="d3dxuvatlascreate-function"></a>D3DXUVAtlasCreate función)

Cree un Atlas UV para una malla.

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

*pmesh* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a una malla de entrada (vea [**ID3DXMesh**](id3dxmesh.md)) que contiene la geometría del objeto para calcular el Atlas. Como mínimo, la malla debe contener datos de posición y coordenadas de textura 2D.

</dd> <dt>

*dwMaxChartNumber* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número máximo de gráficos en los que se va a particionar la malla. Vea comentarios sobre los modos de creación de particiones. Use 0 para indicar a D3DX que el Atlas debe parametrizarse en función de Stretch.

</dd> <dt>

*fMaxStretch* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

La cantidad de ajuste permitido. 0 significa que no se permite la expansión; 1 significa que se puede usar cualquier cantidad de ajuste.

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

*pdwAdjacency* \[ de\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a una matriz de datos de adyacencia. con 3 DWORDs por caras, que indican qué triángulos son adyacentes entre sí (vea [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).

</dd> <dt>

*pdwFalseEdges* 
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Una matriz con 3 DWORDs por caras. Cada una de las caras indica si un borde es falso o no. Un borde que no sea falso se indica mediante-1, un borde falso se indica con cualquier otro valor. Esto permite la parametrización de una malla de cuádruples, donde los bordes inferiores a la mitad de cada cuádruple no se cortarán.

</dd> <dt>

*pfIMTArray* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero a una matriz de decenas de métricas integrados que describe cómo expandir un triángulo (vea [IntegratedMetricTensor](using-uvatlas.md)).

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

Puntero a un valor definido por el usuario que se pasa a la función de devolución de llamada; lo suele usar una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.

</dd> <dt>

*dwOptions* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifique la calidad de los gráficos generados. Vea [**D3DXUVATLAS**](./d3dxuvatlas.md).

</dd> <dt>

*ppMeshOut* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Puntero a la malla creada con el Atlas (vea [**ID3DXMesh**](id3dxmesh.md)).

</dd> <dt>

*ppFacePartitioning* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntero a una matriz de los datos finales de partición de caras. Cada elemento contiene un valor DWORD por cada tipo de letra (vea [**ID3DXBuffer**](id3dxbuffer.md)).

</dd> <dt>

*ppVertexRemapArray* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntero a una matriz de vértices reasignados. Cada elemento de la matriz identifica el vértice original del que proceden los vértices finales (si el vértice se dividió durante la reasignación). Cada elemento de la matriz contiene un valor DWORD por vértice.

</dd> <dt>

*pfMaxStretchOut* \[ enuncia\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero al valor de stretch máximo generado por el algoritmo de Atlas. El intervalo está comprendido entre 0,0 y 1,0.

</dd> <dt>

*pdwNumChartsOut* \[ enuncia\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntero al número de gráficos creados por el algoritmo de Atlas. Si dwMaxChartNumber es demasiado bajo, este parámetro devolverá el número mínimo de gráficos necesarios para crear un Atlas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK; de lo contrario, el valor es D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

D3DXUVAtlasCreate puede crear particiones de la geometría de malla de dos maneras:

-   Basado en el número de gráficos
-   Basado en el ajuste máximo permitido. Si el ajuste máximo permitido es 0, es probable que cada triángulo esté en su propio gráfico.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Herramienta de Command-Line de Atlas de UV (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)
</dt> </dl>

 

 
