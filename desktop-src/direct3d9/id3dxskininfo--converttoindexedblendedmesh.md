---
description: Toma una malla y devuelve una nueva malla con pesos de fusión, índices y una tabla de combinación de hueso por vértices. En la tabla se describen las paletas de hueso que afectan a los subconjuntos de la malla.
ms.assetid: e4758a3b-8a45-4ed3-aa62-9713d12afc56
title: 'ID3DXSkinInfo:: ConvertToIndexedBlendedMesh (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToIndexedBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87c8a4b943a647e52d7260f1ff53b32b40756761
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708042"
---
# <a name="id3dxskininfoconverttoindexedblendedmesh-method"></a><span data-ttu-id="795d5-104">ID3DXSkinInfo:: ConvertToIndexedBlendedMesh (método)</span><span class="sxs-lookup"><span data-stu-id="795d5-104">ID3DXSkinInfo::ConvertToIndexedBlendedMesh method</span></span>

<span data-ttu-id="795d5-105">Toma una malla y devuelve una nueva malla con pesos de fusión, índices y una tabla de combinación de hueso por vértices.</span><span class="sxs-lookup"><span data-stu-id="795d5-105">Takes a mesh and returns a new mesh with per-vertex blend weights, indices, and a bone combination table.</span></span> <span data-ttu-id="795d5-106">En la tabla se describen las paletas de hueso que afectan a los subconjuntos de la malla.</span><span class="sxs-lookup"><span data-stu-id="795d5-106">The table describes which bone palettes affect which subsets of the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="795d5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="795d5-107">Syntax</span></span>


