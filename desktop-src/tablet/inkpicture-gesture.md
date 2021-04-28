---
description: 'Evento InkPicture.Gesture: se produce cuando se reconoce un gesto específico de la aplicación.'
ms.assetid: a20f2d78-6cfe-4755-968e-91369021db1b
title: Evento InkPicture.Gesture (Ms inkut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 915557f304d722ed2819af75dd40284db119abfb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086593"
---
# <a name="inkpicturegesture-event"></a><span data-ttu-id="015e8-103">Evento InkPicture.Gesture</span><span class="sxs-lookup"><span data-stu-id="015e8-103">InkPicture.Gesture event</span></span>

<span data-ttu-id="015e8-104">Se produce cuando se reconoce un *gesto específico de* la aplicación.</span><span class="sxs-lookup"><span data-stu-id="015e8-104">Occurs when an application-specific *gesture* is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="015e8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="015e8-105">Syntax</span></span>


```C++
void Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="015e8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="015e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="015e8-107">*Cursor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="015e8-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="015e8-108">Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento Gesture.**</span><span class="sxs-lookup"><span data-stu-id="015e8-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Gesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="015e8-109">*Trazos* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="015e8-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="015e8-110">Colección [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que el reconocedor devolvió como gesto.</span><span class="sxs-lookup"><span data-stu-id="015e8-110">The [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that the recognizer returned as the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="015e8-111">*Gestos* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="015e8-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="015e8-112">Matriz de [**objetos IInkGesture,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) en orden de confianza, del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="015e8-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence, from the recognizer.</span></span>

<span data-ttu-id="015e8-113">Para obtener más información sobre la estructura VARIANT, vea [Usar la biblioteca COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="015e8-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="015e8-114">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="015e8-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="015e8-115">**VARIANT \_ TRUE** si se debe cancelar este evento, por ejemplo, para no borrar la entrada de lápiz y para que se desaprenda el [**evento Stroke.**](inkpicture-stroke.md)</span><span class="sxs-lookup"><span data-stu-id="015e8-115">**VARIANT\_TRUE** if this event should be cancelled, such as not to erase the ink and to fire the [**Stroke**](inkpicture-stroke.md) event.</span></span> <span data-ttu-id="015e8-116">De lo contrario, **VARIANT \_ FALSE**.</span><span class="sxs-lookup"><span data-stu-id="015e8-116">Otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="015e8-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="015e8-117">Return value</span></span>

<span data-ttu-id="015e8-118">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="015e8-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="015e8-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="015e8-119">Remarks</span></span>

<span data-ttu-id="015e8-120">Este método de evento se define en las interfaces de solo distribución (dispinterfaces) de **\_ IInkCollectorEvents,** **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** con un identificador DE DISPID \_ ICEGesture.</span><span class="sxs-lookup"><span data-stu-id="015e8-120">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEGesture.</span></span>

<span data-ttu-id="015e8-121">Cuando la [**propiedad CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) se establece en [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), el tiempo de espera entre cuando un usuario agrega un gesto y cuando se produce el evento **Gesture** es un valor fijo que no se puede modificar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="015e8-121">When the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) property is set to [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), the timeout between when a user adds a gesture and when the **Gesture** event occurs is a fixed value that you cannot alter programmatically.</span></span> <span data-ttu-id="015e8-122">El reconocimiento de gestos es **más rápido en el modo InkAndGesture.**</span><span class="sxs-lookup"><span data-stu-id="015e8-122">Gesture recognition is faster in **InkAndGesture** mode.</span></span>

<span data-ttu-id="015e8-123">Para evitar la recopilación de lápiz en [**el modo InkAndGesture:**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)</span><span class="sxs-lookup"><span data-stu-id="015e8-123">To prevent the collection of ink while in [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) mode:</span></span>

-   <span data-ttu-id="015e8-124">Establezca [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) en [**InkAndGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)</span><span class="sxs-lookup"><span data-stu-id="015e8-124">Set [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) to [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span></span>
-   <span data-ttu-id="015e8-125">Elimine el trazo en el [**evento Stroke.**](inkpicture-stroke.md)</span><span class="sxs-lookup"><span data-stu-id="015e8-125">Delete the stroke in the [**Stroke**](inkpicture-stroke.md) event.</span></span>
-   <span data-ttu-id="015e8-126">Procese el gesto en el **evento Gesto.**</span><span class="sxs-lookup"><span data-stu-id="015e8-126">Process the gesture in the **Gesture** event.</span></span>

<span data-ttu-id="015e8-127">Para evitar el flujo de entrada de lápiz durante la gesuración, establezca [**la propiedad DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering) en **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="015e8-127">To prevent the flow of ink while gesturing, set [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering) property to **FALSE**.</span></span>

<span data-ttu-id="015e8-128">Además de al insertar la entrada de lápiz, el **evento Gesto** se desencadena cuando se está en modo de selección o borrado.</span><span class="sxs-lookup"><span data-stu-id="015e8-128">In addition to when inserting ink, the **Gesture** event is fired when in select or erase mode.</span></span> <span data-ttu-id="015e8-129">Usted es responsable de realizar el seguimiento del modo de edición y debe tener en cuenta el modo antes de interpretar el evento.</span><span class="sxs-lookup"><span data-stu-id="015e8-129">You are responsible for tracking the editing mode and should be aware of the mode before interpreting the event.</span></span>

> [!Note]  
> <span data-ttu-id="015e8-130">Para reconocer gestos, debe usar un objeto o control que pueda recopilar la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="015e8-130">To recognize gestures, you must use an object or control that can collect ink.</span></span>

 

<span data-ttu-id="015e8-131">Los gestos de aplicación se definen como gestos que se admiten dentro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="015e8-131">Application gestures are defined as gestures that are supported within your application.</span></span>

<span data-ttu-id="015e8-132">Para que se produzca este evento, el objeto o control debe tener interés en un conjunto de gestos de aplicación.</span><span class="sxs-lookup"><span data-stu-id="015e8-132">For this event to occur, the object or control must have interest in a set of application gestures.</span></span> <span data-ttu-id="015e8-133">Para establecer el interés de los objetos o controles en un conjunto de gestos, llame al [**método SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus) del objeto o control.</span><span class="sxs-lookup"><span data-stu-id="015e8-133">To set the objects or controls interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus) method of the object or control.</span></span>

<span data-ttu-id="015e8-134">Para obtener una lista de gestos de aplicación específicos, vea el tipo de enumeración [**InkApplicationGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)</span><span class="sxs-lookup"><span data-stu-id="015e8-134">For a list of specific application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

## <a name="requirements"></a><span data-ttu-id="015e8-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="015e8-135">Requirements</span></span>



| <span data-ttu-id="015e8-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="015e8-136">Requirement</span></span> | <span data-ttu-id="015e8-137">Valor</span><span class="sxs-lookup"><span data-stu-id="015e8-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="015e8-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="015e8-138">Minimum supported client</span></span><br/> | <span data-ttu-id="015e8-139">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="015e8-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="015e8-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="015e8-140">Minimum supported server</span></span><br/> | <span data-ttu-id="015e8-141">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="015e8-141">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="015e8-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="015e8-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="015e8-143"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="015e8-143"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="015e8-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="015e8-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="015e8-145"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="015e8-145"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="015e8-146">Consulte también</span><span class="sxs-lookup"><span data-stu-id="015e8-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="015e8-147">InkPicture</span><span class="sxs-lookup"><span data-stu-id="015e8-147">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="015e8-148">**InkApplicationGesture (enumeración)**</span><span class="sxs-lookup"><span data-stu-id="015e8-148">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[<span data-ttu-id="015e8-149">**SetGestureStatus (método)**</span><span class="sxs-lookup"><span data-stu-id="015e8-149">**SetGestureStatus Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)
</dt> <dt>

[<span data-ttu-id="015e8-150">Uso de gestos</span><span class="sxs-lookup"><span data-stu-id="015e8-150">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

