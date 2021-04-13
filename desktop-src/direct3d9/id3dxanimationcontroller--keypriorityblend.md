---
description: Establece las claves de evento de mezcla para la pista de animación especificada.
ms.assetid: 2023d566-1de5-465a-ad6f-04a78ac01c33
title: 'ID3DXAnimationController:: KeyPriorityBlend (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31778da9b26ddd79b5f05c69c822ed62a5b5281e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362451"
---
# <a name="id3dxanimationcontrollerkeypriorityblend-method"></a><span data-ttu-id="bd963-103">ID3DXAnimationController:: KeyPriorityBlend (método)</span><span class="sxs-lookup"><span data-stu-id="bd963-103">ID3DXAnimationController::KeyPriorityBlend method</span></span>

<span data-ttu-id="bd963-104">Establece las claves de evento de mezcla para la pista de animación especificada.</span><span class="sxs-lookup"><span data-stu-id="bd963-104">Sets blending event keys for the specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd963-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd963-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyPriorityBlend(
  [in] FLOAT               NewBlendWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a><span data-ttu-id="bd963-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd963-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd963-107">*NewBlendWeight* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bd963-107">*NewBlendWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd963-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bd963-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bd963-109">Número comprendido entre 0 y 1 que se usa para fusionar las pistas.</span><span class="sxs-lookup"><span data-stu-id="bd963-109">Number between 0 and 1 that is used to blend tracks together.</span></span>

</dd> <dt>

<span data-ttu-id="bd963-110">*StartTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bd963-110">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd963-111">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bd963-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bd963-112">Hora global para iniciar la mezcla.</span><span class="sxs-lookup"><span data-stu-id="bd963-112">Global time to start the blend.</span></span>

</dd> <dt>

<span data-ttu-id="bd963-113">*Duración* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="bd963-113">*Duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd963-114">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bd963-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bd963-115">Duración global de la mezcla.</span><span class="sxs-lookup"><span data-stu-id="bd963-115">Global time duration of the blend.</span></span>

</dd> <dt>

<span data-ttu-id="bd963-116">*Transición* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bd963-116">*Transition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd963-117">Tipo: **[ **D3DXTRANSITION \_ Type**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="bd963-117">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

<span data-ttu-id="bd963-118">Especifica el tipo de transición que se usa para la duración de la mezcla.</span><span class="sxs-lookup"><span data-stu-id="bd963-118">Specifies the transition type used for the duration of the blend.</span></span> <span data-ttu-id="bd963-119">Consulte [**\_ tipo de D3DXTRANSITION**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="bd963-119">See [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd963-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd963-120">Return value</span></span>

<span data-ttu-id="bd963-121">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="bd963-121">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="bd963-122">Identificador de evento para el evento de mezcla de prioridad.</span><span class="sxs-lookup"><span data-stu-id="bd963-122">Event handle to the priority blend event.</span></span> <span data-ttu-id="bd963-123">Se devuelve **null** si uno o varios de los parámetros de entrada no son válidos o no hay ningún evento libre disponible.</span><span class="sxs-lookup"><span data-stu-id="bd963-123">**NULL** is returned if one or more of the input parameters is invalid, or no free event is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd963-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd963-124">Remarks</span></span>

<span data-ttu-id="bd963-125">El controlador de animación se mezcla en tres fases: las pistas de prioridad baja se mezclan en primer lugar, las pistas de prioridad alta se combinan en segundo y, a continuación, se combinan los resultados de ambos.</span><span class="sxs-lookup"><span data-stu-id="bd963-125">The animation controller blends in three phases: low priority tracks are blended first, high priority tracks are blended second, and then the results of both are blended.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd963-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd963-126">Requirements</span></span>



| <span data-ttu-id="bd963-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd963-127">Requirement</span></span> | <span data-ttu-id="bd963-128">Value</span><span class="sxs-lookup"><span data-stu-id="bd963-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd963-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd963-129">Header</span></span><br/>  | <dl> <span data-ttu-id="bd963-130"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd963-130"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="bd963-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bd963-131">Library</span></span><br/> | <dl> <span data-ttu-id="bd963-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd963-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bd963-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd963-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd963-134">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="bd963-134">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> <dt>

[<span data-ttu-id="bd963-135">**SetPriorityBlend**</span><span class="sxs-lookup"><span data-stu-id="bd963-135">**SetPriorityBlend**</span></span>](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 
