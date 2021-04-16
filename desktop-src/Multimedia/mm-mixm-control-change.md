---
title: Mensaje de MM_MIXM_CONTROL_CHANGE (mmsystem. h)
description: '\_ \_ \_ Un dispositivo de mezclador envía el mensaje de cambio del control mm MIXM para notificar a una aplicación que ha cambiado el estado de un control asociado con una línea de audio. La aplicación debe actualizar su presentación y los valores almacenados en caché para el control especificado.'
ms.assetid: 921c55a7-86c0-43d1-b817-bfbd3c4bb28b
keywords:
- Mensaje de MM_MIXM_CONTROL_CHANGE de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MIXM_CONTROL_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12daa4d9e107a9ba687331731ee9fd7e6f0dc886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651406"
---
# <a name="mm_mixm_control_change-message"></a><span data-ttu-id="0a3e4-105">\_Mensaje de \_ cambio del control MIXM mm \_</span><span class="sxs-lookup"><span data-stu-id="0a3e4-105">MM\_MIXM\_CONTROL\_CHANGE message</span></span>

<span data-ttu-id="0a3e4-106">Un dispositivo de mezclador envía el mensaje de **\_ cambio del \_ control \_ mm MIXM** para notificar a una aplicación que ha cambiado el estado de un control asociado con una línea de audio.</span><span class="sxs-lookup"><span data-stu-id="0a3e4-106">The **MM\_MIXM\_CONTROL\_CHANGE** message is sent by a mixer device to notify an application that the state of a control associated with an audio line has changed.</span></span> <span data-ttu-id="0a3e4-107">La aplicación debe actualizar su presentación y los valores almacenados en caché para el control especificado.</span><span class="sxs-lookup"><span data-stu-id="0a3e4-107">The application should refresh its display and cached values for the specified control.</span></span>


```C++
MM_MIXM_CONTROL_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwControlID 
```



## <a name="parameters"></a><span data-ttu-id="0a3e4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a3e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a3e4-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span><span class="sxs-lookup"><span data-stu-id="0a3e4-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span></span>
</dt> <dd>

<span data-ttu-id="0a3e4-110">Identificador del dispositivo de mezclador (**HMIXER**) que envió el mensaje de notificación.</span><span class="sxs-lookup"><span data-stu-id="0a3e4-110">Handle to the mixer device (**HMIXER**) that sent the notification message.</span></span>

</dd> <dt>

<span data-ttu-id="0a3e4-111"><span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*dwControlID*</span><span class="sxs-lookup"><span data-stu-id="0a3e4-111"><span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*dwControlID*</span></span>
</dt> <dd>

<span data-ttu-id="0a3e4-112">Identificador del control de mezclador que ha cambiado de estado.</span><span class="sxs-lookup"><span data-stu-id="0a3e4-112">Control identifier for the mixer control that has changed state.</span></span> <span data-ttu-id="0a3e4-113">Este identificador es el mismo que el miembro **dwControlID** de la estructura **MIXERCONTROL** devuelta por la función **mixerGetLineControls**.</span><span class="sxs-lookup"><span data-stu-id="0a3e4-113">This identifier is the same as the **dwControlID** member of the **MIXERCONTROL** structure returned by the **mixerGetLineControls** function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a3e4-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a3e4-114">Remarks</span></span>

<span data-ttu-id="0a3e4-115">Una aplicación debe abrir un dispositivo de mezclador y especificar una ventana de devolución de llamada para recibir el mensaje de **\_ cambio del \_ control \_ mm MIXM** .</span><span class="sxs-lookup"><span data-stu-id="0a3e4-115">An application must open a mixer device and specify a callback window to receive the **MM\_MIXM\_CONTROL\_CHANGE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a3e4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a3e4-116">Requirements</span></span>



| <span data-ttu-id="0a3e4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a3e4-117">Requirement</span></span> | <span data-ttu-id="0a3e4-118">Value</span><span class="sxs-lookup"><span data-stu-id="0a3e4-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a3e4-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a3e4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0a3e4-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0a3e4-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0a3e4-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a3e4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0a3e4-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0a3e4-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0a3e4-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a3e4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a3e4-124"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a3e4-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a3e4-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a3e4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a3e4-126">Mezcladores de audio</span><span class="sxs-lookup"><span data-stu-id="0a3e4-126">Audio Mixers</span></span>](audio-mixers.md)
</dt> <dt>

[<span data-ttu-id="0a3e4-127">Mensajes de mezclador de audio</span><span class="sxs-lookup"><span data-stu-id="0a3e4-127">Audio Mixer Messages</span></span>](audio-mixer-messages.md)
</dt> </dl>

 

 





