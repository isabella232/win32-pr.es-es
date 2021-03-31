---
title: Comando MCI_COPY (mmsystem. h)
description: El comando de copia de MCI \_ copia los datos en el portapapeles. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 41807920-3312-4cdb-82e6-6ab4b9b35162
keywords:
- Comando de MCI_COPY de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_COPY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4c27950b9599d0b565b982eb59755e4d3f2ea65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996452"
---
# <a name="mci_copy-command"></a><span data-ttu-id="c1392-105">Comando de copia de MCI \_</span><span class="sxs-lookup"><span data-stu-id="c1392-105">MCI\_COPY command</span></span>

<span data-ttu-id="c1392-106">El comando de copia de MCI \_ copia los datos en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="c1392-106">The MCI\_COPY command copies data to the clipboard.</span></span> <span data-ttu-id="c1392-107">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="c1392-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="c1392-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="c1392-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_COPY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_COPY_PARMS) lpCopy
);
```



## <a name="parameters"></a><span data-ttu-id="c1392-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1392-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1392-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c1392-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c1392-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="c1392-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="c1392-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="c1392-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c1392-113">\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI.</span><span class="sxs-lookup"><span data-stu-id="c1392-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="c1392-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c1392-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1392-115"><span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*lpCopy*</span><span class="sxs-lookup"><span data-stu-id="c1392-115"><span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*lpCopy*</span></span>
</dt> <dd>

<span data-ttu-id="c1392-116">Puntero a una estructura [**MCI \_ DGV \_ Copy \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms) .</span><span class="sxs-lookup"><span data-stu-id="c1392-116">Pointer to an [**MCI\_DGV\_COPY\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1392-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1392-117">Return Value</span></span>

<span data-ttu-id="c1392-118">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c1392-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1392-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1392-119">Remarks</span></span>

<span data-ttu-id="c1392-120">Las siguientes marcas adicionales se aplican a los dispositivos de vídeo digital:</span><span class="sxs-lookup"><span data-stu-id="c1392-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="c1392-121"><span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>\_ \_ copia de DGV \_ de MCI en</span><span class="sxs-lookup"><span data-stu-id="c1392-121"><span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>MCI\_DGV\_COPY\_AT</span></span>
</dt> <dd>

<span data-ttu-id="c1392-122">Se incluye un rectángulo en el miembro **RC** de la estructura identificada por *lpCopy*.</span><span class="sxs-lookup"><span data-stu-id="c1392-122">A rectangle is included in the **rc** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="c1392-123">El rectángulo especifica la parte de cada fotograma que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="c1392-123">The rectangle specifies the portion of each frame to copy.</span></span> <span data-ttu-id="c1392-124">Si se omite la marca, \_ la copia de MCI copia todo el marco.</span><span class="sxs-lookup"><span data-stu-id="c1392-124">If the flag is omitted, MCI\_COPY copies the entire frame.</span></span>

</dd> <dt>

<span data-ttu-id="c1392-125"><span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>\_secuencia de \_ audio de copia DGV \_ de MCI \_</span><span class="sxs-lookup"><span data-stu-id="c1392-125"><span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>MCI\_DGV\_COPY\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="c1392-126">Un número de secuencia de audio se incluye en el miembro **dwAudioStream** de la estructura identificada por *lpCopy*.</span><span class="sxs-lookup"><span data-stu-id="c1392-126">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="c1392-127">Si usa esta marca y también quiere copiar vídeo, también debe usar la \_ marca MCI DGV \_ Copy \_ vídeo \_ Stream.</span><span class="sxs-lookup"><span data-stu-id="c1392-127">If you use this flag and also want to copy video, you must also use the MCI\_DGV\_COPY\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="c1392-128">(Si no se especifica ninguna marca, se copian los datos de todas las secuencias de audio y vídeo).</span><span class="sxs-lookup"><span data-stu-id="c1392-128">(If neither flag is specified, data from all audio and video streams is copied.)</span></span>

</dd> <dt>

<span data-ttu-id="c1392-129"><span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>\_secuencia de \_ vídeo de copiar DGV \_ de MCI \_</span><span class="sxs-lookup"><span data-stu-id="c1392-129"><span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>MCI\_DGV\_COPY\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="c1392-130">Un número de secuencia de vídeo se incluye en el miembro **dwVideoStream** de la estructura identificada por *lpCopy*.</span><span class="sxs-lookup"><span data-stu-id="c1392-130">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="c1392-131">Si usa esta marca y también quiere copiar audio, también debe usar la \_ marca MCI DGV \_ Copy \_ audio \_ Stream.</span><span class="sxs-lookup"><span data-stu-id="c1392-131">If you use this flag and also want to copy audio, you must also use the MCI\_DGV\_COPY\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="c1392-132">(Si no se especifica ninguna marca, se copian los datos de todas las secuencias de audio y vídeo).</span><span class="sxs-lookup"><span data-stu-id="c1392-132">(If neither flag is specified, data from all audio and video streams is copied.)</span></span>

</dd> <dt>

<span data-ttu-id="c1392-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ desde</span><span class="sxs-lookup"><span data-stu-id="c1392-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="c1392-134">Una ubicación de inicio se incluye en el miembro **dwFrom** de la estructura identificada por *lpCopy*.</span><span class="sxs-lookup"><span data-stu-id="c1392-134">A starting location is included in the **dwFrom** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="c1392-135">Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI del comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="c1392-135">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="c1392-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ a</span><span class="sxs-lookup"><span data-stu-id="c1392-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="c1392-137">Una ubicación final se incluye en el miembro **dwTo** de la estructura identificada por *lpCopy*.</span><span class="sxs-lookup"><span data-stu-id="c1392-137">An ending location is included in the **dwTo** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="c1392-138">Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI del \_ comando MCI set.</span><span class="sxs-lookup"><span data-stu-id="c1392-138">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the MCI\_SET command.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1392-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1392-139">Requirements</span></span>



| <span data-ttu-id="c1392-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1392-140">Requirement</span></span> | <span data-ttu-id="c1392-141">Value</span><span class="sxs-lookup"><span data-stu-id="c1392-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1392-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1392-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c1392-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c1392-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c1392-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1392-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c1392-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c1392-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c1392-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c1392-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1392-147"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1392-147"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1392-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1392-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1392-149">MCI</span><span class="sxs-lookup"><span data-stu-id="c1392-149">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c1392-150">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="c1392-150">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

