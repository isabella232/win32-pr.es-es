---
description: Se produce cuando el puntero del mouse se mueve sobre el control InkPicture.
ms.assetid: b4c703da-0e4a-4d4c-9a6c-0e002344fb2f
title: Evento InkPicture. MouseMove (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c5540831594674dd279fc14e822d6b3240b014c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277396"
---
# <a name="inkpicturemousemove-event"></a><span data-ttu-id="e0506-103">Evento InkPicture. MouseMove</span><span class="sxs-lookup"><span data-stu-id="e0506-103">InkPicture.MouseMove event</span></span>

<span data-ttu-id="e0506-104">Se produce cuando el puntero del mouse se mueve sobre el control [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="e0506-104">Occurs when the mouse pointer is moved over the [InkPicture](inkpicture-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0506-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0506-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="e0506-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0506-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0506-107">*Botón* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e0506-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0506-108">Botón que se presionó.</span><span class="sxs-lookup"><span data-stu-id="e0506-108">The button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="e0506-109">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0506-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0506-110">Estado de la tecla Mayús.</span><span class="sxs-lookup"><span data-stu-id="e0506-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="e0506-111">*PX* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0506-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0506-112">La coordenada x, en píxeles, del objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="e0506-112">The x-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="e0506-113">*py* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0506-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0506-114">La coordenada y, en píxeles, del objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="e0506-114">The y-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="e0506-115">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e0506-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0506-116">**Variante \_ TRUE** para cancelar este evento para el control primario; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="e0506-116">**VARIANT\_TRUE** to cancel this event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0506-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0506-117">Return value</span></span>

<span data-ttu-id="e0506-118">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="e0506-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0506-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0506-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e0506-120">Los parámetros *PX* y *py* se encuentran en píxeles, y no las unidades HIMETRIC asociadas con el sistema de coordenadas de espacio de tinta.</span><span class="sxs-lookup"><span data-stu-id="e0506-120">The parameters *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space coordinate system.</span></span> <span data-ttu-id="e0506-121">Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación que no es compatible con el lápiz y ese tipo de aplicación solo hace referencia a píxeles.</span><span class="sxs-lookup"><span data-stu-id="e0506-121">This is because this event replaces the related mouse event of an application that is not pen-aware, and that type of application refers only to pixels.</span></span>

 

> [!Caution]  
> <span data-ttu-id="e0506-122">Algunos controles dependen de una relación específica entre los eventos [**MouseDown**](inkpicture-mousedown.md), **MouseMove** y [**MouseUp**](inkpicture-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="e0506-122">Some controls rely on a specific relationship between [**MouseDown**](inkpicture-mousedown.md), **MouseMove**, and [**MouseUp**](inkpicture-mouseup.md) events.</span></span> <span data-ttu-id="e0506-123">La cancelación de algunos de estos eventos puede tener resultados imprevistos.</span><span class="sxs-lookup"><span data-stu-id="e0506-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="e0506-124">Este método de evento se define en la interfaz **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="e0506-124">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="e0506-125">La interfaz **\_ IInkPictureEvents** implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IPEMouseDown.</span><span class="sxs-lookup"><span data-stu-id="e0506-125">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0506-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0506-126">Requirements</span></span>



| <span data-ttu-id="e0506-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0506-127">Requirement</span></span> | <span data-ttu-id="e0506-128">Value</span><span class="sxs-lookup"><span data-stu-id="e0506-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0506-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0506-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e0506-130">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e0506-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e0506-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0506-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e0506-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e0506-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e0506-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0506-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0506-134"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e0506-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e0506-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0506-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="e0506-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0506-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e0506-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0506-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0506-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="e0506-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

