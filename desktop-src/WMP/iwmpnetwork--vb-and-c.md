---
title: Interfaz IWMPNetwork (VB y C) (WMP. h)
description: Proporciona propiedades y métodos para obtener acceso a las estadísticas relacionadas con la calidad de una conexión de red, y para especificar y recuperar la configuración del proxy de red. La interfaz IWMPNetwork expone las siguientes propiedades.
ms.assetid: d385510f-11cf-4a2a-96be-b416cddc3d80
keywords:
- IWMPNetwork (VB y C) interfaz de Windows Media Player
- IWMPNetwork (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPNetwork (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 301fe5c89d2eb5df3dd4c22927e75a5607e7abd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690367"
---
# <a name="iwmpnetwork-vb-and-c-interface"></a><span data-ttu-id="231c7-105">Interfaz IWMPNetwork (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="231c7-105">IWMPNetwork (VB and C#) interface</span></span>

<span data-ttu-id="231c7-106">Proporciona propiedades y métodos para obtener acceso a las estadísticas relacionadas con la calidad de una conexión de red, y para especificar y recuperar la configuración del proxy de red.</span><span class="sxs-lookup"><span data-stu-id="231c7-106">Provides properties and methods to access statistics relating to the quality of a network connection, and to specify and retrieve the network proxy settings.</span></span>

<span data-ttu-id="231c7-107">La interfaz **IWMPNetwork** expone las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="231c7-107">The **IWMPNetwork** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="231c7-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="231c7-108">Members</span></span>

<span data-ttu-id="231c7-109">La interfaz **IWMPNetwork (VB y C#)** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="231c7-109">The **IWMPNetwork (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="231c7-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="231c7-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="231c7-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="231c7-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="231c7-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="231c7-112">Methods</span></span>

<span data-ttu-id="231c7-113">La interfaz **IWMPNetwork (VB y C#)** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="231c7-113">The **IWMPNetwork (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="231c7-114">Método</span><span class="sxs-lookup"><span data-stu-id="231c7-114">Method</span></span>                                                                                           | <span data-ttu-id="231c7-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="231c7-115">Description</span></span>                                                                                                            |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="231c7-116">**getProxyBypassForLocal**</span><span class="sxs-lookup"><span data-stu-id="231c7-116">**getProxyBypassForLocal**</span></span>](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)                   | <span data-ttu-id="231c7-117">Devuelve un valor que indica si se omite el servidor proxy si el servidor de origen está en una red local.</span><span class="sxs-lookup"><span data-stu-id="231c7-117">Returns a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span><br/> |
| [<span data-ttu-id="231c7-118">**getProxyExceptionList**</span><span class="sxs-lookup"><span data-stu-id="231c7-118">**getProxyExceptionList**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)   | <span data-ttu-id="231c7-119">Devuelve la lista de excepciones de proxy.</span><span class="sxs-lookup"><span data-stu-id="231c7-119">Returns the proxy exception list.</span></span><br/>                                                                           |
| [<span data-ttu-id="231c7-120">**getProxyName**</span><span class="sxs-lookup"><span data-stu-id="231c7-120">**getProxyName**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)                     | <span data-ttu-id="231c7-121">Devuelve el nombre del servidor proxy que se está usando.</span><span class="sxs-lookup"><span data-stu-id="231c7-121">Returns the name of the proxy server being used.</span></span><br/>                                                            |
| [<span data-ttu-id="231c7-122">**getProxyPort**</span><span class="sxs-lookup"><span data-stu-id="231c7-122">**getProxyPort**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)                     | <span data-ttu-id="231c7-123">Devuelve el puerto del proxy que se está usando.</span><span class="sxs-lookup"><span data-stu-id="231c7-123">Returns the proxy port being used.</span></span><br/>                                                                          |
| [<span data-ttu-id="231c7-124">**getProxySettings**</span><span class="sxs-lookup"><span data-stu-id="231c7-124">**getProxySettings**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)             | <span data-ttu-id="231c7-125">Devuelve información acerca de la configuración de proxy para un protocolo.</span><span class="sxs-lookup"><span data-stu-id="231c7-125">Returns information about the proxy settings for a protocol.</span></span><br/>                                                |
| [<span data-ttu-id="231c7-126">**setProxyBypassForLocal**</span><span class="sxs-lookup"><span data-stu-id="231c7-126">**setProxyBypassForLocal**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md) | <span data-ttu-id="231c7-127">Especifica si el servidor proxy se omite si el servidor de origen está en una red local.</span><span class="sxs-lookup"><span data-stu-id="231c7-127">Specifies whether the proxy server is bypassed if the origin server is on a local network.</span></span><br/>                  |
| [<span data-ttu-id="231c7-128">**setProxyExceptionList**</span><span class="sxs-lookup"><span data-stu-id="231c7-128">**setProxyExceptionList**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)   | <span data-ttu-id="231c7-129">Especifica la lista de excepciones de proxy.</span><span class="sxs-lookup"><span data-stu-id="231c7-129">Specifies the proxy exception list.</span></span><br/>                                                                         |
| [<span data-ttu-id="231c7-130">**setProxyName**</span><span class="sxs-lookup"><span data-stu-id="231c7-130">**setProxyName**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)                     | <span data-ttu-id="231c7-131">Especifica el nombre del servidor proxy que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="231c7-131">Specifies the name of the proxy server to use.</span></span><br/>                                                              |
| [<span data-ttu-id="231c7-132">**setProxyPort**</span><span class="sxs-lookup"><span data-stu-id="231c7-132">**setProxyPort**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)                     | <span data-ttu-id="231c7-133">Especifica el puerto del proxy que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="231c7-133">Specifies the proxy port to use.</span></span><br/>                                                                            |
| [<span data-ttu-id="231c7-134">**setProxySettings**</span><span class="sxs-lookup"><span data-stu-id="231c7-134">**setProxySettings**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)             | <span data-ttu-id="231c7-135">Especifica la configuración de proxy para un protocolo.</span><span class="sxs-lookup"><span data-stu-id="231c7-135">Specifies the proxy settings for a protocol.</span></span><br/>                                                                |



 

### <a name="properties"></a><span data-ttu-id="231c7-136">Propiedades</span><span class="sxs-lookup"><span data-stu-id="231c7-136">Properties</span></span>

<span data-ttu-id="231c7-137">La interfaz **IWMPNetwork (VB y C#)** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="231c7-137">The **IWMPNetwork (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="231c7-138">Propiedad</span><span class="sxs-lookup"><span data-stu-id="231c7-138">Property</span></span>                                                                                          | <span data-ttu-id="231c7-139">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="231c7-139">Access type</span></span>           | <span data-ttu-id="231c7-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="231c7-140">Description</span></span>                                                                                  |
|:--------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="231c7-141">**Consumo**</span><span class="sxs-lookup"><span data-stu-id="231c7-141">**bandWidth**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bandwidth--vb-and-c.md)<br/>                 | <span data-ttu-id="231c7-142">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="231c7-142">Read-only</span></span><br/>  | <span data-ttu-id="231c7-143">Obtiene el ancho de banda actual del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="231c7-143">Gets the current bandwidth of the media item.</span></span><br/>                                     |
| [<span data-ttu-id="231c7-144">**Velocidad**</span><span class="sxs-lookup"><span data-stu-id="231c7-144">**bitRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bitrate--vb-and-c.md)<br/>                     | <span data-ttu-id="231c7-145">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="231c7-145">Read-only</span></span><br/>  | <span data-ttu-id="231c7-146">Obtiene la velocidad de bits actual recibida.</span><span class="sxs-lookup"><span data-stu-id="231c7-146">Gets the current bit rate being received.</span></span><br/>                                         |
| [<span data-ttu-id="231c7-147">**bufferingCount**</span><span class="sxs-lookup"><span data-stu-id="231c7-147">**bufferingCount**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingcount--vb-and-c.md)<br/>       | <span data-ttu-id="231c7-148">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="231c7-148">Read-only</span></span><br/>  | <span data-ttu-id="231c7-149">Obtiene el número de veces que se ha producido el almacenamiento en búfer durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="231c7-149">Gets the number of times buffering occurred during playback.</span></span><br/>                      |
| [<span data-ttu-id="231c7-150">**bufferingProgress**</span><span class="sxs-lookup"><span data-stu-id="231c7-150">**bufferingProgress**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)<br/> | <span data-ttu-id="231c7-151">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="231c7-151">Read-only</span></span><br/>  | <span data-ttu-id="231c7-152">Obtiene el porcentaje de almacenamiento en búfer completado.</span><span class="sxs-lookup"><span data-stu-id="231c7-152">Gets the percentage of buffering completed.</span></span><br/>                                       |
| [<span data-ttu-id="231c7-153">**bufferingTime**</span><span class="sxs-lookup"><span data-stu-id="231c7-153">**bufferingTime**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingtime--vb-and-c.md)<br/>         | <span data-ttu-id="231c7-154">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="231c7-154">Read/write</span></span><br/> | <span data-ttu-id="231c7-155">Obtiene o establece la cantidad de tiempo de almacenamiento en búfer en milisegundos antes de que comience la reproducción.</span><span class="sxs-lookup"><span data-stu-id="231c7-155">Gets or sets the amount of buffering time in milliseconds before playback begins.</span></span><br/> |
| [<span data-ttu-id="231c7-156">**downloadProgress**</span><span class="sxs-lookup"><span data-stu-id="231c7-156">**downloadProgress**</span></span>](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)<br/>   | <span data-ttu-id="231c7-157">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="231c7-157">Read-only</span></span><br/>  | <span data-ttu-id="231c7-158">Obtiene el porcentaje de descarga completada.</span><span class="sxs-lookup"><span data-stu-id="231c7-158">Gets the percentage of downloading completed.</span></span><br/>                                     |
| [<span data-ttu-id="231c7-159">**encodedFrameRate**</span><span class="sxs-lookup"><span data-stu-id="231c7-159">**encodedFrameRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)<br/>   | <span data-ttu-id="231c7-160">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="231c7-160">Read-only</span></span><br/>  | <span data-ttu-id="231c7-161">Obtiene la velocidad de fotogramas de vídeo especificada por el autor del contenido.</span><span class="sxs-lookup"><span data-stu-id="231c7-161">Gets the video frame rate specified by the content author.</span></span><br/>                        |
| [<span data-ttu-id="231c7-162">**Velocidad**</span><span class="sxs-lookup"><span data-stu-id="231c7-162">**frameRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)<br/>                 | <span data-ttu-id="231c7-163">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="231c7-163">Read-only</span></span><br/>  | <span data-ttu-id="231c7-164">Obtiene la velocidad de fotogramas de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="231c7-164">Gets the current video frame rate.</span></span><br/>                                                |
| [<span data-ttu-id="231c7-165">**framesSkipped**</span><span class="sxs-lookup"><span data-stu-id="231c7-165">**framesSkipped**</span></span>](wmplibiwmpnetwork-iwmpnetwork-framesskipped--vb-and-c.md)<br/>         | <span data-ttu-id="231c7-166">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="231c7-166">Read-only</span></span><br/>  | <span data-ttu-id="231c7-167">Obtiene el número total de fotogramas omitidos durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="231c7-167">Gets the total number of frames skipped during playback.</span></span><br/>                          |
| [<span data-ttu-id="231c7-168">**lostPackets**</span><span class="sxs-lookup"><span data-stu-id="231c7-168">**lostPackets**</span></span>](wmplibiwmpnetwork-iwmpnetwork-lostpackets--vb-and-c.md)<br/>             | <span data-ttu-id="231c7-169">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="231c7-169">Read-only</span></span><br/>  | <span data-ttu-id="231c7-170">Obtiene el número de paquetes perdidos.</span><span class="sxs-lookup"><span data-stu-id="231c7-170">Gets the number of packets lost.</span></span><br/>                                                  |
| [<span data-ttu-id="231c7-171">**maxBandwidth**</span><span class="sxs-lookup"><span data-stu-id="231c7-171">**maxBandwidth**</span></span>](wmplibiwmpnetwork-iwmpnetwork-maxbandwidth--vb-and-c.md)<br/>           | <span data-ttu-id="231c7-172">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="231c7-172">Read/write</span></span><br/> | <span data-ttu-id="231c7-173">Obtiene o establece el ancho de banda máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="231c7-173">Gets or sets the maximum allowed bandwidth.</span></span><br/>                                       |
| [<span data-ttu-id="231c7-174">**maxBitRate**</span><span class="sxs-lookup"><span data-stu-id="231c7-174">**maxBitRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-maxbitrate--vb-and-c.md)<br/>               | <span data-ttu-id="231c7-175">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="231c7-175">Read-only</span></span><br/>  | <span data-ttu-id="231c7-176">Obtiene la velocidad de bits de vídeo máxima posible.</span><span class="sxs-lookup"><span data-stu-id="231c7-176">Gets the maximum possible video bit rate.</span></span><br/>                                         |
| [<span data-ttu-id="231c7-177">**receivedPackets**</span><span class="sxs-lookup"><span data-stu-id="231c7-177">**receivedPackets**</span></span>](wmplibiwmpnetwork-iwmpnetwork-receivedpackets--vb-and-c.md)<br/>     | <span data-ttu-id="231c7-178">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="231c7-178">Read-only</span></span><br/>  | <span data-ttu-id="231c7-179">Obtiene el número de paquetes recibidos.</span><span class="sxs-lookup"><span data-stu-id="231c7-179">Gets the number of packets received.</span></span><br/>                                              |
| [<span data-ttu-id="231c7-180">**receptionQuality**</span><span class="sxs-lookup"><span data-stu-id="231c7-180">**receptionQuality**</span></span>](wmplibiwmpnetwork-iwmpnetwork-receptionquality--vb-and-c.md)<br/>   | <span data-ttu-id="231c7-181">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="231c7-181">Read-only</span></span><br/>  | <span data-ttu-id="231c7-182">Obtiene el porcentaje de paquetes no perdidos en los últimos 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="231c7-182">Gets the percentage of packets not lost in the last 30 seconds.</span></span><br/>                   |
| [<span data-ttu-id="231c7-183">**recoveredPackets**</span><span class="sxs-lookup"><span data-stu-id="231c7-183">**recoveredPackets**</span></span>](wmplibiwmpnetwork-iwmpnetwork-recoveredpackets--vb-and-c.md)<br/>   | <span data-ttu-id="231c7-184">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="231c7-184">Read-only</span></span><br/>  | <span data-ttu-id="231c7-185">Obtiene el número de paquetes recuperados.</span><span class="sxs-lookup"><span data-stu-id="231c7-185">Gets the number of recovered packets.</span></span><br/>                                             |
| [<span data-ttu-id="231c7-186">**sourceProtocol**</span><span class="sxs-lookup"><span data-stu-id="231c7-186">**sourceProtocol**</span></span>](wmplibiwmpnetwork-iwmpnetwork-sourceprotocol--vb-and-c.md)<br/>       | <span data-ttu-id="231c7-187">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="231c7-187">Read-only</span></span><br/>  | <span data-ttu-id="231c7-188">Obtiene el protocolo de origen utilizado para recibir los datos.</span><span class="sxs-lookup"><span data-stu-id="231c7-188">Gets the source protocol used to receive data.</span></span><br/>                                    |



 

<span data-ttu-id="231c7-189">Obtenga una interfaz **IWMPNetwork** con la siguiente propiedad.</span><span class="sxs-lookup"><span data-stu-id="231c7-189">Get an **IWMPNetwork** interface by using the following property.</span></span>



| <span data-ttu-id="231c7-190">Object</span><span class="sxs-lookup"><span data-stu-id="231c7-190">Object</span></span>                                                                   | <span data-ttu-id="231c7-191">Propiedad</span><span class="sxs-lookup"><span data-stu-id="231c7-191">Property</span></span>                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="231c7-192">Objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="231c7-192">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="231c7-193">**Storage**</span><span class="sxs-lookup"><span data-stu-id="231c7-193">**network**</span></span>](axwmplib-axwindowsmediaplayer-network--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="231c7-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="231c7-194">Requirements</span></span>



| <span data-ttu-id="231c7-195">Requisito</span><span class="sxs-lookup"><span data-stu-id="231c7-195">Requirement</span></span> | <span data-ttu-id="231c7-196">Value</span><span class="sxs-lookup"><span data-stu-id="231c7-196">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="231c7-197">Encabezado</span><span class="sxs-lookup"><span data-stu-id="231c7-197">Header</span></span><br/> | <dl> <span data-ttu-id="231c7-198"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="231c7-198"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="231c7-199">Vea también</span><span class="sxs-lookup"><span data-stu-id="231c7-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="231c7-200">**Interfaces para Visual Basic .NET y C #**</span><span class="sxs-lookup"><span data-stu-id="231c7-200">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





