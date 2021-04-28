---
description: 'Evento InkPicture.Stroke: se produce cuando el usuario dibuja un nuevo trazo en cualquier tableta.'
ms.assetid: 2829b65a-6120-402e-91e3-5587d1f456f9
title: Evento InkPicture.Stroke (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b181c8dc46348c76bd9c2d015d4a97c1f6911ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113703"
---
# <a name="inkpicturestroke-event"></a><span data-ttu-id="d8261-103">Evento InkPicture.Stroke</span><span class="sxs-lookup"><span data-stu-id="d8261-103">InkPicture.Stroke event</span></span>

<span data-ttu-id="d8261-104">Se produce cuando el usuario dibuja un nuevo trazo en cualquier tableta.</span><span class="sxs-lookup"><span data-stu-id="d8261-104">Occurs when the user draws a new stroke on any tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8261-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8261-105">Syntax</span></span>


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="d8261-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8261-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8261-107">*Cursor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d8261-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8261-108">Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento Stroke.**</span><span class="sxs-lookup"><span data-stu-id="d8261-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Stroke** event.</span></span>

</dd> <dt>

<span data-ttu-id="d8261-109">*Trazo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d8261-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8261-110">Objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) recopilado.</span><span class="sxs-lookup"><span data-stu-id="d8261-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="d8261-111">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d8261-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8261-112">**VARIANT \_ TRUE** para cancelar la colección del trazo; en caso contrario, **VARIANT \_ FALSE**.</span><span class="sxs-lookup"><span data-stu-id="d8261-112">**VARIANT\_TRUE** to cancel the collection of the stroke; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8261-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8261-113">Return value</span></span>

<span data-ttu-id="d8261-114">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="d8261-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8261-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d8261-115">Remarks</span></span>

<span data-ttu-id="d8261-116">Este método de evento se define en las interfaces de solo distribución (dispinterfaces) de **\_ IInkCollectorEvents,** **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** con un identificador DE DISPID \_ ICEStroke.</span><span class="sxs-lookup"><span data-stu-id="d8261-116">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEStroke.</span></span>

<span data-ttu-id="d8261-117">El **evento Stroke** tiene lugar cuando se está en modo de selección o borrado, no solo al insertar la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="d8261-117">The **Stroke** event occurs when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="d8261-118">Esto requiere que supervise el modo de edición (del que es responsable de la configuración) y que tenga en cuenta el modo antes de interpretar el evento.</span><span class="sxs-lookup"><span data-stu-id="d8261-118">This requires that you monitor the editing mode (which you are responsible for setting) and are aware of the mode before interpreting the event.</span></span> <span data-ttu-id="d8261-119">La ventaja de este requisito es una mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="d8261-119">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

> [!Note]  
> <span data-ttu-id="d8261-120">El **evento Stroke** tiene lugar cuando el usuario termina de dibujar un trazo, no cuando se agrega un trazo a la colección [InkStrokes.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d8261-120">The **Stroke** event occurs when the user finishes drawing a stroke, not when a stroke is added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span> <span data-ttu-id="d8261-121">Cuando el usuario empieza a dibujar por primera vez un trazo, se agrega inmediatamente a la colección InkStrokes; sin embargo, el **evento Stroke** no se produce hasta que se completa el trazo.</span><span class="sxs-lookup"><span data-stu-id="d8261-121">When the user first starts to draw a stroke, it is added immediately to the InkStrokes collection; however, the **Stroke** event does not occur until the stroke is complete.</span></span> <span data-ttu-id="d8261-122">Por lo tanto, pueden existir trazos en la colección InkStrokes que el **controlador de** eventos Stroke no ha visto.</span><span class="sxs-lookup"><span data-stu-id="d8261-122">Therefore, strokes can exist in the InkStrokes collection that the **Stroke** event handler has not seen.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d8261-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8261-123">Requirements</span></span>



| <span data-ttu-id="d8261-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8261-124">Requirement</span></span> | <span data-ttu-id="d8261-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d8261-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8261-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8261-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d8261-127">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="d8261-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d8261-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8261-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d8261-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d8261-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d8261-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8261-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8261-131"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="d8261-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d8261-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8261-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="d8261-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8261-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d8261-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d8261-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8261-135">InkPicture</span><span class="sxs-lookup"><span data-stu-id="d8261-135">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="d8261-136">[**StrokesAdded Event \[ InkPicture Control\]**](inkpicture-strokesadded.md)</span><span class="sxs-lookup"><span data-stu-id="d8261-136">[**StrokesAdded Event \[InkPicture Control\]**](inkpicture-strokesadded.md)</span></span>
</dt> <dt>

<span data-ttu-id="d8261-137">[**StrokesDeleted Event \[ InkPicture (Control InkPicture)\]**](inkpicture-strokesdeleted.md)</span><span class="sxs-lookup"><span data-stu-id="d8261-137">[**StrokesDeleted Event \[InkPicture Control\]**](inkpicture-strokesdeleted.md)</span></span>
</dt> <dt>

[<span data-ttu-id="d8261-138">**IInkCursor (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="d8261-138">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="d8261-139">**IInkStrokeDisp (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="d8261-139">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

