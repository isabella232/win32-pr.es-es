---
title: Comando MCI_CUT (mmsystem. h)
description: El \_ comando MCI CUT quita los datos del archivo y los copia en el portapapeles. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 09bb505b-715a-4393-80f0-e9ba270a8ac1
keywords:
- Comando de MCI_CUT de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_CUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c564451596f115daca8514785449abf001e224ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996702"
---
# <a name="mci_cut-command"></a><span data-ttu-id="f4eca-105">Comando de corte de MCI \_</span><span class="sxs-lookup"><span data-stu-id="f4eca-105">MCI\_CUT command</span></span>

<span data-ttu-id="f4eca-106">El \_ comando MCI CUT quita los datos del archivo y los copia en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="f4eca-106">The MCI\_CUT command removes data from the file and copies it to the clipboard.</span></span> <span data-ttu-id="f4eca-107">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="f4eca-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="f4eca-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="f4eca-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CUT_PARMS) lpCut
);
```



## <a name="parameters"></a><span data-ttu-id="f4eca-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4eca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4eca-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f4eca-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f4eca-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="f4eca-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="f4eca-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="f4eca-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f4eca-113">\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI.</span><span class="sxs-lookup"><span data-stu-id="f4eca-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="f4eca-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f4eca-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4eca-115"><span id="lpCut"></span><span id="lpcut"></span><span id="LPCUT"></span>*lpCut*</span><span class="sxs-lookup"><span data-stu-id="f4eca-115"><span id="lpCut"></span><span id="lpcut"></span><span id="LPCUT"></span>*lpCut*</span></span>
</dt> <dd>

<span data-ttu-id="f4eca-116">Puntero a una estructura de [**parms de DGV de MCI \_ \_ \_ cortada**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms) .</span><span class="sxs-lookup"><span data-stu-id="f4eca-116">Pointer to an [**MCI\_DGV\_CUT\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4eca-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4eca-117">Return Value</span></span>

<span data-ttu-id="f4eca-118">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f4eca-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4eca-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4eca-119">Remarks</span></span>

<span data-ttu-id="f4eca-120">Las siguientes marcas adicionales se aplican a los dispositivos de vídeo digital:</span><span class="sxs-lookup"><span data-stu-id="f4eca-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="f4eca-121"><span id="MCI_DGV_CUT_AT"></span><span id="mci_dgv_cut_at"></span>\_DGV \_ de MCI cortado \_ en</span><span class="sxs-lookup"><span data-stu-id="f4eca-121"><span id="MCI_DGV_CUT_AT"></span><span id="mci_dgv_cut_at"></span>MCI\_DGV\_CUT\_AT</span></span>
</dt> <dd>

<span data-ttu-id="f4eca-122">Se incluye un rectángulo en el miembro **RC** de la estructura identificada por *lpCut*.</span><span class="sxs-lookup"><span data-stu-id="f4eca-122">A rectangle is included in the **rc** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="f4eca-123">El rectángulo especifica la parte de cada fotograma que se va a cortar.</span><span class="sxs-lookup"><span data-stu-id="f4eca-123">The rectangle specifies the portion of each frame to cut.</span></span> <span data-ttu-id="f4eca-124">Si se omite la marca, \_ el corte de MCI corta todo el marco.</span><span class="sxs-lookup"><span data-stu-id="f4eca-124">If the flag is omitted, MCI\_CUT cuts the entire frame.</span></span>

</dd> <dt>

<span data-ttu-id="f4eca-125"><span id="MCI_DGV_CUT_AUDIO_STREAM"></span><span id="mci_dgv_cut_audio_stream"></span>\_flujo de \_ audio de cortar DGV \_ de MCI \_</span><span class="sxs-lookup"><span data-stu-id="f4eca-125"><span id="MCI_DGV_CUT_AUDIO_STREAM"></span><span id="mci_dgv_cut_audio_stream"></span>MCI\_DGV\_CUT\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="f4eca-126">Un número de secuencia de audio se incluye en el miembro **dwAudioStream** de la estructura identificada por *lpCut*.</span><span class="sxs-lookup"><span data-stu-id="f4eca-126">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="f4eca-127">Si usa esta marca y también desea cortar vídeo, también debe usar la \_ marca MCI DGV \_ Cut \_ video \_ Stream.</span><span class="sxs-lookup"><span data-stu-id="f4eca-127">If you use this flag and also want to cut video, you must also use the MCI\_DGV\_CUT\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="f4eca-128">(Si no se especifica ninguna marca, se cortarán los datos de todas las secuencias de audio y vídeo).</span><span class="sxs-lookup"><span data-stu-id="f4eca-128">(If neither flag is specified, data from all audio and video streams is cut.)</span></span>

</dd> <dt>

<span data-ttu-id="f4eca-129"><span id="MCI_DGV_CUT_VIDEO_STREAM"></span><span id="mci_dgv_cut_video_stream"></span>\_flujo de \_ vídeo de cortar DGV \_ de MCI \_</span><span class="sxs-lookup"><span data-stu-id="f4eca-129"><span id="MCI_DGV_CUT_VIDEO_STREAM"></span><span id="mci_dgv_cut_video_stream"></span>MCI\_DGV\_CUT\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="f4eca-130">Un número de secuencia de vídeo se incluye en el miembro **dwVideoStream** de la estructura identificada por *lpCut*.</span><span class="sxs-lookup"><span data-stu-id="f4eca-130">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="f4eca-131">Si usa esta marca y también desea cortar audio, también debe usar la \_ marca MCI DGV \_ Cut \_ audio \_ Stream.</span><span class="sxs-lookup"><span data-stu-id="f4eca-131">If you use this flag and also want to cut audio, you must also use the MCI\_DGV\_CUT\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="f4eca-132">(Si no se especifica ninguna marca, se cortarán los datos de todas las secuencias de audio y vídeo).</span><span class="sxs-lookup"><span data-stu-id="f4eca-132">(If neither flag is specified, data from all audio and video streams is cut.)</span></span>

</dd> <dt>

<span data-ttu-id="f4eca-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ desde</span><span class="sxs-lookup"><span data-stu-id="f4eca-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="f4eca-134">Una ubicación de inicio se incluye en el miembro **dwFrom** de la estructura identificada por *lpCut*.</span><span class="sxs-lookup"><span data-stu-id="f4eca-134">A starting location is included in the **dwFrom** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="f4eca-135">Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI del comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="f4eca-135">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="f4eca-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ a</span><span class="sxs-lookup"><span data-stu-id="f4eca-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="f4eca-137">Una ubicación final se incluye en el miembro **dwTo** de la estructura identificada por *lpCut*.</span><span class="sxs-lookup"><span data-stu-id="f4eca-137">An ending location is included in the **dwTo** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="f4eca-138">Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI de MCI \_ set.</span><span class="sxs-lookup"><span data-stu-id="f4eca-138">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f4eca-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4eca-139">Requirements</span></span>



| <span data-ttu-id="f4eca-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4eca-140">Requirement</span></span> | <span data-ttu-id="f4eca-141">Value</span><span class="sxs-lookup"><span data-stu-id="f4eca-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4eca-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4eca-142">Minimum supported client</span></span><br/> | <span data-ttu-id="f4eca-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f4eca-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f4eca-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4eca-144">Minimum supported server</span></span><br/> | <span data-ttu-id="f4eca-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f4eca-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f4eca-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4eca-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4eca-147"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4eca-147"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4eca-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4eca-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4eca-149">MCI</span><span class="sxs-lookup"><span data-stu-id="f4eca-149">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f4eca-150">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="f4eca-150">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

