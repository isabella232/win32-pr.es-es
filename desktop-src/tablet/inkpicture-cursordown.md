---
description: Se produce cuando la sugerencia del cursor se pone en contacto con la superficie de la tableta de la digitalización.
ms.assetid: 6d524400-1341-45da-86b2-098e34ed5a1c
title: Evento InkPicture. CursorDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15724f0a71e801393ca8e93100ba2105da9ff2b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546555"
---
# <a name="inkpicturecursordown-event"></a><span data-ttu-id="d1f7d-103">Evento InkPicture. CursorDown</span><span class="sxs-lookup"><span data-stu-id="d1f7d-103">InkPicture.CursorDown event</span></span>

<span data-ttu-id="d1f7d-104">Se produce cuando la sugerencia del cursor se pone en contacto con la superficie de la tableta de la digitalización.</span><span class="sxs-lookup"><span data-stu-id="d1f7d-104">Occurs when the cursor tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1f7d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1f7d-105">Syntax</span></span>


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a><span data-ttu-id="d1f7d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1f7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1f7d-107">*Cursor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d1f7d-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1f7d-108">El objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento **CursorDown** .</span><span class="sxs-lookup"><span data-stu-id="d1f7d-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="d1f7d-109">*Trazo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d1f7d-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1f7d-110">El objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que se inició cuando el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) provocó que se activara el evento **CursorDown** .</span><span class="sxs-lookup"><span data-stu-id="d1f7d-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that was started when the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object caused the **CursorDown** event to fire.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1f7d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1f7d-111">Return value</span></span>

<span data-ttu-id="d1f7d-112">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="d1f7d-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1f7d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1f7d-113">Remarks</span></span>

<span data-ttu-id="d1f7d-114">Estos métodos de evento se definen en las interfaces **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="d1f7d-114">These event methods are defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** interfaces.</span></span> <span data-ttu-id="d1f7d-115">Las interfaces **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** implementan la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ ICECursorDown.</span><span class="sxs-lookup"><span data-stu-id="d1f7d-115">The **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** interfaces implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_ICECursorDown.</span></span>

<span data-ttu-id="d1f7d-116">Utilice este evento con precaución, ya que podría tener un efecto adverso en el rendimiento de las entradas manuscritas si se ejecuta demasiado código en los controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="d1f7d-116">Use this event carefully because it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span> <span data-ttu-id="d1f7d-117">Para mejorar el rendimiento del lápiz en tiempo real, oculte o muestre el cursor del mouse en los controladores de eventos [**MouseDown**](inkpicture-mousedown.md) y [**MouseUp**](inkpicture-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="d1f7d-117">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) event handlers.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1f7d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1f7d-118">Requirements</span></span>



| <span data-ttu-id="d1f7d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1f7d-119">Requirement</span></span> | <span data-ttu-id="d1f7d-120">Value</span><span class="sxs-lookup"><span data-stu-id="d1f7d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1f7d-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1f7d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d1f7d-122">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d1f7d-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d1f7d-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1f7d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d1f7d-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d1f7d-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d1f7d-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1f7d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1f7d-126"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d1f7d-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d1f7d-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d1f7d-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="d1f7d-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1f7d-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d1f7d-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1f7d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1f7d-130">InkPicture</span><span class="sxs-lookup"><span data-stu-id="d1f7d-130">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="d1f7d-131">**Evento CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="d1f7d-131">**CursorButtonUp Event**</span></span>](inkpicture-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="d1f7d-132">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="d1f7d-132">**CursorButtonDown Event**</span></span>](inkpicture-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="d1f7d-133">**Interfaz IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="d1f7d-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="d1f7d-134">**Interfaz IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="d1f7d-134">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

