---
description: Establece una clave de evento que habilita o deshabilita una pista de animación.
ms.assetid: de81e646-0b94-40d3-89c2-060d118d17b2
title: 'ID3DXAnimationController:: KeyTrackEnable (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f22c732ff57e948ebcc2e89d790d352e4dc057ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362450"
---
# <a name="id3dxanimationcontrollerkeytrackenable-method"></a><span data-ttu-id="51a7f-103">ID3DXAnimationController:: KeyTrackEnable (método)</span><span class="sxs-lookup"><span data-stu-id="51a7f-103">ID3DXAnimationController::KeyTrackEnable method</span></span>

<span data-ttu-id="51a7f-104">Establece una clave de evento que habilita o deshabilita una pista de animación.</span><span class="sxs-lookup"><span data-stu-id="51a7f-104">Sets an event key that enables or disables an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="51a7f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51a7f-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackEnable(
  [in] UINT   Track,
  [in] BOOL   NewEnable,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a><span data-ttu-id="51a7f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51a7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51a7f-107">*Seguimiento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="51a7f-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51a7f-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51a7f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="51a7f-109">Identificador de la pista de animación que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="51a7f-109">Identifier of the animation track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="51a7f-110">*NewEnable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="51a7f-110">*NewEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51a7f-111">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51a7f-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="51a7f-112">Habilitar marca.</span><span class="sxs-lookup"><span data-stu-id="51a7f-112">Enable flag.</span></span> <span data-ttu-id="51a7f-113">Establézcalo en **true** para habilitar la pista de animación o en **false** para deshabilitar la pista.</span><span class="sxs-lookup"><span data-stu-id="51a7f-113">Set this to **TRUE** to enable the animation track, or to **FALSE** to disable the track.</span></span>

</dd> <dt>

<span data-ttu-id="51a7f-114">*StartTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="51a7f-114">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51a7f-115">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51a7f-115">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="51a7f-116">Clave de tiempo global.</span><span class="sxs-lookup"><span data-stu-id="51a7f-116">Global time key.</span></span> <span data-ttu-id="51a7f-117">Especifica la hora global a la que se llevará a cabo el cambio.</span><span class="sxs-lookup"><span data-stu-id="51a7f-117">Specifies the global time when the change will take place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51a7f-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51a7f-118">Return value</span></span>

<span data-ttu-id="51a7f-119">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="51a7f-119">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="51a7f-120">Identificador de evento para el evento de mezcla de prioridad.</span><span class="sxs-lookup"><span data-stu-id="51a7f-120">Event handle to the priority blend event.</span></span> <span data-ttu-id="51a7f-121">Se devuelve **null** si Track no es válido.</span><span class="sxs-lookup"><span data-stu-id="51a7f-121">**NULL** is returned if Track is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="51a7f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51a7f-122">Requirements</span></span>



| <span data-ttu-id="51a7f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="51a7f-123">Requirement</span></span> | <span data-ttu-id="51a7f-124">Value</span><span class="sxs-lookup"><span data-stu-id="51a7f-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="51a7f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51a7f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="51a7f-126"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="51a7f-126"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="51a7f-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="51a7f-127">Library</span></span><br/> | <dl> <span data-ttu-id="51a7f-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51a7f-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="51a7f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="51a7f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51a7f-130">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="51a7f-130">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
