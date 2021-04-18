---
description: Se produce cuando el cursor deja el intervalo de detección física (proximidad) del contexto de la tableta.
ms.assetid: c696b2a9-dc47-4b73-a556-9bb222f5bf59
title: Evento InkOverlay. CursorOutOfRange (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1510013d24bf092a08ba7d57b54c0f94bf7c2dcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707153"
---
# <a name="inkoverlaycursoroutofrange-event"></a><span data-ttu-id="a3836-103">Evento InkOverlay. CursorOutOfRange</span><span class="sxs-lookup"><span data-stu-id="a3836-103">InkOverlay.CursorOutOfRange event</span></span>

<span data-ttu-id="a3836-104">Se produce cuando el cursor deja el intervalo de detección física (proximidad) del contexto de la tableta.</span><span class="sxs-lookup"><span data-stu-id="a3836-104">Occurs when the cursor leaves the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3836-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3836-105">Syntax</span></span>


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a><span data-ttu-id="a3836-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3836-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3836-107">*Cursor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a3836-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3836-108">Objeto de [**interfaz IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) .</span><span class="sxs-lookup"><span data-stu-id="a3836-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3836-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3836-109">Return value</span></span>

<span data-ttu-id="a3836-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="a3836-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3836-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3836-111">Remarks</span></span>

<span data-ttu-id="a3836-112">Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ ICECursorOutOfRange.</span><span class="sxs-lookup"><span data-stu-id="a3836-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorOutOfRange.</span></span>

<span data-ttu-id="a3836-113">El evento [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) se desencadena incluso en el modo de selección o borrado, no solo en el modo de entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="a3836-113">The [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="a3836-114">Esto requiere que supervise el modo de edición (que es responsable de establecer) y tenga en cuenta el modo antes de interpretar el evento.</span><span class="sxs-lookup"><span data-stu-id="a3836-114">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="a3836-115">La ventaja de este requisito es mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de plataforma.</span><span class="sxs-lookup"><span data-stu-id="a3836-115">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3836-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3836-116">Requirements</span></span>



| <span data-ttu-id="a3836-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3836-117">Requirement</span></span> | <span data-ttu-id="a3836-118">Value</span><span class="sxs-lookup"><span data-stu-id="a3836-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3836-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3836-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a3836-120">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a3836-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a3836-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3836-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a3836-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a3836-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a3836-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3836-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3836-124"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a3836-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a3836-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a3836-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="a3836-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3836-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a3836-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3836-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3836-128">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="a3836-128">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="a3836-129">**Evento CursorInRange**</span><span class="sxs-lookup"><span data-stu-id="a3836-129">**CursorInRange Event**</span></span>](inkcollector-cursorinrange.md)
</dt> <dt>

[<span data-ttu-id="a3836-130">**Interfaz IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="a3836-130">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




