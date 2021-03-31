---
title: Comando MCI_PASTE (mmsystem. h)
description: El \_ comando MCI Paste pega los datos del portapapeles en un archivo. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: cad5799a-08ef-4e34-803a-415b937d8fbd
keywords:
- Comando de MCI_PASTE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_PASTE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15ff0ae3d14c1df63fbd9ab0c93a85446bdf066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801021"
---
# <a name="mci_paste-command"></a><span data-ttu-id="f1b3d-105">\_Comando de pegado de MCI</span><span class="sxs-lookup"><span data-stu-id="f1b3d-105">MCI\_PASTE command</span></span>

<span data-ttu-id="f1b3d-106">El \_ comando MCI Paste pega los datos del portapapeles en un archivo.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-106">The MCI\_PASTE command pastes data from the clipboard into a file.</span></span> <span data-ttu-id="f1b3d-107">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="f1b3d-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PASTE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_PASTE_PARMS) lpPaste
);
```



## <a name="parameters"></a><span data-ttu-id="f1b3d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1b3d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1b3d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f1b3d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f1b3d-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="f1b3d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="f1b3d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f1b3d-113">\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="f1b3d-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f1b3d-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1b3d-115"><span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lpPaste*</span><span class="sxs-lookup"><span data-stu-id="f1b3d-115"><span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lpPaste*</span></span>
</dt> <dd>

<span data-ttu-id="f1b3d-116">Puntero a una estructura de [**\_ DGV de copia de \_ \_ parms de MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms) .</span><span class="sxs-lookup"><span data-stu-id="f1b3d-116">Pointer to an [**MCI\_ DGV\_ PASTE\_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1b3d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1b3d-117">Return Value</span></span>

<span data-ttu-id="f1b3d-118">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1b3d-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1b3d-119">Remarks</span></span>

<span data-ttu-id="f1b3d-120">Las siguientes marcas adicionales se aplican a los dispositivos de vídeo digital:</span><span class="sxs-lookup"><span data-stu-id="f1b3d-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="f1b3d-121"><span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>\_pegar DGV \_ \_ de MCI</span><span class="sxs-lookup"><span data-stu-id="f1b3d-121"><span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>MCI\_DGV\_PASTE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="f1b3d-122">Se incluye un rectángulo en el miembro **RC** de la estructura identificada por *lpPaste*.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-122">A rectangle is included in the **rc** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="f1b3d-123">Los dos primeros valores del rectángulo especifican el punto dentro del marco para colocar la información del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-123">The first two values of the rectangle specify the point within the frame to place the clipboard information.</span></span> <span data-ttu-id="f1b3d-124">Si el alto y el ancho del rectángulo son distintos de cero, el contenido del portapapeles se escala a esas dimensiones cuando se pegan en el marco.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-124">If the rectangle height and width are nonzero, the clipboard contents are scaled to those dimensions when they are pasted in the frame.</span></span> <span data-ttu-id="f1b3d-125">Si se omite la marca, el pegado de MCI tiene como \_ valor predeterminado el rectángulo del marco completo.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-125">If the flag is omitted, MCI\_PASTE defaults to the entire frame rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="f1b3d-126"><span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>MCI \_ DGV \_ pegar \_ secuencia de audio \_</span><span class="sxs-lookup"><span data-stu-id="f1b3d-126"><span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>MCI\_DGV\_PASTE\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="f1b3d-127">Un número de secuencia de audio se incluye en el miembro **dwAudioStream** de la estructura identificada por *lpPaste*.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-127">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="f1b3d-128">Si solo existe una secuencia de audio en el portapapeles, los datos de audio se pegan en la secuencia designada.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-128">If only one audio stream exists on the clipboard, the audio data is pasted into the designated stream.</span></span> <span data-ttu-id="f1b3d-129">Si existe más de una secuencia de audio en el portapapeles, la secuencia indica el número de inicio de las secuencias de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-129">If more than one audio stream exists on the clipboard, the stream indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="f1b3d-130">Si usa esta marca y también quiere pegar vídeo, también debe usar la \_ marca MCI DGV \_ pegar vídeo de \_ la \_ secuencia.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-130">If you use this flag and also want to paste video, you must also use the MCI\_DGV\_PASTE\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="f1b3d-131">(Si no se especifica ninguna marca, todas las secuencias de audio y vídeo se pegarán a partir de la primera secuencia de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-131">(If neither flag is specified, all audio and video streams are pasted starting with the first audio and video stream.</span></span> <span data-ttu-id="f1b3d-132">Cada secuencia pegada conserva su número de secuencia original).</span><span class="sxs-lookup"><span data-stu-id="f1b3d-132">Each pasted stream retains its original stream number.)</span></span>

</dd> <dt>

<span data-ttu-id="f1b3d-133"><span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>\_DGV MCI \_ pegar \_ inserción</span><span class="sxs-lookup"><span data-stu-id="f1b3d-133"><span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>MCI\_DGV\_PASTE\_INSERT</span></span>
</dt> <dd>

<span data-ttu-id="f1b3d-134">Los datos del portapapeles se deben insertar en el área de trabajo existente en la posición especificada por el MCI \_ para la marca.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-134">Clipboard data should be inserted in the existing workspace at the position specified by the MCI\_TO flag.</span></span> <span data-ttu-id="f1b3d-135">Los datos existentes después del punto de inserción se mueven en el área de trabajo para dejar espacio.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-135">Any existing data after the insertion point is moved in the workspace to make room.</span></span> <span data-ttu-id="f1b3d-136">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-136">This is the default.</span></span>

</dd> <dt>

<span data-ttu-id="f1b3d-137"><span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>SOBRESCRITURA de la copia de DGV de MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="f1b3d-137"><span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>MCI\_DGV\_PASTE\_OVERWRITE</span></span>
</dt> <dd>

<span data-ttu-id="f1b3d-138">Los datos del portapapeles deben reemplazar los datos que ya están presentes en el área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-138">Clipboard data should replace data already present in the workspace.</span></span> <span data-ttu-id="f1b3d-139">Los datos del área de trabajo reemplazan después del punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-139">The workspace data replaced follows the insertion point.</span></span>

</dd> <dt>

<span data-ttu-id="f1b3d-140"><span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>\_secuencia de \_ vídeo de pegado de MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="f1b3d-140"><span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>MCI\_DGV\_PASTE\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="f1b3d-141">Un número de secuencia de vídeo se incluye en el miembro **dwVideoStream** de la estructura identificada por *lpPaste*.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-141">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="f1b3d-142">Si solo existe una secuencia de vídeo en el portapapeles, los datos de vídeo se pegan en la secuencia designada.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-142">If only one video stream exists on the clipboard, the video data is pasted into the designated stream.</span></span> <span data-ttu-id="f1b3d-143">Si existe más de una secuencia de vídeo en el portapapeles, la secuencia indica el número de inicio de las secuencias de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-143">If more than one video stream exists on the clipboard, the stream indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="f1b3d-144">Si usa esta marca y también quiere pegar audio, también debe usar la \_ marca MCI DGV \_ pegar audio de \_ la \_ secuencia.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-144">If you use this flag and also want to paste audio, you must also use the MCI\_DGV\_PASTE\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="f1b3d-145">(Si no se especifica ninguna marca, todas las secuencias de audio y vídeo se pegarán a partir de la primera secuencia de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-145">(If neither flag is specified, all audio and video streams are pasted starting with the first audio and video stream.</span></span> <span data-ttu-id="f1b3d-146">Cada secuencia pegada conserva su número de secuencia original).</span><span class="sxs-lookup"><span data-stu-id="f1b3d-146">Each pasted stream retains its original stream number.)</span></span>

</dd> <dt>

<span data-ttu-id="f1b3d-147"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ a</span><span class="sxs-lookup"><span data-stu-id="f1b3d-147"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="f1b3d-148">Un valor de posición se incluye en el miembro **dwTo** de la estructura identificada por *lpPaste*.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-148">A position value is included in the **dwTo** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="f1b3d-149">El valor de posición especifica la posición en la que se comienzan a pegar los datos en el área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-149">The position value specifies the position to begin pasting data into the workspace.</span></span> <span data-ttu-id="f1b3d-150">Si se omite esta marca, la posición tiene como valor predeterminado la posición actual.</span><span class="sxs-lookup"><span data-stu-id="f1b3d-150">If this flag is omitted, the position defaults to the current position.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1b3d-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1b3d-151">Requirements</span></span>



| <span data-ttu-id="f1b3d-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1b3d-152">Requirement</span></span> | <span data-ttu-id="f1b3d-153">Value</span><span class="sxs-lookup"><span data-stu-id="f1b3d-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1b3d-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1b3d-154">Minimum supported client</span></span><br/> | <span data-ttu-id="f1b3d-155">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f1b3d-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f1b3d-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1b3d-156">Minimum supported server</span></span><br/> | <span data-ttu-id="f1b3d-157">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f1b3d-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f1b3d-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1b3d-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1b3d-159"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1b3d-159"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1b3d-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1b3d-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1b3d-161">MCI</span><span class="sxs-lookup"><span data-stu-id="f1b3d-161">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f1b3d-162">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="f1b3d-162">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

