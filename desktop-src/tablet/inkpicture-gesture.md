---
description: Se produce cuando se reconoce un gesto específico de la aplicación.
ms.assetid: a20f2d78-6cfe-4755-968e-91369021db1b
title: Evento InkPicture. gesto (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94581369554b4aef16530c9ddc8b3fd1a31ad861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697554"
---
# <a name="inkpicturegesture-event"></a><span data-ttu-id="79fb9-103">Evento InkPicture. gesto</span><span class="sxs-lookup"><span data-stu-id="79fb9-103">InkPicture.Gesture event</span></span>

<span data-ttu-id="79fb9-104">Se produce cuando se reconoce un *gesto* específico de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="79fb9-104">Occurs when an application-specific *gesture* is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="79fb9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79fb9-105">Syntax</span></span>


```C++
void Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="79fb9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79fb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79fb9-107">*Cursor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="79fb9-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79fb9-108">El objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento de **gesto** .</span><span class="sxs-lookup"><span data-stu-id="79fb9-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Gesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="79fb9-109">*Trazos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79fb9-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79fb9-110">La colección [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que el reconocedor devolvió como el gesto.</span><span class="sxs-lookup"><span data-stu-id="79fb9-110">The [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that the recognizer returned as the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="79fb9-111">*Gestos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79fb9-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79fb9-112">Matriz de objetos [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) , en orden de confianza, del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="79fb9-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence, from the recognizer.</span></span>

<span data-ttu-id="79fb9-113">Para obtener más información sobre la estructura de variante, vea [usar la biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="79fb9-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="79fb9-114">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="79fb9-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="79fb9-115">**Variante \_ TRUE** si se debe cancelar este evento, por ejemplo, no borrar la tinta y activar el evento [**Stroke**](inkpicture-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="79fb9-115">**VARIANT\_TRUE** if this event should be cancelled, such as not to erase the ink and to fire the [**Stroke**](inkpicture-stroke.md) event.</span></span> <span data-ttu-id="79fb9-116">De lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="79fb9-116">Otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79fb9-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79fb9-117">Return value</span></span>

<span data-ttu-id="79fb9-118">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="79fb9-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="79fb9-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79fb9-119">Remarks</span></span>

<span data-ttu-id="79fb9-120">Este método de evento se define en las interfaces de solo distribución (dispinterfaces) **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** con el identificador DISPID \_ ICEGesture.</span><span class="sxs-lookup"><span data-stu-id="79fb9-120">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEGesture.</span></span>

<span data-ttu-id="79fb9-121">Cuando la propiedad [**si CollectionMode es**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) se establece en [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), el tiempo de espera entre el momento en que un usuario agrega un gesto y el momento en que se produce el evento de **gesto** es un valor fijo que no se puede modificar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="79fb9-121">When the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) property is set to [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), the timeout between when a user adds a gesture and when the **Gesture** event occurs is a fixed value that you cannot alter programmatically.</span></span> <span data-ttu-id="79fb9-122">El reconocimiento de gestos es más rápido en el modo **InkAndGesture** .</span><span class="sxs-lookup"><span data-stu-id="79fb9-122">Gesture recognition is faster in **InkAndGesture** mode.</span></span>

<span data-ttu-id="79fb9-123">Para evitar la recopilación de entradas manuscritas en modo [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) :</span><span class="sxs-lookup"><span data-stu-id="79fb9-123">To prevent the collection of ink while in [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) mode:</span></span>

-   <span data-ttu-id="79fb9-124">Establezca [**si CollectionMode es**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) en [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span><span class="sxs-lookup"><span data-stu-id="79fb9-124">Set [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) to [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span></span>
-   <span data-ttu-id="79fb9-125">Elimine el trazo en el evento [**Stroke**](inkpicture-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="79fb9-125">Delete the stroke in the [**Stroke**](inkpicture-stroke.md) event.</span></span>
-   <span data-ttu-id="79fb9-126">Procesa el gesto en el evento de **gesto** .</span><span class="sxs-lookup"><span data-stu-id="79fb9-126">Process the gesture in the **Gesture** event.</span></span>

<span data-ttu-id="79fb9-127">Para evitar el flujo de tinta mientras se gesturing, establezca la propiedad [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering) en **false**.</span><span class="sxs-lookup"><span data-stu-id="79fb9-127">To prevent the flow of ink while gesturing, set [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering) property to **FALSE**.</span></span>

<span data-ttu-id="79fb9-128">Además de cuando se inserta la entrada de lápiz, el evento de **gesto** se desencadena cuando se está en modo de selección o de borrado.</span><span class="sxs-lookup"><span data-stu-id="79fb9-128">In addition to when inserting ink, the **Gesture** event is fired when in select or erase mode.</span></span> <span data-ttu-id="79fb9-129">Usted es responsable de realizar el seguimiento del modo de edición y debe tener en cuenta el modo antes de interpretar el evento.</span><span class="sxs-lookup"><span data-stu-id="79fb9-129">You are responsible for tracking the editing mode and should be aware of the mode before interpreting the event.</span></span>

> [!Note]  
> <span data-ttu-id="79fb9-130">Para reconocer gestos, debe usar un objeto o un control que pueda recopilar entradas manuscritas.</span><span class="sxs-lookup"><span data-stu-id="79fb9-130">To recognize gestures, you must use an object or control that can collect ink.</span></span>

 

<span data-ttu-id="79fb9-131">Los gestos de aplicación se definen como gestos que se admiten en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="79fb9-131">Application gestures are defined as gestures that are supported within your application.</span></span>

<span data-ttu-id="79fb9-132">Para que se produzca este evento, el objeto o el control deben tener interés en un conjunto de gestos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="79fb9-132">For this event to occur, the object or control must have interest in a set of application gestures.</span></span> <span data-ttu-id="79fb9-133">Para establecer el interés de los objetos o controles en un conjunto de gestos, llame al método [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus) del objeto o control.</span><span class="sxs-lookup"><span data-stu-id="79fb9-133">To set the objects or controls interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus) method of the object or control.</span></span>

<span data-ttu-id="79fb9-134">Para obtener una lista de gestos de aplicación específicos, vea el tipo de enumeración [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="79fb9-134">For a list of specific application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

## <a name="requirements"></a><span data-ttu-id="79fb9-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79fb9-135">Requirements</span></span>



| <span data-ttu-id="79fb9-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="79fb9-136">Requirement</span></span> | <span data-ttu-id="79fb9-137">Value</span><span class="sxs-lookup"><span data-stu-id="79fb9-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79fb9-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79fb9-138">Minimum supported client</span></span><br/> | <span data-ttu-id="79fb9-139">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="79fb9-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="79fb9-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79fb9-140">Minimum supported server</span></span><br/> | <span data-ttu-id="79fb9-141">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="79fb9-141">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="79fb9-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79fb9-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="79fb9-143"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="79fb9-143"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="79fb9-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79fb9-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="79fb9-145"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79fb9-145"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="79fb9-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="79fb9-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79fb9-147">InkPicture</span><span class="sxs-lookup"><span data-stu-id="79fb9-147">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="79fb9-148">**Enumeración InkApplicationGesture**</span><span class="sxs-lookup"><span data-stu-id="79fb9-148">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[<span data-ttu-id="79fb9-149">**Método SetGestureStatus**</span><span class="sxs-lookup"><span data-stu-id="79fb9-149">**SetGestureStatus Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)
</dt> <dt>

[<span data-ttu-id="79fb9-150">Usar gestos</span><span class="sxs-lookup"><span data-stu-id="79fb9-150">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

