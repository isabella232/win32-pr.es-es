---
description: Indica que el reproductor de DVD inició la reproducción de un nuevo programa en el dominio de título de dominio de DVD \_ \_ .
ms.assetid: c0745615-d527-4d93-9118-30419c6c811e
title: EC_DVD_CHAPTER_START (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CHAPTER_START
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 87a4408f1631d8a23cf42e790688856d6c246393
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653381"
---
# <a name="ec_dvd_chapter_start"></a><span data-ttu-id="51985-103">\_Inicio de \_ capítulo de DVD de EC \_</span><span class="sxs-lookup"><span data-stu-id="51985-103">EC\_DVD\_CHAPTER\_START</span></span>

<span data-ttu-id="51985-104">Indica que el reproductor de DVD inició la reproducción de un nuevo programa en el dominio de título de dominio de DVD \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="51985-104">Signals that the DVD player started playback of a new program in the DVD\_DOMAIN\_Title domain.</span></span>

## <a name="parameters"></a><span data-ttu-id="51985-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51985-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51985-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="51985-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="51985-107">Valor **DWORD** que indica el nuevo número de capítulo (programa).</span><span class="sxs-lookup"><span data-stu-id="51985-107">**DWORD** value indicating the new chapter (program) number.</span></span>

</dd> <dt>

<span data-ttu-id="51985-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="51985-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="51985-109">Cero.</span><span class="sxs-lookup"><span data-stu-id="51985-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51985-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51985-110">Remarks</span></span>

<span data-ttu-id="51985-111">Solo las películas lineales simples señalan este evento.</span><span class="sxs-lookup"><span data-stu-id="51985-111">Only simple linear movies signal this event.</span></span>

<span data-ttu-id="51985-112">Este evento se desencadena en el dominio de título.</span><span class="sxs-lookup"><span data-stu-id="51985-112">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="51985-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51985-113">Requirements</span></span>



| <span data-ttu-id="51985-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="51985-114">Requirement</span></span> | <span data-ttu-id="51985-115">Value</span><span class="sxs-lookup"><span data-stu-id="51985-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51985-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51985-116">Header</span></span><br/> | <dl> <span data-ttu-id="51985-117"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51985-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51985-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="51985-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51985-119">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="51985-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="51985-120">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="51985-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="51985-121">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="51985-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="51985-122">**\_Enumeración de dominio de DVD**</span><span class="sxs-lookup"><span data-stu-id="51985-122">**DVD\_DOMAIN Enumeration**</span></span>](/windows/win32/api/strmif/ne-strmif-dvd_domain)
</dt> </dl>

 

 




