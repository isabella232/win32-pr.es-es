---
title: Put (comando)
description: El comando Put define el área de la imagen de origen y la ventana de destino que se usan para la presentación. Los dispositivos de vídeo digital y de superposición reconocen este comando.
ms.assetid: 55fb7192-2083-45e7-a0bf-0d72a6320f91
keywords:
- poner comando en Windows multimedia
topic_type:
- apiref
api_name:
- put
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d22fb7c74c1ed469e609e7dcfdd3d36ba355cc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150961"
---
# <a name="put-command"></a><span data-ttu-id="882f2-105">Put (comando)</span><span class="sxs-lookup"><span data-stu-id="882f2-105">put command</span></span>

<span data-ttu-id="882f2-106">El comando Put define el área de la imagen de origen y la ventana de destino que se usan para la presentación.</span><span class="sxs-lookup"><span data-stu-id="882f2-106">The put command defines the area of the source image and destination window used for display.</span></span> <span data-ttu-id="882f2-107">Los dispositivos de vídeo digital y de superposición reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="882f2-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="882f2-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="882f2-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("put %s %s %s"), 
  lpszDeviceID, 
  lpszRegions, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="882f2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="882f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="882f2-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="882f2-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="882f2-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="882f2-111">Identifier of an MCI device.</span></span> <span data-ttu-id="882f2-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="882f2-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="882f2-113"><span id="lpszRegions"></span><span id="lpszregions"></span><span id="LPSZREGIONS"></span>*lpszRegions*</span><span class="sxs-lookup"><span data-stu-id="882f2-113"><span id="lpszRegions"></span><span id="lpszregions"></span><span id="LPSZREGIONS"></span>*lpszRegions*</span></span>
</dt> <dd>

<span data-ttu-id="882f2-114">Marca para definir el área.</span><span class="sxs-lookup"><span data-stu-id="882f2-114">Flag for defining the area.</span></span> <span data-ttu-id="882f2-115">En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando Put y las marcas usadas por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="882f2-115">The following table lists device types that recognize the put command and the flags used by each type.</span></span>



| <span data-ttu-id="882f2-116">Value</span><span class="sxs-lookup"><span data-stu-id="882f2-116">Value</span></span>        | <span data-ttu-id="882f2-117">Significado</span><span class="sxs-lookup"><span data-stu-id="882f2-117">Meaning</span></span>                                                                                      | <span data-ttu-id="882f2-118">Significado</span><span class="sxs-lookup"><span data-stu-id="882f2-118">Meaning</span></span>                                                                                          |
|--------------|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="882f2-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="882f2-119">digitalvideo</span></span> | <span data-ttu-id="882f2-120">destino de destino *en el* marco del marco del rectángulo en el origen del *rectángulo* de origen en el *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="882f2-120">destination destination at *rectangle* frame frame at *rectangle* source source at *rectangle*</span></span> | <span data-ttu-id="882f2-121">vídeo en vídeo en la ventana de la ventana de *rectángulo* en la ventana de *rectángulo* cliente Window Client en *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="882f2-121">video video at *rectangle* window window at *rectangle* window client window client at *rectangle*</span></span> |
| <span data-ttu-id="882f2-122">overlay</span><span class="sxs-lookup"><span data-stu-id="882f2-122">overlay</span></span>      | <span data-ttu-id="882f2-123">destino de destino en el marco del marco del *rectángulo* en el *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="882f2-123">destination destination at *rectangle* frame frame at *rectangle*</span></span>                             | <span data-ttu-id="882f2-124">vídeo de origen en vídeo en rectángulo *en el* rectángulo</span><span class="sxs-lookup"><span data-stu-id="882f2-124">source source at *rectangle* video video at *rectangle*</span></span>                                           |



 

<span data-ttu-id="882f2-125">En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszRegions** y su significado.</span><span class="sxs-lookup"><span data-stu-id="882f2-125">The following table lists the flags that can be specified in the **lpszRegions** parameter and their meanings.</span></span>



