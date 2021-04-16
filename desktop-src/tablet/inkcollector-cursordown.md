---
description: Se produce cuando la sugerencia del cursor se pone en contacto con la superficie de la tableta de la digitalización.
ms.assetid: bf914849-ef33-4746-b2e1-c768cd1d87aa
title: InkCollector. CursorDown evento (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fd009c5f42e6a26cdaf493e97532be7716381c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705554"
---
# <a name="inkcollectorcursordown-event"></a><span data-ttu-id="1b69c-103">InkCollector. CursorDown, evento</span><span class="sxs-lookup"><span data-stu-id="1b69c-103">InkCollector.CursorDown event</span></span>

<span data-ttu-id="1b69c-104">Se produce cuando la sugerencia del cursor se pone en contacto con la superficie de la tableta de la digitalización.</span><span class="sxs-lookup"><span data-stu-id="1b69c-104">Occurs when the cursor tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b69c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b69c-105">Syntax</span></span>


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a><span data-ttu-id="1b69c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b69c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b69c-107">*Cursor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1b69c-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b69c-108">El objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento **CursorDown** .</span><span class="sxs-lookup"><span data-stu-id="1b69c-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="1b69c-109">*Trazo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1b69c-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b69c-110">El objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que se inició cuando el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) provocó que se activara el evento **CursorDown** .</span><span class="sxs-lookup"><span data-stu-id="1b69c-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that was started when the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object caused the **CursorDown** event to fire.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b69c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b69c-111">Return value</span></span>

<span data-ttu-id="1b69c-112">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="1b69c-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b69c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b69c-113">Remarks</span></span>

<span data-ttu-id="1b69c-114">Este método de evento se define en \_ IInkCollectorEvents, \_ IInkOverlayEvents y \_ IInkPictureEvents.</span><span class="sxs-lookup"><span data-stu-id="1b69c-114">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents.</span></span> <span data-ttu-id="1b69c-115">las \_ interfaces IInkCollectorEvents, \_ IInkOverlayEvents y \_ IInkPictureEvents implementan la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ ICECursorDown.</span><span class="sxs-lookup"><span data-stu-id="1b69c-115">the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents interfaces implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_ICECursorDown.</span></span>

<span data-ttu-id="1b69c-116">Utilice este evento con precaución, ya que podría tener un efecto adverso en el rendimiento de las entradas manuscritas si se ejecuta demasiado código en los controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="1b69c-116">Use this event carefully because it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span> <span data-ttu-id="1b69c-117">Para mejorar el rendimiento del lápiz en tiempo real, oculte o muestre el cursor del mouse en los controladores de eventos [**MouseDown**](inkcollector-mousedown.md) y [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="1b69c-117">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b69c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b69c-118">Requirements</span></span>



| <span data-ttu-id="1b69c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b69c-119">Requirement</span></span> | <span data-ttu-id="1b69c-120">Value</span><span class="sxs-lookup"><span data-stu-id="1b69c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b69c-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b69c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1b69c-122">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1b69c-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1b69c-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b69c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1b69c-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1b69c-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1b69c-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b69c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b69c-126"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1b69c-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1b69c-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1b69c-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="1b69c-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b69c-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="1b69c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b69c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b69c-130">**InkCollector (clase)**</span><span class="sxs-lookup"><span data-stu-id="1b69c-130">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="1b69c-131">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="1b69c-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="1b69c-132">**Evento CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="1b69c-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="1b69c-133">**Interfaz IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="1b69c-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="1b69c-134">**Interfaz IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="1b69c-134">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

