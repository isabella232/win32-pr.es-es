---
description: Tessellates una revisión de la superficie de orden superior rectangular en una malla de triángulo.
ms.assetid: d941d994-8a13-49ff-a0b1-b21a3f84ed78
title: Función D3DXTessellateRectPatch (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateRectPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 887f0035b50efd860149410e50dd6abff301968d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280299"
---
# <a name="d3dxtessellaterectpatch-function"></a><span data-ttu-id="74a53-103">D3DXTessellateRectPatch función)</span><span class="sxs-lookup"><span data-stu-id="74a53-103">D3DXTessellateRectPatch function</span></span>

<span data-ttu-id="74a53-104">Tessellates una revisión de la superficie de orden superior rectangular en una malla de triángulo.</span><span class="sxs-lookup"><span data-stu-id="74a53-104">Tessellates a rectangular higher-order surface patch into a triangle mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="74a53-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74a53-105">Syntax</span></span>


```C++
HRESULT D3DXTessellateRectPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3DRECTPATCH_INFO       *pRectPatchInfo,
  _Inout_       LPD3DXMESH              pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="74a53-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74a53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74a53-107">*pVB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74a53-107">*pVB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74a53-108">Tipo: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span><span class="sxs-lookup"><span data-stu-id="74a53-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span></span>

<span data-ttu-id="74a53-109">Búfer de vértices que contiene los datos de revisión.</span><span class="sxs-lookup"><span data-stu-id="74a53-109">Vertex buffer containing the patch data.</span></span>

</dd> <dt>

<span data-ttu-id="74a53-110">*pNumSegs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74a53-110">*pNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74a53-111">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="74a53-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="74a53-112">Puntero a una matriz de cuatro valores de punto flotante que identifican el número de segmentos en los que cada borde de la revisión del rectángulo debe dividirse cuando se tesela.</span><span class="sxs-lookup"><span data-stu-id="74a53-112">Pointer to an array of four floating-point values that identify the number of segments into which each edge of the rectangle patch should be divided when tessellated.</span></span> <span data-ttu-id="74a53-113">Vea [**\_ información de D3DRECTPATCH**](d3drectpatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="74a53-113">See [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="74a53-114">*pInDecl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74a53-114">*pInDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74a53-115">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="74a53-115">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="74a53-116">Estructura de declaración de vértices que define los datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="74a53-116">Vertex declaration structure that defines the vertex data.</span></span> <span data-ttu-id="74a53-117">Vea [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="74a53-117">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="74a53-118">*pRectPatchInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74a53-118">*pRectPatchInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74a53-119">Tipo: **const [**D3DRECTPATCH \_ info**](d3drectpatch-info.md) \***</span><span class="sxs-lookup"><span data-stu-id="74a53-119">Type: **const [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md)\***</span></span>

<span data-ttu-id="74a53-120">Describe una revisión rectangular.</span><span class="sxs-lookup"><span data-stu-id="74a53-120">Describes a rectangular patch.</span></span> <span data-ttu-id="74a53-121">Vea [**\_ información de D3DRECTPATCH**](d3drectpatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="74a53-121">See [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="74a53-122">*pmesh* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="74a53-122">*pMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="74a53-123">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="74a53-123">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="74a53-124">Puntero a la malla creada.</span><span class="sxs-lookup"><span data-stu-id="74a53-124">Pointer to the created mesh.</span></span> <span data-ttu-id="74a53-125">Vea [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="74a53-125">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74a53-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74a53-126">Return value</span></span>

<span data-ttu-id="74a53-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="74a53-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="74a53-128">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="74a53-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="74a53-129">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="74a53-129">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="74a53-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74a53-130">Remarks</span></span>

<span data-ttu-id="74a53-131">Use [**D3DXRectPatchSize**](d3dxrectpatchsize.md) para obtener el número de vértices y índices de salida que necesita la función de teselación.</span><span class="sxs-lookup"><span data-stu-id="74a53-131">Use [**D3DXRectPatchSize**](d3dxrectpatchsize.md) to get the number of output vertices and indices that the tessellation function needs.</span></span>

## <a name="requirements"></a><span data-ttu-id="74a53-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74a53-132">Requirements</span></span>



| <span data-ttu-id="74a53-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="74a53-133">Requirement</span></span> | <span data-ttu-id="74a53-134">Value</span><span class="sxs-lookup"><span data-stu-id="74a53-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74a53-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74a53-135">Header</span></span><br/>  | <dl> <span data-ttu-id="74a53-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="74a53-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="74a53-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="74a53-137">Library</span></span><br/> | <dl> <span data-ttu-id="74a53-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74a53-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="74a53-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="74a53-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74a53-140">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="74a53-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="74a53-141">**D3DXTessellateTriPatch**</span><span class="sxs-lookup"><span data-stu-id="74a53-141">**D3DXTessellateTriPatch**</span></span>](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
