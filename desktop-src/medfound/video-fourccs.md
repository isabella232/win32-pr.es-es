---
description: Vídeo FOURCCs
ms.assetid: bea4835d-fd7f-4ac3-8466-7f4e0d799a12
title: Vídeo FOURCCs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b804962308d0ecc5bf32fcddf5176905d0e17fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360569"
---
# <a name="video-fourccs"></a><span data-ttu-id="c12e6-103">Vídeo FOURCCs</span><span class="sxs-lookup"><span data-stu-id="c12e6-103">Video FOURCCs</span></span>

<span data-ttu-id="c12e6-104">Muchos formatos de vídeo tienen códigos FOURCC asignados.</span><span class="sxs-lookup"><span data-stu-id="c12e6-104">Many video formats have FOURCC codes assigned to them.</span></span> <span data-ttu-id="c12e6-105">Un código FOURCC es un entero de 32 bits sin signo que se crea mediante la concatenación de cuatro caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="c12e6-105">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span> <span data-ttu-id="c12e6-106">Por ejemplo, el código FOURCC del vídeo YUY2 es "YUY2".</span><span class="sxs-lookup"><span data-stu-id="c12e6-106">For example, the FOURCC code for YUY2 video is 'YUY2'.</span></span>

<span data-ttu-id="c12e6-107">Se definen varias macros de C/C++ para declarar valores FOURCC en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="c12e6-107">Various C/C++ macros are defined for declaring FOURCC values in source code.</span></span> <span data-ttu-id="c12e6-108">La macro **MAKEFOURCC** se define en mmsystem. h y la macro **FCC** se define en Aviriff. h y otros archivos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="c12e6-108">The **MAKEFOURCC** macro is defined in Mmsystem.h, and the **FCC** macro is defined in Aviriff.h and various other header files.</span></span> <span data-ttu-id="c12e6-109">También puede declarar un código FOURCC directamente como un literal de cadena simplemente invirtiendo el orden de los caracteres.</span><span class="sxs-lookup"><span data-stu-id="c12e6-109">You can also declare a FOURCC code directly as a string literal simply by reversing the order of the characters.</span></span> <span data-ttu-id="c12e6-110">Por lo tanto, las siguientes instrucciones son equivalentes:</span><span class="sxs-lookup"><span data-stu-id="c12e6-110">Thus, the following statements are equivalent:</span></span>

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```

<span data-ttu-id="c12e6-111">(En el último ejemplo, se requiere invertir el orden de los bytes porque Windows utiliza una arquitectura little-endian.</span><span class="sxs-lookup"><span data-stu-id="c12e6-111">(In the last example, reversing the byte order is necessary because Windows uses a little-endian architecture.</span></span> <span data-ttu-id="c12e6-112">' Y ' = 0x59, ' U ' = 0x55 y ' 2 ' = 2, por lo que ' 2YUY ' es 0x32595559).</span><span class="sxs-lookup"><span data-stu-id="c12e6-112">'Y' = 0x59, 'U' = 0x55, and '2' = 0x32, so '2YUY' is 0x32595559.)</span></span>

<span data-ttu-id="c12e6-113">Algunas de las API de [DirectX video Acceleration 2,0](directx-video-acceleration-2-0.md) usan un valor de **D3DFORMAT** para describir un formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c12e6-113">Some of the [DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md) APIs use a **D3DFORMAT** value to describe a video format.</span></span> <span data-ttu-id="c12e6-114">También se puede utilizar un código FOURCC en este contexto:</span><span class="sxs-lookup"><span data-stu-id="c12e6-114">A FOURCC code can be used in this context as well:</span></span>

``` syntax
D3DFORMAT fmt = (D3DFORMAT)MAKEFOURCC('Y','U','Y','2');
D3DFORMAT fmt = (D3DFORMAT)FCC('YUY2');
D3DFORMAT fmt = D3DFORMAT('2YUY'); // Coerce to D3DFORMAT type.
```

### <a name="fourcc-constants"></a><span data-ttu-id="c12e6-115">Constantes FOURCC</span><span class="sxs-lookup"><span data-stu-id="c12e6-115">FOURCC Constants</span></span>

<span data-ttu-id="c12e6-116">En la tabla siguiente se enumeran algunos códigos FOURCC comunes.</span><span class="sxs-lookup"><span data-stu-id="c12e6-116">The following table lists some common FOURCC codes.</span></span>



| <span data-ttu-id="c12e6-117">Valor FOURCC</span><span class="sxs-lookup"><span data-stu-id="c12e6-117">FOURCC value</span></span> | <span data-ttu-id="c12e6-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="c12e6-118">Description</span></span>                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c12e6-119">H264</span><span class="sxs-lookup"><span data-stu-id="c12e6-119">'H264'</span></span>       | <span data-ttu-id="c12e6-120">Vídeo H. 264.</span><span class="sxs-lookup"><span data-stu-id="c12e6-120">H.264 video.</span></span>                                                                                                          |
| <span data-ttu-id="c12e6-121">'I420'</span><span class="sxs-lookup"><span data-stu-id="c12e6-121">'I420'</span></span>       | <span data-ttu-id="c12e6-122">Vídeo YUV almacenado en formato 4:2:0 plano.</span><span class="sxs-lookup"><span data-stu-id="c12e6-122">YUV video stored in planar 4:2:0 format.</span></span>                                                                              |
| <span data-ttu-id="c12e6-123">'IYUV'</span><span class="sxs-lookup"><span data-stu-id="c12e6-123">'IYUV'</span></span>       | <span data-ttu-id="c12e6-124">Vídeo YUV almacenado en formato 4:2:0 plano.</span><span class="sxs-lookup"><span data-stu-id="c12e6-124">YUV video stored in planar 4:2:0 format.</span></span>                                                                              |
| <span data-ttu-id="c12e6-125">' M 4S2 '</span><span class="sxs-lookup"><span data-stu-id="c12e6-125">'M4S2'</span></span>       | <span data-ttu-id="c12e6-126">Vídeo MPEG-4 parte 2.</span><span class="sxs-lookup"><span data-stu-id="c12e6-126">MPEG-4 part 2 video.</span></span>                                                                                                  |
| <span data-ttu-id="c12e6-127">MP4</span><span class="sxs-lookup"><span data-stu-id="c12e6-127">'MP4S'</span></span>       | <span data-ttu-id="c12e6-128">Códec Microsoft MPEG 4 versión 3.</span><span class="sxs-lookup"><span data-stu-id="c12e6-128">Microsoft MPEG 4 codec version 3.</span></span> <span data-ttu-id="c12e6-129">Este códec ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="c12e6-129">This codec is no longer supported.</span></span>                                                  |
| <span data-ttu-id="c12e6-130">MP4V</span><span class="sxs-lookup"><span data-stu-id="c12e6-130">'MP4V'</span></span>       | <span data-ttu-id="c12e6-131">Vídeo MPEG-4 parte 2.</span><span class="sxs-lookup"><span data-stu-id="c12e6-131">MPEG-4 part 2 video.</span></span>                                                                                                  |
| <span data-ttu-id="c12e6-132">'MPG1'</span><span class="sxs-lookup"><span data-stu-id="c12e6-132">'MPG1'</span></span>       | <span data-ttu-id="c12e6-133">Vídeo MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="c12e6-133">MPEG-1 video.</span></span>                                                                                                         |
| <span data-ttu-id="c12e6-134">'MSS1'</span><span class="sxs-lookup"><span data-stu-id="c12e6-134">'MSS1'</span></span>       | <span data-ttu-id="c12e6-135">Contenido codificado con el códec de pantalla Windows Media Video 7.</span><span class="sxs-lookup"><span data-stu-id="c12e6-135">Content encoded with the Windows Media Video 7 screen codec.</span></span>                                                          |
| <span data-ttu-id="c12e6-136">'MSS2'</span><span class="sxs-lookup"><span data-stu-id="c12e6-136">'MSS2'</span></span>       | <span data-ttu-id="c12e6-137">Contenido codificado con el códec de pantalla de Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="c12e6-137">Content encoded with the Windows Media Video 9 screen codec.</span></span>                                                          |
| <span data-ttu-id="c12e6-138">UYVY</span><span class="sxs-lookup"><span data-stu-id="c12e6-138">'UYVY'</span></span>       | <span data-ttu-id="c12e6-139">Vídeo YUV almacenado en formato 4:2:2 empaquetado.</span><span class="sxs-lookup"><span data-stu-id="c12e6-139">YUV video stored in packed 4:2:2 format.</span></span> <span data-ttu-id="c12e6-140">Similar a YUY2, pero con diferente orden de datos.</span><span class="sxs-lookup"><span data-stu-id="c12e6-140">Similar to YUY2 but with different ordering of data.</span></span>                         |
| <span data-ttu-id="c12e6-141">'WMV1'</span><span class="sxs-lookup"><span data-stu-id="c12e6-141">'WMV1'</span></span>       | <span data-ttu-id="c12e6-142">Contenido codificado con el códec Windows Media Video 7.</span><span class="sxs-lookup"><span data-stu-id="c12e6-142">Content encoded with the Windows Media Video 7 codec.</span></span>                                                                 |
| <span data-ttu-id="c12e6-143">'WMV2'</span><span class="sxs-lookup"><span data-stu-id="c12e6-143">'WMV2'</span></span>       | <span data-ttu-id="c12e6-144">Contenido codificado con el códec Windows Media Video 8.</span><span class="sxs-lookup"><span data-stu-id="c12e6-144">Content encoded with the Windows Media Video 8 codec.</span></span>                                                                 |
| <span data-ttu-id="c12e6-145">'WMV3'</span><span class="sxs-lookup"><span data-stu-id="c12e6-145">'WMV3'</span></span>       | <span data-ttu-id="c12e6-146">Contenido codificado con el códec Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="c12e6-146">Content encoded with the Windows Media Video 9 codec.</span></span>                                                                 |
| <span data-ttu-id="c12e6-147">'WMVA'</span><span class="sxs-lookup"><span data-stu-id="c12e6-147">'WMVA'</span></span>       | <span data-ttu-id="c12e6-148">Contenido codificado con la versión antigua obsoleta del códec de perfil avanzado de Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="c12e6-148">Content encoded with the older, obsolete version of the Windows Media Video 9 Advanced Profile codec.</span></span>                 |
| <span data-ttu-id="c12e6-149">'WMVP'</span><span class="sxs-lookup"><span data-stu-id="c12e6-149">'WMVP'</span></span>       | <span data-ttu-id="c12e6-150">Contenido codificado con el códec de imagen Windows Media Video 9,1.</span><span class="sxs-lookup"><span data-stu-id="c12e6-150">Content encoded with the Windows Media Video 9.1 Image codec.</span></span>                                                         |
| <span data-ttu-id="c12e6-151">'WVC1'</span><span class="sxs-lookup"><span data-stu-id="c12e6-151">'WVC1'</span></span>       | <span data-ttu-id="c12e6-152">SMPTE 421M ("VC-1").</span><span class="sxs-lookup"><span data-stu-id="c12e6-152">SMPTE 421M ("VC-1").</span></span> <span data-ttu-id="c12e6-153">Contenido codificado con el perfil avanzado de Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="c12e6-153">Content encoded with Windows Media Video 9 Advanced Profile.</span></span>                                     |
| <span data-ttu-id="c12e6-154">'WVP2'</span><span class="sxs-lookup"><span data-stu-id="c12e6-154">'WVP2'</span></span>       | <span data-ttu-id="c12e6-155">Contenido codificado con el códec Windows Media Video 9,1 Image V2.</span><span class="sxs-lookup"><span data-stu-id="c12e6-155">Content encoded with the Windows Media Video 9.1 Image v2 codec.</span></span>                                                      |
| <span data-ttu-id="c12e6-156">YUY2</span><span class="sxs-lookup"><span data-stu-id="c12e6-156">'YUY2'</span></span>       | <span data-ttu-id="c12e6-157">Vídeo YUV almacenado en formato 4:2:2 empaquetado.</span><span class="sxs-lookup"><span data-stu-id="c12e6-157">YUV video stored in packed 4:2:2 format.</span></span>                                                                              |
| <span data-ttu-id="c12e6-158">'YV12'</span><span class="sxs-lookup"><span data-stu-id="c12e6-158">'YV12'</span></span>       | <span data-ttu-id="c12e6-159">Vídeo YUV almacenado en formato planar 4:2:0 o 4:1:1.</span><span class="sxs-lookup"><span data-stu-id="c12e6-159">YUV video stored in planar 4:2:0 or 4:1:1 format.</span></span> <span data-ttu-id="c12e6-160">Es idéntico a i420/IYUV, salvo que se cambian los planos usted y V.</span><span class="sxs-lookup"><span data-stu-id="c12e6-160">Identical to I420/IYUV except that the U and V planes are switched.</span></span> |
| <span data-ttu-id="c12e6-161">YVU9</span><span class="sxs-lookup"><span data-stu-id="c12e6-161">'YVU9'</span></span>       | <span data-ttu-id="c12e6-162">Vídeo YUV almacenado en formato 16:1:1 plano.</span><span class="sxs-lookup"><span data-stu-id="c12e6-162">YUV video stored in planar 16:1:1 format.</span></span>                                                                             |
| <span data-ttu-id="c12e6-163">YVYU</span><span class="sxs-lookup"><span data-stu-id="c12e6-163">'YVYU'</span></span>       | <span data-ttu-id="c12e6-164">Vídeo YUV almacenado en formato 4:2:2 empaquetado.</span><span class="sxs-lookup"><span data-stu-id="c12e6-164">YUV video stored in packed 4:2:2 format.</span></span> <span data-ttu-id="c12e6-165">Similar a YUY2, pero con diferente orden de datos.</span><span class="sxs-lookup"><span data-stu-id="c12e6-165">Similar to YUY2 but with different ordering of data.</span></span>                         |



 

## <a name="related-topics"></a><span data-ttu-id="c12e6-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c12e6-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c12e6-167">Tipos de medios de vídeo</span><span class="sxs-lookup"><span data-stu-id="c12e6-167">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="c12e6-168">GUID de subtipo de vídeo</span><span class="sxs-lookup"><span data-stu-id="c12e6-168">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> </dl>

 

 



