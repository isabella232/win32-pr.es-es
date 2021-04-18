---
description: Se produce cuando el puntero del mouse se encuentra sobre el objeto InkCollector o InkOverlay y se presiona un botón del mouse.
ms.assetid: db9ec396-b2a7-4f4f-99f2-95aad46eea28
title: InkCollector. MouseDown (evento) (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 760801fb5c578ddbdd67b15a4201c21c4981b097
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540387"
---
# <a name="inkcollectormousedown-event"></a><span data-ttu-id="fd3d9-103">InkCollector. MouseDown (evento)</span><span class="sxs-lookup"><span data-stu-id="fd3d9-103">InkCollector.MouseDown event</span></span>

<span data-ttu-id="fd3d9-104">Se produce cuando el puntero del mouse se encuentra sobre el objeto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) y se presiona un botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd3d9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd3d9-105">Syntax</span></span>


```C++
void MouseDown(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="fd3d9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fd3d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd3d9-107">*Botón* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="fd3d9-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd3d9-108">Botón del mouse que se presionó.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="fd3d9-109">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fd3d9-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd3d9-110">Estado de la tecla Mayús.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="fd3d9-111">*PX* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fd3d9-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd3d9-112">Coordenada X, en píxeles, de un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-112">The X-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="fd3d9-113">*py* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fd3d9-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd3d9-114">Coordenada Y, en píxeles, de un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-114">The Y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="fd3d9-115">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fd3d9-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd3d9-116">**Variante \_ TRUE** para cancelar el evento para el control primario; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd3d9-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd3d9-117">Return value</span></span>

<span data-ttu-id="fd3d9-118">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd3d9-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd3d9-119">Remarks</span></span>

<span data-ttu-id="fd3d9-120">Para mejorar el rendimiento del lápiz en tiempo real, oculte o muestre el cursor del mouse en los controladores de eventos **MouseDown** y [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="fd3d9-120">To improve real-time ink performance, hide or show the mouse cursor in the **MouseDown** and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="fd3d9-121">Las propiedades *PX* y *py* se encuentran en píxeles, y no las unidades HIMETRIC asociadas al espacio de la tinta.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="fd3d9-122">Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación que no tiene en cuenta el lápiz y este tipo de aplicación solo entiende píxeles.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="fd3d9-123">Algunos controles dependen de una relación específica entre los eventos **MouseDown**, [**MouseMove**](inkcollector-mousemove.md)y [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="fd3d9-123">Some controls rely on a specific relationship between **MouseDown**, [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="fd3d9-124">La cancelación de algunos de estos eventos puede tener resultados imprevistos.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="fd3d9-125">Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ IPEMouseDown.</span><span class="sxs-lookup"><span data-stu-id="fd3d9-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd3d9-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd3d9-126">Requirements</span></span>



| <span data-ttu-id="fd3d9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd3d9-127">Requirement</span></span> | <span data-ttu-id="fd3d9-128">Value</span><span class="sxs-lookup"><span data-stu-id="fd3d9-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd3d9-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd3d9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fd3d9-130">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="fd3d9-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fd3d9-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd3d9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fd3d9-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fd3d9-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="fd3d9-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd3d9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd3d9-134"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fd3d9-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fd3d9-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fd3d9-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="fd3d9-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd3d9-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="fd3d9-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd3d9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd3d9-138">**InkCollector (clase)**</span><span class="sxs-lookup"><span data-stu-id="fd3d9-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="fd3d9-139">**Enumeración InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="fd3d9-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="fd3d9-140">**Enumeración InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="fd3d9-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[<span data-ttu-id="fd3d9-141">**MouseUp (evento)**</span><span class="sxs-lookup"><span data-stu-id="fd3d9-141">**MouseUp Event**</span></span>](inkcollector-mouseup.md)
</dt> </dl>

 

 




