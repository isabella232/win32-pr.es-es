---
description: Indica cuándo cambia el número de título de DVD actual.
ms.assetid: 9888f2ec-fc2d-4d6d-a03d-b381373337eb
title: EC_DVD_TITLE_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_TITLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 9539d29704797b1c7b001d426250762d2ed27b3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653403"
---
# <a name="ec_dvd_title_change"></a><span data-ttu-id="c32b9-103">\_cambio de \_ título de DVD de EC \_</span><span class="sxs-lookup"><span data-stu-id="c32b9-103">EC\_DVD\_TITLE\_CHANGE</span></span>

<span data-ttu-id="c32b9-104">Indica cuándo cambia el número de título de DVD actual.</span><span class="sxs-lookup"><span data-stu-id="c32b9-104">Indicates when the current DVD title number changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="c32b9-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c32b9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c32b9-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="c32b9-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="c32b9-107">Valor **DWORD** que indica el nuevo número de título.</span><span class="sxs-lookup"><span data-stu-id="c32b9-107">**DWORD** value indicating the new title number.</span></span>

</dd> <dt>

<span data-ttu-id="c32b9-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="c32b9-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c32b9-109">Cero.</span><span class="sxs-lookup"><span data-stu-id="c32b9-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c32b9-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c32b9-110">Remarks</span></span>

<span data-ttu-id="c32b9-111">Los números de título oscilan entre 1 y 99.</span><span class="sxs-lookup"><span data-stu-id="c32b9-111">Title numbers range from 1 to 99.</span></span> <span data-ttu-id="c32b9-112">Este número indica el valor de TTN, que es el número de título con respecto a todo el disco, no a la TTN de VTS, \_ que es el número de título con respecto a un STB actual.</span><span class="sxs-lookup"><span data-stu-id="c32b9-112">This number indicates the TTN, which is the title number with respect to the whole disc, not the VTS\_TTN which is the title number with respect to just a current VTS.</span></span>

<span data-ttu-id="c32b9-113">Este evento se desencadena en el dominio de título.</span><span class="sxs-lookup"><span data-stu-id="c32b9-113">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="c32b9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c32b9-114">Requirements</span></span>



| <span data-ttu-id="c32b9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c32b9-115">Requirement</span></span> | <span data-ttu-id="c32b9-116">Value</span><span class="sxs-lookup"><span data-stu-id="c32b9-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c32b9-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c32b9-117">Header</span></span><br/> | <dl> <span data-ttu-id="c32b9-118"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c32b9-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c32b9-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="c32b9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c32b9-120">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="c32b9-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="c32b9-121">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="c32b9-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="c32b9-122">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="c32b9-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




