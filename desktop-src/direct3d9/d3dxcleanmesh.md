---
description: Limpia una malla y la prepara para simplificarla.
ms.assetid: 2b586ecc-db87-4b20-a4fc-c8b547bebf65
title: Función D3DXCleanMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCleanMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5565978dc1ad0e80c33718275ea65080930ce7cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649423"
---
# <a name="d3dxcleanmesh-function"></a><span data-ttu-id="58443-103">D3DXCleanMesh función)</span><span class="sxs-lookup"><span data-stu-id="58443-103">D3DXCleanMesh function</span></span>

<span data-ttu-id="58443-104">Limpia una malla y la prepara para simplificarla.</span><span class="sxs-lookup"><span data-stu-id="58443-104">Cleans a mesh, preparing it for simplification.</span></span>

## <a name="syntax"></a><span data-ttu-id="58443-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58443-105">Syntax</span></span>


```C++
HRESULT D3DXCleanMesh(
  _In_        D3DXCLEANTYPE CleanType,
  _In_        LPD3DXMESH    pMeshIn,
  _In_  const DWORD         *pAdjacencyIn,
  _Out_       LPD3DXMESH    *ppMeshOut,
  _Out_       DWORD         *pAdjacencyOut,
  _Out_       LPD3DXBUFFER  *ppErrorsAndWarnings
);
```



## <a name="parameters"></a><span data-ttu-id="58443-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58443-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58443-107">*CleanType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="58443-107">*CleanType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58443-108">Tipo: **[ **D3DXCLEANTYPE**](./d3dxcleantype.md)**</span><span class="sxs-lookup"><span data-stu-id="58443-108">Type: **[**D3DXCLEANTYPE**](./d3dxcleantype.md)**</span></span>

<span data-ttu-id="58443-109">Operaciones de vértices que se deben realizar como preparación para la limpieza de malla.</span><span class="sxs-lookup"><span data-stu-id="58443-109">Vertex operations to perform in preparation for mesh cleaning.</span></span> <span data-ttu-id="58443-110">Vea [**D3DXCLEANTYPE**](./d3dxcleantype.md).</span><span class="sxs-lookup"><span data-stu-id="58443-110">See [**D3DXCLEANTYPE**](./d3dxcleantype.md).</span></span>

</dd> <dt>

<span data-ttu-id="58443-111">*pMeshIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="58443-111">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58443-112">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="58443-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="58443-113">Puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla que se va a limpiar.</span><span class="sxs-lookup"><span data-stu-id="58443-113">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to be cleaned.</span></span>

</dd> <dt>

<span data-ttu-id="58443-114">*pAdjacencyIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="58443-114">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58443-115">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="58443-115">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="58443-116">Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos de cada una de las caras de la malla que se van a limpiar.</span><span class="sxs-lookup"><span data-stu-id="58443-116">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be cleaned.</span></span>

</dd> <dt>

<span data-ttu-id="58443-117">*ppMeshOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="58443-117">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58443-118">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="58443-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="58443-119">Dirección de un puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla limpiada devuelta.</span><span class="sxs-lookup"><span data-stu-id="58443-119">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the returned cleaned mesh.</span></span> <span data-ttu-id="58443-120">Se devuelve la misma malla que se pasó si no se necesita ninguna limpieza.</span><span class="sxs-lookup"><span data-stu-id="58443-120">The same mesh is returned that was passed in if no cleaning was necessary.</span></span>

</dd> <dt>

<span data-ttu-id="58443-121">*pAdjacencyOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="58443-121">*pAdjacencyOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58443-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="58443-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="58443-123">Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla de salida.</span><span class="sxs-lookup"><span data-stu-id="58443-123">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="58443-124">*ppErrorsAndWarnings* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="58443-124">*ppErrorsAndWarnings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58443-125">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="58443-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="58443-126">Devuelve un búfer que contiene una cadena de errores y advertencias, que explican los problemas encontrados en la malla.</span><span class="sxs-lookup"><span data-stu-id="58443-126">Returns a buffer containing a string of errors and warnings, which explain the problems found in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58443-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58443-127">Return value</span></span>

<span data-ttu-id="58443-128">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="58443-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="58443-129">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="58443-129">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="58443-130">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="58443-130">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="58443-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58443-131">Remarks</span></span>

<span data-ttu-id="58443-132">Esta función limpia una malla mediante el método de limpieza y las opciones especificadas en el parámetro CleanType.</span><span class="sxs-lookup"><span data-stu-id="58443-132">This function cleans a mesh using the cleaning method and options specified in the CleanType parameter.</span></span> <span data-ttu-id="58443-133">Vea la enumeración [**D3DXCLEANTYPE**](./d3dxcleantype.md) para obtener una descripción de las opciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="58443-133">See the [**D3DXCLEANTYPE**](./d3dxcleantype.md) enumeration for a description of the available options.</span></span>

## <a name="requirements"></a><span data-ttu-id="58443-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58443-134">Requirements</span></span>



| <span data-ttu-id="58443-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="58443-135">Requirement</span></span> | <span data-ttu-id="58443-136">Value</span><span class="sxs-lookup"><span data-stu-id="58443-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58443-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="58443-137">Header</span></span><br/>  | <dl> <span data-ttu-id="58443-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="58443-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="58443-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="58443-139">Library</span></span><br/> | <dl> <span data-ttu-id="58443-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58443-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="58443-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="58443-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58443-142">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="58443-142">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
