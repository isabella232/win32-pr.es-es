---
description: Se produce cuando la rueda del mouse se mueve mientras el objeto InkCollector o InkOverlay tiene el foco.
ms.assetid: 418cf67c-0ec0-49e3-a17f-9eaeb40bb602
title: InkCollector. MouseWheel (evento) (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e6a6728bfcbe058ff5eab56499f6c8e885351
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705551"
---
# <a name="inkcollectormousewheel-event"></a><span data-ttu-id="2c062-103">InkCollector. MouseWheel (evento)</span><span class="sxs-lookup"><span data-stu-id="2c062-103">InkCollector.MouseWheel event</span></span>

<span data-ttu-id="2c062-104">Se produce cuando la rueda del mouse se mueve mientras el objeto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="2c062-104">Occurs when the mouse wheel moves while the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c062-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c062-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="2c062-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c062-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c062-107">*Botón* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2c062-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c062-108">Botón del mouse que se presionó.</span><span class="sxs-lookup"><span data-stu-id="2c062-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="2c062-109">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2c062-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c062-110">Estado de la tecla Mayús.</span><span class="sxs-lookup"><span data-stu-id="2c062-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="2c062-111">*Delta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2c062-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c062-112">Recuento con signo del número de pasos que ha girado la rueda del mouse.</span><span class="sxs-lookup"><span data-stu-id="2c062-112">A signed count of the number of detents the mouse wheel has rotated.</span></span> <span data-ttu-id="2c062-113">Un paso es una muesca de la rueda del mouse.</span><span class="sxs-lookup"><span data-stu-id="2c062-113">A detent is one notch of the mouse wheel.</span></span>

</dd> <dt>

<span data-ttu-id="2c062-114">*x* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="2c062-114">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c062-115">Coordenada x, en píxeles, de un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="2c062-115">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="2c062-116">*y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="2c062-116">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c062-117">Coordenada y, en píxeles, de un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="2c062-117">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="2c062-118">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2c062-118">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c062-119">**Variante \_ TRUE** para cancelar el evento para el control primario; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="2c062-119">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span> <span data-ttu-id="2c062-120">El valor predeterminado es **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="2c062-120">The default value is **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c062-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c062-121">Return value</span></span>

<span data-ttu-id="2c062-122">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="2c062-122">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c062-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c062-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2c062-124">Las propiedades *PX* y *py* se encuentran en píxeles, y no las unidades HIMETRIC asociadas al espacio de la tinta.</span><span class="sxs-lookup"><span data-stu-id="2c062-124">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="2c062-125">Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación que no tiene en cuenta el lápiz y este tipo de aplicación solo entiende píxeles.</span><span class="sxs-lookup"><span data-stu-id="2c062-125">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

<span data-ttu-id="2c062-126">Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ IPEMouseWheel.</span><span class="sxs-lookup"><span data-stu-id="2c062-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c062-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c062-127">Requirements</span></span>



| <span data-ttu-id="2c062-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c062-128">Requirement</span></span> | <span data-ttu-id="2c062-129">Value</span><span class="sxs-lookup"><span data-stu-id="2c062-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c062-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c062-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2c062-131">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2c062-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="2c062-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c062-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2c062-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2c062-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="2c062-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2c062-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c062-135"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2c062-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2c062-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2c062-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="2c062-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c062-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="2c062-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c062-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c062-139">**InkCollector (clase)**</span><span class="sxs-lookup"><span data-stu-id="2c062-139">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="2c062-140">**Enumeración InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="2c062-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="2c062-141">**Enumeración InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="2c062-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




