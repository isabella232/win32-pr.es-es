---
title: comando Open (Corecrt \_ IO. h)
description: El comando Open Inicializa un dispositivo. Todos los dispositivos MCI reconocen este comando.
ms.assetid: 0bb97c8c-8222-4d4e-b20b-94e9f9095afe
keywords:
- abrir comando de Windows multimedia
topic_type:
- apiref
api_name:
- open
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8d31f1806a9c12f764c679548564aa053c3041
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802222"
---
# <a name="open-command"></a><span data-ttu-id="fd3d4-105">abrir (comando)</span><span class="sxs-lookup"><span data-stu-id="fd3d4-105">open command</span></span>

<span data-ttu-id="fd3d4-106">El comando Open Inicializa un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-106">The open command initializes a device.</span></span> <span data-ttu-id="fd3d4-107">Todos los dispositivos MCI reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-107">All MCI devices recognize this command.</span></span>

<span data-ttu-id="fd3d4-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("open %s %s %s"), 
  lpszDevice, 
  lpszOpenFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="fd3d4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fd3d4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd3d4-110"><span id="lpszDevice"></span><span id="lpszdevice"></span><span id="LPSZDEVICE"></span>*lpszDevice*</span><span class="sxs-lookup"><span data-stu-id="fd3d4-110"><span id="lpszDevice"></span><span id="lpszdevice"></span><span id="LPSZDEVICE"></span>*lpszDevice*</span></span>
</dt> <dd>

<span data-ttu-id="fd3d4-111">Identificador de un dispositivo MCI o controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-111">Identifier of an MCI device or device driver.</span></span> <span data-ttu-id="fd3d4-112">Puede ser un nombre de dispositivo (como se indica en el registro o en el archivo SYSTEM.INI) o el nombre de archivo del controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-112">This can be either a device name (as given in the registry or the SYSTEM.INI file) or the filename of the device driver.</span></span> <span data-ttu-id="fd3d4-113">Si especifica el nombre de archivo del controlador de dispositivo, puede incluir opcionalmente el. Extensión DRV, pero no debe incluir la ruta de acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-113">If you specify the filename of the device driver, you can optionally include the .DRV extension, but you should not include the path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="fd3d4-114"><span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszOpenFlags*</span><span class="sxs-lookup"><span data-stu-id="fd3d4-114"><span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszOpenFlags*</span></span>
</dt> <dd>

<span data-ttu-id="fd3d4-115">Marca que identifica lo que se va a inicializar.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-115">Flag that identifies what to initialize.</span></span> <span data-ttu-id="fd3d4-116">En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **Open** y las marcas usadas por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-116">The following table lists device types that recognize the **open** command and the flags used by each type.</span></span>



