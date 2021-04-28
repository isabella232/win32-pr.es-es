---
description: 'Evento InkPicture.CursorDown: se produce cuando la punta del cursor se pone en contacto con la superficie de la tableta de digitalización.'
ms.assetid: 6d524400-1341-45da-86b2-098e34ed5a1c
title: Evento InkPicture.CursorDown (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4b6128589ba2d0b87d4369e8bb58aa66eabf23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116703"
---
# <a name="inkpicturecursordown-event"></a><span data-ttu-id="98a96-103">Evento InkPicture.CursorDown</span><span class="sxs-lookup"><span data-stu-id="98a96-103">InkPicture.CursorDown event</span></span>

<span data-ttu-id="98a96-104">Se produce cuando la punta del cursor se pone en contacto con la superficie de la tableta de digitalización.</span><span class="sxs-lookup"><span data-stu-id="98a96-104">Occurs when the cursor tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="98a96-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98a96-105">Syntax</span></span>


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a><span data-ttu-id="98a96-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98a96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98a96-107">*Cursor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="98a96-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98a96-108">Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento CursorDown.**</span><span class="sxs-lookup"><span data-stu-id="98a96-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="98a96-109">*Trazo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="98a96-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98a96-110">Objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que se inició cuando el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) hizo que se iniciara el evento **CursorDown.**</span><span class="sxs-lookup"><span data-stu-id="98a96-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that was started when the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object caused the **CursorDown** event to fire.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98a96-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98a96-111">Return value</span></span>

<span data-ttu-id="98a96-112">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="98a96-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98a96-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="98a96-113">Remarks</span></span>

<span data-ttu-id="98a96-114">Estos métodos de evento se definen en las **\_ interfaces IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents.**</span><span class="sxs-lookup"><span data-stu-id="98a96-114">These event methods are defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** interfaces.</span></span> <span data-ttu-id="98a96-115">Las **\_ interfaces IInkCollectorEvents,** **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** implementan la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de \_ DISPID ICECursorDown.</span><span class="sxs-lookup"><span data-stu-id="98a96-115">The **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** interfaces implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_ICECursorDown.</span></span>

<span data-ttu-id="98a96-116">Use este evento con cuidado porque podría tener un efecto adverso en el rendimiento de la entrada de lápiz si se ejecuta demasiado código en los controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="98a96-116">Use this event carefully because it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span> <span data-ttu-id="98a96-117">Para mejorar el rendimiento de la entrada de lápiz en tiempo real, oculte o muestre el cursor del mouse en los controladores de eventos [**MouseDown**](inkpicture-mousedown.md) y [**MouseUp.**](inkpicture-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="98a96-117">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) event handlers.</span></span>

## <a name="requirements"></a><span data-ttu-id="98a96-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98a96-118">Requirements</span></span>



| <span data-ttu-id="98a96-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="98a96-119">Requirement</span></span> | <span data-ttu-id="98a96-120">Valor</span><span class="sxs-lookup"><span data-stu-id="98a96-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98a96-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98a96-121">Minimum supported client</span></span><br/> | <span data-ttu-id="98a96-122">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="98a96-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="98a96-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98a96-123">Minimum supported server</span></span><br/> | <span data-ttu-id="98a96-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="98a96-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="98a96-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98a96-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="98a96-126"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="98a96-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="98a96-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98a96-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="98a96-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98a96-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="98a96-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="98a96-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98a96-130">InkPicture</span><span class="sxs-lookup"><span data-stu-id="98a96-130">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="98a96-131">**Evento CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="98a96-131">**CursorButtonUp Event**</span></span>](inkpicture-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="98a96-132">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="98a96-132">**CursorButtonDown Event**</span></span>](inkpicture-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="98a96-133">**IInkCursor (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="98a96-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="98a96-134">**IInkStrokeDisp (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="98a96-134">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

