---
description: Se produce cuando se reconoce un gesto del sistema.
ms.assetid: 11071d6f-8aa3-4902-94fd-89ad0cf17729
title: InkCollector.Sysevento temGesture (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282f28e5ef1bc3a86f51b6d345be6e00d78c8213
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541286"
---
# <a name="inkcollectorsystemgesture-event"></a><span data-ttu-id="520ef-103">InkCollector.Sysevento temGesture</span><span class="sxs-lookup"><span data-stu-id="520ef-103">InkCollector.SystemGesture event</span></span>

<span data-ttu-id="520ef-104">Se produce cuando se reconoce un gesto del sistema.</span><span class="sxs-lookup"><span data-stu-id="520ef-104">Occurs when a system gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="520ef-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="520ef-105">Syntax</span></span>


```C++
void SystemGesture(
  [in] IInkCursor       *Cursor,
  [in] InkSystemGesture Id,
  [in] long             X,
  [in] long             Y,
  [in] long             Modifier,
  [in] BSTR             Character,
  [in] long             CursorMode
);
```



## <a name="parameters"></a><span data-ttu-id="520ef-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="520ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="520ef-107">*Cursor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="520ef-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="520ef-108">El objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento **SystemGesture** .</span><span class="sxs-lookup"><span data-stu-id="520ef-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **SystemGesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="520ef-109">*ID.* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="520ef-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="520ef-110">Valor del gesto del sistema.</span><span class="sxs-lookup"><span data-stu-id="520ef-110">The value of the system gesture.</span></span>

</dd> <dt>

<span data-ttu-id="520ef-111">*X* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="520ef-111">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="520ef-112">Coordenada x de la ubicación del gesto.</span><span class="sxs-lookup"><span data-stu-id="520ef-112">The x-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="520ef-113">*Y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="520ef-113">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="520ef-114">Coordenada y de la ubicación del gesto.</span><span class="sxs-lookup"><span data-stu-id="520ef-114">The y-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="520ef-115">*Modificador* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="520ef-115">*Modifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="520ef-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="520ef-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="520ef-117">*Carácter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="520ef-117">*Character* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="520ef-118">Reservado.</span><span class="sxs-lookup"><span data-stu-id="520ef-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="520ef-119">*CursorMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="520ef-119">*CursorMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="520ef-120">Valor que indica si el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) está en modo normal o en modo de borrador.</span><span class="sxs-lookup"><span data-stu-id="520ef-120">A value that indicates whether the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object is in normal mode or eraser mode.</span></span> <span data-ttu-id="520ef-121">1 es para el modo normal y 2 para el modo de borrador.</span><span class="sxs-lookup"><span data-stu-id="520ef-121">1 is for normal mode and 2 are for eraser mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="520ef-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="520ef-122">Return value</span></span>

<span data-ttu-id="520ef-123">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="520ef-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="520ef-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="520ef-124">Remarks</span></span>

<span data-ttu-id="520ef-125">Los gestos del sistema son útiles porque proporcionan información sobre el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que se usa para crear el gesto.</span><span class="sxs-lookup"><span data-stu-id="520ef-125">System gestures are useful because they give information about the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that is being used to create the gesture.</span></span> <span data-ttu-id="520ef-126">También proporcionan accesos directos a combinaciones de eventos del mouse y son formas "más baratas" de detectar eventos del mouse.</span><span class="sxs-lookup"><span data-stu-id="520ef-126">They also provide shortcuts to combinations of mouse events and are "cheaper" ways to detect mouse events.</span></span>

<span data-ttu-id="520ef-127">Por ejemplo, en lugar de buscar un par de eventos MouseDown del [**evento MouseUp**](inkcollector-mouseup.md)  /  [](inkcollector-mousedown.md) de eventos sin que se produzcan otros eventos del mouse en, puede buscar los gestos del sistema [**TAP**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) o **RightTap** .</span><span class="sxs-lookup"><span data-stu-id="520ef-127">For example, instead of looking for a [**MouseUp Event**](inkcollector-mouseup.md) / [**MouseDown Event**](inkcollector-mousedown.md) pair of events with no other mouse events occurring in between, you can look for the [**Tap**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightTap** system gestures.</span></span>

<span data-ttu-id="520ef-128">Otro ejemplo, en lugar de realizar escuchas de eventos de evento de evento de evento [**MouseDown**](inkcollector-mousedown.md)  /  [](inkcollector-mousemove.md) y obtener numerosos mensajes de **eventos de MouseMove** , puede ver los gestos de [**arrastrar**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) o **RightDrag** del sistema siempre que no le interesen las coordenadas (x, y) de cada posición del mouse.</span><span class="sxs-lookup"><span data-stu-id="520ef-128">As another example, instead of listening for [**MouseDown Event**](inkcollector-mousedown.md) / [**MouseMove Event**](inkcollector-mousemove.md) events and getting numerous **MouseMove Event** messages, you can watch for the [**Drag**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightDrag** system gestures as long as you're not interested in the (x, y) coordinates of every position of the mouse.</span></span> <span data-ttu-id="520ef-129">Esto le permite recibir solo un mensaje en lugar de numerosos mensajes de **eventos de MouseMove** .</span><span class="sxs-lookup"><span data-stu-id="520ef-129">This allows you to receive only one message instead of numerous **MouseMove Event** messages.</span></span>

<span data-ttu-id="520ef-130">Para obtener una lista de gestos específicos del sistema, vea el tipo de enumeración [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) .</span><span class="sxs-lookup"><span data-stu-id="520ef-130">For a list of specific system gestures, see the [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration type.</span></span> <span data-ttu-id="520ef-131">Para obtener más información acerca de los gestos del sistema, consulte [uso de gestos](using-gestures.md) y [entradas de comandos en Tablet PC](/previous-versions//dd314533(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="520ef-131">For more information about system gestures, see [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).</span></span>

<span data-ttu-id="520ef-132">Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ ICESystemGesture.</span><span class="sxs-lookup"><span data-stu-id="520ef-132">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICESystemGesture.</span></span>

## <a name="requirements"></a><span data-ttu-id="520ef-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="520ef-133">Requirements</span></span>



| <span data-ttu-id="520ef-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="520ef-134">Requirement</span></span> | <span data-ttu-id="520ef-135">Value</span><span class="sxs-lookup"><span data-stu-id="520ef-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="520ef-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="520ef-136">Minimum supported client</span></span><br/> | <span data-ttu-id="520ef-137">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="520ef-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="520ef-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="520ef-138">Minimum supported server</span></span><br/> | <span data-ttu-id="520ef-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="520ef-139">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="520ef-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="520ef-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="520ef-141"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="520ef-141"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="520ef-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="520ef-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="520ef-143"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="520ef-143"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="520ef-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="520ef-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="520ef-145">**InkCollector (clase)**</span><span class="sxs-lookup"><span data-stu-id="520ef-145">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="520ef-146">**Enumeración InkSystemGesture**</span><span class="sxs-lookup"><span data-stu-id="520ef-146">**InkSystemGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[<span data-ttu-id="520ef-147">**Interfaz IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="520ef-147">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="520ef-148">Usar gestos</span><span class="sxs-lookup"><span data-stu-id="520ef-148">Using Gestures</span></span>](using-gestures.md)
</dt> <dt>

[<span data-ttu-id="520ef-149">Entrada de lápiz, tinta y reconocimiento</span><span class="sxs-lookup"><span data-stu-id="520ef-149">Pen Input, Ink, and Recognition</span></span>](pen-input--ink--and-recognition.md)
</dt> <dt>

<span data-ttu-id="520ef-150">[Entrada de comando en Tablet PC](/previous-versions//dd314533(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="520ef-150">[Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85))</span></span>
</dt> </dl>

 

