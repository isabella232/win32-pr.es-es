---
description: 'Evento InkOverlay.CursorButtonUp: se produce cuando InkCollector detecta un botón de cursor que está encendido.'
ms.assetid: ce7205f7-727c-4acf-a727-4dbb3cc42441
title: Evento InkOverlay.CursorButtonUp (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f22590362c6eb9a987da94bf3adb4e99943c12cd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086853"
---
# <a name="inkoverlaycursorbuttonup-event"></a><span data-ttu-id="b814a-103">Evento InkOverlay.CursorButtonUp</span><span class="sxs-lookup"><span data-stu-id="b814a-103">InkOverlay.CursorButtonUp event</span></span>

<span data-ttu-id="b814a-104">Se produce cuando [**InkCollector detecta**](inkcollector-class.md) un botón de cursor que está en marcha.</span><span class="sxs-lookup"><span data-stu-id="b814a-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="b814a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b814a-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="b814a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b814a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b814a-107">*Cursor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b814a-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b814a-108">Objeto [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el [**evento CursorButtonUp.**](inkcollector-cursorbuttonup.md)</span><span class="sxs-lookup"><span data-stu-id="b814a-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorButtonUp**](inkcollector-cursorbuttonup.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="b814a-109">*Botón* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b814a-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b814a-110">Botón que se ha liberado.</span><span class="sxs-lookup"><span data-stu-id="b814a-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b814a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b814a-111">Return value</span></span>

<span data-ttu-id="b814a-112">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="b814a-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b814a-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b814a-113">Remarks</span></span>

<span data-ttu-id="b814a-114">Un botón de una punta de lápiz está arriba cuando el usuario completa un trazo y eleva el lápiz del digitalizador.</span><span class="sxs-lookup"><span data-stu-id="b814a-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="b814a-115">Un botón de un cilindro está en marcha cuando no se presiona el botón.</span><span class="sxs-lookup"><span data-stu-id="b814a-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="b814a-116">Cuando suelte el botón derecho del mouse, recibirá dos eventos [**CursorButtonUp:**](inkcollector-cursorbuttonup.md) uno para el botón derecho hacia arriba y otro para el botón izquierdo hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="b814a-116">When you release the right mouse button, you actually receive two [**CursorButtonUp**](inkcollector-cursorbuttonup.md) events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="b814a-117">Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ DE DISPID \_ ICECursorButtonUp.</span><span class="sxs-lookup"><span data-stu-id="b814a-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="b814a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b814a-118">Requirements</span></span>



| <span data-ttu-id="b814a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b814a-119">Requirement</span></span> | <span data-ttu-id="b814a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b814a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b814a-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b814a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b814a-122">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="b814a-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b814a-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b814a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b814a-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b814a-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b814a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b814a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b814a-126"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="b814a-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b814a-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b814a-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="b814a-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b814a-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b814a-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b814a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b814a-130">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="b814a-130">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="b814a-131">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="b814a-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="b814a-132">**Evento CursorDown**</span><span class="sxs-lookup"><span data-stu-id="b814a-132">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="b814a-133">**IInkCursor (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="b814a-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="b814a-134">**IInkCursorButton (Interfaz)**</span><span class="sxs-lookup"><span data-stu-id="b814a-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




