---
description: Se produce cuando un usuario hace clic en el control InkPicture.
ms.assetid: 326bac37-2d5d-434b-916c-8a675bab5052
title: Evento InkPicture. click (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1dd90cd69555f65531f5ab2684f886dab23e191
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912346"
---
# <a name="inkpictureclick-event"></a><span data-ttu-id="b6bc4-103">InkPicture. click (evento)</span><span class="sxs-lookup"><span data-stu-id="b6bc4-103">InkPicture.Click event</span></span>

<span data-ttu-id="b6bc4-104">Se produce cuando un usuario hace clic en el control [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="b6bc4-104">Occurs when a user clicks the [InkPicture](inkpicture-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6bc4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6bc4-105">Syntax</span></span>


```C++
void Click();
```



## <a name="parameters"></a><span data-ttu-id="b6bc4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6bc4-106">Parameters</span></span>

<span data-ttu-id="b6bc4-107">Este evento no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b6bc4-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b6bc4-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6bc4-108">Return value</span></span>

<span data-ttu-id="b6bc4-109">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="b6bc4-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6bc4-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6bc4-110">Remarks</span></span>

<span data-ttu-id="b6bc4-111">Al hacer clic en un control, se generan eventos [**MouseDown**](inkpicture-mousedown.md) y [**MouseUp**](inkpicture-mouseup.md) además del evento click.</span><span class="sxs-lookup"><span data-stu-id="b6bc4-111">Clicking a control generates [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) events in addition to the Click event.</span></span>

> [!Note]  
> <span data-ttu-id="b6bc4-112">Para distinguir entre los botones izquierdo, derecho e intermedio del mouse, use los eventos [**MouseDown**](inkpicture-mousedown.md) y [**MouseUp**](inkpicture-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="b6bc4-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) events.</span></span>

 

<span data-ttu-id="b6bc4-113">Si hay código en el evento **click** , el evento [**DblClick**](inkpicture-dblclick.md) nunca se desencadenará, porque el evento **click** es el primer evento que se va a desencadenar entre los dos.</span><span class="sxs-lookup"><span data-stu-id="b6bc4-113">If there is code in the **Click** event, the [**DblClick**](inkpicture-dblclick.md) event will never trigger, because the **Click** event is the first event to trigger between the two.</span></span> <span data-ttu-id="b6bc4-114">Como resultado, el evento **click** intercepta el clic del mouse, por lo que no se produce el evento **DblClick** .</span><span class="sxs-lookup"><span data-stu-id="b6bc4-114">As a result, the mouse click is intercepted by the **Click** event, so the **DblClick** event doesn't occur.</span></span>

<span data-ttu-id="b6bc4-115">Este método de evento se define en la interfaz **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="b6bc4-115">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="b6bc4-116">La interfaz **\_ IInkPictureEvents** implementa la interfaz IDispatch con un identificador de **DISPID \_ IPEClick**.</span><span class="sxs-lookup"><span data-stu-id="b6bc4-116">The **\_IInkPictureEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IPEClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6bc4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6bc4-117">Requirements</span></span>



| <span data-ttu-id="b6bc4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6bc4-118">Requirement</span></span> | <span data-ttu-id="b6bc4-119">Value</span><span class="sxs-lookup"><span data-stu-id="b6bc4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6bc4-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6bc4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b6bc4-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b6bc4-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b6bc4-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6bc4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b6bc4-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b6bc4-123">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b6bc4-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6bc4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6bc4-125"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b6bc4-125"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b6bc4-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b6bc4-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6bc4-127"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6bc4-127"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b6bc4-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6bc4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6bc4-129">InkPicture</span><span class="sxs-lookup"><span data-stu-id="b6bc4-129">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




