---
description: Realice la piel de software en una matriz de vértices.
ms.assetid: 6c1a713f-4ae7-4ee2-afa6-079dd8354fe7
title: ID3DX10SkinInfo::D método oSoftwareSkinning (D3DX10. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698264"
---
# <a name="id3dx10skininfodosoftwareskinning-method"></a>ID3DX10SkinInfo::D método oSoftwareSkinning

Realice la piel de software en una matriz de vértices.

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

*StartVertex* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice de base cero en pSrcVertices.

</dd> <dt>

*VertexCount* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de vértices que se van a transformar.

</dd> <dt>

*pSrcVertices* \[ de\]
</dt> <dd>

Tipo: **void \***

Puntero a una matriz de vértices que se van a transformar.

</dd> <dt>

*SrcStride* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Tamaño, en bytes, de un vértice en pSrcVertices.

</dd> <dt>

*pDestVertices* \[ in, out\]
</dt> <dd>

Tipo: **void \***

Puntero a una matriz de vértices, que se rellenará con los vértices transformados.

</dd> <dt>

*DestStride* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Tamaño, en bytes, de un vértice en pDestVertices.

</dd> <dt>

*pBoneMatrices* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Matriz de matrices que se usará para transformar los puntos asignados a cada hueso, de modo que los vértices asignados al hueso se \[ \] transformarán por pBoneMatrices \[ i \] . Esta matriz se usará para transformar las matrices solo si el valor Isnormal (de pChannelDescs se establece en **false**; de lo contrario, se usará pInverseTransposeBoneMatrices.

</dd> <dt>

*pInverseTransposeBoneMatrices* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Si este valor es **null**, se establecerá en pBoneMatrices. Esta matriz de matrices se usará para transformar los vértices solo si el valor Isnormal (de pChannelDescs se establece en **true**; de lo contrario, se usará pBoneMatrices.

</dd> <dt>

*pChannelDescs* \[ de\]
</dt> <dd>

Tipo: **[ **\_ \_ canal de D3DX10** de la piel](d3dx10-skinning-channel.md)\***

Puntero a una estructura de canal de D3DX10 de la \_ piel \_ , que determina el miembro del vértice decl en el que se realizará la piel del software.

</dd> <dt>

*NumChannels* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

El número de estructuras de canal de D3DX10 \_ \_ en pChannelDescs.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser: E \_ INVALIDARG.

## <a name="remarks"></a>Observaciones

A continuación se muestra un ejemplo de cómo usar la piel de software:


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
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
