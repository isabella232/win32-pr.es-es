---
description: Genera una reasignación de caras optimizada para una lista de triángulos.
ms.assetid: 428c2af8-43e7-4cf7-8b9b-04ba5cff82c8
title: Función D3DXOptimizeFaces (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeFaces
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c56dec04e01b542d2c760852a58826a8186c213
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698178"
---
# <a name="d3dxoptimizefaces-function"></a><span data-ttu-id="4e0eb-103">D3DXOptimizeFaces función)</span><span class="sxs-lookup"><span data-stu-id="4e0eb-103">D3DXOptimizeFaces function</span></span>

<span data-ttu-id="4e0eb-104">Genera una reasignación de caras optimizada para una lista de triángulos.</span><span class="sxs-lookup"><span data-stu-id="4e0eb-104">Generates an optimized face remapping for a triangle list.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e0eb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e0eb-105">Syntax</span></span>


```C++
HRESULT D3DXOptimizeFaces(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pFaceRemap
);
```



## <a name="parameters"></a><span data-ttu-id="4e0eb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e0eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e0eb-107">*pIndices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e0eb-107">*pIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e0eb-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e0eb-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e0eb-109">Puntero a los índices de la lista de triángulos que se van a usar para ordenar vértices.</span><span class="sxs-lookup"><span data-stu-id="4e0eb-109">Pointer to triangle list indices to use for ordering vertices.</span></span>

</dd> <dt>

<span data-ttu-id="4e0eb-110">*NumFaces* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e0eb-110">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e0eb-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e0eb-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e0eb-112">Número de caras en la lista de triángulos.</span><span class="sxs-lookup"><span data-stu-id="4e0eb-112">Number of faces in the triangle list.</span></span> <span data-ttu-id="4e0eb-113">En el caso de las mallas de 16 bits, esto está limitado a 2 ^ 16-1 (65535) o a menos caras.</span><span class="sxs-lookup"><span data-stu-id="4e0eb-113">For 16-bit meshes, this is limited to 2^16 - 1 (65535) or fewer faces.</span></span>

</dd> <dt>

<span data-ttu-id="4e0eb-114">*NumVertices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e0eb-114">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e0eb-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e0eb-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e0eb-116">Número de vértices a los que hace referencia la lista de triángulos.</span><span class="sxs-lookup"><span data-stu-id="4e0eb-116">Number of vertices referenced by the triangle list.</span></span>

</dd> <dt>

<span data-ttu-id="4e0eb-117">*Indices32Bit* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e0eb-117">*Indices32Bit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e0eb-118">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e0eb-118">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e0eb-119">Marca que indica el tipo de índice: **true** si los índices son de 32 bits (más de 65535 índices), **false** si los índices son de 16 bits (65535 o menos índices).</span><span class="sxs-lookup"><span data-stu-id="4e0eb-119">Flag indicating index type: **TRUE** if indices are 32-bit (more than 65535 indices), **FALSE** if indices are 16-bit (65535 or fewer indices).</span></span>

</dd> <dt>

<span data-ttu-id="4e0eb-120">*pFaceRemap* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4e0eb-120">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e0eb-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4e0eb-121">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4e0eb-122">Puntero a la superficie de la malla original que se ha dividido para generar la superficie actual.</span><span class="sxs-lookup"><span data-stu-id="4e0eb-122">Pointer to the original mesh face that was split to generate the current face.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e0eb-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e0eb-123">Return value</span></span>

<span data-ttu-id="4e0eb-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4e0eb-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4e0eb-125">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4e0eb-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4e0eb-126">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="4e0eb-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e0eb-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e0eb-127">Remarks</span></span>

<span data-ttu-id="4e0eb-128">El procedimiento de optimización de esta función es funcionalmente equivalente a llamar a [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) con la \_ marca DEVICEINDEPENDENT de D3DXMESHOPT, pero esta función hace un uso más eficaz de las memorias caché de vértices.</span><span class="sxs-lookup"><span data-stu-id="4e0eb-128">This function's optimization procedure is functionally equivalent to calling [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) with the D3DXMESHOPT\_DEVICEINDEPENDENT flag, but this function makes more efficient use of vertex caches.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e0eb-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e0eb-129">Requirements</span></span>



| <span data-ttu-id="4e0eb-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e0eb-130">Requirement</span></span> | <span data-ttu-id="4e0eb-131">Value</span><span class="sxs-lookup"><span data-stu-id="4e0eb-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e0eb-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e0eb-132">Header</span></span><br/>  | <dl> <span data-ttu-id="4e0eb-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e0eb-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4e0eb-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e0eb-134">Library</span></span><br/> | <dl> <span data-ttu-id="4e0eb-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e0eb-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4e0eb-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e0eb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e0eb-137">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="4e0eb-137">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
