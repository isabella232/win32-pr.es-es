---
description: Toma una malla y devuelve una nueva malla con pesos de mezcla por vértice y una tabla de combinación de hueso. En la tabla se describen los huesos que afectan a los subconjuntos de la malla.
ms.assetid: c26a9e84-5731-4394-a047-5f1ffe7688d9
title: 'ID3DXSkinInfo:: ConvertToBlendedMesh (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 051c51291416dd7e190c83433a9bf84baeb92957
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718478"
---
# <a name="id3dxskininfoconverttoblendedmesh-method"></a><span data-ttu-id="e755d-104">ID3DXSkinInfo:: ConvertToBlendedMesh (método)</span><span class="sxs-lookup"><span data-stu-id="e755d-104">ID3DXSkinInfo::ConvertToBlendedMesh method</span></span>

<span data-ttu-id="e755d-105">Toma una malla y devuelve una nueva malla con pesos de mezcla por vértice y una tabla de combinación de hueso.</span><span class="sxs-lookup"><span data-stu-id="e755d-105">Takes a mesh and returns a new mesh with per-vertex blend weights and a bone combination table.</span></span> <span data-ttu-id="e755d-106">En la tabla se describen los huesos que afectan a los subconjuntos de la malla.</span><span class="sxs-lookup"><span data-stu-id="e755d-106">The table describes which bones affect which subsets of the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="e755d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e755d-107">Syntax</span></span>


```C++
HRESULT ConvertToBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
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



## <a name="parameters"></a><span data-ttu-id="e755d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e755d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e755d-109">*pmesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e755d-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e755d-110">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="e755d-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="e755d-111">Malla de entrada.</span><span class="sxs-lookup"><span data-stu-id="e755d-111">Input mesh.</span></span> <span data-ttu-id="e755d-112">Vea [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="e755d-112">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="e755d-113">*Opciones* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e755d-113">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e755d-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e755d-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e755d-115">Actualmente no se usa.</span><span class="sxs-lookup"><span data-stu-id="e755d-115">Currently unused.</span></span>

</dd> <dt>

<span data-ttu-id="e755d-116">*pAdjacencyIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e755d-116">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e755d-117">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e755d-117">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e755d-118">Información de proximidad de la malla de entrada.</span><span class="sxs-lookup"><span data-stu-id="e755d-118">Input mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="e755d-119">*pAdjacencyOut* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e755d-119">*pAdjacencyOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e755d-120">Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e755d-120">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e755d-121">Información de proximidad de la malla de salida.</span><span class="sxs-lookup"><span data-stu-id="e755d-121">Output mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="e755d-122">*pFaceRemap* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e755d-122">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e755d-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e755d-123">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e755d-124">Matriz de DWORDs, una por cada tipo, que identifica la superficie de la malla original que corresponde a cada una de las caras de la malla combinada.</span><span class="sxs-lookup"><span data-stu-id="e755d-124">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the blended mesh.</span></span> <span data-ttu-id="e755d-125">Si el valor proporcionado para este argumento es **null**, no se devuelven los datos de reasignación de caras.</span><span class="sxs-lookup"><span data-stu-id="e755d-125">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="e755d-126">*ppVertexRemap* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e755d-126">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e755d-127">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e755d-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e755d-128">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) , que contiene un valor DWORD para cada vértice que especifica cómo se asignan los nuevos vértices a los vértices anteriores.</span><span class="sxs-lookup"><span data-stu-id="e755d-128">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="e755d-129">Esta reasignación es útil si necesita modificar los datos externos en función de la nueva asignación de vértices.</span><span class="sxs-lookup"><span data-stu-id="e755d-129">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span> <span data-ttu-id="e755d-130">Este parámetro es opcional; Se puede utilizar **null** .</span><span class="sxs-lookup"><span data-stu-id="e755d-130">This parameter is optional; **NULL** may be used.</span></span>

</dd> <dt>

<span data-ttu-id="e755d-131">*pMaxVertexInfl* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e755d-131">*pMaxVertexInfl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e755d-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e755d-132">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e755d-133">Puntero a un valor DWORD que contendrá el número máximo de influencias del hueso necesarias por vértice para este método de la piel.</span><span class="sxs-lookup"><span data-stu-id="e755d-133">Pointer to a DWORD that will contain the maximum number of bone influences required per vertex for this skinning method.</span></span>

</dd> <dt>

<span data-ttu-id="e755d-134">*pNumBoneCombinations* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e755d-134">*pNumBoneCombinations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e755d-135">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e755d-135">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e755d-136">Puntero al número de huesos en la tabla de combinación de hueso.</span><span class="sxs-lookup"><span data-stu-id="e755d-136">Pointer to the number of bones in the bone combination table.</span></span>

</dd> <dt>

<span data-ttu-id="e755d-137">*ppBoneCombinationTable* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e755d-137">*ppBoneCombinationTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e755d-138">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e755d-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e755d-139">Puntero a la tabla de combinación de hueso.</span><span class="sxs-lookup"><span data-stu-id="e755d-139">Pointer to the bone combination table.</span></span> <span data-ttu-id="e755d-140">Los datos se organizan en una estructura [**D3DXBONECOMBINATION**](d3dxbonecombination.md) .</span><span class="sxs-lookup"><span data-stu-id="e755d-140">The data is organized in a [**D3DXBONECOMBINATION**](d3dxbonecombination.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e755d-141">*ppMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e755d-141">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e755d-142">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="e755d-142">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="e755d-143">Puntero a la nueva malla.</span><span class="sxs-lookup"><span data-stu-id="e755d-143">Pointer to the new mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e755d-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e755d-144">Return value</span></span>

<span data-ttu-id="e755d-145">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e755d-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e755d-146">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e755d-146">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e755d-147">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e755d-147">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e755d-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e755d-148">Remarks</span></span>

<span data-ttu-id="e755d-149">Cada elemento de la matriz de reasignación especifica el índice anterior para esa posición.</span><span class="sxs-lookup"><span data-stu-id="e755d-149">Each element in the remap array specifies the previous index for that position.</span></span> <span data-ttu-id="e755d-150">Por ejemplo, si un vértice estaba en la posición 3 pero se ha reasignado a la posición 5, el quinto elemento de pVertexRemap contendrá 3.</span><span class="sxs-lookup"><span data-stu-id="e755d-150">For example, if a vertex was in position 3 but has been remapped to position 5, then the fifth element of pVertexRemap will contain 3.</span></span>

<span data-ttu-id="e755d-151">Este método no se ejecuta en hardware que no admite la combinación de vértices de funciones fijas.</span><span class="sxs-lookup"><span data-stu-id="e755d-151">This method does not run on hardware that does not support fixed-function vertex blending.</span></span>

## <a name="requirements"></a><span data-ttu-id="e755d-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e755d-152">Requirements</span></span>



| <span data-ttu-id="e755d-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="e755d-153">Requirement</span></span> | <span data-ttu-id="e755d-154">Value</span><span class="sxs-lookup"><span data-stu-id="e755d-154">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e755d-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e755d-155">Header</span></span><br/>  | <dl> <span data-ttu-id="e755d-156"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e755d-156"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e755d-157">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e755d-157">Library</span></span><br/> | <dl> <span data-ttu-id="e755d-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e755d-158"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e755d-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="e755d-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e755d-160">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="e755d-160">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
