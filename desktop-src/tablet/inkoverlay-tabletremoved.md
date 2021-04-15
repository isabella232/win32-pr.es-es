---
description: Se produce cuando se quita un IInkTablet del sistema.
ms.assetid: 2217a69e-5b39-4827-82cd-99a02e9d39c6
title: Evento InkOverlay. TabletRemoved (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a7d0e69bae7cb6360794b9624fcef7c8be639e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648434"
---
# <a name="inkoverlaytabletremoved-event"></a><span data-ttu-id="ee567-103">Evento InkOverlay. TabletRemoved</span><span class="sxs-lookup"><span data-stu-id="ee567-103">InkOverlay.TabletRemoved event</span></span>

<span data-ttu-id="ee567-104">Se produce cuando se quita un [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) del sistema.</span><span class="sxs-lookup"><span data-stu-id="ee567-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is removed from the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee567-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee567-105">Syntax</span></span>


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a><span data-ttu-id="ee567-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee567-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee567-107">*TabletId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ee567-107">*TabletId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee567-108">Valor Long que se usó como identificador para el objeto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="ee567-108">The long value that was used as the ID for the [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee567-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee567-109">Return value</span></span>

<span data-ttu-id="ee567-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="ee567-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee567-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee567-111">Remarks</span></span>

<span data-ttu-id="ee567-112">Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ ICETabletRemoved.</span><span class="sxs-lookup"><span data-stu-id="ee567-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee567-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee567-113">Requirements</span></span>



| <span data-ttu-id="ee567-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee567-114">Requirement</span></span> | <span data-ttu-id="ee567-115">Value</span><span class="sxs-lookup"><span data-stu-id="ee567-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee567-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee567-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ee567-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ee567-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ee567-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee567-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ee567-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ee567-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ee567-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee567-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee567-121"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ee567-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ee567-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee567-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="ee567-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee567-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ee567-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee567-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee567-125">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="ee567-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="ee567-126">**Interfaz IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="ee567-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




