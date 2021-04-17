---
description: Se produce cuando se hace doble clic en el control InkEdit.
ms.assetid: 380499e4-8697-4823-8153-29f24b2f234c
title: Evento InkEdit. DblClick (autodibujado. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fee0ec42171c9abbe0c99691f881b99db512869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688504"
---
# <a name="inkeditdblclick-event"></a><span data-ttu-id="62833-103">Evento InkEdit. DblClick</span><span class="sxs-lookup"><span data-stu-id="62833-103">InkEdit.DblClick event</span></span>

<span data-ttu-id="62833-104">Se produce cuando se hace doble clic en el control [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="62833-104">Occurs when the [InkEdit](inkedit-control-reference.md) control is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="62833-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62833-105">Syntax</span></span>


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="62833-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62833-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62833-107">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="62833-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="62833-108">**Variante \_ TRUE** para cancelar el evento para el control primario; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="62833-108">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62833-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62833-109">Return value</span></span>

<span data-ttu-id="62833-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="62833-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62833-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62833-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="62833-112">Para distinguir entre los botones izquierdo, derecho e intermedio del mouse, use los eventos [**MouseDown**](inkedit-mousedown.md) y [**MouseUp**](inkedit-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="62833-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkedit-mousedown.md) and [**MouseUp**](inkedit-mouseup.md) events.</span></span> <span data-ttu-id="62833-113">Si hay código en el evento [**click**](inkedit-click.md) , el evento **DblClick** nunca se desencadenará.</span><span class="sxs-lookup"><span data-stu-id="62833-113">If there is code in the [**Click**](inkedit-click.md) event, the **DblClick** event will never trigger.</span></span>

 

<span data-ttu-id="62833-114">Este método de evento se define en la interfaz **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="62833-114">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="62833-115">La interfaz **\_ IInkEditEvents** implementa la interfaz IDispatch con un identificador de **DISPID \_ IeeDblClick**.</span><span class="sxs-lookup"><span data-stu-id="62833-115">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IeeDblClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="62833-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62833-116">Requirements</span></span>



| <span data-ttu-id="62833-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="62833-117">Requirement</span></span> | <span data-ttu-id="62833-118">Value</span><span class="sxs-lookup"><span data-stu-id="62833-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62833-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62833-119">Minimum supported client</span></span><br/> | <span data-ttu-id="62833-120">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="62833-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="62833-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62833-121">Minimum supported server</span></span><br/> | <span data-ttu-id="62833-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="62833-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="62833-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62833-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="62833-124"><dt>Autodibujado. h (también requiere la intermano \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="62833-124"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="62833-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62833-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="62833-126"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62833-126"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="62833-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="62833-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62833-128">InkEdit</span><span class="sxs-lookup"><span data-stu-id="62833-128">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 




