---
description: Se usa con los resultados comprimidos de la versión de vértice del simulador Radiance Transfer (PRT) precalculado.
ms.assetid: 0ec28b8c-5010-48a4-8e45-d7f9aa08185f
title: Función D3DXSHPRTCompSuperCluster (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSuperCluster
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1daf25dddfaf738ecc2fed9605429a19170177ed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362541"
---
# <a name="d3dxshprtcompsupercluster-function"></a><span data-ttu-id="5aa43-103">D3DXSHPRTCompSuperCluster función)</span><span class="sxs-lookup"><span data-stu-id="5aa43-103">D3DXSHPRTCompSuperCluster function</span></span>

<span data-ttu-id="5aa43-104">Se usa con los resultados comprimidos de la versión de vértice del simulador Radiance Transfer (PRT) precalculado.</span><span class="sxs-lookup"><span data-stu-id="5aa43-104">Used with compressed results of the vertex version of the precomputed radiance transfer (PRT) simulator.</span></span> <span data-ttu-id="5aa43-105">Genera "superclústeres", que son grupos de clústeres que se pueden dibujar en la misma llamada a Draw.</span><span class="sxs-lookup"><span data-stu-id="5aa43-105">Generates "superclusters," which are groups of clusters that can be drawn in the same draw call.</span></span> <span data-ttu-id="5aa43-106">Se usa un algoritmo expansivo que minimiza el desdibujo para agrupar los clústeres.</span><span class="sxs-lookup"><span data-stu-id="5aa43-106">A greedy algorithm that minimizes overdraw is used to group the clusters.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aa43-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5aa43-107">Syntax</span></span>


```C++
HRESULT D3DXSHPRTCompSuperCluster(
  _In_    UINT       *pClusterIDs,
  _In_    LPD3DXMESH pScene,
  _In_    UINT       MaxNumClusters,
  _In_    UINT       NumClusters,
  _Inout_ UINT       *pSClusterIDs,
  _Inout_ UINT       *pNumSCs
);
```



## <a name="parameters"></a><span data-ttu-id="5aa43-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5aa43-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aa43-109">*pClusterIDs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5aa43-109">*pClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aa43-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5aa43-110">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5aa43-111">Puntero a los identificadores de clúster de NumVerts (extraídos de un búfer comprimido).</span><span class="sxs-lookup"><span data-stu-id="5aa43-111">Pointer to a NumVerts cluster IDs (extracted from a compressed buffer.)</span></span>

</dd> <dt>

<span data-ttu-id="5aa43-112">*pScene* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5aa43-112">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aa43-113">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="5aa43-113">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="5aa43-114">Puntero a una malla que representa la escena compuesta pasada al simulador.</span><span class="sxs-lookup"><span data-stu-id="5aa43-114">Pointer to a mesh that represents composite scene passed to the simulator.</span></span> <span data-ttu-id="5aa43-115">Vea [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="5aa43-115">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="5aa43-116">*MaxNumClusters* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5aa43-116">*MaxNumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aa43-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5aa43-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5aa43-118">Número máximo de clústeres asignados por Super cluster.</span><span class="sxs-lookup"><span data-stu-id="5aa43-118">Maximum number of clusters allocated per super cluster.</span></span>

</dd> <dt>

<span data-ttu-id="5aa43-119">*NumClusters* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5aa43-119">*NumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aa43-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5aa43-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5aa43-121">Número de clústeres calculados en el simulador.</span><span class="sxs-lookup"><span data-stu-id="5aa43-121">Number of clusters computed in the simulator.</span></span>

</dd> <dt>

<span data-ttu-id="5aa43-122">*pSClusterIDs* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5aa43-122">*pSClusterIDs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5aa43-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5aa43-123">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5aa43-124">Puntero a una matriz de longitud *NumClusters*.</span><span class="sxs-lookup"><span data-stu-id="5aa43-124">Pointer to an array of length *NumClusters*.</span></span> <span data-ttu-id="5aa43-125">Contiene el índice del clúster Super al que se asignó el clúster correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5aa43-125">Contains the index of the super cluster to which the corresponding cluster was assigned.</span></span>

</dd> <dt>

<span data-ttu-id="5aa43-126">*pNumSCs* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5aa43-126">*pNumSCs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5aa43-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5aa43-127">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5aa43-128">Número de clústeres superpuestos asignados.</span><span class="sxs-lookup"><span data-stu-id="5aa43-128">Number of super clusters allocated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aa43-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5aa43-129">Return value</span></span>

<span data-ttu-id="5aa43-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5aa43-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5aa43-131">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5aa43-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5aa43-132">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="5aa43-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aa43-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5aa43-133">Requirements</span></span>



| <span data-ttu-id="5aa43-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aa43-134">Requirement</span></span> | <span data-ttu-id="5aa43-135">Value</span><span class="sxs-lookup"><span data-stu-id="5aa43-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa43-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5aa43-136">Header</span></span><br/>  | <dl> <span data-ttu-id="5aa43-137"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5aa43-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5aa43-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5aa43-138">Library</span></span><br/> | <dl> <span data-ttu-id="5aa43-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5aa43-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5aa43-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="5aa43-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aa43-141">Funciones de transferencia Radiance precalculadas</span><span class="sxs-lookup"><span data-stu-id="5aa43-141">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
