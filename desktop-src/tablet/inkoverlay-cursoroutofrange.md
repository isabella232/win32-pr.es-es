---
description: 'Evento InkOverlay.CursorOutOfRange: se produce cuando el cursor sale del intervalo de detección físico (proximidad) del contexto de la tableta.'
ms.assetid: c696b2a9-dc47-4b73-a556-9bb222f5bf59
title: Evento InkOverlay.CursorOutOfRange (Msplaceut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a30bfde1e96edfa286e9afeac147dc141c4942
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116963"
---
# <a name="inkoverlaycursoroutofrange-event"></a><span data-ttu-id="a1e66-103">Evento InkOverlay.CursorOutOfRange</span><span class="sxs-lookup"><span data-stu-id="a1e66-103">InkOverlay.CursorOutOfRange event</span></span>

<span data-ttu-id="a1e66-104">Se produce cuando el cursor sale del intervalo de detección físico (proximidad) del contexto de la tableta.</span><span class="sxs-lookup"><span data-stu-id="a1e66-104">Occurs when the cursor leaves the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1e66-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1e66-105">Syntax</span></span>


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a><span data-ttu-id="a1e66-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1e66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1e66-107">*Cursor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a1e66-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1e66-108">Objeto [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el [**evento CursorOutOfRange.**](inkcollector-cursoroutofrange.md)</span><span class="sxs-lookup"><span data-stu-id="a1e66-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1e66-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1e66-109">Return value</span></span>

<span data-ttu-id="a1e66-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="a1e66-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1e66-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a1e66-111">Remarks</span></span>

<span data-ttu-id="a1e66-112">Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ DE DISPID \_ ICECursorOutOfRange.</span><span class="sxs-lookup"><span data-stu-id="a1e66-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorOutOfRange.</span></span>

<span data-ttu-id="a1e66-113">El [**evento CursorOutOfRange**](inkcollector-cursoroutofrange.md) se desencadena incluso cuando está en modo de selección o borrado, no solo cuando está en modo de entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="a1e66-113">The [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="a1e66-114">Esto requiere que supervise el modo de edición (del que es responsable de la configuración) y tenga en cuenta el modo antes de interpretar el evento.</span><span class="sxs-lookup"><span data-stu-id="a1e66-114">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="a1e66-115">La ventaja de este requisito es una mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="a1e66-115">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1e66-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1e66-116">Requirements</span></span>



| <span data-ttu-id="a1e66-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1e66-117">Requirement</span></span> | <span data-ttu-id="a1e66-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a1e66-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1e66-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1e66-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a1e66-120">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="a1e66-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a1e66-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1e66-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a1e66-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a1e66-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a1e66-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1e66-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1e66-124"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="a1e66-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a1e66-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1e66-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="a1e66-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1e66-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a1e66-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a1e66-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1e66-128">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="a1e66-128">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="a1e66-129">**Evento CursorInRange**</span><span class="sxs-lookup"><span data-stu-id="a1e66-129">**CursorInRange Event**</span></span>](inkcollector-cursorinrange.md)
</dt> <dt>

[<span data-ttu-id="a1e66-130">**IInkCursor (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="a1e66-130">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




