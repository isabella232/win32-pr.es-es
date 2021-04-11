---
description: Establece una clave de evento que cambia la hora local de una pista de animación.
ms.assetid: b527e960-8ab9-42a0-bb4d-bea5aaf83424
title: 'ID3DXAnimationController:: KeyTrackPosition (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d027069efa9fb49cad3d2344da593eae4c3c844c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362701"
---
# <a name="id3dxanimationcontrollerkeytrackposition-method"></a><span data-ttu-id="84fde-103">ID3DXAnimationController:: KeyTrackPosition (método)</span><span class="sxs-lookup"><span data-stu-id="84fde-103">ID3DXAnimationController::KeyTrackPosition method</span></span>

<span data-ttu-id="84fde-104">Establece una clave de evento que cambia la hora local de una pista de animación.</span><span class="sxs-lookup"><span data-stu-id="84fde-104">Sets an event key that changes the local time of an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="84fde-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84fde-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackPosition(
  [in] UINT   Track,
  [in] DOUBLE NewPosition,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a><span data-ttu-id="84fde-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84fde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84fde-107">*Seguimiento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="84fde-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84fde-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84fde-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84fde-109">Identificador de la pista que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="84fde-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="84fde-110">*NewPosition* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84fde-110">*NewPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84fde-111">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84fde-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84fde-112">Nueva hora local de la pista de animación.</span><span class="sxs-lookup"><span data-stu-id="84fde-112">New local time of the animation track.</span></span>

</dd> <dt>

<span data-ttu-id="84fde-113">*StartTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84fde-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84fde-114">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84fde-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84fde-115">Clave de tiempo global.</span><span class="sxs-lookup"><span data-stu-id="84fde-115">Global time key.</span></span> <span data-ttu-id="84fde-116">Especifica la hora global a la que se llevará a cabo el cambio.</span><span class="sxs-lookup"><span data-stu-id="84fde-116">Specifies the global time when the change will take place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84fde-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84fde-117">Return value</span></span>

<span data-ttu-id="84fde-118">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="84fde-118">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="84fde-119">Identificador de evento para el evento de mezcla de prioridad.</span><span class="sxs-lookup"><span data-stu-id="84fde-119">Event handle to the priority blend event.</span></span> <span data-ttu-id="84fde-120">Se devuelve **null** si Track no es válido o si no hay ningún evento Free disponible.</span><span class="sxs-lookup"><span data-stu-id="84fde-120">**NULL** is returned if Track is invalid, or if no free event is available.</span></span>

## <a name="requirements"></a><span data-ttu-id="84fde-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84fde-121">Requirements</span></span>



| <span data-ttu-id="84fde-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="84fde-122">Requirement</span></span> | <span data-ttu-id="84fde-123">Value</span><span class="sxs-lookup"><span data-stu-id="84fde-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="84fde-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84fde-124">Header</span></span><br/>  | <dl> <span data-ttu-id="84fde-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="84fde-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="84fde-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="84fde-126">Library</span></span><br/> | <dl> <span data-ttu-id="84fde-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="84fde-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="84fde-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="84fde-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84fde-129">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="84fde-129">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
