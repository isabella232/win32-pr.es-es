---
description: Establece una clave de evento que cambia la velocidad de reproducción de una pista de animación.
ms.assetid: 217d3a2d-0fb7-4995-86ec-7a4e8420e338
title: 'ID3DXAnimationController:: KeyTrackSpeed (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 09705dd03e7767e94b1508cf4951186a509a3c5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708097"
---
# <a name="id3dxanimationcontrollerkeytrackspeed-method"></a><span data-ttu-id="0a271-103">ID3DXAnimationController:: KeyTrackSpeed (método)</span><span class="sxs-lookup"><span data-stu-id="0a271-103">ID3DXAnimationController::KeyTrackSpeed method</span></span>

<span data-ttu-id="0a271-104">Establece una clave de evento que cambia la velocidad de reproducción de una pista de animación.</span><span class="sxs-lookup"><span data-stu-id="0a271-104">Sets an event key that changes the rate of play of an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a271-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a271-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackSpeed(
  [in] UINT                Track,
  [in] FLOAT               NewSpeed,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a><span data-ttu-id="0a271-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a271-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a271-107">*Seguimiento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0a271-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a271-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a271-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a271-109">Identificador de la pista que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="0a271-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="0a271-110">*NewSpeed* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0a271-110">*NewSpeed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a271-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a271-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a271-112">Nueva velocidad de la pista de animación.</span><span class="sxs-lookup"><span data-stu-id="0a271-112">New speed of the animation track.</span></span>

</dd> <dt>

<span data-ttu-id="0a271-113">*StartTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0a271-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a271-114">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a271-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a271-115">Clave de tiempo global.</span><span class="sxs-lookup"><span data-stu-id="0a271-115">Global time key.</span></span> <span data-ttu-id="0a271-116">Especifica la hora global a la que se llevará a cabo el cambio.</span><span class="sxs-lookup"><span data-stu-id="0a271-116">Specifies the global time when the change will take place.</span></span>

</dd> <dt>

<span data-ttu-id="0a271-117">*Duración* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0a271-117">*Duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a271-118">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a271-118">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a271-119">Tiempo de transición, que especifica cuánto tiempo tardará la transición suave en completarse.</span><span class="sxs-lookup"><span data-stu-id="0a271-119">Transition time, which specifies how long the smooth transition will take to complete.</span></span>

</dd> <dt>

<span data-ttu-id="0a271-120">*Transición* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0a271-120">*Transition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a271-121">Tipo: **[ **D3DXTRANSITION \_ Type**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="0a271-121">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

<span data-ttu-id="0a271-122">Especifica el tipo de transición que se usa para realizar la transición entre velocidades.</span><span class="sxs-lookup"><span data-stu-id="0a271-122">Specifies the transition type used for transitioning between speeds.</span></span> <span data-ttu-id="0a271-123">Consulte [**\_ tipo de D3DXTRANSITION**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="0a271-123">See [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a271-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a271-124">Return value</span></span>

<span data-ttu-id="0a271-125">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="0a271-125">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="0a271-126">Identificador de evento para el evento de mezcla de prioridad.</span><span class="sxs-lookup"><span data-stu-id="0a271-126">Event handle to the priority blend event.</span></span> <span data-ttu-id="0a271-127">Se devuelve **null** si uno o varios de los parámetros de entrada no son válidos o no hay ningún evento libre disponible.</span><span class="sxs-lookup"><span data-stu-id="0a271-127">**NULL** is returned if one or more of the input parameters is invalid, or no free event is available.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a271-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a271-128">Requirements</span></span>



| <span data-ttu-id="0a271-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a271-129">Requirement</span></span> | <span data-ttu-id="0a271-130">Value</span><span class="sxs-lookup"><span data-stu-id="0a271-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a271-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a271-131">Header</span></span><br/>  | <dl> <span data-ttu-id="0a271-132"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a271-132"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0a271-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0a271-133">Library</span></span><br/> | <dl> <span data-ttu-id="0a271-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a271-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0a271-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a271-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a271-136">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="0a271-136">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
