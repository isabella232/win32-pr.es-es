---
description: Se produce cuando se agrega un trazo al objeto InkDisp.
ms.assetid: 46bbdb98-524f-4b4b-95c0-005e71d672f1
title: Evento InkDisp. InkAdded (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d25266a8cd75f873c5a7c1c18fa20fcf5126faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082093"
---
# <a name="inkdispinkadded-event"></a><span data-ttu-id="cb5bd-103">Evento InkDisp. InkAdded</span><span class="sxs-lookup"><span data-stu-id="cb5bd-103">InkDisp.InkAdded event</span></span>

<span data-ttu-id="cb5bd-104">Se produce cuando se agrega un trazo al objeto [**InkDisp**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="cb5bd-104">Occurs when a stroke is added to the [**InkDisp**](inkdisp-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb5bd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb5bd-105">Syntax</span></span>


```C++
void InkAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="cb5bd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb5bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb5bd-107">*StrokeIds* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb5bd-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb5bd-108">La matriz de enteros de la información de ID. de trazo para todos los trazos que se han agregado cuando se produce este evento.</span><span class="sxs-lookup"><span data-stu-id="cb5bd-108">The integer array of stroke ID information for all of the strokes that have been added when this event occurs.</span></span>

<span data-ttu-id="cb5bd-109">Para obtener más información sobre la estructura de variante, vea [usar la biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="cb5bd-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb5bd-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb5bd-110">Return value</span></span>

<span data-ttu-id="cb5bd-111">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="cb5bd-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb5bd-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb5bd-112">Remarks</span></span>

<span data-ttu-id="cb5bd-113">Si usa el objeto [**InkOverlay**](inkoverlay-class.md) o el control [InkPicture](inkpicture-control-reference.md) (donde [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) es igual a [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) y [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) es igual a [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) y pasa el borrador sobre un trazo, obtendrá la siguiente secuencia de eventos:</span><span class="sxs-lookup"><span data-stu-id="cb5bd-113">If you use the [**InkOverlay**](inkoverlay-class.md) object or the [InkPicture](inkpicture-control-reference.md) control (where [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) equals [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) and [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) equals [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) and pass the eraser over a stroke, you get the following sequence of events:</span></span>

-   [<span data-ttu-id="cb5bd-114">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="cb5bd-114">**InkDeleted**</span></span>](inkdisp-inkdeleted.md)
-   <span data-ttu-id="cb5bd-115">**InkAdded**</span><span class="sxs-lookup"><span data-stu-id="cb5bd-115">**InkAdded**</span></span>
-   [<span data-ttu-id="cb5bd-116">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="cb5bd-116">**InkDeleted**</span></span>](inkdisp-inkdeleted.md)

<span data-ttu-id="cb5bd-117">Los eventos **InkAdded** y [**InkDeleted**](inkdisp-inkdeleted.md) adicionales se producen porque el código subyacente agrega un trazo interno e invisible para realizar el seguimiento del borrador.</span><span class="sxs-lookup"><span data-stu-id="cb5bd-117">The additional **InkAdded** and [**InkDeleted**](inkdisp-inkdeleted.md) events occur because the underlying code adds an internal, invisible stroke to track the eraser.</span></span>

<span data-ttu-id="cb5bd-118">Este método de evento se define en la \_ interfaz IInkEvents.</span><span class="sxs-lookup"><span data-stu-id="cb5bd-118">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="cb5bd-119">La \_ interfaz IInkEvents implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IEInkAdded.</span><span class="sxs-lookup"><span data-stu-id="cb5bd-119">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IEInkAdded.</span></span>

<span data-ttu-id="cb5bd-120">El evento **InkAdded** se desencadena incluso cuando está en modo de selección o borrado, no solo cuando se inserta una entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="cb5bd-120">The **InkAdded** event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="cb5bd-121">Esto requiere que supervise el modo de edición (que es responsable de establecer) y tenga en cuenta el modo antes de interpretar el evento.</span><span class="sxs-lookup"><span data-stu-id="cb5bd-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="cb5bd-122">La ventaja de este requisito es mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de plataforma.</span><span class="sxs-lookup"><span data-stu-id="cb5bd-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb5bd-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb5bd-123">Requirements</span></span>



| <span data-ttu-id="cb5bd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb5bd-124">Requirement</span></span> | <span data-ttu-id="cb5bd-125">Value</span><span class="sxs-lookup"><span data-stu-id="cb5bd-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb5bd-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb5bd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cb5bd-127">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cb5bd-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="cb5bd-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb5bd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cb5bd-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cb5bd-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="cb5bd-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb5bd-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb5bd-131"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cb5bd-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cb5bd-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cb5bd-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="cb5bd-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb5bd-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="cb5bd-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb5bd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb5bd-135">**Clase InkDisp**</span><span class="sxs-lookup"><span data-stu-id="cb5bd-135">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> <dt>

<span data-ttu-id="cb5bd-136">[**Propiedad EditingMode \[ InkOverlay (clase)\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)</span><span class="sxs-lookup"><span data-stu-id="cb5bd-136">[**EditingMode Property \[InkOverlay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)</span></span>
</dt> <dt>

<span data-ttu-id="cb5bd-137">[**Propiedad EraserMode \[ InkOverlay (clase)\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)</span><span class="sxs-lookup"><span data-stu-id="cb5bd-137">[**EraserMode Property \[InkOverlay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)</span></span>
</dt> <dt>

[<span data-ttu-id="cb5bd-138">**Evento InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="cb5bd-138">**InkDeleted Event**</span></span>](inkdisp-inkdeleted.md)
</dt> <dt>

[<span data-ttu-id="cb5bd-139">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="cb5bd-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="cb5bd-140">Referencia del control InkPicture</span><span class="sxs-lookup"><span data-stu-id="cb5bd-140">InkPicture Control Reference</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="cb5bd-141">**Interfaz IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="cb5bd-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

