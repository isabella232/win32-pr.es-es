---
title: Configuración de red predeterminada
description: Configuración de red predeterminada
ms.assetid: 07464107-9cf7-4ed0-a76b-17ea153399a1
keywords:
- SDK de Windows Media Format, configuración de red predeterminada
- Advanced Systems Format (ASF), configuración de red predeterminada
- ASF (formato de sistemas avanzados), configuración de red predeterminada
- SDK de Windows Media Format, configuración de red
- Advanced Systems Format (ASF), configuración de red
- ASF (formato de sistemas avanzados), configuración de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f219a60d9211b63eb124500c014452a0143d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903864"
---
# <a name="default-networking-settings"></a><span data-ttu-id="89f41-109">Configuración de red predeterminada</span><span class="sxs-lookup"><span data-stu-id="89f41-109">Default Networking Settings</span></span>

<span data-ttu-id="89f41-110">En las tablas siguientes se describe la configuración predeterminada de los parámetros de red en el SDK de Windows Media Format, agrupados por interfaz.</span><span class="sxs-lookup"><span data-stu-id="89f41-110">The following tables describe the default settings of the networking parameters in the Windows Media Format SDK, grouped by interface.</span></span>



| <span data-ttu-id="89f41-111">IWMReaderNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="89f41-111">IWMReaderNetworkConfig</span></span>                | <span data-ttu-id="89f41-112">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="89f41-112">Default setting</span></span>              |
|---------------------------------------|------------------------------|
| <span data-ttu-id="89f41-113">Tiempo de almacenamiento en búfer</span><span class="sxs-lookup"><span data-stu-id="89f41-113">Buffering time</span></span>                        | <span data-ttu-id="89f41-114">5 segundos</span><span class="sxs-lookup"><span data-stu-id="89f41-114">5 seconds</span></span>                    |
| <span data-ttu-id="89f41-115">UseFixedUDPPort</span><span class="sxs-lookup"><span data-stu-id="89f41-115">UseFixedUDPPort</span></span>                       | <span data-ttu-id="89f41-116">false</span><span class="sxs-lookup"><span data-stu-id="89f41-116">FALSE</span></span>                        |
| <span data-ttu-id="89f41-117">FixedUDPPort</span><span class="sxs-lookup"><span data-stu-id="89f41-117">FixedUDPPort</span></span>                          | <span data-ttu-id="89f41-118">0 (no válido)</span><span class="sxs-lookup"><span data-stu-id="89f41-118">0 (not valid)</span></span>                |
| <span data-ttu-id="89f41-119">ProxySetting: HTTP</span><span class="sxs-lookup"><span data-stu-id="89f41-119">ProxySetting: HTTP</span></span>                    | <span data-ttu-id="89f41-120">\_Explorador de \_ configuración del proxy WMT \_</span><span class="sxs-lookup"><span data-stu-id="89f41-120">WMT\_PROXY\_SETTING\_BROWSER</span></span> |
| <span data-ttu-id="89f41-121">ProxySetting: MMS</span><span class="sxs-lookup"><span data-stu-id="89f41-121">ProxySetting: MMS</span></span>                     | <span data-ttu-id="89f41-122">\_configuración del proxy WMT \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="89f41-122">WMT\_PROXY\_SETTING\_NONE</span></span>    |
| <span data-ttu-id="89f41-123">ProxySetting: RTSP</span><span class="sxs-lookup"><span data-stu-id="89f41-123">ProxySetting: RTSP</span></span>                    | <span data-ttu-id="89f41-124">\_configuración del proxy WMT \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="89f41-124">WMT\_PROXY\_SETTING\_NONE</span></span>    |
| <span data-ttu-id="89f41-125">ProxyHostName (HTTP, MMS, RTSP)</span><span class="sxs-lookup"><span data-stu-id="89f41-125">ProxyHostName (HTTP, MMS, RTSP)</span></span>       | <span data-ttu-id="89f41-126">""</span><span class="sxs-lookup"><span data-stu-id="89f41-126">""</span></span>                           |
| <span data-ttu-id="89f41-127">ProxyPort: HTTP</span><span class="sxs-lookup"><span data-stu-id="89f41-127">ProxyPort: HTTP</span></span>                       | <span data-ttu-id="89f41-128">80</span><span class="sxs-lookup"><span data-stu-id="89f41-128">80</span></span>                           |
| <span data-ttu-id="89f41-129">ProxyPort: MMS</span><span class="sxs-lookup"><span data-stu-id="89f41-129">ProxyPort: MMS</span></span>                        | <span data-ttu-id="89f41-130">1755</span><span class="sxs-lookup"><span data-stu-id="89f41-130">1755</span></span>                         |
| <span data-ttu-id="89f41-131">ProxtPort: RTSP</span><span class="sxs-lookup"><span data-stu-id="89f41-131">ProxtPort: RTSP</span></span>                       | <span data-ttu-id="89f41-132">554</span><span class="sxs-lookup"><span data-stu-id="89f41-132">554</span></span>                          |
| <span data-ttu-id="89f41-133">ProxyExceptionList (HTTP, MMS, RTSP)</span><span class="sxs-lookup"><span data-stu-id="89f41-133">ProxyExceptionList (HTTP, MMS, RTSP)</span></span>  | <span data-ttu-id="89f41-134">""</span><span class="sxs-lookup"><span data-stu-id="89f41-134">""</span></span>                           |
| <span data-ttu-id="89f41-135">ProxyBypassForLocal (HTTP, MMS, RTSP)</span><span class="sxs-lookup"><span data-stu-id="89f41-135">ProxyBypassForLocal (HTTP, MMS, RTSP)</span></span> | <span data-ttu-id="89f41-136">false</span><span class="sxs-lookup"><span data-stu-id="89f41-136">FALSE</span></span>                        |
| <span data-ttu-id="89f41-137">ForceRerunAutoDetection</span><span class="sxs-lookup"><span data-stu-id="89f41-137">ForceRerunAutoDetection</span></span>               | <span data-ttu-id="89f41-138">false</span><span class="sxs-lookup"><span data-stu-id="89f41-138">FALSE</span></span>                        |
| <span data-ttu-id="89f41-139">EnableMulticast</span><span class="sxs-lookup"><span data-stu-id="89f41-139">EnableMulticast</span></span>                       | <span data-ttu-id="89f41-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="89f41-140">TRUE</span></span>                         |
| <span data-ttu-id="89f41-141">EnableHTTP</span><span class="sxs-lookup"><span data-stu-id="89f41-141">EnableHTTP</span></span>                            | <span data-ttu-id="89f41-142">TRUE</span><span class="sxs-lookup"><span data-stu-id="89f41-142">TRUE</span></span>                         |
| <span data-ttu-id="89f41-143">EnableTCP</span><span class="sxs-lookup"><span data-stu-id="89f41-143">EnableTCP</span></span>                             | <span data-ttu-id="89f41-144">TRUE</span><span class="sxs-lookup"><span data-stu-id="89f41-144">TRUE</span></span>                         |
| <span data-ttu-id="89f41-145">EnableUDP</span><span class="sxs-lookup"><span data-stu-id="89f41-145">EnableUDP</span></span>                             | <span data-ttu-id="89f41-146">TRUE</span><span class="sxs-lookup"><span data-stu-id="89f41-146">TRUE</span></span>                         |
| <span data-ttu-id="89f41-147">Ancho de banda de conexión</span><span class="sxs-lookup"><span data-stu-id="89f41-147">Connection Bandwidth</span></span>                  | <span data-ttu-id="89f41-148">0 (detección automática)</span><span class="sxs-lookup"><span data-stu-id="89f41-148">0 (auto-detect)</span></span>              |



 



