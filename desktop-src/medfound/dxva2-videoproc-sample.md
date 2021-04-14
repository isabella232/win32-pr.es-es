---
description: Muestra cómo usar el procesamiento de vídeo de DXVA.
ms.assetid: 1465bd41-94f9-4e19-8236-00e7a2d6f54a
title: Ejemplo de DXVA2_VideoProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8497a241baf07b76148a5bc2e7ddb4dd5e878e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360098"
---
# <a name="dxva2_videoproc-sample"></a><span data-ttu-id="4928c-103">DXVA2 \_ ejemplo de Videoproc</span><span class="sxs-lookup"><span data-stu-id="4928c-103">DXVA2\_VideoProc Sample</span></span>

<span data-ttu-id="4928c-104">Muestra cómo usar el [procesamiento de vídeo de DXVA](dxva-video-processing.md).</span><span class="sxs-lookup"><span data-stu-id="4928c-104">Shows how to use [DXVA Video Processing](dxva-video-processing.md).</span></span>

<span data-ttu-id="4928c-105">Este ejemplo genera mediante programación un vídeo con un flujo principal y un subflujo.</span><span class="sxs-lookup"><span data-stu-id="4928c-105">This sample programmatically generates video with a primary stream and a substream.</span></span> <span data-ttu-id="4928c-106">El flujo principal muestra las barras de color SMPTE y el subflujo es un rectángulo semitransparente.</span><span class="sxs-lookup"><span data-stu-id="4928c-106">The primary stream displays SMPTE color bars, and the substream is a semi-transparent rectangle.</span></span> <span data-ttu-id="4928c-107">A continuación, el vídeo se procesa y se muestra mediante un procesador de vídeo DXVA.</span><span class="sxs-lookup"><span data-stu-id="4928c-107">The video is then processed and displayed using a DXVA video processor.</span></span> <span data-ttu-id="4928c-108">El usuario puede cambiar los valores alfa planos, los rectángulos de origen y de destino, los ajustes de color y el espacio de colores.</span><span class="sxs-lookup"><span data-stu-id="4928c-108">The user can change the planar alpha values, source and destination rectangles, color adjustments, and color space.</span></span>

![captura de pantalla del \- ejemplo de videoproc de dxva2](images/dxva2-videoproc.png)

## <a name="apis-demonstrated"></a><span data-ttu-id="4928c-110">API mostradas</span><span class="sxs-lookup"><span data-stu-id="4928c-110">APIs Demonstrated</span></span>

<span data-ttu-id="4928c-111">En este ejemplo se muestran las siguientes interfaces de DXVA:</span><span class="sxs-lookup"><span data-stu-id="4928c-111">This sample demonstrates the following DXVA interfaces:</span></span>

-   [<span data-ttu-id="4928c-112">**IDirectXVideoProcessorService**</span><span class="sxs-lookup"><span data-stu-id="4928c-112">**IDirectXVideoProcessorService**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)
-   [<span data-ttu-id="4928c-113">**IDirectXVideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="4928c-113">**IDirectXVideoProcessor**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor)

## <a name="usage"></a><span data-ttu-id="4928c-114">Uso</span><span class="sxs-lookup"><span data-stu-id="4928c-114">Usage</span></span>

<span data-ttu-id="4928c-115">El \_ ejemplo de Videoproc DXVA2 crea una aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="4928c-115">The DXVA2\_VideoProc sample builds a Windows application.</span></span>

<span data-ttu-id="4928c-116">Opciones de la línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="4928c-116">Command line options:</span></span>



