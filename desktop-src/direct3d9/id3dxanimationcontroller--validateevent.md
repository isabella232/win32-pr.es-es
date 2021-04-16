---
description: Comprueba si un identificador de evento especificado es válido y el evento de animación no se ha completado todavía.
ms.assetid: 242ad1e2-4b04-4ce1-9cdf-f66da9f83f06
title: 'ID3DXAnimationController:: ValidateEvent (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ValidateEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e1a632fa867269f04e8f5f66e6bc352ef1701cd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649461"
---
# <a name="id3dxanimationcontrollervalidateevent-method"></a><span data-ttu-id="9129f-103">ID3DXAnimationController:: ValidateEvent (método)</span><span class="sxs-lookup"><span data-stu-id="9129f-103">ID3DXAnimationController::ValidateEvent method</span></span>

<span data-ttu-id="9129f-104">Comprueba si un identificador de evento especificado es válido y el evento de animación no se ha completado todavía.</span><span class="sxs-lookup"><span data-stu-id="9129f-104">Checks whether a specified event handle is valid and the animation event has not yet completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9129f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9129f-105">Syntax</span></span>


```C++
HRESULT ValidateEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="9129f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9129f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9129f-107">*hEvent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9129f-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9129f-108">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="9129f-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="9129f-109">Identificador de evento de un evento de animación.</span><span class="sxs-lookup"><span data-stu-id="9129f-109">Event handle to an animation event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9129f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9129f-110">Return value</span></span>

<span data-ttu-id="9129f-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9129f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9129f-112">Devuelve S \_ OK si el identificador de evento es válido y el evento aún no se ha completado.</span><span class="sxs-lookup"><span data-stu-id="9129f-112">Returns S\_OK if the event handle is valid and the event has not yet completed.</span></span>

<span data-ttu-id="9129f-113">Devuelve E \_ produce un error si el identificador de evento no es válido y/o se ha completado el evento.</span><span class="sxs-lookup"><span data-stu-id="9129f-113">Returns E\_FAIL if the event handle is invalid and/or the event has completed.</span></span>

## <a name="remarks"></a><span data-ttu-id="9129f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9129f-114">Remarks</span></span>

<span data-ttu-id="9129f-115">El método indicará que un identificador de evento es válido aunque el evento se esté ejecutando pero aún no se haya completado.</span><span class="sxs-lookup"><span data-stu-id="9129f-115">The method will indicate that an event handle is valid even if the event is running but has not yet completed.</span></span>

## <a name="requirements"></a><span data-ttu-id="9129f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9129f-116">Requirements</span></span>



| <span data-ttu-id="9129f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9129f-117">Requirement</span></span> | <span data-ttu-id="9129f-118">Value</span><span class="sxs-lookup"><span data-stu-id="9129f-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9129f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9129f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="9129f-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="9129f-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="9129f-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9129f-121">Library</span></span><br/> | <dl> <span data-ttu-id="9129f-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9129f-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9129f-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="9129f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9129f-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="9129f-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




