---
description: Se produce cuando InkCollector detecta un botón de cursor que está activo.
ms.assetid: ce7205f7-727c-4acf-a727-4dbb3cc42441
title: Evento InkOverlay. CursorButtonUp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8315f2cf87589bb24e5fb3c6ac6fd7128df426e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361334"
---
# <a name="inkoverlaycursorbuttonup-event"></a><span data-ttu-id="a1415-103">Evento InkOverlay. CursorButtonUp</span><span class="sxs-lookup"><span data-stu-id="a1415-103">InkOverlay.CursorButtonUp event</span></span>

<span data-ttu-id="a1415-104">Se produce cuando [**InkCollector**](inkcollector-class.md) detecta un botón de cursor que está activo.</span><span class="sxs-lookup"><span data-stu-id="a1415-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1415-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1415-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="a1415-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1415-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1415-107">*Cursor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a1415-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1415-108">Objeto de [**interfaz IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento [**CursorButtonUp**](inkcollector-cursorbuttonup.md) .</span><span class="sxs-lookup"><span data-stu-id="a1415-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorButtonUp**](inkcollector-cursorbuttonup.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="a1415-109">*Botón* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a1415-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1415-110">Botón que se liberó.</span><span class="sxs-lookup"><span data-stu-id="a1415-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1415-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1415-111">Return value</span></span>

<span data-ttu-id="a1415-112">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="a1415-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1415-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1415-113">Remarks</span></span>

<span data-ttu-id="a1415-114">Un botón de una punta de lápiz está activo cuando el usuario completa un trazo y eleva el lápiz del digitalizador.</span><span class="sxs-lookup"><span data-stu-id="a1415-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="a1415-115">Un botón de un barril está activo cuando el botón no está presionado.</span><span class="sxs-lookup"><span data-stu-id="a1415-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="a1415-116">Al soltar el botón secundario del mouse, en realidad recibe dos eventos [**CursorButtonUp**](inkcollector-cursorbuttonup.md) : uno para el botón derecho arriba y otro para el botón primario hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="a1415-116">When you release the right mouse button, you actually receive two [**CursorButtonUp**](inkcollector-cursorbuttonup.md) events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="a1415-117">Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ ICECursorButtonUp.</span><span class="sxs-lookup"><span data-stu-id="a1415-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1415-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1415-118">Requirements</span></span>



| <span data-ttu-id="a1415-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1415-119">Requirement</span></span> | <span data-ttu-id="a1415-120">Value</span><span class="sxs-lookup"><span data-stu-id="a1415-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1415-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1415-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a1415-122">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a1415-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a1415-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1415-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a1415-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a1415-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a1415-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1415-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1415-126"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a1415-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a1415-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1415-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="a1415-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1415-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a1415-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1415-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1415-130">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="a1415-130">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="a1415-131">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="a1415-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="a1415-132">**Evento CursorDown**</span><span class="sxs-lookup"><span data-stu-id="a1415-132">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="a1415-133">**Interfaz IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="a1415-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="a1415-134">**Interfaz IInkCursorButton**</span><span class="sxs-lookup"><span data-stu-id="a1415-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