| <span data-ttu-id="4928c-117">Opción</span><span class="sxs-lookup"><span data-stu-id="4928c-117">Option</span></span> | <span data-ttu-id="4928c-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="4928c-118">Description</span></span>                                                                          |
|--------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4928c-119">-HH</span><span class="sxs-lookup"><span data-stu-id="4928c-119">-hh</span></span>    | <span data-ttu-id="4928c-120">Fuerza a la aplicación a usar un dispositivo Direct3D de hardware y un dispositivo DXVA de hardware.</span><span class="sxs-lookup"><span data-stu-id="4928c-120">Forces the application to use a hardware Direct3D device and a hardware DXVA device.</span></span> |
| <span data-ttu-id="4928c-121">-HS</span><span class="sxs-lookup"><span data-stu-id="4928c-121">-hs</span></span>    | <span data-ttu-id="4928c-122">Fuerza a la aplicación a usar un dispositivo Direct3D de hardware y un dispositivo de software DXVA.</span><span class="sxs-lookup"><span data-stu-id="4928c-122">Forces the application to use a hardware Direct3D device and a software DXVA device.</span></span> |
| <span data-ttu-id="4928c-123">-ss</span><span class="sxs-lookup"><span data-stu-id="4928c-123">-ss</span></span>    | <span data-ttu-id="4928c-124">Fuerza a la aplicación a usar un dispositivo Direct3D de software y un dispositivo de software DXVA.</span><span class="sxs-lookup"><span data-stu-id="4928c-124">Forces the application to use a software Direct3D device and a software DXVA device.</span></span> |



 

<span data-ttu-id="4928c-125">Comandos de teclado:</span><span class="sxs-lookup"><span data-stu-id="4928c-125">Keyboard commands:</span></span>



| <span data-ttu-id="4928c-126">Clave</span><span class="sxs-lookup"><span data-stu-id="4928c-126">Key</span></span>       | <span data-ttu-id="4928c-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="4928c-127">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="4928c-128">ALT+ENTRAR</span><span class="sxs-lookup"><span data-stu-id="4928c-128">ALT+ENTER</span></span> | <span data-ttu-id="4928c-129">Cambiar entre el modo de ventana y el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="4928c-129">Switch between windowed mode and full-screen mode.</span></span>      |
| <span data-ttu-id="4928c-130">F1: F8</span><span class="sxs-lookup"><span data-stu-id="4928c-130">F1–F8</span></span>     | <span data-ttu-id="4928c-131">Escriba uno de los modos que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="4928c-131">Enter one of the modes shown in the following table.</span></span>    |
| <span data-ttu-id="4928c-132">FIN</span><span class="sxs-lookup"><span data-stu-id="4928c-132">END</span></span>       | <span data-ttu-id="4928c-133">Habilitar o deshabilitar el registro de depuración para fotogramas quitados.</span><span class="sxs-lookup"><span data-stu-id="4928c-133">Enable or disable debugging logging for dropped frames.</span></span> |
| <span data-ttu-id="4928c-134">INICIO</span><span class="sxs-lookup"><span data-stu-id="4928c-134">HOME</span></span>      | <span data-ttu-id="4928c-135">Restablezca un parámetro a su valor inicial.</span><span class="sxs-lookup"><span data-stu-id="4928c-135">Reset a parameter to its initial value.</span></span>                 |



 

