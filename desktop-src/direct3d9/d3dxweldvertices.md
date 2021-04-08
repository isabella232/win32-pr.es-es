---
description: Soldaduras juntas los vértices replicados que tienen los mismos atributos. Este método usa valores de épsilon especificados para comparaciones de igualdad.
ms.assetid: bddf6e0c-55a1-40d2-8681-e7f0f9002bfa
title: Función D3DXWeldVertices (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWeldVertices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 76e0a6f259bc8ba547a02b2e95cccf718d54e904
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821135"
---
# <a name="d3dxweldvertices-function"></a>D3DXWeldVertices función)

Soldaduras juntas los vértices replicados que tienen los mismos atributos. Este método usa valores de épsilon especificados para comparaciones de igualdad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXWeldVertices(
  _In_          LPD3DXMESH       pMesh,
  _In_          DWORD            Flags,
  _In_    const D3DXWeldEpsilons *pEpsilons,
  _In_    const DWORD            *pAdjacencyIn,
  _Inout_       DWORD            *pAdjacencyOut,
  _Out_         DWORD            *pFaceRemap,
  _Out_         LPD3DXBUFFER     *ppVertexRemap
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pmesh* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a un objeto [**ID3DXMesh**](id3dxmesh.md) , la malla desde la que se van a soldar los vértices.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de una o varias marcas de [**D3DXWELDEPSILONSFLAGS**](./d3dxweldepsilonsflags.md).

</dd> <dt>

*pEpsilons* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXWeldEpsilons**](d3dxweldepsilons.md) \***

Puntero a una estructura [**D3DXWeldEpsilons**](d3dxweldepsilons.md) , que especifica los valores de épsilon que se usarán para este método. Use **null** para inicializar todos los miembros de la estructura con un valor predeterminado de 1,0 e-6F.

</dd> <dt>

*pAdjacencyIn* \[ de\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla de origen. Si el borde no tiene caras adyacentes, el valor es 0xFFFFFFFF. Si este parámetro se establece en **null**, se llamará a [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md) para crear información lógica de proximidad.

</dd> <dt>

*pAdjacencyOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla optimizada. Si el borde no tiene caras adyacentes, el valor es 0xFFFFFFFF.

</dd> <dt>

*pFaceRemap* \[ enuncia\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Matriz de DWORDs, una por cada tipo, que identifica la superficie de la malla original que corresponde a cada una de las caras de la malla soldada.

</dd> <dt>

*ppVertexRemap* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) , que contiene un valor DWORD para cada vértice que especifica cómo se asignan los nuevos vértices a los vértices anteriores. Esta reasignación es útil si necesita modificar los datos externos en función de la nueva asignación de vértices.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Esta función usa la información de adyacencia suministrada para determinar los puntos que se replican. Los vértices se combinan en función de una comparación de épsilon. Los vértices con la misma posición deben haberse calculado y representados mediante datos de representadores de puntos.

Esta función combina vértices con soldadura lógica que tienen componentes similares, como normales o coordenadas de textura dentro de pEpsilons.

En el siguiente código de ejemplo se llama a esta función con la soldadura habilitada. Los vértices se comparan usando valores de épsilon para el vector normal y la posición del vértice. Se devuelve un puntero a una matriz de reasignación de caras (*pFaceRemap*).


```
TCHAR            strMediaPath[512];       // X-file path 
LPD3DXBUFFER     pAdjacencyBuffer = NULL; // adjacency data buffer
LPD3DXBUFFER     pD3DXMtrlBuffer  = NULL; // material buffer
LPD3DXMESH       pMesh            = NULL; // mesh object
DWORD            m_dwNumMaterials;        // number of materials
D3DXWELDEPSILONS Epsilons;                // structure with epsilon values
DWORD            *pFaceRemap[65536];      // face remapping array
DWORD            i;                       // internal variable
    
    // Load the mesh from the specified file
    hr = D3DXLoadMeshFromX ( strMediaPath,
                         D3DXMESH_MANAGED,
                         m_pd3dDevice,
                         &pAdjacencyBuffer,
                         &pD3DXMtrlBuffer,
                         NULL,
                         &m_dwNumMaterials,
                         &pMesh ) )
                             
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
    
    // Set epsilon values
    Epsilons.Normal = 0.001;
    Epsilons.Position = 0.1;
    
    // Weld the vertices
    for( i=0; i < 65536; i++ )
    { 
        pFaceRemap[i] = 0; 
    }
    
    hr = D3DXWeldVertices ( pMesh,
                            D3DXWELDEPSILONS_WELDPARTIALMATCHES,
                            &Epsilons,
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pFaceRemap,
                            NULL )
                            
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
