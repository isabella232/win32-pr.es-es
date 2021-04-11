---
description: Se produce cuando el puntero del mouse se mueve sobre el objeto InkCollector o InkOverlay.
ms.assetid: b25aeead-9fb1-4221-82fa-ce2d81f5fed8
title: Evento InkOverlay. MouseMove (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ddefd5f3b3f75b03488f74bdbd4aee222a89d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278856"
---
# <a name="inkoverlaymousemove-event"></a><span data-ttu-id="fbe09-103">Evento InkOverlay. MouseMove</span><span class="sxs-lookup"><span data-stu-id="fbe09-103">InkOverlay.MouseMove event</span></span>

<span data-ttu-id="fbe09-104">Se produce cuando el puntero del mouse se mueve sobre el objeto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="fbe09-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbe09-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fbe09-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="fbe09-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fbe09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbe09-107">*Botón* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="fbe09-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbe09-108">Botón del mouse que se presionó.</span><span class="sxs-lookup"><span data-stu-id="fbe09-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="fbe09-109">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fbe09-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbe09-110">Estado de la tecla Mayús.</span><span class="sxs-lookup"><span data-stu-id="fbe09-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="fbe09-111">*PX* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fbe09-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbe09-112">Coordenada x, en píxeles, de un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="fbe09-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="fbe09-113">*py* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fbe09-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbe09-114">Coordenada y, en píxeles, de un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="fbe09-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="fbe09-115">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fbe09-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbe09-116">Indica si se debe cancelar el evento para el control primario.</span><span class="sxs-lookup"><span data-stu-id="fbe09-116">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="fbe09-117">El valor predeterminado es **false**, que especifica que no se debe cancelar el evento.</span><span class="sxs-lookup"><span data-stu-id="fbe09-117">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbe09-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fbe09-118">Return value</span></span>

<span data-ttu-id="fbe09-119">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="fbe09-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbe09-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fbe09-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fbe09-121">Las propiedades *PX* y *py* se encuentran en píxeles, y no las unidades HIMETRIC asociadas al espacio de la tinta.</span><span class="sxs-lookup"><span data-stu-id="fbe09-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="fbe09-122">Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación que no tiene en cuenta el lápiz y este tipo de aplicación solo entiende píxeles.</span><span class="sxs-lookup"><span data-stu-id="fbe09-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="fbe09-123">Algunos controles dependen de una relación específica entre los eventos [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)y [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="fbe09-123">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="fbe09-124">La cancelación de algunos de estos eventos puede tener resultados imprevistos.</span><span class="sxs-lookup"><span data-stu-id="fbe09-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="fbe09-125">Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ IPEMouseMove.</span><span class="sxs-lookup"><span data-stu-id="fbe09-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbe09-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbe09-126">Requirements</span></span>



| <span data-ttu-id="fbe09-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbe09-127">Requirement</span></span> | <span data-ttu-id="fbe09-128">Value</span><span class="sxs-lookup"><span data-stu-id="fbe09-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbe09-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbe09-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fbe09-130">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="fbe09-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fbe09-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbe09-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fbe09-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fbe09-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="fbe09-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fbe09-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbe09-134"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fbe09-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fbe09-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fbe09-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="fbe09-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbe09-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="fbe09-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbe09-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbe09-138">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="fbe09-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="fbe09-139">**Enumeración InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="fbe09-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="fbe09-140">**Enumeración InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="fbe09-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




