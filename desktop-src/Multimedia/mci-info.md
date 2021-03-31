---
title: Comando MCI_INFO (mmsystem. h)
description: El \_ comando MCI info recupera información de cadena de un dispositivo.
ms.assetid: aed3fed3-87b9-4673-9171-4f57770d765c
keywords:
- Comando de MCI_INFO de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_INFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9f6ba5be1c2a4ce94b880a87a468c594bc5b676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150962"
---
# <a name="mci_info-command"></a><span data-ttu-id="34843-104">Comando de información de MCI \_</span><span class="sxs-lookup"><span data-stu-id="34843-104">MCI\_INFO command</span></span>

<span data-ttu-id="34843-105">El \_ comando MCI info recupera información de cadena de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34843-105">The MCI\_INFO command retrieves string information from a device.</span></span> <span data-ttu-id="34843-106">Todos los dispositivos reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="34843-106">All devices recognize this command.</span></span> <span data-ttu-id="34843-107">La información se devuelve en el miembro **lpstrReturn** de la estructura identificada por *lpInfo*.</span><span class="sxs-lookup"><span data-stu-id="34843-107">Information is returned in the **lpstrReturn** member of the structure identified by *lpInfo*.</span></span> <span data-ttu-id="34843-108">El miembro **dwRetSize** especifica la longitud del búfer para los datos devueltos.</span><span class="sxs-lookup"><span data-stu-id="34843-108">The **dwRetSize** member specifies the buffer length for the returned data.</span></span>

