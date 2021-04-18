---
description: Establece una clave de evento que cambia el peso de una pista de animación. El peso se utiliza como multiplicador al combinar varias pistas.
ms.assetid: fb2859de-9e77-49dd-be48-a50e22e2fc3a
title: 'ID3DXAnimationController:: KeyTrackWeight (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74f5e38392f6b4ac192f02b9d85421c8357a16ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718416"
---
# <a name="id3dxanimationcontrollerkeytrackweight-method"></a><span data-ttu-id="8ba2a-103">ID3DXAnimationController:: KeyTrackWeight (método)</span><span class="sxs-lookup"><span data-stu-id="8ba2a-103">ID3DXAnimationController::KeyTrackWeight method</span></span>

<span data-ttu-id="8ba2a-104">Establece una clave de evento que cambia el peso de una pista de animación. El peso se utiliza como multiplicador al combinar varias pistas.</span><span class="sxs-lookup"><span data-stu-id="8ba2a-104">Sets an event key that changes the weight of an animation track. The weight is used as a multiplier when combining multiple tracks together.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ba2a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ba2a-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackWeight(
  [in] UINT                Track,
  [in] FLOAT               NewWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a><span data-ttu-id="8ba2a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ba2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ba2a-107">*Seguimiento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8ba2a-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba2a-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ba2a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ba2a-109">Identificador de la pista que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="8ba2a-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="8ba2a-110">*NewWeight* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ba2a-110">*NewWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba2a-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ba2a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ba2a-112">Nuevo peso de la pista.</span><span class="sxs-lookup"><span data-stu-id="8ba2a-112">New weight of the track.</span></span>

</dd> <dt>

<span data-ttu-id="8ba2a-113">*StartTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ba2a-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba2a-114">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ba2a-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ba2a-115">Clave de tiempo global.</span><span class="sxs-lookup"><span data-stu-id="8ba2a-115">Global time key.</span></span> <span data-ttu-id="8ba2a-116">Especifica la hora global a la que se llevará a cabo el cambio.</span><span class="sxs-lookup"><span data-stu-id="8ba2a-116">Specifies the global time when the change will take place.</span></span>

</dd> <dt>

<span data-ttu-id="8ba2a-117">*Duración* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8ba2a-117">*Duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba2a-118">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ba2a-118">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ba2a-119">Tiempo de transición, que especifica cuánto tiempo tardará la transición suave en completarse.</span><span class="sxs-lookup"><span data-stu-id="8ba2a-119">Transition time, which specifies how long the smooth transition will take to complete.</span></span>

</dd> <dt>

<span data-ttu-id="8ba2a-120">*Transición* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ba2a-120">*Transition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba2a-121">Tipo: **[ **D3DXTRANSITION \_ Type**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="8ba2a-121">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

<span data-ttu-id="8ba2a-122">Especifica el tipo de transición que se usa para realizar la transición entre pesos.</span><span class="sxs-lookup"><span data-stu-id="8ba2a-122">Specifies the transition type used for transitioning between weights.</span></span> <span data-ttu-id="8ba2a-123">Consulte [**\_ tipo de D3DXTRANSITION**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="8ba2a-123">See [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ba2a-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ba2a-124">Return value</span></span>

<span data-ttu-id="8ba2a-125">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="8ba2a-125">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="8ba2a-126">Identificador de evento para el evento de mezcla de prioridad.</span><span class="sxs-lookup"><span data-stu-id="8ba2a-126">Event handle to the priority blend event.</span></span> <span data-ttu-id="8ba2a-127">Se devuelve **null** si uno o varios de los parámetros de entrada no son válidos o no hay ningún evento libre disponible.</span><span class="sxs-lookup"><span data-stu-id="8ba2a-127">**NULL** is returned if one or more of the input parameters is invalid, or no free event is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ba2a-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ba2a-128">Remarks</span></span>

<span data-ttu-id="8ba2a-129">El peso se usa como un multiplicador para determinar la cantidad de esta pista que se va a combinar con otras pistas.</span><span class="sxs-lookup"><span data-stu-id="8ba2a-129">The weight is used like a multiplier to determine how much of this track to blend together with other tracks.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ba2a-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ba2a-130">Requirements</span></span>



| <span data-ttu-id="8ba2a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ba2a-131">Requirement</span></span> | <span data-ttu-id="8ba2a-132">Value</span><span class="sxs-lookup"><span data-stu-id="8ba2a-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ba2a-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ba2a-133">Header</span></span><br/>  | <dl> <span data-ttu-id="8ba2a-134"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ba2a-134"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="8ba2a-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ba2a-135">Library</span></span><br/> | <dl> <span data-ttu-id="8ba2a-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ba2a-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8ba2a-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ba2a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ba2a-138">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="8ba2a-138">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
