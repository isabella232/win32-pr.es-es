---
title: Where (comando)
description: El comando Where recupera el rectángulo que especifica el área de origen o de destino. Este rectángulo se especificó mediante el comando Put. Los dispositivos de vídeo digital y de superposición reconocen este comando.
ms.assetid: 85c68ded-bd3e-4a48-9af7-58478615a7f0
keywords:
- comando Where Windows multimedia
topic_type:
- apiref
api_name:
- where
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c499eae8f0209c1ef93efb9677ae438dcf0e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996950"
---
# <a name="where-command"></a><span data-ttu-id="2e285-106">Where (comando)</span><span class="sxs-lookup"><span data-stu-id="2e285-106">where command</span></span>

<span data-ttu-id="2e285-107">El comando Where recupera el rectángulo que especifica el área de origen o de destino.</span><span class="sxs-lookup"><span data-stu-id="2e285-107">The where command retrieves the rectangle specifying the source or destination area.</span></span> <span data-ttu-id="2e285-108">Este rectángulo se especificó mediante el comando [Put](put.md) .</span><span class="sxs-lookup"><span data-stu-id="2e285-108">This rectangle was specified using the [put](put.md) command.</span></span> <span data-ttu-id="2e285-109">Los dispositivos de vídeo digital y de superposición reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="2e285-109">Digital-video, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="2e285-110">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="2e285-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("where %s %s %s"), 
  lpszDeviceID, 
  lpszRequestRect, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="2e285-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e285-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e285-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="2e285-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="2e285-113">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="2e285-113">Identifier of an MCI device.</span></span> <span data-ttu-id="2e285-114">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2e285-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="2e285-115"><span id="lpszRequestRect"></span><span id="lpszrequestrect"></span><span id="LPSZREQUESTRECT"></span>*lpszRequestRect*</span><span class="sxs-lookup"><span data-stu-id="2e285-115"><span id="lpszRequestRect"></span><span id="lpszrequestrect"></span><span id="LPSZREQUESTRECT"></span>*lpszRequestRect*</span></span>
</dt> <dd>

<span data-ttu-id="2e285-116">Marca que identifica el rectángulo cuyas dimensiones se recuperan.</span><span class="sxs-lookup"><span data-stu-id="2e285-116">Flag that identifies the rectangle whose dimensions are retrieved.</span></span> <span data-ttu-id="2e285-117">En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **Where** y las marcas usadas por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="2e285-117">The following table lists device types that recognize the **where** command and the flags used by each type.</span></span>



| <span data-ttu-id="2e285-118">Value</span><span class="sxs-lookup"><span data-stu-id="2e285-118">Value</span></span>        | <span data-ttu-id="2e285-119">Significado</span><span class="sxs-lookup"><span data-stu-id="2e285-119">Meaning</span></span>                                                       | <span data-ttu-id="2e285-120">Significado</span><span class="sxs-lookup"><span data-stu-id="2e285-120">Meaning</span></span>                                  |
|--------------|---------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="2e285-121">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="2e285-121">digitalvideo</span></span> | <span data-ttu-id="2e285-122">destinationdestination [**Max**](max.md)frameFrame maxsource</span><span class="sxs-lookup"><span data-stu-id="2e285-122">destinationdestination [**max**](max.md)frameframe maxsource</span></span> | <span data-ttu-id="2e285-123">Source maxvideovideo maxwindowwindow Max</span><span class="sxs-lookup"><span data-stu-id="2e285-123">source maxvideovideo maxwindowwindow max</span></span> |
| <span data-ttu-id="2e285-124">overlay</span><span class="sxs-lookup"><span data-stu-id="2e285-124">overlay</span></span>      | <span data-ttu-id="2e285-125">destinationframe</span><span class="sxs-lookup"><span data-stu-id="2e285-125">destinationframe</span></span>                                              | <span data-ttu-id="2e285-126">sourcevideo</span><span class="sxs-lookup"><span data-stu-id="2e285-126">sourcevideo</span></span>                              |



 

<span data-ttu-id="2e285-127">En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszRequestRect** y su significado.</span><span class="sxs-lookup"><span data-stu-id="2e285-127">The following table lists the flags that can be specified in the **lpszRequestRect** parameter and their meanings.</span></span>



