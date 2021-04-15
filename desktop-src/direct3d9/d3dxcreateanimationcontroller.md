---
description: Crea un objeto de controlador de animación.
ms.assetid: 771e5966-ac1a-43c2-8e81-b6d573343ff0
title: Función D3DXCreateAnimationController (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateAnimationController
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a61b2c42a1eafa2ed28ac98c753588181a0ccf7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707868"
---
# <a name="d3dxcreateanimationcontroller-function"></a><span data-ttu-id="159d4-103">D3DXCreateAnimationController función)</span><span class="sxs-lookup"><span data-stu-id="159d4-103">D3DXCreateAnimationController function</span></span>

<span data-ttu-id="159d4-104">Crea un objeto de controlador de animación.</span><span class="sxs-lookup"><span data-stu-id="159d4-104">Creates an animation controller object.</span></span>

## <a name="syntax"></a><span data-ttu-id="159d4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="159d4-105">Syntax</span></span>


```C++
HRESULT D3DXCreateAnimationController(
  _In_  UINT                      MaxNumAnimationOutputs,
  _In_  UINT                      MaxNumAnimationSets,
  _In_  UINT                      MaxNumTracks,
  _In_  UINT                      MaxNumEvents,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="159d4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="159d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="159d4-107">*MaxNumAnimationOutputs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="159d4-107">*MaxNumAnimationOutputs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="159d4-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="159d4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="159d4-109">Número máximo de salidas de animación que el controlador puede admitir.</span><span class="sxs-lookup"><span data-stu-id="159d4-109">Maximum number of animation outputs the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="159d4-110">*MaxNumAnimationSets* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="159d4-110">*MaxNumAnimationSets* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="159d4-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="159d4-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="159d4-112">Número máximo de conjuntos de animaciones que se pueden mezclar.</span><span class="sxs-lookup"><span data-stu-id="159d4-112">Maximum number of animation sets that can be mixed.</span></span>

</dd> <dt>

<span data-ttu-id="159d4-113">*MaxNumTracks* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="159d4-113">*MaxNumTracks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="159d4-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="159d4-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="159d4-115">Número máximo de conjuntos de animaciones que se pueden mezclar simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="159d4-115">Maximum number of animation sets that can be mixed simultaneously.</span></span>

</dd> <dt>

<span data-ttu-id="159d4-116">*MaxNumEvents* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="159d4-116">*MaxNumEvents* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="159d4-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="159d4-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="159d4-118">Número máximo de eventos pendientes que el controlador admitirá.</span><span class="sxs-lookup"><span data-stu-id="159d4-118">Maximum number of outstanding events that the controller will support.</span></span>

</dd> <dt>

<span data-ttu-id="159d4-119">*ppAnimController* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="159d4-119">*ppAnimController* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="159d4-120">Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="159d4-120">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="159d4-121">Puntero al objeto de controlador de animación creado.</span><span class="sxs-lookup"><span data-stu-id="159d4-121">Pointer to the animation controller object created.</span></span> <span data-ttu-id="159d4-122">Vea [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="159d4-122">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="159d4-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="159d4-123">Return value</span></span>

<span data-ttu-id="159d4-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="159d4-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="159d4-125">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="159d4-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="159d4-126">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="159d4-126">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="159d4-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="159d4-127">Remarks</span></span>

<span data-ttu-id="159d4-128">Un controlador de animación controla un mezclador de animación.</span><span class="sxs-lookup"><span data-stu-id="159d4-128">An animation controller controls an animation mixer.</span></span> <span data-ttu-id="159d4-129">El controlador agrega métodos para modificar los parámetros de fusión a lo largo del tiempo para permitir transiciones suaves.</span><span class="sxs-lookup"><span data-stu-id="159d4-129">The controller adds methods to modify blending parameters over time to enable smooth transitions.</span></span>

## <a name="requirements"></a><span data-ttu-id="159d4-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="159d4-130">Requirements</span></span>



| <span data-ttu-id="159d4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="159d4-131">Requirement</span></span> | <span data-ttu-id="159d4-132">Value</span><span class="sxs-lookup"><span data-stu-id="159d4-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="159d4-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="159d4-133">Header</span></span><br/>  | <dl> <span data-ttu-id="159d4-134"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="159d4-134"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="159d4-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="159d4-135">Library</span></span><br/> | <dl> <span data-ttu-id="159d4-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="159d4-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="159d4-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="159d4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="159d4-138">Funciones de animación</span><span class="sxs-lookup"><span data-stu-id="159d4-138">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
