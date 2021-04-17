---
title: comando de calidad
description: El comando calidad define un nivel de calidad personalizado para la compresión de datos audio, vídeo o imagen fija. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: cc920ec9-362c-43db-808e-b9fb59d1df6d
keywords:
- comando de calidad multimedia de Windows
topic_type:
- apiref
api_name:
- quality
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de9cc61d72db541b5f06d8903d7c9dcf153ce07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666065"
---
# <a name="quality-command"></a><span data-ttu-id="0a9e3-105">comando de calidad</span><span class="sxs-lookup"><span data-stu-id="0a9e3-105">quality command</span></span>

<span data-ttu-id="0a9e3-106">El comando calidad define un nivel de calidad personalizado para la compresión de datos audio, vídeo o imagen fija.</span><span class="sxs-lookup"><span data-stu-id="0a9e3-106">The quality command defines a custom quality level for either audio, video or still image data compression.</span></span> <span data-ttu-id="0a9e3-107">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="0a9e3-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="0a9e3-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="0a9e3-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("quality %s %s %s"), 
  lpszDeviceID, 
  lpszQuality, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="0a9e3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a9e3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a9e3-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="0a9e3-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="0a9e3-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="0a9e3-111">Identifier of an MCI device.</span></span> <span data-ttu-id="0a9e3-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a9e3-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="0a9e3-113"><span id="lpszQuality"></span><span id="lpszquality"></span><span id="LPSZQUALITY"></span>*lpszQuality*</span><span class="sxs-lookup"><span data-stu-id="0a9e3-113"><span id="lpszQuality"></span><span id="lpszquality"></span><span id="LPSZQUALITY"></span>*lpszQuality*</span></span>
</dt> <dd>

