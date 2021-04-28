---
description: 'Evento InkOverlay.MouseDown: se produce cuando el puntero del mouse está sobre el objeto InkCollector o InkOverlay y se presiona un botón del mouse.'
ms.assetid: 95c3b1ae-0e77-4ca2-ab73-a0e97ab115b5
title: Evento InkOverlay.MouseDown (Msplaceut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ff1e4bff715a6585ee607de766c809579f527aa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086823"
---
# <a name="inkoverlaymousedown-event"></a><span data-ttu-id="5ccf2-103">Evento InkOverlay.MouseDown</span><span class="sxs-lookup"><span data-stu-id="5ccf2-103">InkOverlay.MouseDown event</span></span>

<span data-ttu-id="5ccf2-104">Se produce cuando el puntero del mouse está sobre el objeto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) y se presiona un botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="5ccf2-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ccf2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ccf2-105">Syntax</span></span>


```C++
void MouseDown(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="5ccf2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ccf2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ccf2-107">*Botón* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="5ccf2-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccf2-108">Botón del mouse que se presionó.</span><span class="sxs-lookup"><span data-stu-id="5ccf2-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="5ccf2-109">*Mayús* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="5ccf2-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccf2-110">Estado de la tecla MAYÚS.</span><span class="sxs-lookup"><span data-stu-id="5ccf2-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="5ccf2-111">*pX* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="5ccf2-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccf2-112">Coordenada X, en píxeles, de un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="5ccf2-112">The X-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="5ccf2-113">*pY* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="5ccf2-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccf2-114">Coordenada Y, en píxeles, de un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="5ccf2-114">The Y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="5ccf2-115">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5ccf2-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccf2-116">**VARIANT \_ TRUE** para cancelar el evento para el control primario; en caso contrario, **VARIANT \_ FALSE**.</span><span class="sxs-lookup"><span data-stu-id="5ccf2-116">**VARIANT\_TRUE** to cancelt he event forthe parent control; otherwise, **VARIANT\_FALSE**.</span></span> <span data-ttu-id="5ccf2-117">El valor predeterminado es **VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="5ccf2-117">The default value is **VARIANT\_FALSE**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ccf2-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ccf2-118">Return value</span></span>

<span data-ttu-id="5ccf2-119">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="5ccf2-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ccf2-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5ccf2-120">Remarks</span></span>

<span data-ttu-id="5ccf2-121">Para mejorar el rendimiento de la entrada de lápiz en tiempo real, oculte o muestre el cursor del mouse en los controladores de eventos [**MouseDown**](inkcollector-mousedown.md) y [**MouseUp.**](inkcollector-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="5ccf2-121">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="5ccf2-122">Las propiedades pX y pY están en píxeles y no las unidades HIMETRIC asociadas al espacio de entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="5ccf2-122">The properties pX and pY are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="5ccf2-123">Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación sin conocimiento de lápiz y este tipo de aplicación solo entiende píxeles.</span><span class="sxs-lookup"><span data-stu-id="5ccf2-123">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="5ccf2-124">Algunos controles se basan en una relación específica entre [**los eventos MouseDown,**](inkcollector-mousedown.md) [**MouseMove**](inkcollector-mousemove.md)y [**MouseUp.**](inkcollector-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="5ccf2-124">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="5ccf2-125">La cancelación de algunos de estos eventos puede tener resultados imprevistos.</span><span class="sxs-lookup"><span data-stu-id="5ccf2-125">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="5ccf2-126">Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador de \_ \_ DISPID IPEMouseDown.</span><span class="sxs-lookup"><span data-stu-id="5ccf2-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ccf2-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ccf2-127">Requirements</span></span>



| <span data-ttu-id="5ccf2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ccf2-128">Requirement</span></span> | <span data-ttu-id="5ccf2-129">Valor</span><span class="sxs-lookup"><span data-stu-id="5ccf2-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ccf2-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ccf2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5ccf2-131">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="5ccf2-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5ccf2-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ccf2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5ccf2-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5ccf2-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="5ccf2-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ccf2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ccf2-135"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="5ccf2-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5ccf2-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5ccf2-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="5ccf2-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ccf2-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="5ccf2-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5ccf2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ccf2-139">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="5ccf2-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="5ccf2-140">**InkMouseButton (enumeración)**</span><span class="sxs-lookup"><span data-stu-id="5ccf2-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="5ccf2-141">**InkShiftKeyModifierFlags (Enumeración)**</span><span class="sxs-lookup"><span data-stu-id="5ccf2-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[<span data-ttu-id="5ccf2-142">**Evento MouseUp**</span><span class="sxs-lookup"><span data-stu-id="5ccf2-142">**MouseUp Event**</span></span>](inkcollector-mouseup.md)
</dt> </dl>

 

 




