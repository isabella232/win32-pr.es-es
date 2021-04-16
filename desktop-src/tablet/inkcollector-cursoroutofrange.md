---
description: Se produce cuando el cursor deja el intervalo de detección física (proximidad) del contexto de la tableta.
ms.assetid: a3a570ed-570b-4579-b120-ed5457630bc2
title: InkCollector. CursorOutOfRange evento (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e2d6ee30a60c260d861cdc5c24e22d7b4b43b0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677365"
---
# <a name="inkcollectorcursoroutofrange-event"></a><span data-ttu-id="bea60-103">InkCollector. CursorOutOfRange, evento</span><span class="sxs-lookup"><span data-stu-id="bea60-103">InkCollector.CursorOutOfRange event</span></span>

<span data-ttu-id="bea60-104">Se produce cuando el cursor deja el intervalo de detección física (proximidad) del contexto de la tableta.</span><span class="sxs-lookup"><span data-stu-id="bea60-104">Occurs when the cursor leaves the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="bea60-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bea60-105">Syntax</span></span>


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a><span data-ttu-id="bea60-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bea60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bea60-107">*Cursor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="bea60-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bea60-108">Objeto de [**interfaz IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento **CursorOutOfRange** .</span><span class="sxs-lookup"><span data-stu-id="bea60-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorOutOfRange** event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bea60-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bea60-109">Return value</span></span>

<span data-ttu-id="bea60-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="bea60-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bea60-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bea60-111">Remarks</span></span>

<span data-ttu-id="bea60-112">Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ ICECursorOutOfRange.</span><span class="sxs-lookup"><span data-stu-id="bea60-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorOutOfRange.</span></span>

<span data-ttu-id="bea60-113">El evento **CursorOutOfRange** se desencadena incluso en el modo de selección o borrado, no solo en el modo de entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="bea60-113">The **CursorOutOfRange** event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="bea60-114">Esto requiere que supervise el modo de edición (que es responsable de establecer) y tenga en cuenta el modo antes de interpretar el evento.</span><span class="sxs-lookup"><span data-stu-id="bea60-114">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="bea60-115">La ventaja de este requisito es mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de plataforma.</span><span class="sxs-lookup"><span data-stu-id="bea60-115">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="bea60-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bea60-116">Requirements</span></span>



| <span data-ttu-id="bea60-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bea60-117">Requirement</span></span> | <span data-ttu-id="bea60-118">Value</span><span class="sxs-lookup"><span data-stu-id="bea60-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bea60-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bea60-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bea60-120">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bea60-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="bea60-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bea60-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bea60-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bea60-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="bea60-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bea60-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bea60-124"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bea60-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bea60-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bea60-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="bea60-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bea60-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="bea60-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="bea60-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bea60-128">**InkCollector (clase)**</span><span class="sxs-lookup"><span data-stu-id="bea60-128">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="bea60-129">**Evento CursorInRange**</span><span class="sxs-lookup"><span data-stu-id="bea60-129">**CursorInRange Event**</span></span>](inkcollector-cursorinrange.md)
</dt> <dt>

[<span data-ttu-id="bea60-130">**Interfaz IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="bea60-130">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




