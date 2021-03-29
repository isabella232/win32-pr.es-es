---
description: Indica que el número de secuencia de audio actual cambió para el título principal del DVD.
ms.assetid: ab626c6b-765a-4b2e-be96-f45260d1a078
title: EC_DVD_AUDIO_STREAM_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_AUDIO_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 947e19310a77869dbff97851e1ffa0684a3e43a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680855"
---
# <a name="ec_dvd_audio_stream_change"></a><span data-ttu-id="2e026-103">\_cambio de \_ flujo de audio de DVD de EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="2e026-103">EC\_DVD\_AUDIO\_STREAM\_CHANGE</span></span>

<span data-ttu-id="2e026-104">Indica que el número de secuencia de audio actual cambió para el título principal del DVD.</span><span class="sxs-lookup"><span data-stu-id="2e026-104">Signals that the current audio stream number changed for the DVD main title.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e026-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e026-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e026-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="2e026-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="2e026-107">Valor **DWORD** que indica el nuevo número de secuencia de audio del usuario.</span><span class="sxs-lookup"><span data-stu-id="2e026-107">**DWORD** value indicating the new user audio stream number.</span></span> <span data-ttu-id="2e026-108">Los números de secuencia de audio oscilan entre 0 y 7.</span><span class="sxs-lookup"><span data-stu-id="2e026-108">Audio stream numbers range from 0 to 7.</span></span> <span data-ttu-id="2e026-109">El flujo 0xFFFFFFFF indica que no hay ninguna secuencia seleccionada.</span><span class="sxs-lookup"><span data-stu-id="2e026-109">Stream 0xFFFFFFFF indicates that no stream is selected.</span></span>

</dd> <dt>

<span data-ttu-id="2e026-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="2e026-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="2e026-111">Cero.</span><span class="sxs-lookup"><span data-stu-id="2e026-111">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e026-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e026-112">Remarks</span></span>

<span data-ttu-id="2e026-113">La secuencia de audio actual puede cambiar automáticamente con un comando de navegación creado en el disco, así como a través del control de la aplicación mediante la interfaz [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .</span><span class="sxs-lookup"><span data-stu-id="2e026-113">The current audio stream can change automatically with a navigation command authored on the disc as well as through application control by using the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface.</span></span>

<span data-ttu-id="2e026-114">Este evento se desencadena en todos los dominios.</span><span class="sxs-lookup"><span data-stu-id="2e026-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e026-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e026-115">Requirements</span></span>



| <span data-ttu-id="2e026-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e026-116">Requirement</span></span> | <span data-ttu-id="2e026-117">Value</span><span class="sxs-lookup"><span data-stu-id="2e026-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e026-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e026-118">Header</span></span><br/> | <dl> <span data-ttu-id="2e026-119"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e026-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e026-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e026-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e026-121">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="2e026-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="2e026-122">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="2e026-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="2e026-123">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="2e026-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




