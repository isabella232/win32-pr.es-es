---
description: Se produce cuando el puntero del mouse se mueve sobre el objeto InkCollector o InkOverlay.
ms.assetid: 688ac7ef-dcee-44a4-8947-117966365061
title: InkCollector. MouseMove (evento) (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ad88c35871ed73125be73b66329ede464f0c00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705552"
---
# <a name="inkcollectormousemove-event"></a><span data-ttu-id="7cbb9-103">InkCollector. MouseMove (evento)</span><span class="sxs-lookup"><span data-stu-id="7cbb9-103">InkCollector.MouseMove event</span></span>

<span data-ttu-id="7cbb9-104">Se produce cuando el puntero del mouse se mueve sobre el objeto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="7cbb9-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cbb9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7cbb9-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="7cbb9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7cbb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cbb9-107">*Botón* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="7cbb9-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cbb9-108">Botón del mouse que se presionó.</span><span class="sxs-lookup"><span data-stu-id="7cbb9-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="7cbb9-109">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7cbb9-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cbb9-110">Estado de la tecla Mayús.</span><span class="sxs-lookup"><span data-stu-id="7cbb9-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="7cbb9-111">*PX* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7cbb9-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cbb9-112">Coordenada x, en píxeles, de un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="7cbb9-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="7cbb9-113">*py* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7cbb9-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cbb9-114">Coordenada y, en píxeles, de un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="7cbb9-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="7cbb9-115">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7cbb9-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cbb9-116">**Variante \_ TRUE** para cancelar el evento para el control primario; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="7cbb9-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cbb9-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7cbb9-117">Return value</span></span>

<span data-ttu-id="7cbb9-118">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="7cbb9-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cbb9-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7cbb9-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7cbb9-120">Las propiedades *PX* y *py* se encuentran en píxeles, y no las unidades HIMETRIC asociadas al espacio de la tinta.</span><span class="sxs-lookup"><span data-stu-id="7cbb9-120">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="7cbb9-121">Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación que no tiene en cuenta el lápiz y este tipo de aplicación solo entiende píxeles.</span><span class="sxs-lookup"><span data-stu-id="7cbb9-121">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="7cbb9-122">Algunos controles dependen de una relación específica entre los eventos [**MouseDown**](inkcollector-mousedown.md), **MouseMove** y [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="7cbb9-122">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), **MouseMove**, and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="7cbb9-123">La cancelación de algunos de estos eventos puede tener resultados imprevistos.</span><span class="sxs-lookup"><span data-stu-id="7cbb9-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="7cbb9-124">Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ IPEMouseMove.</span><span class="sxs-lookup"><span data-stu-id="7cbb9-124">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cbb9-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cbb9-125">Requirements</span></span>



| <span data-ttu-id="7cbb9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cbb9-126">Requirement</span></span> | <span data-ttu-id="7cbb9-127">Value</span><span class="sxs-lookup"><span data-stu-id="7cbb9-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cbb9-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7cbb9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7cbb9-129">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7cbb9-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7cbb9-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7cbb9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7cbb9-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7cbb9-131">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="7cbb9-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7cbb9-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cbb9-133"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7cbb9-133"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7cbb9-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7cbb9-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="7cbb9-135"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cbb9-135"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="7cbb9-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="7cbb9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cbb9-137">**InkCollector (clase)**</span><span class="sxs-lookup"><span data-stu-id="7cbb9-137">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="7cbb9-138">**Enumeración InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="7cbb9-138">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="7cbb9-139">**Enumeración InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="7cbb9-139">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




