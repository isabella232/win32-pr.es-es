---
description: Obtiene el tamaño de la revisión del rectángulo.
ms.assetid: d25373ef-789d-4515-83da-7049f040c9a4
title: Función D3DXRectPatchSize (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRectPatchSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5770e05493164db9da75fb38fa1e41594bfae8f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105689870"
---
# <a name="d3dxrectpatchsize-function"></a><span data-ttu-id="3301d-103">D3DXRectPatchSize función)</span><span class="sxs-lookup"><span data-stu-id="3301d-103">D3DXRectPatchSize function</span></span>

<span data-ttu-id="3301d-104">Obtiene el tamaño de la revisión del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="3301d-104">Gets the size of the rectangle patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="3301d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3301d-105">Syntax</span></span>


```C++
HRESULT D3DXRectPatchSize(
  _In_  const FLOAT *pfNumSegs,
  _Out_       DWORD *pdwTriangles,
  _Out_       DWORD *pwdVertices
);
```



## <a name="parameters"></a><span data-ttu-id="3301d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3301d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3301d-107">*pfNumSegs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3301d-107">*pfNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3301d-108">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="3301d-108">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3301d-109">Número de segmentos por borde a dividirlas.</span><span class="sxs-lookup"><span data-stu-id="3301d-109">Number of segments per edge to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="3301d-110">*pdwTriangles* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3301d-110">*pdwTriangles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3301d-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3301d-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3301d-112">Puntero a un valor DWORD que contiene el número de triángulos de la revisión.</span><span class="sxs-lookup"><span data-stu-id="3301d-112">Pointer to a DWORD that contains the number of triangles in the patch.</span></span>

</dd> <dt>

<span data-ttu-id="3301d-113">*pwdVertices* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3301d-113">*pwdVertices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3301d-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3301d-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3301d-115">Puntero a un valor DWORD que contiene el número de vértices de la revisión.</span><span class="sxs-lookup"><span data-stu-id="3301d-115">Pointer to a DWORD that contains the number of vertices in the patch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3301d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3301d-116">Return value</span></span>

<span data-ttu-id="3301d-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3301d-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3301d-118">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3301d-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3301d-119">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3301d-119">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="3301d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3301d-120">Requirements</span></span>



| <span data-ttu-id="3301d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3301d-121">Requirement</span></span> | <span data-ttu-id="3301d-122">Value</span><span class="sxs-lookup"><span data-stu-id="3301d-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3301d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3301d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="3301d-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3301d-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3301d-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3301d-125">Library</span></span><br/> | <dl> <span data-ttu-id="3301d-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3301d-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3301d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3301d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3301d-128">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="3301d-128">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="3301d-129">**D3DXTessellateRectPatch**</span><span class="sxs-lookup"><span data-stu-id="3301d-129">**D3DXTessellateRectPatch**</span></span>](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
