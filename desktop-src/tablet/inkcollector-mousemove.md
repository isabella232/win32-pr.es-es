---
description: 'Evento InkCollector.MouseMove: se produce cuando el puntero del mouse se mueve sobre el objeto InkCollector o InkOverlay.'
ms.assetid: 688ac7ef-dcee-44a4-8947-117966365061
title: Evento InkCollector.MouseMove (Ms mouseut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3392f2022af39600cb24461b26d37e5d624f4cb4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110163"
---
# <a name="inkcollectormousemove-event"></a><span data-ttu-id="9e9d8-103">Evento InkCollector.MouseMove</span><span class="sxs-lookup"><span data-stu-id="9e9d8-103">InkCollector.MouseMove event</span></span>

<span data-ttu-id="9e9d8-104">Se produce cuando el puntero del mouse se mueve sobre el objeto [**InkCollector**](inkcollector-class.md) [**o InkOverlay.**](inkoverlay-class.md)</span><span class="sxs-lookup"><span data-stu-id="9e9d8-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e9d8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e9d8-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="9e9d8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e9d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e9d8-107">*Botón* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9e9d8-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9d8-108">Botón del mouse que se presionó.</span><span class="sxs-lookup"><span data-stu-id="9e9d8-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="9e9d8-109">*Mayús* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9e9d8-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9d8-110">Estado de la tecla MAYÚS.</span><span class="sxs-lookup"><span data-stu-id="9e9d8-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="9e9d8-111">*pX* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9e9d8-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9d8-112">Coordenada x, en píxeles, de un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="9e9d8-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="9e9d8-113">*pY* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9e9d8-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9d8-114">Coordenada y, en píxeles, de un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="9e9d8-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="9e9d8-115">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9e9d8-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9d8-116">**VARIANT \_ TRUE** para cancelar el evento del control primario; en caso contrario, **VARIANT \_ FALSE**.</span><span class="sxs-lookup"><span data-stu-id="9e9d8-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e9d8-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9e9d8-117">Return value</span></span>

<span data-ttu-id="9e9d8-118">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="9e9d8-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e9d8-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9e9d8-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9e9d8-120">Las propiedades *pX* y *pY* están en píxeles y no las unidades HIMETRIC asociadas al espacio de entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="9e9d8-120">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="9e9d8-121">Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación sin conocimiento de lápiz y este tipo de aplicación solo entiende píxeles.</span><span class="sxs-lookup"><span data-stu-id="9e9d8-121">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="9e9d8-122">Algunos controles se basan en una relación específica entre [**los eventos MouseDown,**](inkcollector-mousedown.md) **MouseMove** y [**MouseUp.**](inkcollector-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="9e9d8-122">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), **MouseMove**, and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="9e9d8-123">La cancelación de algunos de estos eventos puede tener resultados imprevistos.</span><span class="sxs-lookup"><span data-stu-id="9e9d8-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="9e9d8-124">Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ de DISPID \_ IPEMouseMove.</span><span class="sxs-lookup"><span data-stu-id="9e9d8-124">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e9d8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e9d8-125">Requirements</span></span>



| <span data-ttu-id="9e9d8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e9d8-126">Requirement</span></span> | <span data-ttu-id="9e9d8-127">Valor</span><span class="sxs-lookup"><span data-stu-id="9e9d8-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e9d8-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e9d8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9e9d8-129">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="9e9d8-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9e9d8-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e9d8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9e9d8-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9e9d8-131">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="9e9d8-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e9d8-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e9d8-133"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="9e9d8-133"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9e9d8-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e9d8-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="9e9d8-135"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e9d8-135"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="9e9d8-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9e9d8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e9d8-137">**InkCollector (clase)**</span><span class="sxs-lookup"><span data-stu-id="9e9d8-137">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="9e9d8-138">**InkMouseButton (enumeración)**</span><span class="sxs-lookup"><span data-stu-id="9e9d8-138">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="9e9d8-139">**InkShiftKeyModifierFlags (Enumeración)**</span><span class="sxs-lookup"><span data-stu-id="9e9d8-139">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




