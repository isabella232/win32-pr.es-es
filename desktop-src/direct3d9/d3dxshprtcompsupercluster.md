---
description: 'Función D3DXSHPRTCompSuperCluster: se usa con los resultados comprimidos de la versión de vértice del simulador de transferencia de radiancia (PRT) precalutado.'
ms.assetid: 0ec28b8c-5010-48a4-8e45-d7f9aa08185f
title: Función D3DXSHPRTCompSuperCluster (D3DX9Mesh.h)
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
ms.openlocfilehash: 0c22c8a3a14fd8af3e9104889b421068c7ff1457
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117863"
---
# <a name="d3dxshprtcompsupercluster-function"></a><span data-ttu-id="4ae0b-103">Función D3DXSHPRTCompSuperCluster</span><span class="sxs-lookup"><span data-stu-id="4ae0b-103">D3DXSHPRTCompSuperCluster function</span></span>

<span data-ttu-id="4ae0b-104">Se usa con resultados comprimidos de la versión de vértice del simulador de transferencia de radiancia precalutada (PRT).</span><span class="sxs-lookup"><span data-stu-id="4ae0b-104">Used with compressed results of the vertex version of the precomputed radiance transfer (PRT) simulator.</span></span> <span data-ttu-id="4ae0b-105">Genera "superclústeres", que son grupos de clústeres que se pueden dibujar en la misma llamada a draw.</span><span class="sxs-lookup"><span data-stu-id="4ae0b-105">Generates "superclusters," which are groups of clusters that can be drawn in the same draw call.</span></span> <span data-ttu-id="4ae0b-106">Se usa un algoritmo expansión que minimiza el sobredesgráfico para agrupar los clústeres.</span><span class="sxs-lookup"><span data-stu-id="4ae0b-106">A greedy algorithm that minimizes overdraw is used to group the clusters.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ae0b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ae0b-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="4ae0b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ae0b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ae0b-109">*pClusterIDs* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4ae0b-109">*pClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ae0b-110">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4ae0b-110">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4ae0b-111">Puntero a los IDs de clúster numverts (extraídos de un búfer comprimido).</span><span class="sxs-lookup"><span data-stu-id="4ae0b-111">Pointer to a NumVerts cluster IDs (extracted from a compressed buffer.)</span></span>

</dd> <dt>

<span data-ttu-id="4ae0b-112">*pScene* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4ae0b-112">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ae0b-113">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="4ae0b-113">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="4ae0b-114">Puntero a una malla que representa la escena compuesta pasada al simulador.</span><span class="sxs-lookup"><span data-stu-id="4ae0b-114">Pointer to a mesh that represents composite scene passed to the simulator.</span></span> <span data-ttu-id="4ae0b-115">Vea [**ID3DXMesh.**](id3dxmesh.md)</span><span class="sxs-lookup"><span data-stu-id="4ae0b-115">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ae0b-116">*MaxNumClusters* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4ae0b-116">*MaxNumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ae0b-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ae0b-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4ae0b-118">Número máximo de clústeres asignados por super clúster.</span><span class="sxs-lookup"><span data-stu-id="4ae0b-118">Maximum number of clusters allocated per super cluster.</span></span>

</dd> <dt>

<span data-ttu-id="4ae0b-119">*NumClusters* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4ae0b-119">*NumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ae0b-120">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ae0b-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4ae0b-121">Número de clústeres calculados en el simulador.</span><span class="sxs-lookup"><span data-stu-id="4ae0b-121">Number of clusters computed in the simulator.</span></span>

</dd> <dt>

<span data-ttu-id="4ae0b-122">*pSClusterIDs* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4ae0b-122">*pSClusterIDs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ae0b-123">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4ae0b-123">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4ae0b-124">Puntero a una matriz de *longitud NumClusters.*</span><span class="sxs-lookup"><span data-stu-id="4ae0b-124">Pointer to an array of length *NumClusters*.</span></span> <span data-ttu-id="4ae0b-125">Contiene el índice del superc cluster al que se asignó el clúster correspondiente.</span><span class="sxs-lookup"><span data-stu-id="4ae0b-125">Contains the index of the super cluster to which the corresponding cluster was assigned.</span></span>

</dd> <dt>

<span data-ttu-id="4ae0b-126">*pNumSCs* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4ae0b-126">*pNumSCs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ae0b-127">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4ae0b-127">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4ae0b-128">Número de super clústeres asignados.</span><span class="sxs-lookup"><span data-stu-id="4ae0b-128">Number of super clusters allocated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ae0b-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ae0b-129">Return value</span></span>

<span data-ttu-id="4ae0b-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4ae0b-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4ae0b-131">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4ae0b-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4ae0b-132">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="4ae0b-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ae0b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ae0b-133">Requirements</span></span>



| <span data-ttu-id="4ae0b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ae0b-134">Requirement</span></span> | <span data-ttu-id="4ae0b-135">Value</span><span class="sxs-lookup"><span data-stu-id="4ae0b-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae0b-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ae0b-136">Header</span></span><br/>  | <dl> <span data-ttu-id="4ae0b-137"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="4ae0b-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4ae0b-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4ae0b-138">Library</span></span><br/> | <dl> <span data-ttu-id="4ae0b-139"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ae0b-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4ae0b-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4ae0b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ae0b-141">Funciones de transferencia de radiancia precalcaladas</span><span class="sxs-lookup"><span data-stu-id="4ae0b-141">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
