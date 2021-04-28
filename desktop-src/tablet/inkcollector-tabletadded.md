---
description: 'Evento InkCollector.TabletAdded: se produce cuando se agrega un IInkTablet al sistema.'
ms.assetid: c5f90fce-faf7-411b-a4d6-deb5d0f22f4a
title: Evento InkCollector.TabletAdded (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3088eff151d9857f8a1449d3c99805c949b790
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110013"
---
# <a name="inkcollectortabletadded-event"></a><span data-ttu-id="8b895-103">Evento InkCollector.TabletAdded</span><span class="sxs-lookup"><span data-stu-id="8b895-103">InkCollector.TabletAdded event</span></span>

<span data-ttu-id="8b895-104">Se produce cuando [**se agrega un IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) al sistema.</span><span class="sxs-lookup"><span data-stu-id="8b895-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b895-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b895-105">Syntax</span></span>


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a><span data-ttu-id="8b895-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b895-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b895-107">*Tableta* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8b895-107">*Tablet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b895-108">Objeto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) que se ha agregado al sistema.</span><span class="sxs-lookup"><span data-stu-id="8b895-108">The [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that has been added to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b895-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b895-109">Return value</span></span>

<span data-ttu-id="8b895-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="8b895-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b895-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8b895-111">Remarks</span></span>

<span data-ttu-id="8b895-112">Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ de \_ DISPID ICETabletAdded.</span><span class="sxs-lookup"><span data-stu-id="8b895-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b895-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b895-113">Requirements</span></span>



| <span data-ttu-id="8b895-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b895-114">Requirement</span></span> | <span data-ttu-id="8b895-115">Valor</span><span class="sxs-lookup"><span data-stu-id="8b895-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b895-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b895-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8b895-117">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="8b895-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8b895-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b895-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8b895-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8b895-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="8b895-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b895-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b895-121"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="8b895-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8b895-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8b895-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="8b895-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b895-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="8b895-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8b895-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b895-125">**InkCollector (clase)**</span><span class="sxs-lookup"><span data-stu-id="8b895-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="8b895-126">**IInkTablet (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="8b895-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