| <span data-ttu-id="fd3d4-117">Value</span><span class="sxs-lookup"><span data-stu-id="fd3d4-117">Value</span></span>        | <span data-ttu-id="fd3d4-118">Significado</span><span class="sxs-lookup"><span data-stu-id="fd3d4-118">Meaning</span></span>                                                        | <span data-ttu-id="fd3d4-119">Significado</span><span class="sxs-lookup"><span data-stu-id="fd3d4-119">Meaning</span></span>                                                                         |
|--------------|----------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="fd3d4-120">cdaudio</span><span class="sxs-lookup"><span data-stu-id="fd3d4-120">cdaudio</span></span>      | <span data-ttu-id="fd3d4-121">alias *de \_ dispositivo* de alias compartible</span><span class="sxs-lookup"><span data-stu-id="fd3d4-121">alias *device\_alias* sharable</span></span>                                  | <span data-ttu-id="fd3d4-122">tipo *de \_ dispositivo*</span><span class="sxs-lookup"><span data-stu-id="fd3d4-122">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="fd3d4-123">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="fd3d4-123">digitalvideo</span></span> | <span data-ttu-id="fd3d4-124">alias *Device \_ aliaselementname* nostatic *hWnd* primario compartible</span><span class="sxs-lookup"><span data-stu-id="fd3d4-124">alias *device\_aliaselementname* nostatic parent *hwnd* sharable</span></span> | <span data-ttu-id="fd3d4-125">estilo secundario de estilo superpuesto estilo *emergente \_ tipo de estilo tipo* de *\_ dispositivo*</span><span class="sxs-lookup"><span data-stu-id="fd3d4-125">style child style overlapped style popup style *style\_type* type *device\_type*</span></span> |
| <span data-ttu-id="fd3d4-126">overlay</span><span class="sxs-lookup"><span data-stu-id="fd3d4-126">overlay</span></span>      | <span data-ttu-id="fd3d4-127">alias de dispositivo alias primario *hWnd* elemento secundario de estilo compartido *\_*</span><span class="sxs-lookup"><span data-stu-id="fd3d4-127">alias *device\_alias* parent *hwnd* sharable style child</span></span>         | <span data-ttu-id="fd3d4-128">estilo de estilo emergente de estilo superpuesto de estilo tipo de tipo de *dispositivo \_* *\_*</span><span class="sxs-lookup"><span data-stu-id="fd3d4-128">style overlapped style popup style *style\_type* type *device\_type*</span></span>             |
| <span data-ttu-id="fd3d4-129">sequencer</span><span class="sxs-lookup"><span data-stu-id="fd3d4-129">sequencer</span></span>    | <span data-ttu-id="fd3d4-130">alias *de \_ dispositivo* de alias compartible</span><span class="sxs-lookup"><span data-stu-id="fd3d4-130">alias *device\_alias* sharable</span></span>                                 | <span data-ttu-id="fd3d4-131">tipo *de \_ dispositivo*</span><span class="sxs-lookup"><span data-stu-id="fd3d4-131">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="fd3d4-132">vídeos</span><span class="sxs-lookup"><span data-stu-id="fd3d4-132">vcr</span></span>          | <span data-ttu-id="fd3d4-133">alias *de \_ dispositivo* de alias compartible</span><span class="sxs-lookup"><span data-stu-id="fd3d4-133">alias *device\_alias* sharable</span></span>                                  | <span data-ttu-id="fd3d4-134">tipo *de \_ dispositivo*</span><span class="sxs-lookup"><span data-stu-id="fd3d4-134">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="fd3d4-135">videodisco</span><span class="sxs-lookup"><span data-stu-id="fd3d4-135">videodisk</span></span>    | <span data-ttu-id="fd3d4-136">alias *de \_ dispositivo* de alias compartible</span><span class="sxs-lookup"><span data-stu-id="fd3d4-136">alias *device\_alias* sharable</span></span>                                  | <span data-ttu-id="fd3d4-137">tipo *de \_ dispositivo*</span><span class="sxs-lookup"><span data-stu-id="fd3d4-137">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="fd3d4-138">waveaudio</span><span class="sxs-lookup"><span data-stu-id="fd3d4-138">waveaudio</span></span>    | <span data-ttu-id="fd3d4-139">*\_ tamaño de búfer* de búfer de *\_ alias de dispositivo* de alias</span><span class="sxs-lookup"><span data-stu-id="fd3d4-139">alias *device\_alias* buffer *buffer\_size*</span></span>                     | <span data-ttu-id="fd3d4-140">tipo de *dispositivo \_* compartible</span><span class="sxs-lookup"><span data-stu-id="fd3d4-140">sharable type *device\_type*</span></span>                                                    |



 

