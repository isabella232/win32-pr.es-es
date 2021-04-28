---
description: 'Evento InkOverlay.CursorButtonDown: se produce cuando la clase InkCollector detecta un botón de cursor que está apagado.'
ms.assetid: 993b84a3-a5ac-4b00-bfb4-26ca1c9727c6
title: Evento InkOverlay.CursorButtonDown (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcae13afb67be0312959939e0793d89d99c841ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117083"
---
# <a name="inkoverlaycursorbuttondown-event"></a><span data-ttu-id="25573-103">Evento InkOverlay.CursorButtonDown</span><span class="sxs-lookup"><span data-stu-id="25573-103">InkOverlay.CursorButtonDown event</span></span>

<span data-ttu-id="25573-104">Se produce cuando [**la clase InkCollector**](inkcollector-class.md) detecta un botón de cursor que está apagado.</span><span class="sxs-lookup"><span data-stu-id="25573-104">Occurs when the [**InkCollector Class**](inkcollector-class.md) detects a cursor button that is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="25573-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25573-105">Syntax</span></span>


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="25573-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25573-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25573-107">*Cursor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="25573-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25573-108">Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el [**evento CursorButtonDown.**](inkcollector-cursorbuttondown.md)</span><span class="sxs-lookup"><span data-stu-id="25573-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorButtonDown**](inkcollector-cursorbuttondown.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="25573-109">*Botón* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="25573-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25573-110">Botón que se presionó.</span><span class="sxs-lookup"><span data-stu-id="25573-110">The button that was pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25573-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25573-111">Return value</span></span>

<span data-ttu-id="25573-112">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="25573-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="25573-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="25573-113">Remarks</span></span>

<span data-ttu-id="25573-114">Un botón de una punta de lápiz está abajo cuando el usuario baja el lápiz al digitalizador y comienza a realizar el seguimiento de un trazo.</span><span class="sxs-lookup"><span data-stu-id="25573-114">A button on a pen tip is down when the user lowers the pen to the digitizer and starts tracing a stroke.</span></span> <span data-ttu-id="25573-115">Un botón de un cilindro está apagado cuando se presiona el botón.</span><span class="sxs-lookup"><span data-stu-id="25573-115">A button on a barrel is down when the button is pressed.</span></span>

<span data-ttu-id="25573-116">Al presionar el botón derecho del mouse, se reciben dos eventos [**CursorButtonDown:**](inkcollector-cursorbuttondown.md) uno para el botón derecho presionado y otro para el botón izquierdo presionado.</span><span class="sxs-lookup"><span data-stu-id="25573-116">When you press the right mouse button, you actually receive two [**CursorButtonDown**](inkcollector-cursorbuttondown.md) events - one for right button pressed and one for left button pressed.</span></span>

<span data-ttu-id="25573-117">Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ DE DISPID \_ ICECursorButtonDown.</span><span class="sxs-lookup"><span data-stu-id="25573-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="25573-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25573-118">Requirements</span></span>



| <span data-ttu-id="25573-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="25573-119">Requirement</span></span> | <span data-ttu-id="25573-120">Valor</span><span class="sxs-lookup"><span data-stu-id="25573-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25573-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25573-121">Minimum supported client</span></span><br/> | <span data-ttu-id="25573-122">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="25573-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="25573-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25573-123">Minimum supported server</span></span><br/> | <span data-ttu-id="25573-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="25573-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="25573-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25573-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="25573-126"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="25573-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="25573-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="25573-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="25573-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25573-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="25573-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="25573-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25573-130">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="25573-130">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="25573-131">**Evento CursorDown**</span><span class="sxs-lookup"><span data-stu-id="25573-131">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="25573-132">**Evento CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="25573-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="25573-133">**IInkCursor (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="25573-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="25573-134">**IInkCursorButton (Interfaz)**</span><span class="sxs-lookup"><span data-stu-id="25573-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




