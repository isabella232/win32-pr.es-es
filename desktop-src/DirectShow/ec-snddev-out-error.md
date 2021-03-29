---
description: Se ha producido un error de dispositivo en un filtro de representador de audio.
ms.assetid: 60e36476-f553-468d-a28d-351fdf4a02f1
title: EC_SNDDEV_OUT_ERROR (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1182aaba7bb30ad27511b47ba8e4432d8fd33da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653880"
---
# <a name="ec_snddev_out_error"></a><span data-ttu-id="442b4-103">\_error de SNDDEV de \_ salida de EC \_</span><span class="sxs-lookup"><span data-stu-id="442b4-103">EC\_SNDDEV\_OUT\_ERROR</span></span>

<span data-ttu-id="442b4-104">Se ha producido un error de dispositivo en un filtro de representador de audio.</span><span class="sxs-lookup"><span data-stu-id="442b4-104">A device error has occurred in an audio renderer filter.</span></span>

## <a name="parameters"></a><span data-ttu-id="442b4-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="442b4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="442b4-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="442b4-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="442b4-107">Valor DWORD del tipo enumerado de [**SNDDEV \_ Err**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) , que indica cómo se estaba accediendo al dispositivo cuando se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="442b4-107">DWORD value from the [**SNDDEV\_ERR**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) enumerated type, indicating how the device was being accessed when the failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="442b4-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="442b4-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="442b4-109">Valor DWORD que indica el error devuelto por la llamada de dispositivo de sonido.</span><span class="sxs-lookup"><span data-stu-id="442b4-109">DWORD value indicating the error returned from the sound device call.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="442b4-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="442b4-110">Default Action</span></span>

<span data-ttu-id="442b4-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="442b4-111">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="442b4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="442b4-112">Requirements</span></span>



| <span data-ttu-id="442b4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="442b4-113">Requirement</span></span> | <span data-ttu-id="442b4-114">Value</span><span class="sxs-lookup"><span data-stu-id="442b4-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="442b4-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="442b4-115">Header</span></span><br/> | <dl> <span data-ttu-id="442b4-116"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="442b4-116"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="442b4-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="442b4-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="442b4-118">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="442b4-118">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="442b4-119">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="442b4-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




