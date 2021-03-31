---
description: Se produce cuando la rueda del mouse se mueve mientras el objeto InkCollector o InkOverlay tiene el foco.
ms.assetid: b7269e07-7001-48ca-8e20-a39cb02f3719
title: Evento InkOverlay. MouseWheel (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bbd919fdf02d85c32efa2a1a923d5de7ebe4f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912910"
---
# <a name="inkoverlaymousewheel-event"></a><span data-ttu-id="8929c-103">InkOverlay. MouseWheel (evento)</span><span class="sxs-lookup"><span data-stu-id="8929c-103">InkOverlay.MouseWheel event</span></span>

<span data-ttu-id="8929c-104">Se produce cuando la rueda del mouse se mueve mientras el objeto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="8929c-104">Occurs when the mouse wheel moves while the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="8929c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8929c-105">Syntax</span></span>


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="8929c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8929c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8929c-107">*Botón* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8929c-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8929c-108">Botón del mouse que se presionó.</span><span class="sxs-lookup"><span data-stu-id="8929c-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="8929c-109">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8929c-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8929c-110">Estado de la tecla Mayús.</span><span class="sxs-lookup"><span data-stu-id="8929c-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="8929c-111">*Delta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8929c-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8929c-112">Recuento con signo del número de pasos que ha girado la rueda del mouse.</span><span class="sxs-lookup"><span data-stu-id="8929c-112">A signed count of the number of detents the mouse wheel has rotated.</span></span> <span data-ttu-id="8929c-113">Un paso es una muesca de la rueda del mouse.</span><span class="sxs-lookup"><span data-stu-id="8929c-113">A detent is one notch of the mouse wheel.</span></span>

</dd> <dt>

<span data-ttu-id="8929c-114">*x* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="8929c-114">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8929c-115">Coordenada x, en píxeles, de un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="8929c-115">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="8929c-116">*y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="8929c-116">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8929c-117">Coordenada y, en píxeles, de un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="8929c-117">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="8929c-118">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8929c-118">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8929c-119">Indica si se debe cancelar el evento para el control primario.</span><span class="sxs-lookup"><span data-stu-id="8929c-119">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="8929c-120">El valor predeterminado es **false**, que especifica que no se debe cancelar el evento.</span><span class="sxs-lookup"><span data-stu-id="8929c-120">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8929c-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8929c-121">Return value</span></span>

<span data-ttu-id="8929c-122">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="8929c-122">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8929c-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8929c-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8929c-124">Las propiedades *PX* y *py* se encuentran en píxeles, y no las unidades HIMETRIC asociadas al espacio de la tinta.</span><span class="sxs-lookup"><span data-stu-id="8929c-124">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="8929c-125">Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación que no tiene en cuenta el lápiz y este tipo de aplicación solo entiende píxeles.</span><span class="sxs-lookup"><span data-stu-id="8929c-125">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

<span data-ttu-id="8929c-126">Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ IPEMouseWheel.</span><span class="sxs-lookup"><span data-stu-id="8929c-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="8929c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8929c-127">Requirements</span></span>



| <span data-ttu-id="8929c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8929c-128">Requirement</span></span> | <span data-ttu-id="8929c-129">Value</span><span class="sxs-lookup"><span data-stu-id="8929c-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8929c-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8929c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8929c-131">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8929c-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8929c-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8929c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8929c-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8929c-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="8929c-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8929c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8929c-135"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8929c-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8929c-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8929c-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="8929c-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8929c-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="8929c-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="8929c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8929c-139">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="8929c-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="8929c-140">**Enumeración InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="8929c-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="8929c-141">**Enumeración InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="8929c-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




