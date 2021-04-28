---
description: 'InkOverlay.Sysevento temGesture: se produce cuando se reconoce un gesto del sistema.'
ms.assetid: 6f82b234-2088-4207-a6b4-6c6919623d6a
title: InkOverlay.Sysevento temGesture (Ms ashut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3498d6b5fa779f6a15866ac93d53be8348f3d1a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086673"
---
# <a name="inkoverlaysystemgesture-event"></a><span data-ttu-id="17af1-103">InkOverlay.Sysevento temGesture</span><span class="sxs-lookup"><span data-stu-id="17af1-103">InkOverlay.SystemGesture event</span></span>

<span data-ttu-id="17af1-104">Se produce cuando se reconoce un gesto del sistema.</span><span class="sxs-lookup"><span data-stu-id="17af1-104">Occurs when a system gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="17af1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17af1-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="17af1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17af1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17af1-107">*Cursor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="17af1-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17af1-108">Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el [**evento SystemGesture.**](inkcollector-systemgesture.md)</span><span class="sxs-lookup"><span data-stu-id="17af1-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**SystemGesture**](inkcollector-systemgesture.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="17af1-109">*Id.* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="17af1-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17af1-110">Valor del gesto del sistema.</span><span class="sxs-lookup"><span data-stu-id="17af1-110">The value of the system gesture.</span></span>

</dd> <dt>

<span data-ttu-id="17af1-111">*X* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="17af1-111">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17af1-112">Coordenada x de la ubicación del gesto.</span><span class="sxs-lookup"><span data-stu-id="17af1-112">The x-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="17af1-113">*Y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="17af1-113">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17af1-114">Coordenada y de la ubicación del gesto.</span><span class="sxs-lookup"><span data-stu-id="17af1-114">The y-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="17af1-115">*Modificador* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="17af1-115">*Modifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17af1-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="17af1-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="17af1-117">*Carácter* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="17af1-117">*Character* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17af1-118">Reservado.</span><span class="sxs-lookup"><span data-stu-id="17af1-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="17af1-119">*CursorMode* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="17af1-119">*CursorMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17af1-120">Valor que indica si el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) está en modo normal o en modo borrador.</span><span class="sxs-lookup"><span data-stu-id="17af1-120">A value that indicates whether the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object is in normal mode or eraser mode.</span></span> <span data-ttu-id="17af1-121">1 es para el modo normal y 2 para el modo borrador.</span><span class="sxs-lookup"><span data-stu-id="17af1-121">1 is for normal mode and 2 are for eraser mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17af1-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17af1-122">Return value</span></span>

<span data-ttu-id="17af1-123">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="17af1-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17af1-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="17af1-124">Remarks</span></span>

<span data-ttu-id="17af1-125">Los gestos del sistema son útiles porque dan información sobre el [**objeto IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que se usa para crear el gesto.</span><span class="sxs-lookup"><span data-stu-id="17af1-125">System gestures are useful because they give information about the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that is being used to create the gesture.</span></span> <span data-ttu-id="17af1-126">También proporcionan accesos directos a combinaciones de eventos del mouse y son formas "más económicas" de detectar eventos del mouse.</span><span class="sxs-lookup"><span data-stu-id="17af1-126">They also provide shortcuts to combinations of mouse events and are "cheaper" ways to detect mouse events.</span></span>

<span data-ttu-id="17af1-127">Por ejemplo, en lugar de buscar un par de eventos MouseDown Event mousedown de [**mouseup**](inkcollector-mouseup.md)sin que se produzcan otros eventos del mouse entre ellos, puede buscar los gestos del sistema Tap o  /  [](inkcollector-mousedown.md) **RightTap.** [](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)</span><span class="sxs-lookup"><span data-stu-id="17af1-127">For example, instead of looking for a [**MouseUp Event**](inkcollector-mouseup.md) / [**MouseDown Event**](inkcollector-mousedown.md) pair of events with no other mouse events occurring in between, you can look for the [**Tap**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightTap** system gestures.</span></span>

<span data-ttu-id="17af1-128">Como otro ejemplo, en lugar de escuchar eventos [**MouseMove**](inkcollector-mousedown.md)Event de MouseDown y obtener numerosos mensajes de evento  /  [](inkcollector-mousemove.md) **MouseMove,** puede ver los gestos del sistema Drag o **RightDrag** siempre que no esté interesado en las coordenadas (x, y) de cada posición del mouse. [](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)</span><span class="sxs-lookup"><span data-stu-id="17af1-128">As another example, instead of listening for [**MouseDown Event**](inkcollector-mousedown.md) / [**MouseMove Event**](inkcollector-mousemove.md) events and getting numerous **MouseMove Event** messages, you can watch for the [**Drag**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightDrag** system gestures as long as you're not interested in the (x, y) coordinates of every position of the mouse.</span></span> <span data-ttu-id="17af1-129">Esto le permite recibir solo un mensaje en lugar de varios **mensajes mousemove Event.**</span><span class="sxs-lookup"><span data-stu-id="17af1-129">This allows you to receive only one message instead of numerous **MouseMove Event** messages.</span></span>

<span data-ttu-id="17af1-130">Para obtener una lista de gestos específicos del sistema, vea el tipo de enumeración [**InkSystemGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)</span><span class="sxs-lookup"><span data-stu-id="17af1-130">For a list of specific system gestures, see the [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration type.</span></span> <span data-ttu-id="17af1-131">Para obtener más información sobre los gestos del sistema, vea [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="17af1-131">For more information about system gestures, see [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).</span></span>

<span data-ttu-id="17af1-132">Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ de DISPID \_ ICESystemGesture.</span><span class="sxs-lookup"><span data-stu-id="17af1-132">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICESystemGesture.</span></span>

## <a name="requirements"></a><span data-ttu-id="17af1-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17af1-133">Requirements</span></span>



| <span data-ttu-id="17af1-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="17af1-134">Requirement</span></span> | <span data-ttu-id="17af1-135">Valor</span><span class="sxs-lookup"><span data-stu-id="17af1-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17af1-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17af1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="17af1-137">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="17af1-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="17af1-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17af1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="17af1-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="17af1-139">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="17af1-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17af1-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="17af1-141"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="17af1-141"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="17af1-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="17af1-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="17af1-143"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17af1-143"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="17af1-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="17af1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17af1-145">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="17af1-145">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="17af1-146">**InkSystemGesture (enumeración)**</span><span class="sxs-lookup"><span data-stu-id="17af1-146">**InkSystemGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[<span data-ttu-id="17af1-147">**IInkCursor (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="17af1-147">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="17af1-148">Uso de gestos</span><span class="sxs-lookup"><span data-stu-id="17af1-148">Using Gestures</span></span>](using-gestures.md)
</dt> <dt>

[<span data-ttu-id="17af1-149">Entrada de lápiz, entrada de lápiz y reconocimiento</span><span class="sxs-lookup"><span data-stu-id="17af1-149">Pen Input, Ink, and Recognition</span></span>](pen-input--ink--and-recognition.md)
</dt> <dt>

<span data-ttu-id="17af1-150">[Entrada de comandos en tablet PC](/previous-versions//dd314533(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="17af1-150">[Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85))</span></span>
</dt> </dl>

 

