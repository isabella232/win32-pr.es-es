---
description: 'Evento InkPicture.CursorButtonUp: se produce cuando InkCollector detecta un botón de cursor que está en marcha.'
ms.assetid: bb10b032-a88d-4b52-9062-c0b63dfe98e9
title: Evento InkPicture.CursorButtonUp (Msplaceut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 639d0cbd89e2ca44d8855b6508c5284f59a7c654
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086663"
---
# <a name="inkpicturecursorbuttonup-event"></a><span data-ttu-id="721e2-103">Evento InkPicture.CursorButtonUp</span><span class="sxs-lookup"><span data-stu-id="721e2-103">InkPicture.CursorButtonUp event</span></span>

<span data-ttu-id="721e2-104">Se produce cuando [**InkCollector detecta**](inkcollector-class.md) un botón de cursor que está en marcha.</span><span class="sxs-lookup"><span data-stu-id="721e2-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="721e2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="721e2-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="721e2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="721e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="721e2-107">*Cursor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="721e2-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="721e2-108">Objeto [**IInkCursor Interface que**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) generó el evento **CursorButtonUp.**</span><span class="sxs-lookup"><span data-stu-id="721e2-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonUp** event.</span></span>

</dd> <dt>

<span data-ttu-id="721e2-109">*Botón* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="721e2-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="721e2-110">Botón que se ha liberado.</span><span class="sxs-lookup"><span data-stu-id="721e2-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="721e2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="721e2-111">Return value</span></span>

<span data-ttu-id="721e2-112">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="721e2-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="721e2-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="721e2-113">Remarks</span></span>

<span data-ttu-id="721e2-114">Un botón de una punta de lápiz está arriba cuando el usuario completa un trazo y eleva el lápiz del digitalizador.</span><span class="sxs-lookup"><span data-stu-id="721e2-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="721e2-115">Un botón de un menú está en marcha cuando no se presiona el botón.</span><span class="sxs-lookup"><span data-stu-id="721e2-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="721e2-116">Cuando se suelta el botón derecho del mouse, se reciben dos eventos **CursorButtonUp:** uno para el botón derecho hacia arriba y otro para el botón izquierdo hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="721e2-116">When you release the right mouse button, you actually receive two **CursorButtonUp** events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="721e2-117">Este método de evento se define en las **\_ interfaces IInkCollectorEvents,** **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** con un identificador de \_ DISPID ICECursorButtonUp.</span><span class="sxs-lookup"><span data-stu-id="721e2-117">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispinterfaces with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="721e2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="721e2-118">Requirements</span></span>



| <span data-ttu-id="721e2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="721e2-119">Requirement</span></span> | <span data-ttu-id="721e2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="721e2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="721e2-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="721e2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="721e2-122">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="721e2-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="721e2-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="721e2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="721e2-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="721e2-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="721e2-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="721e2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="721e2-126"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="721e2-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="721e2-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="721e2-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="721e2-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="721e2-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="721e2-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="721e2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="721e2-130">InkPicture</span><span class="sxs-lookup"><span data-stu-id="721e2-130">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="721e2-131">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="721e2-131">**CursorButtonDown Event**</span></span>](inkpicture-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="721e2-132">**Evento CursorDown**</span><span class="sxs-lookup"><span data-stu-id="721e2-132">**CursorDown Event**</span></span>](inkpicture-cursordown.md)
</dt> <dt>

[<span data-ttu-id="721e2-133">**IInkCursor (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="721e2-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="721e2-134">**IInkCursorButton (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="721e2-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




