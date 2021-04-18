---
description: Se envía cuando el navegador de DVD analiza un paquete PCI.
ms.assetid: e2e65007-7c34-4be4-86b9-9491061891e5
title: EC_DVD_VOBU_Offset (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Offset
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 531207d4d8b0debb29dd5d02e01e400218e4a2bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679164"
---
# <a name="ec_dvd_vobu_offset"></a><span data-ttu-id="3b781-103">\_Desplazamiento de \_ VOBU de DVD de EC \_</span><span class="sxs-lookup"><span data-stu-id="3b781-103">EC\_DVD\_VOBU\_Offset</span></span>

<span data-ttu-id="3b781-104">Se envía cuando el [navegador de DVD](dvd-navigator-filter.md) analiza un paquete PCI.</span><span class="sxs-lookup"><span data-stu-id="3b781-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) parses a PCI packet.</span></span>

## <a name="parameters"></a><span data-ttu-id="3b781-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b781-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b781-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="3b781-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="3b781-107">El desplazamiento de bloque de la unidad de objeto de vídeo más reciente (VOBU).</span><span class="sxs-lookup"><span data-stu-id="3b781-107">The block offset of the most recent video object unit (VOBU).</span></span>

</dd> <dt>

<span data-ttu-id="3b781-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="3b781-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="3b781-109">Número del conjunto de títulos de vídeo actual (VTSN).</span><span class="sxs-lookup"><span data-stu-id="3b781-109">The current video title set number (VTSN).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b781-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b781-110">Remarks</span></span>

<span data-ttu-id="3b781-111">Este evento está deshabilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3b781-111">This event is disabled by default.</span></span> <span data-ttu-id="3b781-112">Para habilitar este evento, llame a [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) y establezca la opción **DVD \_ EnableLoggingEvents** en **true**.</span><span class="sxs-lookup"><span data-stu-id="3b781-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b781-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b781-113">Requirements</span></span>



| <span data-ttu-id="3b781-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b781-114">Requirement</span></span> | <span data-ttu-id="3b781-115">Value</span><span class="sxs-lookup"><span data-stu-id="3b781-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b781-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b781-116">Header</span></span><br/> | <dl> <span data-ttu-id="3b781-117"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b781-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b781-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b781-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b781-119">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="3b781-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="3b781-120">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="3b781-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="3b781-121">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="3b781-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