| <span data-ttu-id="2e285-128">Value</span><span class="sxs-lookup"><span data-stu-id="2e285-128">Value</span></span>                          | <span data-ttu-id="2e285-129">Significado</span><span class="sxs-lookup"><span data-stu-id="2e285-129">Meaning</span></span>                                                                                                                                                                                                                                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e285-130">destination</span><span class="sxs-lookup"><span data-stu-id="2e285-130">destination</span></span>                    | <span data-ttu-id="2e285-131">Recupera el desplazamiento y la extensión de destino.</span><span class="sxs-lookup"><span data-stu-id="2e285-131">Retrieves the destination offset and extent.</span></span> <span data-ttu-id="2e285-132">En el caso de los dispositivos de superposición de vídeo, el rectángulo de destino define el área del área de cliente de la ventana de presentación que muestra los datos de imagen del búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2e285-132">For video-overlay devices, the destination rectangle defines the area of the display window client area that displays the image data from the frame buffer.</span></span>                                                                                             |
| <span data-ttu-id="2e285-133">destino [ **máximo**](max.md)</span><span class="sxs-lookup"><span data-stu-id="2e285-133">destination [**max**](max.md)</span></span> | <span data-ttu-id="2e285-134">Recupera el tamaño actual del rectángulo del cliente.</span><span class="sxs-lookup"><span data-stu-id="2e285-134">Retrieves the current size of the client rectangle.</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="2e285-135">frame</span><span class="sxs-lookup"><span data-stu-id="2e285-135">frame</span></span>                          | <span data-ttu-id="2e285-136">Recupera el desplazamiento y la extensión del rectángulo de búfer del marco.</span><span class="sxs-lookup"><span data-stu-id="2e285-136">Retrieves the offset and extent of the frame buffer rectangle.</span></span> <span data-ttu-id="2e285-137">El rectángulo de búfer de marco define el área del búfer de fotogramas que recibe los datos de vídeo entrantes.</span><span class="sxs-lookup"><span data-stu-id="2e285-137">The frame buffer rectangle defines the area of the frame buffer that receives incoming video data.</span></span> <span data-ttu-id="2e285-138">Las imágenes del rectángulo "vídeo" se escalan en esta región.</span><span class="sxs-lookup"><span data-stu-id="2e285-138">Images from the "video" rectangle are scaled into this region.</span></span>                                                                     |
| <span data-ttu-id="2e285-139">fotograma [ **máximo**](max.md)</span><span class="sxs-lookup"><span data-stu-id="2e285-139">frame [**max**](max.md)</span></span>       | <span data-ttu-id="2e285-140">Devuelve el tamaño máximo del búfer de marco.</span><span class="sxs-lookup"><span data-stu-id="2e285-140">Returns the maximum size of the frame buffer.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="2e285-141">source</span><span class="sxs-lookup"><span data-stu-id="2e285-141">source</span></span>                         | <span data-ttu-id="2e285-142">Recupera el desplazamiento de origen y la extensión.</span><span class="sxs-lookup"><span data-stu-id="2e285-142">Retrieves the source offset and extent.</span></span> <span data-ttu-id="2e285-143">En el caso de los dispositivos de superposición de vídeo, el rectángulo de origen define la región del búfer de fotogramas que se muestra en la ventana de destino.</span><span class="sxs-lookup"><span data-stu-id="2e285-143">For video-overlay devices, the source rectangle defines the region of the frame buffer that is displayed in the destination window.</span></span> <span data-ttu-id="2e285-144">El dispositivo usa este rectángulo para recortar la imagen antes de que se ajuste para ajustarse al rectángulo de destino de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="2e285-144">The device uses this rectangle to crop the image before it is stretched to fit the destination rectangle on the display.</span></span> |
| <span data-ttu-id="2e285-145">[ **número máximo** de orígenes](max.md)</span><span class="sxs-lookup"><span data-stu-id="2e285-145">source [**max**](max.md)</span></span>      | <span data-ttu-id="2e285-146">Recupera el tamaño máximo del búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2e285-146">Retrieves the maximum size of the frame buffer.</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="2e285-147">video</span><span class="sxs-lookup"><span data-stu-id="2e285-147">video</span></span>                          | <span data-ttu-id="2e285-148">Recupera el desplazamiento y la extensión del rectángulo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2e285-148">Retrieves the offset and extent of the video rectangle.</span></span> <span data-ttu-id="2e285-149">El rectángulo de vídeo define la región de los datos de vídeo entrantes que se transfieren al búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2e285-149">The video rectangle defines the region of the incoming video data that is transferred to the frame buffer.</span></span>                                                                                                                                   |
| <span data-ttu-id="2e285-150">vídeo [ **máx** .](max.md)</span><span class="sxs-lookup"><span data-stu-id="2e285-150">video [**max**](max.md)</span></span>       | <span data-ttu-id="2e285-151">Devuelve el tamaño máximo de la entrada.</span><span class="sxs-lookup"><span data-stu-id="2e285-151">Returns the maximum size of the input.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="2e285-152">periodo</span><span class="sxs-lookup"><span data-stu-id="2e285-152">window</span></span>                         | <span data-ttu-id="2e285-153">Recupera el tamaño y la posición actuales del marco de la ventana de presentación.</span><span class="sxs-lookup"><span data-stu-id="2e285-153">Retrieves the current size and position of the display-window frame.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="2e285-154">ventana [ **máx** .](max.md)</span><span class="sxs-lookup"><span data-stu-id="2e285-154">window [**max**](max.md)</span></span>      | <span data-ttu-id="2e285-155">Recupera el tamaño de la pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="2e285-155">Retrieves the size of the entire display.</span></span>                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="2e285-156"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="2e285-156"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="2e285-157">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="2e285-157">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="2e285-158">En el caso de los dispositivos de vídeo digital, también se puede especificar "Test".</span><span class="sxs-lookup"><span data-stu-id="2e285-158">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="2e285-159">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="2e285-159">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e285-160">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e285-160">Return Value</span></span>

