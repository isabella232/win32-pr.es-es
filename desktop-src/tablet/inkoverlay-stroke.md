---
description: 'Evento InkOverlay.Stroke: se produce cuando el usuario dibuja un nuevo trazo en cualquier tableta.'
ms.assetid: 315155ec-0de1-4052-ae7c-51bc3127fbbf
title: Evento InkOverlay.Stroke (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 408c44cf47ecfbf3ea0cfd0f8306be61efb0f8e9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116853"
---
# <a name="inkoverlaystroke-event"></a><span data-ttu-id="ee0dc-103">Evento InkOverlay.Stroke</span><span class="sxs-lookup"><span data-stu-id="ee0dc-103">InkOverlay.Stroke event</span></span>

<span data-ttu-id="ee0dc-104">Se produce cuando el usuario dibuja un nuevo trazo en cualquier tableta.</span><span class="sxs-lookup"><span data-stu-id="ee0dc-104">Occurs when the user draws a new stroke on any tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee0dc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee0dc-105">Syntax</span></span>


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="ee0dc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee0dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee0dc-107">*Cursor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ee0dc-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee0dc-108">Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el [**evento Stroke.**](inkcollector-stroke.md)</span><span class="sxs-lookup"><span data-stu-id="ee0dc-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**Stroke**](inkcollector-stroke.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="ee0dc-109">*Trazo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ee0dc-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee0dc-110">Objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) recopilado.</span><span class="sxs-lookup"><span data-stu-id="ee0dc-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="ee0dc-111">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ee0dc-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee0dc-112">Especifica si se debe cancelar el evento.</span><span class="sxs-lookup"><span data-stu-id="ee0dc-112">Specifies whether the event should be canceled.</span></span> <span data-ttu-id="ee0dc-113">Si **es TRUE**, se cancela la colección del trazo.</span><span class="sxs-lookup"><span data-stu-id="ee0dc-113">If **TRUE**, the collection of the stroke is canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee0dc-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee0dc-114">Return value</span></span>

<span data-ttu-id="ee0dc-115">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="ee0dc-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee0dc-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ee0dc-116">Remarks</span></span>

<span data-ttu-id="ee0dc-117">Este método de evento se define en las interfaces de solo distribución \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ DE DISPID \_ ICEStroke.</span><span class="sxs-lookup"><span data-stu-id="ee0dc-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEStroke.</span></span>

<span data-ttu-id="ee0dc-118">El [**evento Stroke**](inkcollector-stroke.md) se desencadena cuando se está en modo de selección o borrado, no solo al insertar la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="ee0dc-118">The [**Stroke**](inkcollector-stroke.md) event is fired when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="ee0dc-119">Esto requiere que supervise el modo de edición (del que es responsable de la configuración) y que tenga en cuenta el modo antes de interpretar el evento.</span><span class="sxs-lookup"><span data-stu-id="ee0dc-119">This requires that you monitor the editing mode (which you are responsible for setting) and are aware of the mode before interpreting the event.</span></span> <span data-ttu-id="ee0dc-120">La ventaja de este requisito es una mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="ee0dc-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

> [!Note]  
> <span data-ttu-id="ee0dc-121">El [**evento Stroke**](inkcollector-stroke.md) se produce cuando el usuario termina de dibujar un trazo, no cuando se agrega un trazo a la colección [InkStrokes.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ee0dc-121">The [**Stroke**](inkcollector-stroke.md) event fires when the user finishes drawing a stroke, not when a stroke is added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span> <span data-ttu-id="ee0dc-122">Cuando el usuario empieza a dibujar por primera vez un trazo, se agrega inmediatamente a la colección InkStrokes; sin embargo, **el evento Stroke** no se produce hasta que se completa el trazo.</span><span class="sxs-lookup"><span data-stu-id="ee0dc-122">When the user first starts to draw a stroke, it is added immediately to the InkStrokes collection; however, the **Stroke** event does not fire until the stroke is complete.</span></span> <span data-ttu-id="ee0dc-123">Por lo tanto, pueden existir trazos en la colección InkStrokes que el **controlador de** eventos Stroke no ha visto.</span><span class="sxs-lookup"><span data-stu-id="ee0dc-123">Therefore, strokes can exist in the InkStrokes collection that the **Stroke** event handler has not seen.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ee0dc-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee0dc-124">Requirements</span></span>



| <span data-ttu-id="ee0dc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee0dc-125">Requirement</span></span> | <span data-ttu-id="ee0dc-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ee0dc-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee0dc-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee0dc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ee0dc-128">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="ee0dc-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ee0dc-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee0dc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ee0dc-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ee0dc-130">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ee0dc-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee0dc-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee0dc-132"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="ee0dc-132"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ee0dc-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee0dc-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="ee0dc-134"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee0dc-134"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ee0dc-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ee0dc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee0dc-136">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="ee0dc-136">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="ee0dc-137">[**Colección StrokesAdded Event \[ InkStrokes\]**](inkstrokes-strokesadded.md)</span><span class="sxs-lookup"><span data-stu-id="ee0dc-137">[**StrokesAdded Event \[InkStrokes Collection\]**](inkstrokes-strokesadded.md)</span></span>
</dt> <dt>

<span data-ttu-id="ee0dc-138">[**StrokesDeleted \[ (clase InkOverlay)\]**](inkoverlay-strokesdeleted.md)</span><span class="sxs-lookup"><span data-stu-id="ee0dc-138">[**StrokesDeleted Event \[InkOverlay Class\]**](inkoverlay-strokesdeleted.md)</span></span>
</dt> <dt>

[<span data-ttu-id="ee0dc-139">**IInkCursor (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="ee0dc-139">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="ee0dc-140">**IInkStrokeDisp (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="ee0dc-140">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

