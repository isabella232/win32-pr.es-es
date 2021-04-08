---
description: Devuelve un identificador de evento al siguiente evento programado para que se produzca después de un evento especificado en una pista de animación.
ms.assetid: 616b2de1-6107-4d18-ad2e-de2ef4560aee
title: 'ID3DXAnimationController:: GetUpcomingTrackEvent (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f863ce918f25c6b0975010f71a63f067c01f7345
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003772"
---
# <a name="id3dxanimationcontrollergetupcomingtrackevent-method"></a><span data-ttu-id="b3d72-103">ID3DXAnimationController:: GetUpcomingTrackEvent (método)</span><span class="sxs-lookup"><span data-stu-id="b3d72-103">ID3DXAnimationController::GetUpcomingTrackEvent method</span></span>

<span data-ttu-id="b3d72-104">Devuelve un identificador de evento al siguiente evento programado para que se produzca después de un evento especificado en una pista de animación.</span><span class="sxs-lookup"><span data-stu-id="b3d72-104">Returns an event handle to the next event scheduled to occur after a specified event on an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3d72-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3d72-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetUpcomingTrackEvent(
  [in] UINT            Track,
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="b3d72-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3d72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3d72-107">*Seguimiento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b3d72-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3d72-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3d72-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3d72-109">Identificador de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="b3d72-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b3d72-110">*hEvent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b3d72-110">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3d72-111">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="b3d72-111">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="b3d72-112">Identificador de evento de un evento especificado después del cual se va a buscar un evento siguiente.</span><span class="sxs-lookup"><span data-stu-id="b3d72-112">Event handle to a specified event after which to search for a following event.</span></span> <span data-ttu-id="b3d72-113">Si se establece en **null**, el método devolverá el siguiente evento programado.</span><span class="sxs-lookup"><span data-stu-id="b3d72-113">If set to **NULL**, then the method will return the next scheduled event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3d72-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3d72-114">Return value</span></span>

<span data-ttu-id="b3d72-115">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="b3d72-115">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="b3d72-116">Identificador de evento para el siguiente evento programado para ejecutarse en la pista especificada. Se devuelve **null** si no hay ningún evento nuevo programado.</span><span class="sxs-lookup"><span data-stu-id="b3d72-116">Event handle to the next event scheduled to run on the specified track. **NULL** is returned if no new event is scheduled.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3d72-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3d72-117">Remarks</span></span>

<span data-ttu-id="b3d72-118">Este método se puede usar de forma iterativa para buscar un evento deseado pasando de manera repetida **null** para hEvent.</span><span class="sxs-lookup"><span data-stu-id="b3d72-118">This method can be used iteratively to locate a desired event by repeatedly passing in **NULL** for hEvent.</span></span>

> [!Note]  
> <span data-ttu-id="b3d72-119">No itere más después de que el método devuelva **null**.</span><span class="sxs-lookup"><span data-stu-id="b3d72-119">Do not iterate further after the method has returned **NULL**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b3d72-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3d72-120">Requirements</span></span>



| <span data-ttu-id="b3d72-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3d72-121">Requirement</span></span> | <span data-ttu-id="b3d72-122">Value</span><span class="sxs-lookup"><span data-stu-id="b3d72-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3d72-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3d72-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b3d72-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3d72-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="b3d72-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3d72-125">Library</span></span><br/> | <dl> <span data-ttu-id="b3d72-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3d72-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b3d72-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3d72-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3d72-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="b3d72-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