<span data-ttu-id="0a9e3-114">Una o varias de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="0a9e3-114">One or more of the following flags.</span></span> <span data-ttu-id="0a9e3-115">(Una de las tres marcas "audio", "todavía" y "vídeo" debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="0a9e3-115">(One of the three flags "audio", "still", and "video" must be present.)</span></span>



| <span data-ttu-id="0a9e3-116">Value</span><span class="sxs-lookup"><span data-stu-id="0a9e3-116">Value</span></span>                 | <span data-ttu-id="0a9e3-117">Significado</span><span class="sxs-lookup"><span data-stu-id="0a9e3-117">Meaning</span></span>                                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a9e3-118">*algoritmo* de algoritmo</span><span class="sxs-lookup"><span data-stu-id="0a9e3-118">algorithm *algorithm*</span></span> | <span data-ttu-id="0a9e3-119">Asocia el nivel de calidad con el *algoritmo* especificado.</span><span class="sxs-lookup"><span data-stu-id="0a9e3-119">Associates the quality level with the specified *algorithm*.</span></span> <span data-ttu-id="0a9e3-120">Este *algoritmo* debe ser compatible con el dispositivo y ser compatible con la marca "audio", "todavía" o "vídeo" que se usa.</span><span class="sxs-lookup"><span data-stu-id="0a9e3-120">This *algorithm* must be supported by the device and be compatible with the "audio", "still", or "video" flag that is used.</span></span> <span data-ttu-id="0a9e3-121">Si se omite, se usa el algoritmo actual.</span><span class="sxs-lookup"><span data-stu-id="0a9e3-121">If omitted, the current algorithm is used.</span></span> |
| <span data-ttu-id="0a9e3-122">*nombre* de audio</span><span class="sxs-lookup"><span data-stu-id="0a9e3-122">audio *name*</span></span>          | <span data-ttu-id="0a9e3-123">Indica que este comando especifica un nivel de calidad de "audio" identificado con *el nombre*.</span><span class="sxs-lookup"><span data-stu-id="0a9e3-123">Indicates this command specifies an "audio" quality level identified with *name*.</span></span>                                                                                                                                                   |
| <span data-ttu-id="0a9e3-124">diálogo</span><span class="sxs-lookup"><span data-stu-id="0a9e3-124">dialog</span></span>                | <span data-ttu-id="0a9e3-125">Solicita que el dispositivo muestre un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0a9e3-125">Requests that the device display a dialog box.</span></span> <span data-ttu-id="0a9e3-126">Este cuadro de diálogo tiene campos específicos del algoritmo que el dispositivo usa internamente para crear la estructura que describe un nivel de calidad específico.</span><span class="sxs-lookup"><span data-stu-id="0a9e3-126">This dialog box has algorithm-specific fields that are used internally by the device to create the structure describing a specific quality level.</span></span>                                    |
| <span data-ttu-id="0a9e3-127">identificador *de controlador*</span><span class="sxs-lookup"><span data-stu-id="0a9e3-127">handle *handle*</span></span>       | <span data-ttu-id="0a9e3-128">Especifica un *identificador* para una estructura que contiene datos específicos del algoritmo que describen un nivel de calidad específico.</span><span class="sxs-lookup"><span data-stu-id="0a9e3-128">Specifies a *handle* to a structure that contains algorithmic-specific data describing a specific quality level.</span></span> <span data-ttu-id="0a9e3-129">Las estructuras de los datos a los que hace referencia este identificador son específicas del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a9e3-129">The structures for the data referenced by this handle are device specific.</span></span>                                         |
| <span data-ttu-id="0a9e3-130">*nombre* todavía</span><span class="sxs-lookup"><span data-stu-id="0a9e3-130">still *name*</span></span>          | <span data-ttu-id="0a9e3-131">Indica que el comando especifica un nivel de calidad "todavía" identificado con *el nombre.*</span><span class="sxs-lookup"><span data-stu-id="0a9e3-131">Indicates the command specifies a "still" quality level identified with *name.*</span></span>                                                                                                                                                     |
| <span data-ttu-id="0a9e3-132">*nombre* de vídeo</span><span class="sxs-lookup"><span data-stu-id="0a9e3-132">video *name*</span></span>          | <span data-ttu-id="0a9e3-133">Indica que el comando especifica un nivel de calidad "vídeo" identificado con *el nombre*.</span><span class="sxs-lookup"><span data-stu-id="0a9e3-133">Indicates the command specifies a "video" quality level identified with *name*.</span></span>                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="0a9e3-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="0a9e3-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0a9e3-135">Puede ser "Wait", "Notify", "Test" o una combinación de estos.</span><span class="sxs-lookup"><span data-stu-id="0a9e3-135">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="0a9e3-136">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0a9e3-136">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a9e3-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a9e3-137">Return Value</span></span>

<span data-ttu-id="0a9e3-138">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0a9e3-138">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a9e3-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a9e3-139">Remarks</span></span>

<span data-ttu-id="0a9e3-140">Este comando define un nombre de cadena para el nivel de calidad, que se puede usar en un comando [setvideo](setvideo.md) "Quality", setvideo "Quality" o [SetAudio](setaudio.md) "Quality" para establecerlo como el nivel de calidad de vídeo, todavía o compresión de audio actual.</span><span class="sxs-lookup"><span data-stu-id="0a9e3-140">This command defines a string name for the quality level, which can then be used in a [setvideo](setvideo.md) "quality", setvideo "still quality", or [setaudio](setaudio.md) "quality" command to establish it as the current video, still, or audio-compression quality level.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a9e3-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a9e3-141">Requirements</span></span>



| <span data-ttu-id="0a9e3-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a9e3-142">Requirement</span></span> | <span data-ttu-id="0a9e3-143">Value</span><span class="sxs-lookup"><span data-stu-id="0a9e3-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0a9e3-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a9e3-144">Minimum supported client</span></span><br/> | <span data-ttu-id="0a9e3-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0a9e3-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0a9e3-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a9e3-146">Minimum supported server</span></span><br/> | <span data-ttu-id="0a9e3-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0a9e3-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0a9e3-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a9e3-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a9e3-149">MCI</span><span class="sxs-lookup"><span data-stu-id="0a9e3-149">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0a9e3-150">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="0a9e3-150">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="0a9e3-151">setaudio</span><span class="sxs-lookup"><span data-stu-id="0a9e3-151">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="0a9e3-152">setvideo</span><span class="sxs-lookup"><span data-stu-id="0a9e3-152">setvideo</span></span>](setvideo.md)
</dt> </dl>

 

