---
title: Configurar el registro para asignaciones de puerto y enlace selectivo
description: A partir de Windows 2000, se debe usar una utilidad en el kit de recursos de Windows denominada Rpccfg.exe para establecer enlaces. Para obtener más información, consulte el kit de recursos de Windows para conocer la versión del sistema operativo adecuada.
ms.assetid: a33b51e7-2ded-46bd-aadb-27cbd99e1029
keywords:
- RPC llamada a procedimiento remoto, tareas, configurar el registro para asignaciones de puerto y enlace selectivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef1749fab1beb8e637d208a7d7af64577066fe6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103995706"
---
# <a name="configuring-the-registry-for-port-allocations-and-selective-binding"></a><span data-ttu-id="7a4ca-105">Configurar el registro para asignaciones de puerto y enlace selectivo</span><span class="sxs-lookup"><span data-stu-id="7a4ca-105">Configuring the Registry for Port Allocations and Selective Binding</span></span>

<span data-ttu-id="7a4ca-106">A partir de Windows 2000, se debe usar una utilidad en el kit de recursos de Windows denominada Rpccfg.exe para establecer enlaces.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-106">Starting with Windows 2000, a utility in the Windows Resource Kit called Rpccfg.exe should be used to set bindings.</span></span> <span data-ttu-id="7a4ca-107">Para obtener más información, consulte el kit de recursos de Windows para conocer la versión del sistema operativo adecuada.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-107">For more information, consult the Windows Resource Kit for the appropriate operating system version.</span></span>

<span data-ttu-id="7a4ca-108">En el caso de las versiones de Windows anteriores a Windows 2000, las claves del registro de la tabla siguiente especifican los valores predeterminados del sistema para la asignación dinámica de puertos y para el enlace a NIC en equipos de host múltiple.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-108">For versions of windows prior to Windows 2000, the registry keys in the following table specify the system defaults for dynamic port allocation and for binding to NICs on multihomed computers.</span></span> <span data-ttu-id="7a4ca-109">Primero debe crear estas claves y, a continuación, especificar la configuración adecuada.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-109">You must first create these keys and then specify the appropriate settings.</span></span>

<span data-ttu-id="7a4ca-110">El uso de la función [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) afecta a esta configuración.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-110">Using the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function affects these settings.</span></span> <span data-ttu-id="7a4ca-111">Los desarrolladores deben estar familiarizados con la configuración del registro que se explica en esta sección y la función **RpcServerUseProtseqEx** al administrar las asignaciones de puertos.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-111">Developers should be familiar with the registry settings explained in this section and the **RpcServerUseProtseqEx** function when managing port allocations.</span></span> <span data-ttu-id="7a4ca-112">Un ejemplo con tres aplicaciones hipotéticas sigue la tabla siguiente y muestra cómo interoperan esta configuración y la función **RpcServerUseProtseqEx** .</span><span class="sxs-lookup"><span data-stu-id="7a4ca-112">An example with three hypothetical applications follows the table below, and illustrates how these settings and the **RpcServerUseProtseqEx** function interoperate.</span></span>

<span data-ttu-id="7a4ca-113">Si falta una clave o contiene un valor no válido, toda la configuración se marca como no válida y se producirá un error en todas las llamadas a **RpcServerUseProtseq \*** a través de [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) o [**ncadg \_ IP \_ UDP**](/windows/desktop/Midl/ncadg-ip-udp) .</span><span class="sxs-lookup"><span data-stu-id="7a4ca-113">If a key is missing or if it contains an invalid value, the entire configuration is marked as invalid, and all **RpcServerUseProtseq\*** calls over [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp) or [**ncadg\_ip\_udp**](/windows/desktop/Midl/ncadg-ip-udp) will fail.</span></span>

