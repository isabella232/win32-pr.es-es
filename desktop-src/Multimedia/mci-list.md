---
title: Comando MCI_LIST (mmsystem. h)
description: El \_ comando MCI List obtiene información sobre el número y los tipos de entradas disponibles para el dispositivo. Los dispositivos digitales-vídeo y VCR reconocen este comando.
ms.assetid: 1977fbfa-cae4-4afe-9fc5-ac68177574ca
keywords:
- Comando de MCI_LIST de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_LIST
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d5a616085028132c83fd71c46f7d409bf48a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535422"
---
# <a name="mci_list-command"></a><span data-ttu-id="509e7-105">\_Comando de lista MCI</span><span class="sxs-lookup"><span data-stu-id="509e7-105">MCI\_LIST command</span></span>

<span data-ttu-id="509e7-106">El \_ comando MCI List obtiene información sobre el número y los tipos de entradas disponibles para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="509e7-106">The MCI\_LIST command obtains information about the number and types of inputs available to the device.</span></span> <span data-ttu-id="509e7-107">Los dispositivos digitales-vídeo y VCR reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="509e7-107">Digital-video and VCR devices recognize this command.</span></span>

<span data-ttu-id="509e7-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="509e7-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LIST, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpList
);
```



## <a name="parameters"></a><span data-ttu-id="509e7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="509e7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="509e7-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="509e7-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="509e7-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="509e7-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="509e7-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="509e7-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="509e7-113">\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI.</span><span class="sxs-lookup"><span data-stu-id="509e7-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="509e7-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="509e7-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="509e7-115"><span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lpList*</span><span class="sxs-lookup"><span data-stu-id="509e7-115"><span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lpList*</span></span>
</dt> <dd>

<span data-ttu-id="509e7-116">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="509e7-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="509e7-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="509e7-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="509e7-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="509e7-118">Return Value</span></span>

<span data-ttu-id="509e7-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="509e7-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="509e7-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="509e7-120">Remarks</span></span>

<span data-ttu-id="509e7-121">Las siguientes marcas adicionales se aplican al tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="509e7-121">The following additional flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="509e7-122"><span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>\_DGV de \_ lista de MCI \_</span><span class="sxs-lookup"><span data-stu-id="509e7-122"><span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>MCI\_DGV\_LIST\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="509e7-123">El miembro **lpstrAlgorithm** de la estructura identificada por *lpList* contiene una dirección de un búfer que contiene el nombre de un algoritmo.</span><span class="sxs-lookup"><span data-stu-id="509e7-123">The **lpstrAlgorithm** member of the structure identified by *lpList* contains an address of a buffer containing the name of an algorithm.</span></span> <span data-ttu-id="509e7-124">El nombre se utiliza para recuperar los tipos de descriptores de calidad asociados a un algoritmo.</span><span class="sxs-lookup"><span data-stu-id="509e7-124">The name is used to retrieve the types of quality descriptors associated with an algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="509e7-125"><span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>recuento de listas de DGV de MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="509e7-125"><span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>MCI\_DGV\_LIST\_COUNT</span></span>
</dt> <dd>

<span data-ttu-id="509e7-126">Devuelve el número de opciones del tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="509e7-126">Returns the number of options of the specified type.</span></span>

</dd> <dt>

<span data-ttu-id="509e7-127"><span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>\_elemento de \_ lista \_ DGV de MCI</span><span class="sxs-lookup"><span data-stu-id="509e7-127"><span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>MCI\_DGV\_LIST\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="509e7-128">Una constante que indica que el tipo de lista se incluye en el miembro **dwItem** de la estructura identificada por *lpList*.</span><span class="sxs-lookup"><span data-stu-id="509e7-128">A constant indicating the list type is included in the **dwItem** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="509e7-129">Esta marca es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="509e7-129">This flag is required.</span></span> <span data-ttu-id="509e7-130">Use una de las siguientes constantes para indicar el tipo de lista:</span><span class="sxs-lookup"><span data-stu-id="509e7-130">Use one of the following constants to indicate the list type:</span></span>

</dd> <dt>

<span data-ttu-id="509e7-131"><span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>\_DGV de \_ audio de lista \_ \_ de MCI</span><span class="sxs-lookup"><span data-stu-id="509e7-131"><span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>MCI\_DGV\_LIST\_AUDIO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="509e7-132">El comando debe recuperar los nombres de los algoritmos de audio.</span><span class="sxs-lookup"><span data-stu-id="509e7-132">The command should retrieve names of audio algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="509e7-133"><span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>MCI \_ DGV \_ lista \_ de \_ calidad de audio</span><span class="sxs-lookup"><span data-stu-id="509e7-133"><span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>MCI\_DGV\_LIST\_AUDIO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="509e7-134">El comando debe recuperar los niveles de calidad de audio.</span><span class="sxs-lookup"><span data-stu-id="509e7-134">The command should retrieve audio quality levels.</span></span> <span data-ttu-id="509e7-135">Los niveles devueltos están asociados al algoritmo al que hace referencia el miembro **lpstrAlgorithm** de la estructura identificada por *lpList*.</span><span class="sxs-lookup"><span data-stu-id="509e7-135">The levels returned are associated with the algorithm referenced by the **lpstrAlgorithm** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="509e7-136">Si ese miembro se especifica mediante la cadena "actual", se devuelven las cualidades asociadas al algoritmo actual.</span><span class="sxs-lookup"><span data-stu-id="509e7-136">If that member is specified using the string "current", then the qualities associated with the current algorithm are returned.</span></span>

</dd> <dt>

<span data-ttu-id="509e7-137"><span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>\_secuencia de \_ audio de lista DGV \_ de MCI \_</span><span class="sxs-lookup"><span data-stu-id="509e7-137"><span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>MCI\_DGV\_LIST\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="509e7-138">El comando debe recuperar los nombres de las secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="509e7-138">The command should retrieve names of audio streams.</span></span>

</dd> <dt>

<span data-ttu-id="509e7-139"><span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>lista de DGV de MCI \_ \_ \_ todavía \_ al</span><span class="sxs-lookup"><span data-stu-id="509e7-139"><span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>MCI\_DGV\_LIST\_STILL\_AL</span></span>
</dt> <dd>

<span data-ttu-id="509e7-140">El comando debe recuperar los nombres de los algoritmos de todavía.</span><span class="sxs-lookup"><span data-stu-id="509e7-140">The command should retrieve names of still algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="509e7-141"><span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>calidad de la \_ lista de DGV MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="509e7-141"><span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>MCI\_DGV\_LIST\_STILL\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="509e7-142">El comando debe recuperar los niveles de calidad.</span><span class="sxs-lookup"><span data-stu-id="509e7-142">The command should retrieve quality levels.</span></span> <span data-ttu-id="509e7-143">Los niveles devueltos están asociados al algoritmo al que hace referencia el miembro **lpstrAlgorithm** de la estructura identificada por *lpList*.</span><span class="sxs-lookup"><span data-stu-id="509e7-143">The levels returned are associated with the algorithm referenced by the **lpstrAlgorithm** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="509e7-144">Si ese miembro se especifica mediante la cadena "actual", se devuelven las cualidades asociadas al algoritmo actual.</span><span class="sxs-lookup"><span data-stu-id="509e7-144">If that member is specified using the string "current", then the qualities associated with the current algorithm are returned.</span></span>

</dd> <dt>

<span data-ttu-id="509e7-145"><span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>\_vídeo de \_ vídeo de lista de DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="509e7-145"><span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>MCI\_DGV\_LIST\_VIDEO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="509e7-146">El comando debe recuperar los nombres de los algoritmos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="509e7-146">The command should retrieve names of video algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="509e7-147"><span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>\_calidad de \_ vídeo de lista DGV \_ de MCI \_</span><span class="sxs-lookup"><span data-stu-id="509e7-147"><span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>MCI\_DGV\_LIST\_VIDEO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="509e7-148">El comando debe recuperar los niveles de calidad de vídeo.</span><span class="sxs-lookup"><span data-stu-id="509e7-148">The command should retrieve video quality levels.</span></span> <span data-ttu-id="509e7-149">Los niveles devueltos están asociados al algoritmo al que hace referencia el miembro **lpstrAlgorithm** de la estructura identificada por *lpList*.</span><span class="sxs-lookup"><span data-stu-id="509e7-149">The levels returned are associated with the algorithm referenced by the **lpstrAlgorithm** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="509e7-150">Si ese miembro se especifica mediante la cadena "actual", se devuelven las cualidades asociadas al algoritmo actual.</span><span class="sxs-lookup"><span data-stu-id="509e7-150">If that member is specified using the string "current", then the qualities associated with the current algorithm are returned.</span></span>

</dd> <dt>

<span data-ttu-id="509e7-151"><span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>\_origen de \_ vídeo de lista de DGV de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="509e7-151"><span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>MCI\_DGV\_LIST\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="509e7-152">El comando debe devolver información sobre los orígenes de vídeo.</span><span class="sxs-lookup"><span data-stu-id="509e7-152">The command should return information about the video sources.</span></span> <span data-ttu-id="509e7-153">Cuando se usa con \_ \_ \_ el recuento de lista de DGV de MCI, el comando devuelve el número de orígenes de vídeo.</span><span class="sxs-lookup"><span data-stu-id="509e7-153">When used with MCI\_DGV\_LIST\_COUNT, the command returns the number of video sources.</span></span> <span data-ttu-id="509e7-154">Cuando se usa con \_ \_ \_ el número de lista DGV de MCI, el comando devuelve el tipo de un origen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="509e7-154">When used with MCI\_DGV\_LIST\_NUMBER, the command returns the type of a video source.</span></span> <span data-ttu-id="509e7-155">MCI define los siguientes tipos:</span><span class="sxs-lookup"><span data-stu-id="509e7-155">MCI defines the following types:</span></span>

-   <span data-ttu-id="509e7-156">MCI \_ DGV \_ SETVIDEO \_ src \_ Generic</span><span class="sxs-lookup"><span data-stu-id="509e7-156">MCI\_DGV\_SETVIDEO\_SRC\_GENERIC</span></span>
-   <span data-ttu-id="509e7-157">MCI \_ DGV \_ SETVIDEO \_ src \_ NTSC</span><span class="sxs-lookup"><span data-stu-id="509e7-157">MCI\_DGV\_SETVIDEO\_SRC\_NTSC</span></span>
-   <span data-ttu-id="509e7-158">MCI \_ DGV \_ SETVIDEO \_ src \_ PAL</span><span class="sxs-lookup"><span data-stu-id="509e7-158">MCI\_DGV\_SETVIDEO\_SRC\_PAL</span></span>
-   <span data-ttu-id="509e7-159">MCI \_ DGV \_ SETVIDEO \_ src \_ RGB</span><span class="sxs-lookup"><span data-stu-id="509e7-159">MCI\_DGV\_SETVIDEO\_SRC\_RGB</span></span>
-   <span data-ttu-id="509e7-160">MCI \_ DGV \_ SETVIDEO \_ src \_ SECAM</span><span class="sxs-lookup"><span data-stu-id="509e7-160">MCI\_DGV\_SETVIDEO\_SRC\_SECAM</span></span>
-   <span data-ttu-id="509e7-161">MCI \_ DGV \_ SETVIDEO \_ src \_ Svideo</span><span class="sxs-lookup"><span data-stu-id="509e7-161">MCI\_DGV\_SETVIDEO\_SRC\_SVIDEO</span></span>

<span data-ttu-id="509e7-162">Puede haber más de un origen de cada tipo devuelto.</span><span class="sxs-lookup"><span data-stu-id="509e7-162">There might be more than one source of each type returned.</span></span> <span data-ttu-id="509e7-163">El tipo de origen genérico se usa cuando se permite más de un tipo de señal para dicho conector.</span><span class="sxs-lookup"><span data-stu-id="509e7-163">The generic source type is used when more then one type of signal is allowed for that connector.</span></span>

</dd> <dt>

<span data-ttu-id="509e7-164"><span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>\_secuencia de \_ vídeo de lista de DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="509e7-164"><span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>MCI\_DGV\_LIST\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="509e7-165">El comando debe recuperar los nombres de las secuencias de vídeo.</span><span class="sxs-lookup"><span data-stu-id="509e7-165">The command should retrieve names of video streams.</span></span>

</dd> <dt>

<span data-ttu-id="509e7-166"><span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>\_número de \_ lista de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="509e7-166"><span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>MCI\_DGV\_LIST\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="509e7-167">Se especifica un índice en el miembro **dwNumber** de la estructura identificada por *lpList*.</span><span class="sxs-lookup"><span data-stu-id="509e7-167">An index is specified in the **dwNumber** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="509e7-168">El índice debe ser un entero comprendido entre 1 y el valor devuelto para \_ la \_ marca de recuento de lista MCI DGV \_ .</span><span class="sxs-lookup"><span data-stu-id="509e7-168">The index must be an integer between 1 and the value returned for the MCI\_DGV\_LIST\_COUNT flag.</span></span>

</dd> </dl>

<span data-ttu-id="509e7-169">En el caso de los dispositivos de vídeo digital, *lpList* apunta a una estructura [**parms de MCI \_ DGV \_ List \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="509e7-169">For digital-video devices, *lpList* points to an [**MCI\_DGV\_LIST\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa) structure.</span></span>

<span data-ttu-id="509e7-170">Las siguientes marcas adicionales se aplican al tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="509e7-170">The following additional flags apply to the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="509e7-171"><span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>\_origen de \_ audio de lista de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="509e7-171"><span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>MCI\_VCR\_LIST\_AUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="509e7-172">Enumerar entradas o tipos de audio.</span><span class="sxs-lookup"><span data-stu-id="509e7-172">List audio inputs or types.</span></span>

</dd> <dt>

<span data-ttu-id="509e7-173"><span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>recuento de lista de VCR de MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="509e7-173"><span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>MCI\_VCR\_LIST\_COUNT</span></span>
</dt> <dd>

<span data-ttu-id="509e7-174">Establece el miembro **dwReturn** de la estructura identificada por *lpList* en el número total de entradas de vídeo o audio.</span><span class="sxs-lookup"><span data-stu-id="509e7-174">Sets the **dwReturn** member of the structure identified by *lpList* to the total number of video or audio inputs.</span></span>

</dd> <dt>

<span data-ttu-id="509e7-175"><span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>número de la \_ lista de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="509e7-175"><span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>MCI\_VCR\_LIST\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="509e7-176">Establece el miembro **dwReturn** de la estructura identificada por *lpList* en el tipo de la entrada de vídeo o audio especificada por el miembro **dwNumber** .</span><span class="sxs-lookup"><span data-stu-id="509e7-176">Sets the **dwReturn** member of the structure identified by *lpList* to the type of the video or audio input specified by the **dwNumber** member.</span></span>

</dd> <dt>

<span data-ttu-id="509e7-177"><span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>\_origen de \_ vídeo de lista de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="509e7-177"><span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>MCI\_VCR\_LIST\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="509e7-178">Enumerar entradas o tipos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="509e7-178">List video inputs or types.</span></span>

</dd> </dl>

<span data-ttu-id="509e7-179">En el caso de los dispositivos VCR, *lpList* apunta a una estructura de [**\_ \_ \_ parms de VCR de MCI**](mci-vcr-list-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="509e7-179">For VCR devices, *lpList* points to an [**MCI\_VCR\_LIST\_PARMS**](mci-vcr-list-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="509e7-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="509e7-180">Requirements</span></span>



| <span data-ttu-id="509e7-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="509e7-181">Requirement</span></span> | <span data-ttu-id="509e7-182">Value</span><span class="sxs-lookup"><span data-stu-id="509e7-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="509e7-183">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="509e7-183">Minimum supported client</span></span><br/> | <span data-ttu-id="509e7-184">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="509e7-184">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="509e7-185">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="509e7-185">Minimum supported server</span></span><br/> | <span data-ttu-id="509e7-186">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="509e7-186">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="509e7-187">Encabezado</span><span class="sxs-lookup"><span data-stu-id="509e7-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="509e7-188"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="509e7-188"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="509e7-189">Vea también</span><span class="sxs-lookup"><span data-stu-id="509e7-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="509e7-190">MCI</span><span class="sxs-lookup"><span data-stu-id="509e7-190">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="509e7-191">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="509e7-191">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

