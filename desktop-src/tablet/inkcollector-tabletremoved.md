---
description: 'Evento InkCollector.TabletRemoved: se produce cuando se quita un IInkTablet del sistema.'
ms.assetid: 659a9809-fe35-4d34-aa95-af353998c350
title: Evento InkCollector.TabletRemoved (Msmutut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df76c27b1a0d47e456f69a789d17ef6343706284
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110003"
---
# <a name="inkcollectortabletremoved-event"></a><span data-ttu-id="1e2e0-103">Evento InkCollector.TabletRemoved</span><span class="sxs-lookup"><span data-stu-id="1e2e0-103">InkCollector.TabletRemoved event</span></span>

<span data-ttu-id="1e2e0-104">Se produce cuando [**se quita un IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) del sistema.</span><span class="sxs-lookup"><span data-stu-id="1e2e0-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is removed from the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e2e0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e2e0-105">Syntax</span></span>


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a><span data-ttu-id="1e2e0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e2e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e2e0-107">*TabletId* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="1e2e0-107">*TabletId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e2e0-108">Valor long que se usó como identificador del objeto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) que se quitó.</span><span class="sxs-lookup"><span data-stu-id="1e2e0-108">The long value that was used as the ID for the [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e2e0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e2e0-109">Return value</span></span>

<span data-ttu-id="1e2e0-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="1e2e0-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e2e0-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1e2e0-111">Remarks</span></span>

<span data-ttu-id="1e2e0-112">Este método de evento se define en las interfaces de solo distribución \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ de \_ DISPID ICETabletRemoved.</span><span class="sxs-lookup"><span data-stu-id="1e2e0-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e2e0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e2e0-113">Requirements</span></span>



| <span data-ttu-id="1e2e0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e2e0-114">Requirement</span></span> | <span data-ttu-id="1e2e0-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1e2e0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e2e0-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e2e0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1e2e0-117">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="1e2e0-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1e2e0-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e2e0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1e2e0-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1e2e0-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1e2e0-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e2e0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e2e0-121"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="1e2e0-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1e2e0-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1e2e0-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="1e2e0-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e2e0-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="1e2e0-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1e2e0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e2e0-125">**InkCollector (clase)**</span><span class="sxs-lookup"><span data-stu-id="1e2e0-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="1e2e0-126">**IInkTablet (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="1e2e0-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




