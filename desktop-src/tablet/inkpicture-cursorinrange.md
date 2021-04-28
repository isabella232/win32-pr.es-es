---
description: 'Evento InkPicture.CursorInRange: se produce cuando un cursor entra en el intervalo de detección física (proximidad) del contexto de la tableta.'
ms.assetid: e921e175-a2cf-45e6-bb81-dc82e384d3b1
title: Evento InkPicture.CursorInRange (Msiguaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05d703022e8d97df0d8d74a73e20af3d91b8531
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086583"
---
# <a name="inkpicturecursorinrange-event"></a><span data-ttu-id="dee0e-103">Evento InkPicture.CursorInRange</span><span class="sxs-lookup"><span data-stu-id="dee0e-103">InkPicture.CursorInRange event</span></span>

<span data-ttu-id="dee0e-104">Se produce cuando un cursor entra en el intervalo de detección física (proximidad) del contexto de la tableta.</span><span class="sxs-lookup"><span data-stu-id="dee0e-104">Occurs when a cursor enters the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="dee0e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dee0e-105">Syntax</span></span>


```C++
void CursorInRange(
  [in] IInkCursor   *Cursor,
  [in] VARIANT_BOOL NewCursor,
  [in] VARIANT      ButtonsState
);
```



## <a name="parameters"></a><span data-ttu-id="dee0e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dee0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dee0e-107">*Cursor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="dee0e-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dee0e-108">Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento CursorInRange.**</span><span class="sxs-lookup"><span data-stu-id="dee0e-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorInRange** event.</span></span>

</dd> <dt>

<span data-ttu-id="dee0e-109">*NewCursor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="dee0e-109">*NewCursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dee0e-110">**VARIANT \_ TRUE** si es la primera vez que este recopilador de entrada de lápiz entra en contacto con el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento CursorInRange;** de lo contrario, **VARIANT \_ FALSE**.</span><span class="sxs-lookup"><span data-stu-id="dee0e-110">**VARIANT\_TRUE** if this is the first time this ink collector has come in contact with the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorInRange** event; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="dee0e-111">*ButtonsState* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="dee0e-111">*ButtonsState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dee0e-112">Estado de los botones del cursor que generó el **evento CursorInRange.**</span><span class="sxs-lookup"><span data-stu-id="dee0e-112">The state of the buttons for the cursor that generated the **CursorInRange** event.</span></span>

<span data-ttu-id="dee0e-113">Para obtener más información sobre la estructura VARIANT, vea [Usar la biblioteca COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="dee0e-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dee0e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dee0e-114">Return value</span></span>

<span data-ttu-id="dee0e-115">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="dee0e-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dee0e-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dee0e-116">Remarks</span></span>

<span data-ttu-id="dee0e-117">Este método de evento se define en **\_ IInkCollectorEvents,** **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** interfaz de solo distribución (dispinterfaces) con un identificador DE DISPID \_ ICECursorInRange.</span><span class="sxs-lookup"><span data-stu-id="dee0e-117">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interface (dispinterfaces) with an ID of DISPID\_ICECursorInRange.</span></span>

<span data-ttu-id="dee0e-118">El **evento CursorInRange** se desencadena incluso cuando está en modo de selección o borrado, no solo cuando está en modo de lápiz.</span><span class="sxs-lookup"><span data-stu-id="dee0e-118">The **CursorInRange** event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="dee0e-119">Esto requiere que supervise el modo de edición (del que es responsable de la configuración) y tenga en cuenta el modo antes de interpretar el evento.</span><span class="sxs-lookup"><span data-stu-id="dee0e-119">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="dee0e-120">La ventaja de este requisito es una mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="dee0e-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="dee0e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dee0e-121">Requirements</span></span>



| <span data-ttu-id="dee0e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dee0e-122">Requirement</span></span> | <span data-ttu-id="dee0e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="dee0e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dee0e-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dee0e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dee0e-125">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="dee0e-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="dee0e-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dee0e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dee0e-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="dee0e-127">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="dee0e-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dee0e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="dee0e-129"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="dee0e-129"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="dee0e-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dee0e-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="dee0e-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dee0e-131"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="dee0e-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dee0e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dee0e-133">InkPicture</span><span class="sxs-lookup"><span data-stu-id="dee0e-133">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="dee0e-134">**Evento CursorOutOfRange**</span><span class="sxs-lookup"><span data-stu-id="dee0e-134">**CursorOutOfRange Event**</span></span>](inkpicture-cursoroutofrange.md)
</dt> <dt>

[<span data-ttu-id="dee0e-135">**InkCursorButtonState (Enumeración)**</span><span class="sxs-lookup"><span data-stu-id="dee0e-135">**InkCursorButtonState Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[<span data-ttu-id="dee0e-136">**IInkCursor (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="dee0e-136">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




