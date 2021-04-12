---
description: Devuelve un identificador de evento de un evento de mezcla de prioridad que se está ejecutando actualmente.
ms.assetid: a7184459-7644-4e65-a8ea-13019889e02b
title: 'ID3DXAnimationController:: GetCurrentPriorityBlend (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: df8b52a5bd5267cf88eaf101a0589000099dd600
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362758"
---
# <a name="id3dxanimationcontrollergetcurrentpriorityblend-method"></a><span data-ttu-id="94e35-103">ID3DXAnimationController:: GetCurrentPriorityBlend (método)</span><span class="sxs-lookup"><span data-stu-id="94e35-103">ID3DXAnimationController::GetCurrentPriorityBlend method</span></span>

<span data-ttu-id="94e35-104">Devuelve un identificador de evento de un evento de mezcla de prioridad que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="94e35-104">Returns an event handle to a priority blend event that is currently running.</span></span>

## <a name="syntax"></a><span data-ttu-id="94e35-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94e35-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetCurrentPriorityBlend();
```



## <a name="parameters"></a><span data-ttu-id="94e35-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94e35-106">Parameters</span></span>

<span data-ttu-id="94e35-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="94e35-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="94e35-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94e35-108">Return value</span></span>

<span data-ttu-id="94e35-109">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="94e35-109">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="94e35-110">Identificador de evento para el evento de Blend de prioridad que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="94e35-110">Event handle to the currently running priority blend event.</span></span> <span data-ttu-id="94e35-111">Se devuelve **null** si no hay ningún evento de mezcla de prioridad en ejecución.</span><span class="sxs-lookup"><span data-stu-id="94e35-111">**NULL** is returned if no priority blend event is currently running.</span></span>

## <a name="requirements"></a><span data-ttu-id="94e35-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94e35-112">Requirements</span></span>



| <span data-ttu-id="94e35-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="94e35-113">Requirement</span></span> | <span data-ttu-id="94e35-114">Value</span><span class="sxs-lookup"><span data-stu-id="94e35-114">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="94e35-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94e35-115">Header</span></span><br/>  | <dl> <span data-ttu-id="94e35-116"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="94e35-116"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="94e35-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="94e35-117">Library</span></span><br/> | <dl> <span data-ttu-id="94e35-118"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94e35-118"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="94e35-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="94e35-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94e35-120">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="94e35-120">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




