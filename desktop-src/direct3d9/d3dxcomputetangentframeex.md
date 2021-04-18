---
description: Realiza cálculos de fotogramas tangentes en una malla. Se generan vectores de tangente, binormalización y, opcionalmente, normales. Las singularidades se controlan según sea necesario mediante la agrupación de los bordes y la división de los vértices.
ms.assetid: 15cc46bc-6db6-4e1d-a95e-cd60d2666600
title: Función D3DXComputeTangentFrameEx (D3DX9Mesh. h)
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
ms.openlocfilehash: 58c7e8a1f1f7247d6a3ecc92d5771d68c9c3e5a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717639"
---
# <a name="d3dxcomputetangentframeex-function"></a>D3DXComputeTangentFrameEx función)

Realiza cálculos de fotogramas tangentes en una malla. Se generan vectores de tangente, binormalización y, opcionalmente, normales. Las singularidades se controlan según sea necesario mediante la agrupación de los bordes y la división de los vértices.

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

*pmesh* \[ de\]
</dt> <dd>

Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\***

Puntero a un objeto de malla [**ID3DXMesh**](id3dxmesh.md) de entrada.

</dd> <dt>

*dwTextureInSemantic* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica la semántica de entrada de coordenadas de textura. Si \_ el valor predeterminado de D3DX es, la función supone que no hay ninguna coordenadas de textura y se producirá un error en la función a menos que se especifique el cálculo del vector normal.

</dd> <dt>

*dwTextureInIndex* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Si una malla tiene varias coordenadas de textura, especifica la coordenada de textura que se va a usar para los cálculos de fotogramas tangentes. Si el valor es cero, la malla solo tiene una coordenada de textura.

</dd> <dt>

*dwUPartialOutSemantic* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica la semántica de salida para el tipo, normalmente D3DDECLUSAGE \_ tangente, que describe dónde se almacenará el derivado parcial con respecto a la coordenada de textura U. Si \_ el valor predeterminado de D3DX es, este derivado parcial no se almacenará.

</dd> <dt>

*dwUPartialOutIndex* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica el índice semántico en el que se almacena el derivado parcial con respecto a la coordenada de textura U.

</dd> <dt>

*dwVPartialOutSemantic* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica el tipo [**D3DDECLUSAGE**](./d3ddeclusage.md) , normalmente D3DDECLUSAGE \_ binormal, que describe dónde se almacenará el derivado parcial con respecto a la coordenada de textura V. Si \_ el valor predeterminado de D3DX es, este derivado parcial no se almacenará.

</dd> <dt>

*dwVPartialOutIndex* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica el índice semántico en el que se almacena el derivado parcial con respecto a la coordenada de textura V.

</dd> <dt>

*dwNormalOutSemantic* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica la semántica normal de salida, normalmente D3DDECLUSAGE \_ normal, que describe dónde se almacenará el vector normal en cada vértice. Si \_ el valor predeterminado de D3DX es, este vector normal no se almacenará.

</dd> <dt>

*dwNormalOutIndex* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica el índice semántico en el que se va a almacenar el vector normal en cada vértice.

</dd> <dt>

*dwOptions* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de una o varias marcas [**D3DXTANGENT**](./d3dxtangent.md) que especifican las opciones de cálculo de fotogramas tangentes. Si **es null**, se especificarán las siguientes opciones:



| Descripción                                                                                              | [**D3DXTANGENT**](./d3dxtangent.md) Valor de marca                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| Pondera la longitud del vector normal por el ángulo, en radianes, que se repite en los dos bordes que abandonan el vértice. | &. (D3DXTANGENT \_ PESO \_ por \_ área \| D3DXTANGENT \_ peso \_ igual)                |
| Calcular coordenadas cartesianas ortogonales a partir de coordenadas de textura (u, v). Vea la sección Comentarios.                   | &. (D3DXTANGENT \_ ORTOGONAL \_ desde \_ U \| D3DXTANGENT \_ ortogonal \_ desde \_ V) |
| Las texturas no se ajustan en las direcciones u o v                                                     | &. (D3DXTANGENT \_ ENCAPSULAdo \_ UV)                                                      |
| Se normalizan las derivadas parciales con respecto a las coordenadas de textura.                                  | &. (D3DXTANGENT \_ no \_ normalizar \_ parciales)                                     |
| Los vértices se ordenan en sentido contrario a las agujas del reloj alrededor de cada triángulo.                               | &. (D3DXTANGENT \_ VIENTO \_ CW)                                                      |
| Use vectores normales por vértice ya presentes en la malla de entrada.                                         | &. (D3DXTANGENT \_ CALCULAR \_ normales)                                            |



 

Si \_ \_ \_ no se establece D3DXTANGENT generar en contexto, la malla de entrada se clona. Por lo tanto, la malla original debe tener espacio suficiente para almacenar el vector normal calculado y los datos derivados parciales.

</dd> <dt>

*pdwAdjacency* \[ de\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla. El número de bytes de esta matriz debe ser de al menos 3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).

</dd> <dt>

*fPartialEdgeThreshold* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Especifica el coseno máximo del ángulo en el que dos derivados parciales se consideran incompatibles entre sí. Si el producto de punto de la dirección de los dos derivados parciales de triángulos adyacentes es menor o igual que este umbral, los vértices compartidos entre estos triángulos se dividirán.

</dd> <dt>

*fSingularPointThreshold* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Especifica la magnitud máxima de un derivado parcial en el que un vértice se considerará singular. Dado que varios triángulos son incidentes en un punto que tiene fotogramas tangentes cercanos, pero que se cancelan entre sí (por ejemplo, en la parte superior de una esfera), la magnitud del derivado parcial disminuirá. Si la magnitud es menor o igual que este umbral, el vértice se dividirá para cada triángulo que lo contenga.

</dd> <dt>

*fNormalEdgeThreshold* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Similar a fPartialEdgeThreshold, especifica el coseno máximo del ángulo entre dos normales que es un umbral más allá del cual se dividirán los vértices compartidos entre triángulos. Si el producto de punto de las dos normales es inferior al umbral, se dividirán los vértices compartidos, formando un borde duro entre los triángulos vecinos. Si el producto de punto es mayor que el umbral, se interpolarán sus normales triángulos adyacentes.

</dd> <dt>

*ppMeshOut* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\*\***

Dirección de un puntero a un objeto de malla [**ID3DXMesh**](id3dxmesh.md) de salida que recibe los datos de vector de la tangente calculada, binormalización y normal.

</dd> <dt>

*ppVertexMapping* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3DXBuffer**](id3dxbuffer.md)\*\***

Dirección de un puntero a un objeto de búfer de [**ID3DXBuffer**](id3dxbuffer.md) de salida que recibe una asignación de los nuevos vértices calculados por este método para los vértices originales. El búfer es una matriz de DWORDs, con el tamaño de la matriz definido como el número de vértices en ppMeshOut.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Una versión simplificada de esta función está disponible como [**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md).

El vector normal calculado en cada vértice siempre se normaliza para tener una longitud de unidad.

La solución más sólida para calcular coordenadas cartesianos ortogonales consiste en no establecer marcas D3DXTANGENT \_ ortogonales \_ desde el \_ usuario y D3DXTANGENT \_ ortogonal \_ desde \_ V, de modo que las coordenadas ortogonales se calculan a partir de las coordenadas de textura que usted y V. Sin embargo, en este caso, si u o v es cero, la función calculará las coordenadas ortogonales mediante D3DXTANGENT \_ ortogonal \_ desde \_ v o D3DXTANGENT se \_ ortogonala \_ desde \_ u, respectivamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md)
</dt> </dl>

 

 
