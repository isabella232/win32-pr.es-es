---
title: Comando MCI_OPEN (mmsystem. h)
description: El \_ comando MCI Open Inicializa un dispositivo o un archivo. Todos los dispositivos reconocen este comando.
ms.assetid: e2ee92b5-b10b-4408-950e-3002fe775b25
keywords:
- Comando de MCI_OPEN de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d8b33e70a2e061b54260aeffc6e69432c469f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103904980"
---
# <a name="mci_open-command"></a><span data-ttu-id="98621-105">\_Comando MCI Open</span><span class="sxs-lookup"><span data-stu-id="98621-105">MCI\_OPEN command</span></span>

<span data-ttu-id="98621-106">El \_ comando MCI Open Inicializa un dispositivo o un archivo.</span><span class="sxs-lookup"><span data-stu-id="98621-106">The MCI\_OPEN command initializes a device or file.</span></span> <span data-ttu-id="98621-107">Todos los dispositivos reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="98621-107">All devices recognize this command.</span></span>

<span data-ttu-id="98621-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="98621-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_OPEN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_OPEN_PARMS) lpOpen
);
```



## <a name="parameters"></a><span data-ttu-id="98621-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98621-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98621-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="98621-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="98621-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="98621-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="98621-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="98621-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="98621-113">\_Notificación de MCI o \_ espera de MCI.</span><span class="sxs-lookup"><span data-stu-id="98621-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="98621-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="98621-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="98621-115"><span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpOpen*</span><span class="sxs-lookup"><span data-stu-id="98621-115"><span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpOpen*</span></span>
</dt> <dd>

<span data-ttu-id="98621-116">Puntero a una [**estructura \_ \_ parms abierta de MCI**](mci-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="98621-116">Pointer to an [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure.</span></span> <span data-ttu-id="98621-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="98621-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98621-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98621-118">Return Value</span></span>

<span data-ttu-id="98621-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="98621-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="98621-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98621-120">Remarks</span></span>

<span data-ttu-id="98621-121">La \_ marca MCI Open \_ Type se debe usar siempre que se especifique un dispositivo en la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="98621-121">The MCI\_OPEN\_TYPE flag must be used whenever a device is specified in the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span> <span data-ttu-id="98621-122">Si abre un dispositivo mediante la especificación de una constante de tipo de dispositivo, debe especificar la \_ marca MCI Open \_ type id, además de \_ MCI \_ Open \_ Type.</span><span class="sxs-lookup"><span data-stu-id="98621-122">If you open a device by specifying a device-type constant, you must specify the MCI\_OPEN\_TYPE\_ID flag in addition to MCI\_OPEN\_TYPE.</span></span> <span data-ttu-id="98621-123">Para obtener una lista de las constantes de tipo de dispositivo, consulte [tipos de dispositivos MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="98621-123">For a list of device-type constants, see [MCI Device Types](mci-device-types.md).</span></span>

<span data-ttu-id="98621-124">Si \_ \_ no se especifica la marca MCI Open Shareable cuando se abre un dispositivo o un archivo inicialmente, se \_ producirá un error en todos los comandos abiertos de MCI posteriores al dispositivo o archivo.</span><span class="sxs-lookup"><span data-stu-id="98621-124">If the MCI\_OPEN\_SHAREABLE flag is not specified when a device or file is initially opened, all subsequent MCI\_OPEN commands to the device or file will fail.</span></span> <span data-ttu-id="98621-125">Si el dispositivo o el archivo ya están abiertos y no se especifica este marcador, se producirá un error en la llamada aunque el primer comando abierto especifique MCI \_ Open \_ Shareable.</span><span class="sxs-lookup"><span data-stu-id="98621-125">If the device or file is already open and this flag is not specified, the call will fail even if the first open command specified MCI\_OPEN\_SHAREABLE.</span></span> <span data-ttu-id="98621-126">Archivos abiertos para MCISEQ. DRV y MCIWAVE. Los dispositivos DRV no se pueden compartir.</span><span class="sxs-lookup"><span data-stu-id="98621-126">Files opened for the MCISEQ.DRV and MCIWAVE.DRV devices are nonsharable.</span></span>

<span data-ttu-id="98621-127">El caso se omite en el nombre del dispositivo, pero no puede haber espacios en blanco iniciales ni finales.</span><span class="sxs-lookup"><span data-stu-id="98621-127">Case is ignored in the device name, but there cannot be leading or trailing blanks.</span></span>

<span data-ttu-id="98621-128">Para usar la selección automática de tipos (a través de las entradas del registro), asigne el nombre de archivo y la extensión de archivo al miembro **lpstrElementName** de la estructura identificada por *lpOpen*, establezca el miembro **lpstrDeviceType** en **null** y establezca la \_ marca de elemento abierto MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="98621-128">To use automatic type selection (via the entries in the registry), assign the filename and file extension to the **lpstrElementName** member of the structure identified by *lpOpen*, set the **lpstrDeviceType** member to **NULL**, and set the MCI\_OPEN\_ELEMENT flag.</span></span>

<span data-ttu-id="98621-129">Las siguientes marcas adicionales se aplican a todos los dispositivos que admiten MCI \_ Open:</span><span class="sxs-lookup"><span data-stu-id="98621-129">The following additional flags apply to all devices supporting MCI\_OPEN:</span></span>

<dl> <dt>

<span data-ttu-id="98621-130"><span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>\_alias abierto de MCI \_</span><span class="sxs-lookup"><span data-stu-id="98621-130"><span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>MCI\_OPEN\_ALIAS</span></span>
</dt> <dd>

<span data-ttu-id="98621-131">Un alias se incluye en el miembro **lpstrAlias** de la estructura identificada por *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="98621-131">An alias is included in the **lpstrAlias** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="98621-132"><span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>MCI \_ abierto \_ compartible</span><span class="sxs-lookup"><span data-stu-id="98621-132"><span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>MCI\_OPEN\_SHAREABLE</span></span>
</dt> <dd>

<span data-ttu-id="98621-133">El dispositivo o archivo debe abrirse como compartible.</span><span class="sxs-lookup"><span data-stu-id="98621-133">The device or file should be opened as sharable.</span></span>

</dd> <dt>

<span data-ttu-id="98621-134"><span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>\_tipo abierto \_ MCI</span><span class="sxs-lookup"><span data-stu-id="98621-134"><span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>MCI\_OPEN\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="98621-135">Un nombre de tipo de dispositivo o constante se incluye en el miembro **lpstrDeviceType** de la estructura identificada por *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="98621-135">A device type name or constant is included in the **lpstrDeviceType** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="98621-136"><span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>\_ \_ ID. de tipo abierto MCI \_</span><span class="sxs-lookup"><span data-stu-id="98621-136"><span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>MCI\_OPEN\_TYPE\_ID</span></span>
</dt> <dd>

<span data-ttu-id="98621-137">La palabra de orden inferior del miembro **lpstrDeviceType** de la estructura identificada por *lpOpen* contiene un identificador de tipo de dispositivo MCI estándar y la palabra de orden superior, opcionalmente, contiene el índice ordinal para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98621-137">The low-order word of the **lpstrDeviceType** member of the structure identified by *lpOpen* contains a standard MCI device type identifier and the high-order word optionally contains the ordinal index for the device.</span></span> <span data-ttu-id="98621-138">Use esta marca con la \_ marca MCI Open \_ Type.</span><span class="sxs-lookup"><span data-stu-id="98621-138">Use this flag with the MCI\_OPEN\_TYPE flag.</span></span>

</dd> </dl>

<span data-ttu-id="98621-139">Las siguientes marcas adicionales se aplican a los dispositivos compuestos:</span><span class="sxs-lookup"><span data-stu-id="98621-139">The following additional flags apply to compound devices:</span></span>

<dl> <dt>

<span data-ttu-id="98621-140"><span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>MCI \_ Open ( \_ elemento)</span><span class="sxs-lookup"><span data-stu-id="98621-140"><span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>MCI\_OPEN\_ELEMENT</span></span>
</dt> <dd>

<span data-ttu-id="98621-141">Un nombre de archivo se incluye en el miembro **lpstrElementName** de la estructura identificada por *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="98621-141">A filename is included in the **lpstrElementName** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="98621-142"><span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>\_identificador de \_ elemento \_ abierto MCI</span><span class="sxs-lookup"><span data-stu-id="98621-142"><span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>MCI\_OPEN\_ELEMENT\_ID</span></span>
</dt> <dd>

<span data-ttu-id="98621-143">El miembro **lpstrElementName** de la estructura identificada por *lpOpen* se interpreta como un valor **DWORD** y tiene un significado interno en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98621-143">The **lpstrElementName** member of the structure identified by *lpOpen* is interpreted as a **DWORD** value and has meaning internal to the device.</span></span> <span data-ttu-id="98621-144">Use esta marca con la \_ marca de \_ elemento abierto MCI.</span><span class="sxs-lookup"><span data-stu-id="98621-144">Use this flag with the MCI\_OPEN\_ELEMENT flag.</span></span>

</dd> </dl>

<span data-ttu-id="98621-145">Con el tipo de dispositivo **DigitalVideo** se usan las siguientes marcas adicionales:</span><span class="sxs-lookup"><span data-stu-id="98621-145">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="98621-146"><span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>MCI \_ DGV \_ abrir \_ nostatic</span><span class="sxs-lookup"><span data-stu-id="98621-146"><span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>MCI\_DGV\_OPEN\_NOSTATIC</span></span>
</dt> <dd>

<span data-ttu-id="98621-147">El dispositivo debe reducir el número de colores estáticos (del sistema) de la paleta.</span><span class="sxs-lookup"><span data-stu-id="98621-147">The device should reduce the number of static (system) colors in the palette.</span></span> <span data-ttu-id="98621-148">Esto aumenta el número de colores disponibles para representar la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="98621-148">This increases the number of colors available for rendering the video stream.</span></span> <span data-ttu-id="98621-149">Esta marca solo se aplica a los dispositivos que comparten una paleta con Windows.</span><span class="sxs-lookup"><span data-stu-id="98621-149">This flag applies only to devices that share a palette with Windows.</span></span>

</dd> <dt>

<span data-ttu-id="98621-150"><span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>MCI \_ DGV \_ abrir \_ primario</span><span class="sxs-lookup"><span data-stu-id="98621-150"><span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>MCI\_DGV\_OPEN\_PARENT</span></span>
</dt> <dd>

<span data-ttu-id="98621-151">El identificador de ventana principal se especifica en el miembro **hWndParent** de la estructura identificada por *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="98621-151">The parent window handle is specified in the **hWndParent** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="98621-152"><span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>MCI \_ DGV \_ Open \_ WS</span><span class="sxs-lookup"><span data-stu-id="98621-152"><span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>MCI\_DGV\_OPEN\_WS</span></span>
</dt> <dd>

<span data-ttu-id="98621-153">Un estilo de ventana se especifica en el miembro **dwStyle** de la estructura identificada por *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="98621-153">A window style is specified in the **dwStyle** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="98621-154"><span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>\_DGV de \_ \_ 16 bits de apertura de MCI</span><span class="sxs-lookup"><span data-stu-id="98621-154"><span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>MCI\_DGV\_OPEN\_16BIT</span></span>
</dt> <dd>

<span data-ttu-id="98621-155">Indica una preferencia para la compatibilidad con dispositivos MCI de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="98621-155">Indicates a preference for 16-bit MCI device support.</span></span>

</dd> <dt>

<span data-ttu-id="98621-156"><span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>MCI \_ DGV \_ Open \_ 32bit</span><span class="sxs-lookup"><span data-stu-id="98621-156"><span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>MCI\_DGV\_OPEN\_32BIT</span></span>
</dt> <dd>

<span data-ttu-id="98621-157">Indica una preferencia para la compatibilidad con dispositivos MCI de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="98621-157">Indicates a preference for 32-bit MCI device support.</span></span>

</dd> </dl>

<span data-ttu-id="98621-158">En el caso de los dispositivos de vídeo digital, el parámetro *lpOpen* apunta a una estructura [**MCI \_ DGV \_ Open \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="98621-158">For digital-video devices, the *lpOpen* parameter points to an [**MCI\_DGV\_OPEN\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa) structure.</span></span>

<span data-ttu-id="98621-159">Se usan las siguientes marcas adicionales con el tipo de dispositivo **superpuesto** :</span><span class="sxs-lookup"><span data-stu-id="98621-159">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="98621-160"><span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>MCI \_ OVLY \_ abrir \_ primario</span><span class="sxs-lookup"><span data-stu-id="98621-160"><span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>MCI\_OVLY\_OPEN\_PARENT</span></span>
</dt> <dd>

<span data-ttu-id="98621-161">El identificador de ventana principal se especifica en el miembro **hWndParent** de la estructura identificada por *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="98621-161">The parent window handle is specified in the **hWndParent** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="98621-162"><span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>MCI \_ OVLY \_ Open \_ WS</span><span class="sxs-lookup"><span data-stu-id="98621-162"><span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>MCI\_OVLY\_OPEN\_WS</span></span>
</dt> <dd>

<span data-ttu-id="98621-163">Un estilo de ventana se especifica en el miembro **dwStyle** de la estructura identificada por *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="98621-163">A window style is specified in the **dwStyle** member of the structure identified by *lpOpen*.</span></span> <span data-ttu-id="98621-164">El valor **dwStyle** especifica el estilo de la ventana que el controlador creará y mostrará si la aplicación no proporciona una.</span><span class="sxs-lookup"><span data-stu-id="98621-164">The **dwStyle** value specifies the style of the window that the driver will create and display if the application does not provide one.</span></span> <span data-ttu-id="98621-165">El parámetro Style toma un entero que define el estilo de la ventana.</span><span class="sxs-lookup"><span data-stu-id="98621-165">The style parameter takes an integer that defines the window style.</span></span> <span data-ttu-id="98621-166">Estas constantes son las mismas que los estilos de ventana estándar (como WS \_ Child, WS \_ OVERLAPPEDWINDOW o WS \_ popup).</span><span class="sxs-lookup"><span data-stu-id="98621-166">These constants are the same as the standard window styles (such as WS\_CHILD, WS\_OVERLAPPEDWINDOW, or WS\_POPUP).</span></span>

</dd> </dl>

<span data-ttu-id="98621-167">En el caso de los dispositivos de superposición de vídeo, el parámetro *lpOpen* apunta a una estructura [**MCI \_ OVLY \_ Open \_ parms**](mci-ovly-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="98621-167">For video-overlay devices, the *lpOpen* parameter points to an [**MCI\_OVLY\_OPEN\_PARMS**](mci-ovly-open-parms.md) structure.</span></span>

<span data-ttu-id="98621-168">Con el tipo de dispositivo **WaveAudio** se usa la siguiente marca adicional:</span><span class="sxs-lookup"><span data-stu-id="98621-168">The following additional flag is used with the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="98621-169"><span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>\_ \_ búfer abierto de onda de MCI \_</span><span class="sxs-lookup"><span data-stu-id="98621-169"><span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>MCI\_WAVE\_OPEN\_BUFFER</span></span>
</dt> <dd>

<span data-ttu-id="98621-170">Se especifica una longitud de búfer en el miembro **dwBufferSeconds** de la estructura identificada por *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="98621-170">A buffer length is specified in the **dwBufferSeconds** member of the structure identified by *lpOpen*.</span></span>

</dd> </dl>

<span data-ttu-id="98621-171">En el caso de los dispositivos de audio de onda, el parámetro *lpOpen* apunta a una estructura [**parms de MCI \_ \_ Open \_ Wave**](mci-wave-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="98621-171">For waveform-audio devices, the *lpOpen* parameter points to an [**MCI\_WAVE\_OPEN\_PARMS**](mci-wave-open-parms.md) structure.</span></span> <span data-ttu-id="98621-172">El controlador MCIWAVE requiere un dispositivo de audio de onda asincrónica.</span><span class="sxs-lookup"><span data-stu-id="98621-172">The MCIWAVE driver requires an asynchronous waveform-audio device.</span></span>

## <a name="requirements"></a><span data-ttu-id="98621-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98621-173">Requirements</span></span>



| <span data-ttu-id="98621-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="98621-174">Requirement</span></span> | <span data-ttu-id="98621-175">Value</span><span class="sxs-lookup"><span data-stu-id="98621-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98621-176">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98621-176">Minimum supported client</span></span><br/> | <span data-ttu-id="98621-177">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="98621-177">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="98621-178">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98621-178">Minimum supported server</span></span><br/> | <span data-ttu-id="98621-179">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="98621-179">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="98621-180">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98621-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="98621-181"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98621-181"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98621-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="98621-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98621-183">MCI</span><span class="sxs-lookup"><span data-stu-id="98621-183">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="98621-184">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="98621-184">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

