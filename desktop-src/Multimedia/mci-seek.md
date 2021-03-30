---
title: Comando MCI_SEEK (mmsystem. h)
description: El \_ comando MCI Seek cambia la posición actual en el contenido lo más rápido posible.
ms.assetid: 5ffab964-a28d-4dc2-ac04-da501cd34d24
keywords:
- Comando de MCI_SEEK de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0e34f6fa823092968e74515a885e7a40db9f2d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079061"
---
# <a name="mci_seek-command"></a><span data-ttu-id="bb7d5-104">Comando de búsqueda de MCI \_</span><span class="sxs-lookup"><span data-stu-id="bb7d5-104">MCI\_SEEK command</span></span>

<span data-ttu-id="bb7d5-105">El \_ comando MCI Seek cambia la posición actual en el contenido lo más rápido posible.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-105">The MCI\_SEEK command changes the current position in the content as quickly as possible.</span></span> <span data-ttu-id="bb7d5-106">La salida de vídeo y audio se deshabilitan durante la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-106">Video and audio output are disabled during the seek.</span></span> <span data-ttu-id="bb7d5-107">Una vez finalizada la búsqueda, el dispositivo se detiene.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-107">After the seek is complete, the device is stopped.</span></span> <span data-ttu-id="bb7d5-108">Los dispositivos de audio de CD, digital-video, MIDI Sequencer, VCR, Videodisc y de onda-audio reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-108">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="bb7d5-109">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SEEK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SEEK_PARMS) lpSeek
);
```



## <a name="parameters"></a><span data-ttu-id="bb7d5-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb7d5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb7d5-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="bb7d5-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="bb7d5-112">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="bb7d5-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="bb7d5-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="bb7d5-114">MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="bb7d5-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="bb7d5-115">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="bb7d5-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb7d5-116"><span id="lpSeek"></span><span id="lpseek"></span><span id="LPSEEK"></span>*lpSeek*</span><span class="sxs-lookup"><span data-stu-id="bb7d5-116"><span id="lpSeek"></span><span id="lpseek"></span><span id="LPSEEK"></span>*lpSeek*</span></span>
</dt> <dd>

<span data-ttu-id="bb7d5-117">Puntero a una [**estructura \_ \_ parms de búsqueda de MCI**](mci-seek-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="bb7d5-117">Pointer to an [**MCI\_SEEK\_PARMS**](mci-seek-parms.md) structure.</span></span> <span data-ttu-id="bb7d5-118">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="bb7d5-118">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb7d5-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb7d5-119">Return Value</span></span>

<span data-ttu-id="bb7d5-120">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb7d5-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb7d5-121">Remarks</span></span>

<span data-ttu-id="bb7d5-122">Si un tamaño de muestra de datos para un dispositivo es mayor que 1 byte (por ejemplo, con datos estéreo de audio de onda), este comando se desplaza al principio del ejemplo más próximo cuando una posición especificada no coincide con el inicio de un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-122">If a data sample size for a device is larger than 1 byte (such as with waveform-audio stereo data), this command moves to the beginning of the nearest sample when a specified position does not coincide with the start of a sample.</span></span>

<span data-ttu-id="bb7d5-123">Las siguientes marcas adicionales se aplican a todos los dispositivos que admiten MCI \_ Seek:</span><span class="sxs-lookup"><span data-stu-id="bb7d5-123">The following additional flags apply to all devices supporting MCI\_SEEK:</span></span>

<dl> <dt>

<span data-ttu-id="bb7d5-124"><span id="MCI_SEEK_TO_END"></span><span id="mci_seek_to_end"></span>\_búsqueda \_ de MCI hasta el \_ final</span><span class="sxs-lookup"><span data-stu-id="bb7d5-124"><span id="MCI_SEEK_TO_END"></span><span id="mci_seek_to_end"></span>MCI\_SEEK\_TO\_END</span></span>
</dt> <dd>

<span data-ttu-id="bb7d5-125">Busque el final del contenido.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-125">Seek to the end of the content.</span></span>

</dd> <dt>

<span data-ttu-id="bb7d5-126"><span id="MCI_SEEK_TO_START"></span><span id="mci_seek_to_start"></span>\_búsqueda \_ de MCI en \_ Start</span><span class="sxs-lookup"><span data-stu-id="bb7d5-126"><span id="MCI_SEEK_TO_START"></span><span id="mci_seek_to_start"></span>MCI\_SEEK\_TO\_START</span></span>
</dt> <dd>

<span data-ttu-id="bb7d5-127">Busque el principio del contenido.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-127">Seek to the beginning of the content.</span></span>

</dd> <dt>

<span data-ttu-id="bb7d5-128"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ a</span><span class="sxs-lookup"><span data-stu-id="bb7d5-128"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="bb7d5-129">Se incluye una posición en el miembro **dwTo** de la estructura identificada por *lpSeek*.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-129">A position is included in the **dwTo** member of the structure identified by *lpSeek*.</span></span> <span data-ttu-id="bb7d5-130">Las unidades asignadas a los valores de posición se especifican con la \_ \_ \_ marca de formato de tiempo Set MCI del comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="bb7d5-130">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="bb7d5-131">No use esta marca con MCI \_ Seek \_ to \_ End o MCI \_ Seek \_ to \_ Start.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-131">Do not use this flag with MCI\_SEEK\_TO\_END or MCI\_SEEK\_TO\_START.</span></span>

</dd> </dl>

<span data-ttu-id="bb7d5-132">Se usan las siguientes marcas adicionales con el tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="bb7d5-132">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="bb7d5-133"><span id="MCI_VCR_SEEK_AT"></span><span id="mci_vcr_seek_at"></span>\_ \_ búsqueda de VCR \_ de MCI en</span><span class="sxs-lookup"><span data-stu-id="bb7d5-133"><span id="MCI_VCR_SEEK_AT"></span><span id="mci_vcr_seek_at"></span>MCI\_VCR\_SEEK\_AT</span></span>
</dt> <dd>

<span data-ttu-id="bb7d5-134">El miembro **dwAt** de la estructura identificada por *lpSeek* contiene la hora a la que comienza el comando completo.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-134">The **dwAt** member of the structure identified by *lpSeek* contains a time when the entire command begins.</span></span>

</dd> <dt>

<span data-ttu-id="bb7d5-135"><span id="MCI_VCR_SEEK_MARK"></span><span id="mci_vcr_seek_mark"></span>\_marca de \_ búsqueda de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="bb7d5-135"><span id="MCI_VCR_SEEK_MARK"></span><span id="mci_vcr_seek_mark"></span>MCI\_VCR\_SEEK\_MARK</span></span>
</dt> <dd>

<span data-ttu-id="bb7d5-136">El miembro **dwMark** de la estructura identificada por *lpSeek* contiene la marca numerada que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-136">The **dwMark** member of the structure identified by *lpSeek* contains the numbered mark to search for.</span></span>

</dd> <dt>

<span data-ttu-id="bb7d5-137"><span id="MCI_VCR_SEEK_REVERSE"></span><span id="mci_vcr_seek_reverse"></span>búsqueda de VCR de MCI \_ \_ \_ inversa</span><span class="sxs-lookup"><span data-stu-id="bb7d5-137"><span id="MCI_VCR_SEEK_REVERSE"></span><span id="mci_vcr_seek_reverse"></span>MCI\_VCR\_SEEK\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="bb7d5-138">La dirección de búsqueda es inversa; solo se usa con la marca de \_ búsqueda de vídeo de MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="bb7d5-138">Seek direction is reverse; this is used only with the MCI\_VCR\_SEEK\_MARK flag.</span></span>

</dd> </dl>

<span data-ttu-id="bb7d5-139">En el caso de los dispositivos VCR, el parámetro *lpSeek* apunta a una estructura [**parms de búsqueda de VCR de MCI \_ \_ \_**](mci-vcr-seek-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="bb7d5-139">For VCR devices, the *lpSeek* parameter points to an [**MCI\_VCR\_SEEK\_PARMS**](mci-vcr-seek-parms.md) structure.</span></span>

<span data-ttu-id="bb7d5-140">La siguiente marca adicional se usa con el tipo de dispositivo de **videodisco** :</span><span class="sxs-lookup"><span data-stu-id="bb7d5-140">The following additional flag is used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="bb7d5-141"><span id="MCI_VD_SEEK_REVERSE"></span><span id="mci_vd_seek_reverse"></span>búsqueda de MCI \_ Vd \_ \_ inverso</span><span class="sxs-lookup"><span data-stu-id="bb7d5-141"><span id="MCI_VD_SEEK_REVERSE"></span><span id="mci_vd_seek_reverse"></span>MCI\_VD\_SEEK\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="bb7d5-142">La dirección de búsqueda es inversa.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-142">Seek direction is reverse.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb7d5-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb7d5-143">Requirements</span></span>



| <span data-ttu-id="bb7d5-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb7d5-144">Requirement</span></span> | <span data-ttu-id="bb7d5-145">Value</span><span class="sxs-lookup"><span data-stu-id="bb7d5-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb7d5-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb7d5-146">Minimum supported client</span></span><br/> | <span data-ttu-id="bb7d5-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bb7d5-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bb7d5-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb7d5-148">Minimum supported server</span></span><br/> | <span data-ttu-id="bb7d5-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bb7d5-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bb7d5-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb7d5-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb7d5-151"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb7d5-151"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb7d5-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb7d5-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb7d5-153">MCI</span><span class="sxs-lookup"><span data-stu-id="bb7d5-153">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="bb7d5-154">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="bb7d5-154">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

