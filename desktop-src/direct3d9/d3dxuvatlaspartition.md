---
description: Cree un Atlas UV para una malla.
ms.assetid: c46f3e47-8e72-435c-875d-cccfa4b893a2
title: Función D3DXUVAtlasPartition (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPartition
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 707a503832a4fd66ab2e8d9346587d11544a885c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707862"
---
# <a name="d3dxuvatlaspartition-function"></a>D3DXUVAtlasPartition función)

Cree un Atlas UV para una malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXUVAtlasPartition(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContent,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    pFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
              LPD3DXBUFFER    *ppPartitionResultAdjacency,
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

*dwTextureIndex* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice de coordenadas de textura basado en cero que identifica el conjunto de coordenadas de textura que se va a usar.

</dd> <dt>

*pdwAdjacency* \[ de\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a una matriz de datos de adyacencia con 3 DWORDs por caras, que indica qué triángulos son adyacentes entre sí (vea [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).

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

Especifique la calidad de los gráficos generados mediante la combinación de una o varias marcas de [**D3DXUVATLAS**](./d3dxuvatlas.md) .

</dd> <dt>

*ppMeshOut* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Puntero a la malla creada con el Atlas (vea [**ID3DXMesh**](id3dxmesh.md)).

</dd> <dt>

*pFacePartitioning* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

Puntero a una matriz de los datos finales de partición de caras. Cada elemento contiene un valor DWORD por cada tipo de letra (vea [**ID3DXBuffer**](id3dxbuffer.md)).

</dd> <dt>

*ppVertexRemapArray* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntero a una matriz de vértices reasignados. Cada elemento de la matriz identifica el vértice original del que proceden los vértices finales (si el vértice se dividió durante la reasignación). Cada elemento de la matriz contiene un valor DWORD por vértice.

</dd> <dt>

*ppPartitionResultAdjacency* 
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) . Este búfer contendrá una matriz de tres DWORD por cada tipo que especifique los tres vecinos para cada una de las caras de la malla de salida. Este parámetro no debe ser **null**, ya que la siguiente llamada a D3DXUVAtlasPack () lo requiere.

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

D3DXUVAtlasPartition es similar a [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md), salvo que D3DXUVAtlasPartition no realiza el paso de empaquetado final.

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

 

 