<span data-ttu-id="fd3d4-141">En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszOpenFlags** y su significado.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-141">The following table lists the flags that can be specified in the **lpszOpenFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="fd3d4-142">Value</span><span class="sxs-lookup"><span data-stu-id="fd3d4-142">Value</span></span>                 | <span data-ttu-id="fd3d4-143">Significado</span><span class="sxs-lookup"><span data-stu-id="fd3d4-143">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd3d4-144">alias *de \_ dispositivo* alias</span><span class="sxs-lookup"><span data-stu-id="fd3d4-144">alias *device\_alias*</span></span> | <span data-ttu-id="fd3d4-145">Especifica un nombre alternativo para el dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-145">Specifies an alternate name for the given device.</span></span> <span data-ttu-id="fd3d4-146">Si se especifica, se debe usar como el *\_ identificador del dispositivo* en los siguientes comandos.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-146">If specified, it must be used as the *device\_id* in subsequent commands.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="fd3d4-147">*ElementName*</span><span class="sxs-lookup"><span data-stu-id="fd3d4-147">*elementname*</span></span>         | <span data-ttu-id="fd3d4-148">Especifica el nombre del elemento de dispositivo (archivo) que se carga cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-148">Specifies the name of the device element (file) loaded when the device opens.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="fd3d4-149">*\_ tamaño de búfer* de búfer</span><span class="sxs-lookup"><span data-stu-id="fd3d4-149">buffer *buffer\_size*</span></span> | <span data-ttu-id="fd3d4-150">Establece el tamaño, en segundos, del búfer usado por el dispositivo de audio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-150">Sets the size, in seconds, of the buffer used by the waveform-audio device.</span></span> <span data-ttu-id="fd3d4-151">El tamaño predeterminado del búfer se establece cuando el dispositivo de audio de forma de onda está instalado o configurado.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-151">The default size of the buffer is set when the waveform-audio device is installed or configured.</span></span> <span data-ttu-id="fd3d4-152">Normalmente, el tamaño del búfer se establece en 4 segundos.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-152">Typically the buffer size is set to 4 seconds.</span></span> <span data-ttu-id="fd3d4-153">Con el dispositivo MCIWAVE, el tamaño mínimo es 2 segundos y el tamaño máximo es de 9 segundos.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-153">With the MCIWAVE device, the minimum size is 2 seconds and the maximum size is 9 seconds.</span></span>                                                |
| <span data-ttu-id="fd3d4-154">*hWnd* primario</span><span class="sxs-lookup"><span data-stu-id="fd3d4-154">parent *hwnd*</span></span>         | <span data-ttu-id="fd3d4-155">Especifica el identificador de ventana de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-155">Specifies the window handle of the parent window.</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="fd3d4-156">compartible</span><span class="sxs-lookup"><span data-stu-id="fd3d4-156">sharable</span></span>              | <span data-ttu-id="fd3d4-157">Inicializa el dispositivo o archivo como compartible.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-157">Initializes the device or file as sharable.</span></span> <span data-ttu-id="fd3d4-158">Los intentos posteriores para abrir el dispositivo o el archivo producirán un error a menos que especifique "compartible" en los comandos **abiertos** originales y posteriores.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-158">Subsequent attempts to open the device or file fail unless you specify "sharable" in both the original and subsequent **open** commands.</span></span> <span data-ttu-id="fd3d4-159">MCI devuelve un error de dispositivo no válido si el dispositivo ya está abierto y no se pueda compartir.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-159">MCI returns an invalid device error if the device is already open and not sharable.</span></span><br/> <span data-ttu-id="fd3d4-160">Los dispositivos MCISEQ Sequencer y MCIWAVE no admiten archivos compartidos.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-160">The MCISEQ sequencer and MCIWAVE devices do not support shared files.</span></span><br/> |
| <span data-ttu-id="fd3d4-161">estilo secundario</span><span class="sxs-lookup"><span data-stu-id="fd3d4-161">style child</span></span>           | <span data-ttu-id="fd3d4-162">Abre una ventana con un estilo de ventana secundario.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-162">Opens a window with a child window style.</span></span>                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="fd3d4-163">estilo superpuesto</span><span class="sxs-lookup"><span data-stu-id="fd3d4-163">style overlapped</span></span>      | <span data-ttu-id="fd3d4-164">Abre una ventana con un estilo de ventana superpuesto.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-164">Opens a window with an overlapped window style.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="fd3d4-165">cuadro emergente de estilo</span><span class="sxs-lookup"><span data-stu-id="fd3d4-165">style popup</span></span>           | <span data-ttu-id="fd3d4-166">Abre una ventana con un estilo de ventana emergente.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-166">Opens a window with a pop-up window style.</span></span>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="fd3d4-167">*\_ tipo de estilo* de estilo</span><span class="sxs-lookup"><span data-stu-id="fd3d4-167">style *style\_type*</span></span>   | <span data-ttu-id="fd3d4-168">Indica un estilo de ventana.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-168">Indicates a window style.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="fd3d4-169">tipo *de \_ dispositivo*</span><span class="sxs-lookup"><span data-stu-id="fd3d4-169">type *device\_type*</span></span>   | <span data-ttu-id="fd3d4-170">Especifica el tipo de dispositivo de un archivo.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-170">Specifies the device type of a file.</span></span>                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="fd3d4-171"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="fd3d4-171"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="fd3d4-172">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-172">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="fd3d4-173">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="fd3d4-173">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd3d4-174">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd3d4-174">Return Value</span></span>

<span data-ttu-id="fd3d4-175">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-175">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd3d4-176">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd3d4-176">Remarks</span></span>

<span data-ttu-id="fd3d4-177">MCI reserva "cdaudio" para el tipo de dispositivo de audio de CD, "VideoDisc" para el tipo de dispositivo de videodisco, "Sequencer" para el tipo de dispositivo del secuenciador de MIDI, "AVIVideo" para el tipo de dispositivo de vídeo digital y "WaveAudio" para el tipo de dispositivo de audio de onda.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-177">MCI reserves "cdaudio" for the CD audio device type, "videodisc" for the videodisc device type, "sequencer" for the MIDI sequencer device type, "AVIVideo" for the digital-video device type, and "waveaudio" for the waveform-audio device type.</span></span>

<span data-ttu-id="fd3d4-178">Como alternativa a la marca "tipo", MCI puede seleccionar el dispositivo en función de la extensión que usa el archivo, tal como se registra en el registro o en la \[ sección de la extensión MCI \] del archivo de SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-178">As an alternative to the "type" flag, MCI can select the device based on the extension used by the file, as recorded in the registry or the \[mci extension\] section of the SYSTEM.INI file.</span></span>

