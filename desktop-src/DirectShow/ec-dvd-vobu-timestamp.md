---
description: Se envía cuando el navegador de DVD analiza un paquete PCI.
ms.assetid: 25548c23-22f0-47cb-9062-273ad39d3007
title: EC_DVD_VOBU_Timestamp (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Timestamp
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 762a900a83154ce38ee00fcf4173ebc32b41cf30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679163"
---
# <a name="ec_dvd_vobu_timestamp"></a><span data-ttu-id="004b1-103">Marca de tiempo VOBU de DVD de EC \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="004b1-103">EC\_DVD\_VOBU\_Timestamp</span></span>

<span data-ttu-id="004b1-104">Se envía cuando el [navegador de DVD](dvd-navigator-filter.md) analiza un paquete PCI.</span><span class="sxs-lookup"><span data-stu-id="004b1-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) parses a PCI packet.</span></span>

<span data-ttu-id="004b1-105">Los datos de evento son la marca de tiempo de la unidad de objeto de vídeo más reciente (VOBU).</span><span class="sxs-lookup"><span data-stu-id="004b1-105">The event data is the time stamp of the most recent video object unit (VOBU).</span></span>

## <a name="parameters"></a><span data-ttu-id="004b1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="004b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="004b1-107"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="004b1-107"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="004b1-108">Contiene el **valor DWORD** de orden inferior de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="004b1-108">Contains the low-order **DWORD** of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="004b1-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="004b1-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="004b1-110">Contiene el **valor DWORD** de orden superior de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="004b1-110">Contains the high-order **DWORD** of the time stamp.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="004b1-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="004b1-111">Remarks</span></span>

<span data-ttu-id="004b1-112">Este evento está deshabilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="004b1-112">This event is disabled by default.</span></span> <span data-ttu-id="004b1-113">Para habilitar este evento, llame a [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) y establezca la opción **DVD \_ EnableLoggingEvents** en **true**.</span><span class="sxs-lookup"><span data-stu-id="004b1-113">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

<span data-ttu-id="004b1-114">Reconstruya la marca de tiempo de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="004b1-114">Reconstruct the time stamp as follows:</span></span>


```C++
LARGE_INTEGER li;
li.LowPart = DWORD( lParam1 );
li.HighPart = DWORD( lParam2 );
```



## <a name="requirements"></a><span data-ttu-id="004b1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="004b1-115">Requirements</span></span>



| <span data-ttu-id="004b1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="004b1-116">Requirement</span></span> | <span data-ttu-id="004b1-117">Value</span><span class="sxs-lookup"><span data-stu-id="004b1-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="004b1-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="004b1-118">Header</span></span><br/> | <dl> <span data-ttu-id="004b1-119"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="004b1-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="004b1-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="004b1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="004b1-121">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="004b1-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="004b1-122">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="004b1-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="004b1-123">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="004b1-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




