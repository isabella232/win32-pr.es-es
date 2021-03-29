---
title: Configuración del registro del puerto del firewall
description: Configuración del registro del puerto del firewall
ms.assetid: 86995f2c-8794-45da-9dca-9cdd388b2a21
keywords:
- Windows Media Player, configuración del registro del puerto del firewall
- Windows Media Player, configuración del registro de puertos
- Media Player de Windows, registro
- registro, configuración de puerto de Firewall
- registro, configuración de Puerto
- registro, configuración para Windows Media Player
- configuración del registro del puerto del firewall
- configuración del registro de Puerto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e231732e8d62efce575ae3fdee5edc63975f23c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903184"
---
# <a name="firewall-port-registry-settings"></a><span data-ttu-id="0b371-111">Configuración del registro del puerto del firewall</span><span class="sxs-lookup"><span data-stu-id="0b371-111">Firewall Port Registry Settings</span></span>

<span data-ttu-id="0b371-112">Windows Media Player coloca entradas en el registro para que los firewalls puedan determinar si se deben abrir o cerrar los puertos utilizados por el uso compartido de la biblioteca multimedia.</span><span class="sxs-lookup"><span data-stu-id="0b371-112">Windows Media Player places entries in the registry so that firewalls can determine whether to open or close the ports that are used by media library sharing.</span></span>

<span data-ttu-id="0b371-113">**Entrada del registro AcceptedEULA**</span><span class="sxs-lookup"><span data-stu-id="0b371-113">**AcceptedEULA Registry Entry**</span></span>

<span data-ttu-id="0b371-114">Windows Media Player usa la siguiente entrada del registro para indicar si el usuario ha aceptado el contrato de licencia para el usuario final (CLUF).</span><span class="sxs-lookup"><span data-stu-id="0b371-114">Windows Media Player uses the following registry entry to indicate whether the user has accepted the end user license agreement (EULA).</span></span>


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"AcceptedEULA" = dword:value
```



<span data-ttu-id="0b371-115">Un valor de 1 indica que el usuario ha aceptado el contrato de licencia.</span><span class="sxs-lookup"><span data-stu-id="0b371-115">A value of 1 indicates that the user has accepted the license agreement.</span></span> <span data-ttu-id="0b371-116">Un valor de 0 indica que el usuario no ha aceptado el contrato de licencia.</span><span class="sxs-lookup"><span data-stu-id="0b371-116">A value of 0 indicates that the user has not accepted the license agreement.</span></span>

<span data-ttu-id="0b371-117">**Entrada del registro WMPNSSFirewallPortsOpen**</span><span class="sxs-lookup"><span data-stu-id="0b371-117">**WMPNSSFirewallPortsOpen Registry Entry**</span></span>

<span data-ttu-id="0b371-118">Windows Media Player usa la siguiente entrada del registro para indicar si el usuario ha elegido compartir su biblioteca multimedia con otros equipos de una red doméstica.</span><span class="sxs-lookup"><span data-stu-id="0b371-118">Windows Media Player uses the following registry entry to indicate whether the user has chosen to share his or her media library with other computers on a home network.</span></span>


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"WMPNSSFirewallPortsOpen" = dword:value
```



<span data-ttu-id="0b371-119">Un valor de 1 indica que el usuario ha elegido compartir la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="0b371-119">A value of 1 indicates that the user has chosen to share the library.</span></span> <span data-ttu-id="0b371-120">Un valor de 0 indica que el usuario ha elegido no compartir la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="0b371-120">A value of 0 indicates that the user has chosen not to share the library.</span></span>

<span data-ttu-id="0b371-121">**Puertos relacionados con el uso compartido de la biblioteca multimedia**</span><span class="sxs-lookup"><span data-stu-id="0b371-121">**Ports Related to Media Library Sharing**</span></span>

<span data-ttu-id="0b371-122">En Windows Vista, si la entrada del registro **WMPNSSFirewallPortsOpen** tiene un valor de 1, deben abrirse los puertos siguientes.</span><span class="sxs-lookup"><span data-stu-id="0b371-122">On Windows Vista, if the **WMPNSSFirewallPortsOpen** registry entry has a value of 1, the following ports should be open.</span></span>



