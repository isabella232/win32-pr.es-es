---
description: Realice el desnasado de software en una matriz de vértices.
ms.assetid: 6c1a713f-4ae7-4ee2-afa6-079dd8354fe7
title: Método ID3DX10SkinInfo::D oSoftwareSkinning (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.DoSoftwareSkinning
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 54dfe909e36be0273e0679a824ff0674b0e3b38c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888772"
---
# <a name="id3dx10skininfodosoftwareskinning-method"></a>Método ID3DX10SkinInfo::D oSoftwareSkinning

Realice el desnasado de software en una matriz de vértices.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DoSoftwareSkinning(
  [in]      UINT                    StartVertex,
  [in]      UINT                    VertexCount,
  [in]      void                    *pSrcVertices,
  [in]      UINT                    SrcStride,
  [in, out] void                    *pDestVertices,
  [in]      UINT                    DestStride,
  [in]      D3DXMATRIX              *pBoneMatrices,
  [in]      D3DXMATRIX              *pInverseTransposeBoneMatrices,
  [in]      D3DX10_SKINNING_CHANNEL *pChannelDescs,
  [in]      UINT                    NumChannels
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StartVertex* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice basado en 0 en pSrcVertices.

</dd> <dt>

*VertexCount* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de vértices que se transformarán.

</dd> <dt>

*pSrcVertices* \[ En\]
</dt> <dd>

Tipo: **\* void**

Puntero a una matriz de vértices que se transformarán.

</dd> <dt>

*SrcStride* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Tamaño, en bytes, de un vértice en pSrcVertices.

</dd> <dt>

*pDestVertices* \[ in, out\]
</dt> <dd>

Tipo: **\* void**

Puntero a una matriz de vértices, que se rellenarán con los vértices transformados.

</dd> <dt>

*DestStride* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Tamaño, en bytes, de un vértice en pDestVertices.

</dd> <dt>

*pIqueMatrices* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Matriz de matrices que se usará para transformar los puntos asignados a cada ternón, de tal forma que los vértices asignados a la matriz i se transformarán \[ \] mediante pMutMmatrizs \[ i \] . Esta matriz se usará para transformar las matrices solo si el valor IsNormal de pChannelDescs está establecido en **FALSE;** de lo contrario, se usará pInverseTransposeDivers.

</dd> <dt>

*pInverseTransposeDivmatrices* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Si este valor es **NULL,** se establecerá igual a pIonalMatrices. Esta matriz de matrices se usará para transformar los vértices solo si el valor IsNormal de pChannelDescs está establecido en **TRUE;** de lo contrario, se usará pMutmatrices.

</dd> <dt>

*pChannelDescs* \[ En\]
</dt> <dd>

Tipo: **[ **CANAL DE \_ SKINNING \_ D3DX10**](d3dx10-skinning-channel.md)\***

Puntero a una estructura D3DX10 SKINNING CHANNEL, que determina el miembro del vértice en el que se desclá la aplicación de \_ \_ software.

</dd> <dt>

*NumChannels* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de estructuras de canal de SKINNING de D3DX10 \_ \_ en pChannelDescs.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser: E \_ INVALIDARG.

## <a name="remarks"></a>Observaciones

Este es un ejemplo de cómo usar el desnasado de software:


```
//vertex definition
struct MyVertex
{
    D3DXVECTOR3 Position;
    D3DXVECTOR2 Weight;
    D3DXVECTOR2 TexCoord;
};

//create vertex data
const UINT numVertices = 16;
MyVertex vertices[numVertices] = {...};
MyVertex destVertices[numVertices];

//create bone matrices
D3DXMATRIX boneMatrices[2];
D3DXMatrixIdentity(&boneMatrices[0]);
D3DXMatrixRotationX(&boneMatrices[1], 3.14159f / 180.0f);

//create bone indices and weights
UINT boneIndices[numVertices] = {...};
float boneWeights[2][numVertices] = {...};

//create skin info, populate it with bones and vertices, and then map them to each other
ID3DX10SkinInfo *pSkinInfo = NULL;
D3DX10CreateSkinInfo(&pSkinInfo);
pSkinInfo->AddBones(2);
pSkinInfo->AddVertices(numVertices);
pSkinInfo->AddBoneInfluences(0, numVertices, boneIndices, boneWeights[0]);
pSkinInfo->AddBoneInfluences(1, numVertices, boneIndices, boneWeights[1]);

//create channel desc
D3DX10_SKINNING_CHANNEL channelDesc;
channelDesc.SrcOffset = 0;
channelDesc.DestOffset = 0;
channelDesc.IsNormal = FALSE;

//do the skinning
pSkinInfo->DoSoftwareSkinning(0, numVertices,
                              vertices, sizeof(MyVertex), 
                              destVertices, sizeof(MyVertex), 
                              boneMatrices, NULL, 
                              &channelDesc, 1);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
