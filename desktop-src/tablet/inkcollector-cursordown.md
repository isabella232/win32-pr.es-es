---
description: 'Evento InkCollector.CursorDown: se produce cuando la punta del cursor se pone en contacto con la superficie digitalizadora de la tableta.'
ms.assetid: bf914849-ef33-4746-b2e1-c768cd1d87aa
title: Evento InkCollector.CursorDown (Msplaceut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0cdb729f36706202fad2c6c03ab8031e90c845
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110303"
---
# <a name="inkcollectorcursordown-event"></a><span data-ttu-id="9f17b-103">Evento InkCollector.CursorDown</span><span class="sxs-lookup"><span data-stu-id="9f17b-103">InkCollector.CursorDown event</span></span>

<span data-ttu-id="9f17b-104">Se produce cuando la punta del cursor se pone en contacto con la superficie digitalizadora de la tableta.</span><span class="sxs-lookup"><span data-stu-id="9f17b-104">Occurs when the cursor tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f17b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f17b-105">Syntax</span></span>


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a><span data-ttu-id="9f17b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f17b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f17b-107">*Cursor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9f17b-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f17b-108">Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento CursorDown.**</span><span class="sxs-lookup"><span data-stu-id="9f17b-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="9f17b-109">*Trazo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9f17b-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f17b-110">Objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que se inició cuando el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) hizo que se iniciara el evento **CursorDown.**</span><span class="sxs-lookup"><span data-stu-id="9f17b-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that was started when the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object caused the **CursorDown** event to fire.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f17b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f17b-111">Return value</span></span>

<span data-ttu-id="9f17b-112">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="9f17b-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f17b-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9f17b-113">Remarks</span></span>

<span data-ttu-id="9f17b-114">Este método de evento se define en \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents.</span><span class="sxs-lookup"><span data-stu-id="9f17b-114">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents.</span></span> <span data-ttu-id="9f17b-115">Las \_ interfaces IInkCollectorEvents, \_ IInkOverlayEvents e IInkPictureEvents implementan la interfaz IDispatch con un identificador \_ [](/windows/win32/api/oaidl/nn-oaidl-idispatch) \_ DEPID ICECursorDown.</span><span class="sxs-lookup"><span data-stu-id="9f17b-115">the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents interfaces implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_ICECursorDown.</span></span>

<span data-ttu-id="9f17b-116">Use este evento con cuidado porque podría tener un efecto adverso en el rendimiento de la entrada de lápiz si se ejecuta demasiado código en los controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="9f17b-116">Use this event carefully because it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span> <span data-ttu-id="9f17b-117">Para mejorar el rendimiento de la entrada de lápiz en tiempo real, oculte o muestre el cursor del mouse en los controladores de eventos [**MouseDown**](inkcollector-mousedown.md) y [**MouseUp.**](inkcollector-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="9f17b-117">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f17b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f17b-118">Requirements</span></span>



| <span data-ttu-id="9f17b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f17b-119">Requirement</span></span> | <span data-ttu-id="9f17b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9f17b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f17b-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f17b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9f17b-122">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="9f17b-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9f17b-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f17b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9f17b-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9f17b-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="9f17b-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f17b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f17b-126"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="9f17b-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9f17b-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f17b-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f17b-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f17b-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="9f17b-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9f17b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f17b-130">**InkCollector (clase)**</span><span class="sxs-lookup"><span data-stu-id="9f17b-130">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="9f17b-131">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="9f17b-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="9f17b-132">**Evento CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="9f17b-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="9f17b-133">**IInkCursor (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="9f17b-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="9f17b-134">**IInkStrokeDisp (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="9f17b-134">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

