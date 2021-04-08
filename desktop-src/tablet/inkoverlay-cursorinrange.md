---
description: Se produce cuando un cursor entra en el intervalo de detección física (proximidad) del contexto de la tableta.
ms.assetid: 11327fef-1f5e-407a-812b-48f427af291e
title: Evento InkOverlay. CursorInRange (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b65745e93bfb7351f7e1fa6d01965ce7a271bc0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002717"
---
# <a name="inkoverlaycursorinrange-event"></a><span data-ttu-id="0bdb0-103">Evento InkOverlay. CursorInRange</span><span class="sxs-lookup"><span data-stu-id="0bdb0-103">InkOverlay.CursorInRange event</span></span>

<span data-ttu-id="0bdb0-104">Se produce cuando un cursor entra en el intervalo de detección física (proximidad) del contexto de la tableta.</span><span class="sxs-lookup"><span data-stu-id="0bdb0-104">Occurs when a cursor enters the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bdb0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0bdb0-105">Syntax</span></span>


```C++
void CursorInRange(
  [in] IInkCursor   *Cursor,
  [in] VARIANT_BOOL NewCursor,
  [in] VARIANT      ButtonsState
);
```



## <a name="parameters"></a><span data-ttu-id="0bdb0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0bdb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bdb0-107">*Cursor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0bdb0-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bdb0-108">El objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento [**CursorInRange**](inkcollector-cursorinrange.md) .</span><span class="sxs-lookup"><span data-stu-id="0bdb0-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorInRange**](inkcollector-cursorinrange.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="0bdb0-109">*NewCursor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0bdb0-109">*NewCursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bdb0-110">Indica si se trata de la primera vez que este recopilador de entrada de lápiz se pone en contacto con el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento [**CursorInRange**](inkcollector-cursorinrange.md) .</span><span class="sxs-lookup"><span data-stu-id="0bdb0-110">Whether this is the first time this ink collector has come in contact with the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorInRange**](inkcollector-cursorinrange.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="0bdb0-111">*ButtonsState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0bdb0-111">*ButtonsState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bdb0-112">El estado de los botones del cursor que generó el evento [**CursorInRange**](inkcollector-cursorinrange.md) .</span><span class="sxs-lookup"><span data-stu-id="0bdb0-112">The state of the buttons for the cursor that generated the [**CursorInRange**](inkcollector-cursorinrange.md) event.</span></span>

<span data-ttu-id="0bdb0-113">Para obtener más información sobre la estructura de variante, vea [usar la biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="0bdb0-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bdb0-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0bdb0-114">Return value</span></span>

<span data-ttu-id="0bdb0-115">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="0bdb0-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bdb0-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0bdb0-116">Remarks</span></span>

<span data-ttu-id="0bdb0-117">Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ ICECursorInRange.</span><span class="sxs-lookup"><span data-stu-id="0bdb0-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorInRange.</span></span>

<span data-ttu-id="0bdb0-118">El evento [**CursorInRange**](inkcollector-cursorinrange.md) se desencadena incluso en el modo de selección o borrado, no solo en el modo de entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="0bdb0-118">The [**CursorInRange**](inkcollector-cursorinrange.md) event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="0bdb0-119">Esto requiere que supervise el modo de edición (que es responsable de establecer) y tenga en cuenta el modo antes de interpretar el evento.</span><span class="sxs-lookup"><span data-stu-id="0bdb0-119">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="0bdb0-120">La ventaja de este requisito es mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de plataforma.</span><span class="sxs-lookup"><span data-stu-id="0bdb0-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bdb0-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bdb0-121">Requirements</span></span>



| <span data-ttu-id="0bdb0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bdb0-122">Requirement</span></span> | <span data-ttu-id="0bdb0-123">Value</span><span class="sxs-lookup"><span data-stu-id="0bdb0-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bdb0-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0bdb0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0bdb0-125">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0bdb0-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="0bdb0-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0bdb0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0bdb0-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0bdb0-127">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="0bdb0-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0bdb0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bdb0-129"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0bdb0-129"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0bdb0-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0bdb0-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="0bdb0-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bdb0-131"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="0bdb0-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="0bdb0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bdb0-133">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="0bdb0-133">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="0bdb0-134">**Evento CursorOutOfRange**</span><span class="sxs-lookup"><span data-stu-id="0bdb0-134">**CursorOutOfRange Event**</span></span>](inkcollector-cursoroutofrange.md)
</dt> <dt>

[<span data-ttu-id="0bdb0-135">**Enumeración InkCursorButtonState**</span><span class="sxs-lookup"><span data-stu-id="0bdb0-135">**InkCursorButtonState Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[<span data-ttu-id="0bdb0-136">**Interfaz IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="0bdb0-136">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




