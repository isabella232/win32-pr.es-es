---
description: Se produce antes de que se eliminen los objetos IInkStrokeDisp de la propiedad Ink.
ms.assetid: 747e0fdf-c68b-4805-bdc8-aa05e95ec0f7
title: Evento InkPicture. StrokesDeleting (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aef70e8526798f306f99c17b511b5c18c502858a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083108"
---
# <a name="inkpicturestrokesdeleting-event"></a><span data-ttu-id="28865-103">Evento InkPicture. StrokesDeleting</span><span class="sxs-lookup"><span data-stu-id="28865-103">InkPicture.StrokesDeleting event</span></span>

<span data-ttu-id="28865-104">Se produce antes de que se eliminen los objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) de la propiedad [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .</span><span class="sxs-lookup"><span data-stu-id="28865-104">Occurs before [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects are deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="28865-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28865-105">Syntax</span></span>


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a><span data-ttu-id="28865-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28865-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28865-107">*Trazos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="28865-107">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28865-108">Colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) eliminada cuando se desencadena el evento **StrokesDeleting** .</span><span class="sxs-lookup"><span data-stu-id="28865-108">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection deleted when the **StrokesDeleting** event fires.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28865-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28865-109">Return value</span></span>

<span data-ttu-id="28865-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="28865-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="28865-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28865-111">Remarks</span></span>

<span data-ttu-id="28865-112">Este método de evento se define en las interfaces de solo envío **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** (dispinterfaces) con un identificador de DISPID \_ IOEStrokesDeleting.</span><span class="sxs-lookup"><span data-stu-id="28865-112">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleting.</span></span>

## <a name="requirements"></a><span data-ttu-id="28865-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28865-113">Requirements</span></span>



| <span data-ttu-id="28865-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="28865-114">Requirement</span></span> | <span data-ttu-id="28865-115">Value</span><span class="sxs-lookup"><span data-stu-id="28865-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28865-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28865-116">Minimum supported client</span></span><br/> | <span data-ttu-id="28865-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="28865-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="28865-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28865-118">Minimum supported server</span></span><br/> | <span data-ttu-id="28865-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="28865-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="28865-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28865-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="28865-121"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="28865-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="28865-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="28865-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="28865-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28865-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="28865-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="28865-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28865-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="28865-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