```C++
HRESULT ConvertToIndexedBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
  [in]        DWORD        paletteSize,
  [in]  const DWORD        *pAdjacencyIn,
  [in]        LPDWORD      pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap,
  [out]       DWORD        *pMaxVertexInfl,
  [out]       DWORD        *pNumBoneCombinations,
  [out]       LPD3DXBUFFER *ppBoneCombinationTable,
  [out]       LPD3DXMESH   *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="795d5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="795d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="795d5-109">*pmesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="795d5-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="795d5-110">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="795d5-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="795d5-111">La malla de entrada.</span><span class="sxs-lookup"><span data-stu-id="795d5-111">The input mesh.</span></span> <span data-ttu-id="795d5-112">Vea [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="795d5-112">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="795d5-113">*Opciones* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="795d5-113">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="795d5-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="795d5-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="795d5-115">Actualmente no se usa.</span><span class="sxs-lookup"><span data-stu-id="795d5-115">Currently unused.</span></span>

</dd> <dt>

<span data-ttu-id="795d5-116">*paletteSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="795d5-116">*paletteSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="795d5-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="795d5-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="795d5-118">Número de matrices del hueso disponibles para el recubrimiento de la paleta de matrices.</span><span class="sxs-lookup"><span data-stu-id="795d5-118">Number of bone matrices available for matrix palette skinning.</span></span>

</dd> <dt>

<span data-ttu-id="795d5-119">*pAdjacencyIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="795d5-119">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="795d5-120">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="795d5-120">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="795d5-121">Información de proximidad de la malla de entrada.</span><span class="sxs-lookup"><span data-stu-id="795d5-121">Input mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="795d5-122">*pAdjacencyOut* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="795d5-122">*pAdjacencyOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="795d5-123">Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="795d5-123">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="795d5-124">Información de proximidad de la malla de salida.</span><span class="sxs-lookup"><span data-stu-id="795d5-124">Output mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="795d5-125">*pFaceRemap* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="795d5-125">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="795d5-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="795d5-126">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="795d5-127">Matriz de DWORDs, una por cada tipo, que identifica la superficie de la malla original que corresponde a cada una de las caras de la malla combinada.</span><span class="sxs-lookup"><span data-stu-id="795d5-127">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the blended mesh.</span></span> <span data-ttu-id="795d5-128">Si el valor proporcionado para este argumento es **null**, no se devuelven los datos de reasignación de caras.</span><span class="sxs-lookup"><span data-stu-id="795d5-128">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="795d5-129">*ppVertexRemap* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="795d5-129">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="795d5-130">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="795d5-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="795d5-131">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) , que contiene un valor DWORD para cada vértice que especifica cómo se asignan los nuevos vértices a los vértices anteriores.</span><span class="sxs-lookup"><span data-stu-id="795d5-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="795d5-132">Esta reasignación es útil si necesita modificar los datos externos en función de la nueva asignación de vértices.</span><span class="sxs-lookup"><span data-stu-id="795d5-132">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span> <span data-ttu-id="795d5-133">Este parámetro es opcional; Se puede utilizar **null** .</span><span class="sxs-lookup"><span data-stu-id="795d5-133">This parameter is optional; **NULL** may be used.</span></span>

</dd> <dt>

<span data-ttu-id="795d5-134">*pMaxVertexInfl* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="795d5-134">*pMaxVertexInfl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="795d5-135">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="795d5-135">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="795d5-136">Puntero a un valor DWORD que contendrá el número máximo de influencias del hueso necesarias por vértice para este método de la piel.</span><span class="sxs-lookup"><span data-stu-id="795d5-136">Pointer to a DWORD that will contain the maximum number of bone influences required per vertex for this skinning method.</span></span>

</dd> <dt>

<span data-ttu-id="795d5-137">*pNumBoneCombinations* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="795d5-137">*pNumBoneCombinations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="795d5-138">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="795d5-138">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="795d5-139">Puntero al número de huesos en la tabla de combinación de hueso.</span><span class="sxs-lookup"><span data-stu-id="795d5-139">Pointer to the number of bones in the bone combination table.</span></span>

</dd> <dt>

<span data-ttu-id="795d5-140">*ppBoneCombinationTable* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="795d5-140">*ppBoneCombinationTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="795d5-141">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="795d5-141">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="795d5-142">Puntero a la tabla de combinación de hueso.</span><span class="sxs-lookup"><span data-stu-id="795d5-142">Pointer to the bone combination table.</span></span> <span data-ttu-id="795d5-143">Los datos se organizan en una estructura [**D3DXBONECOMBINATION**](d3dxbonecombination.md) .</span><span class="sxs-lookup"><span data-stu-id="795d5-143">The data is organized in a [**D3DXBONECOMBINATION**](d3dxbonecombination.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="795d5-144">*ppMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="795d5-144">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="795d5-145">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="795d5-145">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="795d5-146">Puntero a la nueva malla.</span><span class="sxs-lookup"><span data-stu-id="795d5-146">Pointer to the new mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="795d5-147">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="795d5-147">Return value</span></span>

<span data-ttu-id="795d5-148">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="795d5-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="795d5-149">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="795d5-149">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="795d5-150">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="795d5-150">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="795d5-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="795d5-151">Remarks</span></span>

<span data-ttu-id="795d5-152">Cada elemento de las matrices de reasignación especifica el índice anterior para esa posición.</span><span class="sxs-lookup"><span data-stu-id="795d5-152">Each element in the remap arrays specifies the previous index for that position.</span></span> <span data-ttu-id="795d5-153">Por ejemplo, si un vértice estaba en la posición 3 pero se ha reasignado a la posición 5, el quinto elemento de pVertexRemap contendrá 3.</span><span class="sxs-lookup"><span data-stu-id="795d5-153">For example, if a vertex was in position 3 but has been remapped to position 5, then the fifth element of pVertexRemap will contain 3.</span></span>

<span data-ttu-id="795d5-154">Este método no se ejecuta en hardware que no admite la combinación de vértices de funciones fijas.</span><span class="sxs-lookup"><span data-stu-id="795d5-154">This method does not run on hardware that does not support fixed-function vertex blending.</span></span>

## <a name="requirements"></a><span data-ttu-id="795d5-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="795d5-155">Requirements</span></span>



| <span data-ttu-id="795d5-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="795d5-156">Requirement</span></span> | <span data-ttu-id="795d5-157">Value</span><span class="sxs-lookup"><span data-stu-id="795d5-157">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="795d5-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="795d5-158">Header</span></span><br/>  | <dl> <span data-ttu-id="795d5-159"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="795d5-159"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="795d5-160">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="795d5-160">Library</span></span><br/> | <dl> <span data-ttu-id="795d5-161"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="795d5-161"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="795d5-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="795d5-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="795d5-163">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="795d5-163">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
