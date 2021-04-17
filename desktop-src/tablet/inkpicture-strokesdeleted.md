---
description: Se produce después de eliminar los objetos IInkStrokeDisp de la propiedad Ink.
ms.assetid: 395544e1-dc93-45d3-ac7a-d54712f3c027
title: Evento InkPicture. StrokesDeleted (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf98e51196d760f467d507c133429201883b340e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716911"
---
# <a name="inkpicturestrokesdeleted-event"></a><span data-ttu-id="7b935-103">Evento InkPicture. StrokesDeleted</span><span class="sxs-lookup"><span data-stu-id="7b935-103">InkPicture.StrokesDeleted event</span></span>

<span data-ttu-id="7b935-104">Se produce después de eliminar los objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) de la propiedad [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .</span><span class="sxs-lookup"><span data-stu-id="7b935-104">Occurs after [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects have been deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b935-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b935-105">Syntax</span></span>


```C++
void StrokesDeleted();
```



## <a name="parameters"></a><span data-ttu-id="7b935-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b935-106">Parameters</span></span>

<span data-ttu-id="7b935-107">Este evento no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7b935-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7b935-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b935-108">Return value</span></span>

<span data-ttu-id="7b935-109">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="7b935-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b935-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b935-110">Remarks</span></span>

<span data-ttu-id="7b935-111">No hay datos de evento.</span><span class="sxs-lookup"><span data-stu-id="7b935-111">There is no event data.</span></span>

<span data-ttu-id="7b935-112">Este método de evento se define en las interfaces de solo envío **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** (dispinterfaces) con un identificador de DISPID \_ IOEStrokesDeleted.</span><span class="sxs-lookup"><span data-stu-id="7b935-112">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b935-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b935-113">Requirements</span></span>



| <span data-ttu-id="7b935-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b935-114">Requirement</span></span> | <span data-ttu-id="7b935-115">Value</span><span class="sxs-lookup"><span data-stu-id="7b935-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b935-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b935-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7b935-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7b935-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7b935-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b935-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7b935-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7b935-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="7b935-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b935-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b935-121"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7b935-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7b935-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7b935-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="7b935-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b935-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="7b935-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b935-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b935-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="7b935-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




