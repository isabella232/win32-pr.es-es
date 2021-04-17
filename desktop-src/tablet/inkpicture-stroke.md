---
description: Se produce cuando el usuario dibuja un nuevo trazo en cualquier tableta.
ms.assetid: 2829b65a-6120-402e-91e3-5587d1f456f9
title: Evento InkPicture. Stroke (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b85d2410141c2d6d5f7ae92408b7d6da49a447f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716912"
---
# <a name="inkpicturestroke-event"></a><span data-ttu-id="e4480-103">Evento InkPicture. Stroke</span><span class="sxs-lookup"><span data-stu-id="e4480-103">InkPicture.Stroke event</span></span>

<span data-ttu-id="e4480-104">Se produce cuando el usuario dibuja un nuevo trazo en cualquier tableta.</span><span class="sxs-lookup"><span data-stu-id="e4480-104">Occurs when the user draws a new stroke on any tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4480-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e4480-105">Syntax</span></span>


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="e4480-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4480-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4480-107">*Cursor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e4480-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4480-108">El objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="e4480-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Stroke** event.</span></span>

</dd> <dt>

<span data-ttu-id="e4480-109">*Trazo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e4480-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4480-110">Objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) recopilado.</span><span class="sxs-lookup"><span data-stu-id="e4480-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="e4480-111">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e4480-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4480-112">**Variante \_ TRUE** para cancelar la colección del trazo; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="e4480-112">**VARIANT\_TRUE** to cancel the collection of the stroke; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4480-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e4480-113">Return value</span></span>

<span data-ttu-id="e4480-114">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="e4480-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4480-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e4480-115">Remarks</span></span>

<span data-ttu-id="e4480-116">Este método de evento se define en las interfaces de solo distribución (dispinterfaces) **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** con el identificador DISPID \_ ICEStroke.</span><span class="sxs-lookup"><span data-stu-id="e4480-116">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEStroke.</span></span>

<span data-ttu-id="e4480-117">El evento **Stroke** tiene lugar cuando se está en modo de selección o borrado, no solo cuando se inserta una entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="e4480-117">The **Stroke** event occurs when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="e4480-118">Esto requiere que supervise el modo de edición (que es responsable de establecer) y que sea consciente del modo antes de interpretar el evento.</span><span class="sxs-lookup"><span data-stu-id="e4480-118">This requires that you monitor the editing mode (which you are responsible for setting) and are aware of the mode before interpreting the event.</span></span> <span data-ttu-id="e4480-119">La ventaja de este requisito es mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de plataforma.</span><span class="sxs-lookup"><span data-stu-id="e4480-119">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

> [!Note]  
> <span data-ttu-id="e4480-120">El evento **Stroke** se produce cuando el usuario termina de dibujar un trazo, no cuando se agrega un trazo a la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e4480-120">The **Stroke** event occurs when the user finishes drawing a stroke, not when a stroke is added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span> <span data-ttu-id="e4480-121">Cuando el usuario comienza a dibujar un trazo por primera vez, se agrega inmediatamente a la colección InkStrokes; sin embargo, el evento **Stroke** no se produce hasta que se completa el trazo.</span><span class="sxs-lookup"><span data-stu-id="e4480-121">When the user first starts to draw a stroke, it is added immediately to the InkStrokes collection; however, the **Stroke** event does not occur until the stroke is complete.</span></span> <span data-ttu-id="e4480-122">Por lo tanto, los trazos pueden existir en la colección InkStrokes que el controlador de eventos **Stroke** no ha encontrado.</span><span class="sxs-lookup"><span data-stu-id="e4480-122">Therefore, strokes can exist in the InkStrokes collection that the **Stroke** event handler has not seen.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e4480-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4480-123">Requirements</span></span>



| <span data-ttu-id="e4480-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4480-124">Requirement</span></span> | <span data-ttu-id="e4480-125">Value</span><span class="sxs-lookup"><span data-stu-id="e4480-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4480-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4480-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e4480-127">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e4480-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e4480-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4480-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e4480-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e4480-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e4480-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4480-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4480-131"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e4480-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e4480-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e4480-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="e4480-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4480-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e4480-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4480-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4480-135">InkPicture</span><span class="sxs-lookup"><span data-stu-id="e4480-135">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="e4480-136">[**StrokesAdded \[ control InkPicture de evento\]**](inkpicture-strokesadded.md)</span><span class="sxs-lookup"><span data-stu-id="e4480-136">[**StrokesAdded Event \[InkPicture Control\]**](inkpicture-strokesadded.md)</span></span>
</dt> <dt>

<span data-ttu-id="e4480-137">[**StrokesDeleted \[ control InkPicture de evento\]**](inkpicture-strokesdeleted.md)</span><span class="sxs-lookup"><span data-stu-id="e4480-137">[**StrokesDeleted Event \[InkPicture Control\]**](inkpicture-strokesdeleted.md)</span></span>
</dt> <dt>

[<span data-ttu-id="e4480-138">**Interfaz IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="e4480-138">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="e4480-139">**Interfaz IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="e4480-139">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

