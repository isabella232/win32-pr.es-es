---
description: Señala la hora actual, en \_ formato de código de tiempo HMSF de DVD \_ , con respecto al inicio del título. Este evento se desencadena al principio de cada VOBU, que se produce cada 0,4 a 1,0 segundos.
ms.assetid: 7c81a09a-21f3-49b2-b90a-7cbc9c815bad
title: EC_DVD_CURRENT_HMSF_TIME (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_HMSF_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 36306b95682e62ffebf8fb819dcc4b7c5185493c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690083"
---
# <a name="ec_dvd_current_hmsf_time"></a><span data-ttu-id="7585e-104">\_hora de \_ \_ HMSF actual del DVD \_ de EC</span><span class="sxs-lookup"><span data-stu-id="7585e-104">EC\_DVD\_CURRENT\_HMSF\_TIME</span></span>

<span data-ttu-id="7585e-105">Señala la hora actual, en formato de [**\_ código de \_ tiempo HMSF de DVD**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) , con respecto al inicio del título.</span><span class="sxs-lookup"><span data-stu-id="7585e-105">Signals the current time, in [**DVD\_HMSF\_TIMECODE**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) format, relative to the start of the title.</span></span> <span data-ttu-id="7585e-106">Este evento se desencadena al principio de cada VOBU, que se produce cada 0,4 a 1,0 segundos.</span><span class="sxs-lookup"><span data-stu-id="7585e-106">This event is triggered at the beginning of every VOBU, which occurs every 0.4 to 1.0 seconds.</span></span>

## <a name="parameters"></a><span data-ttu-id="7585e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7585e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7585e-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="7585e-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="7585e-109">Valor ULONG que contiene la estructura de \_ código de tiempo HMSF de DVD \_ .</span><span class="sxs-lookup"><span data-stu-id="7585e-109">A ULONG value that contains the DVD\_HMSF\_TIMECODE structure.</span></span> <span data-ttu-id="7585e-110">Asigne lParam1 a una variable ULONG y, a continuación, convierta esa variable en un \_ \_ código de tiempo HMSF de DVD para tener acceso a sus valores.</span><span class="sxs-lookup"><span data-stu-id="7585e-110">Assign lParam1 to a ULONG variable and then cast that variable to a DVD\_HMSF\_TIMECODE to access its values.</span></span>

</dd> <dt>

<span data-ttu-id="7585e-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="7585e-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="7585e-112">Valor ULONG que contiene una Unión de [**\_ \_ marcas de código de tiempo de DVD**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags).</span><span class="sxs-lookup"><span data-stu-id="7585e-112">A ULONG value containing a union of [**DVD\_TIMECODE\_FLAGS**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7585e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7585e-113">Remarks</span></span>

<span data-ttu-id="7585e-114">El formato de código de tiempo de HMSF de DVD \_ \_ está pensado para reemplazar el formato BCD anterior que se devuelve en \_ \_ los eventos de hora actual de DVD de EC \_ .</span><span class="sxs-lookup"><span data-stu-id="7585e-114">The DVD\_HMSF\_TIMECODE format is intended to replace the old BCD format that is returned in EC\_DVD\_CURRENT\_TIME events.</span></span> <span data-ttu-id="7585e-115">Los códigos de tiempo de HMSF son más fáciles de usar.</span><span class="sxs-lookup"><span data-stu-id="7585e-115">The HMSF timecodes are easier to work with.</span></span> <span data-ttu-id="7585e-116">Para que el navegador envíe \_ eventos de \_ \_ \_ tiempo de HMSF actual de DVD de EC en lugar de \_ eventos de hora actual de DVD de EC \_ \_ , una aplicación debe llamar a `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)` .</span><span class="sxs-lookup"><span data-stu-id="7585e-116">To have the Navigator send EC\_DVD\_CURRENT\_HMSF\_TIME events instead of EC\_DVD\_CURRENT\_TIME events, an application must call `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)`.</span></span> <span data-ttu-id="7585e-117">Cuando se establece esta marca, el navegador también espera que todos los parámetros de tiempo de los métodos [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) y [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) se pasen como códigos de tiempo de HMSF de DVD \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7585e-117">When this flag is set, the Navigator will also expect all time parameters in the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) and [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) methods to be passed as DVD\_HMSF\_TIMECODEs.</span></span>

<span data-ttu-id="7585e-118">Este evento se desencadena en los dominios de título.</span><span class="sxs-lookup"><span data-stu-id="7585e-118">This event is raised in the title domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="7585e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7585e-119">Requirements</span></span>



| <span data-ttu-id="7585e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7585e-120">Requirement</span></span> | <span data-ttu-id="7585e-121">Value</span><span class="sxs-lookup"><span data-stu-id="7585e-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7585e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7585e-122">Header</span></span><br/> | <dl> <span data-ttu-id="7585e-123"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7585e-123"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7585e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="7585e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7585e-125">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="7585e-125">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="7585e-126">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="7585e-126">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="7585e-127">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="7585e-127">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