| <span data-ttu-id="0b371-123">Port</span><span class="sxs-lookup"><span data-stu-id="0b371-123">Port</span></span>          | <span data-ttu-id="0b371-124">Protocolo</span><span class="sxs-lookup"><span data-stu-id="0b371-124">Protocol</span></span>                  | <span data-ttu-id="0b371-125">Proceso</span><span class="sxs-lookup"><span data-stu-id="0b371-125">Process</span></span>                         | <span data-ttu-id="0b371-126">Dirección</span><span class="sxs-lookup"><span data-stu-id="0b371-126">Direction</span></span>            |
|---------------|---------------------------|---------------------------------|----------------------|
| <span data-ttu-id="0b371-127">554</span><span class="sxs-lookup"><span data-stu-id="0b371-127">554</span></span>           | <span data-ttu-id="0b371-128">RTSP DE TCP</span><span class="sxs-lookup"><span data-stu-id="0b371-128">TCP RTSP</span></span>                  | <span data-ttu-id="0b371-129">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="0b371-129">wmpnetwk.exe</span></span>                    | <span data-ttu-id="0b371-130">entrante y saliente</span><span class="sxs-lookup"><span data-stu-id="0b371-130">inbound and outbound</span></span> |
| <span data-ttu-id="0b371-131">8554-8558</span><span class="sxs-lookup"><span data-stu-id="0b371-131">8554 - 8558</span></span>   | <span data-ttu-id="0b371-132">RTSP DE TCP</span><span class="sxs-lookup"><span data-stu-id="0b371-132">TCP RTSP</span></span>                  | <span data-ttu-id="0b371-133">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="0b371-133">wmpnetwk.exe</span></span>                    | <span data-ttu-id="0b371-134">entrante y saliente</span><span class="sxs-lookup"><span data-stu-id="0b371-134">inbound and outbound</span></span> |
| <span data-ttu-id="0b371-135">5004, 5005</span><span class="sxs-lookup"><span data-stu-id="0b371-135">5004, 5005</span></span>    | <span data-ttu-id="0b371-136">UDP RTCP/RTP</span><span class="sxs-lookup"><span data-stu-id="0b371-136">UDP RTCP/RTP</span></span>              | <span data-ttu-id="0b371-137">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="0b371-137">wmpnetwk.exe</span></span>                    | <span data-ttu-id="0b371-138">entrante y saliente</span><span class="sxs-lookup"><span data-stu-id="0b371-138">inbound and outbound</span></span> |
| <span data-ttu-id="0b371-139">50004-50013</span><span class="sxs-lookup"><span data-stu-id="0b371-139">50004 - 50013</span></span> | <span data-ttu-id="0b371-140">UDP RTCP/RTP</span><span class="sxs-lookup"><span data-stu-id="0b371-140">UDP RTCP/RTP</span></span>              | <span data-ttu-id="0b371-141">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="0b371-141">wmpnetwk.exe</span></span>                    | <span data-ttu-id="0b371-142">entrante y saliente</span><span class="sxs-lookup"><span data-stu-id="0b371-142">inbound and outbound</span></span> |
| <span data-ttu-id="0b371-143">1900</span><span class="sxs-lookup"><span data-stu-id="0b371-143">1900</span></span>          | <span data-ttu-id="0b371-144">SSDP DE UDP</span><span class="sxs-lookup"><span data-stu-id="0b371-144">UDP SSDP</span></span>                  | <span data-ttu-id="0b371-145">SSDPsrv en svchost.exe</span><span class="sxs-lookup"><span data-stu-id="0b371-145">SSDPsrv in svchost.exe</span></span>          | <span data-ttu-id="0b371-146">entrante y saliente</span><span class="sxs-lookup"><span data-stu-id="0b371-146">inbound and outbound</span></span> |
| <span data-ttu-id="0b371-147">2869</span><span class="sxs-lookup"><span data-stu-id="0b371-147">2869</span></span>          | <span data-ttu-id="0b371-148">SSDP de TCP, UPnP</span><span class="sxs-lookup"><span data-stu-id="0b371-148">TCP SSDP, UPnP</span></span>            | <span data-ttu-id="0b371-149">SSDPsrv/UPnPHost en svchost.exe</span><span class="sxs-lookup"><span data-stu-id="0b371-149">SSDPsrv/UPnPHost in svchost.exe</span></span> | <span data-ttu-id="0b371-150">hacia la ciudad</span><span class="sxs-lookup"><span data-stu-id="0b371-150">inbound</span></span>              |
| <span data-ttu-id="0b371-151">10280-10284</span><span class="sxs-lookup"><span data-stu-id="0b371-151">10280 - 10284</span></span> | <span data-ttu-id="0b371-152">Registro de WMDRM-ND UDP</span><span class="sxs-lookup"><span data-stu-id="0b371-152">UDP WMDRM-ND registration</span></span> | <span data-ttu-id="0b371-153">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="0b371-153">wmpnetwk.exe</span></span>                    | <span data-ttu-id="0b371-154">entrante y saliente</span><span class="sxs-lookup"><span data-stu-id="0b371-154">inbound and outbound</span></span> |
| <span data-ttu-id="0b371-155">10243</span><span class="sxs-lookup"><span data-stu-id="0b371-155">10243</span></span>         | <span data-ttu-id="0b371-156">HTTP DE TCP</span><span class="sxs-lookup"><span data-stu-id="0b371-156">TCP HTTP</span></span>                  | <span data-ttu-id="0b371-157">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="0b371-157">wmpnetwk.exe</span></span>                    | <span data-ttu-id="0b371-158">hacia la ciudad</span><span class="sxs-lookup"><span data-stu-id="0b371-158">inbound</span></span>              |
| <span data-ttu-id="0b371-159">2177</span><span class="sxs-lookup"><span data-stu-id="0b371-159">2177</span></span>          | <span data-ttu-id="0b371-160">QWAVE TCP UDP</span><span class="sxs-lookup"><span data-stu-id="0b371-160">TCP UDP qWAVE</span></span>             | <span data-ttu-id="0b371-161">svchost.exe</span><span class="sxs-lookup"><span data-stu-id="0b371-161">svchost.exe</span></span>                     | <span data-ttu-id="0b371-162">entrante y saliente</span><span class="sxs-lookup"><span data-stu-id="0b371-162">inbound and outbound</span></span> |



 

