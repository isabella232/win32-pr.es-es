---
description: Se produce antes de que se eliminen los trazos de la propiedad de entrada de lápiz.
ms.assetid: 09468416-ad08-48ea-aa4a-3af0fe553f3d
title: Evento InkOverlay. StrokesDeleting (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64422e61869c633514c3e219e3d090476a693dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002715"
---
# <a name="inkoverlaystrokesdeleting-event"></a><span data-ttu-id="a3b9e-103">Evento InkOverlay. StrokesDeleting</span><span class="sxs-lookup"><span data-stu-id="a3b9e-103">InkOverlay.StrokesDeleting event</span></span>

<span data-ttu-id="a3b9e-104">Se produce antes de que se eliminen los trazos de la propiedad de [**entrada de lápiz**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .</span><span class="sxs-lookup"><span data-stu-id="a3b9e-104">Occurs before strokes are deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3b9e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3b9e-105">Syntax</span></span>


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a><span data-ttu-id="a3b9e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3b9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3b9e-107">*Trazos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a3b9e-107">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3b9e-108">Colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) eliminada cuando se desencadena el evento **StrokesDeleting** .</span><span class="sxs-lookup"><span data-stu-id="a3b9e-108">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection deleted when the **StrokesDeleting** event fires.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3b9e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3b9e-109">Return value</span></span>

<span data-ttu-id="a3b9e-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="a3b9e-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3b9e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3b9e-111">Remarks</span></span>

<span data-ttu-id="a3b9e-112">Este método de evento se define en las \_ \_ interfaces de solo envío IInkOverlayEvents y IInkPictureEvents (dispinterfaces) con un identificador de DISPID \_ IOEStrokesDeleting.</span><span class="sxs-lookup"><span data-stu-id="a3b9e-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleting.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3b9e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3b9e-113">Requirements</span></span>



| <span data-ttu-id="a3b9e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3b9e-114">Requirement</span></span> | <span data-ttu-id="a3b9e-115">Value</span><span class="sxs-lookup"><span data-stu-id="a3b9e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3b9e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3b9e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a3b9e-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a3b9e-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a3b9e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3b9e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a3b9e-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a3b9e-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a3b9e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3b9e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3b9e-121"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a3b9e-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a3b9e-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a3b9e-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="a3b9e-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3b9e-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a3b9e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3b9e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3b9e-125">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="a3b9e-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="a3b9e-126">[**Propiedad de entrada manuscrita \[ InkCollector/InkOverLay (clase)\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span><span class="sxs-lookup"><span data-stu-id="a3b9e-126">[**Ink Property \[InkCollector/InkOverLay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span></span>
</dt> </dl>

 