<span data-ttu-id="34843-109">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="34843-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_INFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_INFO_PARMS) lpInfo
);
```



## <a name="parameters"></a><span data-ttu-id="34843-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34843-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34843-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="34843-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="34843-112">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="34843-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="34843-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="34843-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="34843-114">MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="34843-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="34843-115">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="34843-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="34843-116"><span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*lpInfo*</span><span class="sxs-lookup"><span data-stu-id="34843-116"><span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*lpInfo*</span></span>
</dt> <dd>

<span data-ttu-id="34843-117">Puntero a una [**estructura \_ \_ parms**](mci-info-parms.md) de la información de MCI.</span><span class="sxs-lookup"><span data-stu-id="34843-117">Pointer to an [**MCI\_INFO\_PARMS**](mci-info-parms.md) structure.</span></span> <span data-ttu-id="34843-118">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="34843-118">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34843-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34843-119">Return Value</span></span>

<span data-ttu-id="34843-120">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="34843-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="34843-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="34843-121">Remarks</span></span>

<span data-ttu-id="34843-122">La siguiente marca estándar adicional y específica del comando se aplica a todos los dispositivos que admiten la información de MCI \_ :</span><span class="sxs-lookup"><span data-stu-id="34843-122">The following additional standard and command-specific flag applies to all devices supporting MCI\_INFO:</span></span>

<dl> <dt>

<span data-ttu-id="34843-123"><span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>\_producto de información de MCI \_</span><span class="sxs-lookup"><span data-stu-id="34843-123"><span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>MCI\_INFO\_PRODUCT</span></span>
</dt> <dd>

<span data-ttu-id="34843-124">Obtiene una descripción del hardware asociado a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34843-124">Obtains a description of the hardware associated with a device.</span></span> <span data-ttu-id="34843-125">Los dispositivos deben proporcionar una descripción que identifique el controlador y el hardware utilizados.</span><span class="sxs-lookup"><span data-stu-id="34843-125">Devices should supply a description that identifies both the driver and the hardware used.</span></span>

</dd> </dl>

<span data-ttu-id="34843-126">Las siguientes marcas adicionales se aplican al tipo de dispositivo **cdaudio** :</span><span class="sxs-lookup"><span data-stu-id="34843-126">The following additional flags apply to the **cdaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="34843-127"><span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>\_identidad de \_ medios de información de MCI \_</span><span class="sxs-lookup"><span data-stu-id="34843-127"><span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>MCI\_INFO\_MEDIA\_IDENTITY</span></span>
</dt> <dd>

<span data-ttu-id="34843-128">Genera un identificador único para el CD de audio cargado actualmente en el reproductor que se consulta.</span><span class="sxs-lookup"><span data-stu-id="34843-128">Produces a unique identifier for the audio CD currently loaded in the player being queried.</span></span> <span data-ttu-id="34843-129">Esta marca devuelve una cadena de 16 dígitos hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="34843-129">This flag returns a string of 16 hexadecimal digits.</span></span>

</dd> <dt>

<span data-ttu-id="34843-130"><span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>\_UPC de \_ multimedia de información de MCI \_</span><span class="sxs-lookup"><span data-stu-id="34843-130"><span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>MCI\_INFO\_MEDIA\_UPC</span></span>
</dt> <dd>

<span data-ttu-id="34843-131">Genera el código universal de producto (UPC) que está codificado en un CD de audio.</span><span class="sxs-lookup"><span data-stu-id="34843-131">Produces the Universal Product Code (UPC) that is encoded on an audio CD.</span></span> <span data-ttu-id="34843-132">UPC es una cadena de dígitos.</span><span class="sxs-lookup"><span data-stu-id="34843-132">The UPC is a string of digits.</span></span> <span data-ttu-id="34843-133">Es posible que no esté disponible para todos los CD.</span><span class="sxs-lookup"><span data-stu-id="34843-133">It might not be available for all CDs.</span></span>

</dd> </dl>

<span data-ttu-id="34843-134">Las siguientes marcas adicionales se aplican al tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="34843-134">The following additional flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="34843-135"><span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>elemento de información de MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="34843-135"><span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>MCI\_DGV\_INFO\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="34843-136">Se incluye una constante que indica la información deseada en el miembro **dwItem** de la estructura identificada por *lpInfo*.</span><span class="sxs-lookup"><span data-stu-id="34843-136">A constant indicating the information desired is included in the **dwItem** member of the structure identified by *lpInfo*.</span></span> <span data-ttu-id="34843-137">Las siguientes constantes se definen para dispositivos de vídeo digital:</span><span class="sxs-lookup"><span data-stu-id="34843-137">The following constants are defined for digital-video devices:</span></span>

</dd> <dt>

<span data-ttu-id="34843-138"><span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>\_DGV de \_ audio de info \_ \_ de MCI</span><span class="sxs-lookup"><span data-stu-id="34843-138"><span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>MCI\_DGV\_INFO\_AUDIO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="34843-139">Devuelve el nombre del algoritmo de compresión de audio actual.</span><span class="sxs-lookup"><span data-stu-id="34843-139">Returns the name for the current audio compression algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="34843-140"><span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>MCI \_ DGV \_ info \_ audio \_ Quality</span><span class="sxs-lookup"><span data-stu-id="34843-140"><span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>MCI\_DGV\_INFO\_AUDIO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="34843-141">Devuelve el nombre del descriptor de calidad de audio actual.</span><span class="sxs-lookup"><span data-stu-id="34843-141">Returns the name for the current audio quality descriptor.</span></span>

</dd> <dt>

<span data-ttu-id="34843-142"><span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>información de DGV de MCI \_ \_ \_ todavía \_ alg</span><span class="sxs-lookup"><span data-stu-id="34843-142"><span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>MCI\_DGV\_INFO\_STILL\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="34843-143">Devuelve el nombre del algoritmo de compresión de imagen fija actual.</span><span class="sxs-lookup"><span data-stu-id="34843-143">Returns the name for the current still image compression algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="34843-144"><span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>calidad de la información de MCI \_ DGV \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="34843-144"><span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>MCI\_DGV\_INFO\_STILL\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="34843-145">Devuelve el nombre del descriptor de calidad de imagen todavía actual.</span><span class="sxs-lookup"><span data-stu-id="34843-145">Returns the name for the current still image quality descriptor.</span></span>

</dd> <dt>

<span data-ttu-id="34843-146"><span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>uso de información de MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="34843-146"><span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>MCI\_DGV\_INFO\_USAGE</span></span>
</dt> <dd>

<span data-ttu-id="34843-147">Devuelve una cadena que describe las restricciones de uso que puede imponer el propietario de los datos visuales o sonoros en el área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="34843-147">Returns a string describing usage restrictions that might be imposed by the owner of the visual or audible data in the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="34843-148"><span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>\_DGV de \_ vídeo de info \_ \_ de MCI</span><span class="sxs-lookup"><span data-stu-id="34843-148"><span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>MCI\_DGV\_INFO\_VIDEO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="34843-149">Devuelve el nombre del algoritmo de compresión de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="34843-149">Returns the name for the current video compression algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="34843-150"><span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>calidad de vídeo de MCI \_ DGV \_ info \_ \_</span><span class="sxs-lookup"><span data-stu-id="34843-150"><span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>MCI\_DGV\_INFO\_VIDEO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="34843-151">Devuelve el nombre del descriptor de calidad de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="34843-151">Returns the name for the current video quality descriptor.</span></span>

</dd> <dt>

<span data-ttu-id="34843-152"><span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>\_versión de información de MCI \_</span><span class="sxs-lookup"><span data-stu-id="34843-152"><span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>MCI\_INFO\_VERSION</span></span>
</dt> <dd>

<span data-ttu-id="34843-153">Devuelve el nivel de versión del controlador de dispositivo y el hardware.</span><span class="sxs-lookup"><span data-stu-id="34843-153">Returns the release level of the device driver and hardware.</span></span> <span data-ttu-id="34843-154">Los desarrolladores de controladores de dispositivos deben documentar la sintaxis de la cadena devuelta.</span><span class="sxs-lookup"><span data-stu-id="34843-154">Device driver developers must document the syntax of the returned string.</span></span>

</dd> <dt>

<span data-ttu-id="34843-155"><span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>texto de información de MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="34843-155"><span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>MCI\_DGV\_INFO\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="34843-156">Obtiene el título de la ventana.</span><span class="sxs-lookup"><span data-stu-id="34843-156">Obtains the window caption.</span></span>

</dd> <dt>

<span data-ttu-id="34843-157"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_archivo de información de MCI \_</span><span class="sxs-lookup"><span data-stu-id="34843-157"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="34843-158">Obtiene la ruta de acceso y el nombre del último archivo especificado con el comando [MCI \_ Open](mci-open.md) o [MCI \_ Load](mci-load.md) .</span><span class="sxs-lookup"><span data-stu-id="34843-158">Obtains the path and filename of the last file specified with the [MCI\_OPEN](mci-open.md) or [MCI\_LOAD](mci-load.md) command.</span></span> <span data-ttu-id="34843-159">Si no se ha especificado un archivo, el dispositivo devuelve una cadena terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="34843-159">If a file has not been specified, the device returns a null-terminated string.</span></span> <span data-ttu-id="34843-160">Esta marca solo es compatible con dispositivos que devuelven **true** a la \_ marca MCI GETDEVCAPS \_ use \_ files del comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="34843-160">This flag is supported only by devices that return **TRUE** to the MCI\_GETDEVCAPS\_USES\_FILES flag of the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command.</span></span>

</dd> </dl>

<span data-ttu-id="34843-161">En el caso de los dispositivos de vídeo digital, *lpInfo* apunta a una estructura [**MCI \_ DGV \_ info \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="34843-161">For digital-video devices, *lpInfo* points to an [**MCI\_DGV\_INFO\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa) structure.</span></span>

<span data-ttu-id="34843-162">Las siguientes marcas adicionales se aplican al tipo de dispositivo **Sequencer** :</span><span class="sxs-lookup"><span data-stu-id="34843-162">The following additional flags apply to the **sequencer** device type:</span></span>

<dl> <dt>

<span data-ttu-id="34843-163"><span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>\_copyright de información de MCI \_</span><span class="sxs-lookup"><span data-stu-id="34843-163"><span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>MCI\_INFO\_COPYRIGHT</span></span>
</dt> <dd>

<span data-ttu-id="34843-164">Obtiene el aviso de copyright del archivo MIDI del evento meta de copyright.</span><span class="sxs-lookup"><span data-stu-id="34843-164">Obtains the MIDI file copyright notice from the copyright meta event.</span></span>

</dd> <dt>

<span data-ttu-id="34843-165"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_archivo de información de MCI \_</span><span class="sxs-lookup"><span data-stu-id="34843-165"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="34843-166">Obtiene el nombre de archivo del archivo actual.</span><span class="sxs-lookup"><span data-stu-id="34843-166">Obtains the filename of the current file.</span></span> <span data-ttu-id="34843-167">Esta marca solo es compatible con los dispositivos que devuelven **true** cuando se llama al comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) con la \_ marca MCI GETDEVCAPS \_ usa \_ files.</span><span class="sxs-lookup"><span data-stu-id="34843-167">This flag is supported only by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_USES\_FILES flag.</span></span>

</dd> <dt>

<span data-ttu-id="34843-168"><span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>nombre de la información de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="34843-168"><span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>MCI\_INFO\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="34843-169">Obtiene el nombre de secuencia del evento meta Sequence/Track Name.</span><span class="sxs-lookup"><span data-stu-id="34843-169">Obtains the sequence name from the sequence/track name meta event.</span></span>

</dd> </dl>

<span data-ttu-id="34843-170">La marca adicional siguiente se aplica al tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="34843-170">The following additional flag applies to the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="34843-171"><span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>\_versión de \_ información de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="34843-171"><span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>MCI\_VCR\_INFO\_VERSION</span></span>
</dt> <dd>

<span data-ttu-id="34843-172">Establece el miembro **lpstrReturn** de la estructura [**MCI \_ info \_ parms**](mci-info-parms.md) para que apunte al número de versión.</span><span class="sxs-lookup"><span data-stu-id="34843-172">Sets **lpstrReturn** member of the [**MCI\_INFO\_PARMS**](mci-info-parms.md) structure to point to the version number.</span></span> <span data-ttu-id="34843-173">También establece el miembro **dwRetSize** igual a la longitud de la cadena a la que se señala.</span><span class="sxs-lookup"><span data-stu-id="34843-173">Also sets the **dwRetSize** member equal to the length of the string pointed to.</span></span>

</dd> </dl>

<span data-ttu-id="34843-174">Las siguientes marcas adicionales se aplican al tipo de dispositivo **superpuesto** :</span><span class="sxs-lookup"><span data-stu-id="34843-174">The following additional flags apply to the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="34843-175"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_archivo de información de MCI \_</span><span class="sxs-lookup"><span data-stu-id="34843-175"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="34843-176">Obtiene el nombre de archivo del archivo actual.</span><span class="sxs-lookup"><span data-stu-id="34843-176">Obtains the filename of the current file.</span></span> <span data-ttu-id="34843-177">Esta marca solo es compatible con dispositivos que devuelven **true** a la \_ marca MCI GETDEVCAPS \_ use \_ files del comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="34843-177">This flag is supported only by devices that return **TRUE** to the MCI\_GETDEVCAPS\_USES\_FILES flag of the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="34843-178"><span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>texto de información de MCI \_ OVLY \_ \_</span><span class="sxs-lookup"><span data-stu-id="34843-178"><span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>MCI\_OVLY\_INFO\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="34843-179">Obtiene el título de la ventana asociada con el dispositivo de superposición de vídeo.</span><span class="sxs-lookup"><span data-stu-id="34843-179">Obtains the caption of the window associated with the video-overlay device.</span></span>

</dd> </dl>

<span data-ttu-id="34843-180">Las siguientes marcas adicionales se aplican al tipo de dispositivo **WaveAudio** :</span><span class="sxs-lookup"><span data-stu-id="34843-180">The following additional flags apply to the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="34843-181"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_archivo de información de MCI \_</span><span class="sxs-lookup"><span data-stu-id="34843-181"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="34843-182">Obtiene el nombre de archivo del archivo actual.</span><span class="sxs-lookup"><span data-stu-id="34843-182">Obtains the filename of the current file.</span></span> <span data-ttu-id="34843-183">Esta marca es compatible con los dispositivos que devuelven **true** cuando se llama al comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) con la \_ marca MCI GETDEVCAPS \_ usa \_ files.</span><span class="sxs-lookup"><span data-stu-id="34843-183">This flag is supported by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_USES\_FILES flag.</span></span>

</dd> <dt>

<span data-ttu-id="34843-184"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrada de onda de MCI \_</span><span class="sxs-lookup"><span data-stu-id="34843-184"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="34843-185">Obtiene el nombre de producto de la entrada actual.</span><span class="sxs-lookup"><span data-stu-id="34843-185">Obtains the product name of the current input.</span></span>

</dd> <dt>

<span data-ttu-id="34843-186"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_salida de onda de MCI \_</span><span class="sxs-lookup"><span data-stu-id="34843-186"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="34843-187">Obtiene el nombre de producto de la salida actual y su valor es específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34843-187">Obtains the product name of the current output and its value is device specific.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="34843-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34843-188">Requirements</span></span>



| <span data-ttu-id="34843-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="34843-189">Requirement</span></span> | <span data-ttu-id="34843-190">Value</span><span class="sxs-lookup"><span data-stu-id="34843-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34843-191">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34843-191">Minimum supported client</span></span><br/> | <span data-ttu-id="34843-192">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="34843-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="34843-193">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34843-193">Minimum supported server</span></span><br/> | <span data-ttu-id="34843-194">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="34843-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="34843-195">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34843-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="34843-196"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34843-196"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34843-197">Vea también</span><span class="sxs-lookup"><span data-stu-id="34843-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34843-198">MCI</span><span class="sxs-lookup"><span data-stu-id="34843-198">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="34843-199">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="34843-199">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

