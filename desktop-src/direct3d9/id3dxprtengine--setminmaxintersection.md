---
description: Establece las distancias mínima y máxima de intersección entre los objetos 3D.
ms.assetid: da825c70-0c55-4303-b78a-a761ba037182
title: 'ID3DXPRTEngine:: SetMinMaxIntersection (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMinMaxIntersection
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68845f713289c524afc844037ca305909e5b89b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362629"
---
# <a name="id3dxprtenginesetminmaxintersection-method"></a><span data-ttu-id="4f4c6-103">ID3DXPRTEngine:: SetMinMaxIntersection (método)</span><span class="sxs-lookup"><span data-stu-id="4f4c6-103">ID3DXPRTEngine::SetMinMaxIntersection method</span></span>

<span data-ttu-id="4f4c6-104">Establece las distancias mínima y máxima de intersección entre los objetos 3D.</span><span class="sxs-lookup"><span data-stu-id="4f4c6-104">Sets the minimum and maximum distances of intersection between 3D objects.</span></span> <span data-ttu-id="4f4c6-105">Estos valores de distancia se pueden usar para controlar la distancia mínima o máxima con la que los objetos pueden sombrear o reflejar la luz.</span><span class="sxs-lookup"><span data-stu-id="4f4c6-105">These distance values can be used to control the minimum or maximum distance that objects can shadow or reflect light.</span></span> <span data-ttu-id="4f4c6-106">Por ejemplo, el método se puede utilizar para limitar el sombreado de las características cercanas de un modelo 3D.</span><span class="sxs-lookup"><span data-stu-id="4f4c6-106">For example, the method can be used to limit the shadowing of nearby features of a 3D model.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f4c6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f4c6-107">Syntax</span></span>


```C++
HRESULT SetMinMaxIntersection(
  [in] FLOAT fMin ,
  [in] FLOAT fMax
);
```



## <a name="parameters"></a><span data-ttu-id="4f4c6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f4c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f4c6-109">*fMin (* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4f4c6-109">*fMin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f4c6-110">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f4c6-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4f4c6-111">Distancia de intersección mínima.</span><span class="sxs-lookup"><span data-stu-id="4f4c6-111">Minimum intersection distance.</span></span> <span data-ttu-id="4f4c6-112">Debe ser positivo y menor que fMax.</span><span class="sxs-lookup"><span data-stu-id="4f4c6-112">Must be positive and less than fMax.</span></span>

</dd> <dt>

<span data-ttu-id="4f4c6-113">*fMax* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4f4c6-113">*fMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f4c6-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f4c6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4f4c6-115">Distancia máxima de intersección.</span><span class="sxs-lookup"><span data-stu-id="4f4c6-115">Maximum intersection distance.</span></span> <span data-ttu-id="4f4c6-116">Si 0,0 f, se usará el valor anterior; de lo contrario, debe ser mayor que fMin (.</span><span class="sxs-lookup"><span data-stu-id="4f4c6-116">If 0.0f, the previous value will be used; otherwise, must be greater than fMin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f4c6-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f4c6-117">Return value</span></span>

<span data-ttu-id="4f4c6-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4f4c6-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4f4c6-119">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4f4c6-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4f4c6-120">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="4f4c6-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f4c6-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f4c6-121">Remarks</span></span>

<span data-ttu-id="4f4c6-122">Este método no se puede usar en las simulaciones de transferencia Radiance (PRT) precalculadas que se ejecutan en la GPU.</span><span class="sxs-lookup"><span data-stu-id="4f4c6-122">This method cannot be used in precomputed radiance transfer (PRT) simulations that run in the GPU.</span></span> <span data-ttu-id="4f4c6-123">Vea [**ID3DXPRTEngine:: ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md).</span><span class="sxs-lookup"><span data-stu-id="4f4c6-123">See [**ID3DXPRTEngine::ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f4c6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f4c6-124">Requirements</span></span>



| <span data-ttu-id="4f4c6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f4c6-125">Requirement</span></span> | <span data-ttu-id="4f4c6-126">Value</span><span class="sxs-lookup"><span data-stu-id="4f4c6-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f4c6-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f4c6-127">Header</span></span><br/>  | <dl> <span data-ttu-id="4f4c6-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f4c6-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4f4c6-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4f4c6-129">Library</span></span><br/> | <dl> <span data-ttu-id="4f4c6-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f4c6-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4f4c6-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f4c6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f4c6-132">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="4f4c6-132">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
