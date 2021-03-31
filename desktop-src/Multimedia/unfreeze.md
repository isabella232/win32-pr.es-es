---
title: unfreeze (comando)
description: El comando unfreeze permite volver a habilitar la adquisición de vídeo en el búfer de fotogramas después de que el comando Freeze lo haya deshabilitado. Los dispositivos digitales-vídeo, VCR y superposición de vídeo reconocen este comando.
ms.assetid: ca90c299-2003-44cb-a879-4bc767480965
keywords:
- unfreeze (comando) multimedia de Windows
topic_type:
- apiref
api_name:
- unfreeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 155ba6b65fb08411d8404920c8f3337d1bddbcb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803818"
---
# <a name="unfreeze-command"></a><span data-ttu-id="aea9b-105">unfreeze (comando)</span><span class="sxs-lookup"><span data-stu-id="aea9b-105">unfreeze command</span></span>

<span data-ttu-id="aea9b-106">El comando unfreeze permite volver a habilitar la adquisición de vídeo en el búfer de fotogramas después de que el comando [Freeze](freeze.md) lo haya deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="aea9b-106">The unfreeze command reenables video acquisition to the frame buffer after it has been disabled by the [freeze](freeze.md) command.</span></span> <span data-ttu-id="aea9b-107">Los dispositivos digitales-vídeo, VCR y superposición de vídeo reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="aea9b-107">Digital-video, VCR, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="aea9b-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="aea9b-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("unfreeze %s %s %s"), 
  lpszDeviceID, 
  lpszUnfreeze, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="aea9b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aea9b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aea9b-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="aea9b-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="aea9b-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="aea9b-111">Identifier of an MCI device.</span></span> <span data-ttu-id="aea9b-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aea9b-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="aea9b-113"><span id="lpszUnfreeze"></span><span id="lpszunfreeze"></span><span id="LPSZUNFREEZE"></span>*lpszUnfreeze*</span><span class="sxs-lookup"><span data-stu-id="aea9b-113"><span id="lpszUnfreeze"></span><span id="lpszunfreeze"></span><span id="LPSZUNFREEZE"></span>*lpszUnfreeze*</span></span>
</dt> <dd>

<span data-ttu-id="aea9b-114">Marca para volver a habilitar la adquisición de vídeo en el búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="aea9b-114">Flag for reenabling video acquisition to the frame buffer.</span></span> <span data-ttu-id="aea9b-115">En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **unfreeze** y las marcas usadas por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="aea9b-115">The following table lists device types that recognize the **unfreeze** command and the flags used by each type.</span></span>



| <span data-ttu-id="aea9b-116">Value</span><span class="sxs-lookup"><span data-stu-id="aea9b-116">Value</span></span>        | <span data-ttu-id="aea9b-117">Significado</span><span class="sxs-lookup"><span data-stu-id="aea9b-117">Meaning</span></span>        |
|--------------|----------------|
| <span data-ttu-id="aea9b-118">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="aea9b-118">digitalvideo</span></span> | <span data-ttu-id="aea9b-119">en el *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="aea9b-119">at *rectangle*</span></span> |
| <span data-ttu-id="aea9b-120">overlay</span><span class="sxs-lookup"><span data-stu-id="aea9b-120">overlay</span></span>      | <span data-ttu-id="aea9b-121">en el *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="aea9b-121">at *rectangle*</span></span> |
| <span data-ttu-id="aea9b-122">vídeos</span><span class="sxs-lookup"><span data-stu-id="aea9b-122">vcr</span></span>          | <span data-ttu-id="aea9b-123">salida de entrada</span><span class="sxs-lookup"><span data-stu-id="aea9b-123">input output</span></span>   |



 

<span data-ttu-id="aea9b-124">En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszUnfreeze** y su significado.</span><span class="sxs-lookup"><span data-stu-id="aea9b-124">The following table lists the flags that can be specified in the **lpszUnfreeze** parameter and their meanings.</span></span>



| <span data-ttu-id="aea9b-125">Value</span><span class="sxs-lookup"><span data-stu-id="aea9b-125">Value</span></span>          | <span data-ttu-id="aea9b-126">Significado</span><span class="sxs-lookup"><span data-stu-id="aea9b-126">Meaning</span></span>                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aea9b-127">en el *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="aea9b-127">at *rectangle*</span></span> | <span data-ttu-id="aea9b-128">Especifica la región en la que se volverá a habilitar la adquisición de vídeo.</span><span class="sxs-lookup"><span data-stu-id="aea9b-128">Specifies the region that will have video acquisition reenabled.</span></span> <span data-ttu-id="aea9b-129">El rectángulo es relativo al origen del búfer de vídeo y se especifica como *x1 Y1 x2 Y2*.</span><span class="sxs-lookup"><span data-stu-id="aea9b-129">The rectangle is relative to the video buffer origin and is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="aea9b-130">Las coordenadas *x1 Y1* especifican la esquina superior izquierda del rectángulo y las coordenadas *x2 Y2* especifican el ancho y el alto.</span><span class="sxs-lookup"><span data-stu-id="aea9b-130">The coordinates *X1 Y1* specify the upper left corner of the rectangle, and the coordinates *X2 Y2* specify the width and height.</span></span> |
| <span data-ttu-id="aea9b-131">input</span><span class="sxs-lookup"><span data-stu-id="aea9b-131">input</span></span>          | <span data-ttu-id="aea9b-132">Libere la imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="aea9b-132">Unfreeze the input image.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="aea9b-133">output</span><span class="sxs-lookup"><span data-stu-id="aea9b-133">output</span></span>         | <span data-ttu-id="aea9b-134">Libere la imagen de salida.</span><span class="sxs-lookup"><span data-stu-id="aea9b-134">Unfreeze the output image.</span></span> <span data-ttu-id="aea9b-135">Si no se especifica "Input" ni "Output", se asume "Output".</span><span class="sxs-lookup"><span data-stu-id="aea9b-135">If neither "input" nor "output" is given, "output" is assumed.</span></span>                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="aea9b-136"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="aea9b-136"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="aea9b-137">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="aea9b-137">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="aea9b-138">En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba".</span><span class="sxs-lookup"><span data-stu-id="aea9b-138">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="aea9b-139">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="aea9b-139">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aea9b-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aea9b-140">Return Value</span></span>

<span data-ttu-id="aea9b-141">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="aea9b-141">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="aea9b-142">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="aea9b-142">Examples</span></span>

<span data-ttu-id="aea9b-143">El siguiente comando libera una región del búfer de vídeo.</span><span class="sxs-lookup"><span data-stu-id="aea9b-143">The following command unfreezes a region of the video buffer.</span></span>

``` syntax
unfreeze vboard at 10 20 90 165
```

## <a name="requirements"></a><span data-ttu-id="aea9b-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aea9b-144">Requirements</span></span>



| <span data-ttu-id="aea9b-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="aea9b-145">Requirement</span></span> | <span data-ttu-id="aea9b-146">Value</span><span class="sxs-lookup"><span data-stu-id="aea9b-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="aea9b-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aea9b-147">Minimum supported client</span></span><br/> | <span data-ttu-id="aea9b-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="aea9b-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="aea9b-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aea9b-149">Minimum supported server</span></span><br/> | <span data-ttu-id="aea9b-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aea9b-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="aea9b-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="aea9b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aea9b-152">MCI</span><span class="sxs-lookup"><span data-stu-id="aea9b-152">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="aea9b-153">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="aea9b-153">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="aea9b-154">Inmovilice</span><span class="sxs-lookup"><span data-stu-id="aea9b-154">freeze</span></span>](freeze.md)
</dt> </dl>

 