> [!Note]  
> <span data-ttu-id="7a4ca-114">Los puertos asignados a un proceso permanecen asignados hasta que se agota el proceso.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-114">Ports allocated to a process remain allocated until that process dies.</span></span> <span data-ttu-id="7a4ca-115">Si todos los puertos disponibles están en uso, la función devuelve \_ \_ \_ \_ los recursos de RPC.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-115">If all available ports are in use, the function returns RPC\_S\_OUT\_OF\_RESOURCES.</span></span>

 



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7a4ca-116">Clave de Puerto</span><span class="sxs-lookup"><span data-stu-id="7a4ca-116">Port key</span></span></th>
<th><span data-ttu-id="7a4ca-117">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7a4ca-117">Data type</span></span></th>
<th><span data-ttu-id="7a4ca-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a4ca-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               Ports</code></pre></td>
<td><span data-ttu-id="7a4ca-119"><strong>REG_MULTI_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="7a4ca-119"><strong>REG_MULTI_SZ</strong></span></span></td>
<td><span data-ttu-id="7a4ca-120">Especifica un conjunto de intervalos de puertos IP que consta de todos los puertos disponibles en Internet o de todos los puertos que no están disponibles en Internet.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-120">Specifies a set of IP port ranges consisting of either all the ports available from the Internet or all the ports not available from the Internet.</span></span> <span data-ttu-id="7a4ca-121">Cada cadena representa un único puerto o un conjunto inclusivo de puertos (por ejemplo, 1000-1050, 1984).</span><span class="sxs-lookup"><span data-stu-id="7a4ca-121">Each string represents a single port or an inclusive set of ports (for example,1000-1050, 1984).</span></span> <span data-ttu-id="7a4ca-122">Si alguna entrada está fuera del intervalo comprendido entre 0 y 65535, o si no se puede interpretar una cadena, el tiempo de ejecución de RPC tratará toda la configuración como no válida.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-122">If any entries are outside the range 0 to 65535, or if any string cannot be interpreted, the RPC run time will treat the entire configuration as invalid.</span></span></td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               PortsInternetAvailable</code></pre></td>
<td><span data-ttu-id="7a4ca-123"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="7a4ca-123"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="7a4ca-124">Y o N (no distingue entre mayúsculas y minúsculas).</span><span class="sxs-lookup"><span data-stu-id="7a4ca-124">Y or N (not case-sensitive).</span></span> <span data-ttu-id="7a4ca-125">Si es Y, los puertos enumerados en la clave puertos son todos los puertos disponibles en Internet de ese equipo.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-125">If Y, the ports listed in the Ports key are all the Internet-available ports on that computer.</span></span> <span data-ttu-id="7a4ca-126">Si es N, los puertos enumerados en la clave de puertos son todos los puertos que no están disponibles en Internet.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-126">If N, the ports listed in the Ports key are all those ports that are not Internet-available.</span></span></td>
</tr>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               UseInternetPorts</code></pre></td>
<td><span data-ttu-id="7a4ca-127"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="7a4ca-127"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="7a4ca-128">Y o N (no distingue entre mayúsculas y minúsculas).</span><span class="sxs-lookup"><span data-stu-id="7a4ca-128">Y or N (not case-sensitive).</span></span> <span data-ttu-id="7a4ca-129">Especifica la directiva predeterminada del sistema.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-129">Specifies the system default policy.</span></span> <span data-ttu-id="7a4ca-130">Si es Y, los procesos que usan el valor predeterminado serán puertos asignados del conjunto de puertos disponibles para Internet, tal como se ha definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-130">If Y, the processes using the default will be assigned ports from the set of Internet-available ports, as defined above.</span></span> <span data-ttu-id="7a4ca-131">Si es N, los procesos que usan el valor predeterminado serán puertos asignados del conjunto de puertos solo de la intranet.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-131">If N, processes using the default will be assigned ports from the set of intranet-only ports.</span></span></td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rpc
               Linkage
                  Bind</code></pre></td>
