---
title: Objeto de red
description: El objeto de red proporciona las propiedades y los métodos utilizados para obtener acceso a las estadísticas relacionadas con la calidad de una conexión de red, y para especificar y recuperar la configuración del proxy de red.
ms.assetid: 5ae6137e-22f5-4a65-8793-b6f66adb4cba
keywords:
- Media Player de objetos de red de Windows
topic_type:
- apiref
api_name:
- Network Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d439679636bce773c43f5610060c4744ef4d5d7c
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104419765"
---
# <a name="network-object"></a><span data-ttu-id="6cd7a-104">Objeto de red</span><span class="sxs-lookup"><span data-stu-id="6cd7a-104">Network Object</span></span>

<span data-ttu-id="6cd7a-105">El objeto de **red** proporciona las propiedades y los métodos utilizados para obtener acceso a las estadísticas relacionadas con la calidad de una conexión de red, y para especificar y recuperar la configuración del proxy de red.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-105">The **Network** object provides properties and methods used to access statistics relating to the quality of a network connection, and to specify and retrieve the network proxy settings.</span></span>

<span data-ttu-id="6cd7a-106">El objeto de **red** admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-106">The **Network** object supports the following properties.</span></span>



| <span data-ttu-id="6cd7a-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6cd7a-107">Property</span></span>                                           | <span data-ttu-id="6cd7a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cd7a-108">Description</span></span>                                                                                 |
|----------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6cd7a-109">Consumo</span><span class="sxs-lookup"><span data-stu-id="6cd7a-109">bandWidth</span></span>](network-bandwidth.md)                 | <span data-ttu-id="6cd7a-110">Recupera el ancho de banda actual del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-110">Retrieves the current bandwidth of the media item.</span></span>                                          |
| [<span data-ttu-id="6cd7a-111">Velocidad</span><span class="sxs-lookup"><span data-stu-id="6cd7a-111">bitRate</span></span>](network-bitrate.md)                     | <span data-ttu-id="6cd7a-112">Recupera la velocidad de bits actual recibida.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-112">Retrieves the current bit rate being received.</span></span>                                              |
| [<span data-ttu-id="6cd7a-113">bufferingCount</span><span class="sxs-lookup"><span data-stu-id="6cd7a-113">bufferingCount</span></span>](network-bufferingcount.md)       | <span data-ttu-id="6cd7a-114">Recupera el número de veces que se ha producido el almacenamiento en búfer durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-114">Retrieves the number of times buffering occurred during playback.</span></span>                           |
| [<span data-ttu-id="6cd7a-115">bufferingProgress</span><span class="sxs-lookup"><span data-stu-id="6cd7a-115">bufferingProgress</span></span>](network-bufferingprogress.md) | <span data-ttu-id="6cd7a-116">Recupera el porcentaje de almacenamiento en búfer completado.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-116">Retrieves the percentage of buffering completed.</span></span>                                            |
| [<span data-ttu-id="6cd7a-117">bufferingTime</span><span class="sxs-lookup"><span data-stu-id="6cd7a-117">bufferingTime</span></span>](network-bufferingtime.md)         | <span data-ttu-id="6cd7a-118">Especifica o recupera la cantidad de tiempo de almacenamiento en búfer en milisegundos antes de que comience la reproducción.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-118">Specifies or retrieves the amount of buffering time in milliseconds before playback begins.</span></span> |
| [<span data-ttu-id="6cd7a-119">downloadProgress</span><span class="sxs-lookup"><span data-stu-id="6cd7a-119">downloadProgress</span></span>](network-downloadprogress.md)   | <span data-ttu-id="6cd7a-120">Recupera el porcentaje de descarga completada.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-120">Retrieves the percentage of download completed.</span></span>                                             |
| [<span data-ttu-id="6cd7a-121">encodedFrameRate</span><span class="sxs-lookup"><span data-stu-id="6cd7a-121">encodedFrameRate</span></span>](network-encodedframerate.md)   | <span data-ttu-id="6cd7a-122">Recupera la velocidad de fotogramas de vídeo especificada por el autor del contenido.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-122">Retrieves the video frame rate specified by the content author.</span></span>                             |
| [<span data-ttu-id="6cd7a-123">Velocidad</span><span class="sxs-lookup"><span data-stu-id="6cd7a-123">frameRate</span></span>](network-framerate.md)                 | <span data-ttu-id="6cd7a-124">Recupera la velocidad de fotogramas de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-124">Retrieves the current video frame rate.</span></span>                                                     |
| [<span data-ttu-id="6cd7a-125">framesSkipped</span><span class="sxs-lookup"><span data-stu-id="6cd7a-125">framesSkipped</span></span>](network-framesskipped.md)         | <span data-ttu-id="6cd7a-126">Recupera el número total de fotogramas omitidos durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-126">Retrieves the total number of frames skipped during playback.</span></span>                               |
| [<span data-ttu-id="6cd7a-127">lostPackets</span><span class="sxs-lookup"><span data-stu-id="6cd7a-127">lostPackets</span></span>](network-lostpackets.md)             | <span data-ttu-id="6cd7a-128">Recupera el número de paquetes perdidos.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-128">Retrieves the number of packets lost.</span></span>                                                       |
| [<span data-ttu-id="6cd7a-129">maxBandwidth</span><span class="sxs-lookup"><span data-stu-id="6cd7a-129">maxBandwidth</span></span>](network-maxbandwidth.md)           | <span data-ttu-id="6cd7a-130">Especifica o recupera el ancho de banda máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-130">Specifies or retrieves the maximum allowed bandwidth.</span></span>                                       |
| [<span data-ttu-id="6cd7a-131">maxBitRate</span><span class="sxs-lookup"><span data-stu-id="6cd7a-131">maxBitRate</span></span>](network-maxbitrate.md)               | <span data-ttu-id="6cd7a-132">Recupera la velocidad de bits de vídeo máxima posible.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-132">Retrieves the maximum possible video bit rate.</span></span>                                              |
| [<span data-ttu-id="6cd7a-133">receivedPackets</span><span class="sxs-lookup"><span data-stu-id="6cd7a-133">receivedPackets</span></span>](network-receivedpackets.md)     | <span data-ttu-id="6cd7a-134">Recupera el número de paquetes recibidos.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-134">Retrieves the number of packets received.</span></span>                                                   |
| [<span data-ttu-id="6cd7a-135">receptionQuality</span><span class="sxs-lookup"><span data-stu-id="6cd7a-135">receptionQuality</span></span>](network-receptionquality.md)   | <span data-ttu-id="6cd7a-136">Recupera el porcentaje de paquetes recibidos en los últimos 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-136">Retrieves the percentage of packets received in the last 30 seconds.</span></span>                        |
| [<span data-ttu-id="6cd7a-137">recoveredPackets</span><span class="sxs-lookup"><span data-stu-id="6cd7a-137">recoveredPackets</span></span>](network-recoveredpackets.md)   | <span data-ttu-id="6cd7a-138">Recupera el número de paquetes recuperados.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-138">Retrieves the number of recovered packets.</span></span>                                                  |
| [<span data-ttu-id="6cd7a-139">sourceProtocol</span><span class="sxs-lookup"><span data-stu-id="6cd7a-139">sourceProtocol</span></span>](network-sourceprotocol.md)       | <span data-ttu-id="6cd7a-140">Recupera el protocolo de origen usado para recibir los datos.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-140">Retrieves the source protocol used to receive data.</span></span>                                         |



 

