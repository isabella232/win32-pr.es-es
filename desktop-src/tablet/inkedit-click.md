---
description: Se produce cuando un usuario hace clic en el control InkEdit.
ms.assetid: 99fd7ef0-02cf-4390-9026-00ef2bbc1e37
title: Evento InkEdit. click (autodibujado. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55df62807ee78e0f083a301c83a756b4cffb729d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688300"
---
# <a name="inkeditclick-event"></a><span data-ttu-id="8d66b-103">Evento InkEdit. click</span><span class="sxs-lookup"><span data-stu-id="8d66b-103">InkEdit.Click event</span></span>

<span data-ttu-id="8d66b-104">Se produce cuando un usuario hace clic en el control [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="8d66b-104">Occurs when a user clicks the [InkEdit](inkedit-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d66b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d66b-105">Syntax</span></span>


```C++
void Click();
```



## <a name="parameters"></a><span data-ttu-id="8d66b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d66b-106">Parameters</span></span>

<span data-ttu-id="8d66b-107">Este evento no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8d66b-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8d66b-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d66b-108">Return value</span></span>

<span data-ttu-id="8d66b-109">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="8d66b-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d66b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d66b-110">Remarks</span></span>

<span data-ttu-id="8d66b-111">Al hacer clic en un control, se generan eventos [**MouseDown**](inkedit-mousedown.md) y [**MouseUp**](inkedit-mouseup.md) además del evento click.</span><span class="sxs-lookup"><span data-stu-id="8d66b-111">Clicking a control generates [**MouseDown**](inkedit-mousedown.md) and [**MouseUp**](inkedit-mouseup.md) events in addition to the Click event.</span></span>

> [!Note]  
> <span data-ttu-id="8d66b-112">Para distinguir entre los botones izquierdo, derecho e intermedio del mouse, use los eventos [**MouseDown**](inkedit-mousedown.md) y [**MouseUp**](inkedit-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="8d66b-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkedit-mousedown.md) and [**MouseUp**](inkedit-mouseup.md) events.</span></span>

 

<span data-ttu-id="8d66b-113">Si hay código en el evento **click** , el evento [**DblClick**](inkedit-dblclick.md) nunca se desencadenará, porque el evento **click** es el primer evento que se va a desencadenar entre los dos.</span><span class="sxs-lookup"><span data-stu-id="8d66b-113">If there is code in the **Click** event, the [**DblClick**](inkedit-dblclick.md) event will never trigger, because the **Click** event is the first event to trigger between the two.</span></span> <span data-ttu-id="8d66b-114">Como resultado, el evento **click** intercepta el clic del mouse, por lo que no se produce el evento **DblClick** .</span><span class="sxs-lookup"><span data-stu-id="8d66b-114">As a result, the mouse click is intercepted by the **Click** event, so the **DblClick** event doesn't occur.</span></span>

<span data-ttu-id="8d66b-115">Este método de evento se define en la interfaz **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="8d66b-115">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="8d66b-116">La interfaz **\_ IInkEditEvents** implementa la interfaz IDispatch con un identificador de **DISPID \_ IeeClick**.</span><span class="sxs-lookup"><span data-stu-id="8d66b-116">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IeeClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d66b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d66b-117">Requirements</span></span>



| <span data-ttu-id="8d66b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d66b-118">Requirement</span></span> | <span data-ttu-id="8d66b-119">Value</span><span class="sxs-lookup"><span data-stu-id="8d66b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d66b-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d66b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8d66b-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8d66b-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8d66b-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d66b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8d66b-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8d66b-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8d66b-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d66b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d66b-125"><dt>Autodibujado. h (también requiere la intermano \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8d66b-125"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8d66b-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8d66b-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="8d66b-127"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d66b-127"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8d66b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d66b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d66b-129">InkEdit</span><span class="sxs-lookup"><span data-stu-id="8d66b-129">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 