<span data-ttu-id="2e285-161">Devuelve un rectángulo en el parámetro *lpszReturnString* de la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2e285-161">Returns a rectangle in the *lpszReturnString* parameter of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="2e285-162">El rectángulo describe el área especificada en el parámetro *lpszRequestRect* de este comando.</span><span class="sxs-lookup"><span data-stu-id="2e285-162">The rectangle describes the area specified in the *lpszRequestRect* parameter of this command.</span></span> <span data-ttu-id="2e285-163">El rectángulo se especifica como *x1 Y1 x2 Y2*.</span><span class="sxs-lookup"><span data-stu-id="2e285-163">The rectangle is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="2e285-164">Las coordenadas *x1 Y1* especifican la esquina superior izquierda del rectángulo y las coordenadas *x2 Y2* especifican el ancho y el alto.</span><span class="sxs-lookup"><span data-stu-id="2e285-164">The coordinates *X1 Y1* specify the upper left corner of the rectangle, and the coordinates *X2 Y2* specify the width and height.</span></span>

## <a name="examples"></a><span data-ttu-id="2e285-165">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2e285-165">Examples</span></span>

<span data-ttu-id="2e285-166">El siguiente comando devuelve el rectángulo de visualización del dispositivo "Movie".</span><span class="sxs-lookup"><span data-stu-id="2e285-166">The following command returns the display rectangle of the "movie" device.</span></span>

``` syntax
where movie destination
```

## <a name="requirements"></a><span data-ttu-id="2e285-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e285-167">Requirements</span></span>



| <span data-ttu-id="2e285-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e285-168">Requirement</span></span> | <span data-ttu-id="2e285-169">Value</span><span class="sxs-lookup"><span data-stu-id="2e285-169">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2e285-170">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e285-170">Minimum supported client</span></span><br/> | <span data-ttu-id="2e285-171">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2e285-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2e285-172">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e285-172">Minimum supported server</span></span><br/> | <span data-ttu-id="2e285-173">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2e285-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="2e285-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e285-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e285-175">MCI</span><span class="sxs-lookup"><span data-stu-id="2e285-175">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2e285-176">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="2e285-176">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="2e285-177">pondrán</span><span class="sxs-lookup"><span data-stu-id="2e285-177">put</span></span>](put.md)
</dt> </dl>

 