<span data-ttu-id="0b371-163">En Windows Vista, si la entrada del registro **AcceptedEULA** tiene un valor de 1, deben abrirse los puertos siguientes.</span><span class="sxs-lookup"><span data-stu-id="0b371-163">On Windows Vista, if the **AcceptedEULA** registry entry has a value of 1, the following ports should be open.</span></span>



| <span data-ttu-id="0b371-164">Port</span><span class="sxs-lookup"><span data-stu-id="0b371-164">Port</span></span>          | <span data-ttu-id="0b371-165">Protocolo</span><span class="sxs-lookup"><span data-stu-id="0b371-165">Protocol</span></span>       | <span data-ttu-id="0b371-166">Proceso</span><span class="sxs-lookup"><span data-stu-id="0b371-166">Process</span></span>                         | <span data-ttu-id="0b371-167">Dirección</span><span class="sxs-lookup"><span data-stu-id="0b371-167">Direction</span></span>            |
|---------------|----------------|---------------------------------|----------------------|
| <span data-ttu-id="0b371-168">Todos los puertos UDP</span><span class="sxs-lookup"><span data-stu-id="0b371-168">All UDP ports</span></span> | <span data-ttu-id="0b371-169">RTP DE UDP, MSB</span><span class="sxs-lookup"><span data-stu-id="0b371-169">UDP RTP, MSB</span></span>   | <span data-ttu-id="0b371-170">wmplayer.exe, cualquier subred</span><span class="sxs-lookup"><span data-stu-id="0b371-170">wmplayer.exe, any subnet</span></span>        | <span data-ttu-id="0b371-171">hacia la ciudad</span><span class="sxs-lookup"><span data-stu-id="0b371-171">inbound</span></span>              |
| <span data-ttu-id="0b371-172">1900</span><span class="sxs-lookup"><span data-stu-id="0b371-172">1900</span></span>          | <span data-ttu-id="0b371-173">SSDP DE UDP</span><span class="sxs-lookup"><span data-stu-id="0b371-173">UDP SSDP</span></span>       | <span data-ttu-id="0b371-174">SSDPsrv/UPnPHost en svchost.exe</span><span class="sxs-lookup"><span data-stu-id="0b371-174">SSDPsrv/UPnPHost in svchost.exe</span></span> | <span data-ttu-id="0b371-175">entrante y saliente</span><span class="sxs-lookup"><span data-stu-id="0b371-175">inbound and outbound</span></span> |
| <span data-ttu-id="0b371-176">2869</span><span class="sxs-lookup"><span data-stu-id="0b371-176">2869</span></span>          | <span data-ttu-id="0b371-177">SSDP de TCP, UPnP</span><span class="sxs-lookup"><span data-stu-id="0b371-177">TCP SSDP, UPnP</span></span> | <span data-ttu-id="0b371-178">SSDPsrv, UPnPHost</span><span class="sxs-lookup"><span data-stu-id="0b371-178">SSDPsrv, UPnPHost</span></span>               | <span data-ttu-id="0b371-179">hacia la ciudad</span><span class="sxs-lookup"><span data-stu-id="0b371-179">inbound</span></span>              |



 

