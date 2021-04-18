---
description: Se produce cuando se quita un IInkTablet del sistema.
ms.assetid: 659a9809-fe35-4d34-aa95-af353998c350
title: InkCollector. TabletRemoved evento (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ec723a6752f79a1a1d56d318d49ec3d025919d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715081"
---
# <a name="inkcollectortabletremoved-event"></a><span data-ttu-id="e2e43-103">InkCollector. TabletRemoved, evento</span><span class="sxs-lookup"><span data-stu-id="e2e43-103">InkCollector.TabletRemoved event</span></span>

<span data-ttu-id="e2e43-104">Se produce cuando se quita un [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) del sistema.</span><span class="sxs-lookup"><span data-stu-id="e2e43-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is removed from the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2e43-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2e43-105">Syntax</span></span>


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a><span data-ttu-id="e2e43-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2e43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2e43-107">*TabletId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e2e43-107">*TabletId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e43-108">Valor Long que se usó como identificador para el objeto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="e2e43-108">The long value that was used as the ID for the [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2e43-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2e43-109">Return value</span></span>

<span data-ttu-id="e2e43-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="e2e43-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2e43-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2e43-111">Remarks</span></span>

<span data-ttu-id="e2e43-112">Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ ICETabletRemoved.</span><span class="sxs-lookup"><span data-stu-id="e2e43-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2e43-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2e43-113">Requirements</span></span>



| <span data-ttu-id="e2e43-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2e43-114">Requirement</span></span> | <span data-ttu-id="e2e43-115">Value</span><span class="sxs-lookup"><span data-stu-id="e2e43-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2e43-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2e43-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e2e43-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e2e43-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e2e43-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2e43-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e2e43-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e2e43-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e2e43-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2e43-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2e43-121"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e2e43-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e2e43-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e2e43-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="e2e43-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2e43-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e2e43-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2e43-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2e43-125">**InkCollector (clase)**</span><span class="sxs-lookup"><span data-stu-id="e2e43-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="e2e43-126">**Interfaz IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="e2e43-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




