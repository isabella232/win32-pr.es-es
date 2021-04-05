---
title: Comando MCI_RESERVE (mmsystem. h)
description: El \_ comando reserva de MCI asigna espacio en disco contiguo para el área de trabajo de la instancia de controlador de dispositivo para su uso con grabaciones posteriores. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 01f0a377-0179-4b05-a642-af152a7a12ae
keywords:
- Comando de MCI_RESERVE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_RESERVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b89eb457b63012aa9ee5624efef95945258d42c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996858"
---
# <a name="mci_reserve-command"></a><span data-ttu-id="7f4de-105">\_Comando reserva de MCI</span><span class="sxs-lookup"><span data-stu-id="7f4de-105">MCI\_RESERVE command</span></span>

<span data-ttu-id="7f4de-106">El \_ comando reserva de MCI asigna espacio en disco contiguo para el área de trabajo de la instancia de controlador de dispositivo para su uso con grabaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="7f4de-106">The MCI\_RESERVE command allocates contiguous disk space for the workspace of the device driver instance for use with subsequent recording.</span></span> <span data-ttu-id="7f4de-107">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="7f4de-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="7f4de-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="7f4de-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESERVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESERVE_PARMS) lpReserve
);
```



## <a name="parameters"></a><span data-ttu-id="7f4de-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f4de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f4de-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="7f4de-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="7f4de-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="7f4de-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="7f4de-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="7f4de-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="7f4de-113">\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI.</span><span class="sxs-lookup"><span data-stu-id="7f4de-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="7f4de-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="7f4de-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f4de-115"><span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpReserve*</span><span class="sxs-lookup"><span data-stu-id="7f4de-115"><span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpReserve*</span></span>
</dt> <dd>

<span data-ttu-id="7f4de-116">Puntero a una estructura de [**parms de DGV de MCI \_ \_ reservada \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="7f4de-116">Pointer to an [**MCI\_DGV\_RESERVE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f4de-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f4de-117">Return Value</span></span>

<span data-ttu-id="7f4de-118">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7f4de-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f4de-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f4de-119">Remarks</span></span>

<span data-ttu-id="7f4de-120">Si el área de trabajo contiene datos no guardados, estos datos se perderán.</span><span class="sxs-lookup"><span data-stu-id="7f4de-120">If the workspace contains unsaved data, this data is lost.</span></span> <span data-ttu-id="7f4de-121">Si no se reserva espacio en disco antes de la grabación, el comando [MCI \_ Record](mci-record.md) realiza una reserva implícita con parámetros predeterminados específicos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f4de-121">If disk space is not reserved prior to recording, the [MCI\_RECORD](mci-record.md) command performs an implied reserve with device-specific default parameters.</span></span> <span data-ttu-id="7f4de-122">En algunas implementaciones, no es necesario reservar y el controlador del dispositivo puede omitirla.</span><span class="sxs-lookup"><span data-stu-id="7f4de-122">On some implementations, reserve is not required and might be ignored by the device driver.</span></span> <span data-ttu-id="7f4de-123">El espacio de reserva explícita proporciona un mejor control sobre cuándo se produce el retraso de la asignación de disco, cuánto espacio se asigna y dónde se asigna el espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="7f4de-123">Explicitly reserving space gives you better control over when the delay for disk allocation occurs, how much space is allocated, and where the disk space is allocated.</span></span> <span data-ttu-id="7f4de-124">La cantidad y la ubicación del espacio en disco que ya está reservada para esta instancia de dispositivo se pueden cambiar emitiendo la reserva de MCI de \_ nuevo.</span><span class="sxs-lookup"><span data-stu-id="7f4de-124">The amount and location of disk space already reserved for this device instance can be changed by issuing MCI\_RESERVE again.</span></span> <span data-ttu-id="7f4de-125">Cualquier espacio en disco asignado y todavía sin usar no se cancela hasta que se guardan los datos grabados o hasta que se cierra la instancia del controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f4de-125">Any allocated and still unused disk space is not deallocated until any recorded data is saved or until the device driver instance is closed.</span></span>

<span data-ttu-id="7f4de-126">Si el vídeo está desactivado con la \_ marca MCI OFF del comando [MCI \_ SETVIDEO](mci-setvideo.md) , el espacio reservado no incluye ningún vídeo.</span><span class="sxs-lookup"><span data-stu-id="7f4de-126">If video is turned off with the MCI\_OFF flag of the [MCI\_SETVIDEO](mci-setvideo.md) command, the space reserved does not include any video.</span></span> <span data-ttu-id="7f4de-127">Si el audio está desactivado con la \_ marca MCI OFF del comando [MCI \_ SETAUDIO](mci-setaudio.md) , el espacio reservado no incluye audio.</span><span class="sxs-lookup"><span data-stu-id="7f4de-127">If audio is turned off with the MCI\_OFF flag of the [MCI\_SETAUDIO](mci-setaudio.md) command, the space reserved does not include any audio.</span></span> <span data-ttu-id="7f4de-128">Si el audio y el vídeo están desactivados o si el tamaño solicitado es cero, no se reserva ningún espacio y se cancela la asignación de cualquier espacio reservado existente.</span><span class="sxs-lookup"><span data-stu-id="7f4de-128">If both audio and video are turned off or if the requested size is zero, no space is reserved and any existing reserved space is deallocated.</span></span>

<span data-ttu-id="7f4de-129">Las siguientes marcas adicionales se aplican a los dispositivos de vídeo digital:</span><span class="sxs-lookup"><span data-stu-id="7f4de-129">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="7f4de-130"><span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>\_ \_ reserva de MCI DGV \_ en</span><span class="sxs-lookup"><span data-stu-id="7f4de-130"><span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>MCI\_DGV\_RESERVE\_IN</span></span>
</dt> <dd>

<span data-ttu-id="7f4de-131">El miembro **lpstrPath** de la estructura identificada por *lpReserve* contiene una dirección de un búfer que contiene la ubicación de un archivo temporal.</span><span class="sxs-lookup"><span data-stu-id="7f4de-131">The **lpstrPath** member of the structure identified by *lpReserve* contains an address of a buffer containing the location of a temporary file.</span></span> <span data-ttu-id="7f4de-132">El búfer contiene solo la unidad y la ruta de acceso al directorio del archivo utilizado para almacenar los datos registrados; el nombre de archivo lo especifica el controlador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f4de-132">The buffer contains only the drive and directory path of the file used to hold recorded data; the filename is specified by the device driver.</span></span> <span data-ttu-id="7f4de-133">Este archivo temporal se elimina cuando se cierra la instancia del dispositivo a menos que se guarde explícitamente.</span><span class="sxs-lookup"><span data-stu-id="7f4de-133">This temporary file is deleted when the device instance is closed unless it is explicitly saved.</span></span> <span data-ttu-id="7f4de-134">Si se omite esta marca, el controlador de dispositivo especifica dónde se asigna espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="7f4de-134">If this flag is omitted, the device driver specifies where disk space is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="7f4de-135"><span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>tamaño de reserva de MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="7f4de-135"><span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>MCI\_DGV\_RESERVE\_SIZE</span></span>
</dt> <dd>

<span data-ttu-id="7f4de-136">El miembro **dwSize** de la estructura identificada por *lpReserve* especifica la cantidad aproximada de espacio en disco que se va a reservar en el área de trabajo para la grabación.</span><span class="sxs-lookup"><span data-stu-id="7f4de-136">The **dwSize** member of the structure identified by *lpReserve* specifies the approximate amount of disk space to reserve in the workspace for recording.</span></span> <span data-ttu-id="7f4de-137">El valor se especifica en el formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="7f4de-137">The value is specified in the current time format.</span></span> <span data-ttu-id="7f4de-138">La cantidad de espacio en disco se calcula a partir de la hora solicitada y desde la que el formato de archivo y el algoritmo de audio y vídeo y los valores de calidad están en vigor.</span><span class="sxs-lookup"><span data-stu-id="7f4de-138">The amount of disk space is estimated from the requested time and from which file format and video and audio algorithm and quality values are in effect.</span></span> <span data-ttu-id="7f4de-139">Si se omite esta marca, el controlador de dispositivo podría usar un valor predeterminado que defina.</span><span class="sxs-lookup"><span data-stu-id="7f4de-139">If this flag is omitted, the device driver might use a default value it defines.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7f4de-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f4de-140">Requirements</span></span>



| <span data-ttu-id="7f4de-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f4de-141">Requirement</span></span> | <span data-ttu-id="7f4de-142">Value</span><span class="sxs-lookup"><span data-stu-id="7f4de-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f4de-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f4de-143">Minimum supported client</span></span><br/> | <span data-ttu-id="7f4de-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7f4de-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7f4de-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f4de-145">Minimum supported server</span></span><br/> | <span data-ttu-id="7f4de-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7f4de-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7f4de-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f4de-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f4de-148"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f4de-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f4de-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f4de-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f4de-150">MCI</span><span class="sxs-lookup"><span data-stu-id="7f4de-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7f4de-151">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="7f4de-151">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

