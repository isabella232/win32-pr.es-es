---
title: Comando MCI_GETDEVCAPS (mmsystem. h)
description: El \_ comando MCI GETDEVCAPS recupera información estática sobre un dispositivo.
ms.assetid: a839006f-ea57-4595-9208-cfc465c95298
keywords:
- Comando de MCI_GETDEVCAPS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85abb0354d36979741d0b292dd9def469cec0049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535428"
---
# <a name="mci_getdevcaps-command"></a><span data-ttu-id="89085-104">\_Comando MCI GETDEVCAPS</span><span class="sxs-lookup"><span data-stu-id="89085-104">MCI\_GETDEVCAPS command</span></span>

<span data-ttu-id="89085-105">El \_ comando MCI GETDEVCAPS recupera información estática sobre un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="89085-105">The MCI\_GETDEVCAPS command retrieves static information about a device.</span></span> <span data-ttu-id="89085-106">Todos los dispositivos reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="89085-106">All devices recognize this command.</span></span> <span data-ttu-id="89085-107">Los parámetros y las marcas disponibles para este comando dependen del dispositivo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="89085-107">The parameters and flags available for this command depend on the selected device.</span></span> <span data-ttu-id="89085-108">La información se devuelve en el miembro **dwReturn** de la estructura identificada por *lpCapsParms*.</span><span class="sxs-lookup"><span data-stu-id="89085-108">Information is returned in the **dwReturn** member of the structure identified by *lpCapsParms*.</span></span>

