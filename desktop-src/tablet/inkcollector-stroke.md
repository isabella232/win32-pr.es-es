---
description: 'Evento InkCollector.Stroke: se produce cuando el usuario dibuja un nuevo trazo en cualquier tableta.'
ms.assetid: eaa89dfe-6141-4205-845b-634321130e26
title: Evento InkCollector.Stroke (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49cb90b02ab3fca60a8fa17089b6a76f959a60e0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110063"
---
# <a name="inkcollectorstroke-event"></a><span data-ttu-id="e18e1-103">Evento InkCollector.Stroke</span><span class="sxs-lookup"><span data-stu-id="e18e1-103">InkCollector.Stroke event</span></span>

<span data-ttu-id="e18e1-104">Se produce cuando el usuario dibuja un nuevo trazo en cualquier tableta.</span><span class="sxs-lookup"><span data-stu-id="e18e1-104">Occurs when the user draws a new stroke on any tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="e18e1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e18e1-105">Syntax</span></span>


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="e18e1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e18e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e18e1-107">*Cursor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e18e1-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e18e1-108">Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento Stroke.**</span><span class="sxs-lookup"><span data-stu-id="e18e1-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Stroke** event.</span></span>

</dd> <dt>

<span data-ttu-id="e18e1-109">*Trazo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e18e1-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e18e1-110">Objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) recopilado.</span><span class="sxs-lookup"><span data-stu-id="e18e1-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="e18e1-111">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e18e1-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e18e1-112">**VARIANT \_ TRUE** para cancelar el evento; de lo contrario, **VARIANT \_ FALSE**.</span><span class="sxs-lookup"><span data-stu-id="e18e1-112">**VARIANT\_TRUE** to cancel the event; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e18e1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e18e1-113">Return value</span></span>

<span data-ttu-id="e18e1-114">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="e18e1-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e18e1-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e18e1-115">Remarks</span></span>

<span data-ttu-id="e18e1-116">Este método de evento se define en las interfaces de solo distribución \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ DE DISPID \_ ICEStroke.</span><span class="sxs-lookup"><span data-stu-id="e18e1-116">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEStroke.</span></span>

<span data-ttu-id="e18e1-117">El **evento Stroke** se desencadena cuando se está en modo de selección o borrado, no solo al insertar la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="e18e1-117">The **Stroke** event is fired when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="e18e1-118">Esto requiere que supervise el modo de edición (del que es responsable de la configuración) y que tenga en cuenta el modo antes de interpretar el evento.</span><span class="sxs-lookup"><span data-stu-id="e18e1-118">This requires that you monitor the editing mode (which you are responsible for setting) and are aware of the mode before interpreting the event.</span></span> <span data-ttu-id="e18e1-119">La ventaja de este requisito es una mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="e18e1-119">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

> [!Note]  
> <span data-ttu-id="e18e1-120">El **evento Stroke** se produce cuando el usuario termina de dibujar un trazo, no cuando se agrega un trazo a la colección [InkStrokes.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e18e1-120">The **Stroke** event fires when the user finishes drawing a stroke, not when a stroke is added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span> <span data-ttu-id="e18e1-121">Cuando el usuario empieza a dibujar por primera vez un trazo, se agrega inmediatamente a la colección InkStrokes; sin embargo, **el evento Stroke** no se produce hasta que se completa el trazo.</span><span class="sxs-lookup"><span data-stu-id="e18e1-121">When the user first starts to draw a stroke, it is added immediately to the InkStrokes collection; however, the **Stroke** event does not fire until the stroke is complete.</span></span> <span data-ttu-id="e18e1-122">Por lo tanto, pueden existir trazos en la colección InkStrokes que el **controlador de** eventos Stroke no ha visto.</span><span class="sxs-lookup"><span data-stu-id="e18e1-122">Therefore, strokes can exist in the InkStrokes collection that the **Stroke** event handler has not seen.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e18e1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e18e1-123">Requirements</span></span>



| <span data-ttu-id="e18e1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e18e1-124">Requirement</span></span> | <span data-ttu-id="e18e1-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e18e1-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e18e1-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e18e1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e18e1-127">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="e18e1-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e18e1-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e18e1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e18e1-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e18e1-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e18e1-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e18e1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e18e1-131"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="e18e1-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e18e1-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e18e1-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="e18e1-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e18e1-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e18e1-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e18e1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e18e1-135">**InkCollector (clase)**</span><span class="sxs-lookup"><span data-stu-id="e18e1-135">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

<span data-ttu-id="e18e1-136">[**Colección StrokesAdded Event \[ InkStrokes\]**](inkstrokes-strokesadded.md)</span><span class="sxs-lookup"><span data-stu-id="e18e1-136">[**StrokesAdded Event \[InkStrokes Collection\]**](inkstrokes-strokesadded.md)</span></span>
</dt> <dt>

<span data-ttu-id="e18e1-137">[**StrokesDeleted \[ (clase InkOverlay)\]**](inkoverlay-strokesdeleted.md)</span><span class="sxs-lookup"><span data-stu-id="e18e1-137">[**StrokesDeleted Event \[InkOverlay Class\]**](inkoverlay-strokesdeleted.md)</span></span>
</dt> <dt>

[<span data-ttu-id="e18e1-138">**IInkCursor (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="e18e1-138">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="e18e1-139">**IInkStrokeDisp (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="e18e1-139">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