| <span data-ttu-id="882f2-126">Value</span><span class="sxs-lookup"><span data-stu-id="882f2-126">Value</span></span>                        | <span data-ttu-id="882f2-127">Significado</span><span class="sxs-lookup"><span data-stu-id="882f2-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="882f2-128">destination</span><span class="sxs-lookup"><span data-stu-id="882f2-128">destination</span></span>                  | <span data-ttu-id="882f2-129">Selecciona el área de cliente completa de la ventana de destino para mostrar los datos.</span><span class="sxs-lookup"><span data-stu-id="882f2-129">Selects the entire client area of the destination window to display the data.</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="882f2-130">destino en el *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="882f2-130">destination at *rectangle*</span></span>   | <span data-ttu-id="882f2-131">Selecciona una parte del área de cliente de la ventana de destino que se usa para mostrar la imagen.</span><span class="sxs-lookup"><span data-stu-id="882f2-131">Selects a portion of the client area of the destination window used to display the image.</span></span> <span data-ttu-id="882f2-132">Cuando se especifica un área de la ventana de presentación y el dispositivo admite la expansión, la imagen de origen se ajusta al desplazamiento y la extensión de destino.</span><span class="sxs-lookup"><span data-stu-id="882f2-132">When an area of the display window is specified and the device supports stretching, the source image is stretched to the destination offset and extent.</span></span>                                                                                                     |
| <span data-ttu-id="882f2-133">frame</span><span class="sxs-lookup"><span data-stu-id="882f2-133">frame</span></span>                        | <span data-ttu-id="882f2-134">Selecciona todo el búfer de fotogramas para recibir las imágenes de vídeo entrantes.</span><span class="sxs-lookup"><span data-stu-id="882f2-134">Selects the entire frame buffer to receive the incoming video images.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="882f2-135">marco en *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="882f2-135">frame at *rectangle*</span></span>         | <span data-ttu-id="882f2-136">Selecciona una parte del búfer de fotogramas para recibir las imágenes de vídeo entrantes.</span><span class="sxs-lookup"><span data-stu-id="882f2-136">Selects a portion of the frame buffer to receive the incoming video images.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="882f2-137">source</span><span class="sxs-lookup"><span data-stu-id="882f2-137">source</span></span>                       | <span data-ttu-id="882f2-138">Selecciona toda la imagen que se va a mostrar en la ventana de destino.</span><span class="sxs-lookup"><span data-stu-id="882f2-138">Selects the entire image for display in the destination window.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="882f2-139">origen en el *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="882f2-139">source at *rectangle*</span></span>        | <span data-ttu-id="882f2-140">Selecciona una parte de la imagen que se va a mostrar en la ventana de destino.</span><span class="sxs-lookup"><span data-stu-id="882f2-140">Selects a portion of the image to display in the destination window.</span></span> <span data-ttu-id="882f2-141">Cuando se especifica un área de la imagen de origen y el dispositivo admite la expansión, la imagen de origen se ajusta al desplazamiento y la extensión de destino.</span><span class="sxs-lookup"><span data-stu-id="882f2-141">When an area of the source image is specified, and the device supports stretching, the source image is stretched to the destination offset and extent.</span></span>                                                                                                                           |
| <span data-ttu-id="882f2-142">video</span><span class="sxs-lookup"><span data-stu-id="882f2-142">video</span></span>                        | <span data-ttu-id="882f2-143">Selecciona la imagen de vídeo entrante completa que se va a capturar en el búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="882f2-143">Selects the entire incoming video image to capture in the frame buffer.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="882f2-144">vídeo en *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="882f2-144">video at *rectangle*</span></span>         | <span data-ttu-id="882f2-145">Selecciona una parte de la imagen de vídeo entrante para capturar en el búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="882f2-145">Selects a portion of the incoming video image to capture in the frame buffer.</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="882f2-146">periodo</span><span class="sxs-lookup"><span data-stu-id="882f2-146">window</span></span>                       | <span data-ttu-id="882f2-147">Restaura el tamaño inicial de la ventana en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="882f2-147">Restores the initial window size on the display.</span></span> <span data-ttu-id="882f2-148">Este comando también muestra la ventana.</span><span class="sxs-lookup"><span data-stu-id="882f2-148">This command also displays the window.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="882f2-149">ventana en *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="882f2-149">window at *rectangle*</span></span>        | <span data-ttu-id="882f2-150">Cambia el tamaño y la ubicación de la ventana de presentación.</span><span class="sxs-lookup"><span data-stu-id="882f2-150">Changes the size and location of the display window.</span></span> <span data-ttu-id="882f2-151">El rectángulo especificado es relativo a la ventana primaria de la ventana de presentación (normalmente el escritorio) si se ha usado la marca "secundario de estilo" para el comando [abrir](open.md) .</span><span class="sxs-lookup"><span data-stu-id="882f2-151">The specified rectangle is relative to the parent window of the display window (usually the desktop) if the "style child" flag has been used for the [open](open.md) command.</span></span> <span data-ttu-id="882f2-152">Para cambiar la ubicación de la ventana sin cambiar su alto o ancho, especifique cero para el alto y el ancho.</span><span class="sxs-lookup"><span data-stu-id="882f2-152">To change the location of the window without changing its height or width, specify zero for the height and width.</span></span> |
| <span data-ttu-id="882f2-153">cliente de Windows</span><span class="sxs-lookup"><span data-stu-id="882f2-153">window client</span></span>                | <span data-ttu-id="882f2-154">Restaura el área cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="882f2-154">Restores the client area of the window.</span></span>                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="882f2-155">cliente de ventana en *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="882f2-155">window client at *rectangle*</span></span> | <span data-ttu-id="882f2-156">Cambia el tamaño y la ubicación del área de cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="882f2-156">Changes the size and location of the client area of the window.</span></span> <span data-ttu-id="882f2-157">El rectángulo especificado es relativo a la ventana primaria de la ventana de cliente.</span><span class="sxs-lookup"><span data-stu-id="882f2-157">The specified rectangle is relative to the parent window of the client window.</span></span> <span data-ttu-id="882f2-158">Para cambiar la ubicación de la ventana sin cambiar su alto o ancho, especifique cero para el alto y el ancho.</span><span class="sxs-lookup"><span data-stu-id="882f2-158">To change the location of the window without changing its height or width, specify zero for the height and width.</span></span>                                                                                      |



 

