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
# <a name="id3dx10skininfodosoftwareskinning-method"></a><span data-ttu-id="1182e-103">ID3DX10SkinInfo::D método oSoftwareSkinning</span><span class="sxs-lookup"><span data-stu-id="1182e-103">ID3DX10SkinInfo::DoSoftwareSkinning method</span></span>

<span data-ttu-id="1182e-104">Realice la piel de software en una matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="1182e-104">Do software skinning on an array of vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="1182e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1182e-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="1182e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1182e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1182e-107">*StartVertex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1182e-107">*StartVertex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1182e-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1182e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1182e-109">Índice de base cero en pSrcVertices.</span><span class="sxs-lookup"><span data-stu-id="1182e-109">A 0-based index into pSrcVertices.</span></span>

</dd> <dt>

<span data-ttu-id="1182e-110">*VertexCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1182e-110">*VertexCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1182e-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1182e-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1182e-112">Número de vértices que se van a transformar.</span><span class="sxs-lookup"><span data-stu-id="1182e-112">Number of vertices to transform.</span></span>

</dd> <dt>

<span data-ttu-id="1182e-113">*pSrcVertices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1182e-113">*pSrcVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1182e-114">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="1182e-114">Type: **void\***</span></span>

<span data-ttu-id="1182e-115">Puntero a una matriz de vértices que se van a transformar.</span><span class="sxs-lookup"><span data-stu-id="1182e-115">Pointer to an array of vertices to transform.</span></span>

</dd> <dt>

<span data-ttu-id="1182e-116">*SrcStride* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1182e-116">*SrcStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1182e-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1182e-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1182e-118">Tamaño, en bytes, de un vértice en pSrcVertices.</span><span class="sxs-lookup"><span data-stu-id="1182e-118">The size, in bytes, of a vertex in pSrcVertices.</span></span>

</dd> <dt>

<span data-ttu-id="1182e-119">*pDestVertices* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1182e-119">*pDestVertices* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1182e-120">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="1182e-120">Type: **void\***</span></span>

<span data-ttu-id="1182e-121">Puntero a una matriz de vértices, que se rellenará con los vértices transformados.</span><span class="sxs-lookup"><span data-stu-id="1182e-121">Pointer to an array of vertices, which will be filled with the transformed vertices.</span></span>

</dd> <dt>

<span data-ttu-id="1182e-122">*DestStride* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1182e-122">*DestStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1182e-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1182e-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1182e-124">Tamaño, en bytes, de un vértice en pDestVertices.</span><span class="sxs-lookup"><span data-stu-id="1182e-124">The size, in bytes, of a vertex in pDestVertices.</span></span>

</dd> <dt>

<span data-ttu-id="1182e-125">*pBoneMatrices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1182e-125">*pBoneMatrices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1182e-126">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1182e-126">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1182e-127">Matriz de matrices que se usará para transformar los puntos asignados a cada hueso, de modo que los vértices asignados al hueso se \[ \] transformarán por pBoneMatrices \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="1182e-127">An array of matrices that will be used to transform the points mapped to each bone, such that the vertices mapped to bone\[i\] will be transformed by pBoneMatrices\[i\].</span></span> <span data-ttu-id="1182e-128">Esta matriz se usará para transformar las matrices solo si el valor Isnormal (de pChannelDescs se establece en **false**; de lo contrario, se usará pInverseTransposeBoneMatrices.</span><span class="sxs-lookup"><span data-stu-id="1182e-128">This array will be used to transform the matrices only if the IsNormal value in pChannelDescs is set to **FALSE**, otherwise pInverseTransposeBoneMatrices will be used.</span></span>

</dd> <dt>

<span data-ttu-id="1182e-129">*pInverseTransposeBoneMatrices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1182e-129">*pInverseTransposeBoneMatrices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1182e-130">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1182e-130">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1182e-131">Si este valor es **null**, se establecerá en pBoneMatrices.</span><span class="sxs-lookup"><span data-stu-id="1182e-131">If this value is **NULL**, it will be set equal to pBoneMatrices.</span></span> <span data-ttu-id="1182e-132">Esta matriz de matrices se usará para transformar los vértices solo si el valor Isnormal (de pChannelDescs se establece en **true**; de lo contrario, se usará pBoneMatrices.</span><span class="sxs-lookup"><span data-stu-id="1182e-132">This array of matrices will be used to transform the vertices only if the IsNormal value in pChannelDescs is set to **TRUE**, otherwise pBoneMatrices will be used.</span></span>

</dd> <dt>

<span data-ttu-id="1182e-133">*pChannelDescs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1182e-133">*pChannelDescs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1182e-134">Tipo: **[ **\_ \_ canal de D3DX10** de la piel](d3dx10-skinning-channel.md)\***</span><span class="sxs-lookup"><span data-stu-id="1182e-134">Type: **[**D3DX10\_SKINNING\_CHANNEL**](d3dx10-skinning-channel.md)\***</span></span>

<span data-ttu-id="1182e-135">Puntero a una estructura de canal de D3DX10 de la \_ piel \_ , que determina el miembro del vértice decl en el que se realizará la piel del software.</span><span class="sxs-lookup"><span data-stu-id="1182e-135">Pointer to a D3DX10\_SKINNING\_CHANNEL structure, which determines the member of the vertex decl the software skinning will be done on.</span></span>

</dd> <dt>

<span data-ttu-id="1182e-136">*NumChannels* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1182e-136">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1182e-137">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1182e-137">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1182e-138">El número de estructuras de canal de D3DX10 \_ \_ en pChannelDescs.</span><span class="sxs-lookup"><span data-stu-id="1182e-138">The number of D3DX10\_SKINNING\_CHANNEL structures in pChannelDescs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1182e-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1182e-139">Return value</span></span>

<span data-ttu-id="1182e-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1182e-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1182e-141">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1182e-141">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1182e-142">Si se produce un error en el método, el valor devuelto puede ser: E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="1182e-142">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="remarks"></a><span data-ttu-id="1182e-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1182e-143">Remarks</span></span>

<span data-ttu-id="1182e-144">A continuación se muestra un ejemplo de cómo usar la piel de software:</span><span class="sxs-lookup"><span data-stu-id="1182e-144">Here is an example of how to use software skinning:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="1182e-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1182e-145">Requirements</span></span>



| <span data-ttu-id="1182e-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="1182e-146">Requirement</span></span> | <span data-ttu-id="1182e-147">Value</span><span class="sxs-lookup"><span data-stu-id="1182e-147">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1182e-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1182e-148">Header</span></span><br/>  | <dl> <span data-ttu-id="1182e-149"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1182e-149"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1182e-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1182e-150">Library</span></span><br/> | <dl> <span data-ttu-id="1182e-151"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1182e-151"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1182e-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="1182e-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1182e-153">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="1182e-153">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="1182e-154">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="1182e-154">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
