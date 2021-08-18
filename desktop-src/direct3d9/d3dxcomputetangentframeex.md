---
description: Realiza cálculos de fotogramas tangentes en una malla. Se generan vectores tangentes, binormales y opcionalmente normales. Las singularidades se controlan según sea necesario mediante la agrupación de bordes y la división de vértices.
ms.assetid: 15cc46bc-6db6-4e1d-a95e-cd60d2666600
title: Función D3DXComputeTangentFrameEx (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrameEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d091b7ca243e4833cd6aa36a409fca32069e52a267ec3f588b338777ed34338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988681"
---
# <a name="d3dxcomputetangentframeex-function"></a>Función D3DXComputeTangentFrameEx

Realiza cálculos de fotogramas tangentes en una malla. Se generan vectores tangentes, binormales y opcionalmente normales. Las singularidades se controlan según sea necesario mediante la agrupación de bordes y la división de vértices.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXComputeTangentFrameEx(
  _In_        ID3DXMesh   *pMesh,
  _In_        DWORD       dwTextureInSemantic,
  _In_        DWORD       dwTextureInIndex,
  _In_        DWORD       dwUPartialOutSemantic,
  _In_        DWORD       dwUPartialOutIndex,
  _In_        DWORD       dwVPartialOutSemantic,
  _In_        DWORD       dwVPartialOutIndex,
  _In_        DWORD       dwNormalOutSemantic,
  _In_        DWORD       dwNormalOutIndex,
  _In_        DWORD       dwOptions,
  _In_  const DWORD       *pdwAdjacency,
  _In_        FLOAT       fPartialEdgeThreshold,
  _In_        FLOAT       fSingularPointThreshold,
  _In_        FLOAT       fNormalEdgeThreshold,
  _Out_       ID3DXMesh   **ppMeshOut,
  _Out_       ID3DXBuffer **ppVertexMapping
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMesh* \[ En\]
</dt> <dd>

Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\***

Puntero a un objeto de [**malla ID3DXMesh**](id3dxmesh.md) de entrada.

</dd> <dt>

*dwTextureInSemantic* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica la semántica de entrada de la coordenada de textura. Si D3DX DEFAULT, la función supone que no hay coordenadas de textura y la función producirá un error a menos que se especifique \_ un cálculo de vector normal.

</dd> <dt>

*dwTextureInIndex* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Si una malla tiene varias coordenadas de textura, especifica la coordenada de textura que se usará para los cálculos del marco tangente. Si es cero, la malla solo tiene una coordenada de textura.

</dd> <dt>

*dwUPartialOutSemantic* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica la semántica de salida para el tipo, normalmente D3DDECLUSAGE TANGENT, que describe dónde se almacenará el derivado parcial con respecto a la coordenada de textura \_ U. Si D3DX \_ DEFAULT, este derivado parcial no se almacenará.

</dd> <dt>

*dwUPartialOutIndex* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica el índice semántico en el que se va a almacenar el derivado parcial con respecto a la coordenada de textura U.

</dd> <dt>

*dwVPartialOutSemantic* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica el [**tipo D3DDECLUSAGE,**](./d3ddeclusage.md) normalmente D3DDECLUSAGE BINORMAL, que describe dónde se almacenará el derivado parcial con respecto a la coordenada de textura \_ V. Si D3DX \_ DEFAULT, este derivado parcial no se almacenará.

</dd> <dt>

*dwVPartialOutIndex* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica el índice semántico en el que se va a almacenar el derivado parcial con respecto a la coordenada de textura V.

</dd> <dt>

*dwNormalOutSemantic* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica la semántica normal de salida, normalmente D3DDECLUSAGE NORMAL, que describe dónde se almacenará el vector normal en \_ cada vértice. Si D3DX \_ DEFAULT, este vector normal no se almacenará.

</dd> <dt>

*dwNormalOutIndex* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica el índice semántico en el que se va a almacenar el vector normal en cada vértice.

</dd> <dt>

*dwOptions* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de una o varias marcas [**D3DXTANGENT**](./d3dxtangent.md) que especifican opciones de cálculo de fotogramas tangentes. Si **es NULL,** se especificarán las siguientes opciones:



| Descripción                                                                                              | [**D3DXTANGENT**](./d3dxtangent.md) Valor de marca                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| Pondera la longitud del vector normal por el ángulo, en radianes, subterfundo por los dos bordes que salen del vértice. | & ! ( D3DXTANGENT \_ WEIGHT \_ BY \_ AREA \| D3DXTANGENT \_ WEIGHT EQUAL \_ )                |
| Calcular coordenadas cartesianas ortogonales a partir de coordenadas de textura (u, v). Vea la sección Comentarios.                   | & ! ( D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ U \| D3DXTANGENT \_ ORTHOGONALIZE \_ FROM V \_ ) |
| Las texturas no se encapsulan en las direcciones u o v                                                     | & ! ( D3DXTANGENT \_ WRAP \_ UV )                                                      |
| Se normalizan los derivados parciales con respecto a las coordenadas de textura.                                  | & ! ( D3DXTANGENT \_ NO \_ NORMALIZAR \_ PARCIALES )                                     |
| Los vértices se ordenan en sentido contrario a las agujas del reloj alrededor de cada triángulo.                               | & ! ( D3DXTANGENT \_ WIND \_ CW )                                                      |
| Use vectores normales por vértice ya presentes en la malla de entrada.                                         | & ! ( D3DXTANGENT \_ CALCULATE \_ NORMALS )                                            |



 

Si D3DXTANGENT \_ GENERATE IN PLACE no está \_ \_ establecido, se clona la malla de entrada. Por lo tanto, la malla original debe tener espacio suficiente para almacenar el vector normal calculado y los datos derivados parciales.

</dd> <dt>

*pdwAdjacency* \[ En\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a una matriz de tres DWORD por cara que especifican los tres vecinos de cada cara de la malla. El número de bytes de esta matriz debe ser al menos 3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).

</dd> <dt>

*fPartialEdgeThreshold* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Especifica el coseno máximo del ángulo en el que dos derivados parciales se consideran incompatibles entre sí. Si el producto de punto de la dirección de los dos derivados parciales en triángulos adyacentes es menor o igual que este umbral, se dividirán los vértices compartidos entre estos triángulos.

</dd> <dt>

*fSingularPointThreshold* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Especifica la magnitud máxima de un derivado parcial en el que un vértice se considerará singular. Dado que varios triángulos son incidentes en un punto que tienen fotogramas tangentes cercanos, pero que se cancelan entre sí (por ejemplo, en la parte superior de una esfera), la magnitud del derivado parcial disminuirá. Si la magnitud es menor o igual que este umbral, el vértice se dividirá para cada triángulo que lo contenga.

</dd> <dt>

*fNormalEdgeThreshold* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

De forma similar a fPartialEdgeThreshold, especifica el coseno máximo del ángulo entre dos normales que es un umbral más allá del cual se dividirán los vértices compartidos entre triángulos. Si el producto de puntos de las dos normales es menor que el umbral, los vértices compartidos se dividirán, formando un borde duro entre triángulos vecinos. Si el producto de puntos supera el umbral, los triángulos vecinos tendrán sus normales interpolados.

</dd> <dt>

*ppMeshOut* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\*\***

Dirección de un puntero a un objeto de malla [**ID3DXMesh**](id3dxmesh.md) de salida que recibe los datos de vectores normales, binormales y tangentes calculados.

</dd> <dt>

*ppVertexMapping* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DXBuffer**](id3dxbuffer.md)\*\***

Dirección de un puntero a un objeto de búfer [**ID3DXBuffer de**](id3dxbuffer.md) salida que recibe una asignación de nuevos vértices calculados por este método a los vértices originales. El búfer es una matriz de DWORD, con el tamaño de la matriz definido como el número de vértices en ppMeshOut.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Hay disponible una versión simplificada de esta función [**como D3DXComputeTangentFrame.**](d3dxcomputetangentframe.md)

El vector normal calculado en cada vértice siempre se normaliza para tener longitud de unidad.

La solución más sólida para calcular las coordenadas cartesianas ortogonales es no establecer marcas D3DXTANGENT \_ ORTHOGONALIZE FROM you y \_ \_ D3DXTANGENT \_ ORTHOGONALIZE FROM V, para que las coordenadas \_ \_ ortogonales se calcule a partir de las coordenadas de textura usted y v. Sin embargo, en este caso, si u o v es cero, la función calculará las coordenadas ortogonales mediante D3DXTANGENT \_ ORTHOGONALIZE FROM V o \_ \_ D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ U, respectivamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md)
</dt> </dl>

 

 
