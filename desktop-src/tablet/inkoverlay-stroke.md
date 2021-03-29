---
description: Se produce cuando el usuario dibuja un nuevo trazo en cualquier tableta.
ms.assetid: 315155ec-0de1-4052-ae7c-51bc3127fbbf
title: Evento InkOverlay. Stroke (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6db3bdbe996830596a8e25cebf6f05b94638894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817731"
---
# <a name="inkoverlaystroke-event"></a><span data-ttu-id="792bf-103">Evento InkOverlay. Stroke</span><span class="sxs-lookup"><span data-stu-id="792bf-103">InkOverlay.Stroke event</span></span>

<span data-ttu-id="792bf-104">Se produce cuando el usuario dibuja un nuevo trazo en cualquier tableta.</span><span class="sxs-lookup"><span data-stu-id="792bf-104">Occurs when the user draws a new stroke on any tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="792bf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="792bf-105">Syntax</span></span>


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="792bf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="792bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="792bf-107">*Cursor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="792bf-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="792bf-108">El objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento [**Stroke**](inkcollector-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="792bf-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**Stroke**](inkcollector-stroke.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="792bf-109">*Trazo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="792bf-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="792bf-110">Objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) recopilado.</span><span class="sxs-lookup"><span data-stu-id="792bf-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="792bf-111">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="792bf-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="792bf-112">Especifica si se debe cancelar el evento.</span><span class="sxs-lookup"><span data-stu-id="792bf-112">Specifies whether the event should be canceled.</span></span> <span data-ttu-id="792bf-113">Si es **true**, se cancela la colección del trazo.</span><span class="sxs-lookup"><span data-stu-id="792bf-113">If **TRUE**, the collection of the stroke is canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="792bf-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="792bf-114">Return value</span></span>

<span data-ttu-id="792bf-115">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="792bf-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="792bf-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="792bf-116">Remarks</span></span>

<span data-ttu-id="792bf-117">Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ ICEStroke.</span><span class="sxs-lookup"><span data-stu-id="792bf-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEStroke.</span></span>

<span data-ttu-id="792bf-118">El evento [**Stroke**](inkcollector-stroke.md) se desencadena cuando se está en modo de selección o borrado, no solo cuando se inserta una entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="792bf-118">The [**Stroke**](inkcollector-stroke.md) event is fired when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="792bf-119">Esto requiere que supervise el modo de edición (que es responsable de establecer) y que sea consciente del modo antes de interpretar el evento.</span><span class="sxs-lookup"><span data-stu-id="792bf-119">This requires that you monitor the editing mode (which you are responsible for setting) and are aware of the mode before interpreting the event.</span></span> <span data-ttu-id="792bf-120">La ventaja de este requisito es mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de plataforma.</span><span class="sxs-lookup"><span data-stu-id="792bf-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

> [!Note]  
> <span data-ttu-id="792bf-121">El evento [**Stroke**](inkcollector-stroke.md) se activa cuando el usuario termina de dibujar un trazo, no cuando se agrega un trazo a la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="792bf-121">The [**Stroke**](inkcollector-stroke.md) event fires when the user finishes drawing a stroke, not when a stroke is added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span> <span data-ttu-id="792bf-122">Cuando el usuario comienza a dibujar un trazo por primera vez, se agrega inmediatamente a la colección InkStrokes; sin embargo, el evento **Stroke** no se activa hasta que se completa el trazo.</span><span class="sxs-lookup"><span data-stu-id="792bf-122">When the user first starts to draw a stroke, it is added immediately to the InkStrokes collection; however, the **Stroke** event does not fire until the stroke is complete.</span></span> <span data-ttu-id="792bf-123">Por lo tanto, los trazos pueden existir en la colección InkStrokes que el controlador de eventos **Stroke** no ha encontrado.</span><span class="sxs-lookup"><span data-stu-id="792bf-123">Therefore, strokes can exist in the InkStrokes collection that the **Stroke** event handler has not seen.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="792bf-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="792bf-124">Requirements</span></span>



| <span data-ttu-id="792bf-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="792bf-125">Requirement</span></span> | <span data-ttu-id="792bf-126">Value</span><span class="sxs-lookup"><span data-stu-id="792bf-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="792bf-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="792bf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="792bf-128">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="792bf-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="792bf-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="792bf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="792bf-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="792bf-130">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="792bf-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="792bf-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="792bf-132"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="792bf-132"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="792bf-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="792bf-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="792bf-134"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="792bf-134"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="792bf-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="792bf-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="792bf-136">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="792bf-136">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="792bf-137">[**Colección InkStrokes de eventos StrokesAdded \[\]**](inkstrokes-strokesadded.md)</span><span class="sxs-lookup"><span data-stu-id="792bf-137">[**StrokesAdded Event \[InkStrokes Collection\]**](inkstrokes-strokesadded.md)</span></span>
</dt> <dt>

<span data-ttu-id="792bf-138">[**StrokesDeleted Event \[ InkOverlay (clase)\]**](inkoverlay-strokesdeleted.md)</span><span class="sxs-lookup"><span data-stu-id="792bf-138">[**StrokesDeleted Event \[InkOverlay Class\]**](inkoverlay-strokesdeleted.md)</span></span>
</dt> <dt>

[<span data-ttu-id="792bf-139">**Interfaz IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="792bf-139">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="792bf-140">**Interfaz IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="792bf-140">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

