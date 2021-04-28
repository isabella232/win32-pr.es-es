---
description: 'Evento InkOverlay.MouseMove: se produce cuando el puntero del mouse se mueve sobre el objeto InkCollector o InkOverlay.'
ms.assetid: b25aeead-9fb1-4221-82fa-ce2d81f5fed8
title: Evento InkOverlay.MouseMove (Msplaceut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f8290a11b00dcf97b3f3d8568ebe9890f715454
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116913"
---
# <a name="inkoverlaymousemove-event"></a><span data-ttu-id="d37fb-103">Evento InkOverlay.MouseMove</span><span class="sxs-lookup"><span data-stu-id="d37fb-103">InkOverlay.MouseMove event</span></span>

<span data-ttu-id="d37fb-104">Se produce cuando el puntero del mouse se mueve sobre el objeto [**InkCollector**](inkcollector-class.md) [**o InkOverlay.**](inkoverlay-class.md)</span><span class="sxs-lookup"><span data-stu-id="d37fb-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d37fb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d37fb-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="d37fb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d37fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d37fb-107">*Botón* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d37fb-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d37fb-108">Botón del mouse que se presionó.</span><span class="sxs-lookup"><span data-stu-id="d37fb-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="d37fb-109">*Mayús* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d37fb-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d37fb-110">Estado de la tecla MAYÚS.</span><span class="sxs-lookup"><span data-stu-id="d37fb-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="d37fb-111">*pX* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d37fb-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d37fb-112">Coordenada x, en píxeles, de un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="d37fb-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="d37fb-113">*pY* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d37fb-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d37fb-114">Coordenada y, en píxeles, de un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="d37fb-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="d37fb-115">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d37fb-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d37fb-116">Si el evento se debe cancelar para el control primario.</span><span class="sxs-lookup"><span data-stu-id="d37fb-116">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="d37fb-117">El valor predeterminado es **FALSE,** que especifica que no se debe cancelar el evento.</span><span class="sxs-lookup"><span data-stu-id="d37fb-117">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d37fb-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d37fb-118">Return value</span></span>

<span data-ttu-id="d37fb-119">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="d37fb-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d37fb-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d37fb-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d37fb-121">Las propiedades *pX* y *pY* están en píxeles y no las unidades HIMETRIC asociadas al espacio de entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="d37fb-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="d37fb-122">Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación sin conocimiento de lápiz y este tipo de aplicación solo entiende píxeles.</span><span class="sxs-lookup"><span data-stu-id="d37fb-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="d37fb-123">Algunos controles se basan en una relación específica entre [**los eventos MouseDown,**](inkcollector-mousedown.md) [**MouseMove**](inkcollector-mousemove.md)y [**MouseUp.**](inkcollector-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="d37fb-123">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="d37fb-124">La cancelación de algunos de estos eventos puede tener resultados imprevistos.</span><span class="sxs-lookup"><span data-stu-id="d37fb-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="d37fb-125">Este método de evento se define en las interfaces de solo distribución \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador de \_ DISPID \_ IPEMouseMove.</span><span class="sxs-lookup"><span data-stu-id="d37fb-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="d37fb-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d37fb-126">Requirements</span></span>



| <span data-ttu-id="d37fb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d37fb-127">Requirement</span></span> | <span data-ttu-id="d37fb-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d37fb-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d37fb-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d37fb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d37fb-130">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="d37fb-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d37fb-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d37fb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d37fb-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d37fb-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d37fb-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d37fb-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d37fb-134"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="d37fb-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d37fb-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d37fb-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="d37fb-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d37fb-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d37fb-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d37fb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d37fb-138">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="d37fb-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="d37fb-139">**InkMouseButton (enumeración)**</span><span class="sxs-lookup"><span data-stu-id="d37fb-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="d37fb-140">**InkShiftKeyModifierFlags (Enumeración)**</span><span class="sxs-lookup"><span data-stu-id="d37fb-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




