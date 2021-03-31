---
description: Se produce después de eliminar los trazos de la propiedad de entrada manuscrita.
ms.assetid: 60ee8bbd-9230-4b6a-a4b0-4783195e3173
title: Evento InkOverlay. StrokesDeleted (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc37b0de7f86f7d2b68df7074a0f3bb6c9e075e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277218"
---
# <a name="inkoverlaystrokesdeleted-event"></a><span data-ttu-id="ce521-103">Evento InkOverlay. StrokesDeleted</span><span class="sxs-lookup"><span data-stu-id="ce521-103">InkOverlay.StrokesDeleted event</span></span>

<span data-ttu-id="ce521-104">Se produce después de eliminar los trazos de la propiedad de [**entrada manuscrita**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .</span><span class="sxs-lookup"><span data-stu-id="ce521-104">Occurs after strokes have been deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce521-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce521-105">Syntax</span></span>


```C++
void StrokesDeleted();
```



## <a name="parameters"></a><span data-ttu-id="ce521-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce521-106">Parameters</span></span>

<span data-ttu-id="ce521-107">Este evento no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ce521-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ce521-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce521-108">Return value</span></span>

<span data-ttu-id="ce521-109">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="ce521-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce521-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce521-110">Remarks</span></span>

<span data-ttu-id="ce521-111">No hay datos de evento.</span><span class="sxs-lookup"><span data-stu-id="ce521-111">There is no event data.</span></span>

<span data-ttu-id="ce521-112">Este método de evento se define en las \_ \_ interfaces de solo envío IInkOverlayEvents y IInkPictureEvents (dispinterfaces) con un identificador de DISPID \_ IOEStrokesDeleted.</span><span class="sxs-lookup"><span data-stu-id="ce521-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce521-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce521-113">Requirements</span></span>



| <span data-ttu-id="ce521-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce521-114">Requirement</span></span> | <span data-ttu-id="ce521-115">Value</span><span class="sxs-lookup"><span data-stu-id="ce521-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce521-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce521-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ce521-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ce521-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ce521-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce521-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ce521-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ce521-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ce521-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce521-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce521-121"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ce521-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ce521-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce521-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="ce521-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce521-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ce521-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce521-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce521-125">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="ce521-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="ce521-126">[**Propiedad de entrada manuscrita \[ InkCollector/InkOverLay (clase)\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span><span class="sxs-lookup"><span data-stu-id="ce521-126">[**Ink Property \[InkCollector/InkOverLay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span></span>
</dt> </dl>

 

 