<span data-ttu-id="882f2-159">Cuando una marca incluye un rectángulo, las coordenadas del rectángulo se relacionan con el origen de la ventana o el origen de la imagen, según corresponda, y se especifican como **x1 Y1 x2 Y2**.</span><span class="sxs-lookup"><span data-stu-id="882f2-159">When a flag includes a rectangle, the rectangle coordinates are relative to the window origin or the image origin, as appropriate, and are specified as **X1 Y1 X2 Y2**.</span></span> <span data-ttu-id="882f2-160">Las coordenadas **X1Y1** especifican la esquina superior izquierda y las coordenadas **X2Y2** especifican el ancho y el alto del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="882f2-160">The coordinates **X1Y1** specify the upper left corner, and the coordinates **X2Y2** specify the width and height of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="882f2-161"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="882f2-161"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="882f2-162">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="882f2-162">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="882f2-163">En el caso de los dispositivos de vídeo digital, también se puede especificar "Test".</span><span class="sxs-lookup"><span data-stu-id="882f2-163">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="882f2-164">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="882f2-164">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="882f2-165">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="882f2-165">Return Value</span></span>

<span data-ttu-id="882f2-166">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="882f2-166">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="882f2-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="882f2-167">Remarks</span></span>

<span data-ttu-id="882f2-168">El comando Put define uno o varios de los siguientes rectángulos cuando se trabaja con dispositivos de superposición de vídeo:</span><span class="sxs-lookup"><span data-stu-id="882f2-168">The put command defines one or more of the following rectangles when working with video-overlay devices:</span></span>

