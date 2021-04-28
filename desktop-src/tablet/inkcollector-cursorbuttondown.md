---
description: 'Evento InkCollector.CursorButtonDown: se produce cuando la clase InkCollector detecta un botón de cursor que está fuera de servicio.'
ms.assetid: 65e7f68b-f911-4634-b850-178eb6eaf86e
title: Evento InkCollector.CursorButtonDown (Msplaceut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd1a820445a1ba3ed07dad8a22a11ad86e8da96f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110333"
---
# <a name="inkcollectorcursorbuttondown-event"></a><span data-ttu-id="5168c-103">Evento InkCollector.CursorButtonDown</span><span class="sxs-lookup"><span data-stu-id="5168c-103">InkCollector.CursorButtonDown event</span></span>

<span data-ttu-id="5168c-104">Se produce cuando [**la clase InkCollector**](inkcollector-class.md) detecta un botón de cursor que está fuera de servicio.</span><span class="sxs-lookup"><span data-stu-id="5168c-104">Occurs when the [**InkCollector Class**](inkcollector-class.md) detects a cursor button that is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="5168c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5168c-105">Syntax</span></span>


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="5168c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5168c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5168c-107">*Cursor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="5168c-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5168c-108">Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento CursorButtonDown.**</span><span class="sxs-lookup"><span data-stu-id="5168c-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="5168c-109">*Botón* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="5168c-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5168c-110">Botón que se presionó.</span><span class="sxs-lookup"><span data-stu-id="5168c-110">The button that was pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5168c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5168c-111">Return value</span></span>

<span data-ttu-id="5168c-112">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="5168c-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5168c-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5168c-113">Remarks</span></span>

<span data-ttu-id="5168c-114">Un botón de una punta de lápiz está abajo cuando el usuario baja el lápiz al digitalizador y comienza a realizar el seguimiento de un trazo.</span><span class="sxs-lookup"><span data-stu-id="5168c-114">A button on a pen tip is down when the user lowers the pen to the digitizer and starts tracing a stroke.</span></span> <span data-ttu-id="5168c-115">Un botón de un menú está apagado cuando se presiona el botón.</span><span class="sxs-lookup"><span data-stu-id="5168c-115">A button on a barrel is down when the button is pressed.</span></span>

<span data-ttu-id="5168c-116">Al presionar el botón derecho del mouse, recibe dos eventos **CursorButtonDown:** uno para el botón derecho presionado y otro para el botón izquierdo presionado.</span><span class="sxs-lookup"><span data-stu-id="5168c-116">When you press the right mouse button, you actually receive two **CursorButtonDown** events - one for right button pressed and one for left button pressed.</span></span>

<span data-ttu-id="5168c-117">Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ DE \_ DISPID ICECursorButtonDown.</span><span class="sxs-lookup"><span data-stu-id="5168c-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="5168c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5168c-118">Requirements</span></span>



| <span data-ttu-id="5168c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5168c-119">Requirement</span></span> | <span data-ttu-id="5168c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5168c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5168c-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5168c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5168c-122">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="5168c-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5168c-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5168c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5168c-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5168c-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="5168c-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5168c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5168c-126"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="5168c-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5168c-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5168c-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="5168c-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5168c-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="5168c-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5168c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5168c-130">**InkCollector (clase)**</span><span class="sxs-lookup"><span data-stu-id="5168c-130">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="5168c-131">**Evento CursorDown**</span><span class="sxs-lookup"><span data-stu-id="5168c-131">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="5168c-132">**Evento CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="5168c-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="5168c-133">**IInkCursor (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="5168c-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="5168c-134">**IInkCursorButton (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="5168c-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




