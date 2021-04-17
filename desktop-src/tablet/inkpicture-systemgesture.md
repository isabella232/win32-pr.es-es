---
description: Se produce cuando se reconoce un gesto del sistema.
ms.assetid: 36e2ac5a-dc91-47c2-a8e5-e555437c0a5d
title: InkPicture.Sysevento temGesture (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 918198e4d18a854bb4238ce9d878dc70ab1f2f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717071"
---
# <a name="inkpicturesystemgesture-event"></a><span data-ttu-id="d5d53-103">InkPicture.Sysevento temGesture</span><span class="sxs-lookup"><span data-stu-id="d5d53-103">InkPicture.SystemGesture event</span></span>

<span data-ttu-id="d5d53-104">Se produce cuando se reconoce un gesto del sistema.</span><span class="sxs-lookup"><span data-stu-id="d5d53-104">Occurs when a system gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5d53-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5d53-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="d5d53-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5d53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5d53-107">*Cursor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d5d53-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d53-108">El objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento **SystemGesture** .</span><span class="sxs-lookup"><span data-stu-id="d5d53-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **SystemGesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="d5d53-109">*ID.* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="d5d53-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d53-110">Valor del gesto del sistema.</span><span class="sxs-lookup"><span data-stu-id="d5d53-110">The value of the system gesture.</span></span>

</dd> <dt>

<span data-ttu-id="d5d53-111">*X* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="d5d53-111">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d53-112">Coordenada x de la ubicación del gesto.</span><span class="sxs-lookup"><span data-stu-id="d5d53-112">The x-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="d5d53-113">*Y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="d5d53-113">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d53-114">Coordenada y de la ubicación del gesto.</span><span class="sxs-lookup"><span data-stu-id="d5d53-114">The y-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="d5d53-115">*Modificador* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5d53-115">*Modifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d53-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d5d53-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d5d53-117">*Carácter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5d53-117">*Character* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d53-118">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d5d53-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d5d53-119">*CursorMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5d53-119">*CursorMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d53-120">Valor que indica si el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) está en modo normal o en modo de borrador.</span><span class="sxs-lookup"><span data-stu-id="d5d53-120">A value that indicates whether the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object is in normal mode or eraser mode.</span></span> <span data-ttu-id="d5d53-121">1 es para el modo normal y 2 para el modo de borrador.</span><span class="sxs-lookup"><span data-stu-id="d5d53-121">1 is for normal mode and 2 are for eraser mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5d53-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5d53-122">Return value</span></span>

<span data-ttu-id="d5d53-123">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="d5d53-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5d53-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5d53-124">Remarks</span></span>

<span data-ttu-id="d5d53-125">Los gestos del sistema proporcionan información sobre el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que se usa para crear el gesto.</span><span class="sxs-lookup"><span data-stu-id="d5d53-125">System gestures give information about the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that is being used to create the gesture.</span></span> <span data-ttu-id="d5d53-126">También proporcionan accesos directos a combinaciones de eventos del mouse y son maneras de detectar eventos del mouse con menos impacto en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="d5d53-126">They also provide shortcuts to combinations of mouse events and are ways to detect mouse events with less impact on performance.</span></span>

<span data-ttu-id="d5d53-127">Por ejemplo, en lugar de buscar un par de eventos de evento [**MouseUp del \[ control \] InkPicture**](inkpicture-mouseup.md)Event InkPicture / [**\[ \] control**](inkpicture-mousedown.md) de eventos sin que se produzcan otros eventos del mouse en Between, puede buscar los gestos del sistema TAP o RightTap.</span><span class="sxs-lookup"><span data-stu-id="d5d53-127">For example, instead of looking for a [**MouseUp Event \[InkPicture Control\]**](inkpicture-mouseup.md)/[**MouseDown Event \[InkPicture Control\]**](inkpicture-mousedown.md) pair of events with no other mouse events occurring in between, you can look for the Tap or RightTap system gestures.</span></span>

<span data-ttu-id="d5d53-128">Otro ejemplo, en lugar de realizar escuchas de eventos [**MouseDown \[ \]**](inkpicture-mousedown.md)del control InkPicture del evento / [**MouseMove \[ \]**](inkpicture-mousemove.md) en el control InkPicture y obtener numerosos mensajes del **\[ \] control InkPicture del evento MouseMove** , puede ver los gestos del sistema de arrastrar o RightDrag siempre y cuando no esté interesado en las coordenadas (x, y) de cada posición del mouse.</span><span class="sxs-lookup"><span data-stu-id="d5d53-128">As another example, instead of listening for [**MouseDown Event \[InkPicture Control\]**](inkpicture-mousedown.md)/[**MouseMove Event \[InkPicture Control\]**](inkpicture-mousemove.md) events and getting numerous **MouseMove Event \[InkPicture Control\]** messages, you can watch for the Drag or RightDrag system gestures as long as you're not interested in the (x, y) coordinates of every position of the mouse.</span></span> <span data-ttu-id="d5d53-129">Esto le permite recibir un solo mensaje en lugar de numerosos mensajes del **\[ \] control InkPicture del evento MouseMove** .</span><span class="sxs-lookup"><span data-stu-id="d5d53-129">This allows you to receive only one message instead of numerous **MouseMove Event \[InkPicture Control\]** messages.</span></span>

<span data-ttu-id="d5d53-130">Para obtener una lista de gestos específicos del sistema, vea el tipo de enumeración [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) .</span><span class="sxs-lookup"><span data-stu-id="d5d53-130">For a list of specific system gestures, see the [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration type.</span></span> <span data-ttu-id="d5d53-131">Para obtener más información acerca de los gestos del sistema, consulte [uso de gestos](using-gestures.md) y [entradas de comandos en Tablet PC](/previous-versions//dd314533(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d5d53-131">For more information about system gestures, see [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).</span></span>

<span data-ttu-id="d5d53-132">Este método de evento se define en las interfaces de solo distribución (dispinterfaces) **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** con el identificador DISPID \_ ICESystemGesture.</span><span class="sxs-lookup"><span data-stu-id="d5d53-132">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICESystemGesture.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5d53-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5d53-133">Requirements</span></span>



| <span data-ttu-id="d5d53-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5d53-134">Requirement</span></span> | <span data-ttu-id="d5d53-135">Value</span><span class="sxs-lookup"><span data-stu-id="d5d53-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d53-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5d53-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d5d53-137">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d5d53-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d5d53-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5d53-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d5d53-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d5d53-139">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d5d53-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5d53-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5d53-141"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d5d53-141"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d5d53-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d5d53-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5d53-143"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5d53-143"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d5d53-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5d53-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5d53-145">InkPicture</span><span class="sxs-lookup"><span data-stu-id="d5d53-145">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="d5d53-146">**Enumeración InkSystemGesture**</span><span class="sxs-lookup"><span data-stu-id="d5d53-146">**InkSystemGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[<span data-ttu-id="d5d53-147">Usar gestos</span><span class="sxs-lookup"><span data-stu-id="d5d53-147">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

