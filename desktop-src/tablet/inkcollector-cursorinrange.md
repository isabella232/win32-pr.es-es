---
description: 'Evento InkCollector.CursorInRange: se produce cuando un cursor entra en el intervalo de detección físico (proximidad) del contexto de la tableta.'
ms.assetid: d05b240c-ba64-4008-b25d-e06c052eb5b0
title: Evento InkCollector.CursorInRange (Msplaceut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9b7cd6204b2dbb29f9a46e48ecb12569e1301f4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110293"
---
# <a name="inkcollectorcursorinrange-event"></a><span data-ttu-id="7ba55-103">Evento InkCollector.CursorInRange</span><span class="sxs-lookup"><span data-stu-id="7ba55-103">InkCollector.CursorInRange event</span></span>

<span data-ttu-id="7ba55-104">Se produce cuando un cursor entra en el intervalo de detección físico (proximidad) del contexto de la tableta.</span><span class="sxs-lookup"><span data-stu-id="7ba55-104">Occurs when a cursor enters the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ba55-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7ba55-105">Syntax</span></span>


```C++
void CursorInRange(
  [in] IInkCursor   *Cursor,
  [in] VARIANT_BOOL NewCursor,
  [in] VARIANT      ButtonsState
);
```



## <a name="parameters"></a><span data-ttu-id="7ba55-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7ba55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ba55-107">*Cursor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7ba55-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ba55-108">Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento CursorInRange.**</span><span class="sxs-lookup"><span data-stu-id="7ba55-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorInRange** event.</span></span>

</dd> <dt>

<span data-ttu-id="7ba55-109">*NewCursor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7ba55-109">*NewCursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ba55-110">**VARIANT \_ TRUE** para indicar que es la primera vez que este recopilador de entrada de lápiz entra en contacto con el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento CursorInRange.** en caso contrario, **VARIANT \_ FALSE**.</span><span class="sxs-lookup"><span data-stu-id="7ba55-110">**VARIANT\_TRUE** to indicate that this is the first time this ink collector has come in contact with the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorInRange** event; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="7ba55-111">*ButtonsState* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7ba55-111">*ButtonsState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ba55-112">Estado de los botones del cursor que generó el **evento CursorInRange.**</span><span class="sxs-lookup"><span data-stu-id="7ba55-112">The state of the buttons for the cursor that generated the **CursorInRange** event.</span></span>

<span data-ttu-id="7ba55-113">Para obtener más información sobre la estructura VARIANT, vea [Usar la biblioteca COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="7ba55-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ba55-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7ba55-114">Return value</span></span>

<span data-ttu-id="7ba55-115">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="7ba55-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ba55-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7ba55-116">Remarks</span></span>

<span data-ttu-id="7ba55-117">El método de evento TThis se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ \_ DE DISPID ICECursorInRange.</span><span class="sxs-lookup"><span data-stu-id="7ba55-117">TThis event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorInRange.</span></span>

<span data-ttu-id="7ba55-118">El **evento CursorInRange** se desencadena incluso en el modo de selección o borrado, no solo cuando está en modo de entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="7ba55-118">The **CursorInRange** event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="7ba55-119">Esto requiere que supervise el modo de edición (del que es responsable de la configuración) y tenga en cuenta el modo antes de interpretar el evento.</span><span class="sxs-lookup"><span data-stu-id="7ba55-119">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="7ba55-120">La ventaja de este requisito es una mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="7ba55-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ba55-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ba55-121">Requirements</span></span>



| <span data-ttu-id="7ba55-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ba55-122">Requirement</span></span> | <span data-ttu-id="7ba55-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7ba55-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ba55-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ba55-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7ba55-125">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="7ba55-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7ba55-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ba55-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7ba55-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7ba55-127">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="7ba55-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ba55-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ba55-129"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="7ba55-129"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7ba55-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ba55-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="7ba55-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ba55-131"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="7ba55-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7ba55-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ba55-133">**InkCollector (clase)**</span><span class="sxs-lookup"><span data-stu-id="7ba55-133">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="7ba55-134">**Evento CursorOutOfRange**</span><span class="sxs-lookup"><span data-stu-id="7ba55-134">**CursorOutOfRange Event**</span></span>](inkcollector-cursoroutofrange.md)
</dt> <dt>

[<span data-ttu-id="7ba55-135">**InkCursorButtonState (enumeración)**</span><span class="sxs-lookup"><span data-stu-id="7ba55-135">**InkCursorButtonState Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[<span data-ttu-id="7ba55-136">**IInkCursor (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="7ba55-136">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




