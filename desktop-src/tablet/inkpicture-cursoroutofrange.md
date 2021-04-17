---
description: Se produce cuando el cursor deja el intervalo de detección física (proximidad) del contexto de la tableta.
ms.assetid: 0c71a4ad-3c09-4134-b0e7-82f29e8913ed
title: Evento InkPicture. CursorOutOfRange (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e6a3eb09ca54fcfc4df3135896ea14f9bf56570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697555"
---
# <a name="inkpicturecursoroutofrange-event"></a><span data-ttu-id="3998e-103">Evento InkPicture. CursorOutOfRange</span><span class="sxs-lookup"><span data-stu-id="3998e-103">InkPicture.CursorOutOfRange event</span></span>

<span data-ttu-id="3998e-104">Se produce cuando el cursor deja el intervalo de detección física (proximidad) del contexto de la tableta.</span><span class="sxs-lookup"><span data-stu-id="3998e-104">Occurs when the cursor leaves the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="3998e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3998e-105">Syntax</span></span>


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a><span data-ttu-id="3998e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3998e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3998e-107">*Cursor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3998e-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3998e-108">Objeto de [**interfaz IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento **CursorOutOfRange** .</span><span class="sxs-lookup"><span data-stu-id="3998e-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorOutOfRange** event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3998e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3998e-109">Return value</span></span>

<span data-ttu-id="3998e-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="3998e-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3998e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3998e-111">Remarks</span></span>

<span data-ttu-id="3998e-112">Este método de evento se define en las interfaces de solo distribución (dispinterfaces) **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** con el identificador DISPID \_ ICECursorOutOfRange.</span><span class="sxs-lookup"><span data-stu-id="3998e-112">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorOutOfRange.</span></span>

<span data-ttu-id="3998e-113">El evento **CursorOutOfRange** se desencadena incluso en el modo de selección o borrado, no solo en el modo de entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="3998e-113">The **CursorOutOfRange** event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="3998e-114">Esto requiere que supervise el modo de edición (que es responsable de establecer) y tenga en cuenta el modo antes de interpretar el evento.</span><span class="sxs-lookup"><span data-stu-id="3998e-114">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="3998e-115">La ventaja de este requisito es mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de plataforma.</span><span class="sxs-lookup"><span data-stu-id="3998e-115">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="3998e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3998e-116">Requirements</span></span>



| <span data-ttu-id="3998e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3998e-117">Requirement</span></span> | <span data-ttu-id="3998e-118">Value</span><span class="sxs-lookup"><span data-stu-id="3998e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3998e-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3998e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3998e-120">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3998e-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3998e-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3998e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3998e-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3998e-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3998e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3998e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3998e-124"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3998e-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3998e-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3998e-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="3998e-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3998e-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3998e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3998e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3998e-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="3998e-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="3998e-129">**Evento CursorInRange**</span><span class="sxs-lookup"><span data-stu-id="3998e-129">**CursorInRange Event**</span></span>](inkpicture-cursorinrange.md)
</dt> <dt>

[<span data-ttu-id="3998e-130">**Interfaz IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="3998e-130">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