<span data-ttu-id="89085-109">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="89085-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_GETDEVCAPS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GETDEVCAPS_PARMS) lpCapsParms
);
```



## <a name="parameters"></a><span data-ttu-id="89085-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89085-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89085-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="89085-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="89085-112">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="89085-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="89085-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="89085-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="89085-114">MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="89085-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="89085-115">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="89085-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="89085-116"><span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpCapsParms*</span><span class="sxs-lookup"><span data-stu-id="89085-116"><span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpCapsParms*</span></span>
</dt> <dd>

<span data-ttu-id="89085-117">Puntero a una [**estructura \_ GETDEVCAPS de \_ parms de MCI**](mci-getdevcaps-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="89085-117">Pointer to an [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89085-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89085-118">Return Value</span></span>

<span data-ttu-id="89085-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="89085-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="89085-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89085-120">Remarks</span></span>

<span data-ttu-id="89085-121">Las siguientes marcas estándar y específicas del comando adicionales se aplican a todos los dispositivos que admiten MCI \_ GETDEVCAPS:</span><span class="sxs-lookup"><span data-stu-id="89085-121">The following additional standard and command-specific flags apply to all devices supporting MCI\_GETDEVCAPS:</span></span>

<dl> <dt>

<span data-ttu-id="89085-122"><span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>\_ \_ dispositivo compuesto MCI \_ GETDEVCAPS</span><span class="sxs-lookup"><span data-stu-id="89085-122"><span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>MCI\_GETDEVCAPS\_COMPOUND\_DEVICE</span></span>
</dt> <dd>

<span data-ttu-id="89085-123">El miembro **dwReturn** se establece en **true** si el dispositivo usa almacenamiento de datos que se debe abrir y cerrar explícitamente; en caso contrario, se establece en **false** .</span><span class="sxs-lookup"><span data-stu-id="89085-123">The **dwReturn** member is set to **TRUE** if the device uses data storage that must be explicitly opened and closed; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="89085-124"><span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>\_tipo de \_ dispositivo MCI GETDEVCAPS \_</span><span class="sxs-lookup"><span data-stu-id="89085-124"><span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>MCI\_GETDEVCAPS\_DEVICE\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="89085-125">El miembro **dwReturn** se establece en uno de los valores enumerados en [tipos de dispositivo MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="89085-125">The **dwReturn** member is set to one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="89085-126"><span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>MCI \_ GETDEVCAPS \_ tiene \_ audio</span><span class="sxs-lookup"><span data-stu-id="89085-126"><span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>MCI\_GETDEVCAPS\_HAS\_AUDIO</span></span>
</dt> <dd>

<span data-ttu-id="89085-127">El miembro **dwReturn** se establece en **true** si el dispositivo tiene salida de audio; en caso contrario, se establece en **false** .</span><span class="sxs-lookup"><span data-stu-id="89085-127">The **dwReturn** member is set to **TRUE** if the device has audio output; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="89085-128"><span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI \_ GETDEVCAPS \_ tiene \_ vídeo</span><span class="sxs-lookup"><span data-stu-id="89085-128"><span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI\_GETDEVCAPS\_HAS\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="89085-129">El miembro **dwReturn** se establece en **true** si el dispositivo tiene salida de vídeo. en caso contrario, se establece en **false** .</span><span class="sxs-lookup"><span data-stu-id="89085-129">The **dwReturn** member is set to **TRUE** if the device has video output; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="89085-130">Por ejemplo, el miembro se establece en **true** para los dispositivos que admiten el conjunto de comandos VideoDisc.</span><span class="sxs-lookup"><span data-stu-id="89085-130">For example, the member is set to **TRUE** for devices that support the videodisc command set.</span></span>

</dd> <dt>

<span data-ttu-id="89085-131"><span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>\_elemento GETDEVCAPS de MCI \_</span><span class="sxs-lookup"><span data-stu-id="89085-131"><span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>MCI\_GETDEVCAPS\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="89085-132">Especifica que el miembro **dwItem** de la [**estructura \_ \_ parms de MCI GETDEVCAPS**](mci-getdevcaps-parms.md) contiene una de las constantes siguientes:</span><span class="sxs-lookup"><span data-stu-id="89085-132">Specifies that the **dwItem** member of the [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) structure contains one of the following constants:</span></span>

</dd> <dt>

<span data-ttu-id="89085-133"><span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>MCI \_ GETDEVCAPS se \_ puede \_ expulsar</span><span class="sxs-lookup"><span data-stu-id="89085-133"><span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>MCI\_GETDEVCAPS\_CAN\_EJECT</span></span>
</dt> <dd>

<span data-ttu-id="89085-134">El miembro **dwReturn** se establece en **true** si el dispositivo puede expulsar el medio; de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-134">The **dwReturn** member is set to **TRUE** if the device can eject the media; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89085-135"><span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>se \_ \_ puede \_ reproducir MCI GETDEVCAPS</span><span class="sxs-lookup"><span data-stu-id="89085-135"><span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>MCI\_GETDEVCAPS\_CAN\_PLAY</span></span>
</dt> <dd>

<span data-ttu-id="89085-136">El miembro **dwReturn** se establece en **true** si el dispositivo puede reproducir el medio; de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-136">The **dwReturn** member is set to **TRUE** if the device can play the media; otherwise, it is set to **FALSE**.</span></span> <span data-ttu-id="89085-137">Si un dispositivo especifica **true**, significa que el dispositivo es compatible con los comandos [de \_ detención](mci-stop.md) de [ \_ MCI y](mci-pause.md) MCI, así como con el comando de [ \_ reproducción de MCI](mci-play.md) .</span><span class="sxs-lookup"><span data-stu-id="89085-137">If a device specifies **TRUE**, it implies the device supports the [MCI\_PAUSE](mci-pause.md) and [MCI\_STOP](mci-stop.md) commands as well as the [MCI\_PLAY](mci-play.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="89085-138"><span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>\_ \_ puede grabar GETDEVCAPS \_ de MCI</span><span class="sxs-lookup"><span data-stu-id="89085-138"><span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>MCI\_GETDEVCAPS\_CAN\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="89085-139">El miembro **dwReturn** se establece en **true** si el dispositivo admite la grabación; de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-139">The **dwReturn** member is set to **TRUE** if the device supports recording; otherwise, it is set to **FALSE**.</span></span> <span data-ttu-id="89085-140">Si un dispositivo especifica **true**, significa que el dispositivo es compatible con los \_ comandos MCI PAUSE y MCI STOP, así \_ como con el comando [MCI \_ Record](mci-record.md) .</span><span class="sxs-lookup"><span data-stu-id="89085-140">If a device specifies **TRUE**, it implies the device supports the MCI\_PAUSE and MCI\_STOP commands as well as the [MCI\_RECORD](mci-record.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="89085-141"><span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>MCI \_ GETDEVCAPS \_ puede \_ Guardar</span><span class="sxs-lookup"><span data-stu-id="89085-141"><span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>MCI\_GETDEVCAPS\_CAN\_SAVE</span></span>
</dt> <dd>

<span data-ttu-id="89085-142">El miembro **dwReturn** se establece en **true** si el dispositivo puede guardar un archivo; de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-142">The **dwReturn** member is set to **TRUE** if the device can save a file; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89085-143"><span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI \_ GETDEVCAPS \_ usa \_ archivos</span><span class="sxs-lookup"><span data-stu-id="89085-143"><span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI\_GETDEVCAPS\_USES\_FILES</span></span>
</dt> <dd>

<span data-ttu-id="89085-144">El miembro **dwReturn** se establece en **true** si el dispositivo requiere un nombre de archivo; en caso contrario, se establece en **false** .</span><span class="sxs-lookup"><span data-stu-id="89085-144">The **dwReturn** member is set to **TRUE** if the device requires a filename; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="89085-145">Solo los dispositivos compuestos usan archivos.</span><span class="sxs-lookup"><span data-stu-id="89085-145">Only compound devices use files.</span></span>

</dd> </dl>

<span data-ttu-id="89085-146">Se pueden especificar las marcas siguientes en el miembro **dwItem** de [**MCI \_ GETDEVCAPS \_ parms**](mci-getdevcaps-parms.md) para el tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="89085-146">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="89085-147"><span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI \_ DGV \_ GETDEVCAPS se \_ puede \_ inmovilizar</span><span class="sxs-lookup"><span data-stu-id="89085-147"><span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_FREEZE</span></span>
</dt> <dd>

<span data-ttu-id="89085-148">El miembro **dwReturn** se establece en **true** si el dispositivo puede inmovilizar fotogramas; de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-148">The **dwReturn** member is set to **TRUE** if the device can freeze frames; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89085-149"><span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>MCI \_ DGV \_ GETDEVCAPS \_ puede \_ bloquear</span><span class="sxs-lookup"><span data-stu-id="89085-149"><span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_LOCK</span></span>
</dt> <dd>

<span data-ttu-id="89085-150">El miembro **dwReturn** se establece en **true** si el dispositivo puede bloquearse; de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-150">The **dwReturn** member is set to **TRUE** if the device can lock; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89085-151"><span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>MCI \_ DGV \_ GETDEVCAPS \_ puede \_ invertir</span><span class="sxs-lookup"><span data-stu-id="89085-151"><span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="89085-152">El miembro **dwReturn** se establece en **true** si el dispositivo puede reproducirse en orden inverso; de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-152">The **dwReturn** member is set to **TRUE** if the device can play in reverse; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89085-153"><span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI \_ DGV \_ GETDEVCAPS \_ puede \_ Str \_</span><span class="sxs-lookup"><span data-stu-id="89085-153"><span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_STR\_IN</span></span>
</dt> <dd>

<span data-ttu-id="89085-154">El miembro **dwReturn** se establece en **true** si el dispositivo puede ajustar la entrada; de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-154">The **dwReturn** member is set to **TRUE** if the device can stretch input; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89085-155"><span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>MCI \_ DGV \_ GETDEVCAPS \_ puede \_ ajustarse</span><span class="sxs-lookup"><span data-stu-id="89085-155"><span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="89085-156">El miembro **dwReturn** se establece en **true** si el dispositivo puede ajustar una imagen; de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-156">The **dwReturn** member is set to **TRUE** if the device can stretch an image; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89085-157"><span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>MCI \_ DGV \_ GETDEVCAPS \_ puede \_ probar</span><span class="sxs-lookup"><span data-stu-id="89085-157"><span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_TEST</span></span>
</dt> <dd>

<span data-ttu-id="89085-158">El miembro **dwReturn** se establece en **true** si el dispositivo puede realizar pruebas; de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-158">The **dwReturn** member is set to **TRUE** if the device can perform tests; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89085-159"><span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI \_ DGV \_ GETDEVCAPS \_ \_ todavía</span><span class="sxs-lookup"><span data-stu-id="89085-159"><span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI\_DGV\_GETDEVCAPS\_HAS\_STILL</span></span>
</dt> <dd>

<span data-ttu-id="89085-160">El miembro **dwReturn** se establece en **true** si el dispositivo puede mostrar imágenes fijas; de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-160">The **dwReturn** member is set to **TRUE** if the device can display still images; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89085-161"><span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>MCI \_ DGV \_ GETDEVCAPS \_ Max \_ Windows</span><span class="sxs-lookup"><span data-stu-id="89085-161"><span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>MCI\_DGV\_GETDEVCAPS\_MAX\_WINDOWS</span></span>
</dt> <dd>

<span data-ttu-id="89085-162">El miembro **dwReturn** se establece en el número máximo de ventanas que el dispositivo puede controlar simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="89085-162">The **dwReturn** member is set to the maximum number of windows that the device can handle simultaneously.</span></span>

</dd> <dt>

<span data-ttu-id="89085-163"><span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>\_ \_ \_ velocidad máxima de DGV de MCI GETDEVCAPS \_</span><span class="sxs-lookup"><span data-stu-id="89085-163"><span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>MCI\_DGV\_GETDEVCAPS\_MAXIMUM\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="89085-164">El miembro **dwReturn** se establece en la velocidad máxima de reproducción del dispositivo, en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="89085-164">The **dwReturn** member is set to the maximum play rate for the device, in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="89085-165"><span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>\_ \_ \_ tasa mínima de DGV de MCI GETDEVCAPS \_</span><span class="sxs-lookup"><span data-stu-id="89085-165"><span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>MCI\_DGV\_GETDEVCAPS\_MINIMUM\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="89085-166">El miembro **dwReturn** se establece en la velocidad de reproducción mínima del dispositivo, en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="89085-166">The **dwReturn** member is set to the minimum play rate for the device, in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="89085-167"><span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>\_ \_ paletas de GETDEVCAPS DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="89085-167"><span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>MCI\_DGV\_GETDEVCAPS\_PALETTES</span></span>
</dt> <dd>

<span data-ttu-id="89085-168">El miembro **dwReturn** se establece en **true** si el dispositivo puede devolver un identificador de paleta; de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-168">The **dwReturn** member is set to **TRUE** if the device can return a palette handle; otherwise, it is set to **FALSE**.</span></span>

</dd> </dl>

<span data-ttu-id="89085-169">Se pueden especificar las marcas siguientes en el miembro **dwItem** de [**MCI \_ GETDEVCAPS \_ parms**](mci-getdevcaps-parms.md) para el tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="89085-169">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="89085-170"><span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>\_velocidad de \_ incremento de reloj de GETDEVCAPS de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="89085-170"><span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>MCI\_GETDEVCAPS\_CLOCK\_INCREMENT\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="89085-171">El miembro **dwReturn** se establece en el número de incrementos por segundo.</span><span class="sxs-lookup"><span data-stu-id="89085-171">The **dwReturn** member is set to the number of increments per second.</span></span>

</dd> <dt>

<span data-ttu-id="89085-172"><span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>MCI \_ VCR \_ GETDEVCAPS \_ puede \_ detectar \_ longitud</span><span class="sxs-lookup"><span data-stu-id="89085-172"><span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_DETECT\_LENGTH</span></span>
</dt> <dd>

<span data-ttu-id="89085-173">El miembro **dwReturn** se establece en **true** si el dispositivo es capaz de detectar la longitud del medio. de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-173">The **dwReturn** member is set to **TRUE** if the device is capable of detecting the length of the media; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89085-174"><span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>MCI \_ VCR \_ GETDEVCAPS \_ puede \_ congelarse</span><span class="sxs-lookup"><span data-stu-id="89085-174"><span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_FREEZE</span></span>
</dt> <dd>

<span data-ttu-id="89085-175">El miembro **dwReturn** se establece en **true** si el dispositivo es capaz de inmovilizar la imagen de salida; de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-175">The **dwReturn** member is set to **TRUE** if the device is capable of freezing the output image; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89085-176"><span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>MCI \_ VCR \_ GETDEVCAPS \_ puede \_ supervisar \_ orígenes</span><span class="sxs-lookup"><span data-stu-id="89085-176"><span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_MONITOR\_SOURCES</span></span>
</dt> <dd>

<span data-ttu-id="89085-177">El miembro **dwReturn** se establece en **true** si el dispositivo es capaz de supervisar los orígenes; de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-177">The **dwReturn** member is set to **TRUE** if the device is capable of monitoring sources; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89085-178"><span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>MCI \_ VCR \_ GETDEVCAPS \_ puede \_ prevertir</span><span class="sxs-lookup"><span data-stu-id="89085-178"><span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_PREROLL</span></span>
</dt> <dd>

<span data-ttu-id="89085-179">El miembro **dwReturn** se establece en **true** si el dispositivo es capaz de prehacer; de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-179">The **dwReturn** member is set to **TRUE** if the device is capable of preroll; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89085-180"><span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>MCI \_ VCR \_ GETDEVCAPS \_ puede \_ obtener una vista previa</span><span class="sxs-lookup"><span data-stu-id="89085-180"><span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_PREVIEW</span></span>
</dt> <dd>

<span data-ttu-id="89085-181">El miembro **dwReturn** se establece en **true** si el dispositivo es capaz de obtener vistas previas; de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-181">The **dwReturn** member is set to **TRUE** if the device is capable of previews; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89085-182"><span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>MCI \_ VCR \_ GETDEVCAPS \_ puede \_ invertir</span><span class="sxs-lookup"><span data-stu-id="89085-182"><span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="89085-183">El miembro **dwReturn** se establece en **true** si el dispositivo es capaz de reproducirse en orden inverso; de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-183">The **dwReturn** member is set to **TRUE** if the device is capable of playing in reverse; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89085-184"><span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>MCI \_ VCR \_ GETDEVCAPS \_ puede \_ probar</span><span class="sxs-lookup"><span data-stu-id="89085-184"><span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_TEST</span></span>
</dt> <dd>

<span data-ttu-id="89085-185">El miembro **dwReturn** se establece en **true** si el dispositivo es capaz de realizar pruebas; de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-185">The **dwReturn** member is set to **TRUE** if the device is capable of testing; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89085-186"><span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>MCI \_ VCR \_ GETDEVCAPS \_ tiene \_ reloj</span><span class="sxs-lookup"><span data-stu-id="89085-186"><span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>MCI\_VCR\_GETDEVCAPS\_HAS\_CLOCK</span></span>
</dt> <dd>

<span data-ttu-id="89085-187">El miembro **dwReturn** se establece en **true** si el dispositivo admite un reloj externo; de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-187">The **dwReturn** member is set to **TRUE** if the device supports an external clock; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89085-188"><span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>MCI \_ VCR \_ GETDEVCAPS \_ tiene \_ código de tiempo</span><span class="sxs-lookup"><span data-stu-id="89085-188"><span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>MCI\_VCR\_GETDEVCAPS\_HAS\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="89085-189">El miembro **dwReturn** se establece en **true** si el dispositivo tiene capacidad de código de tiempo o si esta funcionalidad es desconocida. de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-189">The **dwReturn** member is set to **TRUE** if device has timecode capability or if this capability is unknown; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89085-190"><span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>\_ \_ GETDEVCAPS de vídeo MCI \_ número \_ de \_ marcas</span><span class="sxs-lookup"><span data-stu-id="89085-190"><span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>MCI\_VCR\_GETDEVCAPS\_NUMBER\_OF\_MARKS</span></span>
</dt> <dd>

<span data-ttu-id="89085-191">El miembro **dwReturn** se establece en el número de marcas (99).</span><span class="sxs-lookup"><span data-stu-id="89085-191">The **dwReturn** member is set to the number of marks (99).</span></span>

</dd> <dt>

<span data-ttu-id="89085-192"><span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>\_precisión de búsqueda de VCR VCR \_ GETDEVCAPS \_ \_</span><span class="sxs-lookup"><span data-stu-id="89085-192"><span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>MCI\_VCR\_GETDEVCAPS\_SEEK\_ACCURACY</span></span>
</dt> <dd>

<span data-ttu-id="89085-193">El miembro **dwReturn** se establece en la precisión de búsqueda del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="89085-193">The **dwReturn** member is set to the seek accuracy of the device.</span></span>

</dd> </dl>

<span data-ttu-id="89085-194">Se pueden especificar las marcas siguientes en el miembro **dwItem** de [**MCI \_ GETDEVCAPS \_ parms**](mci-getdevcaps-parms.md) para el tipo de dispositivo **superpuesto** :</span><span class="sxs-lookup"><span data-stu-id="89085-194">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="89085-195"><span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>MCI \_ OVLY \_ GETDEVCAPS se \_ puede \_ inmovilizar</span><span class="sxs-lookup"><span data-stu-id="89085-195"><span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>MCI\_OVLY\_GETDEVCAPS\_CAN\_FREEZE</span></span>
</dt> <dd>

<span data-ttu-id="89085-196">El miembro **dwReturn** se establece en **true** si el dispositivo puede inmovilizar la imagen; de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-196">The **dwReturn** member is set to **TRUE** if the device can freeze the image; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89085-197"><span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>MCI \_ OVLY \_ GETDEVCAPS \_ puede \_ ajustarse</span><span class="sxs-lookup"><span data-stu-id="89085-197"><span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>MCI\_OVLY\_GETDEVCAPS\_CAN\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="89085-198">El miembro **dwReturn** se establece en **true** si el dispositivo puede ajustar la imagen para rellenar el fotograma. de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-198">The **dwReturn** member is set to **TRUE** if the device can stretch the image to fill the frame; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89085-199"><span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>MCI \_ OVLY \_ GETDEVCAPS \_ Max \_ Windows</span><span class="sxs-lookup"><span data-stu-id="89085-199"><span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>MCI\_OVLY\_GETDEVCAPS\_MAX\_WINDOWS</span></span>
</dt> <dd>

<span data-ttu-id="89085-200">El miembro **dwReturn** se establece en el número máximo de ventanas que el dispositivo puede controlar simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="89085-200">The **dwReturn** member is set to the maximum number of windows that the device can handle simultaneously.</span></span>

</dd> </dl>

<span data-ttu-id="89085-201">Se pueden especificar las marcas siguientes en el miembro **dwItem** de [**MCI \_ GETDEVCAPS \_ parms**](mci-getdevcaps-parms.md) para el tipo de dispositivo de **videodisco** :</span><span class="sxs-lookup"><span data-stu-id="89085-201">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="89085-202"><span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>MCI \_ Vd \_ GETDEVCAPS \_ puede \_ invertir</span><span class="sxs-lookup"><span data-stu-id="89085-202"><span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>MCI\_VD\_GETDEVCAPS\_CAN\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="89085-203">El miembro **dwReturn** se establece en **true** si el reproductor de CD puede reproducirse en orden inverso; de lo contrario, se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="89085-203">The **dwReturn** member is set to **TRUE** if the videodisc player can play in reverse; otherwise, it is set to **FALSE**.</span></span> <span data-ttu-id="89085-204">Algunos jugadores pueden reproducir discos CLV en discos inversos y CAV.</span><span class="sxs-lookup"><span data-stu-id="89085-204">Some players can play CLV discs in reverse as well as CAV discs.</span></span>

</dd> <dt>

<span data-ttu-id="89085-205"><span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI \_ Vd \_ GETDEVCAPS \_ CAV</span><span class="sxs-lookup"><span data-stu-id="89085-205"><span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI\_VD\_GETDEVCAPS\_CAV</span></span>
</dt> <dd>

<span data-ttu-id="89085-206">Cuando se combina con otros elementos, especifica que la información de devolución se aplica al formato de CAV de videodisco.</span><span class="sxs-lookup"><span data-stu-id="89085-206">When combined with other items, specifies that the return information applies to CAV format videodiscs.</span></span> <span data-ttu-id="89085-207">Este es el valor predeterminado si no se inserta ningún CD.</span><span class="sxs-lookup"><span data-stu-id="89085-207">This is the default if no videodisc is inserted.</span></span>

</dd> <dt>

<span data-ttu-id="89085-208"><span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI \_ Vd \_ GETDEVCAPS \_ CLV</span><span class="sxs-lookup"><span data-stu-id="89085-208"><span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI\_VD\_GETDEVCAPS\_CLV</span></span>
</dt> <dd>

<span data-ttu-id="89085-209">Cuando se combina con otros elementos, especifica que la información de devolución se aplica al formato de CLV de videodisco.</span><span class="sxs-lookup"><span data-stu-id="89085-209">When combined with other items, specifies that the return information applies to CLV format videodiscs.</span></span>

</dd> <dt>

<span data-ttu-id="89085-210"><span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>\_ \_ \_ tasa rápida de GETDEVCAPS \_ de MCI Vd</span><span class="sxs-lookup"><span data-stu-id="89085-210"><span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>MCI\_VD\_GETDEVCAPS\_FAST\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="89085-211">El miembro **dwReturn** se establece en la velocidad de reproducción rápida estándar en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="89085-211">The **dwReturn** member is set to the standard fast play rate in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="89085-212"><span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>tasa normal de MCI \_ Vd \_ GETDEVCAPS \_ \_</span><span class="sxs-lookup"><span data-stu-id="89085-212"><span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>MCI\_VD\_GETDEVCAPS\_NORMAL\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="89085-213">El miembro **dwReturn** se establece en la velocidad de reproducción normal en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="89085-213">The **dwReturn** member is set to the normal play rate in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="89085-214"><span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>velocidad lenta de MCI \_ Vd \_ GETDEVCAPS \_ \_</span><span class="sxs-lookup"><span data-stu-id="89085-214"><span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>MCI\_VD\_GETDEVCAPS\_SLOW\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="89085-215">El miembro **dwReturn** se establece en la velocidad de reproducción lenta estándar en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="89085-215">The **dwReturn** member is set to the standard slow play rate in frames per second.</span></span>

</dd> </dl>

<span data-ttu-id="89085-216">Se pueden especificar las marcas siguientes en el miembro **dwItem** de [**MCI \_ GETDEVCAPS \_ parms**](mci-getdevcaps-parms.md) para el tipo de dispositivo **WaveAudio** :</span><span class="sxs-lookup"><span data-stu-id="89085-216">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="89085-217"><span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>\_ \_ entrada GETDEVCAPS de onda de MCI \_</span><span class="sxs-lookup"><span data-stu-id="89085-217"><span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>MCI\_WAVE\_GETDEVCAPS\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="89085-218">El miembro **dwReturn** se establece en el número total de dispositivos de entrada de onda (grabación).</span><span class="sxs-lookup"><span data-stu-id="89085-218">The **dwReturn** member is set to the total number of waveform input (recording) devices.</span></span>

</dd> <dt>

<span data-ttu-id="89085-219"><span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>salida de MCI \_ Wave \_ GETDEVCAPS \_</span><span class="sxs-lookup"><span data-stu-id="89085-219"><span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>MCI\_WAVE\_GETDEVCAPS\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="89085-220">El miembro **dwReturn** se establece en el número total de dispositivos de salida de forma de onda (reproducción).</span><span class="sxs-lookup"><span data-stu-id="89085-220">The **dwReturn** member is set to the total number of waveform output (playback) devices.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89085-221">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89085-221">Requirements</span></span>



| <span data-ttu-id="89085-222">Requisito</span><span class="sxs-lookup"><span data-stu-id="89085-222">Requirement</span></span> | <span data-ttu-id="89085-223">Value</span><span class="sxs-lookup"><span data-stu-id="89085-223">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89085-224">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89085-224">Minimum supported client</span></span><br/> | <span data-ttu-id="89085-225">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="89085-225">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="89085-226">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89085-226">Minimum supported server</span></span><br/> | <span data-ttu-id="89085-227">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="89085-227">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="89085-228">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89085-228">Header</span></span><br/>                   | <dl> <span data-ttu-id="89085-229"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89085-229"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89085-230">Vea también</span><span class="sxs-lookup"><span data-stu-id="89085-230">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89085-231">MCI</span><span class="sxs-lookup"><span data-stu-id="89085-231">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="89085-232">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="89085-232">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