<td><span data-ttu-id="7a4ca-132"><strong>REG_MULTI_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="7a4ca-132"><strong>REG_MULTI_SZ</strong></span></span></td>
<td><span data-ttu-id="7a4ca-133">Enumera los nombres de los dispositivos de todas las NIC en las que se va a enlazar de forma predeterminada (por ejemplo, \Device\AMDPCN1).</span><span class="sxs-lookup"><span data-stu-id="7a4ca-133">Lists the device names of all the NICs on which to bind by default (for example, \Device\AMDPCN1).</span></span> <span data-ttu-id="7a4ca-134">Si la clave no existe, el servidor se enlazará a todas las NIC.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-134">If the key does not exist, the server will bind to all NICs.</span></span> <span data-ttu-id="7a4ca-135">Si la clave existe, el servidor se enlazará a las NIC especificadas en la clave, a menos que el campo NICFlags se establezca en RPC_C_BIND_TO_ALL_NICS.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-135">If the key does exist, the server will bind to the NICs specified in the key, unless the NICFlags field is set to RPC_C_BIND_TO_ALL_NICS.</span></span> <span data-ttu-id="7a4ca-136">Si la clave tiene un valor null ( &quot; &quot; ), la configuración se marcará como no válida y se producirá un error en todas las llamadas a <strong>RpcServerUseProtseq \*</strong> en <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong>ncacn_ip_tcp</strong></a> o <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7a4ca-136">If the key has a null (&quot;&quot;) value, the configuration will be marked as invalid and all calls to <strong>RpcServerUseProtseq\*</strong> over <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong>ncacn_ip_tcp</strong></a> or <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a> will fail.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7a4ca-137">En la tabla siguiente se muestra cómo las tres aplicaciones de ejemplo se ven afectadas por la configuración definida en la tabla anterior, y cómo también se ven afectadas las Configuraciones aplicadas mediante la función [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .</span><span class="sxs-lookup"><span data-stu-id="7a4ca-137">The following table illustrates how three sample applications are affected by the settings defined in the previous table, and how settings applied using the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function are also affected.</span></span>

<span data-ttu-id="7a4ca-138">En este ejemplo, se consideran tres aplicaciones hipotéticas:</span><span class="sxs-lookup"><span data-stu-id="7a4ca-138">In this example, three hypothetical applications are considered:</span></span>

-   <span data-ttu-id="7a4ca-139">Internetapp: esta aplicación está diseñada para su exposición a Internet y ha especificado el puerto de Internet de RPC \_ C \_ \_ \_ en el miembro **EndpointFlags** de la estructura de la [**\_ Directiva RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) pasada a la función [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .</span><span class="sxs-lookup"><span data-stu-id="7a4ca-139">InternetApp: This application is intended for exposure to the Internet, and has specified RPC\_C\_USE\_INTERNET\_PORT in the **EndpointFlags** member of the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure passed to the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function.</span></span>
-   <span data-ttu-id="7a4ca-140">LocalApp: esta aplicación no está pensada para su exposición a Internet y ha especificado RPC \_ C \_ use \_ el \_ Puerto de la intranet en el miembro **EndpointFlags** de la estructura de la [**\_ Directiva RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) pasada a la función [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .</span><span class="sxs-lookup"><span data-stu-id="7a4ca-140">LocalApp: This application is not intended for exposure to the Internet, and has specified RPC\_C\_USE\_INTRANET\_PORT in the **EndpointFlags** member of the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure passed to the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function.</span></span>
-   <span data-ttu-id="7a4ca-141">DefaultApp: esta aplicación especifica cero en el miembro **EndpointFlags** de la estructura de la [**\_ Directiva RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) pasada a la función [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .</span><span class="sxs-lookup"><span data-stu-id="7a4ca-141">DefaultApp: This application specifies zero in the **EndpointFlags** member of the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure passed to the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function.</span></span>

<span data-ttu-id="7a4ca-142">En la tabla siguiente se explica el impacto que estas opciones tienen en función de los valores especificados en las entradas del registro explicadas en la tabla anterior.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-142">The following table explains the impact these settings have based on values specified in the registry entries explained in the previous table.</span></span> <span data-ttu-id="7a4ca-143">En el caso de las consideraciones de formato, se asignan los siguientes códigos:</span><span class="sxs-lookup"><span data-stu-id="7a4ca-143">For formatting considerations, the following codes are assigned:</span></span>

<span data-ttu-id="7a4ca-144">PIA = valor de clave PortsInternetAvailable</span><span class="sxs-lookup"><span data-stu-id="7a4ca-144">PIA = PortsInternetAvailable Key value</span></span>

<span data-ttu-id="7a4ca-145">UIP = valor de clave UseInternetPorts</span><span class="sxs-lookup"><span data-stu-id="7a4ca-145">UIP = UseInternetPorts Key value</span></span>

<span data-ttu-id="7a4ca-146">En este ejemplo, el valor de la clave ports es 5000-5100 para cada entrada.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-146">The value of the Ports key, for sake of this example, is 5000-5100 for each entry.</span></span>



| <span data-ttu-id="7a4ca-147">Application</span><span class="sxs-lookup"><span data-stu-id="7a4ca-147">Application</span></span> | <span data-ttu-id="7a4ca-148">PIA</span><span class="sxs-lookup"><span data-stu-id="7a4ca-148">PIA</span></span> | <span data-ttu-id="7a4ca-149">UIP</span><span class="sxs-lookup"><span data-stu-id="7a4ca-149">UIP</span></span> | <span data-ttu-id="7a4ca-150">Resultado</span><span class="sxs-lookup"><span data-stu-id="7a4ca-150">Result</span></span>                                  |
|-------------|-----|-----|-----------------------------------------|
| <span data-ttu-id="7a4ca-151">Entre netApp</span><span class="sxs-lookup"><span data-stu-id="7a4ca-151">InternetApp</span></span> | <span data-ttu-id="7a4ca-152">Y</span><span class="sxs-lookup"><span data-stu-id="7a4ca-152">Y</span></span>   | <span data-ttu-id="7a4ca-153">Y</span><span class="sxs-lookup"><span data-stu-id="7a4ca-153">Y</span></span>   | <span data-ttu-id="7a4ca-154">Usa puertos entre 5000 y 5100</span><span class="sxs-lookup"><span data-stu-id="7a4ca-154">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="7a4ca-155">LocalApp</span><span class="sxs-lookup"><span data-stu-id="7a4ca-155">LocalApp</span></span>    | <span data-ttu-id="7a4ca-156">Y</span><span class="sxs-lookup"><span data-stu-id="7a4ca-156">Y</span></span>   | <span data-ttu-id="7a4ca-157">Y</span><span class="sxs-lookup"><span data-stu-id="7a4ca-157">Y</span></span>   | <span data-ttu-id="7a4ca-158">Usa un puerto fuera del intervalo de 5000-5100</span><span class="sxs-lookup"><span data-stu-id="7a4ca-158">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="7a4ca-159">DefaultApp</span><span class="sxs-lookup"><span data-stu-id="7a4ca-159">DefaultApp</span></span>  | <span data-ttu-id="7a4ca-160">Y</span><span class="sxs-lookup"><span data-stu-id="7a4ca-160">Y</span></span>   | <span data-ttu-id="7a4ca-161">Y</span><span class="sxs-lookup"><span data-stu-id="7a4ca-161">Y</span></span>   | <span data-ttu-id="7a4ca-162">Usa puertos entre 5000 y 5100</span><span class="sxs-lookup"><span data-stu-id="7a4ca-162">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="7a4ca-163">Entre netApp</span><span class="sxs-lookup"><span data-stu-id="7a4ca-163">InternetApp</span></span> | <span data-ttu-id="7a4ca-164">Y</span><span class="sxs-lookup"><span data-stu-id="7a4ca-164">Y</span></span>   | <span data-ttu-id="7a4ca-165">N</span><span class="sxs-lookup"><span data-stu-id="7a4ca-165">N</span></span>   | <span data-ttu-id="7a4ca-166">Usa puertos entre 5000 y 5100</span><span class="sxs-lookup"><span data-stu-id="7a4ca-166">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="7a4ca-167">LocalApp</span><span class="sxs-lookup"><span data-stu-id="7a4ca-167">LocalApp</span></span>    | <span data-ttu-id="7a4ca-168">Y</span><span class="sxs-lookup"><span data-stu-id="7a4ca-168">Y</span></span>   | <span data-ttu-id="7a4ca-169">N</span><span class="sxs-lookup"><span data-stu-id="7a4ca-169">N</span></span>   | <span data-ttu-id="7a4ca-170">Usa un puerto fuera del intervalo de 5000-5100</span><span class="sxs-lookup"><span data-stu-id="7a4ca-170">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="7a4ca-171">DefaultApp</span><span class="sxs-lookup"><span data-stu-id="7a4ca-171">DefaultApp</span></span>  | <span data-ttu-id="7a4ca-172">Y</span><span class="sxs-lookup"><span data-stu-id="7a4ca-172">Y</span></span>   | <span data-ttu-id="7a4ca-173">N</span><span class="sxs-lookup"><span data-stu-id="7a4ca-173">N</span></span>   | <span data-ttu-id="7a4ca-174">Usa un puerto fuera del intervalo de 5000-5100</span><span class="sxs-lookup"><span data-stu-id="7a4ca-174">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="7a4ca-175">Entre netApp</span><span class="sxs-lookup"><span data-stu-id="7a4ca-175">InternetApp</span></span> | <span data-ttu-id="7a4ca-176">N</span><span class="sxs-lookup"><span data-stu-id="7a4ca-176">N</span></span>   | <span data-ttu-id="7a4ca-177">Y</span><span class="sxs-lookup"><span data-stu-id="7a4ca-177">Y</span></span>   | <span data-ttu-id="7a4ca-178">Usa un puerto fuera del intervalo de 5000-5100</span><span class="sxs-lookup"><span data-stu-id="7a4ca-178">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="7a4ca-179">LocalApp</span><span class="sxs-lookup"><span data-stu-id="7a4ca-179">LocalApp</span></span>    | <span data-ttu-id="7a4ca-180">N</span><span class="sxs-lookup"><span data-stu-id="7a4ca-180">N</span></span>   | <span data-ttu-id="7a4ca-181">Y</span><span class="sxs-lookup"><span data-stu-id="7a4ca-181">Y</span></span>   | <span data-ttu-id="7a4ca-182">Usa puertos entre 5000 y 5100</span><span class="sxs-lookup"><span data-stu-id="7a4ca-182">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="7a4ca-183">DefaultApp</span><span class="sxs-lookup"><span data-stu-id="7a4ca-183">DefaultApp</span></span>  | <span data-ttu-id="7a4ca-184">N</span><span class="sxs-lookup"><span data-stu-id="7a4ca-184">N</span></span>   | <span data-ttu-id="7a4ca-185">Y</span><span class="sxs-lookup"><span data-stu-id="7a4ca-185">Y</span></span>   | <span data-ttu-id="7a4ca-186">Usa un puerto fuera del intervalo de 5000-5100</span><span class="sxs-lookup"><span data-stu-id="7a4ca-186">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="7a4ca-187">Entre netApp</span><span class="sxs-lookup"><span data-stu-id="7a4ca-187">InternetApp</span></span> | <span data-ttu-id="7a4ca-188">N</span><span class="sxs-lookup"><span data-stu-id="7a4ca-188">N</span></span>   | <span data-ttu-id="7a4ca-189">N</span><span class="sxs-lookup"><span data-stu-id="7a4ca-189">N</span></span>   | <span data-ttu-id="7a4ca-190">Usa un puerto fuera del intervalo de 5000-5100</span><span class="sxs-lookup"><span data-stu-id="7a4ca-190">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="7a4ca-191">LocalApp</span><span class="sxs-lookup"><span data-stu-id="7a4ca-191">LocalApp</span></span>    | <span data-ttu-id="7a4ca-192">N</span><span class="sxs-lookup"><span data-stu-id="7a4ca-192">N</span></span>   | <span data-ttu-id="7a4ca-193">N</span><span class="sxs-lookup"><span data-stu-id="7a4ca-193">N</span></span>   | <span data-ttu-id="7a4ca-194">Usa puertos entre 5000 y 5100</span><span class="sxs-lookup"><span data-stu-id="7a4ca-194">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="7a4ca-195">DefaultApp</span><span class="sxs-lookup"><span data-stu-id="7a4ca-195">DefaultApp</span></span>  | <span data-ttu-id="7a4ca-196">N</span><span class="sxs-lookup"><span data-stu-id="7a4ca-196">N</span></span>   | <span data-ttu-id="7a4ca-197">N</span><span class="sxs-lookup"><span data-stu-id="7a4ca-197">N</span></span>   | <span data-ttu-id="7a4ca-198">Usa puertos entre 5000 y 5100</span><span class="sxs-lookup"><span data-stu-id="7a4ca-198">Uses ports between 5000 and 5100</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7a4ca-199">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7a4ca-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a4ca-200">**\_Directiva RPC**</span><span class="sxs-lookup"><span data-stu-id="7a4ca-200">**RPC\_POLICY**</span></span>](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)
</dt> <dt>

[<span data-ttu-id="7a4ca-201">**RpcServerUseAllProtseqsEx**</span><span class="sxs-lookup"><span data-stu-id="7a4ca-201">**RpcServerUseAllProtseqsEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex)
</dt> <dt>

[<span data-ttu-id="7a4ca-202">**RpcServerUseAllProtseqsIfEx**</span><span class="sxs-lookup"><span data-stu-id="7a4ca-202">**RpcServerUseAllProtseqsIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex)
</dt> <dt>

[<span data-ttu-id="7a4ca-203">**RpcServerUseProtseqEx**</span><span class="sxs-lookup"><span data-stu-id="7a4ca-203">**RpcServerUseProtseqEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)
</dt> <dt>

[<span data-ttu-id="7a4ca-204">**RpcServerUseProtseqEpEx**</span><span class="sxs-lookup"><span data-stu-id="7a4ca-204">**RpcServerUseProtseqEpEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)
</dt> <dt>

[<span data-ttu-id="7a4ca-205">**RpcServerUseProtseqIfEx**</span><span class="sxs-lookup"><span data-stu-id="7a4ca-205">**RpcServerUseProtseqIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqifex)
</dt> <dt>

[<span data-ttu-id="7a4ca-206">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="7a4ca-206">**ncacn\_ip\_tcp**</span></span>](/windows/desktop/Midl/ncacn-ip-tcp)
</dt> <dt>

[<span data-ttu-id="7a4ca-207">**ncadg \_ IP \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="7a4ca-207">**ncadg\_ip\_udp**</span></span>](/windows/desktop/Midl/ncadg-ip-udp)
</dt> </dl>

 

 