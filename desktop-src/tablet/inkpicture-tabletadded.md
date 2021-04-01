---
description: Se produce cuando se agrega un IInkTablet al sistema.
ms.assetid: 5df10efd-7055-43fa-881f-67eb5fd6adcf
title: Evento InkPicture. TabletAdded (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d75cb3a67b00c5a26c0c3494fc752595954a23da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279182"
---
# <a name="inkpicturetabletadded-event"></a><span data-ttu-id="741dd-103">Evento InkPicture. TabletAdded</span><span class="sxs-lookup"><span data-stu-id="741dd-103">InkPicture.TabletAdded event</span></span>

<span data-ttu-id="741dd-104">Se produce cuando se agrega un [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) al sistema.</span><span class="sxs-lookup"><span data-stu-id="741dd-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="741dd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="741dd-105">Syntax</span></span>


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a><span data-ttu-id="741dd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="741dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="741dd-107">*Tableta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="741dd-107">*Tablet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="741dd-108">El objeto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) que se ha agregado al sistema.</span><span class="sxs-lookup"><span data-stu-id="741dd-108">The [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that has been added to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="741dd-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="741dd-109">Return value</span></span>

<span data-ttu-id="741dd-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="741dd-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="741dd-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="741dd-111">Remarks</span></span>

<span data-ttu-id="741dd-112">Este método de evento se define en las interfaces de solo distribución (dispinterfaces) **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** con el identificador DISPID \_ ICETabletAdded.</span><span class="sxs-lookup"><span data-stu-id="741dd-112">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="741dd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="741dd-113">Requirements</span></span>



| <span data-ttu-id="741dd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="741dd-114">Requirement</span></span> | <span data-ttu-id="741dd-115">Value</span><span class="sxs-lookup"><span data-stu-id="741dd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="741dd-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="741dd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="741dd-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="741dd-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="741dd-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="741dd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="741dd-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="741dd-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="741dd-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="741dd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="741dd-121"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="741dd-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="741dd-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="741dd-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="741dd-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="741dd-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="741dd-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="741dd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="741dd-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="741dd-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="741dd-126">**Interfaz IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="741dd-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