-   <span data-ttu-id="882f2-169">El rectángulo de vídeo define la región de la imagen de vídeo entrante que se va a capturar.</span><span class="sxs-lookup"><span data-stu-id="882f2-169">The video rectangle defines the region of the incoming video image to capture.</span></span>
-   <span data-ttu-id="882f2-170">El rectángulo del marco define la región del búfer de fotogramas que recibe la imagen de vídeo entrante.</span><span class="sxs-lookup"><span data-stu-id="882f2-170">The frame rectangle defines the region of the frame buffer that receives the incoming video image.</span></span>
-   <span data-ttu-id="882f2-171">El rectángulo de origen define qué región del búfer de fotogramas se copia en el rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="882f2-171">The source rectangle defines which region of the frame buffer is copied to the destination rectangle.</span></span>
-   <span data-ttu-id="882f2-172">El rectángulo de destino define la región del área de cliente de la ventana de presentación que recibe la imagen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="882f2-172">The destination rectangle defines the region of the display window client area that receives the video image.</span></span>

<span data-ttu-id="882f2-173">El rectángulo de vídeo está relacionado con el rectángulo del marco de la misma manera que el rectángulo de origen está relacionado con el rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="882f2-173">The video rectangle is related to the frame rectangle in the same way the source rectangle is related to the destination rectangle.</span></span> <span data-ttu-id="882f2-174">La expansión puede producirse desde el rectángulo del vídeo hasta el rectángulo del marco y desde el rectángulo de origen hasta el rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="882f2-174">Stretching can occur from the video rectangle to the frame rectangle and from the source rectangle to the destination rectangle.</span></span> <span data-ttu-id="882f2-175">No todos los dispositivos admiten la ampliación y la expansión debe estar habilitada (mediante el comando [set](set.md) ).</span><span class="sxs-lookup"><span data-stu-id="882f2-175">Not all devices support stretching, and stretching must be enabled (by using the [set](set.md) command).</span></span>

<span data-ttu-id="882f2-176">El comando siguiente define tres regiones para el vídeo, el marco y el origen.</span><span class="sxs-lookup"><span data-stu-id="882f2-176">The following command defines three regions for the video, frame, and source.</span></span>

``` syntax
put vboard video 120 120 200 200 frame 0 0 200 200 source 0 0 200 200
```

<span data-ttu-id="882f2-177">Las regiones de este ejemplo se definen de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="882f2-177">The regions in this example are defined as follows:</span></span>

-   <span data-ttu-id="882f2-178">Una región de 200 x 200 píxeles de los datos de vídeo entrantes, a partir de un origen de 120 píxeles desde la esquina superior izquierda, se capturará en el búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="882f2-178">A 200- by 200-pixel region of the incoming video data, starting at an origin 120 pixels from the upper left corner, will be captured to the frame buffer.</span></span>
-   <span data-ttu-id="882f2-179">Los datos de vídeo se colocarán en una región de 200 x 200 píxeles en la esquina superior izquierda del búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="882f2-179">The video data will be placed in a 200- by 200-pixel region at the upper left corner of the frame buffer.</span></span>
-   <span data-ttu-id="882f2-180">Las transferencias se realizan desde la región 200-by 200-pixel en la esquina superior izquierda del búfer de fotogramas hasta la ventana de destino.</span><span class="sxs-lookup"><span data-stu-id="882f2-180">Transfers are made from the 200- by 200-pixel region at the upper left corner of the frame buffer to the destination window.</span></span>

## <a name="requirements"></a><span data-ttu-id="882f2-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="882f2-181">Requirements</span></span>



| <span data-ttu-id="882f2-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="882f2-182">Requirement</span></span> | <span data-ttu-id="882f2-183">Value</span><span class="sxs-lookup"><span data-stu-id="882f2-183">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="882f2-184">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="882f2-184">Minimum supported client</span></span><br/> | <span data-ttu-id="882f2-185">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="882f2-185">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="882f2-186">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="882f2-186">Minimum supported server</span></span><br/> | <span data-ttu-id="882f2-187">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="882f2-187">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="882f2-188">Vea también</span><span class="sxs-lookup"><span data-stu-id="882f2-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="882f2-189">MCI</span><span class="sxs-lookup"><span data-stu-id="882f2-189">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="882f2-190">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="882f2-190">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="882f2-191">open</span><span class="sxs-lookup"><span data-stu-id="882f2-191">open</span></span>](open.md)
</dt> <dt>

[<span data-ttu-id="882f2-192">set</span><span class="sxs-lookup"><span data-stu-id="882f2-192">set</span></span>](set.md)
</dt> </dl>

 

