---
title: Mensaje de MM_MIXM_LINE_CHANGE (mmsystem. h)
description: '\_ \_ \_ Un dispositivo de mezclador envía el mensaje de cambio de línea mm MIXM para notificar a una aplicación que ha cambiado el estado de una línea de audio en el dispositivo especificado. La aplicación debe actualizar su presentación y los valores almacenados en caché para la línea de audio especificada.'
ms.assetid: 68ada0be-9dc5-4edf-b924-ef0d10a1b79a
keywords:
- Mensaje de MM_MIXM_LINE_CHANGE de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MIXM_LINE_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92c4aa10d9934f8cf5f5747ecb4e4eb736af2655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686090"
---
# <a name="mm_mixm_line_change-message"></a><span data-ttu-id="e6275-105">\_Mensaje de \_ cambio de línea mm MIXM \_</span><span class="sxs-lookup"><span data-stu-id="e6275-105">MM\_MIXM\_LINE\_CHANGE message</span></span>

<span data-ttu-id="e6275-106">Un dispositivo de mezclador envía el mensaje de **\_ cambio de \_ línea \_ mm MIXM** para notificar a una aplicación que ha cambiado el estado de una línea de audio en el dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="e6275-106">The **MM\_MIXM\_LINE\_CHANGE** message is sent by a mixer device to notify an application that the state of an audio line on the specified device has changed.</span></span> <span data-ttu-id="e6275-107">La aplicación debe actualizar su presentación y los valores almacenados en caché para la línea de audio especificada.</span><span class="sxs-lookup"><span data-stu-id="e6275-107">The application should refresh its display and cached values for the specified audio line.</span></span>


```C++
MM_MIXM_LINE_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwLineID 
```



## <a name="parameters"></a><span data-ttu-id="e6275-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6275-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6275-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span><span class="sxs-lookup"><span data-stu-id="e6275-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span></span>
</dt> <dd>

<span data-ttu-id="e6275-110">Identificador del dispositivo de mezclador que envió el mensaje de notificación.</span><span class="sxs-lookup"><span data-stu-id="e6275-110">Handle to the mixer device that sent the notification message.</span></span>

</dd> <dt>

<span data-ttu-id="e6275-111"><span id="dwLineID"></span><span id="dwlineid"></span><span id="DWLINEID"></span>*dwLineID*</span><span class="sxs-lookup"><span data-stu-id="e6275-111"><span id="dwLineID"></span><span id="dwlineid"></span><span id="DWLINEID"></span>*dwLineID*</span></span>
</dt> <dd>

<span data-ttu-id="e6275-112">Identificador de línea de la línea de audio que ha cambiado de estado.</span><span class="sxs-lookup"><span data-stu-id="e6275-112">Line identifier for the audio line that has changed state.</span></span> <span data-ttu-id="e6275-113">Este identificador es el mismo que el miembro **dwLineID** de la estructura **MIXERLINE** devuelta por la función **mixerGetLineInfo**.</span><span class="sxs-lookup"><span data-stu-id="e6275-113">This identifier is the same as the **dwLineID** member of the **MIXERLINE** structure returned by the **mixerGetLineInfo** function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6275-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6275-114">Remarks</span></span>

<span data-ttu-id="e6275-115">Una aplicación debe abrir un dispositivo de mezclador y especificar una ventana de devolución de llamada para recibir el mensaje de **\_ cambio de \_ línea \_ mm MIXM** .</span><span class="sxs-lookup"><span data-stu-id="e6275-115">An application must open a mixer device and specify a callback window to receive the **MM\_MIXM\_LINE\_CHANGE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6275-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6275-116">Requirements</span></span>



| <span data-ttu-id="e6275-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6275-117">Requirement</span></span> | <span data-ttu-id="e6275-118">Value</span><span class="sxs-lookup"><span data-stu-id="e6275-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6275-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6275-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e6275-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e6275-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e6275-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6275-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e6275-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e6275-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e6275-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6275-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6275-124"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6275-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6275-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6275-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6275-126">Mezcladores de audio</span><span class="sxs-lookup"><span data-stu-id="e6275-126">Audio Mixers</span></span>](audio-mixers.md)
</dt> <dt>

[<span data-ttu-id="e6275-127">Mensajes de mezclador de audio</span><span class="sxs-lookup"><span data-stu-id="e6275-127">Audio Mixer Messages</span></span>](audio-mixer-messages.md)
</dt> </dl>

 

 





