---
description: Se envía cuando cambia el valor de un registro de parámetros general (GPRM).
ms.assetid: 3e0c400e-9ea5-458c-9eca-97d66a440590
title: EC_DVD_GPRM_Change (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_GPRM_Change
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: f67a8646a72689c2570462f7dc4aeee6b2474136
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653407"
---
# <a name="ec_dvd_gprm_change"></a><span data-ttu-id="bc0f8-103">\_Cambio de \_ GPRM de DVD de EC \_</span><span class="sxs-lookup"><span data-stu-id="bc0f8-103">EC\_DVD\_GPRM\_Change</span></span>

<span data-ttu-id="bc0f8-104">Se envía cuando cambia el valor de un registro de parámetros general (GPRM).</span><span class="sxs-lookup"><span data-stu-id="bc0f8-104">Sent when the value of a general parameter register (GPRM) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="bc0f8-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc0f8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc0f8-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="bc0f8-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="bc0f8-107">Índice de base cero del valor de GPRM que cambió.</span><span class="sxs-lookup"><span data-stu-id="bc0f8-107">The zero-based index of the GPRM value that changed.</span></span>

</dd> <dt>

<span data-ttu-id="bc0f8-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="bc0f8-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="bc0f8-109">Los 16 bits inferiores contienen el nuevo valor GPRM.</span><span class="sxs-lookup"><span data-stu-id="bc0f8-109">The lower 16 bits contains the new GPRM value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc0f8-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc0f8-110">Remarks</span></span>

<span data-ttu-id="bc0f8-111">Este evento está deshabilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="bc0f8-111">This event is disabled by default.</span></span> <span data-ttu-id="bc0f8-112">Para habilitar este evento, llame a [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) y establezca la opción **DVD \_ EnableLoggingEvents** en **true**.</span><span class="sxs-lookup"><span data-stu-id="bc0f8-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc0f8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc0f8-113">Requirements</span></span>



| <span data-ttu-id="bc0f8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc0f8-114">Requirement</span></span> | <span data-ttu-id="bc0f8-115">Value</span><span class="sxs-lookup"><span data-stu-id="bc0f8-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc0f8-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc0f8-116">Header</span></span><br/> | <dl> <span data-ttu-id="bc0f8-117"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc0f8-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc0f8-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc0f8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc0f8-119">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="bc0f8-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="bc0f8-120">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="bc0f8-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="bc0f8-121">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="bc0f8-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="bc0f8-122">**IDvdInfo2::GetAllGPRMs**</span><span class="sxs-lookup"><span data-stu-id="bc0f8-122">**IDvdInfo2::GetAllGPRMs**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallgprms)
</dt> </dl>

 

 




