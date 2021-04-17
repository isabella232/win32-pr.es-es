---
description: Se produce cuando el objeto InkOverlay o el control InkPicture han terminado de volver a dibujarse.
ms.assetid: de3c69de-4a33-46e4-96e5-462805681bda
title: Evento InkOverlay. pintado (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3de0628679aa034b16a3562aa08cdbd1928653ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498076"
---
# <a name="inkoverlaypainted-event"></a><span data-ttu-id="e1670-103">InkOverlay. pintado (evento)</span><span class="sxs-lookup"><span data-stu-id="e1670-103">InkOverlay.Painted event</span></span>

<span data-ttu-id="e1670-104">Se produce cuando el objeto [**InkOverlay**](inkoverlay-class.md) o el control [InkPicture](inkpicture-control-reference.md) han terminado de volver a dibujarse.</span><span class="sxs-lookup"><span data-stu-id="e1670-104">Occurs when the [**InkOverlay**](inkoverlay-class.md) object or [InkPicture](inkpicture-control-reference.md) control has completed redrawing itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1670-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1670-105">Syntax</span></span>


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a><span data-ttu-id="e1670-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1670-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1670-107">*HDC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e1670-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1670-108">Contexto de dispositivo en el que se produjo el evento.</span><span class="sxs-lookup"><span data-stu-id="e1670-108">The device context on which the event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="e1670-109">*Rectángulo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e1670-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1670-110">[**InkRectangle**](inkrectangle-class.md) que se ha repintado.</span><span class="sxs-lookup"><span data-stu-id="e1670-110">The [**InkRectangle**](inkrectangle-class.md) that was repainted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1670-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1670-111">Return value</span></span>

<span data-ttu-id="e1670-112">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="e1670-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1670-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1670-113">Remarks</span></span>

<span data-ttu-id="e1670-114">Este método de evento se define en las \_ \_ interfaces de solo envío IInkOverlayEvents y IInkPictureEvents (dispinterfaces) con un identificador de DISPID \_ IOEPainted.</span><span class="sxs-lookup"><span data-stu-id="e1670-114">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEPainted.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1670-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1670-115">Requirements</span></span>



| <span data-ttu-id="e1670-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1670-116">Requirement</span></span> | <span data-ttu-id="e1670-117">Value</span><span class="sxs-lookup"><span data-stu-id="e1670-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1670-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1670-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e1670-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e1670-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e1670-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1670-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e1670-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e1670-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e1670-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1670-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1670-123"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e1670-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e1670-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e1670-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="e1670-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1670-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e1670-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1670-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1670-127">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="e1670-127">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




