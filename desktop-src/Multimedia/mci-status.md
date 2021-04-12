---
title: Comando MCI_STATUS (mmsystem. h)
description: El \_ comando MCI status recupera información acerca de un dispositivo MCI. Todos los dispositivos reconocen este comando. La información se devuelve en el miembro dwReturn de la estructura identificada por el parámetro lpStatus.
ms.assetid: d1c3dff9-c66f-4525-aac1-4a15b43083e7
keywords:
- Comando de MCI_STATUS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_STATUS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86553ac759a362c1ea4abb53a47d0e9376cbc526
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2021
ms.locfileid: "104361737"
---
# <a name="mci_status-command"></a><span data-ttu-id="38c6a-106">Comando de estado de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-106">MCI\_STATUS command</span></span>

> [!NOTE]
> <span data-ttu-id="38c6a-107">Comunicación sin polarización: Microsoft admite un entorno diverso y de inclusión.</span><span class="sxs-lookup"><span data-stu-id="38c6a-107">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="38c6a-108">Dentro de este documento, hay referencias a la palabra ' Slave '.</span><span class="sxs-lookup"><span data-stu-id="38c6a-108">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="38c6a-109">La guía de estilo de Microsoft [para Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) lo reconoce como una palabra de exclusión.</span><span class="sxs-lookup"><span data-stu-id="38c6a-109">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="38c6a-110">Este texto se usa tal como está actualmente el texto que se usa en los comandos.</span><span class="sxs-lookup"><span data-stu-id="38c6a-110">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="38c6a-111">Para mantener la coherencia, este documento contiene esta palabra.</span><span class="sxs-lookup"><span data-stu-id="38c6a-111">For consistency, this document contains this word.</span></span> <span data-ttu-id="38c6a-112">Cuando se modifique esta palabra en los comandos, se corregirá este documento para que esté alineado.</span><span class="sxs-lookup"><span data-stu-id="38c6a-112">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="38c6a-113">El \_ comando MCI status recupera información acerca de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="38c6a-113">The MCI\_STATUS command retrieves information about an MCI device.</span></span> <span data-ttu-id="38c6a-114">Todos los dispositivos reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="38c6a-114">All devices recognize this command.</span></span> <span data-ttu-id="38c6a-115">La información se devuelve en el miembro **dwReturn** de la estructura identificada por el parámetro *lpStatus* .</span><span class="sxs-lookup"><span data-stu-id="38c6a-115">Information is returned in the **dwReturn** member of the structure identified by the *lpStatus* parameter.</span></span>

