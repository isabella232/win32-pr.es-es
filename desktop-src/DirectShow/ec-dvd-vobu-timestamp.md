---
description: 'EC_DVD_VOBU_Timestamp: se envía cuando el navegador de DVD analiza un paquete PCI.'
ms.assetid: 25548c23-22f0-47cb-9062-273ad39d3007
title: EC_DVD_VOBU_Timestamp (Dvdevcode.h)
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
ms.openlocfilehash: 6bd06eb99cae60960db64a6f32df5e4c932b362f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094623"
---
# <a name="ec_dvd_vobu_timestamp"></a><span data-ttu-id="084fb-103">Marca de \_ tiempo DE VOBU de DVD \_ DE EC \_</span><span class="sxs-lookup"><span data-stu-id="084fb-103">EC\_DVD\_VOBU\_Timestamp</span></span>

<span data-ttu-id="084fb-104">Se envía cuando [el navegador de DVD](dvd-navigator-filter.md) analiza un paquete PCI.</span><span class="sxs-lookup"><span data-stu-id="084fb-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) parses a PCI packet.</span></span>

<span data-ttu-id="084fb-105">Los datos del evento son la marca de tiempo de la unidad de objeto de vídeo (VOBU) más reciente.</span><span class="sxs-lookup"><span data-stu-id="084fb-105">The event data is the time stamp of the most recent video object unit (VOBU).</span></span>

## <a name="parameters"></a><span data-ttu-id="084fb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="084fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="084fb-107"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="084fb-107"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="084fb-108">Contiene el **DWORD** de orden bajo de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="084fb-108">Contains the low-order **DWORD** of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="084fb-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="084fb-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="084fb-110">Contiene el **DWORD** de orden superior de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="084fb-110">Contains the high-order **DWORD** of the time stamp.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="084fb-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="084fb-111">Remarks</span></span>

<span data-ttu-id="084fb-112">Este evento está deshabilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="084fb-112">This event is disabled by default.</span></span> <span data-ttu-id="084fb-113">Para habilitar este evento, llame a [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) y establezca la opción **DVD \_ EnableLoggingEvents** en **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="084fb-113">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

<span data-ttu-id="084fb-114">Reconstruye la marca de tiempo como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="084fb-114">Reconstruct the time stamp as follows:</span></span>


```C++
LARGE_INTEGER li;
li.LowPart = DWORD( lParam1 );
li.HighPart = DWORD( lParam2 );
```



## <a name="requirements"></a><span data-ttu-id="084fb-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="084fb-115">Requirements</span></span>



| <span data-ttu-id="084fb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="084fb-116">Requirement</span></span> | <span data-ttu-id="084fb-117">Value</span><span class="sxs-lookup"><span data-stu-id="084fb-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="084fb-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="084fb-118">Header</span></span><br/> | <dl> <span data-ttu-id="084fb-119"><dt>Dvdevcode.h (incluir Dshow.h)</dt></span><span class="sxs-lookup"><span data-stu-id="084fb-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="084fb-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="084fb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="084fb-121">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="084fb-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="084fb-122">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="084fb-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="084fb-123">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="084fb-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




