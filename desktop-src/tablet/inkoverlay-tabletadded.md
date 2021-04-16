---
description: Se produce cuando se agrega un IInkTablet al sistema.
ms.assetid: 2076a520-bd37-43b5-b57f-030828b096cb
title: Evento InkOverlay. TabletAdded (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c2faadcbf87e0772afb8f417c97a4be546e08b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649231"
---
# <a name="inkoverlaytabletadded-event"></a><span data-ttu-id="dc620-103">Evento InkOverlay. TabletAdded</span><span class="sxs-lookup"><span data-stu-id="dc620-103">InkOverlay.TabletAdded event</span></span>

<span data-ttu-id="dc620-104">Se produce cuando se agrega un [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) al sistema.</span><span class="sxs-lookup"><span data-stu-id="dc620-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc620-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc620-105">Syntax</span></span>


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a><span data-ttu-id="dc620-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc620-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc620-107">*Tableta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dc620-107">*Tablet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc620-108">El objeto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) que se ha agregado al sistema.</span><span class="sxs-lookup"><span data-stu-id="dc620-108">The [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that has been added to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc620-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc620-109">Return value</span></span>

<span data-ttu-id="dc620-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="dc620-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc620-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc620-111">Remarks</span></span>

<span data-ttu-id="dc620-112">Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ ICETabletAdded.</span><span class="sxs-lookup"><span data-stu-id="dc620-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc620-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc620-113">Requirements</span></span>



| <span data-ttu-id="dc620-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc620-114">Requirement</span></span> | <span data-ttu-id="dc620-115">Value</span><span class="sxs-lookup"><span data-stu-id="dc620-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc620-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc620-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dc620-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="dc620-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="dc620-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc620-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dc620-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="dc620-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="dc620-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dc620-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc620-121"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="dc620-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="dc620-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dc620-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="dc620-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc620-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="dc620-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc620-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc620-125">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="dc620-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="dc620-126">**Interfaz IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="dc620-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




