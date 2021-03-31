---
description: Se produce cuando se hace doble clic en el control InkPicture.
ms.assetid: 5b2a6413-d415-4bf1-a291-35f4c3c5a0dc
title: Evento InkPicture. DblClick (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c3d9bb9125c8142186da969acf6ce03f5f76b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361176"
---
# <a name="inkpicturedblclick-event"></a><span data-ttu-id="35342-103">InkPicture. DblClick (evento)</span><span class="sxs-lookup"><span data-stu-id="35342-103">InkPicture.DblClick event</span></span>

<span data-ttu-id="35342-104">Se produce cuando se hace doble clic en el control [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="35342-104">Occurs when the [InkPicture](inkpicture-control-reference.md) control is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="35342-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35342-105">Syntax</span></span>


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="35342-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35342-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35342-107">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="35342-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="35342-108">Indica si se debe cancelar el evento para el control primario.</span><span class="sxs-lookup"><span data-stu-id="35342-108">Whether the event should be canceled for the parent control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35342-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35342-109">Return value</span></span>

<span data-ttu-id="35342-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="35342-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="35342-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35342-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="35342-112">Para distinguir entre los botones izquierdo, derecho e intermedio del mouse, use los eventos [**MouseDown**](inkpicture-mousedown.md) y [**MouseUp**](inkpicture-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="35342-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) events.</span></span> <span data-ttu-id="35342-113">Si hay código en el evento [**click**](inkpicture-click.md) , el evento **DblClick** nunca se desencadenará.</span><span class="sxs-lookup"><span data-stu-id="35342-113">If there is code in the [**Click**](inkpicture-click.md) event, the **DblClick** event will never trigger.</span></span>

 

<span data-ttu-id="35342-114">Este método de evento se define en la interfaz **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="35342-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="35342-115">La interfaz **\_ IInkPictureEvents** implementa la interfaz IDispatch con un identificador de **DISPID \_ IPEDblClick**.</span><span class="sxs-lookup"><span data-stu-id="35342-115">The **\_IInkPictureEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IPEDblClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="35342-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35342-116">Requirements</span></span>



| <span data-ttu-id="35342-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="35342-117">Requirement</span></span> | <span data-ttu-id="35342-118">Value</span><span class="sxs-lookup"><span data-stu-id="35342-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35342-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35342-119">Minimum supported client</span></span><br/> | <span data-ttu-id="35342-120">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="35342-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="35342-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35342-121">Minimum supported server</span></span><br/> | <span data-ttu-id="35342-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="35342-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="35342-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35342-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="35342-124"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="35342-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="35342-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="35342-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="35342-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35342-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="35342-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="35342-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35342-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="35342-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