<span data-ttu-id="0b371-180">En Microsoft Windows XP, si la entrada del registro **WMPNSSFirewallPortsOpen** tiene un valor de 1, deben abrirse los puertos siguientes.</span><span class="sxs-lookup"><span data-stu-id="0b371-180">On Microsoft Windows XP, if the **WMPNSSFirewallPortsOpen** registry entry has a value of 1, the following ports should be open.</span></span>



| <span data-ttu-id="0b371-181">Port</span><span class="sxs-lookup"><span data-stu-id="0b371-181">Port</span></span>          | <span data-ttu-id="0b371-182">Protocolo</span><span class="sxs-lookup"><span data-stu-id="0b371-182">Protocol</span></span>                  | <span data-ttu-id="0b371-183">Proceso</span><span class="sxs-lookup"><span data-stu-id="0b371-183">Process</span></span>                         | <span data-ttu-id="0b371-184">Dirección</span><span class="sxs-lookup"><span data-stu-id="0b371-184">Direction</span></span>            |
|---------------|---------------------------|---------------------------------|----------------------|
| <span data-ttu-id="0b371-185">1900</span><span class="sxs-lookup"><span data-stu-id="0b371-185">1900</span></span>          | <span data-ttu-id="0b371-186">SSDP DE UDP</span><span class="sxs-lookup"><span data-stu-id="0b371-186">UDP SSDP</span></span>                  | <span data-ttu-id="0b371-187">SSDPsrv en svchost.exe</span><span class="sxs-lookup"><span data-stu-id="0b371-187">SSDPsrv in svchost.exe</span></span>          | <span data-ttu-id="0b371-188">entrante y saliente</span><span class="sxs-lookup"><span data-stu-id="0b371-188">inbound and outbound</span></span> |
| <span data-ttu-id="0b371-189">2869</span><span class="sxs-lookup"><span data-stu-id="0b371-189">2869</span></span>          | <span data-ttu-id="0b371-190">SSDP de TCP, UPnP</span><span class="sxs-lookup"><span data-stu-id="0b371-190">TCP SSDP, UPnP</span></span>            | <span data-ttu-id="0b371-191">SSDPsrv/UPnPHost en svchost.exe</span><span class="sxs-lookup"><span data-stu-id="0b371-191">SSDPsrv/UPnPHost in svchost.exe</span></span> | <span data-ttu-id="0b371-192">hacia la ciudad</span><span class="sxs-lookup"><span data-stu-id="0b371-192">inbound</span></span>              |
| <span data-ttu-id="0b371-193">10280-10284</span><span class="sxs-lookup"><span data-stu-id="0b371-193">10280 - 10284</span></span> | <span data-ttu-id="0b371-194">Registro de WMDRM-ND UDP</span><span class="sxs-lookup"><span data-stu-id="0b371-194">UDP WMDRM-ND registration</span></span> | <span data-ttu-id="0b371-195">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="0b371-195">wmpnetwk.exe</span></span>                    | <span data-ttu-id="0b371-196">entrante y saliente</span><span class="sxs-lookup"><span data-stu-id="0b371-196">inbound and outbound</span></span> |
| <span data-ttu-id="0b371-197">10243</span><span class="sxs-lookup"><span data-stu-id="0b371-197">10243</span></span>         | <span data-ttu-id="0b371-198">HTTP DE TCP</span><span class="sxs-lookup"><span data-stu-id="0b371-198">TCP HTTP</span></span>                  | <span data-ttu-id="0b371-199">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="0b371-199">wmpnetwk.exe</span></span>                    | <span data-ttu-id="0b371-200">hacia la ciudad</span><span class="sxs-lookup"><span data-stu-id="0b371-200">inbound</span></span>              |



 

## <a name="related-topics"></a><span data-ttu-id="0b371-201">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0b371-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b371-202">**Configuración del registro**</span><span class="sxs-lookup"><span data-stu-id="0b371-202">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




