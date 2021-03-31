---
description: Se produce cuando se reconoce un gesto de aplicación.
ms.assetid: 736715f4-c610-42cc-9fbb-c2b579da69e5
title: Evento InkEdit. gesto (autodibujado. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a61f4fce033672fde8cc4d74dced727fe60b7f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277400"
---
# <a name="inkeditgesture-event"></a><span data-ttu-id="17fa2-103">Evento InkEdit. gesto</span><span class="sxs-lookup"><span data-stu-id="17fa2-103">InkEdit.Gesture event</span></span>

<span data-ttu-id="17fa2-104">Se produce cuando se reconoce un gesto de aplicación.</span><span class="sxs-lookup"><span data-stu-id="17fa2-104">Occurs when an application gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="17fa2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17fa2-105">Syntax</span></span>


```C++
HRESULT Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="17fa2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17fa2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17fa2-107">*Cursor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="17fa2-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17fa2-108">El objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que se usó para crear este gesto.</span><span class="sxs-lookup"><span data-stu-id="17fa2-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that was used to create this gesture.</span></span>

</dd> <dt>

<span data-ttu-id="17fa2-109">*Trazos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="17fa2-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17fa2-110">La colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que contiene los objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que componen este gesto.</span><span class="sxs-lookup"><span data-stu-id="17fa2-110">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that contains the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects that make up this gesture.</span></span>

</dd> <dt>

<span data-ttu-id="17fa2-111">*Gestos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="17fa2-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17fa2-112">Una matriz de objetos [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) , en orden de confianza.</span><span class="sxs-lookup"><span data-stu-id="17fa2-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence.</span></span>

<span data-ttu-id="17fa2-113">Para obtener más información sobre la estructura de variante, vea [usar la biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="17fa2-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="17fa2-114">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="17fa2-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="17fa2-115">Indica si se debe cancelar la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que constituye este gesto, de modo que no se borre la tinta y se desencadene el evento [**Stroke**](inkedit-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="17fa2-115">Whether the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that makes up this gesture should be canceled, so as not to erase the ink and to fire the [**Stroke**](inkedit-stroke.md) event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17fa2-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17fa2-116">Return value</span></span>

<span data-ttu-id="17fa2-117">Si este evento se realiza correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="17fa2-117">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="17fa2-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="17fa2-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="17fa2-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17fa2-119">Remarks</span></span>

<span data-ttu-id="17fa2-120">Este método de evento se define en la interfaz **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="17fa2-120">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="17fa2-121">La interfaz **\_ IInkEditEvents** implementa la interfaz IDispatch con un identificador de DISPID \_ IeeGesture.</span><span class="sxs-lookup"><span data-stu-id="17fa2-121">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of DISPID\_IeeGesture.</span></span>

<span data-ttu-id="17fa2-122">Un evento de **gesto** solo se desencadena si el [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) del objeto [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) es el primer objeto **IInkStrokeDisp** desde la última llamada al método [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) o la última activación del tiempo de espera del reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="17fa2-122">A **Gesture** event is raised only if the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) for the [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) object is the first **IInkStrokeDisp** object since the last call to the [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) method or the last firing of the recognition timeout.</span></span>

<span data-ttu-id="17fa2-123">Si se cancela el evento de **gesto** , se genera el evento de [**trazo**](inkedit-stroke.md) para la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que provocó el evento de **gesto** .</span><span class="sxs-lookup"><span data-stu-id="17fa2-123">If the **Gesture** event is canceled, the [**Stroke**](inkedit-stroke.md) event is raised for the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that raised the **Gesture** event.</span></span>

<span data-ttu-id="17fa2-124">Para que se produzca este evento, el control [InkEdit](inkedit-control-reference.md) debe suscribirse a un conjunto de gestos de aplicación.</span><span class="sxs-lookup"><span data-stu-id="17fa2-124">For this event to occur, the [InkEdit](inkedit-control-reference.md) control must subscribe to a set of application gestures.</span></span> <span data-ttu-id="17fa2-125">Para establecer el interés del control InkEdit en un conjunto de gestos, llame al método [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) .</span><span class="sxs-lookup"><span data-stu-id="17fa2-125">To set the InkEdit control's interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) method.</span></span>

<span data-ttu-id="17fa2-126">Para obtener una lista de los gestos de aplicación, vea el tipo de enumeración [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="17fa2-126">For a list of application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

<span data-ttu-id="17fa2-127">El control [InkEdit](inkedit-control-reference.md) no reconoce varios gestos de trazo.</span><span class="sxs-lookup"><span data-stu-id="17fa2-127">The [InkEdit](inkedit-control-reference.md) control does not recognize multiple stroke gestures.</span></span>

<span data-ttu-id="17fa2-128">El control [InkEdit](inkedit-control-reference.md) se suscribe a los siguientes movimientos.</span><span class="sxs-lookup"><span data-stu-id="17fa2-128">The [InkEdit](inkedit-control-reference.md) control subscribes to the following gestures.</span></span>



| <span data-ttu-id="17fa2-129">Gesto</span><span class="sxs-lookup"><span data-stu-id="17fa2-129">Gesture</span></span>                              | <span data-ttu-id="17fa2-130">Acción</span><span class="sxs-lookup"><span data-stu-id="17fa2-130">Action</span></span>               |
|--------------------------------------|----------------------|
| <span data-ttu-id="17fa2-131">Abajo-izquierda, hacia abajo y a la izquierda</span><span class="sxs-lookup"><span data-stu-id="17fa2-131">Down-left ,Down-left-long</span></span><br/> | <span data-ttu-id="17fa2-132">Entrar</span><span class="sxs-lookup"><span data-stu-id="17fa2-132">Enter</span></span><br/>     |
| <span data-ttu-id="17fa2-133">Right</span><span class="sxs-lookup"><span data-stu-id="17fa2-133">Right</span></span><br/>                     | <span data-ttu-id="17fa2-134">Space</span><span class="sxs-lookup"><span data-stu-id="17fa2-134">Space</span></span><br/>     |
| <span data-ttu-id="17fa2-135">Left</span><span class="sxs-lookup"><span data-stu-id="17fa2-135">Left</span></span><br/>                      | <span data-ttu-id="17fa2-136">Retroceso</span><span class="sxs-lookup"><span data-stu-id="17fa2-136">Backspace</span></span><br/> |
| <span data-ttu-id="17fa2-137">Arriba a la derecha, arriba y a la derecha</span><span class="sxs-lookup"><span data-stu-id="17fa2-137">Up-right, Up-right-long</span></span><br/>   | <span data-ttu-id="17fa2-138">Pestaña</span><span class="sxs-lookup"><span data-stu-id="17fa2-138">Tab</span></span><br/>       |



 

<span data-ttu-id="17fa2-139">Para modificar la acción predeterminada de un gesto:</span><span class="sxs-lookup"><span data-stu-id="17fa2-139">To alter the default action for a gesture:</span></span>

1.  <span data-ttu-id="17fa2-140">Agregue controladores de eventos para los eventos de **gestos** y [**trazos**](inkedit-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="17fa2-140">Add event handlers for the **Gesture** and [**Stroke**](inkedit-stroke.md) events.</span></span>
2.  <span data-ttu-id="17fa2-141">En el controlador de eventos de **gestos** , cancele el evento de **gesto** para el gesto y realice la acción alternativa para el gesto.</span><span class="sxs-lookup"><span data-stu-id="17fa2-141">In the **Gesture** event handler, cancel the **Gesture** event for the gesture, and perform the alternate action for the gesture.</span></span>
3.  <span data-ttu-id="17fa2-142">En el controlador de eventos [**Stroke**](inkedit-stroke.md) , cancele el evento **Stroke** para el objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que ha generado el evento de **gesto** cancelado.</span><span class="sxs-lookup"><span data-stu-id="17fa2-142">In the [**Stroke**](inkedit-stroke.md) event handler, cancel the **Stroke** event for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that raised the canceled **Gesture** event.</span></span>

## <a name="requirements"></a><span data-ttu-id="17fa2-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17fa2-143">Requirements</span></span>



| <span data-ttu-id="17fa2-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="17fa2-144">Requirement</span></span> | <span data-ttu-id="17fa2-145">Value</span><span class="sxs-lookup"><span data-stu-id="17fa2-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17fa2-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17fa2-146">Minimum supported client</span></span><br/> | <span data-ttu-id="17fa2-147">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="17fa2-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="17fa2-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17fa2-148">Minimum supported server</span></span><br/> | <span data-ttu-id="17fa2-149">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="17fa2-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="17fa2-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17fa2-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="17fa2-151"><dt>Autodibujado. h (también requiere la intermano \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="17fa2-151"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="17fa2-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="17fa2-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="17fa2-153"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17fa2-153"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="17fa2-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="17fa2-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17fa2-155">InkEdit</span><span class="sxs-lookup"><span data-stu-id="17fa2-155">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="17fa2-156">**Enumeración InkApplicationGesture**</span><span class="sxs-lookup"><span data-stu-id="17fa2-156">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

<span data-ttu-id="17fa2-157">[**Control InkEdit del método SetGestureStatus \[\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)</span><span class="sxs-lookup"><span data-stu-id="17fa2-157">[**SetGestureStatus Method \[InkEdit Control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)</span></span>
</dt> <dt>

[<span data-ttu-id="17fa2-158">**Propiedad RecoTimeout**</span><span class="sxs-lookup"><span data-stu-id="17fa2-158">**RecoTimeout Property**</span></span>](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)
</dt> <dt>

<span data-ttu-id="17fa2-159">[**Control InkEdit de evento Stroke \[\]**](inkedit-stroke.md)</span><span class="sxs-lookup"><span data-stu-id="17fa2-159">[**Stroke Event \[InkEdit Control\]**](inkedit-stroke.md)</span></span>
</dt> <dt>

[<span data-ttu-id="17fa2-160">Usar gestos</span><span class="sxs-lookup"><span data-stu-id="17fa2-160">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

