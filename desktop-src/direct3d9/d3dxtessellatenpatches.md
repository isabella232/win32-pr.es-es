---
description: Tessellates la malla determinada mediante el esquema de teselación de N-patch.
ms.assetid: e804905d-ee0b-484f-a621-58b197bd370b
title: Función D3DXTessellateNPatches (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateNPatches
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c8811816447deb858b5c8b42d651d219f06fef5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717701"
---
# <a name="d3dxtessellatenpatches-function"></a><span data-ttu-id="79409-103">D3DXTessellateNPatches función)</span><span class="sxs-lookup"><span data-stu-id="79409-103">D3DXTessellateNPatches function</span></span>

<span data-ttu-id="79409-104">Tessellates la malla determinada mediante el esquema de teselación de N-patch.</span><span class="sxs-lookup"><span data-stu-id="79409-104">Tessellates the given mesh using the N-patch tessellation scheme.</span></span>

## <a name="syntax"></a><span data-ttu-id="79409-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79409-105">Syntax</span></span>


```C++
HRESULT D3DXTessellateNPatches(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const CONST DWORD  *pAdjacencyIn,
  _In_        FLOAT        NumSegs,
  _In_        BOOL         QuadraticInterpNormals,
  _Out_       LPD3DXMESH   *ppMeshOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyOut
);
```



## <a name="parameters"></a><span data-ttu-id="79409-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79409-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79409-107">*pMeshIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79409-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79409-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="79409-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="79409-109">Puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla a dividirlas.</span><span class="sxs-lookup"><span data-stu-id="79409-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="79409-110">*pAdjacencyIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79409-110">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79409-111">Tipo: **CONST const DWORD \***</span><span class="sxs-lookup"><span data-stu-id="79409-111">Type: **const CONST DWORD\***</span></span>

<span data-ttu-id="79409-112">Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla de origen.</span><span class="sxs-lookup"><span data-stu-id="79409-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="79409-113">Este parámetro puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="79409-113">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="79409-114">*NumSegs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79409-114">*NumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79409-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79409-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79409-116">Número de segmentos por borde a dividirlas.</span><span class="sxs-lookup"><span data-stu-id="79409-116">Number of segments per edge to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="79409-117">*QuadraticInterpNormals* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79409-117">*QuadraticInterpNormals* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79409-118">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79409-118">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79409-119">Establézcalo en **true** para usar la interpolación cuadrática para las normales; establézcalo en **false** para la interpolación lineal.</span><span class="sxs-lookup"><span data-stu-id="79409-119">Set to **TRUE** to use quadratic interpolation for normals; set to **FALSE** for linear interpolation.</span></span>

</dd> <dt>

<span data-ttu-id="79409-120">*ppMeshOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="79409-120">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79409-121">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="79409-121">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="79409-122">Dirección de un puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla teselada devuelta.</span><span class="sxs-lookup"><span data-stu-id="79409-122">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the returned tessellated mesh.</span></span>

</dd> <dt>

<span data-ttu-id="79409-123">*ppAdjacencyOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="79409-123">*ppAdjacencyOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79409-124">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="79409-124">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="79409-125">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="79409-125">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="79409-126">Si el valor de este parámetro no se establece en **null**, este búfer contendrá una matriz de tres valores DWORD por cada tipo que especifique los tres vecinos para cada una de las caras de la malla de salida.</span><span class="sxs-lookup"><span data-stu-id="79409-126">If the value of this parameter is not set to **NULL**, this buffer will contain an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span> <span data-ttu-id="79409-127">Este parámetro puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="79409-127">This parameter may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79409-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79409-128">Return value</span></span>

<span data-ttu-id="79409-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="79409-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="79409-130">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="79409-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="79409-131">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="79409-131">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="79409-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79409-132">Remarks</span></span>

<span data-ttu-id="79409-133">Esta función tessellates con el algoritmo N-patch.</span><span class="sxs-lookup"><span data-stu-id="79409-133">This function tessellates by using the N-patch algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="79409-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79409-134">Requirements</span></span>



| <span data-ttu-id="79409-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="79409-135">Requirement</span></span> | <span data-ttu-id="79409-136">Value</span><span class="sxs-lookup"><span data-stu-id="79409-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="79409-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79409-137">Header</span></span><br/>  | <dl> <span data-ttu-id="79409-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="79409-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="79409-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79409-139">Library</span></span><br/> | <dl> <span data-ttu-id="79409-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79409-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="79409-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="79409-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79409-142">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="79409-142">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