<span data-ttu-id="38c6a-116">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="38c6a-116">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STATUS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_STATUS_PARMS) lpStatus
);
```



## <a name="parameters"></a><span data-ttu-id="38c6a-117">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38c6a-117">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38c6a-118"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="38c6a-118"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-119">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="38c6a-119">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-120"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="38c6a-120"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-121">MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="38c6a-121">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="38c6a-122">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="38c6a-122">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-123"><span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*lpStatus*</span><span class="sxs-lookup"><span data-stu-id="38c6a-123"><span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*lpStatus*</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-124">Puntero a una [**estructura \_ \_ parms de estado de MCI**](mci-status-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="38c6a-124">Pointer to an [**MCI\_STATUS\_PARMS**](mci-status-parms.md) structure.</span></span> <span data-ttu-id="38c6a-125">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="38c6a-125">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38c6a-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38c6a-126">Return Value</span></span>

<span data-ttu-id="38c6a-127">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="38c6a-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="38c6a-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38c6a-128">Remarks</span></span>

<span data-ttu-id="38c6a-129">Se aplican las siguientes marcas estándar y específicas del comando adicionales a todos los dispositivos que admiten el estado de MCI \_ :</span><span class="sxs-lookup"><span data-stu-id="38c6a-129">The following additional standard and command-specific flags apply to all devices supporting MCI\_STATUS:</span></span>

<dl> <dt>

<span data-ttu-id="38c6a-130"><span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>\_elemento de estado de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-130"><span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>MCI\_STATUS\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-131">Especifica que el miembro **dwItem** de la estructura identificada por *lpStatus* contiene una constante que especifica qué elemento de estado se debe obtener.</span><span class="sxs-lookup"><span data-stu-id="38c6a-131">Specifies that the **dwItem** member of the structure identified by *lpStatus* contains a constant specifying which status item to obtain.</span></span> <span data-ttu-id="38c6a-132">Las constantes siguientes definen qué elemento de estado se va a devolver en el miembro **dwReturn** de la estructura:</span><span class="sxs-lookup"><span data-stu-id="38c6a-132">The following constants define which status item to return in the **dwReturn** member of the structure:</span></span>

<span data-ttu-id="38c6a-133">\_ \_ pista actual de estado de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-133">MCI\_STATUS\_CURRENT\_TRACK</span></span>

<span data-ttu-id="38c6a-134">El miembro **dwReturn** se establece en el número de seguimiento actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-134">The **dwReturn** member is set to the current track number.</span></span> <span data-ttu-id="38c6a-135">MCI usa números de pista continuos.</span><span class="sxs-lookup"><span data-stu-id="38c6a-135">MCI uses continuous track numbers.</span></span>

<span data-ttu-id="38c6a-136">\_longitud de estado de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-136">MCI\_STATUS\_LENGTH</span></span>

<span data-ttu-id="38c6a-137">El miembro **dwReturn** se establece en la longitud total del medio.</span><span class="sxs-lookup"><span data-stu-id="38c6a-137">The **dwReturn** member is set to the total media length.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-138"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>\_modo de estado de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-138"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MCI\_STATUS\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-139">El miembro **dwReturn** se establece en el modo actual del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="38c6a-139">The **dwReturn** member is set to the current mode of the device.</span></span> <span data-ttu-id="38c6a-140">Entre los modos se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="38c6a-140">The modes include the following:</span></span>

-   <span data-ttu-id="38c6a-141">\_modo MCI \_ no \_ listo</span><span class="sxs-lookup"><span data-stu-id="38c6a-141">MCI\_MODE\_NOT\_READY</span></span>
-   <span data-ttu-id="38c6a-142">\_pausar modo MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-142">MCI\_MODE\_PAUSE</span></span>
-   <span data-ttu-id="38c6a-143">\_reproducción en modo MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-143">MCI\_MODE\_PLAY</span></span>
-   <span data-ttu-id="38c6a-144">\_detención del modo MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-144">MCI\_MODE\_STOP</span></span>
-   <span data-ttu-id="38c6a-145">\_modo MCI \_ abierto</span><span class="sxs-lookup"><span data-stu-id="38c6a-145">MCI\_MODE\_OPEN</span></span>
-   <span data-ttu-id="38c6a-146">\_registro en modo MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-146">MCI\_MODE\_RECORD</span></span>
-   <span data-ttu-id="38c6a-147">\_búsqueda en modo MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-147">MCI\_MODE\_SEEK</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-148"><span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>\_ \_ número \_ de seguimiento de estado de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-148"><span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>MCI\_STATUS\_NUMBER\_OF\_TRACKS</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-149">El miembro **dwReturn** se establece en el número total de pistas que se van a reproducir.</span><span class="sxs-lookup"><span data-stu-id="38c6a-149">The **dwReturn** member is set to the total number of playable tracks.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-150"><span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>\_posición de estado de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-150"><span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>MCI\_STATUS\_POSITION</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-151">El miembro **dwReturn** se establece en la posición actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-151">The **dwReturn** member is set to the current position.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-152"><span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>Estado de MCI \_ \_ preparado</span><span class="sxs-lookup"><span data-stu-id="38c6a-152"><span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>MCI\_STATUS\_READY</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-153">El miembro **dwReturn** se establece en **true** si el dispositivo está listo; en caso contrario, se establece en **false** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-153">The **dwReturn** member is set to **TRUE** if the device is ready; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-154"><span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>\_formato de \_ hora de estado de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-154"><span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>MCI\_STATUS\_TIME\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-155">El miembro **dwReturn** se establece en el formato de hora actual del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="38c6a-155">The **dwReturn** member is set to the current time format of the device.</span></span> <span data-ttu-id="38c6a-156">Los formatos de hora incluyen:</span><span class="sxs-lookup"><span data-stu-id="38c6a-156">The time formats include:</span></span>

-   <span data-ttu-id="38c6a-157">\_bytes de formato de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-157">MCI\_FORMAT\_BYTES</span></span>
-   <span data-ttu-id="38c6a-158">\_marcos de formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-158">MCI\_FORMAT\_FRAMES</span></span>
-   <span data-ttu-id="38c6a-159">\_formato MCI \_ HMS</span><span class="sxs-lookup"><span data-stu-id="38c6a-159">MCI\_FORMAT\_HMS</span></span>
-   <span data-ttu-id="38c6a-160">formato MCI en \_ \_ milisegundos</span><span class="sxs-lookup"><span data-stu-id="38c6a-160">MCI\_FORMAT\_MILLISECONDS</span></span>
-   <span data-ttu-id="38c6a-161">\_formato MCI \_ MSF</span><span class="sxs-lookup"><span data-stu-id="38c6a-161">MCI\_FORMAT\_MSF</span></span>
-   <span data-ttu-id="38c6a-162">\_ejemplos de formato de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-162">MCI\_FORMAT\_SAMPLES</span></span>
-   <span data-ttu-id="38c6a-163">\_formato MCI \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="38c6a-163">MCI\_FORMAT\_TMSF</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-164"><span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>\_Inicio de estado de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-164"><span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>MCI\_STATUS\_START</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-165">Obtiene la posición inicial del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="38c6a-165">Obtains the starting position of the media.</span></span> <span data-ttu-id="38c6a-166">Para obtener la posición inicial, combine esta marca con el \_ elemento de estado \_ de MCI y establezca el miembro **dwItem** de la estructura identificada por *lpStatus* en la posición de estado de MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="38c6a-166">To get the starting position, combine this flag with MCI\_STATUS\_ITEM and set the **dwItem** member of the structure identified by *lpStatus* to MCI\_STATUS\_POSITION.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-167"><span id="MCI_TRACK"></span><span id="mci_track"></span>pista de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-167"><span id="MCI_TRACK"></span><span id="mci_track"></span>MCI\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-168">Indica que un parámetro de seguimiento de estado se incluye en el miembro **dwTrack** de la estructura identificada por *lpStatus*.</span><span class="sxs-lookup"><span data-stu-id="38c6a-168">Indicates a status track parameter is included in the **dwTrack** member of the structure identified by *lpStatus*.</span></span> <span data-ttu-id="38c6a-169">Debe usar esta marca con las constantes de \_ posición de estado de MCI o de \_ longitud de estado de MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="38c6a-169">You must use this flag with the MCI\_STATUS\_POSITION or MCI\_STATUS\_LENGTH constants.</span></span> <span data-ttu-id="38c6a-170">Cuando se usa con \_ la \_ posición de estado de MCI, MCI \_ Track obtiene la posición inicial de la pista especificada. Cuando se usa con \_ la \_ longitud del estado de MCI, MCI \_ Track obtiene la longitud de la pista especificada. MCI usa números de pista continuos.</span><span class="sxs-lookup"><span data-stu-id="38c6a-170">When used with MCI\_STATUS\_POSITION, MCI\_TRACK obtains the starting position of the specified track. When used with MCI\_STATUS\_LENGTH, MCI\_TRACK obtains the length of the specified track. MCI uses continuous track numbers.</span></span>

</dd> </dl>

<span data-ttu-id="38c6a-171">Se usan las siguientes marcas adicionales con el tipo de dispositivo **cdaudio** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-171">The following additional flags are used with the **cdaudio** device type.</span></span> <span data-ttu-id="38c6a-172">Estas constantes se utilizan en el miembro **dwItem** de la estructura a la que apunta el parámetro *lpStatus* cuando \_ \_ se especifica el elemento de estado de MCI para el parámetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="38c6a-172">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="38c6a-173"><span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>\_pista de \_ tipo de estado \_ \_ de MCI CDA</span><span class="sxs-lookup"><span data-stu-id="38c6a-173"><span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>MCI\_CDA\_STATUS\_TYPE\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-174">El miembro **dwReturn** se establece en uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="38c6a-174">The **dwReturn** member is set to one of the following values:</span></span>

-   <span data-ttu-id="38c6a-175">\_audio de \_ rastreo de de MCI CDA \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-175">MCI\_CDA\_TRACK\_AUDIO</span></span>
-   <span data-ttu-id="38c6a-176">pista de MCI \_ CDA \_ \_ otro</span><span class="sxs-lookup"><span data-stu-id="38c6a-176">MCI\_CDA\_TRACK\_OTHER</span></span>

<span data-ttu-id="38c6a-177">Para usar esta marca, \_ se debe establecer la marca de pista de MCI y el miembro **dwTrack** de la estructura identificada por *lpStatus* debe contener un número de seguimiento válido.</span><span class="sxs-lookup"><span data-stu-id="38c6a-177">To use this flag, the MCI\_TRACK flag must be set, and the **dwTrack** member of the structure identified by *lpStatus* must contain a valid track number.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-178"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>medios de estado de MCI \_ \_ \_ presentes</span><span class="sxs-lookup"><span data-stu-id="38c6a-178"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-179">El miembro **dwReturn** se establece en **true** si el medio se inserta en el dispositivo; en caso contrario, se establece en **false** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-179">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="38c6a-180">Con el tipo de dispositivo **DigitalVideo** se usan las siguientes marcas adicionales:</span><span class="sxs-lookup"><span data-stu-id="38c6a-180">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="38c6a-181"><span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>\_Estado de DGV de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-181"><span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>MCI\_DGV\_STATUS\_DISKSPACE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-182">El miembro **lpstrDrive** de la estructura identificada por *lpStatus* especifica una unidad de disco o, en algunas implementaciones, una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="38c6a-182">The **lpstrDrive** member of the structure identified by *lpStatus* specifies a disk drive or, in some implementations, a path.</span></span> <span data-ttu-id="38c6a-183">El \_ comando MCI status devuelve la cantidad aproximada de espacio en disco que podría obtener el comando de [ \_ reserva de MCI](mci-reserve.md) en el miembro **dwReturn** de la estructura identificada por *lpStatus*.</span><span class="sxs-lookup"><span data-stu-id="38c6a-183">The MCI\_STATUS command returns the approximate amount of disk space that could be obtained by the [MCI\_RESERVE](mci-reserve.md) command in the **dwReturn** member of the structure identified by *lpStatus*.</span></span> <span data-ttu-id="38c6a-184">El espacio en disco se mide en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-184">The disk space is measured in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-185"><span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>\_entrada de \_ Estado de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-185"><span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>MCI\_DGV\_STATUS\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-186">La constante especificada por el miembro **dwItem** de la estructura identificada por *lpStatus* se aplica a la entrada.</span><span class="sxs-lookup"><span data-stu-id="38c6a-186">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the input.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-187"><span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>Estado de DGV de MCI \_ \_ \_ restante</span><span class="sxs-lookup"><span data-stu-id="38c6a-187"><span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>MCI\_DGV\_STATUS\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-188">La constante especificada por el miembro **dwItem** de la estructura identificada por *lpStatus* se aplica al canal de audio izquierdo.</span><span class="sxs-lookup"><span data-stu-id="38c6a-188">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the left audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-189"><span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>Estado de DGV de MCI \_ \_ \_ nominal</span><span class="sxs-lookup"><span data-stu-id="38c6a-189"><span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>MCI\_DGV\_STATUS\_NOMINAL</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-190">La constante especificada por el miembro **dwItem** de la estructura identificada por *lpStatus* solicita el valor nominal en lugar del valor actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-190">The constant specified by the **dwItem** member of the structure identified by *lpStatus* requests the nominal value rather than the current value.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-191"><span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>\_salida de \_ Estado de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-191"><span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>MCI\_DGV\_STATUS\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-192">La constante especificada por el miembro **dwItem** de la estructura identificada por *lpStatus* se aplica a la salida.</span><span class="sxs-lookup"><span data-stu-id="38c6a-192">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the output.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-193"><span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>registro de estado de MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-193"><span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>MCI\_DGV\_STATUS\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-194">La velocidad de fotogramas devuelta para la \_ \_ marca de velocidad de fotogramas de estado de MCI DGV \_ \_ es la velocidad usada para la compresión.</span><span class="sxs-lookup"><span data-stu-id="38c6a-194">The frame rate returned for the MCI\_DGV\_STATUS\_FRAME\_RATE flag is the rate used for compression.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-195"><span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>\_referencia de \_ Estado de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-195"><span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>MCI\_DGV\_STATUS\_REFERENCE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-196">El miembro **dwReturn** de la estructura identificada por *lpStatus* devuelve la imagen de fotograma clave más cercana que precede al marco especificado en el miembro **dwReference** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-196">The **dwReturn** member of the structure identified by *lpStatus* returns the nearest key-frame image that precedes the frame specified in the **dwReference** member.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-197"><span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>\_derecho de \_ Estado de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-197"><span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>MCI\_DGV\_STATUS\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-198">La constante especificada por el miembro **dwItem** de la estructura identificada por *lpStatus* se aplica al canal de audio derecho.</span><span class="sxs-lookup"><span data-stu-id="38c6a-198">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the right audio channel.</span></span>

</dd> </dl>

<span data-ttu-id="38c6a-199">Las constantes siguientes se usan con el tipo de dispositivo **DigitalVideo** en el miembro **dwItem** de la estructura a la que apunta el parámetro *lpStatus* cuando \_ \_ se especifica el elemento de estado de MCI para el parámetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="38c6a-199">The following constants are used with the **digitalvideo** device type in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="38c6a-200"><span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>dessaltos de audio de estado de MCI \_ AVI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-200"><span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>MCI\_AVI\_STATUS\_AUDIO\_BREAKS</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-201">El miembro **dwReturn** devuelve el número de veces que se ha interrumpido la parte de audio de la última secuencia AVI.</span><span class="sxs-lookup"><span data-stu-id="38c6a-201">The **dwReturn** member returns the number of times the audio portion of the last AVI sequence broke up.</span></span> <span data-ttu-id="38c6a-202">El sistema cuenta una interrupción de audio cada vez que intenta escribir datos de audio en el controlador de dispositivo y detecta que el controlador ya ha reproducido todos los datos disponibles.</span><span class="sxs-lookup"><span data-stu-id="38c6a-202">The system counts an audio break whenever it attempts to write audio data to the device driver and discovers that the driver has already played all of the available data.</span></span> <span data-ttu-id="38c6a-203">Esta marca solo se reconoce en el controlador de vídeo digital MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="38c6a-203">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-204"><span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>\_tramas de estado de MCI AVI \_ \_ \_ omitidas</span><span class="sxs-lookup"><span data-stu-id="38c6a-204"><span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>MCI\_AVI\_STATUS\_FRAMES\_SKIPPED</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-205">El miembro **dwReturn** devuelve el número de fotogramas que no se dibujaron cuando se reprodujo la última secuencia AVI.</span><span class="sxs-lookup"><span data-stu-id="38c6a-205">The **dwReturn** member returns the number of frames that were not drawn when the last AVI sequence was played.</span></span> <span data-ttu-id="38c6a-206">Esta marca solo se reconoce en el controlador de vídeo digital MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="38c6a-206">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-207"><span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>\_velocidad de \_ \_ última \_ reproducción \_ de estado de MCI AVI</span><span class="sxs-lookup"><span data-stu-id="38c6a-207"><span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>MCI\_AVI\_STATUS\_LAST\_PLAY\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-208">El miembro **dwReturn** devuelve un valor que representa la proximidad del tiempo de reproducción real de la última secuencia de AVI con el tiempo de reproducción del destino.</span><span class="sxs-lookup"><span data-stu-id="38c6a-208">The **dwReturn** member returns a value representing how closely the actual playing time of the last AVI sequence matched the target playing time.</span></span> <span data-ttu-id="38c6a-209">El valor 1000 indica que la hora de destino y la hora real eran iguales.</span><span class="sxs-lookup"><span data-stu-id="38c6a-209">The value 1000 indicates that the target time and the actual time were the same.</span></span> <span data-ttu-id="38c6a-210">Un valor de 2000, por ejemplo, indicaría que la secuencia AVI tardó dos veces más en ejecutarse que debiera.</span><span class="sxs-lookup"><span data-stu-id="38c6a-210">A value of 2000, for example, would indicate that the AVI sequence took twice as long to play as it should have.</span></span> <span data-ttu-id="38c6a-211">Esta marca solo se reconoce en el controlador de vídeo digital MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="38c6a-211">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-212"><span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>\_audio de \_ Estado de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-212"><span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>MCI\_DGV\_STATUS\_AUDIO</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-213">El miembro **dwReturn** devuelve MCI \_ on o MCI \_ OFF según la opción de audio Set MCI más reciente \_ \_ para el comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="38c6a-213">The **dwReturn** member returns MCI\_ON or MCI\_OFF depending on the most recent MCI\_SET\_AUDIO option for the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="38c6a-214">Devuelve MCI \_ en caso de que uno o ambos altavoces estén habilitados y MCI esté \_ desactivado.</span><span class="sxs-lookup"><span data-stu-id="38c6a-214">It returns MCI\_ON if either or both speakers are enabled, and MCI\_OFF otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-215"><span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>\_entrada de \_ audio de estado DGV \_ de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-215"><span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>MCI\_DGV\_STATUS\_AUDIO\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-216">El miembro **dwReturn** devuelve el nivel de audio instantáneo aproximado de la señal de audio analógico.</span><span class="sxs-lookup"><span data-stu-id="38c6a-216">The **dwReturn** member returns the approximate instantaneous audio level of the analog audio signal.</span></span> <span data-ttu-id="38c6a-217">Un valor mayor que 1000 implica que hay distorsión de recorte.</span><span class="sxs-lookup"><span data-stu-id="38c6a-217">A value greater than 1000 implies there is clipping distortion.</span></span> <span data-ttu-id="38c6a-218">Algunos dispositivos pueden determinar este valor solo al grabar audio.</span><span class="sxs-lookup"><span data-stu-id="38c6a-218">Some devices can determine this value only while recording audio.</span></span> <span data-ttu-id="38c6a-219">Este valor de estado no tiene asociado ningún comando MCI **\_ set** o [ \_ SETAUDIO MCI](mci-setaudio.md) .</span><span class="sxs-lookup"><span data-stu-id="38c6a-219">This status value has no associated **MCI\_SET** or [MCI\_SETAUDIO](mci-setaudio.md) command.</span></span> <span data-ttu-id="38c6a-220">Este valor está relacionado con el nivel de estado de onda MCI de comando de audio de onda, pero normalizado de forma diferente a este \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="38c6a-220">This value is related to, but normalized differently from, the waveform-audio command MCI\_WAVE\_STATUS\_LEVEL.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-221"><span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>\_registro de \_ audio de estado de DGV de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-221"><span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>MCI\_DGV\_STATUS\_AUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-222">El miembro **dwReturn** devuelve MCI \_ on o MCI \_ OFF para reflejar el estado establecido por la \_ marca MCI DGV \_ SETAUDIO \_ Record del comando **MCI \_ SETAUDIO** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-222">The **dwReturn** member returns MCI\_ON or MCI\_OFF reflecting the state set by the MCI\_DGV\_SETAUDIO\_RECORD flag of the **MCI\_SETAUDIO** command.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-223"><span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>\_origen de \_ audio de estado de DGV de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-223"><span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>MCI\_DGV\_STATUS\_AUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-224">El miembro **dwReturn** devuelve el origen del digitalizador de audio actual:</span><span class="sxs-lookup"><span data-stu-id="38c6a-224">The **dwReturn** member returns the current audio digitizer source:</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-225"><span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>media de DGV de MCI \_ \_ SETAUDIO \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-225"><span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>MCI\_DGV\_SETAUDIO\_AVERAGE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-226">Especifica el promedio de los canales de audio izquierdo y derecho.</span><span class="sxs-lookup"><span data-stu-id="38c6a-226">Specifies the average of the left and right audio channels.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-227"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>\_DGV MCI \_ SETAUDIO \_ izquierda</span><span class="sxs-lookup"><span data-stu-id="38c6a-227"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI\_DGV\_SETAUDIO\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-228">Especifica el canal de audio izquierdo.</span><span class="sxs-lookup"><span data-stu-id="38c6a-228">Specifies the left audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-229"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>\_DGV MCI \_ SETAUDIO \_ derecha</span><span class="sxs-lookup"><span data-stu-id="38c6a-229"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI\_DGV\_SETAUDIO\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-230">Especifica el canal de audio derecho.</span><span class="sxs-lookup"><span data-stu-id="38c6a-230">Specifies the right audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-231"><span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>MCI \_ DGV \_ SETAUDIO \_ estéreo</span><span class="sxs-lookup"><span data-stu-id="38c6a-231"><span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>MCI\_DGV\_SETAUDIO\_STEREO</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-232">Especifica estéreo.</span><span class="sxs-lookup"><span data-stu-id="38c6a-232">Specifies stereo.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-233"><span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>\_secuencia de \_ audio de estado DGV \_ de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-233"><span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>MCI\_DGV\_STATUS\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-234">El miembro **dwReturn** devuelve el número de secuencia de audio actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-234">The **dwReturn** member returns the current audio-stream number.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-235"><span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>MCI \_ DGV \_ status \_ AVGBYTESPERSEC</span><span class="sxs-lookup"><span data-stu-id="38c6a-235"><span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>MCI\_DGV\_STATUS\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-236">El miembro **dwReturn** devuelve el número promedio de bytes por segundo que se usan para la grabación.</span><span class="sxs-lookup"><span data-stu-id="38c6a-236">The **dwReturn** member returns the average number of bytes per second used for recording.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-237"><span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>\_ \_ graves estado de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-237"><span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>MCI\_DGV\_STATUS\_BASS</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-238">El miembro **dwReturn** devuelve el nivel de graves de audio actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-238">The **dwReturn** member returns the current audio bass level.</span></span> <span data-ttu-id="38c6a-239">Use MCI \_ DGV \_ status \_ nominal con esta marca para obtener el nivel nominal.</span><span class="sxs-lookup"><span data-stu-id="38c6a-239">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-240"><span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>Estado de DGV de MCI \_ \_ \_ BITSPERPEL</span><span class="sxs-lookup"><span data-stu-id="38c6a-240"><span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>MCI\_DGV\_STATUS\_BITSPERPEL</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-241">El miembro **dwReturn** devuelve el número de bits por píxel que se usa para guardar los datos capturados o grabados.</span><span class="sxs-lookup"><span data-stu-id="38c6a-241">The **dwReturn** member returns the number of bits per pixel used for saving captured or recorded data.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-242"><span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>MCI \_ DGV \_ status \_ BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="38c6a-242"><span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>MCI\_DGV\_STATUS\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-243">El miembro **dwReturn** devuelve el número de bits por muestra que el dispositivo usa para la grabación.</span><span class="sxs-lookup"><span data-stu-id="38c6a-243">The **dwReturn** member returns the number of bits per sample the device uses for recording.</span></span> <span data-ttu-id="38c6a-244">Esto solo se aplica a los dispositivos que admiten el formato PCM.</span><span class="sxs-lookup"><span data-stu-id="38c6a-244">This applies only to devices supporting the PCM format.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-245"><span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>MCI \_ DGV \_ status \_ BLOCKALIGN</span><span class="sxs-lookup"><span data-stu-id="38c6a-245"><span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>MCI\_DGV\_STATUS\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-246">El miembro **dwReturn** devuelve la alineación de los bloques de datos en relación con el inicio de la onda de entrada.</span><span class="sxs-lookup"><span data-stu-id="38c6a-246">The **dwReturn** member returns the alignment of data blocks relative to the start of the input waveform.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-247"><span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>\_brillo de \_ Estado de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-247"><span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>MCI\_DGV\_STATUS\_BRIGHTNESS</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-248">El miembro **dwReturn** devuelve el nivel de brillo del vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-248">The **dwReturn** member returns the current video brightness level.</span></span> <span data-ttu-id="38c6a-249">Use MCI \_ DGV \_ status \_ nominal con esta marca para obtener el nivel nominal.</span><span class="sxs-lookup"><span data-stu-id="38c6a-249">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-250"><span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>\_color de \_ Estado de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-250"><span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>MCI\_DGV\_STATUS\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-251">El miembro **dwReturn** devuelve el nivel de color actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-251">The **dwReturn** member returns the current color level.</span></span> <span data-ttu-id="38c6a-252">Use MCI \_ DGV \_ status \_ nominal con esta marca para obtener el nivel nominal.</span><span class="sxs-lookup"><span data-stu-id="38c6a-252">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-253"><span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>\_contraste de \_ Estado de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-253"><span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>MCI\_DGV\_STATUS\_CONTRAST</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-254">El miembro **dwReturn** devuelve el nivel de contraste actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-254">The **dwReturn** member returns the current contrast level.</span></span> <span data-ttu-id="38c6a-255">Use MCI \_ DGV \_ status \_ nominal con esta marca para obtener el nivel nominal.</span><span class="sxs-lookup"><span data-stu-id="38c6a-255">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-256"><span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>MCI \_ DGV \_ status \_ FILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="38c6a-256"><span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>MCI\_DGV\_STATUS\_FILEFORMAT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-257">El miembro **dwReturn** devuelve el formato de archivo actual para grabar o guardar.</span><span class="sxs-lookup"><span data-stu-id="38c6a-257">The **dwReturn** member returns the current file format for recording or saving.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-258"><span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>\_modo de \_ archivo de estado de DGV de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-258"><span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>MCI\_DGV\_STATUS\_FILE\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-259">El miembro **dwReturn** devuelve el estado de la operación de archivo:</span><span class="sxs-lookup"><span data-stu-id="38c6a-259">The **dwReturn** member returns the state of the file operation:</span></span>

<span data-ttu-id="38c6a-260">\_edición del \_ modo de archivo MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-260">MCI\_DGV\_FILE\_MODE\_EDITING</span></span>

<span data-ttu-id="38c6a-261">Se devuelve durante las operaciones de cortar, copiar, eliminar, pegar y deshacer.</span><span class="sxs-lookup"><span data-stu-id="38c6a-261">Returned during cut, copy, delete, paste, and undo operations.</span></span>

<span data-ttu-id="38c6a-262">\_modo de archivo DGV de MCI \_ \_ \_ inactivo</span><span class="sxs-lookup"><span data-stu-id="38c6a-262">MCI\_DGV\_FILE\_MODE\_IDLE</span></span>

<span data-ttu-id="38c6a-263">Se devuelve cuando el archivo está listo para la siguiente operación.</span><span class="sxs-lookup"><span data-stu-id="38c6a-263">Returned when the file is ready for the next operation.</span></span>

<span data-ttu-id="38c6a-264">\_carga del \_ modo de archivo MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-264">MCI\_DGV\_FILE\_MODE\_LOADING</span></span>

<span data-ttu-id="38c6a-265">Se devuelve mientras se carga el archivo.</span><span class="sxs-lookup"><span data-stu-id="38c6a-265">Returned while the file is being loaded.</span></span>

<span data-ttu-id="38c6a-266">\_guardado del \_ modo de archivo MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-266">MCI\_DGV\_FILE\_MODE\_SAVING</span></span>

<span data-ttu-id="38c6a-267">Se devuelve mientras se guarda el archivo.</span><span class="sxs-lookup"><span data-stu-id="38c6a-267">Returned while the file is being saved.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-268"><span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>\_ \_ \_ finalización del archivo de estado de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-268"><span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>MCI\_DGV\_STATUS\_FILE\_COMPLETION</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-269">El miembro **dwReturn** devuelve el porcentaje estimado de progreso de una operación de carga, guardado, captura, cortar, copiar, eliminar, pegar o deshacer.</span><span class="sxs-lookup"><span data-stu-id="38c6a-269">The **dwReturn** member returns the estimated percentage a load, save, capture, cut, copy, delete, paste, or undo operation has progressed.</span></span> <span data-ttu-id="38c6a-270">(Las aplicaciones pueden utilizar esto para proporcionar un indicador visual de progreso). Esta marca no es compatible con todos los dispositivos de vídeo digital.</span><span class="sxs-lookup"><span data-stu-id="38c6a-270">(Applications can use this to provide a visual indicator of progress.) This flag is not supported by all digital-video devices.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-271"><span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>Estado de DGV de MCI \_ \_ \_ hacia delante</span><span class="sxs-lookup"><span data-stu-id="38c6a-271"><span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>MCI\_DGV\_STATUS\_FORWARD</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-272">El miembro **dwReturn** devuelve **true** si la dirección del dispositivo es reenviar o si el dispositivo no se está reproduciendo.</span><span class="sxs-lookup"><span data-stu-id="38c6a-272">The **dwReturn** member returns **TRUE** if the device direction is forward or the device is not playing.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-273"><span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>\_velocidad de \_ \_ fotogramas de estado de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-273"><span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>MCI\_DGV\_STATUS\_FRAME\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-274">El miembro **dwReturn** debe usarse con el \_ Estado de DGV de MCI \_ \_ nominal, el registro de estado de \_ DGV MCI \_ \_ o ambos.</span><span class="sxs-lookup"><span data-stu-id="38c6a-274">The **dwReturn** member must be used with MCI\_DGV\_STATUS\_NOMINAL, MCI\_DGV\_STATUS\_RECORD, or both.</span></span> <span data-ttu-id="38c6a-275">Cuando se usa con \_ el registro de estado de DGV de MCI \_ \_ , se devuelve la velocidad de fotogramas actual utilizada para la grabación.</span><span class="sxs-lookup"><span data-stu-id="38c6a-275">When used with MCI\_DGV\_STATUS\_RECORD, the current frame rate used for recording is returned.</span></span> <span data-ttu-id="38c6a-276">Cuando se usa con el estado de MCI DGV status \_ \_ \_ y MCI \_ DGV \_ status \_ , la velocidad de fotogramas nominal asociada a la señal de vídeo de entrada se devuelve.</span><span class="sxs-lookup"><span data-stu-id="38c6a-276">When used with both MCI\_DGV\_STATUS\_RECORD and MCI\_DGV\_STATUS\_NOMINAL, the nominal frame rate associated with the input video signal is returned.</span></span> <span data-ttu-id="38c6a-277">Cuando se usa con el \_ Estado DGV de MCI \_ \_ , se devuelve la velocidad de fotogramas nominal asociada al archivo.</span><span class="sxs-lookup"><span data-stu-id="38c6a-277">When used with MCI\_DGV\_STATUS\_NOMINAL, the nominal frame rate associated with the file is returned.</span></span> <span data-ttu-id="38c6a-278">En todos los casos, las unidades están en fotogramas por segundo multiplicada por 1000.</span><span class="sxs-lookup"><span data-stu-id="38c6a-278">In all cases the units are in frames per second multiplied by 1000.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-279"><span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>\_gamma de \_ Estado de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-279"><span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>MCI\_DGV\_STATUS\_GAMMA</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-280">El miembro **dwReturn** devuelve el valor gamma actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-280">The **dwReturn** member returns the current gamma value.</span></span> <span data-ttu-id="38c6a-281">Use MCI \_ DGV \_ status \_ nominal con esta marca para obtener el nivel nominal.</span><span class="sxs-lookup"><span data-stu-id="38c6a-281">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-282"><span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>MCI \_ DGV \_ status \_ HPAL</span><span class="sxs-lookup"><span data-stu-id="38c6a-282"><span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>MCI\_DGV\_STATUS\_HPAL</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-283">El miembro **dwReturn** devuelve el valor decimal ASCII para el identificador de la paleta actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-283">The **dwReturn** member returns the ASCII decimal value for the current palette handle.</span></span> <span data-ttu-id="38c6a-284">El identificador está contenido en la palabra de orden inferior del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="38c6a-284">The handle is contained in the low-order word of the returned value.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-285"><span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>\_DGV de \_ estado \_ hWnd de MCI</span><span class="sxs-lookup"><span data-stu-id="38c6a-285"><span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>MCI\_DGV\_STATUS\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-286">El miembro **dwReturn** devuelve el valor decimal ASCII para el identificador de ventana explícito o predeterminado asociado a esta instancia de controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="38c6a-286">The **dwReturn** member returns the ASCII decimal value for the current explicit or default window handle associated with this device driver instance.</span></span> <span data-ttu-id="38c6a-287">El identificador está contenido en la palabra de orden inferior del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="38c6a-287">The handle is contained in the low-order word of the returned value.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-288"><span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>\_color de \_ clave de estado de DGV de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-288"><span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>MCI\_DGV\_STATUS\_KEY\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-289">El miembro **dwReturn** devuelve el valor de color de la clave actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-289">The **dwReturn** member returns the current key-color value.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-290"><span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>\_Índice de \_ clave de estado de DGV de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-290"><span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>MCI\_DGV\_STATUS\_KEY\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-291">El miembro **dwReturn** devuelve el valor de índice de clave actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-291">The **dwReturn** member returns the current key-index value.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-292"><span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>\_monitor de \_ Estado de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-292"><span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>MCI\_DGV\_STATUS\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-293">El miembro **dwReturn** devuelve una constante que indica el origen de la presentación actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-293">The **dwReturn** member returns a constant indicating the source of the current presentation.</span></span> <span data-ttu-id="38c6a-294">Se definen las constantes siguientes:</span><span class="sxs-lookup"><span data-stu-id="38c6a-294">The following constants are defined:</span></span>

<span data-ttu-id="38c6a-295">\_archivo de \_ supervisión MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-295">MCI\_DGV\_MONITOR\_FILE</span></span>

<span data-ttu-id="38c6a-296">Un archivo es el origen.</span><span class="sxs-lookup"><span data-stu-id="38c6a-296">A file is the source.</span></span>

<span data-ttu-id="38c6a-297">\_entrada de \_ monitor de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-297">MCI\_DGV\_MONITOR\_INPUT</span></span>

<span data-ttu-id="38c6a-298">La entrada es el origen.</span><span class="sxs-lookup"><span data-stu-id="38c6a-298">The input is the source.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-299"><span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>\_método de \_ supervisión de estado de DGV de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-299"><span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>MCI\_DGV\_STATUS\_MONITOR\_METHOD</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-300">El miembro **dwReturn** devuelve una constante que indica el método que se usa para la supervisión de entradas.</span><span class="sxs-lookup"><span data-stu-id="38c6a-300">The **dwReturn** member returns a constant indicating the method used for input monitoring.</span></span> <span data-ttu-id="38c6a-301">Se definen las constantes siguientes:</span><span class="sxs-lookup"><span data-stu-id="38c6a-301">The following constants are defined:</span></span>

<span data-ttu-id="38c6a-302">\_método DGV de MCI \_ \_ directo</span><span class="sxs-lookup"><span data-stu-id="38c6a-302">MCI\_DGV\_METHOD\_DIRECT</span></span>

<span data-ttu-id="38c6a-303">Supervisión de entrada directa.</span><span class="sxs-lookup"><span data-stu-id="38c6a-303">Direct input monitoring.</span></span>

<span data-ttu-id="38c6a-304">\_post del \_ método \_ DGV de MCI</span><span class="sxs-lookup"><span data-stu-id="38c6a-304">MCI\_DGV\_METHOD\_POST</span></span>

<span data-ttu-id="38c6a-305">Supervisión posterior a la entrada.</span><span class="sxs-lookup"><span data-stu-id="38c6a-305">Post-input monitoring.</span></span>

<span data-ttu-id="38c6a-306">\_método MCI \_ DGV \_ pre</span><span class="sxs-lookup"><span data-stu-id="38c6a-306">MCI\_DGV\_METHOD\_PRE</span></span>

<span data-ttu-id="38c6a-307">Supervisión de entrada previa.</span><span class="sxs-lookup"><span data-stu-id="38c6a-307">Pre-input monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-308"><span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>\_modo de \_ pausa de estado de DGV de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-308"><span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>MCI\_DGV\_STATUS\_PAUSE\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-309">El miembro **dwReturn** devuelve el \_ modo MCI \_ Play si el dispositivo se pausó mientras se reproduce y devuelve \_ un registro en modo MCI \_ si el dispositivo se pausó durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="38c6a-309">The **dwReturn** member returns MCI\_MODE\_PLAY if the device was paused while playing and returns MCI\_MODE\_RECORD if the device was paused while recording.</span></span> <span data-ttu-id="38c6a-310">El comando devuelve la \_ función MCIERR \_ no aplicable como un error devuelto si el dispositivo no está en pausa.</span><span class="sxs-lookup"><span data-stu-id="38c6a-310">The command returns MCIERR\_NONAPPLICABLE\_FUNCTION as an error return if the device is not paused.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-311"><span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>MCI \_ DGV \_ status \_ SAMPLESPERSECOND</span><span class="sxs-lookup"><span data-stu-id="38c6a-311"><span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>MCI\_DGV\_STATUS\_SAMPLESPERSECOND</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-312">El miembro **dwReturn** devuelve el número de muestras por segundo grabadas.</span><span class="sxs-lookup"><span data-stu-id="38c6a-312">The **dwReturn** member returns the number of samples per second recorded.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-313"><span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>el \_ Estado de DGV de MCI \_ \_ busca \_ exactamente</span><span class="sxs-lookup"><span data-stu-id="38c6a-313"><span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>MCI\_DGV\_STATUS\_SEEK\_EXACTLY</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-314">El miembro **dwReturn** devuelve **true** o **false** que indica si se ha establecido o no el formato de búsqueda exactamente.</span><span class="sxs-lookup"><span data-stu-id="38c6a-314">The **dwReturn** member returns **TRUE** or **FALSE** indicating whether or not the seek exactly format is set.</span></span> <span data-ttu-id="38c6a-315">(Las aplicaciones pueden establecer este formato con el comando [MCI \_ set](mci-set.md) con el \_ marcador MCI DGV \_ set \_ Seek \_ Exactly).</span><span class="sxs-lookup"><span data-stu-id="38c6a-315">(Applications can set this format by using the [MCI\_SET](mci-set.md) command with the MCI\_DGV\_SET\_SEEK\_EXACTLY flag.)</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-316"><span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>\_nitidez de \_ Estado de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-316"><span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>MCI\_DGV\_STATUS\_SHARPNESS</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-317">El miembro **dwReturn** devuelve el nivel de nitidez actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-317">The **dwReturn** member returns the current sharpness level.</span></span> <span data-ttu-id="38c6a-318">Use MCI \_ DGV \_ status \_ nominal con esta marca para obtener el nivel nominal.</span><span class="sxs-lookup"><span data-stu-id="38c6a-318">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-319"><span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>\_tamaño de \_ Estado de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-319"><span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>MCI\_DGV\_STATUS\_SIZE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-320">El miembro **dwReturn** devuelve la duración de reproducción aproximada de los datos comprimidos que conservará el área de trabajo reservada.</span><span class="sxs-lookup"><span data-stu-id="38c6a-320">The **dwReturn** member returns the approximate playback duration of compressed data that the reserved workspace will hold.</span></span> <span data-ttu-id="38c6a-321">Las unidades de duración están en el formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-321">The duration units are in the current time format.</span></span> <span data-ttu-id="38c6a-322">Devuelve cero si no hay espacio en disco reservado.</span><span class="sxs-lookup"><span data-stu-id="38c6a-322">It returns zero if there is no reserved disk space.</span></span> <span data-ttu-id="38c6a-323">El tamaño devuelto es aproximado, ya que el espacio en disco preciso para los datos comprimidos no puede predecirse hasta que se hayan comprimido los datos.</span><span class="sxs-lookup"><span data-stu-id="38c6a-323">The size returned is approximate since the precise disk space for compressed data cannot, in general, be predicted until after the data has been compressed.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-324"><span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>Estado de DGV de MCI \_ \_ \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="38c6a-324"><span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>MCI\_DGV\_STATUS\_SMPTE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-325">El miembro **dwReturn** devuelve el código de tiempo SMPTE asociado a la posición actual en el área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="38c6a-325">The **dwReturn** member returns the SMPTE time code associated with the current position in the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-326"><span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>\_velocidad de \_ Estado de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-326"><span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>MCI\_DGV\_STATUS\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-327">El miembro **dwReturn** devuelve la velocidad de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-327">The **dwReturn** member returns the current playback speed.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-328"><span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>Estado de DGV de MCI \_ \_ \_ todavía \_ FILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="38c6a-328"><span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>MCI\_DGV\_STATUS\_STILL\_FILEFORMAT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-329">El miembro **dwReturn** devuelve el formato de archivo actual para el comando [MCI \_ Capture](mci-capture.md) .</span><span class="sxs-lookup"><span data-stu-id="38c6a-329">The **dwReturn** member returns the current file format for the [MCI\_CAPTURE](mci-capture.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-330"><span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>\_matiz de \_ Estado de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-330"><span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>MCI\_DGV\_STATUS\_TINT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-331">El miembro **dwReturn** devuelve el nivel de matiz de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-331">The **dwReturn** member returns the current video tint level.</span></span> <span data-ttu-id="38c6a-332">Use MCI \_ DGV \_ status \_ nominal con esta marca para obtener el nivel nominal.</span><span class="sxs-lookup"><span data-stu-id="38c6a-332">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-333"><span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>Estado de DGV de MCI \_ \_ \_ agudos</span><span class="sxs-lookup"><span data-stu-id="38c6a-333"><span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>MCI\_DGV\_STATUS\_TREBLE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-334">El miembro **dwReturn** devuelve el nivel de agudos de audio actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-334">The **dwReturn** member returns the current audio treble level.</span></span> <span data-ttu-id="38c6a-335">Use MCI \_ DGV \_ status \_ nominal con esta marca para obtener el nivel nominal.</span><span class="sxs-lookup"><span data-stu-id="38c6a-335">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-336"><span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>Estado de DGV de MCI sin \_ \_ \_ Guardar</span><span class="sxs-lookup"><span data-stu-id="38c6a-336"><span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>MCI\_DGV\_STATUS\_UNSAVED</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-337">El miembro **dwReturn** devuelve **true** si hay datos registrados en el área de trabajo que podrían perderse como resultado de un [comando MCI \_ Close](mci-close.md), MCI [ \_ Load](mci-load.md), [MCI \_ Record](mci-record.md), MCI [ \_ reserva](mci-reserve.md), MCI [ \_ CUT](mci-cut.md), [MCI \_ Delete](mci-delete.md)o [MCI \_ Paste](mci-paste.md) .</span><span class="sxs-lookup"><span data-stu-id="38c6a-337">The **dwReturn** member returns **TRUE** if there is recorded data in the workspace that might be lost as a result of a [MCI\_CLOSE](mci-close.md), [MCI\_LOAD](mci-load.md), [MCI\_RECORD](mci-record.md), [MCI\_RESERVE](mci-reserve.md), [MCI\_CUT](mci-cut.md), [MCI\_DELETE](mci-delete.md), or [MCI\_PASTE](mci-paste.md) command.</span></span> <span data-ttu-id="38c6a-338">De lo contrario, el miembro devuelve **false** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-338">The member returns **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-339"><span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>\_vídeo de \_ Estado de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-339"><span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>MCI\_DGV\_STATUS\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-340">El miembro **dwReturn** devuelve MCI \_ en si el vídeo está HABILITAdo o MCI \_ desactivado si está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="38c6a-340">The **dwReturn** member returns MCI\_ON if video is enabled or MCI\_OFF if it is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-341"><span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>\_registro de \_ vídeo de estado de DGV de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-341"><span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>MCI\_DGV\_STATUS\_VIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-342">El miembro **dwReturn** devuelve MCI \_ on o MCI \_ OFF, que refleja el estado establecido por la \_ marca MCI DGV \_ SETVIDEO \_ Record del comando [MCI \_ SETVIDEO](mci-setvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="38c6a-342">The **dwReturn** member returns MCI\_ON or MCI\_OFF, reflecting the state set by the MCI\_DGV\_SETVIDEO\_RECORD flag of the [MCI\_SETVIDEO](mci-setvideo.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-343"><span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>\_origen de \_ vídeo de estado de DGV de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-343"><span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>MCI\_DGV\_STATUS\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-344">El miembro **dwReturn** devuelve una constante que indica el tipo de origen de vídeo establecido por la \_ marca de origen MCI DGV \_ SETVIDEO \_ del comando **MCI \_ SETVIDEO** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-344">The **dwReturn** member returns a constant indicating the type of video source set by the MCI\_DGV\_SETVIDEO\_SOURCE flag of the **MCI\_SETVIDEO** command.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-345"><span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>Estado de DGV de MCI \_ \_ vídeo de estado \_ \_ src \_ NUM</span><span class="sxs-lookup"><span data-stu-id="38c6a-345"><span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>MCI\_DGV\_STATUS\_VIDEO\_SRC\_NUM</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-346">El miembro **dwReturn** devuelve el número dentro de su tipo de origen de entrada de vídeo activo actualmente.</span><span class="sxs-lookup"><span data-stu-id="38c6a-346">The **dwReturn** member returns the number within its type of the video-input source currently active.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-347"><span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>\_secuencia de \_ vídeo de estado de DGV de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-347"><span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>MCI\_DGV\_STATUS\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-348">El miembro **dwReturn** devuelve el número de secuencia de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-348">The **dwReturn** member returns the current video-stream number.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-349"><span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>\_volumen de \_ Estado de DGV de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-349"><span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>MCI\_DGV\_STATUS\_VOLUME</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-350">El miembro **dwReturn** devuelve el promedio del volumen a los altavoces izquierdo y derecho.</span><span class="sxs-lookup"><span data-stu-id="38c6a-350">The **dwReturn** member returns the average of the volume to the left and right speakers.</span></span> <span data-ttu-id="38c6a-351">Use MCI \_ DGV \_ status \_ nominal con esta marca para obtener el nivel nominal.</span><span class="sxs-lookup"><span data-stu-id="38c6a-351">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-352"><span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>ventana de estado de DGV de MCI \_ \_ \_ \_ visible</span><span class="sxs-lookup"><span data-stu-id="38c6a-352"><span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>MCI\_DGV\_STATUS\_WINDOW\_VISIBLE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-353">El miembro **dwReturn** devuelve **true** si la ventana no está oculta.</span><span class="sxs-lookup"><span data-stu-id="38c6a-353">The **dwReturn** member returns **TRUE** if the window is not hidden.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-354"><span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>ventana de estado de DGV de MCI \_ \_ \_ \_ minimizada</span><span class="sxs-lookup"><span data-stu-id="38c6a-354"><span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>MCI\_DGV\_STATUS\_WINDOW\_MINIMIZED</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-355">El miembro **dwReturn** devuelve **true** si la ventana está minimizada.</span><span class="sxs-lookup"><span data-stu-id="38c6a-355">The **dwReturn** member returns **TRUE** if the window is minimized.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-356"><span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>ventana de estado de DGV de MCI \_ \_ \_ \_ maximizada</span><span class="sxs-lookup"><span data-stu-id="38c6a-356"><span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>MCI\_DGV\_STATUS\_WINDOW\_MAXIMIZED</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-357">El miembro **dwReturn** devuelve **true** si la ventana está maximizada.</span><span class="sxs-lookup"><span data-stu-id="38c6a-357">The **dwReturn** member returns **TRUE** if the window is maximized.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-358"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>medios de estado de MCI \_ \_ \_ presentes</span><span class="sxs-lookup"><span data-stu-id="38c6a-358"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-359">El miembro **dwReturn** devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="38c6a-359">The **dwReturn** member returns **TRUE**.</span></span>

</dd> </dl>

<span data-ttu-id="38c6a-360">En el caso de los dispositivos de vídeo digital, el parámetro *lpStatus* apunta a una estructura [**MCI \_ DGV \_ status \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="38c6a-360">For digital-video devices, the *lpStatus* parameter points to an [**MCI\_DGV\_STATUS\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa) structure.</span></span>

<span data-ttu-id="38c6a-361">Se usan las siguientes marcas adicionales con el tipo de dispositivo **Sequencer** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-361">The following additional flags are used with the **sequencer** device type.</span></span> <span data-ttu-id="38c6a-362">Estas constantes se utilizan en el miembro **dwItem** de la estructura a la que apunta el parámetro *lpStatus* cuando \_ \_ se especifica el elemento de estado de MCI para el parámetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="38c6a-362">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="38c6a-363"><span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>MCI \_ Seq \_ status \_ DIVTYPE</span><span class="sxs-lookup"><span data-stu-id="38c6a-363"><span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>MCI\_SEQ\_STATUS\_DIVTYPE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-364">El miembro **dwReturn** se establece en uno de los siguientes valores que indican el tipo de división actual de una secuencia:</span><span class="sxs-lookup"><span data-stu-id="38c6a-364">The **dwReturn** member is set to one of the following values indicating the current division type of a sequence:</span></span>

-   <span data-ttu-id="38c6a-365">MCI \_ Seq \_ div \_ PPQN</span><span class="sxs-lookup"><span data-stu-id="38c6a-365">MCI\_SEQ\_DIV\_PPQN</span></span>
-   <span data-ttu-id="38c6a-366">MCI \_ Seq \_ div \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="38c6a-366">MCI\_SEQ\_DIV\_SMPTE\_24</span></span>
-   <span data-ttu-id="38c6a-367">MCI \_ Seq \_ div \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="38c6a-367">MCI\_SEQ\_DIV\_SMPTE\_25</span></span>
-   <span data-ttu-id="38c6a-368">MCI \_ Seq \_ div \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="38c6a-368">MCI\_SEQ\_DIV\_SMPTE\_30</span></span>
-   <span data-ttu-id="38c6a-369">MCI \_ Seq \_ div \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="38c6a-369">MCI\_SEQ\_DIV\_SMPTE\_30DROP</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-370"><span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>\_maestro de \_ Estado de SEQ de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-370"><span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>MCI\_SEQ\_STATUS\_MASTER</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-371">El miembro **dwReturn** se establece en el tipo de sincronización que se usa para la operación maestra.</span><span class="sxs-lookup"><span data-stu-id="38c6a-371">The **dwReturn** member is set to the synchronization type used for master operation.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-372"><span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>\_desplazamiento de \_ Estado de SEQ de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-372"><span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>MCI\_SEQ\_STATUS\_OFFSET</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-373">El miembro **dwReturn** se establece en el desplazamiento SMPTE actual de una secuencia.</span><span class="sxs-lookup"><span data-stu-id="38c6a-373">The **dwReturn** member is set to the current SMPTE offset of a sequence.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-374"><span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>\_Puerto de \_ Estado de sec. \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-374"><span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>MCI\_SEQ\_STATUS\_PORT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-375">El miembro **dwReturn** se establece en el identificador de dispositivo MIDI para el puerto actual utilizado por la secuencia.</span><span class="sxs-lookup"><span data-stu-id="38c6a-375">The **dwReturn** member is set to the MIDI device identifier for the current port used by the sequence.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-376"><span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>MCI \_ Seq \_ status \_ esclavo</span><span class="sxs-lookup"><span data-stu-id="38c6a-376"><span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>MCI\_SEQ\_STATUS\_SLAVE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-377">El miembro **dwReturn** se establece en el tipo de sincronización que se usa para la operación subordinada.</span><span class="sxs-lookup"><span data-stu-id="38c6a-377">The **dwReturn** member is set to the synchronization type used for subordinate operation.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-378"><span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>Temp. de \_ Estado de sec. \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-378"><span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>MCI\_SEQ\_STATUS\_TEMPO</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-379">El miembro **dwReturn** se establece en el tempo actual de una secuencia MIDI en pulsaciones por minuto para archivos PPQN o fotogramas por segundo para archivos SMPTE.</span><span class="sxs-lookup"><span data-stu-id="38c6a-379">The **dwReturn** member is set to the current tempo of a MIDI sequence in beats per minute for PPQN files, or frames per second for SMPTE files.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-380"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>medios de estado de MCI \_ \_ \_ presentes</span><span class="sxs-lookup"><span data-stu-id="38c6a-380"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-381">El miembro **dwReturn** se establece en **true** si el medio se inserta en el dispositivo; en caso contrario, se establece en **false** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-381">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="38c6a-382">Se usan las siguientes marcas adicionales con el tipo de dispositivo **VCR** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-382">The following additional flags are used with the **vcr** device type.</span></span> <span data-ttu-id="38c6a-383">Estas constantes se utilizan en el miembro **dwItem** de la estructura a la que apunta el parámetro *lpStatus* cuando \_ \_ se especifica el elemento de estado de MCI para el parámetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="38c6a-383">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="38c6a-384"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>medios de estado de MCI \_ \_ \_ presentes</span><span class="sxs-lookup"><span data-stu-id="38c6a-384"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-385">El miembro **dwReturn** se establece en **true** si el medio se inserta en el dispositivo; en caso contrario, se establece en **false** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-385">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-386"><span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>\_registro de \_ Estado de VCR \_ de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-386"><span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>MCI\_VCR\_STATUS\_ASSEMBLE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-387">El miembro **dwReturn** se establece en **true** si el modo de ensamblaje es on; en caso contrario, se establece en **false** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-387">The **dwReturn** member is set to **TRUE** if assemble mode is on; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-388"><span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>\_monitor de \_ audio de estado de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-388"><span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>MCI\_VCR\_STATUS\_AUDIO\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-389">El miembro **dwReturn** se establece en una constante, que indica el tipo de monitor de audio seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="38c6a-389">The **dwReturn** member is set to a constant, indicating the currently selected audio-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-390"><span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>\_número de \_ monitor de audio de estado de VCR de \_ \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-390"><span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>MCI\_VCR\_STATUS\_AUDIO\_MONITOR\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-391">El miembro **dwReturn** se establece en el número del tipo de monitor de audio seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="38c6a-391">The **dwReturn** member is set to the number of the currently selected audio-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-392"><span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>\_registro de \_ audio de estado de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-392"><span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>MCI\_VCR\_STATUS\_AUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-393">El miembro **dwReturn** se establece en **true** si el audio se grabará cuando se proporcione el siguiente comando de registro; en caso contrario, se establece en **false** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-393">The **dwReturn** member is set to **TRUE** if audio will be recorded when the next record command is given; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="38c6a-394">Si especifica MCI \_ Track en el parámetro *dwFlags* de este comando, **dwTrack** contiene el seguimiento al que se aplica esta consulta.</span><span class="sxs-lookup"><span data-stu-id="38c6a-394">If you specify MCI\_TRACK in the *dwFlags* parameter of this command, **dwTrack** contains the track this inquiry applies to.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-395"><span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>\_origen de \_ audio de estado de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-395"><span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>MCI\_VCR\_STATUS\_AUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-396">El miembro **dwReturn** se establece en una constante, que indica el tipo de origen de audio actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-396">The **dwReturn** member is set to a constant, indicating the current audio-source type.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-397"><span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>\_número de \_ origen de audio de estado de VCR de \_ \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-397"><span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>MCI\_VCR\_STATUS\_AUDIO\_SOURCE\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-398">El miembro **dwReturn** se establece en el número del tipo de origen de audio seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="38c6a-398">The **dwReturn** member is set to the number of the currently selected audio-source type.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-399"><span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>\_reloj de \_ Estado de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-399"><span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>MCI\_VCR\_STATUS\_CLOCK</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-400">El miembro **dwReturn** se establece en el valor del reloj actual, en incrementos de reloj totales.</span><span class="sxs-lookup"><span data-stu-id="38c6a-400">The **dwReturn** member is set to the current clock value, in total clock increments.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-401"><span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>\_identificador de \_ reloj de estado de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-401"><span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>MCI\_VCR\_STATUS\_CLOCK\_ID</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-402">El miembro **dwReturn** se establece en un número que describe de forma única el reloj en uso.</span><span class="sxs-lookup"><span data-stu-id="38c6a-402">The **dwReturn** member is set to a number which uniquely describes the clock in use.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-403"><span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>\_formato de \_ contador de estado de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-403"><span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>MCI\_VCR\_STATUS\_COUNTER\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-404">El miembro **dwReturn** se establece en una constante que describe el formato del contador actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-404">The **dwReturn** member is set to a constant describing the current counter format.</span></span> <span data-ttu-id="38c6a-405">Para obtener más información, consulte la \_ \_ \_ marca de formato de hora de set MCI del comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="38c6a-405">For more information, see the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-406"><span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>\_resolución de \_ contador de estado de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-406"><span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>MCI\_VCR\_STATUS\_COUNTER\_RESOLUTION</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-407">El miembro **dwReturn** se establece en una constante que describe la resolución del contador y es uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="38c6a-407">The **dwReturn** member is set to a constant describing the resolution of the counter, and is one of the following values:</span></span>

-   <span data-ttu-id="38c6a-408">\_ \_ \_ Fotogramas res \_ de contador de VCR MCI: el contador tiene resolución de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="38c6a-408">MCI\_VCR\_COUNTER\_RES\_FRAMES: Counter has resolution of frames.</span></span>
-   <span data-ttu-id="38c6a-409">\_Recuento \_ de contadores de VCR MCI \_ \_ segundos: el contador tiene una resolución de segundos.</span><span class="sxs-lookup"><span data-stu-id="38c6a-409">MCI\_VCR\_COUNTER\_RES\_SECONDS: Counter has resolution of seconds.</span></span>
-   <span data-ttu-id="38c6a-410">\_Valor del \_ contador de estado de VCR \_ de MCI \_ : el miembro **dwReturn** se establece en la lectura del contador actual, en el formato de tiempo de contador actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-410">MCI\_VCR\_STATUS\_COUNTER\_VALUE: The **dwReturn** member is set to the current counter reading, in the current counter-time format.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-411"><span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>\_velocidad de \_ \_ fotogramas de estado VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-411"><span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>MCI\_VCR\_STATUS\_FRAME\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-412">El miembro **dwReturn** se establece en la velocidad actual de fotogramas nativa del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="38c6a-412">The **dwReturn** member is set to the current native frame rate of the device.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-413"><span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>\_Índice de \_ Estado de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-413"><span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>MCI\_VCR\_STATUS\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-414">El miembro **dwReturn** se establece en una constante, que describe el contenido actual de la presentación en pantalla, y es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="38c6a-414">The **dwReturn** member is set to a constant, describing the current contents of the on-screen display, and is one of the following:</span></span>

-   <span data-ttu-id="38c6a-415">\_contador de \_ Índice de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-415">MCI\_VCR\_INDEX\_COUNTER</span></span>
-   <span data-ttu-id="38c6a-416">\_fecha de \_ Índice de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-416">MCI\_VCR\_INDEX\_DATE</span></span>
-   <span data-ttu-id="38c6a-417">\_tiempo de \_ Índice de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-417">MCI\_VCR\_INDEX\_TIME</span></span>
-   <span data-ttu-id="38c6a-418">\_código de \_ tiempo del índice de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-418">MCI\_VCR\_INDEX\_TIMECODE</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-419"><span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>\_ \_ \_ Índice \_ de estado del VCR de MCI en</span><span class="sxs-lookup"><span data-stu-id="38c6a-419"><span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>MCI\_VCR\_STATUS\_INDEX\_ON</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-420">El miembro **dwReturn** se establece en **true** si la presentación en pantalla está activada; en caso contrario, se establece en **false** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-420">The **dwReturn** member is set to **TRUE** if the on-screen display is on; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-421"><span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>\_tipo de medio MCI VCR \_ status \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-421"><span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>MCI\_VCR\_STATUS\_MEDIA\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-422">El miembro **dwReturn** se establece en uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="38c6a-422">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="38c6a-423">Medios de vídeo de MCI \_ \_ \_ 8mm</span><span class="sxs-lookup"><span data-stu-id="38c6a-423">MCI\_VCR\_MEDIA\_8MM</span></span>
-   <span data-ttu-id="38c6a-424">\_Medios VCR de MCI \_ \_ Hi8</span><span class="sxs-lookup"><span data-stu-id="38c6a-424">MCI\_VCR\_MEDIA\_HI8</span></span>
-   <span data-ttu-id="38c6a-425">\_ \_ SHV multimedia de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-425">MCI\_VCR\_MEDIA\_VHS</span></span>
-   <span data-ttu-id="38c6a-426">\_medios VCR de MCI \_ \_ SVHS</span><span class="sxs-lookup"><span data-stu-id="38c6a-426">MCI\_VCR\_MEDIA\_SVHS</span></span>
-   <span data-ttu-id="38c6a-427">\_ \_ versión beta de medios VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-427">MCI\_VCR\_MEDIA\_BETA</span></span>
-   <span data-ttu-id="38c6a-428">\_medios VCR de MCI \_ \_ EDBETA</span><span class="sxs-lookup"><span data-stu-id="38c6a-428">MCI\_VCR\_MEDIA\_EDBETA</span></span>
-   <span data-ttu-id="38c6a-429">\_medios de VCR MCI \_ \_ otros</span><span class="sxs-lookup"><span data-stu-id="38c6a-429">MCI\_VCR\_MEDIA\_OTHER</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-430"><span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>\_número de \_ Estado de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-430"><span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>MCI\_VCR\_STATUS\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-431">El miembro **dwNumber** se establece en el número de sintonizador lógico cuando se usa esta marca con la \_ marca MCI VCR \_ status \_ Tuner \_ Channel.</span><span class="sxs-lookup"><span data-stu-id="38c6a-431">The **dwNumber** member is set to the logical-tuner number when you use this flag with the MCI\_VCR\_STATUS\_TUNER\_CHANNEL flag.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-432"><span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>\_ \_ \_ número \_ de estado del VCR de MCI de \_ pistas de audio \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-432"><span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>MCI\_VCR\_STATUS\_NUMBER\_OF\_AUDIO\_TRACKS</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-433">El miembro **dwReturn** se establece en el número de pistas de audio que se pueden seleccionar de manera independiente.</span><span class="sxs-lookup"><span data-stu-id="38c6a-433">The **dwReturn** member is set to the number of audio tracks that are independently selectable.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-434"><span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>\_ \_ \_ número \_ de estado del VCR de MCI de \_ pistas de vídeo \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-434"><span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>MCI\_VCR\_STATUS\_NUMBER\_OF\_VIDEO\_TRACKS</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-435">El miembro **dwReturn** se establece en el número de pistas de vídeo que pueden seleccionarse de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="38c6a-435">The **dwReturn** member is set to the number of video tracks that are independently selectable.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-436"><span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>\_tiempo de \_ espera de estado del VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-436"><span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>MCI\_VCR\_STATUS\_PAUSE\_TIMEOUT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-437">El miembro **dwReturn** se establece en la duración máxima, en milisegundos, de un comando PAUSE.</span><span class="sxs-lookup"><span data-stu-id="38c6a-437">The **dwReturn** member is set to the maximum duration, in milliseconds, of a pause command.</span></span> <span data-ttu-id="38c6a-438">El valor devuelto de cero indica que no se producirá ningún tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="38c6a-438">The return value of zero indicates that no time-out will occur.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-439"><span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>\_formato de \_ reproducción de estado de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-439"><span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>MCI\_VCR\_STATUS\_PLAY\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-440">El miembro **dwReturn** se establece en uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="38c6a-440">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="38c6a-441">formato de VCR de MCI \_ \_ \_ EP</span><span class="sxs-lookup"><span data-stu-id="38c6a-441">MCI\_VCR\_FORMAT\_EP</span></span>
-   <span data-ttu-id="38c6a-442">formato de VCR de MCI \_ \_ \_ LP</span><span class="sxs-lookup"><span data-stu-id="38c6a-442">MCI\_VCR\_FORMAT\_LP</span></span>
-   <span data-ttu-id="38c6a-443">\_formato de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-443">MCI\_VCR\_FORMAT\_OTHER</span></span>
-   <span data-ttu-id="38c6a-444">\_SP de \_ formato \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="38c6a-444">MCI\_VCR\_FORMAT\_SP</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-445"><span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>\_duración de \_ PostRoll de estado de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-445"><span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>MCI\_VCR\_STATUS\_POSTROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-446">El miembro **dwReturn** se establece en la longitud de la cinta de vídeo que se reproducirá después del punto en el que se detuvo, en el formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-446">The **dwReturn** member is set to the length of the videotape that will play after the spot at which it was stopped, in the current time format.</span></span> <span data-ttu-id="38c6a-447">Esto es necesario para frenar el transporte de cinta VCR desde un comando detener o pausar.</span><span class="sxs-lookup"><span data-stu-id="38c6a-447">This is needed to brake the VCR tape transport from a stop or pause command.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-448"><span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>\_ \_ \_ encendido \_ de estado de VCR de MCI</span><span class="sxs-lookup"><span data-stu-id="38c6a-448"><span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>MCI\_VCR\_STATUS\_POWER\_ON</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-449">El miembro **dwReturn** se establece en **true** si la alimentación está activada; en caso contrario, se establece en **false** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-449">The **dwReturn** member is set to **TRUE** if the power is on; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-450"><span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>\_duración del \_ prelanzamiento de estado de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-450"><span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>MCI\_VCR\_STATUS\_PREROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-451">El miembro **dwReturn** se establece en la longitud de la cinta de vídeo que se reproducirá antes del punto en el que se inició, en el formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-451">The **dwReturn** member is set to the length of the videotape that will play before the spot at which it was started, in the current time format.</span></span> <span data-ttu-id="38c6a-452">Esto es necesario para estabilizar la salida del VCR.</span><span class="sxs-lookup"><span data-stu-id="38c6a-452">This is needed to stabilize the VCR output.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-453"><span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>\_formato de \_ registro de estado de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-453"><span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>MCI\_VCR\_STATUS\_RECORD\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-454">El miembro **dwReturn** se establece en uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="38c6a-454">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="38c6a-455">formato de VCR de MCI \_ \_ \_ EP</span><span class="sxs-lookup"><span data-stu-id="38c6a-455">MCI\_VCR\_FORMAT\_EP</span></span>
-   <span data-ttu-id="38c6a-456">formato de VCR de MCI \_ \_ \_ LP</span><span class="sxs-lookup"><span data-stu-id="38c6a-456">MCI\_VCR\_FORMAT\_LP</span></span>
-   <span data-ttu-id="38c6a-457">\_formato de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-457">MCI\_VCR\_FORMAT\_OTHER</span></span>
-   <span data-ttu-id="38c6a-458">\_SP de \_ formato \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="38c6a-458">MCI\_VCR\_FORMAT\_SP</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-459"><span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>\_velocidad de \_ Estado de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-459"><span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>MCI\_VCR\_STATUS\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-460">El miembro **dwReturn** se establece en la velocidad actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-460">The **dwReturn** member is set to the current speed.</span></span> <span data-ttu-id="38c6a-461">Para obtener más información, consulte la \_ \_ \_ marca de velocidad del conjunto de VCR MCI del comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="38c6a-461">For more information, see the MCI\_VCR\_SET\_SPEED flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-462"><span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>\_modo de \_ tiempo de estado de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-462"><span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>MCI\_VCR\_STATUS\_TIME\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-463">El miembro **dwReturn** se establece en uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="38c6a-463">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="38c6a-464">\_contador de \_ tiempo de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-464">MCI\_VCR\_TIME\_COUNTER</span></span>
-   <span data-ttu-id="38c6a-465">\_detección de \_ tiempo de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-465">MCI\_VCR\_TIME\_DETECT</span></span>
-   <span data-ttu-id="38c6a-466">\_código de \_ tiempo de vídeo de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-466">MCI\_VCR\_TIME\_TIMECODE</span></span>

<span data-ttu-id="38c6a-467">Para obtener más información, consulte la \_ \_ marca del \_ modo de tiempo Set VCR \_ de MCI del comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="38c6a-467">For more information, see the MCI\_VCR\_SET\_TIME\_MODE flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-468"><span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>\_tipo de \_ hora de estado de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-468"><span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>MCI\_VCR\_STATUS\_TIME\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-469">El miembro **dwReturn** se establece en una constante que describe el tipo de hora actual en uso (usado por [Play](play.md), [Record](record.md), [Seek](seek.md), etc.) y es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="38c6a-469">The **dwReturn** member is set to a constant describing the current time type in use (used by [play](play.md), [record](record.md), [seek](seek.md), and so on), and is one of the following:</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-470"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>\_contador de \_ tiempo de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-470"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>MCI\_VCR\_TIME\_COUNTER</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-471">El contador está en uso.</span><span class="sxs-lookup"><span data-stu-id="38c6a-471">Counter is in use.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-472"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>\_código de \_ tiempo de vídeo de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-472"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI\_VCR\_TIME\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-473">El código de tiempo está en uso.</span><span class="sxs-lookup"><span data-stu-id="38c6a-473">Timecode is in use.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-474"><span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>el \_ código de tiempo de estado del VCR de MCI \_ \_ \_ está presente</span><span class="sxs-lookup"><span data-stu-id="38c6a-474"><span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>MCI\_VCR\_STATUS\_TIMECODE\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-475">El miembro **dwReturn** se establece en **true** si el código de tiempo está presente en la posición actual del contenido. en caso contrario, se establece en **false** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-475">The **dwReturn** member is set to **TRUE** if timecode is present at the current position in the content; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-476"><span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>\_registro de \_ código de \_ tiempo de estado VCR \_ de MCI</span><span class="sxs-lookup"><span data-stu-id="38c6a-476"><span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>MCI\_VCR\_STATUS\_TIMECODE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-477">El miembro **dwReturn** se establece en **true** si el código de tiempo se registrará cuando se proporcione el siguiente comando de registro; en caso contrario, se establece en **false** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-477">The **dwReturn** member is set to **TRUE** if the timecode will be recorded when the next record command is given; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-478"><span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>\_tipo de \_ código de tiempo de estado de VCR de \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-478"><span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>MCI\_VCR\_STATUS\_TIMECODE\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-479">El miembro **dwReturn** se establece en una constante, que describe el tipo de código de tiempo que el dispositivo admite directamente, y es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="38c6a-479">The **dwReturn** member is set to a constant, describing the type of timecode that is directly supported by the device, and is one of the following:</span></span>

-   <span data-ttu-id="38c6a-480">\_ \_ Tipo de código de tiempo de VCR de MCI \_ \_ ninguno: este dispositivo no usa un código de tiempo.</span><span class="sxs-lookup"><span data-stu-id="38c6a-480">MCI\_VCR\_TIMECODE\_TYPE\_NONE: This device does not use a timecode.</span></span>
-   <span data-ttu-id="38c6a-481">Tipo de código de tiempo de VCR de MCI \_ \_ \_ \_ : este dispositivo usa un código de tiempo no especificado.</span><span class="sxs-lookup"><span data-stu-id="38c6a-481">MCI\_VCR\_TIMECODE\_TYPE\_OTHER: This device uses an unspecified timecode.</span></span>
-   <span data-ttu-id="38c6a-482">\_Tipo SMPTE de código de tiempo de VCR de MCI \_ \_ \_ : este dispositivo usa código de tiempo SMPTE.</span><span class="sxs-lookup"><span data-stu-id="38c6a-482">MCI\_VCR\_TIMECODE\_TYPE\_SMPTE: This device uses SMPTE timecode.</span></span>
-   <span data-ttu-id="38c6a-483">Tipo de código de tiempo del VCR de MCI \_ \_ \_ \_ \_ Drop SMPTE: este dispositivo usa el código de tiempo Drop SMPTE.</span><span class="sxs-lookup"><span data-stu-id="38c6a-483">MCI\_VCR\_TIMECODE\_TYPE\_SMPTE\_DROP: This device uses SMPTE drop timecode.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-484"><span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>\_canal de \_ \_ sintonizador de estado de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-484"><span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>MCI\_VCR\_STATUS\_TUNER\_CHANNEL</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-485">El miembro **dwReturn** se establece en el número de canal actual.</span><span class="sxs-lookup"><span data-stu-id="38c6a-485">The **dwReturn** member is set to the current channel number.</span></span> <span data-ttu-id="38c6a-486">Si especifica MCI \_ VCR \_ status \_ Number en el parámetro *dwFlags* de este comando, **dwNumber** contiene el número de sintonizador lógico al que se aplica este comando.</span><span class="sxs-lookup"><span data-stu-id="38c6a-486">If you specify MCI\_VCR\_STATUS\_NUMBER in the *dwFlags* parameter of this command, **dwNumber** contains the logical-tuner number this command applies to.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-487"><span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>\_monitor de \_ vídeo de estado de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-487"><span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>MCI\_VCR\_STATUS\_VIDEO\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-488">El miembro **dwReturn** se establece en una constante, que indica el tipo de monitor de vídeo seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="38c6a-488">The **dwReturn** member is set to a constant, indicating the currently selected video-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-489"><span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>\_número de \_ monitor de vídeo de estado de VCR de \_ \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-489"><span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>MCI\_VCR\_STATUS\_VIDEO\_MONITOR\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-490">El miembro **dwReturn** se establece en el número del tipo de monitor de vídeo seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="38c6a-490">The **dwReturn** member is set to the number of the currently selected video-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-491"><span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>\_grabación de \_ vídeo de estado de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-491"><span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>MCI\_VCR\_STATUS\_VIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-492">El miembro **dwReturn** se establece en **true** si el vídeo se registrará cuando se proporcione el siguiente comando de registro; en caso contrario, se establece en **false** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-492">The **dwReturn** member is set to **TRUE** if video will be recorded when the next record command is given; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="38c6a-493">Si especifica MCI \_ Track en el parámetro *dwFlags* de este comando, **dwTrack** contiene el seguimiento al que se aplica esta consulta.</span><span class="sxs-lookup"><span data-stu-id="38c6a-493">If you specify MCI\_TRACK in the *dwFlags* parameter of this command, **dwTrack** contains the track this inquiry applies to.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-494"><span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>\_origen de \_ vídeo de estado de VCR de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-494"><span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>MCI\_VCR\_STATUS\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-495">El miembro **dwReturn** se establece en una constante que indica el tipo de origen de vídeo seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="38c6a-495">The **dwReturn** member is set to a constant indicating the currently selected video-source type.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-496"><span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>\_número de \_ origen de vídeo de estado de VCR de \_ \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-496"><span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>MCI\_VCR\_STATUS\_VIDEO\_SOURCE\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-497">El miembro **dwReturn** se establece en el número del tipo de origen de vídeo seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="38c6a-497">The **dwReturn** member is set to the number of the currently selected video-source type.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-498"><span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>Estado de VCR de MCI \_ \_ \_ \_ protegido contra escritura</span><span class="sxs-lookup"><span data-stu-id="38c6a-498"><span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>MCI\_VCR\_STATUS\_WRITE\_PROTECTED</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-499">El miembro **dwReturn** se establece en **true** si el medio está protegido contra escritura; en caso contrario, se establece en **false** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-499">The **dwReturn** member is set to **TRUE** if the media is write-protected; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="38c6a-500">En el caso de los dispositivos VCR, el parámetro *lpStatus* apunta a una estructura [**MCI \_ VCR \_ status \_ parms**](mci-vcr-status-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="38c6a-500">For VCR devices, the *lpStatus* parameter points to an [**MCI\_VCR\_STATUS\_PARMS**](mci-vcr-status-parms.md) structure.</span></span>

<span data-ttu-id="38c6a-501">El uso de \_ la \_ marca de longitud de estado de MCI para determinar la longitud de los medios siempre devuelve 2 horas para los dispositivos VCR, a menos que la longitud se haya cambiado explícitamente mediante el comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="38c6a-501">Using the MCI\_STATUS\_LENGTH flag to determine the length of the media always returns 2 hours for VCR devices, unless the length has been explicitly changed using the [MCI\_SET](mci-set.md) command.</span></span>

<span data-ttu-id="38c6a-502">Se usan las siguientes marcas adicionales con el tipo de dispositivo **superpuesto** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-502">The following additional flags are used with the **overlay** device type.</span></span> <span data-ttu-id="38c6a-503">Estas constantes se utilizan en el miembro **dwItem** de la estructura a la que apunta el parámetro *lpStatus* cuando \_ \_ se especifica el elemento de estado de MCI para el parámetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="38c6a-503">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="38c6a-504"><span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>\_OVLY de \_ estado \_ hWnd de MCI</span><span class="sxs-lookup"><span data-stu-id="38c6a-504"><span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>MCI\_OVLY\_STATUS\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-505">El miembro **dwReturn** se establece en el identificador de la ventana asociada con el dispositivo de superposición de vídeo.</span><span class="sxs-lookup"><span data-stu-id="38c6a-505">The **dwReturn** member is set to the handle of the window associated with the video-overlay device.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-506"><span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>\_Stretch OVLY de \_ estado \_ de MCI</span><span class="sxs-lookup"><span data-stu-id="38c6a-506"><span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>MCI\_OVLY\_STATUS\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-507">El miembro **dwReturn** se establece en **true** si está habilitada la expansión; en caso contrario, se establece en **false** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-507">The **dwReturn** member is set to **TRUE** if stretching is enabled; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-508"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>medios de estado de MCI \_ \_ \_ presentes</span><span class="sxs-lookup"><span data-stu-id="38c6a-508"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-509">El miembro **dwReturn** se establece en **true** si el medio se inserta en el dispositivo; en caso contrario, se establece en **false** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-509">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="38c6a-510">Se usan las siguientes marcas adicionales con el tipo de dispositivo de **videodisco** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-510">The following additional flags are used with the **videodisc** device type.</span></span> <span data-ttu-id="38c6a-511">Estas constantes se utilizan en el miembro **dwItem** de la estructura a la que apunta el parámetro *lpStatus* cuando \_ \_ se especifica el elemento de estado de MCI para el parámetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="38c6a-511">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="38c6a-512"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>medios de estado de MCI \_ \_ \_ presentes</span><span class="sxs-lookup"><span data-stu-id="38c6a-512"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-513">El miembro **dwReturn** se establece en **true** si el medio se inserta en el dispositivo; en caso contrario, se establece en **false** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-513">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-514"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>\_modo de estado de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-514"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MCI\_STATUS\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-515">El miembro **dwReturn** se establece en el modo actual del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="38c6a-515">The **dwReturn** member is set to the current mode of the device.</span></span> <span data-ttu-id="38c6a-516">Los dispositivos de videodisco pueden devolver la \_ constante de estacionamiento del modo MCI Vd \_ \_ , además de las constantes que puede devolver cualquier dispositivo, tal y como se documenta con el parámetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="38c6a-516">Videodisc devices can return the MCI\_VD\_MODE\_PARK constant, in addition to the constants any device can return, as documented with the *dwFlags* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-517"><span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>\_tamaño de \_ disco de estado \_ \_ de MCI Vd</span><span class="sxs-lookup"><span data-stu-id="38c6a-517"><span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>MCI\_VD\_STATUS\_DISC\_SIZE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-518">El miembro **dwReturn** se establece en el tamaño del disco cargado en pulgadas (8 o 12).</span><span class="sxs-lookup"><span data-stu-id="38c6a-518">The **dwReturn** member is set to the size of the loaded disc in inches (8 or 12).</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-519"><span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>Estado de MCI \_ Vd \_ \_ hacia delante</span><span class="sxs-lookup"><span data-stu-id="38c6a-519"><span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>MCI\_VD\_STATUS\_FORWARD</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-520">El miembro **dwReturn** se establece en **true** si se está jugando hacia delante; en caso contrario, se establece en **false** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-520">The **dwReturn** member is set to **TRUE** if playing forward; it is set to **FALSE** otherwise.</span></span>

<span data-ttu-id="38c6a-521">El dispositivo de videodisco de MCI no es compatible con esta marca.</span><span class="sxs-lookup"><span data-stu-id="38c6a-521">The MCI videodisc device does not support this flag.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-522"><span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>\_tipo de \_ medio de estado \_ \_ de MCI Vd</span><span class="sxs-lookup"><span data-stu-id="38c6a-522"><span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>MCI\_VD\_STATUS\_MEDIA\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-523">El miembro **dwReturn** se establece en el tipo de medio del medio insertado.</span><span class="sxs-lookup"><span data-stu-id="38c6a-523">The **dwReturn** member is set to the media type of the inserted media.</span></span> <span data-ttu-id="38c6a-524">Se pueden devolver los siguientes tipos de medios:</span><span class="sxs-lookup"><span data-stu-id="38c6a-524">The following media types can be returned:</span></span>

<span data-ttu-id="38c6a-525">CAV de medios de MCI \_ Vd \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-525">MCI\_VD\_MEDIA\_CAV</span></span>

<span data-ttu-id="38c6a-526">CLV de medios de MCI \_ Vd \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-526">MCI\_VD\_MEDIA\_CLV</span></span>

<span data-ttu-id="38c6a-527">medios de MCI \_ Vd \_ \_ otros</span><span class="sxs-lookup"><span data-stu-id="38c6a-527">MCI\_VD\_MEDIA\_OTHER</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-528"><span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>Estado de MCI \_ Vd \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-528"><span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>MCI\_VD\_STATUS\_SIDE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-529">El miembro **dwReturn** se establece en 1 o 2 para indicar el lado del disco que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="38c6a-529">The **dwReturn** member is set to 1 or 2 to indicate which side of the disc is loaded.</span></span> <span data-ttu-id="38c6a-530">No todos los dispositivos de videodisco admiten esta marca.</span><span class="sxs-lookup"><span data-stu-id="38c6a-530">Not all videodisc devices support this flag.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-531"><span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>velocidad de estado de MCI \_ Vd \_ \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-531"><span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>MCI\_VD\_STATUS\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-532">El miembro **dwReturn** se establece en la velocidad de reproducción en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="38c6a-532">The **dwReturn** member is set to the play speed in frames per second.</span></span> <span data-ttu-id="38c6a-533">MCIPIONR. El controlador de dispositivo DRV devuelve la \_ función MCIERR no admitida \_ .</span><span class="sxs-lookup"><span data-stu-id="38c6a-533">The MCIPIONR.DRV device driver returns MCIERR\_UNSUPPORTED\_FUNCTION.</span></span>

</dd> </dl>

<span data-ttu-id="38c6a-534">Se usan las siguientes marcas adicionales con el tipo de dispositivo **WaveAudio** .</span><span class="sxs-lookup"><span data-stu-id="38c6a-534">The following additional flags are used with the **waveaudio** device type.</span></span> <span data-ttu-id="38c6a-535">Estas constantes se utilizan en el miembro **dwItem** de la estructura a la que apunta el parámetro *lpStatus* cuando \_ \_ se especifica el elemento de estado de MCI para el parámetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="38c6a-535">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="38c6a-536"><span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>\_FORMATTAG de onda de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-536"><span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>MCI\_WAVE\_FORMATTAG</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-537">El miembro **dwReturn** se establece en la etiqueta de formato actual utilizada para reproducir, grabar y guardar.</span><span class="sxs-lookup"><span data-stu-id="38c6a-537">The **dwReturn** member is set to the current format tag used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-538"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrada de onda de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-538"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-539">El miembro **dwReturn** se establece en el dispositivo de entrada de onda que se usa para la grabación.</span><span class="sxs-lookup"><span data-stu-id="38c6a-539">The **dwReturn** member is set to the wave input device used for recording.</span></span> <span data-ttu-id="38c6a-540">Si no hay ningún dispositivo en uso y no se ha establecido explícitamente ningún dispositivo, el error devuelto es MCIERR \_ Wave \_ INPUTUNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="38c6a-540">If no device is in use and no device has been explicitly set, then the error return is MCIERR\_WAVE\_INPUTUNSPECIFIED.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-541"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_salida de onda de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-541"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-542">El miembro **dwReturn** se establece en el dispositivo de salida de onda que se usa para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="38c6a-542">The **dwReturn** member is set to the wave output device used for playing.</span></span> <span data-ttu-id="38c6a-543">Si no hay ningún dispositivo en uso y no se ha establecido explícitamente ningún dispositivo, el error devuelto es MCIERR \_ Wave \_ OUTPUTUNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="38c6a-543">If no device is in use and no device has been explicitly set, then the error return is MCIERR\_WAVE\_OUTPUTUNSPECIFIED.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-544"><span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>Estado de onda de MCI \_ \_ \_ AVGBYTESPERSEC</span><span class="sxs-lookup"><span data-stu-id="38c6a-544"><span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>MCI\_WAVE\_STATUS\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-545">El miembro **dwReturn** se establece en los bytes actuales por segundo utilizados para reproducir, grabar y guardar.</span><span class="sxs-lookup"><span data-stu-id="38c6a-545">The **dwReturn** member is set to the current bytes per second used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-546"><span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>Estado de onda de MCI \_ \_ \_ BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="38c6a-546"><span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>MCI\_WAVE\_STATUS\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-547">El miembro **dwReturn** se establece en los bits actuales por muestra que se usan para reproducir, grabar y guardar datos con formato PCM.</span><span class="sxs-lookup"><span data-stu-id="38c6a-547">The **dwReturn** member is set to the current bits per sample used for playing, recording, and saving PCM formatted data.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-548"><span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>Estado de onda de MCI \_ \_ \_ BLOCKALIGN</span><span class="sxs-lookup"><span data-stu-id="38c6a-548"><span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>MCI\_WAVE\_STATUS\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-549">El miembro **dwReturn** se establece en la alineación de bloque actual utilizada para reproducir, grabar y guardar.</span><span class="sxs-lookup"><span data-stu-id="38c6a-549">The **dwReturn** member is set to the current block alignment used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-550"><span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>\_canales de \_ Estado de onda de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-550"><span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>MCI\_WAVE\_STATUS\_CHANNELS</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-551">El miembro **dwReturn** se establece en el número de canales actual usado para reproducir, grabar y guardar.</span><span class="sxs-lookup"><span data-stu-id="38c6a-551">The **dwReturn** member is set to the current channel count used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-552"><span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>\_nivel de \_ Estado de onda de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-552"><span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>MCI\_WAVE\_STATUS\_LEVEL</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-553">El miembro **dwReturn** se establece en el nivel de reproducción o registro actual de los datos con formato PCM.</span><span class="sxs-lookup"><span data-stu-id="38c6a-553">The **dwReturn** member is set to the current record or playback level of PCM formatted data.</span></span> <span data-ttu-id="38c6a-554">El valor se devuelve como un valor de 8 o 16 bits, dependiendo del tamaño de muestra utilizado.</span><span class="sxs-lookup"><span data-stu-id="38c6a-554">The value is returned as an 8- or 16-bit value, depending on the sample size used.</span></span> <span data-ttu-id="38c6a-555">El nivel de canal derecho o mono se devuelve en la palabra de orden inferior.</span><span class="sxs-lookup"><span data-stu-id="38c6a-555">The right or mono channel level is returned in the low-order word.</span></span> <span data-ttu-id="38c6a-556">El nivel de canal izquierdo se devuelve en la palabra de orden superior.</span><span class="sxs-lookup"><span data-stu-id="38c6a-556">The left channel level is returned in the high-order word.</span></span>

</dd> <dt>

<span data-ttu-id="38c6a-557"><span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>Estado de onda de MCI \_ \_ \_ SAMPLESPERSEC</span><span class="sxs-lookup"><span data-stu-id="38c6a-557"><span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>MCI\_WAVE\_STATUS\_SAMPLESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="38c6a-558">El miembro **dwReturn** se establece en las muestras actuales por segundo que se usan para reproducir, grabar y guardar.</span><span class="sxs-lookup"><span data-stu-id="38c6a-558">The **dwReturn** member is set to the current samples per second used for playing, recording, and saving.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38c6a-559">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38c6a-559">Requirements</span></span>



| <span data-ttu-id="38c6a-560">Requisito</span><span class="sxs-lookup"><span data-stu-id="38c6a-560">Requirement</span></span> | <span data-ttu-id="38c6a-561">Value</span><span class="sxs-lookup"><span data-stu-id="38c6a-561">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38c6a-562">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38c6a-562">Minimum supported client</span></span><br/> | <span data-ttu-id="38c6a-563">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="38c6a-563">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="38c6a-564">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38c6a-564">Minimum supported server</span></span><br/> | <span data-ttu-id="38c6a-565">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="38c6a-565">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="38c6a-566">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38c6a-566">Header</span></span><br/>                   | <dl> <span data-ttu-id="38c6a-567"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38c6a-567"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38c6a-568">Vea también</span><span class="sxs-lookup"><span data-stu-id="38c6a-568">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38c6a-569">MCI</span><span class="sxs-lookup"><span data-stu-id="38c6a-569">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="38c6a-570">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="38c6a-570">MCI Commands</span></span>](mci-commands.md)
</dt> <dt>

[<span data-ttu-id="38c6a-571">corte de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-571">MCI\_CUT</span></span>](mci-cut.md)
</dt> <dt>

[<span data-ttu-id="38c6a-572">eliminación de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-572">MCI\_DELETE</span></span>](mci-delete.md)
</dt> <dt>

[<span data-ttu-id="38c6a-573">\_pegar MCI</span><span class="sxs-lookup"><span data-stu-id="38c6a-573">MCI\_PASTE</span></span>](mci-paste.md)
</dt> <dt>

[<span data-ttu-id="38c6a-574">Reserva de MCI \_</span><span class="sxs-lookup"><span data-stu-id="38c6a-574">MCI\_RESERVE</span></span>](mci-reserve.md)
</dt> <dt>

[<span data-ttu-id="38c6a-575">MCI \_ set</span><span class="sxs-lookup"><span data-stu-id="38c6a-575">MCI\_SET</span></span>](mci-set.md)
</dt> <dt>

[<span data-ttu-id="38c6a-576">reproducción</span><span class="sxs-lookup"><span data-stu-id="38c6a-576">play</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="38c6a-577">record</span><span class="sxs-lookup"><span data-stu-id="38c6a-577">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="38c6a-578">desean</span><span class="sxs-lookup"><span data-stu-id="38c6a-578">seek</span></span>](seek.md)
</dt> </dl>

 

