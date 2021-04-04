---
description: Tessellates una revisión de la superficie de orden superior triangular en una malla de triángulo.
ms.assetid: bcc9143f-fec0-491a-8d32-1df961b8dade
title: Función D3DXTessellateTriPatch (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateTriPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 61d5a426f9fe3331b85c4a881219319622283820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821047"
---
# <a name="d3dxtessellatetripatch-function"></a><span data-ttu-id="9d884-103">D3DXTessellateTriPatch función)</span><span class="sxs-lookup"><span data-stu-id="9d884-103">D3DXTessellateTriPatch function</span></span>

<span data-ttu-id="9d884-104">Tessellates una revisión de la superficie de orden superior triangular en una malla de triángulo.</span><span class="sxs-lookup"><span data-stu-id="9d884-104">Tessellates a triangular higher-order surface patch into a triangle mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d884-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d884-105">Syntax</span></span>


```C++
HRESULT D3DXTessellateTriPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3TRIPATCH_INFO         *pTriPatchInfo,
  _Inout_       LPD3DXMESH              pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="9d884-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d884-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d884-107">*pVB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9d884-107">*pVB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d884-108">Tipo: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span><span class="sxs-lookup"><span data-stu-id="9d884-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span></span>

<span data-ttu-id="9d884-109">Búfer de vértices que contiene los datos de revisión.</span><span class="sxs-lookup"><span data-stu-id="9d884-109">Vertex buffer containing the patch data.</span></span>

</dd> <dt>

<span data-ttu-id="9d884-110">*pNumSegs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9d884-110">*pNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d884-111">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="9d884-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9d884-112">Puntero a una matriz de tres valores de punto flotante que identifican el número de segmentos en los que cada borde de la revisión del triángulo debe dividirse cuando se tesela.</span><span class="sxs-lookup"><span data-stu-id="9d884-112">Pointer to an array of three floating-point values that identify the number of segments into which each edge of the triangle patch should be divided when tessellated.</span></span> <span data-ttu-id="9d884-113">Vea [**\_ información de D3DTRIPATCH**](d3dtripatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="9d884-113">See [**D3DTRIPATCH\_INFO**](d3dtripatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d884-114">*pInDecl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9d884-114">*pInDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d884-115">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="9d884-115">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="9d884-116">Estructura de declaración de vértices que define los datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="9d884-116">Vertex declaration structure that defines the vertex data.</span></span> <span data-ttu-id="9d884-117">Vea [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="9d884-117">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d884-118">*pTriPatchInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9d884-118">*pTriPatchInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d884-119">Tipo: **const [**D3TRIPATCH \_ info**](d3dtripatch-info.md) \***</span><span class="sxs-lookup"><span data-stu-id="9d884-119">Type: **const [**D3TRIPATCH\_INFO**](d3dtripatch-info.md)\***</span></span>

<span data-ttu-id="9d884-120">Describe una revisión de triángulo.</span><span class="sxs-lookup"><span data-stu-id="9d884-120">Describes a triangle patch.</span></span> <span data-ttu-id="9d884-121">Vea [**\_ información de D3DTRIPATCH**](d3dtripatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="9d884-121">See [**D3DTRIPATCH\_INFO**](d3dtripatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d884-122">*pmesh* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9d884-122">*pMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d884-123">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="9d884-123">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="9d884-124">Puntero a la malla creada.</span><span class="sxs-lookup"><span data-stu-id="9d884-124">Pointer to the created mesh.</span></span> <span data-ttu-id="9d884-125">Vea [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="9d884-125">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d884-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d884-126">Return value</span></span>

<span data-ttu-id="9d884-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9d884-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9d884-128">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9d884-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9d884-129">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="9d884-129">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d884-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9d884-130">Remarks</span></span>

<span data-ttu-id="9d884-131">Use [**D3DXTriPatchSize**](d3dxtripatchsize.md) para obtener el número de vértices y índices de salida que necesita la función de teselación.</span><span class="sxs-lookup"><span data-stu-id="9d884-131">Use [**D3DXTriPatchSize**](d3dxtripatchsize.md) to get the number of output vertices and indices that the tessellation function needs.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d884-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d884-132">Requirements</span></span>



| <span data-ttu-id="9d884-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d884-133">Requirement</span></span> | <span data-ttu-id="9d884-134">Value</span><span class="sxs-lookup"><span data-stu-id="9d884-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d884-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d884-135">Header</span></span><br/>  | <dl> <span data-ttu-id="9d884-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d884-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9d884-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9d884-137">Library</span></span><br/> | <dl> <span data-ttu-id="9d884-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d884-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9d884-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d884-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d884-140">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="9d884-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="9d884-141">**D3DXTessellateRectPatch**</span><span class="sxs-lookup"><span data-stu-id="9d884-141">**D3DXTessellateRectPatch**</span></span>](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
