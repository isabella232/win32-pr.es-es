---
title: Comando MCI_SETVIDEO (mmsystem. h)
description: El \_ comando MCI SETVIDEO establece los valores asociados a la reproducción de vídeo. Los dispositivos digitales-vídeo y VCR reconocen este comando.
ms.assetid: b84956d8-01a0-49f6-a96c-2693a25e6f2a
keywords:
- Comando de MCI_SETVIDEO de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_SETVIDEO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83a20e0cc5466ac9ff28a59543543069fa9acd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490774"
---
# <a name="mci_setvideo-command"></a><span data-ttu-id="ea21b-105">\_Comando MCI SETVIDEO</span><span class="sxs-lookup"><span data-stu-id="ea21b-105">MCI\_SETVIDEO command</span></span>

<span data-ttu-id="ea21b-106">El \_ comando MCI SETVIDEO establece los valores asociados a la reproducción de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ea21b-106">The MCI\_SETVIDEO command sets values associated with video playback.</span></span> <span data-ttu-id="ea21b-107">Los dispositivos digitales-vídeo y VCR reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="ea21b-107">Digital-video and VCR devices recognize this command.</span></span>

<span data-ttu-id="ea21b-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="ea21b-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETVIDEO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetVideo
);
```



## <a name="parameters"></a><span data-ttu-id="ea21b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea21b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea21b-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="ea21b-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="ea21b-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="ea21b-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-113">**MCI \_ NOTIFICAr**, **\_ espera de MCI** o **\_ prueba de MCI**.</span><span class="sxs-lookup"><span data-stu-id="ea21b-113">**MCI\_NOTIFY**, **MCI\_WAIT**, or **MCI\_TEST**.</span></span> <span data-ttu-id="ea21b-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ea21b-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-115"><span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*lpSetVideo*</span><span class="sxs-lookup"><span data-stu-id="ea21b-115"><span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*lpSetVideo*</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-116">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="ea21b-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="ea21b-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="ea21b-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea21b-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ea21b-118">Return Value</span></span>

<span data-ttu-id="ea21b-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ea21b-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea21b-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea21b-120">Remarks</span></span>

<span data-ttu-id="ea21b-121">Se usan las siguientes marcas adicionales con el tipo de dispositivo "DigitalVideo":</span><span class="sxs-lookup"><span data-stu-id="ea21b-121">The following additional flags are used with the "digitalvideo" device type:</span></span>

<dl> <dt>

<span data-ttu-id="ea21b-122"><span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>\_DGV MCI \_ SETVIDEO \_ alg</span><span class="sxs-lookup"><span data-stu-id="ea21b-122"><span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>MCI\_DGV\_SETVIDEO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-123">El miembro **lpstrAlgorithm** de la estructura identificada por *lpSetVideo* contiene una dirección de un búfer que contiene el nombre de un algoritmo de compresión de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ea21b-123">The **lpstrAlgorithm** member of the structure identified by *lpSetVideo* contains an address of a buffer containing the name of a video compression algorithm.</span></span> <span data-ttu-id="ea21b-124">El algoritmo de compresión lo usan los comandos de [ \_ reserva de MCI](mci-reserve.md) o de [ \_ registro MCI](mci-record.md) posteriores.</span><span class="sxs-lookup"><span data-stu-id="ea21b-124">The compression algorithm is used by subsequent [MCI\_RESERVE](mci-reserve.md) or [MCI\_RECORD](mci-record.md) commands.</span></span> <span data-ttu-id="ea21b-125">Los algoritmos disponibles dependen del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea21b-125">The available algorithms are device dependent.</span></span>

<span data-ttu-id="ea21b-126">Si el algoritmo especificado no es compatible con el formato de archivo actual, el formato del archivo se cambia al formato predeterminado para el algoritmo.</span><span class="sxs-lookup"><span data-stu-id="ea21b-126">If the specified algorithm is incompatible with the current file format, the file format is changed to the default format for the algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-127"><span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>MCI \_ DGV \_ SETVIDEO \_ CLOCKTIME</span><span class="sxs-lookup"><span data-stu-id="ea21b-127"><span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>MCI\_DGV\_SETVIDEO\_CLOCKTIME</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-128">Cuando se usa con **MCI \_ DGV \_ SETVIDEO \_ over**, indica que el tiempo se especifica en milisegundos y es una hora absoluta.</span><span class="sxs-lookup"><span data-stu-id="ea21b-128">When used with **MCI\_DGV\_SETVIDEO\_OVER**, indicates time is specified in milliseconds and is absolute time.</span></span> <span data-ttu-id="ea21b-129">(Esta vez no está en el paso con la reproducción del área de trabajo).</span><span class="sxs-lookup"><span data-stu-id="ea21b-129">(This time is not in step with the playing of the workspace.)</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-130"><span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>\_ \_ entrada SETVIDEO de MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-130"><span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>MCI\_DGV\_SETVIDEO\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-131">Modifica los **DGV de \_ MCI \_ SETVIDEO \_ Brightness**, MCI **\_ DGV \_ SETVIDEO \_ color**, **MCI \_ DGV \_ SETVIDEO \_ Contrast**, **MCI \_ DGV \_ SETVIDEO \_ gamma**, **MCI \_ DGV \_ SETVIDEO \_ nitidez** o **MCI \_ DGV \_ SETVIDEO \_ tinte** para que afecte a la señal de entrada y modifique lo que se registra.</span><span class="sxs-lookup"><span data-stu-id="ea21b-131">Modifies the **MCI\_DGV\_SETVIDEO\_BRIGHTNESS**, **MCI\_DGV\_SETVIDEO\_COLOR**, **MCI\_DGV\_SETVIDEO\_CONTRAST**, **MCI\_DGV\_SETVIDEO\_GAMMA**, **MCI\_DGV\_SETVIDEO\_SHARPNESS**, or **MCI\_DGV\_SETVIDEO\_TINT** so that it affects the input signal and modifies what is recorded.</span></span> <span data-ttu-id="ea21b-132">Si es posible, es el valor predeterminado al supervisar la entrada.</span><span class="sxs-lookup"><span data-stu-id="ea21b-132">If possible, this is the default when monitoring the input.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-133"><span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>\_ \_ elemento SETVIDEO de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-133"><span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>MCI\_DGV\_SETVIDEO\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-134">Una constante de vídeo se especifica en el miembro **dwItem** de la estructura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="ea21b-134">A video constant is specified in the **dwItem** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="ea21b-135">La constante identifica el valor que se establece.</span><span class="sxs-lookup"><span data-stu-id="ea21b-135">The constant identifies the value that is being set.</span></span> <span data-ttu-id="ea21b-136">Puede especificar las siguientes constantes con esta marca:</span><span class="sxs-lookup"><span data-stu-id="ea21b-136">You can specify the following constants with this flag:</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-137"><span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>\_ \_ procedimiento SETVIDEO de \_ MCI \_ AVI</span><span class="sxs-lookup"><span data-stu-id="ea21b-137"><span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>MCI\_AVI\_SETVIDEO\_DRAW\_PROCEDURE</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-138">Se especifica una nueva dirección de procedimiento de dibujo en el miembro **dwValue** de la estructura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="ea21b-138">A new drawing procedure address is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="ea21b-139">Solo puede especificar un nuevo procedimiento de dibujo cuando el dispositivo está inactivo.</span><span class="sxs-lookup"><span data-stu-id="ea21b-139">You can specify a new drawing procedure only when the device is idle.</span></span> <span data-ttu-id="ea21b-140">Esta marca solo se reconoce en el controlador de vídeo digital MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="ea21b-140">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="ea21b-141">No hay ningún equivalente a esta marca en la interfaz de comandos de cadena.</span><span class="sxs-lookup"><span data-stu-id="ea21b-141">There is no equivalent to this flag in the string command interface.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-142"><span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>\_color de \_ la \_ paleta \_ SETVIDEO de MCI AVI</span><span class="sxs-lookup"><span data-stu-id="ea21b-142"><span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>MCI\_AVI\_SETVIDEO\_PALETTE\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-143">Se especifica un nuevo color de la paleta en los miembros **dwOver** y **dwValue** de la estructura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="ea21b-143">A new palette color is specified in the **dwOver** and **dwValue** members of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="ea21b-144">El miembro **dwOver** especifica el índice de la paleta del color que se va a cambiar y el miembro **dwValue** especifica el nuevo color, como un valor RGB.</span><span class="sxs-lookup"><span data-stu-id="ea21b-144">The **dwOver** member specifies the palette index of the color to be changed and the **dwValue** member specifies the new color, as an RGB value.</span></span> <span data-ttu-id="ea21b-145">También debe especificar las marcas de valor **MCI \_ DGV \_ SETVIDEO \_ over** y **MCI \_ DGV \_ SETVIDEO \_** con **el \_ \_ \_ elemento MCI DGV SETVIDEO** al usar esta constante.</span><span class="sxs-lookup"><span data-stu-id="ea21b-145">You must also specify the **MCI\_DGV\_SETVIDEO\_OVER** and **MCI\_DGV\_SETVIDEO\_VALUE** flags with **MCI\_DGV\_SETVIDEO\_ITEM** when you use this constant.</span></span> <span data-ttu-id="ea21b-146">Esta marca solo se reconoce en el controlador de vídeo digital MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="ea21b-146">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-147"><span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>\_semitono de \_ la \_ paleta \_ SETVIDEO de MCI AVI</span><span class="sxs-lookup"><span data-stu-id="ea21b-147"><span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>MCI\_AVI\_SETVIDEO\_PALETTE\_HALFTONE</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-148">Indica que se debe usar la paleta de semitonos, en lugar de la paleta predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ea21b-148">Indicates that the halftone palette should be used, instead of the default palette.</span></span> <span data-ttu-id="ea21b-149">Esta marca solo se reconoce en el controlador de vídeo digital MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="ea21b-149">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-150"><span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>MCI \_ DGV \_ SETVIDEO \_ BITSPERPEL</span><span class="sxs-lookup"><span data-stu-id="ea21b-150"><span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>MCI\_DGV\_SETVIDEO\_BITSPERPEL</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-151">El número de bits por píxel se especifica en el miembro **dwValue** de la estructura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="ea21b-151">The number of bits per pixel is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="ea21b-152">El número de bits por píxel se usa para guardar los datos capturados o grabados.</span><span class="sxs-lookup"><span data-stu-id="ea21b-152">The number of bits per pixel is used for saving captured or recorded data</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-153"><span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>brillo de DGV de MCI \_ \_ SETVIDEO \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-153"><span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>MCI\_DGV\_SETVIDEO\_BRIGHTNESS</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-154">El nivel de brillo del vídeo se especifica como un factor en el miembro de **dwValue** de la estructura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="ea21b-154">The video brightness level is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-155"><span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>\_color de \_ SETVIDEO de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-155"><span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>MCI\_DGV\_SETVIDEO\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-156">El nivel de saturación de color de vídeo se especifica como un factor en el miembro **dwValue** de la estructura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="ea21b-156">The video color saturation level is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-157"><span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>contraste de DGV de MCI \_ \_ SETVIDEO \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-157"><span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>MCI\_DGV\_SETVIDEO\_CONTRAST</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-158">El nivel de contraste del vídeo se especifica como un factor en el miembro de **dwValue** de la estructura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="ea21b-158">The video contrast level is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-159"><span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>\_velocidad de \_ \_ fotogramas de MCI DGV SETVIDEO \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-159"><span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>MCI\_DGV\_SETVIDEO\_FRAME\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-160">Una velocidad de fotogramas se especifica en el miembro **dwValue** de la estructura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="ea21b-160">A frame rate is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="ea21b-161">La tasa se especifica en unidades de fotogramas por segundo veces 1000.</span><span class="sxs-lookup"><span data-stu-id="ea21b-161">The rate is specified in units of frames per second times 1000.</span></span> <span data-ttu-id="ea21b-162">Por ejemplo, 29,97 fotogramas por segundo se especifica como 29970.</span><span class="sxs-lookup"><span data-stu-id="ea21b-162">For example, 29.97 frames per second is specified as 29970.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-163"><span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>MCI \_ DGV \_ SETVIDEO \_ gamma</span><span class="sxs-lookup"><span data-stu-id="ea21b-163"><span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>MCI\_DGV\_SETVIDEO\_GAMMA</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-164">Se especifica un valor de exponente de corrección gamma en el miembro **dwValue** de la estructura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="ea21b-164">A gamma correction exponent value is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="ea21b-165">La corrección gamma ajusta la asignación entre la intensidad codificada en el origen de presentación y el brillo mostrado.</span><span class="sxs-lookup"><span data-stu-id="ea21b-165">Gamma correction adjusts the mapping between the intensity encoded in the presentation source and the displayed brightness.</span></span> <span data-ttu-id="ea21b-166">El valor es el exponente multiplicado por 1000.</span><span class="sxs-lookup"><span data-stu-id="ea21b-166">The value is the exponent multiplied by 1000.</span></span> <span data-ttu-id="ea21b-167">Por ejemplo, 2200 indica un exponente de 2,2.</span><span class="sxs-lookup"><span data-stu-id="ea21b-167">For example, 2200 indicates an exponent of 2.2.</span></span> <span data-ttu-id="ea21b-168">Un valor de 1000 indica un exponente de 1, que no se aplica ninguna corrección gamma.</span><span class="sxs-lookup"><span data-stu-id="ea21b-168">A value of 1000 indicates an exponent of 1, which applies no gamma correction.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-169"><span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>COLOR de clave de DGV de MCI \_ \_ SETVIDEO \_ \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-169"><span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>MCI\_DGV\_SETVIDEO\_KEY\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-170">Se especifica un color de clave en el miembro **dwValue** de la estructura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="ea21b-170">A key color is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="ea21b-171">El color de la clave es un valor RGB.</span><span class="sxs-lookup"><span data-stu-id="ea21b-171">The key color is an RGB value.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-172"><span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>\_Índice de \_ clave de SETVIDEO de DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-172"><span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>MCI\_DGV\_SETVIDEO\_KEY\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-173">Un valor de índice de clave se especifica en el miembro **dwValue** de la estructura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="ea21b-173">A key index value is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="ea21b-174">El parámetro de índice es un índice de paleta física.</span><span class="sxs-lookup"><span data-stu-id="ea21b-174">The index parameter is a physical palette index.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-175"><span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>MCI \_ DGV \_ SETVIDEO \_ PALHANDLE</span><span class="sxs-lookup"><span data-stu-id="ea21b-175"><span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>MCI\_DGV\_SETVIDEO\_PALHANDLE</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-176">Se especifica un identificador de paleta en el miembro **dwValue** de la estructura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="ea21b-176">A palette handle is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="ea21b-177">El identificador de la paleta está contenido en la palabra de orden inferior.</span><span class="sxs-lookup"><span data-stu-id="ea21b-177">The palette handle is contained in the low-order word.</span></span> <span data-ttu-id="ea21b-178">Los dispositivos de vídeo digital no deben liberar la paleta pasada con este comando.</span><span class="sxs-lookup"><span data-stu-id="ea21b-178">Digital-video devices should not free the palette passed with this command.</span></span> <span data-ttu-id="ea21b-179">Las aplicaciones deben liberarla después de cerrar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea21b-179">Applications should free it after they close the device.</span></span> <span data-ttu-id="ea21b-180">Esta marca solo es compatible con dispositivos que usan paletas.</span><span class="sxs-lookup"><span data-stu-id="ea21b-180">This flag is supported only by devices that use palettes.</span></span> <span data-ttu-id="ea21b-181">Si el identificador de la paleta especificada es cero, se usa la paleta predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ea21b-181">If this specified palette handle is zero, then the default palette is used.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-182"><span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>\_nitidez de \_ SETVIDEO de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-182"><span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>MCI\_DGV\_SETVIDEO\_SHARPNESS</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-183">Un valor de nitidez de vídeo se especifica como un factor en el miembro **dwValue** de la estructura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="ea21b-183">A video sharpness value is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-184"><span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>origen de DGV de MCI \_ \_ SETVIDEO \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-184"><span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>MCI\_DGV\_SETVIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-185">Una constante que especifica el origen de la entrada de vídeo se especifica en el miembro **dwValue** de la estructura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="ea21b-185">A constant specifying the source of the video input is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="ea21b-186">Se definen las constantes siguientes:</span><span class="sxs-lookup"><span data-stu-id="ea21b-186">The following constants are defined:</span></span>

-   <span data-ttu-id="ea21b-187">**MCI \_ DGV \_ SETVIDEO \_ src \_ NTSC**: televisión NTSC.</span><span class="sxs-lookup"><span data-stu-id="ea21b-187">**MCI\_DGV\_SETVIDEO\_SRC\_NTSC**: NTSC television.</span></span>
-   <span data-ttu-id="ea21b-188">MCI \_ DGV \_ SETVIDEO \_ src \_ PAL: televisión PAL.</span><span class="sxs-lookup"><span data-stu-id="ea21b-188">MCI\_DGV\_SETVIDEO\_SRC\_PAL: PAL television.</span></span>
-   <span data-ttu-id="ea21b-189">MCI \_ DGV \_ SETVIDEO \_ src \_ RGB: RGB video.</span><span class="sxs-lookup"><span data-stu-id="ea21b-189">MCI\_DGV\_SETVIDEO\_SRC\_RGB: RGB video.</span></span>
-   <span data-ttu-id="ea21b-190">MCI \_ DGV \_ SETVIDEO \_ src \_ SECAM: el televisor SECAM.</span><span class="sxs-lookup"><span data-stu-id="ea21b-190">MCI\_DGV\_SETVIDEO\_SRC\_SECAM: SECAM television.</span></span>
-   <span data-ttu-id="ea21b-191">MCI \_ DGV \_ SETVIDEO \_ src \_ Svideo: S-video.</span><span class="sxs-lookup"><span data-stu-id="ea21b-191">MCI\_DGV\_SETVIDEO\_SRC\_SVIDEO: S-Video.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-192"><span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>\_flujo de \_ SETVIDEO de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-192"><span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>MCI\_DGV\_SETVIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-193">Se especifica una secuencia de vídeo en el miembro **dwValue** de la estructura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="ea21b-193">A video stream is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="ea21b-194">El valor entero especifica la secuencia de vídeo que se reproduce desde el área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ea21b-194">The integer value specifies the video stream played back from the workspace.</span></span> <span data-ttu-id="ea21b-195">Si no se especifica la secuencia y el formato de archivo no define una secuencia predeterminada, se reproduce la primera secuencia de vídeo intercalada físicamente.</span><span class="sxs-lookup"><span data-stu-id="ea21b-195">If the stream is not specified and the file format does not define a default stream, the first physically interleaved video stream is played.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-196"><span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>\_matiz DGV \_ SETVIDEO de MCI \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-196"><span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>MCI\_DGV\_SETVIDEO\_TINT</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-197">Un valor de matiz de vídeo se especifica como un factor en el miembro **dwValue** de la estructura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="ea21b-197">A video tint value is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="ea21b-198">Normalmente, este ajuste se modela después del control de matiz de muchos conjuntos de televisión de color, con 250 definido como verde, 750 definido como rojo y 0 (o 1000) definido como azul.</span><span class="sxs-lookup"><span data-stu-id="ea21b-198">Typically, this adjustment is modeled after the tint control of many color television sets, with 250 defined as green, 750 defined as red, and 0 (or 1000) defined as blue.</span></span> <span data-ttu-id="ea21b-199">El valor nominal siempre es 500.</span><span class="sxs-lookup"><span data-stu-id="ea21b-199">The nominal value is always 500.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-200"><span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>\_salida de DGV \_ SETVIDEO \_ de MCI</span><span class="sxs-lookup"><span data-stu-id="ea21b-200"><span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>MCI\_DGV\_SETVIDEO\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-201">La marca de **\_ \_ brillo DGV SETVIDEO \_ Brightness**, MCI **\_ DGV \_ SETVIDEO \_ color**, **MCI \_ DGV \_ SETVIDEO \_ Contrast**, **MCI \_ DGV \_ SETVIDEO \_ gamma**, **MCI \_ DGV \_ SETVIDEO \_ nitidez** o **MCI \_ DGV \_ SETVIDEO \_ tinte** se modifica para que solo afecte a la señal mostrada y no a lo que se registra.</span><span class="sxs-lookup"><span data-stu-id="ea21b-201">The **MCI\_DGV\_SETVIDEO\_BRIGHTNESS**, **MCI\_DGV\_SETVIDEO\_COLOR**, **MCI\_DGV\_SETVIDEO\_CONTRAST**, **MCI\_DGV\_SETVIDEO\_GAMMA**, **MCI\_DGV\_SETVIDEO\_SHARPNESS**, or **MCI\_DGV\_SETVIDEO\_TINT** flag is modified so that it affects only the displayed signal and not what is recorded.</span></span> <span data-ttu-id="ea21b-202">Si es posible, es el valor predeterminado al supervisar un archivo.</span><span class="sxs-lookup"><span data-stu-id="ea21b-202">If possible, this is the default when monitoring a file.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-203"><span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>MCI \_ DGV \_ SETVIDEO \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-203"><span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>MCI\_DGV\_SETVIDEO\_OVER</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-204">Un parámetro de longitud de transición se incluye en el miembro **dwOver** de la estructura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="ea21b-204">A transition length parameter is included in the **dwOver** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="ea21b-205">La longitud de la transición especifica cuánto tiempo (en el formato de hora actual) debe tardar en realizar un cambio.</span><span class="sxs-lookup"><span data-stu-id="ea21b-205">The transition length specifies how long (in the current time format) it should take to make a change.</span></span> <span data-ttu-id="ea21b-206">Si no se usa esta marca, el cambio se produce inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="ea21b-206">If this flag is not used, the change occurs immediately.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-207"><span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>calidad de SETVIDEO de MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-207"><span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>MCI\_DGV\_SETVIDEO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-208">El miembro **lpstrQuality** de la estructura identificada por *lpSetVideo* contiene una dirección de un búfer que describe la calidad del vídeo.</span><span class="sxs-lookup"><span data-stu-id="ea21b-208">The **lpstrQuality** member of the structure identified by *lpSetVideo* contains an address of a buffer describing the video quality.</span></span> <span data-ttu-id="ea21b-209">Una cadena de texto en el búfer especifica las características del algoritmo de compresión de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ea21b-209">A text-string in the buffer specifies the characteristics of the video compression algorithm.</span></span>

<span data-ttu-id="ea21b-210">La marca **MCI \_ DGV \_ SETVIDEO \_ alg** se puede usar para seleccionar un descriptor de calidad para el algoritmo especificado.</span><span class="sxs-lookup"><span data-stu-id="ea21b-210">The **MCI\_DGV\_SETVIDEO\_ALG** flag can be used to select a quality descriptor for the specified algorithm.</span></span> <span data-ttu-id="ea21b-211">Si se omite esta marca, se utiliza el algoritmo actual.</span><span class="sxs-lookup"><span data-stu-id="ea21b-211">If this flag is omitted, then the current algorithm is used.</span></span>

<span data-ttu-id="ea21b-212">Los algoritmos y los nombres de descriptor disponibles dependen del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea21b-212">The algorithms and descriptor names available depend on the device.</span></span> <span data-ttu-id="ea21b-213">Cada dispositivo proporciona documentación para los algoritmos disponibles y una descripción de los nombres de descriptor aplicables.</span><span class="sxs-lookup"><span data-stu-id="ea21b-213">Each device supplies documentation for the available algorithms and a description of the applicable descriptor names.</span></span> <span data-ttu-id="ea21b-214">El comando [MCI \_ Quality](mci-quality.md) puede definir nombres de descriptores adicionales.</span><span class="sxs-lookup"><span data-stu-id="ea21b-214">The [MCI\_QUALITY](mci-quality.md) command can define additional descriptor names.</span></span> <span data-ttu-id="ea21b-215">Todos los dispositivos admiten los descriptores "Low", "Medium" y "High".</span><span class="sxs-lookup"><span data-stu-id="ea21b-215">All devices support the descriptors "low", "medium", and "high".</span></span> <span data-ttu-id="ea21b-216">El valor predeterminado es específico del controlador.</span><span class="sxs-lookup"><span data-stu-id="ea21b-216">The default is driver specific.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-217"><span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>registro de DGV de MCI \_ \_ SETVIDEO \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-217"><span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>MCI\_DGV\_SETVIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-218">Especifica si la grabación incluye o excluye datos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ea21b-218">Specifies whether recording includes or excludes video data.</span></span> <span data-ttu-id="ea21b-219">Cuando se combina con **MCI \_ establecido \_ en**, se registran los datos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ea21b-219">When combined with **MCI\_SET\_ON**, video data is recorded.</span></span> <span data-ttu-id="ea21b-220">Cuando se combina con **MCI \_ set \_ OFF**, se excluyen los datos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ea21b-220">When combined with **MCI\_SET\_OFF**, video data is excluded.</span></span> <span data-ttu-id="ea21b-221">El valor predeterminado incluye datos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ea21b-221">The default includes video data.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-222"><span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>MCI \_ DGV \_ SETVIDEO \_ \_ número src</span><span class="sxs-lookup"><span data-stu-id="ea21b-222"><span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>MCI\_DGV\_SETVIDEO\_SRC\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-223">Se especifica un número para el origen de vídeo en el miembro **dwSourceNumber** de la estructura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="ea21b-223">A number for the video source is specified in the **dwSourceNumber** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="ea21b-224">Si hay más de una entrada del tipo especificado por el **\_ \_ \_ valor SETVIDEO de MCI DGV**, el valor selecciona la entrada.</span><span class="sxs-lookup"><span data-stu-id="ea21b-224">If there is more than one input of the type specified by **MCI\_DGV\_SETVIDEO\_VALUE**, the value selects the input.</span></span> <span data-ttu-id="ea21b-225">Esta marca siempre debe usarse con **el \_ \_ \_ origen MCI DGV SETVIDEO**.</span><span class="sxs-lookup"><span data-stu-id="ea21b-225">This flag must always be used with **MCI\_DGV\_SETVIDEO\_SOURCE**.</span></span> <span data-ttu-id="ea21b-226">Sin embargo, si se omite **MCI \_ DGV \_ SETVIDEO \_ Value** , el número de origen especificado indica el origen absoluto que se usará como se especifica en el comando [MCI \_ List](mci-list.md) .</span><span class="sxs-lookup"><span data-stu-id="ea21b-226">If **MCI\_DGV\_SETVIDEO\_VALUE** is omitted, however, the specified source number indicates the absolute source to use as specified in the [MCI\_LIST](mci-list.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-227"><span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>MCI \_ DGV \_ SETVIDEO \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-227"><span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>MCI\_DGV\_SETVIDEO\_STILL</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-228">El nombre del algoritmo o el valor de calidad especificado se aplica a las imágenes fijas.</span><span class="sxs-lookup"><span data-stu-id="ea21b-228">The algorithm name or quality value specified applies to still images.</span></span>

<span data-ttu-id="ea21b-229">Cada controlador de dispositivo debe admitir un algoritmo de "ninguno", lo que significa que no hay compresión.</span><span class="sxs-lookup"><span data-stu-id="ea21b-229">Every device driver must support an algorithm of "none", which means no compression.</span></span> <span data-ttu-id="ea21b-230">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ea21b-230">This is the default.</span></span> <span data-ttu-id="ea21b-231">En este caso, los dispositivos de vídeo digital guardan las imágenes seguidas como mapas de bits independientes del dispositivo RGB (DIB).</span><span class="sxs-lookup"><span data-stu-id="ea21b-231">In this case, digital-video devices save still images as RGB device-independent bitmaps (DIBs).</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-232"><span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>\_ \_ valor SETVIDEO de MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-232"><span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>MCI\_DGV\_SETVIDEO\_VALUE</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-233">Un valor se incluye en el miembro **dwValue** de la estructura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="ea21b-233">A value is included in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="ea21b-234">El significado del valor se especifica mediante la marca **de \_ \_ \_ elemento SETVIDEO DGV de MCI** .</span><span class="sxs-lookup"><span data-stu-id="ea21b-234">The meaning of the value is specified by the **MCI\_DGV\_SETVIDEO\_ITEM** flag.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-235"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>Desactivación de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-235"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-236">Deshabilita la salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ea21b-236">Disables video output.</span></span> <span data-ttu-id="ea21b-237">En el caso de los dispositivos de vídeo digital, al deshabilitar un vídeo, se establecen los píxeles del rectángulo de destino definido por el comando [MCI \_ Put](mci-put.md) (o su valor predeterminado, la región cliente de la ventana actual) en un color sólido, pero no tiene ningún efecto en el búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="ea21b-237">For digital-video devices, disabling video sets the pixels in the destination rectangle defined by the [MCI\_PUT](mci-put.md) command (or its default, the client region of the current window) to a solid color, but it has no effect on the frame buffer.</span></span> <span data-ttu-id="ea21b-238">Si lo desea, puede ocultar la ventana con el comando de la [ \_ ventana MCI](mci-window.md) .</span><span class="sxs-lookup"><span data-stu-id="ea21b-238">You can hide the window with the [MCI\_WINDOW](mci-window.md) command if desired.</span></span> <span data-ttu-id="ea21b-239">El origen del vídeo, ya sea el área de trabajo o una entrada externa, puede continuar almacenando imágenes nuevas en el búfer de fotogramas, pero no se muestran hasta que se habilite el vídeo.</span><span class="sxs-lookup"><span data-stu-id="ea21b-239">The source of video, whether it's the workspace or an external input, might continue to store new images in the frame buffer, but they are not displayed until the video is enabled.</span></span> <span data-ttu-id="ea21b-240">Mientras que las aplicaciones deben usar el \_ comando MCI SETVIDEO para controlar esta función, los dispositivos de vídeo digital deben seguir admitiendo esta marca.</span><span class="sxs-lookup"><span data-stu-id="ea21b-240">While applications should use the MCI\_SETVIDEO command to control this function, digital-video devices must still support this flag.</span></span> <span data-ttu-id="ea21b-241">El valor predeterminado después de un abierto es on.</span><span class="sxs-lookup"><span data-stu-id="ea21b-241">The default value after an open is on.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-242"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activado \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-242"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-243">Habilita la salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ea21b-243">Enables video output.</span></span>

</dd> </dl>

<span data-ttu-id="ea21b-244">En el caso de los dispositivos de vídeo digital, el parámetro *lpSetVideo* apunta a una estructura [**MCI \_ DGV \_ SETVIDEO \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="ea21b-244">For digital-video devices, the *lpSetVideo* parameter points to an [**MCI\_DGV\_SETVIDEO\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa) structure.</span></span>

<span data-ttu-id="ea21b-245">Se usan las siguientes marcas adicionales con el tipo de dispositivo "VCR":</span><span class="sxs-lookup"><span data-stu-id="ea21b-245">The following additional flags are used with the "vcr" device type:</span></span>

<dl> <dt>

<span data-ttu-id="ea21b-246"><span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>\_registro de \_ SETVIDEO de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-246"><span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>MCI\_VCR\_SETVIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-247">Establece la grabación de vídeo en activado o desactivado.</span><span class="sxs-lookup"><span data-stu-id="ea21b-247">Sets the video recording to on or off.</span></span> <span data-ttu-id="ea21b-248">Se usa junto con una de las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="ea21b-248">Used in conjunction with one of following flags:</span></span>

-   <span data-ttu-id="ea21b-249">**MCI \_ ESTABLEZCA \_ en**.</span><span class="sxs-lookup"><span data-stu-id="ea21b-249">**MCI\_SET\_ON**.</span></span> <span data-ttu-id="ea21b-250">Grabación de vídeo activada.</span><span class="sxs-lookup"><span data-stu-id="ea21b-250">Video recording on.</span></span>
-   <span data-ttu-id="ea21b-251">**MCI \_ ESTABLECER como \_ desactivado**.</span><span class="sxs-lookup"><span data-stu-id="ea21b-251">**MCI\_SET\_OFF**.</span></span> <span data-ttu-id="ea21b-252">Grabación de vídeo desactivada.</span><span class="sxs-lookup"><span data-stu-id="ea21b-252">Video recording off.</span></span> <span data-ttu-id="ea21b-253">Es posible que sea necesario desactivar primero la grabación de ensamblados (con el comando [MCI \_ set](mci-set.md) con la marca de montaje del conjunto de VCR de MCI establecida en OFF) antes de que se pueda desactivar la grabación de vídeo. **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ea21b-253">It might be necessary to first turn off the assemble recording (using the [MCI\_SET](mci-set.md) command with the **MCI\_VCR\_SET\_ASSEMBLE\_RECORD** flag set to off) before the video recording can be turned off.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-254"><span id="MCI_TRACK"></span><span id="mci_track"></span>pista de MCI \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-254"><span id="MCI_TRACK"></span><span id="mci_track"></span>MCI\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-255">El miembro **dwTrack** de la estructura identificada por *lpSetVideo* especifica qué pista se ve afectada por el comando.</span><span class="sxs-lookup"><span data-stu-id="ea21b-255">The **dwTrack** member of the structure identified by *lpSetVideo* specifies which track is affected by the command.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-256"><span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>\_origen de \_ SETVIDEO de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-256"><span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>MCI\_VCR\_SETVIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-257">Establece el origen del vídeo y debe usarse con el **\_ VCR VCR \_ SETVIDEO \_ para** marcarlo.</span><span class="sxs-lookup"><span data-stu-id="ea21b-257">Sets the video source, and must be used with the **MCI\_VCR\_SETVIDEO\_TO** flag.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-258"><span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>\_monitor de \_ SETVIDEO de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-258"><span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>MCI\_VCR\_SETVIDEO\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-259">Establece el monitor de origen de vídeo y debe usarse con el \_ VCR VCR \_ SETVIDEO \_ para marcarlo.</span><span class="sxs-lookup"><span data-stu-id="ea21b-259">Sets the video source monitor, and must be used with the MCI\_VCR\_SETVIDEO\_TO flag.</span></span>

</dd> <dt>

<span data-ttu-id="ea21b-260"><span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>MCI \_ VCR \_ SETVIDEO \_</span><span class="sxs-lookup"><span data-stu-id="ea21b-260"><span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>MCI\_VCR\_SETVIDEO\_TO</span></span>
</dt> <dd>

<span data-ttu-id="ea21b-261">El miembro **dwTo** de la estructura identificada por *lpSetVideo* contiene una de las constantes siguientes:</span><span class="sxs-lookup"><span data-stu-id="ea21b-261">The **dwTo** member of the structure identified by *lpSetVideo* contains one of the following constants:</span></span>

<dl> <dd><span data-ttu-id="ea21b-262">**\_ \_ \_ sintonizador de tipo \_ src VCR de MCI**</span><span class="sxs-lookup"><span data-stu-id="ea21b-262">**MCI\_VCR\_SRC\_TYPE\_TUNER**</span></span></dd> <dd><span data-ttu-id="ea21b-263">**\_línea de \_ \_ tipo src VCR de \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="ea21b-263">**MCI\_VCR\_SRC\_TYPE\_LINE**</span></span></dd> <dd><span data-ttu-id="ea21b-264">**tipo de origen de VCR de MCI \_ \_ \_ \_ AUX**</span><span class="sxs-lookup"><span data-stu-id="ea21b-264">**MCI\_VCR\_SRC\_TYPE\_AUX**</span></span></dd> <dd><span data-ttu-id="ea21b-265">**tipo de origen de VCR de MCI \_ \_ \_ \_ genérico**</span><span class="sxs-lookup"><span data-stu-id="ea21b-265">**MCI\_VCR\_SRC\_TYPE\_GENERIC**</span></span></dd> <dd><span data-ttu-id="ea21b-266">**Desactivación de \_ \_ tipo src VCR \_ de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="ea21b-266">**MCI\_VCR\_SRC\_TYPE\_MUTE**</span></span></dd> <dd><span data-ttu-id="ea21b-267">**\_salida de \_ tipo de origen de VCR de MCI \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ea21b-267">**MCI\_VCR\_SRC\_TYPE\_OUTPUT**</span></span></dd> <dd><span data-ttu-id="ea21b-268">**tipo de origen de VCR de MCI \_ \_ \_ \_ RGB**</span><span class="sxs-lookup"><span data-stu-id="ea21b-268">**MCI\_VCR\_SRC\_TYPE\_RGB**</span></span></dd> <dd><span data-ttu-id="ea21b-269">**\_ \_ número SETVIDEO de VCR de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="ea21b-269">**MCI\_VCR\_SETVIDEO\_NUMBER**</span></span></dd> </dl>

<span data-ttu-id="ea21b-270">El miembro **dwNumber** de la estructura identificada por *lpSetVideo* contiene la entrada de vídeo (del tipo especificado en el miembro **dwTo** ) que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="ea21b-270">The **dwNumber** member of the structure identified by *lpSetVideo* contains the video input (of the type specified in the **dwTo** member) to use.</span></span>

</dd> </dl>

<span data-ttu-id="ea21b-271">En el caso de los dispositivos VCR, el parámetro *lpSetVideo* apunta a una estructura [**MCI \_ VCR \_ SETVIDEO \_ parms**](mci-vcr-setvideo-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="ea21b-271">For VCR devices, the *lpSetVideo* parameter points to an [**MCI\_VCR\_SETVIDEO\_PARMS**](mci-vcr-setvideo-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea21b-272">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea21b-272">Requirements</span></span>



| <span data-ttu-id="ea21b-273">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea21b-273">Requirement</span></span> | <span data-ttu-id="ea21b-274">Value</span><span class="sxs-lookup"><span data-stu-id="ea21b-274">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea21b-275">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea21b-275">Minimum supported client</span></span><br/> | <span data-ttu-id="ea21b-276">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ea21b-276">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ea21b-277">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea21b-277">Minimum supported server</span></span><br/> | <span data-ttu-id="ea21b-278">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ea21b-278">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ea21b-279">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea21b-279">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea21b-280"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea21b-280"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea21b-281">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea21b-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea21b-282">MCI</span><span class="sxs-lookup"><span data-stu-id="ea21b-282">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ea21b-283">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="ea21b-283">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

