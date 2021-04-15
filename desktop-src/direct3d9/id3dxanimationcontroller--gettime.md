---
description: Obtiene el tiempo de animación global.
ms.assetid: a46e2a57-a76a-4d79-a3b6-30b242321ed2
title: 'ID3DXAnimationController:: GetTime (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2bfc3c2c1d5bb0bbbb3c364b47f22f0790f8d102
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707967"
---
# <a name="id3dxanimationcontrollergettime-method"></a><span data-ttu-id="754b6-103">ID3DXAnimationController:: GetTime (método)</span><span class="sxs-lookup"><span data-stu-id="754b6-103">ID3DXAnimationController::GetTime method</span></span>

<span data-ttu-id="754b6-104">Obtiene el tiempo de animación global.</span><span class="sxs-lookup"><span data-stu-id="754b6-104">Gets the global animation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="754b6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="754b6-105">Syntax</span></span>


```C++
DOUBLE GetTime();
```



## <a name="parameters"></a><span data-ttu-id="754b6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="754b6-106">Parameters</span></span>

<span data-ttu-id="754b6-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="754b6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="754b6-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="754b6-108">Return value</span></span>

<span data-ttu-id="754b6-109">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="754b6-109">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="754b6-110">Devuelve el tiempo de animación global.</span><span class="sxs-lookup"><span data-stu-id="754b6-110">Returns the global animation time.</span></span>

## <a name="remarks"></a><span data-ttu-id="754b6-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="754b6-111">Remarks</span></span>

<span data-ttu-id="754b6-112">Las animaciones se diseñan con un tiempo de animación local y se mezclan en la hora global con [**AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span><span class="sxs-lookup"><span data-stu-id="754b6-112">Animations are designed using a local animation time and mixed into global time with [**AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="754b6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="754b6-113">Requirements</span></span>



| <span data-ttu-id="754b6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="754b6-114">Requirement</span></span> | <span data-ttu-id="754b6-115">Value</span><span class="sxs-lookup"><span data-stu-id="754b6-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="754b6-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="754b6-116">Header</span></span><br/>  | <dl> <span data-ttu-id="754b6-117"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="754b6-117"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="754b6-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="754b6-118">Library</span></span><br/> | <dl> <span data-ttu-id="754b6-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="754b6-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="754b6-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="754b6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="754b6-121">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="754b6-121">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