| <span data-ttu-id="89f41-149">IWMReaderNetworkConfig2</span><span class="sxs-lookup"><span data-stu-id="89f41-149">IWMReaderNetworkConfig2</span></span>        | <span data-ttu-id="89f41-150">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="89f41-150">Default setting</span></span>        |
|--------------------------------|------------------------|
| <span data-ttu-id="89f41-151">Duración de transmisión por secuencias acelerada</span><span class="sxs-lookup"><span data-stu-id="89f41-151">Accelerated streaming duration</span></span> | <span data-ttu-id="89f41-152">100 millones (10 segundos)</span><span class="sxs-lookup"><span data-stu-id="89f41-152">100000000 (10 seconds)</span></span> |
| <span data-ttu-id="89f41-153">Habilitar almacenamiento en caché de contenido</span><span class="sxs-lookup"><span data-stu-id="89f41-153">Enable content caching</span></span>         | <span data-ttu-id="89f41-154">TRUE</span><span class="sxs-lookup"><span data-stu-id="89f41-154">TRUE</span></span>                   |
| <span data-ttu-id="89f41-155">Habilitar caché rápida</span><span class="sxs-lookup"><span data-stu-id="89f41-155">Enable fast cache</span></span>              | <span data-ttu-id="89f41-156">TRUE</span><span class="sxs-lookup"><span data-stu-id="89f41-156">TRUE</span></span>                   |
| <span data-ttu-id="89f41-157">Habilitar reenvíos</span><span class="sxs-lookup"><span data-stu-id="89f41-157">Enable resends</span></span>                 | <span data-ttu-id="89f41-158">TRUE</span><span class="sxs-lookup"><span data-stu-id="89f41-158">TRUE</span></span>                   |
| <span data-ttu-id="89f41-159">Habilitar el simplificado del contenido</span><span class="sxs-lookup"><span data-stu-id="89f41-159">Enable content thinning</span></span>        | <span data-ttu-id="89f41-160">TRUE</span><span class="sxs-lookup"><span data-stu-id="89f41-160">TRUE</span></span>                   |
| <span data-ttu-id="89f41-161">Límite de reconexión</span><span class="sxs-lookup"><span data-stu-id="89f41-161">Reconnect limit</span></span>                | <span data-ttu-id="89f41-162">25</span><span class="sxs-lookup"><span data-stu-id="89f41-162">25</span></span>                     |



 



