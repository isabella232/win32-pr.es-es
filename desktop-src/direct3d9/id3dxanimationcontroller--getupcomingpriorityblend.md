---
description: Devuelve un identificador de evento al siguiente evento de Blend de prioridad programado para que se produzca después de un evento especificado.
ms.assetid: 64fa6fca-dc4a-4534-ab8e-b11b3c7ed23c
title: 'ID3DXAnimationController:: GetUpcomingPriorityBlend (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 72f9b8854041094d43d9e8250ab61b5f59a67848
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424323"
---
# <a name="id3dxanimationcontrollergetupcomingpriorityblend-method"></a><span data-ttu-id="11263-103">ID3DXAnimationController:: GetUpcomingPriorityBlend (método)</span><span class="sxs-lookup"><span data-stu-id="11263-103">ID3DXAnimationController::GetUpcomingPriorityBlend method</span></span>

<span data-ttu-id="11263-104">Devuelve un identificador de evento al siguiente evento de Blend de prioridad programado para que se produzca después de un evento especificado.</span><span class="sxs-lookup"><span data-stu-id="11263-104">Returns an event handle to the next priority blend event scheduled to occur after a specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="11263-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11263-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetUpcomingPriorityBlend(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="11263-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11263-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11263-107">*hEvent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="11263-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11263-108">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="11263-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="11263-109">Identificador de evento de un evento especificado después del cual se va a buscar un evento de mezcla de prioridad siguiente.</span><span class="sxs-lookup"><span data-stu-id="11263-109">Event handle to a specified event after which to search for a following priority blend event.</span></span> <span data-ttu-id="11263-110">Si se establece en **null**, el método devolverá el siguiente evento de Blend de prioridad programado.</span><span class="sxs-lookup"><span data-stu-id="11263-110">If set to **NULL**, then the method will return the next scheduled priority blend event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11263-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11263-111">Return value</span></span>

<span data-ttu-id="11263-112">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="11263-112">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="11263-113">Identificador de evento para el siguiente evento de Blend de prioridad programado.</span><span class="sxs-lookup"><span data-stu-id="11263-113">Event handle to the next scheduled priority blend event.</span></span> <span data-ttu-id="11263-114">Se devuelve **null** si no hay un nuevo evento de mezcla de prioridad programado.</span><span class="sxs-lookup"><span data-stu-id="11263-114">**NULL** is returned if no new priority blend event is scheduled.</span></span>

## <a name="remarks"></a><span data-ttu-id="11263-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11263-115">Remarks</span></span>

<span data-ttu-id="11263-116">Este método se puede usar de forma iterativa para buscar un evento de combinación de prioridad que se desee pasando repetidamente el **valor null** para hEvent.</span><span class="sxs-lookup"><span data-stu-id="11263-116">This method can be used iteratively to locate a desired priority blend event by repeatedly passing in **NULL** for hEvent.</span></span>

> [!Note]  
> <span data-ttu-id="11263-117">No itere más después de que el método devuelva **null**.</span><span class="sxs-lookup"><span data-stu-id="11263-117">Do not iterate further after the method has returned **NULL**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="11263-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11263-118">Requirements</span></span>



| <span data-ttu-id="11263-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="11263-119">Requirement</span></span> | <span data-ttu-id="11263-120">Value</span><span class="sxs-lookup"><span data-stu-id="11263-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11263-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11263-121">Header</span></span><br/>  | <dl> <span data-ttu-id="11263-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="11263-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="11263-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="11263-123">Library</span></span><br/> | <dl> <span data-ttu-id="11263-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11263-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="11263-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="11263-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11263-126">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="11263-126">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