<span data-ttu-id="4928c-136">Cada una de las teclas de función F1 a F8 cambia a un modo en el que se pueden utilizar las teclas de dirección para ajustar un parámetro de representación determinado.</span><span class="sxs-lookup"><span data-stu-id="4928c-136">Each of the function keys F1 through F8 switches to a mode in which the arrow keys can be used to adjust a particular rendering parameter.</span></span> <span data-ttu-id="4928c-137">Además, cambia el color de la subsecuencia.</span><span class="sxs-lookup"><span data-stu-id="4928c-137">In addition, the color of the substream changes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4928c-138">Clave</span><span class="sxs-lookup"><span data-stu-id="4928c-138">Key</span></span></th>
<th><span data-ttu-id="4928c-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="4928c-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4928c-140">F1</span><span class="sxs-lookup"><span data-stu-id="4928c-140">F1</span></span></td>
<td><span data-ttu-id="4928c-141">Ajuste los valores alfa.</span><span class="sxs-lookup"><span data-stu-id="4928c-141">Adjust the alpha values.</span></span><br/>
<ul>
<li><span data-ttu-id="4928c-142">SUBIR: aumente el alfa plano de ambos flujos.</span><span class="sxs-lookup"><span data-stu-id="4928c-142">UP: Increase the planar alpha of both streams.</span></span></li>
<li><span data-ttu-id="4928c-143">DOWN: reduce el alfa plano de ambos flujos.</span><span class="sxs-lookup"><span data-stu-id="4928c-143">DOWN: Decrease the planar alpha of both streams.</span></span></li>
<li><span data-ttu-id="4928c-144">RIGHT: aumentar el alfa de píxeles de la subsecuencia.</span><span class="sxs-lookup"><span data-stu-id="4928c-144">RIGHT: Increase the pixel alpha of the substream.</span></span></li>
<li><span data-ttu-id="4928c-145">LEFT: reduce el píxel alfa de la subsecuencia.</span><span class="sxs-lookup"><span data-stu-id="4928c-145">LEFT: Decrease the pixel alpha of the substream.</span></span></li>
</ul>
<span data-ttu-id="4928c-146">Color de subsecuencia: blanco</span><span class="sxs-lookup"><span data-stu-id="4928c-146">Substream color: White</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4928c-147">F2</span><span class="sxs-lookup"><span data-stu-id="4928c-147">F2</span></span></td>
<td><span data-ttu-id="4928c-148">Ajuste el área de origen (zoom) del flujo principal.</span><span class="sxs-lookup"><span data-stu-id="4928c-148">Adjust the primary stream's source area (zoom).</span></span><br/>
<ul>
<li><span data-ttu-id="4928c-149">SUBIR: aumentar verticalmente (acercar).</span><span class="sxs-lookup"><span data-stu-id="4928c-149">UP: Increase vertically (zoom in).</span></span></li>
<li><span data-ttu-id="4928c-150">ABAJO: reducir verticalmente (alejar).</span><span class="sxs-lookup"><span data-stu-id="4928c-150">DOWN: Decrease vertically (zoom out).</span></span></li>
<li><span data-ttu-id="4928c-151">RIGHT: aumentar horizontalmente (acercar).</span><span class="sxs-lookup"><span data-stu-id="4928c-151">RIGHT: Increase horizontally (zoom in).</span></span></li>
<li><span data-ttu-id="4928c-152">LEFT: disminuir horizontalmente (alejar).</span><span class="sxs-lookup"><span data-stu-id="4928c-152">LEFT: Decrease horizontally (zoom out).</span></span></li>
</ul>
<span data-ttu-id="4928c-153">Color de subsecuencia: rojo</span><span class="sxs-lookup"><span data-stu-id="4928c-153">Substream color: Red</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4928c-154">F3</span><span class="sxs-lookup"><span data-stu-id="4928c-154">F3</span></span></td>
<td><span data-ttu-id="4928c-155">Mueva el área de origen del flujo principal.</span><span class="sxs-lookup"><span data-stu-id="4928c-155">Move the primary stream's source area.</span></span><br/>
<ul>
<li><span data-ttu-id="4928c-156">SUBIR: subir.</span><span class="sxs-lookup"><span data-stu-id="4928c-156">UP: Move up.</span></span></li>
<li><span data-ttu-id="4928c-157">ABAJO: bajar.</span><span class="sxs-lookup"><span data-stu-id="4928c-157">DOWN: Move down.</span></span></li>
<li><span data-ttu-id="4928c-158">DERECHA: moverse a la derecha.</span><span class="sxs-lookup"><span data-stu-id="4928c-158">RIGHT: Move right.</span></span></li>
<li><span data-ttu-id="4928c-159">IZQUIERDA: moverse a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="4928c-159">LEFT: Move left.</span></span></li>
</ul>
<span data-ttu-id="4928c-160">Color de subsecuencia: amarillo</span><span class="sxs-lookup"><span data-stu-id="4928c-160">Substream color: Yellow</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4928c-161">F4</span><span class="sxs-lookup"><span data-stu-id="4928c-161">F4</span></span></td>
<td><span data-ttu-id="4928c-162">Ajuste el área de destino del flujo principal.</span><span class="sxs-lookup"><span data-stu-id="4928c-162">Adjust the primary stream's destination area.</span></span><br/>
<ul>
<li><span data-ttu-id="4928c-163">SUBIR: aumentar verticalmente.</span><span class="sxs-lookup"><span data-stu-id="4928c-163">UP: Increase vertically.</span></span></li>
<li><span data-ttu-id="4928c-164">ABAJO: reducir verticalmente.</span><span class="sxs-lookup"><span data-stu-id="4928c-164">DOWN: Decrease vertically.</span></span></li>
<li><span data-ttu-id="4928c-165">RIGHT: aumentar horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="4928c-165">RIGHT: Increase horizontally.</span></span></li>
<li><span data-ttu-id="4928c-166">LEFT: disminuir horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="4928c-166">LEFT: Decrease horizontally.</span></span></li>
</ul>
<span data-ttu-id="4928c-167">Color de subsecuencia: verde</span><span class="sxs-lookup"><span data-stu-id="4928c-167">Substream color: Green</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4928c-168">F5</span><span class="sxs-lookup"><span data-stu-id="4928c-168">F5</span></span></td>
<td><span data-ttu-id="4928c-169">Mueva el área de destino del flujo principal.</span><span class="sxs-lookup"><span data-stu-id="4928c-169">Move the primary stream's destination area.</span></span><br/>
<ul>
<li><span data-ttu-id="4928c-170">SUBIR: subir.</span><span class="sxs-lookup"><span data-stu-id="4928c-170">UP: Move up.</span></span></li>
<li><span data-ttu-id="4928c-171">ABAJO: bajar.</span><span class="sxs-lookup"><span data-stu-id="4928c-171">DOWN: Move down.</span></span></li>
<li><span data-ttu-id="4928c-172">DERECHA: moverse a la derecha.</span><span class="sxs-lookup"><span data-stu-id="4928c-172">RIGHT: Move right.</span></span></li>
<li><span data-ttu-id="4928c-173">IZQUIERDA: moverse a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="4928c-173">LEFT: Move left.</span></span></li>
</ul>
<span data-ttu-id="4928c-174">Color de subsecuencia: Aguamarina</span><span class="sxs-lookup"><span data-stu-id="4928c-174">Substream color: Cyan</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4928c-175">F6</span><span class="sxs-lookup"><span data-stu-id="4928c-175">F6</span></span></td>
<td><span data-ttu-id="4928c-176">Cambiar el color de fondo o el espacio de colores.</span><span class="sxs-lookup"><span data-stu-id="4928c-176">Change background color or color space.</span></span><br/>
<ul>
<li><span data-ttu-id="4928c-177">Subir, bajar: desplazarse por los espacios de colores.</span><span class="sxs-lookup"><span data-stu-id="4928c-177">UP, DOWN: Cycle through color spaces.</span></span></li>
<li><span data-ttu-id="4928c-178">DERECHA, izquierda: desplazarse por los colores de fondo.</span><span class="sxs-lookup"><span data-stu-id="4928c-178">RIGHT, LEFT: Cycle through background colors.</span></span></li>
</ul>
<span data-ttu-id="4928c-179">Color de subsecuencia: azul</span><span class="sxs-lookup"><span data-stu-id="4928c-179">Substream color: Blue</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4928c-180">F7</span><span class="sxs-lookup"><span data-stu-id="4928c-180">F7</span></span></td>
<td><span data-ttu-id="4928c-181">Ajustar el brillo y el contraste.</span><span class="sxs-lookup"><span data-stu-id="4928c-181">Adjust brightness and contrast.</span></span><br/>
<ul>
<li><span data-ttu-id="4928c-182">SUBIR: aumentar el brillo.</span><span class="sxs-lookup"><span data-stu-id="4928c-182">UP: Increase brightness.</span></span></li>
<li><span data-ttu-id="4928c-183">ABAJO: reduce el brillo.</span><span class="sxs-lookup"><span data-stu-id="4928c-183">DOWN: Decrease brightness.</span></span></li>
<li><span data-ttu-id="4928c-184">RIGHT: aumentar contraste.</span><span class="sxs-lookup"><span data-stu-id="4928c-184">RIGHT: Increase contrast.</span></span></li>
<li><span data-ttu-id="4928c-185">LEFT: reduce el contraste.</span><span class="sxs-lookup"><span data-stu-id="4928c-185">LEFT: Decrease contrast.</span></span></li>
</ul>
<span data-ttu-id="4928c-186">Color de subsecuencia: magenta</span><span class="sxs-lookup"><span data-stu-id="4928c-186">Substream color: Magenta</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4928c-187">F8</span><span class="sxs-lookup"><span data-stu-id="4928c-187">F8</span></span></td>
<td><span data-ttu-id="4928c-188">Ajuste el matiz y la saturación.</span><span class="sxs-lookup"><span data-stu-id="4928c-188">Adjust hue and saturation.</span></span><br/>
<ul>
<li><span data-ttu-id="4928c-189">SUBIR: aumentar matiz.</span><span class="sxs-lookup"><span data-stu-id="4928c-189">UP: Increase hue.</span></span></li>
<li><span data-ttu-id="4928c-190">BAJAR: reduce el matiz.</span><span class="sxs-lookup"><span data-stu-id="4928c-190">DOWN: Decrease hue.</span></span></li>
<li><span data-ttu-id="4928c-191">RIGHT: aumentar la saturación.</span><span class="sxs-lookup"><span data-stu-id="4928c-191">RIGHT: Increase saturation.</span></span></li>
<li><span data-ttu-id="4928c-192">LEFT: disminución de la saturación.</span><span class="sxs-lookup"><span data-stu-id="4928c-192">LEFT: Decrease saturation.</span></span></li>
</ul>
<span data-ttu-id="4928c-193">Color de subsecuencia: negro</span><span class="sxs-lookup"><span data-stu-id="4928c-193">Substream color: Black</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4928c-194">En cada modo, al presionar la tecla Inicio, se restablecen los parámetros de ese modo a sus valores iniciales.</span><span class="sxs-lookup"><span data-stu-id="4928c-194">In each mode, pressing the HOME key resets the parameters for that mode to their initial values.</span></span>

## <a name="requirements"></a><span data-ttu-id="4928c-195">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4928c-195">Requirements</span></span>



| <span data-ttu-id="4928c-196">Producto</span><span class="sxs-lookup"><span data-stu-id="4928c-196">Product</span></span>                                                        | <span data-ttu-id="4928c-197">Versión</span><span class="sxs-lookup"><span data-stu-id="4928c-197">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="4928c-198">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="4928c-198">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="4928c-199">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4928c-199">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="4928c-200">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="4928c-200">Downloading the Sample</span></span>

<span data-ttu-id="4928c-201">Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter).</span><span class="sxs-lookup"><span data-stu-id="4928c-201">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4928c-202">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4928c-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4928c-203">Aceleración de vídeo de DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="4928c-203">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="4928c-204">Procesamiento de vídeo de DXVA</span><span class="sxs-lookup"><span data-stu-id="4928c-204">DXVA Video Processing</span></span>](dxva-video-processing.md)
</dt> <dt>

[<span data-ttu-id="4928c-205">Muestras de SDK de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4928c-205">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 




