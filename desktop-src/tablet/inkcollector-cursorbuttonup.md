---
description: Se produce cuando InkCollector detecta un botón de cursor que está activo.
ms.assetid: f07daad7-e0d1-45cf-a708-5486a5dfda8b
title: InkCollector. CursorButtonUp evento (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 932d768c13da953d1926b28fb651c63dc26be572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705467"
---
# <a name="inkcollectorcursorbuttonup-event"></a><span data-ttu-id="93598-103">InkCollector. CursorButtonUp, evento</span><span class="sxs-lookup"><span data-stu-id="93598-103">InkCollector.CursorButtonUp event</span></span>

<span data-ttu-id="93598-104">Se produce cuando [**InkCollector**](inkcollector-class.md) detecta un botón de cursor que está activo.</span><span class="sxs-lookup"><span data-stu-id="93598-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="93598-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93598-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="93598-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="93598-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93598-107">*Cursor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="93598-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93598-108">Objeto de [**interfaz IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento **CursorButtonUp** .</span><span class="sxs-lookup"><span data-stu-id="93598-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonUp** event.</span></span>

</dd> <dt>

<span data-ttu-id="93598-109">*Botón* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="93598-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93598-110">Botón que se liberó.</span><span class="sxs-lookup"><span data-stu-id="93598-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93598-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93598-111">Return value</span></span>

<span data-ttu-id="93598-112">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="93598-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="93598-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93598-113">Remarks</span></span>

<span data-ttu-id="93598-114">Un botón de una punta de lápiz está activo cuando el usuario completa un trazo y eleva el lápiz del digitalizador.</span><span class="sxs-lookup"><span data-stu-id="93598-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="93598-115">Un botón de un barril está activo cuando el botón no está presionado.</span><span class="sxs-lookup"><span data-stu-id="93598-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="93598-116">Al soltar el botón secundario del mouse, en realidad recibe dos eventos **CursorButtonUp** : uno para el botón derecho arriba y otro para el botón primario hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="93598-116">When you release the right mouse button, you actually receive two **CursorButtonUp** events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="93598-117">Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ ICECursorButtonUp.</span><span class="sxs-lookup"><span data-stu-id="93598-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="93598-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93598-118">Requirements</span></span>



| <span data-ttu-id="93598-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="93598-119">Requirement</span></span> | <span data-ttu-id="93598-120">Value</span><span class="sxs-lookup"><span data-stu-id="93598-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93598-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93598-121">Minimum supported client</span></span><br/> | <span data-ttu-id="93598-122">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="93598-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="93598-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93598-123">Minimum supported server</span></span><br/> | <span data-ttu-id="93598-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="93598-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="93598-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="93598-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="93598-126"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="93598-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="93598-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93598-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="93598-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93598-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="93598-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="93598-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93598-130">**InkCollector (clase)**</span><span class="sxs-lookup"><span data-stu-id="93598-130">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="93598-131">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="93598-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="93598-132">**Evento CursorDown**</span><span class="sxs-lookup"><span data-stu-id="93598-132">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="93598-133">**Interfaz IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="93598-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="93598-134">**Interfaz IInkCursorButton**</span><span class="sxs-lookup"><span data-stu-id="93598-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