<span data-ttu-id="fd3d4-179">MCI puede abrir archivos AVI mediante un puntero de interfaz de archivo o un puntero de interfaz de flujo.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-179">MCI can open AVI files by using a file-interface pointer or a stream-interface pointer.</span></span> <span data-ttu-id="fd3d4-180">Para abrir un archivo mediante cualquier tipo de puntero de interfaz, especifique un signo de arroba (@) seguido del puntero de interfaz en lugar del nombre de archivo o dispositivo para el parámetro *lpszDevice* .</span><span class="sxs-lookup"><span data-stu-id="fd3d4-180">To open a file by using either type of interface pointer, specify an at sign (@) followed by the interface pointer in place of the file or device name for the *lpszDevice* parameter.</span></span> <span data-ttu-id="fd3d4-181">Para obtener más información sobre las interfaces de archivo y de secuencia, vea " [funciones y macros de AVIFile](avifile-functions-and-macros.md)".</span><span class="sxs-lookup"><span data-stu-id="fd3d4-181">For more information about the file and stream interfaces, see " [AVIFile Functions and Macros](avifile-functions-and-macros.md)."</span></span>

<span data-ttu-id="fd3d4-182">El siguiente comando abre el dispositivo "de".</span><span class="sxs-lookup"><span data-stu-id="fd3d4-182">The following command opens the "mysound" device.</span></span>

``` syntax
open new type waveaudio alias mysound buffer 6
```

<span data-ttu-id="fd3d4-183">Con el nombre de dispositivo "nuevo", el controlador de la onda prepara un nuevo recurso de onda.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-183">With device name "new", the waveform driver prepares a new waveform resource.</span></span> <span data-ttu-id="fd3d4-184">El comando asigna el alias del dispositivo "mi sonido" y especifica un búfer de 6 segundos.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-184">The command assigns the device alias "mysound" and specifies a 6-second buffer.</span></span>

<span data-ttu-id="fd3d4-185">Puede eliminar la marca "tipo" si combina el nombre del dispositivo con el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-185">You can eliminate the "type" flag if you combine the device name with the filename.</span></span> <span data-ttu-id="fd3d4-186">MCI reconoce esta combinación cuando se usa la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="fd3d4-186">MCI recognizes this combination when you use the following syntax:</span></span>

<span data-ttu-id="fd3d4-187">*\_ nombre del dispositivo*</span><span class="sxs-lookup"><span data-stu-id="fd3d4-187">*device\_name* !</span></span> <span data-ttu-id="fd3d4-188">*nombre del elemento \_*</span><span class="sxs-lookup"><span data-stu-id="fd3d4-188">*element\_name*</span></span>

<span data-ttu-id="fd3d4-189">El signo de exclamación separa el nombre del dispositivo del nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-189">The exclamation point separates the device name from the filename.</span></span> <span data-ttu-id="fd3d4-190">El signo de exclamación no debe estar delimitado por espacios en blanco.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-190">The exclamation point should not be delimited by white spaces.</span></span>

<span data-ttu-id="fd3d4-191">En el siguiente ejemplo se abre la derecha. Archivo WAV mediante el dispositivo "WaveAudio".</span><span class="sxs-lookup"><span data-stu-id="fd3d4-191">The following example opens the RIGHT.WAV file using the "waveaudio" device.</span></span>

``` syntax
open waveaudio!right.wav
```

<span data-ttu-id="fd3d4-192">El controlador MCIWAVE requiere un dispositivo de audio de onda asincrónica.</span><span class="sxs-lookup"><span data-stu-id="fd3d4-192">The MCIWAVE driver requires an asynchronous waveform-audio device.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd3d4-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd3d4-193">Requirements</span></span>



| <span data-ttu-id="fd3d4-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd3d4-194">Requirement</span></span> | <span data-ttu-id="fd3d4-195">Value</span><span class="sxs-lookup"><span data-stu-id="fd3d4-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd3d4-196">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd3d4-196">Minimum supported client</span></span><br/> | <span data-ttu-id="fd3d4-197">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fd3d4-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fd3d4-198">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd3d4-198">Minimum supported server</span></span><br/> | <span data-ttu-id="fd3d4-199">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fd3d4-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fd3d4-200">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd3d4-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd3d4-201"><dt>Corecrt \_ IO. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd3d4-201"><dt>Corecrt\_io.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd3d4-202">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd3d4-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd3d4-203">MCI</span><span class="sxs-lookup"><span data-stu-id="fd3d4-203">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="fd3d4-204">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="fd3d4-204">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

