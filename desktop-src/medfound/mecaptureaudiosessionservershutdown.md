---
description: Enviado por un origen de captura de audio cuando la sesión de captura de audio se desconecta debido a que el servidor de audio se está cerrando.
ms.assetid: 43284B3E-3018-44F3-8D6C-8C3041DCCD3E
title: Evento MECaptureAudioSessionServerShutdown (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad934f6d60868c1db7c5b5b7907ff720312ea439
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720618"
---
# <a name="mecaptureaudiosessionservershutdown-event"></a><span data-ttu-id="0eaba-103">Evento MECaptureAudioSessionServerShutdown</span><span class="sxs-lookup"><span data-stu-id="0eaba-103">MECaptureAudioSessionServerShutdown event</span></span>

<span data-ttu-id="0eaba-104">Enviado por un origen de captura de audio cuando la sesión de captura de audio se desconecta debido a que el servidor de audio se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="0eaba-104">Sent by an audio capture source when the capture audio session is disconnected due to the audio server being shutdown.</span></span>

## <a name="event-values"></a><span data-ttu-id="0eaba-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="0eaba-105">Event values</span></span>

<span data-ttu-id="0eaba-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="0eaba-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0eaba-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0eaba-107">VARTYPE</span></span>               | <span data-ttu-id="0eaba-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="0eaba-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="0eaba-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="0eaba-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="0eaba-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="0eaba-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="0eaba-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0eaba-111">Requirements</span></span>



| <span data-ttu-id="0eaba-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="0eaba-112">Requirement</span></span> | <span data-ttu-id="0eaba-113">Value</span><span class="sxs-lookup"><span data-stu-id="0eaba-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0eaba-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0eaba-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0eaba-115">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="0eaba-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="0eaba-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0eaba-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0eaba-117">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="0eaba-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0eaba-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0eaba-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="0eaba-119"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0eaba-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0eaba-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="0eaba-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eaba-121">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0eaba-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




