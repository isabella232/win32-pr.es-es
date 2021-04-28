---
description: 'Evento InkOverlay.CursorDown: se produce cuando la punta del cursor se pone en contacto con la superficie digitalizadora de la tableta.'
ms.assetid: 753aa733-8d62-4983-b76d-d58844b79c35
title: Evento InkOverlay.CursorDown (Msplaceut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ed26c672aadc9fa19f6a6426fed7339752448d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117063"
---
# <a name="inkoverlaycursordown-event"></a><span data-ttu-id="d4c11-103">Evento InkOverlay.CursorDown</span><span class="sxs-lookup"><span data-stu-id="d4c11-103">InkOverlay.CursorDown event</span></span>

<span data-ttu-id="d4c11-104">Se produce cuando la punta del cursor se pone en contacto con la superficie digitalizadora de la tableta.</span><span class="sxs-lookup"><span data-stu-id="d4c11-104">Occurs when the cursor tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4c11-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4c11-105">Syntax</span></span>


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a><span data-ttu-id="d4c11-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4c11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4c11-107">*Cursor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d4c11-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4c11-108">Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el [**evento CursorDown.**](inkcollector-cursordown.md)</span><span class="sxs-lookup"><span data-stu-id="d4c11-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorDown**](inkcollector-cursordown.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="d4c11-109">*Trazo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d4c11-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4c11-110">Objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que se inició cuando el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) hizo que se iniciara el evento [**CursorDown.**](inkcollector-cursordown.md)</span><span class="sxs-lookup"><span data-stu-id="d4c11-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that was started when the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object caused the [**CursorDown**](inkcollector-cursordown.md) event to fire.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4c11-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4c11-111">Return value</span></span>

<span data-ttu-id="d4c11-112">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="d4c11-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4c11-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d4c11-113">Remarks</span></span>

<span data-ttu-id="d4c11-114">Este método de evento se define en \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents.</span><span class="sxs-lookup"><span data-stu-id="d4c11-114">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents.</span></span> <span data-ttu-id="d4c11-115">Las \_ interfaces IInkCollectorEvents, \_ IInkOverlayEvents e IInkPictureEvents implementan la interfaz IDispatch con un identificador \_ [](/windows/win32/api/oaidl/nn-oaidl-idispatch) \_ DEPID ICECursorDown.</span><span class="sxs-lookup"><span data-stu-id="d4c11-115">the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents interfaces implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_ICECursorDown.</span></span>

<span data-ttu-id="d4c11-116">Use este evento con cuidado porque podría tener un efecto adverso en el rendimiento de la entrada de lápiz si se ejecuta demasiado código en los controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="d4c11-116">Use this event carefully because it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span> <span data-ttu-id="d4c11-117">Para mejorar el rendimiento de la entrada de lápiz en tiempo real, oculte o muestre el cursor del mouse en los controladores de eventos [**MouseDown**](inkcollector-mousedown.md) y [**MouseUp.**](inkcollector-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="d4c11-117">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4c11-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4c11-118">Requirements</span></span>



| <span data-ttu-id="d4c11-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4c11-119">Requirement</span></span> | <span data-ttu-id="d4c11-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d4c11-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4c11-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4c11-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d4c11-122">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="d4c11-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d4c11-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4c11-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d4c11-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d4c11-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d4c11-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4c11-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4c11-126"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="d4c11-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d4c11-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d4c11-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="d4c11-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4c11-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d4c11-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d4c11-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4c11-130">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="d4c11-130">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="d4c11-131">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="d4c11-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="d4c11-132">**Evento CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="d4c11-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="d4c11-133">**IInkCursor (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="d4c11-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="d4c11-134">**IInkStrokeDisp (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="d4c11-134">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