| <span data-ttu-id="89f41-163">IWMWriterNetworkSink</span><span class="sxs-lookup"><span data-stu-id="89f41-163">IWMWriterNetworkSink</span></span> | <span data-ttu-id="89f41-164">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="89f41-164">Default setting</span></span>         |
|----------------------|-------------------------|
| <span data-ttu-id="89f41-165">Número máximo de clientes</span><span class="sxs-lookup"><span data-stu-id="89f41-165">Maximum clients</span></span>      | <span data-ttu-id="89f41-166">5</span><span class="sxs-lookup"><span data-stu-id="89f41-166">5</span></span>                       |
| <span data-ttu-id="89f41-167">Protocolo de red.</span><span class="sxs-lookup"><span data-stu-id="89f41-167">Network protocol</span></span>     | <span data-ttu-id="89f41-168">0 ( \_ Protocolo WMT \_ http)</span><span class="sxs-lookup"><span data-stu-id="89f41-168">0 (WMT\_PROTOCOL\_HTTP)</span></span> |
| <span data-ttu-id="89f41-169">Dirección URL del host</span><span class="sxs-lookup"><span data-stu-id="89f41-169">Host URL</span></span>             | <span data-ttu-id="89f41-170">0 (no válido)</span><span class="sxs-lookup"><span data-stu-id="89f41-170">0 (not valid)</span></span>           |



 



| <span data-ttu-id="89f41-171">IWMWriterAdvanced2</span><span class="sxs-lookup"><span data-stu-id="89f41-171">IWMWriterAdvanced2</span></span>  | <span data-ttu-id="89f41-172">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="89f41-172">Default setting</span></span>             |
|---------------------|-----------------------------|
| <span data-ttu-id="89f41-173">Tamaño máximo de paquete</span><span class="sxs-lookup"><span data-stu-id="89f41-173">Maximum packet size</span></span> | <span data-ttu-id="89f41-174">1400</span><span class="sxs-lookup"><span data-stu-id="89f41-174">1400</span></span>                        |
| <span data-ttu-id="89f41-175">ID. de cliente de registro</span><span class="sxs-lookup"><span data-stu-id="89f41-175">Log client ID</span></span>       | <span data-ttu-id="89f41-176">false</span><span class="sxs-lookup"><span data-stu-id="89f41-176">FALSE</span></span>                       |
| <span data-ttu-id="89f41-177">Modo de reproducción</span><span class="sxs-lookup"><span data-stu-id="89f41-177">Play mode</span></span>           | <span data-ttu-id="89f41-178">\_ \_ selección activa del modo de reproducción WMT \_</span><span class="sxs-lookup"><span data-stu-id="89f41-178">WMT\_PLAY\_MODE\_AUTOSELECT</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="89f41-179">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="89f41-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89f41-180">**Implementación de la funcionalidad de red**</span><span class="sxs-lookup"><span data-stu-id="89f41-180">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> </dl>

 

 