<span data-ttu-id="6cd7a-141">El objeto de **red** admite los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-141">The **Network** object supports the following methods.</span></span>



| <span data-ttu-id="6cd7a-142">Método</span><span class="sxs-lookup"><span data-stu-id="6cd7a-142">Method</span></span>                                                       | <span data-ttu-id="6cd7a-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cd7a-143">Description</span></span>                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6cd7a-144">getProxyBypassForLocal</span><span class="sxs-lookup"><span data-stu-id="6cd7a-144">getProxyBypassForLocal</span></span>](network-getproxybypassforlocal.md) | <span data-ttu-id="6cd7a-145">Recupera un valor que indica si el servidor proxy se debe omitir si el servidor de origen está en una red local.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-145">Retrieves a value indicating whether the proxy server should by bypassed if the origin server is on a local network.</span></span> |
| [<span data-ttu-id="6cd7a-146">getProxyExceptionList</span><span class="sxs-lookup"><span data-stu-id="6cd7a-146">getProxyExceptionList</span></span>](network-getproxyexceptionlist.md)   | <span data-ttu-id="6cd7a-147">Recupera la lista de excepciones del proxy.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-147">Retrieves the proxy exception list.</span></span>                                                                                  |
| [<span data-ttu-id="6cd7a-148">getProxyName</span><span class="sxs-lookup"><span data-stu-id="6cd7a-148">getProxyName</span></span>](network-getproxyname.md)                     | <span data-ttu-id="6cd7a-149">Recupera el nombre de un servidor proxy que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-149">Retrieves the name of a proxy server to use.</span></span>                                                                         |
| [<span data-ttu-id="6cd7a-150">getProxyPort</span><span class="sxs-lookup"><span data-stu-id="6cd7a-150">getProxyPort</span></span>](network-getproxyport.md)                     | <span data-ttu-id="6cd7a-151">Recupera el puerto del proxy que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-151">Retrieves the proxy port to use.</span></span>                                                                                     |
| [<span data-ttu-id="6cd7a-152">getProxySettings</span><span class="sxs-lookup"><span data-stu-id="6cd7a-152">getProxySettings</span></span>](network-getproxysettings.md)             | <span data-ttu-id="6cd7a-153">Recupera la configuración del proxy para un protocolo determinado.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-153">Retrieves the proxy setting for a given protocol.</span></span>                                                                    |
| [<span data-ttu-id="6cd7a-154">setProxyBypassForLocal</span><span class="sxs-lookup"><span data-stu-id="6cd7a-154">setProxyBypassForLocal</span></span>](network-setproxybypassforlocal.md) | <span data-ttu-id="6cd7a-155">Especifica un valor que indica si el servidor proxy debe omitirse si el servidor de origen está en una red local.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-155">Specifies a value indicating whether the proxy server should by bypassed if the origin server is on a local network.</span></span> |
| [<span data-ttu-id="6cd7a-156">setProxyExceptionList</span><span class="sxs-lookup"><span data-stu-id="6cd7a-156">setProxyExceptionList</span></span>](network-setproxyexceptionlist.md)   | <span data-ttu-id="6cd7a-157">Especifica la lista de excepciones de proxy.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-157">Specifies the proxy exception list.</span></span>                                                                                  |
| [<span data-ttu-id="6cd7a-158">setProxyName</span><span class="sxs-lookup"><span data-stu-id="6cd7a-158">setProxyName</span></span>](network-setproxyname.md)                     | <span data-ttu-id="6cd7a-159">Especifica el nombre de un servidor proxy que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-159">Specifies the name of a proxy server to use.</span></span>                                                                         |
| [<span data-ttu-id="6cd7a-160">setProxyPort</span><span class="sxs-lookup"><span data-stu-id="6cd7a-160">setProxyPort</span></span>](network-setproxyport.md)                     | <span data-ttu-id="6cd7a-161">Especifica el puerto del proxy que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-161">Specifies the proxy port to use.</span></span>                                                                                     |
| [<span data-ttu-id="6cd7a-162">setProxySettings</span><span class="sxs-lookup"><span data-stu-id="6cd7a-162">setProxySettings</span></span>](network-setproxysettings.md)             | <span data-ttu-id="6cd7a-163">Especifica la configuración de proxy para un protocolo determinado.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-163">Specifies the proxy setting for a given protocol.</span></span>                                                                    |



 

<span data-ttu-id="6cd7a-164">Se tiene acceso al objeto de **red** a través de la siguiente propiedad.</span><span class="sxs-lookup"><span data-stu-id="6cd7a-164">The **Network** object is accessed through the following property.</span></span>



| <span data-ttu-id="6cd7a-165">Object</span><span class="sxs-lookup"><span data-stu-id="6cd7a-165">Object</span></span>                      | <span data-ttu-id="6cd7a-166">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6cd7a-166">Property</span></span>                      |
|-----------------------------|-------------------------------|
| [<span data-ttu-id="6cd7a-167">Reproductor</span><span class="sxs-lookup"><span data-stu-id="6cd7a-167">Player</span></span>](player-object.md) | [<span data-ttu-id="6cd7a-168">network</span><span class="sxs-lookup"><span data-stu-id="6cd7a-168">network</span></span>](player-network.md) |



 

## <a name="see-also"></a><span data-ttu-id="6cd7a-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="6cd7a-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cd7a-170">**Referencia del modelo de objetos para scripting**</span><span class="sxs-lookup"><span data-stu-id="6cd7a-170">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




