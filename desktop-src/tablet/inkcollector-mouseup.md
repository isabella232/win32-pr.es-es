---
description: 'Evento InkCollector.MouseUp: se produce cuando el puntero del mouse está sobre el objeto InkCollector o InkOverlay y se libera un botón del mouse.'
ms.assetid: 6dcc6c68-89f7-4020-b378-56df9d46974b
title: Evento InkCollector.MouseUp (Ms mouseut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc4fde64603a00ecb8a47d3869f2eb90352fcc4f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110153"
---
# <a name="inkcollectormouseup-event"></a><span data-ttu-id="a4582-103">Evento InkCollector.MouseUp</span><span class="sxs-lookup"><span data-stu-id="a4582-103">InkCollector.MouseUp event</span></span>

<span data-ttu-id="a4582-104">Se produce cuando el puntero del mouse está sobre el objeto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) y se libera un botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="a4582-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4582-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4582-105">Syntax</span></span>


```C++
void MouseUp(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="a4582-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4582-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4582-107">*Botón* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a4582-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4582-108">Botón del mouse que se ha liberado.</span><span class="sxs-lookup"><span data-stu-id="a4582-108">The mouse button that was released.</span></span>

</dd> <dt>

<span data-ttu-id="a4582-109">*Mayús* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a4582-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4582-110">Estado de la tecla MAYÚS.</span><span class="sxs-lookup"><span data-stu-id="a4582-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="a4582-111">*pX* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a4582-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4582-112">Coordenada X, en píxeles, de un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="a4582-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="a4582-113">*pY* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a4582-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4582-114">Coordenada y, en píxeles, de un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="a4582-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="a4582-115">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a4582-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4582-116">**VARIANT \_ TRUE** para cancelar el evento del control primario; de lo contrario, **VARIANT \_ FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a4582-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4582-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4582-117">Return value</span></span>

<span data-ttu-id="a4582-118">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="a4582-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4582-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a4582-119">Remarks</span></span>

<span data-ttu-id="a4582-120">Para mejorar el rendimiento de la entrada de lápiz en tiempo real, oculte o muestre el cursor del mouse en los controladores de eventos [**MouseDown**](inkcollector-mousedown.md) y **MouseUp.**</span><span class="sxs-lookup"><span data-stu-id="a4582-120">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and **MouseUp** event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="a4582-121">Las propiedades *pX* y *pY* están en píxeles y no las unidades HIMETRIC asociadas al espacio de entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="a4582-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="a4582-122">Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación sin conocimiento de lápiz y este tipo de aplicación solo entiende píxeles.</span><span class="sxs-lookup"><span data-stu-id="a4582-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="a4582-123">Algunos controles se basan en una relación específica entre [**los eventos MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)y **MouseUp.**</span><span class="sxs-lookup"><span data-stu-id="a4582-123">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and **MouseUp** events.</span></span> <span data-ttu-id="a4582-124">La cancelación de algunos de estos eventos puede tener resultados imprevistos.</span><span class="sxs-lookup"><span data-stu-id="a4582-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="a4582-125">Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador de \_ DISPID \_ IPEMouseUp.</span><span class="sxs-lookup"><span data-stu-id="a4582-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4582-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4582-126">Requirements</span></span>



| <span data-ttu-id="a4582-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4582-127">Requirement</span></span> | <span data-ttu-id="a4582-128">Valor</span><span class="sxs-lookup"><span data-stu-id="a4582-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4582-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4582-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a4582-130">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="a4582-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a4582-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4582-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a4582-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a4582-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a4582-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4582-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4582-134"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="a4582-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a4582-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a4582-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="a4582-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4582-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a4582-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a4582-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4582-138">**InkCollector (clase)**</span><span class="sxs-lookup"><span data-stu-id="a4582-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="a4582-139">**InkMouseButton (enumeración)**</span><span class="sxs-lookup"><span data-stu-id="a4582-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="a4582-140">**InkShiftKeyModifierFlags (Enumeración)**</span><span class="sxs-lookup"><span data-stu-id="a4582-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




