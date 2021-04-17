---
description: La \_ clase ServerFeature de Win32 representa las características instaladas en un equipo que ejecuta Windows Server.
ms.assetid: fe3bb95c-7f69-47b5-9c3d-771cdc3ed9ca
ms.tgt_platform: multiple
title: Clase Win32_ServerFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ServerFeature
- Win32_ServerFeature.ID
- Win32_ServerFeature.ParentID
- Win32_ServerFeature.Name
api_type:
- DllExport
api_location:
- ServerCompProv.dll
ms.openlocfilehash: 1be8a2ea1d646e9d882febc7c8eba08b69bb69f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707206"
---
# <a name="win32_serverfeature-class"></a><span data-ttu-id="9eeeb-103">\_Clase Win32 ServerFeature</span><span class="sxs-lookup"><span data-stu-id="9eeeb-103">Win32\_ServerFeature class</span></span>

<span data-ttu-id="9eeeb-104">\[La **clase \_ ServerFeature de Win32** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="9eeeb-104">\[The **Win32\_ServerFeature** class is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9eeeb-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="9eeeb-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="9eeeb-106">En su lugar, use las [clases de proveedor de ServerManager deploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment).\]</span><span class="sxs-lookup"><span data-stu-id="9eeeb-106">Instead, use the [ServerManager Deploymentprovider Provider Classes](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment).\]</span></span>

<span data-ttu-id="9eeeb-107">La **clase \_ ServerFeature de Win32** representa las características instaladas en un equipo que ejecuta Windows Server.</span><span class="sxs-lookup"><span data-stu-id="9eeeb-107">The **Win32\_ServerFeature** class represents the features installed on a computer running Windows Server.</span></span>

<span data-ttu-id="9eeeb-108">Los desarrolladores y administradores que necesitan automatizar el proceso de determinación de las características instaladas en un conjunto de equipos servidor pueden utilizar esta clase.</span><span class="sxs-lookup"><span data-stu-id="9eeeb-108">This class can be used by developers and administrators who need to automate the process of determining the features installed on a set of server computers.</span></span> <span data-ttu-id="9eeeb-109">Las instancias de esta clase no están disponibles en los equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="9eeeb-109">Instances of this class are not available on client computers.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eeeb-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9eeeb-110">Syntax</span></span>

``` syntax
[Deprecated("No value"), Dynamic, Provider("ServerFeatureProvider"), AMENDMENT]
class Win32_ServerFeature
{
  uint32 ID;
  uint32 ParentID;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="9eeeb-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="9eeeb-111">Members</span></span>

<span data-ttu-id="9eeeb-112">La **clase \_ ServerFeature de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9eeeb-112">The **Win32\_ServerFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="9eeeb-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9eeeb-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9eeeb-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9eeeb-114">Properties</span></span>

<span data-ttu-id="9eeeb-115">La **clase \_ ServerFeature de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9eeeb-115">The **Win32\_ServerFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9eeeb-116">**Id**</span><span class="sxs-lookup"><span data-stu-id="9eeeb-116">**ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eeeb-117">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9eeeb-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9eeeb-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9eeeb-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9eeeb-119">Calificadores: [**clave**](key-qualifier.md), [**no \_ null**](optional-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-119">Qualifiers: [**Key**](key-qualifier.md), [**Not\_Null**](optional-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="9eeeb-120">IDENTIFICADOR de la característica de servidor.</span><span class="sxs-lookup"><span data-stu-id="9eeeb-120">Server feature ID.</span></span> <span data-ttu-id="9eeeb-121">En la lista siguiente se muestran los posibles valores de la propiedad ID:</span><span class="sxs-lookup"><span data-stu-id="9eeeb-121">The following list shows the possible values of the ID property:</span></span>



<span data-ttu-id="9eeeb-122">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-122">Value</span></span>

<span data-ttu-id="9eeeb-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-123">Name</span></span>

<span data-ttu-id="9eeeb-124">1</span><span class="sxs-lookup"><span data-stu-id="9eeeb-124">1</span></span>

[<span data-ttu-id="9eeeb-125">Servidor de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="9eeeb-125">Application Server</span></span>](/windows)

<span data-ttu-id="9eeeb-126">2</span><span class="sxs-lookup"><span data-stu-id="9eeeb-126">2</span></span>

<span data-ttu-id="9eeeb-127">Servidor web (IIS)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-127">Web Server (IIS)</span></span>

<span data-ttu-id="9eeeb-128">3</span><span class="sxs-lookup"><span data-stu-id="9eeeb-128">3</span></span>

[<span data-ttu-id="9eeeb-129">Servicios de multimedia de transmisión por secuencias</span><span class="sxs-lookup"><span data-stu-id="9eeeb-129">Streaming Media Services</span></span>](/windows)

<span data-ttu-id="9eeeb-130">5</span><span class="sxs-lookup"><span data-stu-id="9eeeb-130">5</span></span>

<span data-ttu-id="9eeeb-131">Servidor de fax</span><span class="sxs-lookup"><span data-stu-id="9eeeb-131">Fax Server</span></span>

<span data-ttu-id="9eeeb-132">6</span><span class="sxs-lookup"><span data-stu-id="9eeeb-132">6</span></span>

<span data-ttu-id="9eeeb-133">Servicios de iSCSI y archivo</span><span class="sxs-lookup"><span data-stu-id="9eeeb-133">File and iSCSI Services</span></span><br/> [<span data-ttu-id="9eeeb-134">cambio de nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-134">name change</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-135">7</span><span class="sxs-lookup"><span data-stu-id="9eeeb-135">7</span></span>

<span data-ttu-id="9eeeb-136">Servicios de impresión y documentos</span><span class="sxs-lookup"><span data-stu-id="9eeeb-136">Print and Document Services</span></span><br/> [<span data-ttu-id="9eeeb-137">cambio de nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-137">name change</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-138">8</span><span class="sxs-lookup"><span data-stu-id="9eeeb-138">8</span></span>

[<span data-ttu-id="9eeeb-139">Servicios de federación de Active Directory (AD FS)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-139">Active Directory Federation Services</span></span>](/windows)

<span data-ttu-id="9eeeb-140">9</span><span class="sxs-lookup"><span data-stu-id="9eeeb-140">9</span></span>

<span data-ttu-id="9eeeb-141">Active Directory Lightweight Directory Services</span><span class="sxs-lookup"><span data-stu-id="9eeeb-141">Active Directory Lightweight Directory Services</span></span>

<span data-ttu-id="9eeeb-142">10</span><span class="sxs-lookup"><span data-stu-id="9eeeb-142">10</span></span>

<span data-ttu-id="9eeeb-143">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="9eeeb-143">Active Directory Domain Services</span></span>

<span data-ttu-id="9eeeb-144">11</span><span class="sxs-lookup"><span data-stu-id="9eeeb-144">11</span></span>

[<span data-ttu-id="9eeeb-145">Servicios UDDI</span><span class="sxs-lookup"><span data-stu-id="9eeeb-145">UDDI Services</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-146">12</span><span class="sxs-lookup"><span data-stu-id="9eeeb-146">12</span></span>

[<span data-ttu-id="9eeeb-147">Servidor DHCP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-147">DHCP Server</span></span>](/windows)

<span data-ttu-id="9eeeb-148">13</span><span class="sxs-lookup"><span data-stu-id="9eeeb-148">13</span></span>

[<span data-ttu-id="9eeeb-149">Servidor DNS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-149">DNS Server</span></span>](/windows)

<span data-ttu-id="9eeeb-150">14</span><span class="sxs-lookup"><span data-stu-id="9eeeb-150">14</span></span>

<span data-ttu-id="9eeeb-151">Network Policy and Access Services</span><span class="sxs-lookup"><span data-stu-id="9eeeb-151">Network Policy and Access Services</span></span>

<span data-ttu-id="9eeeb-152">16</span><span class="sxs-lookup"><span data-stu-id="9eeeb-152">16</span></span>

<span data-ttu-id="9eeeb-153">Servicios de certificados de Active Directory</span><span class="sxs-lookup"><span data-stu-id="9eeeb-153">Active Directory Certificate Services</span></span>

<span data-ttu-id="9eeeb-154">17</span><span class="sxs-lookup"><span data-stu-id="9eeeb-154">17</span></span>

<span data-ttu-id="9eeeb-155">Active Directory Rights Management Services</span><span class="sxs-lookup"><span data-stu-id="9eeeb-155">Active Directory Rights Management Services</span></span>

<span data-ttu-id="9eeeb-156">18</span><span class="sxs-lookup"><span data-stu-id="9eeeb-156">18</span></span>

[<span data-ttu-id="9eeeb-157">Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-157">Remote Desktop Services</span></span>](/windows)<br/> [<span data-ttu-id="9eeeb-158">cambio de nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-158">name change</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-159">19</span><span class="sxs-lookup"><span data-stu-id="9eeeb-159">19</span></span>

<span data-ttu-id="9eeeb-160">Servicios de implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="9eeeb-160">Windows Deployment Services</span></span>

<span data-ttu-id="9eeeb-161">20</span><span class="sxs-lookup"><span data-stu-id="9eeeb-161">20</span></span>

<span data-ttu-id="9eeeb-162">Hyper-V</span><span class="sxs-lookup"><span data-stu-id="9eeeb-162">Hyper-V</span></span>

<span data-ttu-id="9eeeb-163">21</span><span class="sxs-lookup"><span data-stu-id="9eeeb-163">21</span></span>

[<span data-ttu-id="9eeeb-164">Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="9eeeb-164">Windows Server Update Services</span></span>](/windows)

<span data-ttu-id="9eeeb-165">33</span><span class="sxs-lookup"><span data-stu-id="9eeeb-165">33</span></span>

[<span data-ttu-id="9eeeb-166">Clúster de conmutación por error</span><span class="sxs-lookup"><span data-stu-id="9eeeb-166">Failover Clustering</span></span>](/windows)

<span data-ttu-id="9eeeb-167">34</span><span class="sxs-lookup"><span data-stu-id="9eeeb-167">34</span></span>

[<span data-ttu-id="9eeeb-168">Equilibrio de carga de red</span><span class="sxs-lookup"><span data-stu-id="9eeeb-168">Network Load Balancing</span></span>](/windows)

<span data-ttu-id="9eeeb-169">36</span><span class="sxs-lookup"><span data-stu-id="9eeeb-169">36</span></span>

[<span data-ttu-id="9eeeb-170">Características de .NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="9eeeb-170">.NET Framework 3.5.1 Features</span></span>](/windows)<br/> [<span data-ttu-id="9eeeb-171">cambio de nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-171">name change</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-172">37</span><span class="sxs-lookup"><span data-stu-id="9eeeb-172">37</span></span>

[<span data-ttu-id="9eeeb-173">Administrador de recursos del sistema de Windows</span><span class="sxs-lookup"><span data-stu-id="9eeeb-173">Windows System Resource Manager</span></span>](/windows)

<span data-ttu-id="9eeeb-174">38</span><span class="sxs-lookup"><span data-stu-id="9eeeb-174">38</span></span>

<span data-ttu-id="9eeeb-175">Servicio WLAN</span><span class="sxs-lookup"><span data-stu-id="9eeeb-175">Wireless LAN Service</span></span>

<span data-ttu-id="9eeeb-176">39</span><span class="sxs-lookup"><span data-stu-id="9eeeb-176">39</span></span>

[<span data-ttu-id="9eeeb-177">Copias de seguridad de Windows Server características</span><span class="sxs-lookup"><span data-stu-id="9eeeb-177">Windows Server Backup Features</span></span>](/windows)

<span data-ttu-id="9eeeb-178">40</span><span class="sxs-lookup"><span data-stu-id="9eeeb-178">40</span></span>

<span data-ttu-id="9eeeb-179">Servidor WINS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-179">WINS Server</span></span>

<span data-ttu-id="9eeeb-180">41</span><span class="sxs-lookup"><span data-stu-id="9eeeb-180">41</span></span>

<span data-ttu-id="9eeeb-181">Servicio de activación de procesos de Windows</span><span class="sxs-lookup"><span data-stu-id="9eeeb-181">Windows Process Activation Service</span></span>

<span data-ttu-id="9eeeb-182">42</span><span class="sxs-lookup"><span data-stu-id="9eeeb-182">42</span></span>

[<span data-ttu-id="9eeeb-183">Asistencia remota</span><span class="sxs-lookup"><span data-stu-id="9eeeb-183">Remote Assistance</span></span>](/windows)

<span data-ttu-id="9eeeb-184">43</span><span class="sxs-lookup"><span data-stu-id="9eeeb-184">43</span></span>

<span data-ttu-id="9eeeb-185">Servicios simples de TCP/IP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-185">Simple TCP/IP Services</span></span>

<span data-ttu-id="9eeeb-186">44</span><span class="sxs-lookup"><span data-stu-id="9eeeb-186">44</span></span>

[<span data-ttu-id="9eeeb-187">Cliente Telnet</span><span class="sxs-lookup"><span data-stu-id="9eeeb-187">Telnet Client</span></span>](/windows)

<span data-ttu-id="9eeeb-188">45</span><span class="sxs-lookup"><span data-stu-id="9eeeb-188">45</span></span>

[<span data-ttu-id="9eeeb-189">Servidor Telnet</span><span class="sxs-lookup"><span data-stu-id="9eeeb-189">Telnet Server</span></span>](/windows)

<span data-ttu-id="9eeeb-190">46</span><span class="sxs-lookup"><span data-stu-id="9eeeb-190">46</span></span>

[<span data-ttu-id="9eeeb-191">Subsystem for UNIX-Based Applications</span><span class="sxs-lookup"><span data-stu-id="9eeeb-191">Subsystem For Unix-based Applications</span></span>](/windows)

<span data-ttu-id="9eeeb-192">47</span><span class="sxs-lookup"><span data-stu-id="9eeeb-192">47</span></span>

<span data-ttu-id="9eeeb-193">P roxy RPC sobre HTTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-193">RPC Over HTTP Proxy</span></span>

<span data-ttu-id="9eeeb-194">48</span><span class="sxs-lookup"><span data-stu-id="9eeeb-194">48</span></span>

<span data-ttu-id="9eeeb-195">Servidor SMTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-195">SMTP Server</span></span>

<span data-ttu-id="9eeeb-196">49</span><span class="sxs-lookup"><span data-stu-id="9eeeb-196">49</span></span>

<span data-ttu-id="9eeeb-197">Message Queue Server</span><span class="sxs-lookup"><span data-stu-id="9eeeb-197">Message Queuing</span></span>

<span data-ttu-id="9eeeb-198">51</span><span class="sxs-lookup"><span data-stu-id="9eeeb-198">51</span></span>

[<span data-ttu-id="9eeeb-199">Windows Internal Database</span><span class="sxs-lookup"><span data-stu-id="9eeeb-199">Windows Internal Database</span></span>](/windows)

<span data-ttu-id="9eeeb-200">52</span><span class="sxs-lookup"><span data-stu-id="9eeeb-200">52</span></span>

[<span data-ttu-id="9eeeb-201">Administrador de almacenamiento para redes San</span><span class="sxs-lookup"><span data-stu-id="9eeeb-201">Storage Manager For SANs</span></span>](/windows)

<span data-ttu-id="9eeeb-202">53</span><span class="sxs-lookup"><span data-stu-id="9eeeb-202">53</span></span>

<span data-ttu-id="9eeeb-203">Monitor de puerto de LPR</span><span class="sxs-lookup"><span data-stu-id="9eeeb-203">LPR Port Monitor</span></span>

<span data-ttu-id="9eeeb-204">55</span><span class="sxs-lookup"><span data-stu-id="9eeeb-204">55</span></span>

[<span data-ttu-id="9eeeb-205">Servidor de nombres de almacenamiento de Internet</span><span class="sxs-lookup"><span data-stu-id="9eeeb-205">Internet Storage Name Server</span></span>](/windows)

<span data-ttu-id="9eeeb-206">57</span><span class="sxs-lookup"><span data-stu-id="9eeeb-206">57</span></span>

[<span data-ttu-id="9eeeb-207">E/s de múltiples rutas</span><span class="sxs-lookup"><span data-stu-id="9eeeb-207">Multipath I/O</span></span>](/windows)

<span data-ttu-id="9eeeb-208">58</span><span class="sxs-lookup"><span data-stu-id="9eeeb-208">58</span></span>

<span data-ttu-id="9eeeb-209">Cliente TFTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-209">TFTP Client</span></span>

<span data-ttu-id="9eeeb-210">59</span><span class="sxs-lookup"><span data-stu-id="9eeeb-210">59</span></span>

[<span data-ttu-id="9eeeb-211">Servicios SNMP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-211">SNMP Services</span></span>](/windows)

<span data-ttu-id="9eeeb-212">60</span><span class="sxs-lookup"><span data-stu-id="9eeeb-212">60</span></span>

[<span data-ttu-id="9eeeb-213">Administrador de almacenamiento extraíble</span><span class="sxs-lookup"><span data-stu-id="9eeeb-213">Removable Storage Manager</span></span>](/windows)

<span data-ttu-id="9eeeb-214">61</span><span class="sxs-lookup"><span data-stu-id="9eeeb-214">61</span></span>

<span data-ttu-id="9eeeb-215">Cifrado BitLocker de unidades</span><span class="sxs-lookup"><span data-stu-id="9eeeb-215">BitLocker Drive Encryption</span></span>

<span data-ttu-id="9eeeb-216">62</span><span class="sxs-lookup"><span data-stu-id="9eeeb-216">62</span></span>

[<span data-ttu-id="9eeeb-217">Servicios para Network File System</span><span class="sxs-lookup"><span data-stu-id="9eeeb-217">Services For Network File System</span></span>](/windows)

<span data-ttu-id="9eeeb-218">63</span><span class="sxs-lookup"><span data-stu-id="9eeeb-218">63</span></span>

<span data-ttu-id="9eeeb-219">Cliente de impresión en Internet</span><span class="sxs-lookup"><span data-stu-id="9eeeb-219">Internet Printing Client</span></span>

<span data-ttu-id="9eeeb-220">64</span><span class="sxs-lookup"><span data-stu-id="9eeeb-220">64</span></span>

[<span data-ttu-id="9eeeb-221">Protocolo de resolución de nombres del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="9eeeb-221">Peer Name Resolution Protocol</span></span>](/windows)

<span data-ttu-id="9eeeb-222">65</span><span class="sxs-lookup"><span data-stu-id="9eeeb-222">65</span></span>

<span data-ttu-id="9eeeb-223">Kit de administración de Connection Manager</span><span class="sxs-lookup"><span data-stu-id="9eeeb-223">Connection Manager Administration Kit</span></span>

<span data-ttu-id="9eeeb-224">66</span><span class="sxs-lookup"><span data-stu-id="9eeeb-224">66</span></span>

[<span data-ttu-id="9eeeb-225">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-225">Windows PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-226">67</span><span class="sxs-lookup"><span data-stu-id="9eeeb-226">67</span></span>

[<span data-ttu-id="9eeeb-227">Herramientas de administración remota del servidor</span><span class="sxs-lookup"><span data-stu-id="9eeeb-227">Remote Server Administration Tools</span></span>](/windows)

<span data-ttu-id="9eeeb-228">68</span><span class="sxs-lookup"><span data-stu-id="9eeeb-228">68</span></span>

[<span data-ttu-id="9eeeb-229">Experiencia de calidad de audio y vídeo de Windows (qWave)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-229">Quality Windows Audio Video Experience</span></span>](/windows)

<span data-ttu-id="9eeeb-230">69</span><span class="sxs-lookup"><span data-stu-id="9eeeb-230">69</span></span>

[<span data-ttu-id="9eeeb-231">Administración de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="9eeeb-231">Group Policy Management</span></span>](/windows)

<span data-ttu-id="9eeeb-232">71</span><span class="sxs-lookup"><span data-stu-id="9eeeb-232">71</span></span>

[<span data-ttu-id="9eeeb-233">Servicio de Index Server</span><span class="sxs-lookup"><span data-stu-id="9eeeb-233">Indexing Service</span></span>](/windows)

<span data-ttu-id="9eeeb-234">72</span><span class="sxs-lookup"><span data-stu-id="9eeeb-234">72</span></span>

[<span data-ttu-id="9eeeb-235">Administrador de recursos del servidor de archivos (FSRM)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-235">File Server Resource Manager (FSRM)</span></span>](/windows)

<span data-ttu-id="9eeeb-236">73</span><span class="sxs-lookup"><span data-stu-id="9eeeb-236">73</span></span>

<span data-ttu-id="9eeeb-237">Compresión diferencial remota</span><span class="sxs-lookup"><span data-stu-id="9eeeb-237">Remote Differential Compression</span></span>

<span data-ttu-id="9eeeb-238">310</span><span class="sxs-lookup"><span data-stu-id="9eeeb-238">310</span></span>

<span data-ttu-id="9eeeb-239">Servicios de Escritura con lápiz y Escritura a mano</span><span class="sxs-lookup"><span data-stu-id="9eeeb-239">Ink and Handwriting Services</span></span><br/>

<span data-ttu-id="9eeeb-240">320</span><span class="sxs-lookup"><span data-stu-id="9eeeb-240">320</span></span>

[<span data-ttu-id="9eeeb-241">Herramientas de migración de Windows Server</span><span class="sxs-lookup"><span data-stu-id="9eeeb-241">Windows Server Migration Tools</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-242">321</span><span class="sxs-lookup"><span data-stu-id="9eeeb-242">321</span></span>

[<span data-ttu-id="9eeeb-243">Extensión WinRM de IIS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-243">WinRM IIS Extension</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-244">324</span><span class="sxs-lookup"><span data-stu-id="9eeeb-244">324</span></span>

[<span data-ttu-id="9eeeb-245">BranchCache</span><span class="sxs-lookup"><span data-stu-id="9eeeb-245">BranchCache</span></span>](#branchcache)<br/>

<span data-ttu-id="9eeeb-246">334</span><span class="sxs-lookup"><span data-stu-id="9eeeb-246">334</span></span>

[<span data-ttu-id="9eeeb-247">Consola de administración de DirectAccess</span><span class="sxs-lookup"><span data-stu-id="9eeeb-247">DirectAccess Management Console</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-248">335</span><span class="sxs-lookup"><span data-stu-id="9eeeb-248">335</span></span>

[<span data-ttu-id="9eeeb-249">Servicio de transferencia inteligente en segundo plano (BITS)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-249">Background Intelligent Transfer Service (BITS)</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-250">338</span><span class="sxs-lookup"><span data-stu-id="9eeeb-250">338</span></span>

[<span data-ttu-id="9eeeb-251">Visor de XPS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-251">XPS Viewer</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-252">339</span><span class="sxs-lookup"><span data-stu-id="9eeeb-252">339</span></span>

[<span data-ttu-id="9eeeb-253">Marco biométrico de Windows</span><span class="sxs-lookup"><span data-stu-id="9eeeb-253">Windows Biometric Framework</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-254">340</span><span class="sxs-lookup"><span data-stu-id="9eeeb-254">340</span></span>

<span data-ttu-id="9eeeb-255">Compatibilidad con WoW64</span><span class="sxs-lookup"><span data-stu-id="9eeeb-255">WoW64 Support</span></span><br/>

<span data-ttu-id="9eeeb-256">351</span><span class="sxs-lookup"><span data-stu-id="9eeeb-256">351</span></span>

[<span data-ttu-id="9eeeb-257">Entorno de scripting integrado (ISE) de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-257">Windows PowerShell Integrated Scripting Environment (ISE)</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-258">352</span><span class="sxs-lookup"><span data-stu-id="9eeeb-258">352</span></span>

<span data-ttu-id="9eeeb-259">Windows TIFF IFilter</span><span class="sxs-lookup"><span data-stu-id="9eeeb-259">Windows TIFF IFilter</span></span><br/>

<span data-ttu-id="9eeeb-260">404</span><span class="sxs-lookup"><span data-stu-id="9eeeb-260">404</span></span>

[<span data-ttu-id="9eeeb-261">Servicios de actualización de Windows Server</span><span class="sxs-lookup"><span data-stu-id="9eeeb-261">Window Server Update Services</span></span>](/windows)

<span data-ttu-id="9eeeb-262">409</span><span class="sxs-lookup"><span data-stu-id="9eeeb-262">409</span></span>

[<span data-ttu-id="9eeeb-263">Servidor de Administración de direcciones IP (IPAM)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-263">IP Address Management (IPAM) Server</span></span>](/windows)

<span data-ttu-id="9eeeb-264">417</span><span class="sxs-lookup"><span data-stu-id="9eeeb-264">417</span></span>

[<span data-ttu-id="9eeeb-265">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-265">Windows PowerShell</span></span>](/windows)

<span data-ttu-id="9eeeb-266">418</span><span class="sxs-lookup"><span data-stu-id="9eeeb-266">418</span></span>

[<span data-ttu-id="9eeeb-267">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="9eeeb-267">.NET Framework 4.5</span></span>](/windows)

<span data-ttu-id="9eeeb-268">432</span><span class="sxs-lookup"><span data-stu-id="9eeeb-268">432</span></span>

[<span data-ttu-id="9eeeb-269">Servicio de Windows Search</span><span class="sxs-lookup"><span data-stu-id="9eeeb-269">Windows Search Service</span></span>](/windows)

<span data-ttu-id="9eeeb-270">438</span><span class="sxs-lookup"><span data-stu-id="9eeeb-270">438</span></span>

[<span data-ttu-id="9eeeb-271">Cliente para NFS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-271">Client for NFS</span></span>](/windows)

<span data-ttu-id="9eeeb-272">441</span><span class="sxs-lookup"><span data-stu-id="9eeeb-272">441</span></span>

[<span data-ttu-id="9eeeb-273">Desbloqueo de BitLocker en red</span><span class="sxs-lookup"><span data-stu-id="9eeeb-273">BitLocker Network Unlock</span></span>](/windows)

<span data-ttu-id="9eeeb-274">442</span><span class="sxs-lookup"><span data-stu-id="9eeeb-274">442</span></span>

[<span data-ttu-id="9eeeb-275">Extensión IIS Management OData</span><span class="sxs-lookup"><span data-stu-id="9eeeb-275">Management OData IIS Extension</span></span>](/windows)

<span data-ttu-id="9eeeb-276">450</span><span class="sxs-lookup"><span data-stu-id="9eeeb-276">450</span></span>

[<span data-ttu-id="9eeeb-277">Servicios avanzados de .NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="9eeeb-277">.NET Framework 4.5 Advanced Services</span></span>](/windows)

<span data-ttu-id="9eeeb-278">466</span><span class="sxs-lookup"><span data-stu-id="9eeeb-278">466</span></span>

[<span data-ttu-id="9eeeb-279">Características de .NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="9eeeb-279">.NET Framework 4.5 Features</span></span>](/windows)

<span data-ttu-id="9eeeb-280">468</span><span class="sxs-lookup"><span data-stu-id="9eeeb-280">468</span></span>

[<span data-ttu-id="9eeeb-281">Acceso remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-281">Remote Access</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-282">477</span><span class="sxs-lookup"><span data-stu-id="9eeeb-282">477</span></span>

[<span data-ttu-id="9eeeb-283">Infraestructura e interfaces de usuario</span><span class="sxs-lookup"><span data-stu-id="9eeeb-283">User Interfaces and Infrastructure</span></span>](/windows)

<span data-ttu-id="9eeeb-284">478</span><span class="sxs-lookup"><span data-stu-id="9eeeb-284">478</span></span>

[<span data-ttu-id="9eeeb-285">Infraestructura y herramientas de administración de gráficos</span><span class="sxs-lookup"><span data-stu-id="9eeeb-285">Graphical Management Tools and Infrastructure</span></span>](/windows)

<span data-ttu-id="9eeeb-286">481</span><span class="sxs-lookup"><span data-stu-id="9eeeb-286">481</span></span>

[<span data-ttu-id="9eeeb-287">Servicios de archivos y almacenamiento</span><span class="sxs-lookup"><span data-stu-id="9eeeb-287">File and Storage Services</span></span>](/windows)

<span data-ttu-id="9eeeb-288">485</span><span class="sxs-lookup"><span data-stu-id="9eeeb-288">485</span></span>

[<span data-ttu-id="9eeeb-289">Experiencia con Windows Server Essentials</span><span class="sxs-lookup"><span data-stu-id="9eeeb-289">Windows Server Essentials Experience</span></span>](/windows)

<span data-ttu-id="9eeeb-290">488</span><span class="sxs-lookup"><span data-stu-id="9eeeb-290">488</span></span>

[<span data-ttu-id="9eeeb-291">DirectPlay</span><span class="sxs-lookup"><span data-stu-id="9eeeb-291">Direct Play</span></span>](/windows)

<span data-ttu-id="9eeeb-292">Servicios de archivo: servicios de rol (6)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-292">File Services - Role Services (6)</span></span>

<span data-ttu-id="9eeeb-293">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-293">Value</span></span>

<span data-ttu-id="9eeeb-294">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-294">Name</span></span>

<span data-ttu-id="9eeeb-295">100</span><span class="sxs-lookup"><span data-stu-id="9eeeb-295">100</span></span>

[<span data-ttu-id="9eeeb-296">Sistema de archivos distribuido</span><span class="sxs-lookup"><span data-stu-id="9eeeb-296">Distributed File System</span></span>](/windows)

<span data-ttu-id="9eeeb-297">101</span><span class="sxs-lookup"><span data-stu-id="9eeeb-297">101</span></span>

<span data-ttu-id="9eeeb-298">Espacio de nombres DFS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-298">DFS Namespace</span></span>

<span data-ttu-id="9eeeb-299">102</span><span class="sxs-lookup"><span data-stu-id="9eeeb-299">102</span></span>

<span data-ttu-id="9eeeb-300">Replicación DFS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-300">DFS Replication</span></span>

<span data-ttu-id="9eeeb-301">103</span><span class="sxs-lookup"><span data-stu-id="9eeeb-301">103</span></span>

[<span data-ttu-id="9eeeb-302">Servicio de replicación de archivos</span><span class="sxs-lookup"><span data-stu-id="9eeeb-302">File Replication Service</span></span>](/windows)

<span data-ttu-id="9eeeb-303">104</span><span class="sxs-lookup"><span data-stu-id="9eeeb-303">104</span></span>

[<span data-ttu-id="9eeeb-304">Administrador de recursos del servidor de archivos (FSRM)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-304">File Server Resource Manager (FSRM)</span></span>](/windows)

<span data-ttu-id="9eeeb-305">105</span><span class="sxs-lookup"><span data-stu-id="9eeeb-305">105</span></span>

[<span data-ttu-id="9eeeb-306">Servicios para Network File System</span><span class="sxs-lookup"><span data-stu-id="9eeeb-306">Services For Network File System</span></span>](/windows)

<span data-ttu-id="9eeeb-307">106</span><span class="sxs-lookup"><span data-stu-id="9eeeb-307">106</span></span>

[<span data-ttu-id="9eeeb-308">Almacenamiento de instancia única</span><span class="sxs-lookup"><span data-stu-id="9eeeb-308">Single Instance Storage</span></span>](/windows)

<span data-ttu-id="9eeeb-309">107</span><span class="sxs-lookup"><span data-stu-id="9eeeb-309">107</span></span>

[<span data-ttu-id="9eeeb-310">Servicio de Windows Search</span><span class="sxs-lookup"><span data-stu-id="9eeeb-310">Windows Search Service</span></span>](/windows)

<span data-ttu-id="9eeeb-311">108</span><span class="sxs-lookup"><span data-stu-id="9eeeb-311">108</span></span>

[<span data-ttu-id="9eeeb-312">Servicio de Index Server</span><span class="sxs-lookup"><span data-stu-id="9eeeb-312">Indexing Service</span></span>](/windows)

<span data-ttu-id="9eeeb-313">255</span><span class="sxs-lookup"><span data-stu-id="9eeeb-313">255</span></span>

<span data-ttu-id="9eeeb-314">Servidor de archivos</span><span class="sxs-lookup"><span data-stu-id="9eeeb-314">File Server</span></span>

<span data-ttu-id="9eeeb-315">350</span><span class="sxs-lookup"><span data-stu-id="9eeeb-315">350</span></span>

<span data-ttu-id="9eeeb-316">BranchCache para archivos de red</span><span class="sxs-lookup"><span data-stu-id="9eeeb-316">BranchCache for Network Files</span></span>

<span data-ttu-id="9eeeb-317">431</span><span class="sxs-lookup"><span data-stu-id="9eeeb-317">431</span></span>

[<span data-ttu-id="9eeeb-318">Servidor para NFS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-318">Server for NFS</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-319">434</span><span class="sxs-lookup"><span data-stu-id="9eeeb-319">434</span></span>

[<span data-ttu-id="9eeeb-320">Servicio del agente VSS del servidor de archivos</span><span class="sxs-lookup"><span data-stu-id="9eeeb-320">File Server VSS Agent Service</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-321">435</span><span class="sxs-lookup"><span data-stu-id="9eeeb-321">435</span></span>

[<span data-ttu-id="9eeeb-322">Servidor de destino iSCSI</span><span class="sxs-lookup"><span data-stu-id="9eeeb-322">iSCSI Target Server</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-323">436</span><span class="sxs-lookup"><span data-stu-id="9eeeb-323">436</span></span>

[<span data-ttu-id="9eeeb-324">Desduplicación de datos</span><span class="sxs-lookup"><span data-stu-id="9eeeb-324">Data Deduplication</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-325">437</span><span class="sxs-lookup"><span data-stu-id="9eeeb-325">437</span></span>

[<span data-ttu-id="9eeeb-326">Proveedor de almacenamiento del destino iSCSI (proveedores de hardware de VDS y VSS)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-326">iSCSI Target Storage Provider (VDS and VSS hardware providers)</span></span>](/windows)

<span data-ttu-id="9eeeb-327">486</span><span class="sxs-lookup"><span data-stu-id="9eeeb-327">486</span></span>

[<span data-ttu-id="9eeeb-328">Carpetas de trabajo</span><span class="sxs-lookup"><span data-stu-id="9eeeb-328">Work Folders</span></span>](/windows)

<span data-ttu-id="9eeeb-329">AD DS de servicios de rol (10)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-329">AD DS - Role Services (10)</span></span>

<span data-ttu-id="9eeeb-330">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-330">Value</span></span>

<span data-ttu-id="9eeeb-331">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-331">Name</span></span>

<span data-ttu-id="9eeeb-332">110</span><span class="sxs-lookup"><span data-stu-id="9eeeb-332">110</span></span>

[<span data-ttu-id="9eeeb-333">Controlador de dominio de Active Directory</span><span class="sxs-lookup"><span data-stu-id="9eeeb-333">Active Directory Domain Controller</span></span>](/windows)

<span data-ttu-id="9eeeb-334">111</span><span class="sxs-lookup"><span data-stu-id="9eeeb-334">111</span></span>

[<span data-ttu-id="9eeeb-335">Administración de identidades para UNIX</span><span class="sxs-lookup"><span data-stu-id="9eeeb-335">Identity Management For Unix</span></span>](/windows)

<span data-ttu-id="9eeeb-336">112</span><span class="sxs-lookup"><span data-stu-id="9eeeb-336">112</span></span>

[<span data-ttu-id="9eeeb-337">Servidor para servicios de información de red</span><span class="sxs-lookup"><span data-stu-id="9eeeb-337">Server For Network Information Services</span></span>](/windows)

<span data-ttu-id="9eeeb-338">113</span><span class="sxs-lookup"><span data-stu-id="9eeeb-338">113</span></span>

[<span data-ttu-id="9eeeb-339">Sincronización de contraseñas</span><span class="sxs-lookup"><span data-stu-id="9eeeb-339">Password Synchronization</span></span>](/windows)

<span data-ttu-id="9eeeb-340">294</span><span class="sxs-lookup"><span data-stu-id="9eeeb-340">294</span></span>

[<span data-ttu-id="9eeeb-341">Herramientas de administración remota del servidor</span><span class="sxs-lookup"><span data-stu-id="9eeeb-341">Remote Server Administration Tools</span></span>](/windows)

<span data-ttu-id="9eeeb-342">Streaming de multimedia: servicios de rol (3)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-342">Streaming Media - Role Services (3)</span></span>

<span data-ttu-id="9eeeb-343">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-343">Value</span></span>

<span data-ttu-id="9eeeb-344">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-344">Name</span></span>

<span data-ttu-id="9eeeb-345">120</span><span class="sxs-lookup"><span data-stu-id="9eeeb-345">120</span></span>

[<span data-ttu-id="9eeeb-346">Servidor de Windows Media</span><span class="sxs-lookup"><span data-stu-id="9eeeb-346">Windows Media Server</span></span>](/windows)

<span data-ttu-id="9eeeb-347">121</span><span class="sxs-lookup"><span data-stu-id="9eeeb-347">121</span></span>

[<span data-ttu-id="9eeeb-348">Administración basada en Web</span><span class="sxs-lookup"><span data-stu-id="9eeeb-348">Web-based Administration</span></span>](/windows)

<span data-ttu-id="9eeeb-349">122</span><span class="sxs-lookup"><span data-stu-id="9eeeb-349">122</span></span>

[<span data-ttu-id="9eeeb-350">Agente de registro</span><span class="sxs-lookup"><span data-stu-id="9eeeb-350">Logging Agent</span></span>](/windows)

<span data-ttu-id="9eeeb-351">ADFS-servicios de rol (8)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-351">ADFS - Role Services (8)</span></span>

<span data-ttu-id="9eeeb-352">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-352">Value</span></span>

<span data-ttu-id="9eeeb-353">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-353">Name</span></span>

<span data-ttu-id="9eeeb-354">125</span><span class="sxs-lookup"><span data-stu-id="9eeeb-354">125</span></span>

[<span data-ttu-id="9eeeb-355">Servicios de federación de Active Directory (AD FS)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-355">Active Directory Federation Services</span></span>](/windows)

<span data-ttu-id="9eeeb-356">126</span><span class="sxs-lookup"><span data-stu-id="9eeeb-356">126</span></span>

[<span data-ttu-id="9eeeb-357">Directiva de Servicio de federación</span><span class="sxs-lookup"><span data-stu-id="9eeeb-357">Federation Service Policy</span></span>](/windows)

<span data-ttu-id="9eeeb-358">127</span><span class="sxs-lookup"><span data-stu-id="9eeeb-358">127</span></span>

[<span data-ttu-id="9eeeb-359">Agentes web de AD FS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-359">AD FS Web Agents</span></span>](/windows)

<span data-ttu-id="9eeeb-360">128</span><span class="sxs-lookup"><span data-stu-id="9eeeb-360">128</span></span>

[<span data-ttu-id="9eeeb-361">Agente para notificaciones</span><span class="sxs-lookup"><span data-stu-id="9eeeb-361">Claims-aware Agent</span></span>](/windows)

<span data-ttu-id="9eeeb-362">129</span><span class="sxs-lookup"><span data-stu-id="9eeeb-362">129</span></span>

[<span data-ttu-id="9eeeb-363">Agente basado en tokens de Windows</span><span class="sxs-lookup"><span data-stu-id="9eeeb-363">Windows Token-based Agent</span></span>](/windows)

<span data-ttu-id="9eeeb-364">Servicios de Escritorio remoto de servicios de rol (18)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-364">Remote Desktop Services - Role Services (18)</span></span>

<span data-ttu-id="9eeeb-365">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-365">Value</span></span>

<span data-ttu-id="9eeeb-366">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-366">Name</span></span>

<span data-ttu-id="9eeeb-367">130</span><span class="sxs-lookup"><span data-stu-id="9eeeb-367">130</span></span>

<span data-ttu-id="9eeeb-368">Host de sesión de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-368">Remote Desktop Session Host</span></span><br/> [<span data-ttu-id="9eeeb-369">cambio de nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-369">name change</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-370">131</span><span class="sxs-lookup"><span data-stu-id="9eeeb-370">131</span></span>

[<span data-ttu-id="9eeeb-371">Administración de licencias de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-371">Remote Desktop Licensing</span></span>](/windows)<br/> [<span data-ttu-id="9eeeb-372">cambio de nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-372">name change</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-373">132</span><span class="sxs-lookup"><span data-stu-id="9eeeb-373">132</span></span>

<span data-ttu-id="9eeeb-374">Puerta de enlace de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-374">Remote Desktop Gateway</span></span><br/> [<span data-ttu-id="9eeeb-375">cambio de nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-375">name change</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-376">133</span><span class="sxs-lookup"><span data-stu-id="9eeeb-376">133</span></span>

<span data-ttu-id="9eeeb-377">Agente de conexión a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-377">Remote Desktop Connection Broker</span></span><br/> [<span data-ttu-id="9eeeb-378">cambio de nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-378">name change</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-379">134</span><span class="sxs-lookup"><span data-stu-id="9eeeb-379">134</span></span>

<span data-ttu-id="9eeeb-380">Acceso web de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="9eeeb-380">Remote Desktop Web Access</span></span><br/> [<span data-ttu-id="9eeeb-381">cambio de nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-381">name change</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-382">322</span><span class="sxs-lookup"><span data-stu-id="9eeeb-382">322</span></span>

<span data-ttu-id="9eeeb-383">Host de virtualización de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-383">Remote Desktop Virtualization Host</span></span><br/>

<span data-ttu-id="9eeeb-384">Host de virtualización de Escritorio remoto de los servicios de rol (322)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-384">Remote Desktop Virtualization Host - Role Services (322)</span></span>

<span data-ttu-id="9eeeb-385">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-385">Value</span></span>

<span data-ttu-id="9eeeb-386">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-386">Name</span></span>

<span data-ttu-id="9eeeb-387">325</span><span class="sxs-lookup"><span data-stu-id="9eeeb-387">325</span></span>

[<span data-ttu-id="9eeeb-388">Servicios principales</span><span class="sxs-lookup"><span data-stu-id="9eeeb-388">Core Services</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-389">327</span><span class="sxs-lookup"><span data-stu-id="9eeeb-389">327</span></span>

[<span data-ttu-id="9eeeb-390">Escritorio remoto de gráficos virtuales</span><span class="sxs-lookup"><span data-stu-id="9eeeb-390">Remote Desktop Virtual Graphics</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-391">Servicios de impresión y documentos de servicios de rol (7)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-391">Print and Document Services - Role Services (7)</span></span>

<span data-ttu-id="9eeeb-392">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-392">Value</span></span>

<span data-ttu-id="9eeeb-393">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-393">Name</span></span>

<span data-ttu-id="9eeeb-394">135</span><span class="sxs-lookup"><span data-stu-id="9eeeb-394">135</span></span>

<span data-ttu-id="9eeeb-395">Servidor de impresión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-395">Print Server</span></span>

<span data-ttu-id="9eeeb-396">136</span><span class="sxs-lookup"><span data-stu-id="9eeeb-396">136</span></span>

<span data-ttu-id="9eeeb-397">Impresión en Internet</span><span class="sxs-lookup"><span data-stu-id="9eeeb-397">Internet Printing</span></span>

<span data-ttu-id="9eeeb-398">137</span><span class="sxs-lookup"><span data-stu-id="9eeeb-398">137</span></span>

<span data-ttu-id="9eeeb-399">Servicio de impresión de LPD</span><span class="sxs-lookup"><span data-stu-id="9eeeb-399">LPD Print Service</span></span>

<span data-ttu-id="9eeeb-400">328</span><span class="sxs-lookup"><span data-stu-id="9eeeb-400">328</span></span>

[<span data-ttu-id="9eeeb-401">Servidor de digitalización distribuida</span><span class="sxs-lookup"><span data-stu-id="9eeeb-401">Distributed Scan Server</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-402">Servidor Web (IIS)-servicios de rol (2)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-402">Web Server (IIS) - Role Services (2)</span></span>

<span data-ttu-id="9eeeb-403">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-403">Value</span></span>

<span data-ttu-id="9eeeb-404">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-404">Name</span></span>

<span data-ttu-id="9eeeb-405">140</span><span class="sxs-lookup"><span data-stu-id="9eeeb-405">140</span></span>

<span data-ttu-id="9eeeb-406">Servidor Web</span><span class="sxs-lookup"><span data-stu-id="9eeeb-406">Web Server</span></span>

<span data-ttu-id="9eeeb-407">141</span><span class="sxs-lookup"><span data-stu-id="9eeeb-407">141</span></span>

<span data-ttu-id="9eeeb-408">Características HTTP comunes</span><span class="sxs-lookup"><span data-stu-id="9eeeb-408">Common HTTP Features</span></span>

<span data-ttu-id="9eeeb-409">142</span><span class="sxs-lookup"><span data-stu-id="9eeeb-409">142</span></span>

<span data-ttu-id="9eeeb-410">Contenido estático</span><span class="sxs-lookup"><span data-stu-id="9eeeb-410">Static Content</span></span>

<span data-ttu-id="9eeeb-411">143</span><span class="sxs-lookup"><span data-stu-id="9eeeb-411">143</span></span>

<span data-ttu-id="9eeeb-412">Documento predeterminado</span><span class="sxs-lookup"><span data-stu-id="9eeeb-412">Default Document</span></span>

<span data-ttu-id="9eeeb-413">144</span><span class="sxs-lookup"><span data-stu-id="9eeeb-413">144</span></span>

<span data-ttu-id="9eeeb-414">Examinar directorio</span><span class="sxs-lookup"><span data-stu-id="9eeeb-414">Directory Browse</span></span>

<span data-ttu-id="9eeeb-415">145</span><span class="sxs-lookup"><span data-stu-id="9eeeb-415">145</span></span>

<span data-ttu-id="9eeeb-416">Errores HTTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-416">HTTP Errors</span></span>

<span data-ttu-id="9eeeb-417">146</span><span class="sxs-lookup"><span data-stu-id="9eeeb-417">146</span></span>

<span data-ttu-id="9eeeb-418">Redireccionamiento HTTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-418">HTTP Redirection</span></span>

<span data-ttu-id="9eeeb-419">147</span><span class="sxs-lookup"><span data-stu-id="9eeeb-419">147</span></span>

<span data-ttu-id="9eeeb-420">Desarrollo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="9eeeb-420">Application Development</span></span>

<span data-ttu-id="9eeeb-421">148</span><span class="sxs-lookup"><span data-stu-id="9eeeb-421">148</span></span>

<span data-ttu-id="9eeeb-422">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="9eeeb-422">ASP.NET</span></span>

<span data-ttu-id="9eeeb-423">149</span><span class="sxs-lookup"><span data-stu-id="9eeeb-423">149</span></span>

<span data-ttu-id="9eeeb-424">Extensibilidad de .NET</span><span class="sxs-lookup"><span data-stu-id="9eeeb-424">.NET Extensibility</span></span>

<span data-ttu-id="9eeeb-425">150</span><span class="sxs-lookup"><span data-stu-id="9eeeb-425">150</span></span>

<span data-ttu-id="9eeeb-426">ASP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-426">ASP</span></span>

<span data-ttu-id="9eeeb-427">151</span><span class="sxs-lookup"><span data-stu-id="9eeeb-427">151</span></span>

<span data-ttu-id="9eeeb-428">CGI</span><span class="sxs-lookup"><span data-stu-id="9eeeb-428">CGI</span></span>

<span data-ttu-id="9eeeb-429">152</span><span class="sxs-lookup"><span data-stu-id="9eeeb-429">152</span></span>

<span data-ttu-id="9eeeb-430">Extensiones ISAPI</span><span class="sxs-lookup"><span data-stu-id="9eeeb-430">ISAPI Extensions</span></span>

<span data-ttu-id="9eeeb-431">153</span><span class="sxs-lookup"><span data-stu-id="9eeeb-431">153</span></span>

<span data-ttu-id="9eeeb-432">Filtros de ISAPI</span><span class="sxs-lookup"><span data-stu-id="9eeeb-432">ISAPI Filters</span></span>

<span data-ttu-id="9eeeb-433">154</span><span class="sxs-lookup"><span data-stu-id="9eeeb-433">154</span></span>

<span data-ttu-id="9eeeb-434">Inclusión del servidor (SSI)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-434">Server Side Includes</span></span>

<span data-ttu-id="9eeeb-435">155</span><span class="sxs-lookup"><span data-stu-id="9eeeb-435">155</span></span>

<span data-ttu-id="9eeeb-436">Mantenimiento y diagnóstico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-436">Health And Diagnostics</span></span>

<span data-ttu-id="9eeeb-437">156</span><span class="sxs-lookup"><span data-stu-id="9eeeb-437">156</span></span>

<span data-ttu-id="9eeeb-438">Registro HTTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-438">HTTP Logging</span></span>

<span data-ttu-id="9eeeb-439">157</span><span class="sxs-lookup"><span data-stu-id="9eeeb-439">157</span></span>

<span data-ttu-id="9eeeb-440">Herramientas de registro</span><span class="sxs-lookup"><span data-stu-id="9eeeb-440">Logging Tools</span></span>

<span data-ttu-id="9eeeb-441">158</span><span class="sxs-lookup"><span data-stu-id="9eeeb-441">158</span></span>

<span data-ttu-id="9eeeb-442">Monitor de solicitudes</span><span class="sxs-lookup"><span data-stu-id="9eeeb-442">Request Monitor</span></span>

<span data-ttu-id="9eeeb-443">159</span><span class="sxs-lookup"><span data-stu-id="9eeeb-443">159</span></span>

<span data-ttu-id="9eeeb-444">Seguimiento</span><span class="sxs-lookup"><span data-stu-id="9eeeb-444">Tracing</span></span>

<span data-ttu-id="9eeeb-445">160</span><span class="sxs-lookup"><span data-stu-id="9eeeb-445">160</span></span>

<span data-ttu-id="9eeeb-446">Registro personalizado</span><span class="sxs-lookup"><span data-stu-id="9eeeb-446">Custom Logging</span></span>

<span data-ttu-id="9eeeb-447">161</span><span class="sxs-lookup"><span data-stu-id="9eeeb-447">161</span></span>

<span data-ttu-id="9eeeb-448">Registro ODBC</span><span class="sxs-lookup"><span data-stu-id="9eeeb-448">ODBC Logging</span></span>

<span data-ttu-id="9eeeb-449">162</span><span class="sxs-lookup"><span data-stu-id="9eeeb-449">162</span></span>

<span data-ttu-id="9eeeb-450">Seguridad</span><span class="sxs-lookup"><span data-stu-id="9eeeb-450">Security</span></span>

<span data-ttu-id="9eeeb-451">163</span><span class="sxs-lookup"><span data-stu-id="9eeeb-451">163</span></span>

<span data-ttu-id="9eeeb-452">Autenticación básica</span><span class="sxs-lookup"><span data-stu-id="9eeeb-452">Basic Authentication</span></span>

<span data-ttu-id="9eeeb-453">164</span><span class="sxs-lookup"><span data-stu-id="9eeeb-453">164</span></span>

<span data-ttu-id="9eeeb-454">Autenticación de Windows</span><span class="sxs-lookup"><span data-stu-id="9eeeb-454">Windows Authentication</span></span>

<span data-ttu-id="9eeeb-455">165</span><span class="sxs-lookup"><span data-stu-id="9eeeb-455">165</span></span>

<span data-ttu-id="9eeeb-456">Autenticación implícita</span><span class="sxs-lookup"><span data-stu-id="9eeeb-456">Digest Authentication</span></span>

<span data-ttu-id="9eeeb-457">166</span><span class="sxs-lookup"><span data-stu-id="9eeeb-457">166</span></span>

<span data-ttu-id="9eeeb-458">Autenticación de asignaciones de certificados de clientes</span><span class="sxs-lookup"><span data-stu-id="9eeeb-458">Client Certificate Mapping Authentication</span></span>

<span data-ttu-id="9eeeb-459">167</span><span class="sxs-lookup"><span data-stu-id="9eeeb-459">167</span></span>

<span data-ttu-id="9eeeb-460">Autenticación de asignaciones de certificados de cliente IIS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-460">IIS Client Certificate Mapping Authentication</span></span>

<span data-ttu-id="9eeeb-461">168</span><span class="sxs-lookup"><span data-stu-id="9eeeb-461">168</span></span>

<span data-ttu-id="9eeeb-462">Autorización de URL</span><span class="sxs-lookup"><span data-stu-id="9eeeb-462">URL Authorization</span></span>

<span data-ttu-id="9eeeb-463">169</span><span class="sxs-lookup"><span data-stu-id="9eeeb-463">169</span></span>

<span data-ttu-id="9eeeb-464">Filtrado de solicitudes</span><span class="sxs-lookup"><span data-stu-id="9eeeb-464">Request Filtering</span></span>

<span data-ttu-id="9eeeb-465">170</span><span class="sxs-lookup"><span data-stu-id="9eeeb-465">170</span></span>

<span data-ttu-id="9eeeb-466">Restricciones de IP y dominio</span><span class="sxs-lookup"><span data-stu-id="9eeeb-466">IP And Domain Restrictions</span></span>

<span data-ttu-id="9eeeb-467">171</span><span class="sxs-lookup"><span data-stu-id="9eeeb-467">171</span></span>

<span data-ttu-id="9eeeb-468">Rendimiento</span><span class="sxs-lookup"><span data-stu-id="9eeeb-468">Performance</span></span>

<span data-ttu-id="9eeeb-469">172</span><span class="sxs-lookup"><span data-stu-id="9eeeb-469">172</span></span>

<span data-ttu-id="9eeeb-470">Compresión de contenido estático</span><span class="sxs-lookup"><span data-stu-id="9eeeb-470">Static Content Compression</span></span>

<span data-ttu-id="9eeeb-471">173</span><span class="sxs-lookup"><span data-stu-id="9eeeb-471">173</span></span>

<span data-ttu-id="9eeeb-472">compresión de contenido dinámico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-472">Dynamic Content Compression</span></span>

<span data-ttu-id="9eeeb-473">174</span><span class="sxs-lookup"><span data-stu-id="9eeeb-473">174</span></span>

<span data-ttu-id="9eeeb-474">Herramientas de administración</span><span class="sxs-lookup"><span data-stu-id="9eeeb-474">Management Tools</span></span>

<span data-ttu-id="9eeeb-475">175</span><span class="sxs-lookup"><span data-stu-id="9eeeb-475">175</span></span>

<span data-ttu-id="9eeeb-476">Consola de administración de IIS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-476">IIS Management Console</span></span>

<span data-ttu-id="9eeeb-477">176</span><span class="sxs-lookup"><span data-stu-id="9eeeb-477">176</span></span>

<span data-ttu-id="9eeeb-478">Scripts y herramientas de administración de IIS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-478">IIS Management Scripts And Tools</span></span>

<span data-ttu-id="9eeeb-479">177</span><span class="sxs-lookup"><span data-stu-id="9eeeb-479">177</span></span>

<span data-ttu-id="9eeeb-480">Servicio de administración</span><span class="sxs-lookup"><span data-stu-id="9eeeb-480">Management Service</span></span>

<span data-ttu-id="9eeeb-481">178</span><span class="sxs-lookup"><span data-stu-id="9eeeb-481">178</span></span>

<span data-ttu-id="9eeeb-482">Compatibilidad con la administración de IIS 6</span><span class="sxs-lookup"><span data-stu-id="9eeeb-482">IIS 6 Management Compatibility</span></span>

<span data-ttu-id="9eeeb-483">179</span><span class="sxs-lookup"><span data-stu-id="9eeeb-483">179</span></span>

<span data-ttu-id="9eeeb-484">Compatibilidad con la metabase de IIS 6</span><span class="sxs-lookup"><span data-stu-id="9eeeb-484">IIS 6 Metabase Compatibility</span></span>

<span data-ttu-id="9eeeb-485">180</span><span class="sxs-lookup"><span data-stu-id="9eeeb-485">180</span></span>

<span data-ttu-id="9eeeb-486">Compatibilidad con WMI de IIS 6</span><span class="sxs-lookup"><span data-stu-id="9eeeb-486">IIS 6 WMI Compatibility</span></span>

<span data-ttu-id="9eeeb-487">181</span><span class="sxs-lookup"><span data-stu-id="9eeeb-487">181</span></span>

<span data-ttu-id="9eeeb-488">Herramientas de scripting de IIS 6</span><span class="sxs-lookup"><span data-stu-id="9eeeb-488">IIS 6 Scripting Tools</span></span>

<span data-ttu-id="9eeeb-489">182</span><span class="sxs-lookup"><span data-stu-id="9eeeb-489">182</span></span>

<span data-ttu-id="9eeeb-490">Consola de administración de IIS 6</span><span class="sxs-lookup"><span data-stu-id="9eeeb-490">IIS 6 Management Console</span></span>

<span data-ttu-id="9eeeb-491">183</span><span class="sxs-lookup"><span data-stu-id="9eeeb-491">183</span></span>

<span data-ttu-id="9eeeb-492">Servicio de publicación FTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-492">FTP Publishing Service</span></span><br/>

<span data-ttu-id="9eeeb-493">184</span><span class="sxs-lookup"><span data-stu-id="9eeeb-493">184</span></span>

<span data-ttu-id="9eeeb-494">Servidor FTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-494">FTP Server</span></span>

<span data-ttu-id="9eeeb-495">185</span><span class="sxs-lookup"><span data-stu-id="9eeeb-495">185</span></span>

<span data-ttu-id="9eeeb-496">Consola de administración de FTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-496">FTP Management Console</span></span><br/>

<span data-ttu-id="9eeeb-497">314</span><span class="sxs-lookup"><span data-stu-id="9eeeb-497">314</span></span>

<span data-ttu-id="9eeeb-498">Publicación en WebDAV</span><span class="sxs-lookup"><span data-stu-id="9eeeb-498">WebDAV Publishing</span></span>

<span data-ttu-id="9eeeb-499">316</span><span class="sxs-lookup"><span data-stu-id="9eeeb-499">316</span></span>

<span data-ttu-id="9eeeb-500">Servicio FTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-500">FTP Service</span></span><br/>

<span data-ttu-id="9eeeb-501">317</span><span class="sxs-lookup"><span data-stu-id="9eeeb-501">317</span></span>

<span data-ttu-id="9eeeb-502">Extensibilidad de FTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-502">FTP Extensibility</span></span><br/>

<span data-ttu-id="9eeeb-503">336</span><span class="sxs-lookup"><span data-stu-id="9eeeb-503">336</span></span>

<span data-ttu-id="9eeeb-504">Núcleo de web hospedable de IIS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-504">IIS Hostable Web Core</span></span><br/>

<span data-ttu-id="9eeeb-505">413</span><span class="sxs-lookup"><span data-stu-id="9eeeb-505">413</span></span>

[<span data-ttu-id="9eeeb-506">ASP.NET 4,5</span><span class="sxs-lookup"><span data-stu-id="9eeeb-506">ASP.NET 4.5</span></span>](/windows)

<span data-ttu-id="9eeeb-507">414</span><span class="sxs-lookup"><span data-stu-id="9eeeb-507">414</span></span>

[<span data-ttu-id="9eeeb-508">Extensibilidad de .NET 4.5</span><span class="sxs-lookup"><span data-stu-id="9eeeb-508">.NET Extensibility 4.5</span></span>](/windows)

<span data-ttu-id="9eeeb-509">445</span><span class="sxs-lookup"><span data-stu-id="9eeeb-509">445</span></span>

[<span data-ttu-id="9eeeb-510">appialization</span><span class="sxs-lookup"><span data-stu-id="9eeeb-510">appialization</span></span>](/windows)

<span data-ttu-id="9eeeb-511">446</span><span class="sxs-lookup"><span data-stu-id="9eeeb-511">446</span></span>

[<span data-ttu-id="9eeeb-512">compatibilidad centralizada con los certificados SSL</span><span class="sxs-lookup"><span data-stu-id="9eeeb-512">Centralized SSL Certificate Support</span></span>](/windows)

<span data-ttu-id="9eeeb-513">447</span><span class="sxs-lookup"><span data-stu-id="9eeeb-513">447</span></span>

[<span data-ttu-id="9eeeb-514">Protocolo WebSocket</span><span class="sxs-lookup"><span data-stu-id="9eeeb-514">WebSocket Protocol</span></span>](/windows)

<span data-ttu-id="9eeeb-515">Message Queue Server: características (49)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-515">Message Queuing - Features (49)</span></span>

<span data-ttu-id="9eeeb-516">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-516">Value</span></span>

<span data-ttu-id="9eeeb-517">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-517">Name</span></span>

<span data-ttu-id="9eeeb-518">190</span><span class="sxs-lookup"><span data-stu-id="9eeeb-518">190</span></span>

<span data-ttu-id="9eeeb-519">Servicios de Message Queue Server</span><span class="sxs-lookup"><span data-stu-id="9eeeb-519">Message Queuing Services</span></span>

<span data-ttu-id="9eeeb-520">191</span><span class="sxs-lookup"><span data-stu-id="9eeeb-520">191</span></span>

<span data-ttu-id="9eeeb-521">Message Queuing Server</span><span class="sxs-lookup"><span data-stu-id="9eeeb-521">Message Queuing Server</span></span>

<span data-ttu-id="9eeeb-522">192</span><span class="sxs-lookup"><span data-stu-id="9eeeb-522">192</span></span>

<span data-ttu-id="9eeeb-523">Integración del servicio de directorio</span><span class="sxs-lookup"><span data-stu-id="9eeeb-523">Directory Service Integration</span></span>

<span data-ttu-id="9eeeb-524">193</span><span class="sxs-lookup"><span data-stu-id="9eeeb-524">193</span></span>

<span data-ttu-id="9eeeb-525">Desencadenadores de Message Queue Server</span><span class="sxs-lookup"><span data-stu-id="9eeeb-525">Message Queuing Triggers</span></span>

<span data-ttu-id="9eeeb-526">194</span><span class="sxs-lookup"><span data-stu-id="9eeeb-526">194</span></span>

<span data-ttu-id="9eeeb-527">Compatibilidad con HTTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-527">HTTP Support</span></span>

<span data-ttu-id="9eeeb-528">195</span><span class="sxs-lookup"><span data-stu-id="9eeeb-528">195</span></span>

<span data-ttu-id="9eeeb-529">Servicio de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="9eeeb-529">Routing Service</span></span>

<span data-ttu-id="9eeeb-530">196</span><span class="sxs-lookup"><span data-stu-id="9eeeb-530">196</span></span>

[<span data-ttu-id="9eeeb-531">Compatibilidad con clientes de Windows 2000</span><span class="sxs-lookup"><span data-stu-id="9eeeb-531">Windows 2000 Client Support</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-532">197</span><span class="sxs-lookup"><span data-stu-id="9eeeb-532">197</span></span>

<span data-ttu-id="9eeeb-533">Proxy DCOM de Message Queue Server</span><span class="sxs-lookup"><span data-stu-id="9eeeb-533">Message Queuing DCOM Proxy</span></span>

<span data-ttu-id="9eeeb-534">228</span><span class="sxs-lookup"><span data-stu-id="9eeeb-534">228</span></span>

<span data-ttu-id="9eeeb-535">Compatibilidad con multidifusión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-535">Multicasting Support</span></span>

<span data-ttu-id="9eeeb-536">Servicios de certificados de Active Directory: servicios de rol (16)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-536">Active Directory Certificate Services - Role Services (16)</span></span>

<span data-ttu-id="9eeeb-537">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-537">Value</span></span>

<span data-ttu-id="9eeeb-538">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-538">Name</span></span>

<span data-ttu-id="9eeeb-539">200</span><span class="sxs-lookup"><span data-stu-id="9eeeb-539">200</span></span>

<span data-ttu-id="9eeeb-540">Entidad de certificación</span><span class="sxs-lookup"><span data-stu-id="9eeeb-540">Certification Authority</span></span>

<span data-ttu-id="9eeeb-541">201</span><span class="sxs-lookup"><span data-stu-id="9eeeb-541">201</span></span>

<span data-ttu-id="9eeeb-542">Inscripción web de entidad de certificación</span><span class="sxs-lookup"><span data-stu-id="9eeeb-542">Certification Authority Web Enrollment</span></span>

<span data-ttu-id="9eeeb-543">202</span><span class="sxs-lookup"><span data-stu-id="9eeeb-543">202</span></span>

<span data-ttu-id="9eeeb-544">Servicio de respuesta en línea</span><span class="sxs-lookup"><span data-stu-id="9eeeb-544">Online Responder</span></span>

<span data-ttu-id="9eeeb-545">204</span><span class="sxs-lookup"><span data-stu-id="9eeeb-545">204</span></span>

<span data-ttu-id="9eeeb-546">Servicio de inscripción de dispositivos de red</span><span class="sxs-lookup"><span data-stu-id="9eeeb-546">Network Device Enrollment Service</span></span>

<span data-ttu-id="9eeeb-547">318</span><span class="sxs-lookup"><span data-stu-id="9eeeb-547">318</span></span>

[<span data-ttu-id="9eeeb-548">Servicio web de inscripción de certificados</span><span class="sxs-lookup"><span data-stu-id="9eeeb-548">Certificate Enrollment Web Service</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-549">319</span><span class="sxs-lookup"><span data-stu-id="9eeeb-549">319</span></span>

[<span data-ttu-id="9eeeb-550">Servicio web de directivas de inscripción de certificados</span><span class="sxs-lookup"><span data-stu-id="9eeeb-550">Certificate Enrollment Policy Web Service</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-551">Servicios de acceso y directivas de redes: servicios de rol (14)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-551">Network Policy and Access Services - Role Services (14)</span></span>

<span data-ttu-id="9eeeb-552">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-552">Value</span></span>

<span data-ttu-id="9eeeb-553">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-553">Name</span></span>

<span data-ttu-id="9eeeb-554">205</span><span class="sxs-lookup"><span data-stu-id="9eeeb-554">205</span></span>

[<span data-ttu-id="9eeeb-555">Servidor de directivas de redes</span><span class="sxs-lookup"><span data-stu-id="9eeeb-555">Network Policy Server</span></span>](/windows)

<span data-ttu-id="9eeeb-556">206</span><span class="sxs-lookup"><span data-stu-id="9eeeb-556">206</span></span>

[<span data-ttu-id="9eeeb-557">VPN</span><span class="sxs-lookup"><span data-stu-id="9eeeb-557">VPN</span></span>](#vpn)

<span data-ttu-id="9eeeb-558">207</span><span class="sxs-lookup"><span data-stu-id="9eeeb-558">207</span></span>

[<span data-ttu-id="9eeeb-559">Servicios de acceso remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-559">Remote Access Services</span></span>](/windows)

<span data-ttu-id="9eeeb-560">208</span><span class="sxs-lookup"><span data-stu-id="9eeeb-560">208</span></span>

[<span data-ttu-id="9eeeb-561">Enrutamiento</span><span class="sxs-lookup"><span data-stu-id="9eeeb-561">Routing</span></span>](#routing)

<span data-ttu-id="9eeeb-562">210</span><span class="sxs-lookup"><span data-stu-id="9eeeb-562">210</span></span>

[<span data-ttu-id="9eeeb-563">Autoridad de registro de mantenimiento</span><span class="sxs-lookup"><span data-stu-id="9eeeb-563">Health Registration Authority</span></span>](/windows)

<span data-ttu-id="9eeeb-564">250</span><span class="sxs-lookup"><span data-stu-id="9eeeb-564">250</span></span>

[<span data-ttu-id="9eeeb-565">Protocolo de autorización de credenciales de host</span><span class="sxs-lookup"><span data-stu-id="9eeeb-565">Host Credential Authorization Protocol</span></span>](/windows)

<span data-ttu-id="9eeeb-566">Servicios UDDI: servicios de rol (11)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-566">UDDI Services - Role Services (11)</span></span>

<span data-ttu-id="9eeeb-567">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-567">Value</span></span>

<span data-ttu-id="9eeeb-568">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-568">Name</span></span>

<span data-ttu-id="9eeeb-569">215</span><span class="sxs-lookup"><span data-stu-id="9eeeb-569">215</span></span>

[<span data-ttu-id="9eeeb-570">Aplicación web de Servicios UDDI</span><span class="sxs-lookup"><span data-stu-id="9eeeb-570">UDDI Services Web Application</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-571">216</span><span class="sxs-lookup"><span data-stu-id="9eeeb-571">216</span></span>

[<span data-ttu-id="9eeeb-572">Base de datos de Servicios UDDI</span><span class="sxs-lookup"><span data-stu-id="9eeeb-572">UDDI Services Database</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-573">Servicio de activación de procesos de Windows: servicios de rol (41)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-573">Windows Process Activation Service - Role Services (41)</span></span>

<span data-ttu-id="9eeeb-574">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-574">Value</span></span>

<span data-ttu-id="9eeeb-575">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-575">Name</span></span>

<span data-ttu-id="9eeeb-576">217</span><span class="sxs-lookup"><span data-stu-id="9eeeb-576">217</span></span>

<span data-ttu-id="9eeeb-577">API de configuración</span><span class="sxs-lookup"><span data-stu-id="9eeeb-577">Configuration API</span></span>

<span data-ttu-id="9eeeb-578">218</span><span class="sxs-lookup"><span data-stu-id="9eeeb-578">218</span></span>

<span data-ttu-id="9eeeb-579">Entorno .NET</span><span class="sxs-lookup"><span data-stu-id="9eeeb-579">.NET Environment</span></span>

<span data-ttu-id="9eeeb-580">219</span><span class="sxs-lookup"><span data-stu-id="9eeeb-580">219</span></span>

<span data-ttu-id="9eeeb-581">Modelo de proceso</span><span class="sxs-lookup"><span data-stu-id="9eeeb-581">Process Model</span></span>

<span data-ttu-id="9eeeb-582">.NET Framework 3.5.1-características (36)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-582">.NET Framework 3.5.1 - Features (36)</span></span>

<span data-ttu-id="9eeeb-583">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-583">Value</span></span>

<span data-ttu-id="9eeeb-584">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-584">Name</span></span>

<span data-ttu-id="9eeeb-585">220</span><span class="sxs-lookup"><span data-stu-id="9eeeb-585">220</span></span>

<span data-ttu-id="9eeeb-586">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="9eeeb-586">.NET Framework 3.5.1</span></span><br/> [<span data-ttu-id="9eeeb-587">cambio de nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-587">name change</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-588">221</span><span class="sxs-lookup"><span data-stu-id="9eeeb-588">221</span></span>

<span data-ttu-id="9eeeb-589">Activación WCF</span><span class="sxs-lookup"><span data-stu-id="9eeeb-589">WCF Activation</span></span>

<span data-ttu-id="9eeeb-590">222</span><span class="sxs-lookup"><span data-stu-id="9eeeb-590">222</span></span>

<span data-ttu-id="9eeeb-591">Activación de HTTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-591">HTTP Activation</span></span>

<span data-ttu-id="9eeeb-592">223</span><span class="sxs-lookup"><span data-stu-id="9eeeb-592">223</span></span>

<span data-ttu-id="9eeeb-593">Activación no HTTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-593">Non-HTTP Activation</span></span>

<span data-ttu-id="9eeeb-594">227</span><span class="sxs-lookup"><span data-stu-id="9eeeb-594">227</span></span>

<span data-ttu-id="9eeeb-595">Visor de XPS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-595">XPS Viewer</span></span><br/>

<span data-ttu-id="9eeeb-596">Servicios SNMP-características (59)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-596">SNMP Services - Features (59)</span></span>

<span data-ttu-id="9eeeb-597">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-597">Value</span></span>

<span data-ttu-id="9eeeb-598">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-598">Name</span></span>

<span data-ttu-id="9eeeb-599">224</span><span class="sxs-lookup"><span data-stu-id="9eeeb-599">224</span></span>

[<span data-ttu-id="9eeeb-600">Servicio SNMP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-600">SNMP Service</span></span>](/windows)

<span data-ttu-id="9eeeb-601">225</span><span class="sxs-lookup"><span data-stu-id="9eeeb-601">225</span></span>

[<span data-ttu-id="9eeeb-602">Proveedor WMI de SNMP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-602">SNMP WMI Provider</span></span>](/windows)

<span data-ttu-id="9eeeb-603">Servicios de aplicación de servicios de rol</span><span class="sxs-lookup"><span data-stu-id="9eeeb-603">Application Services - Role Services</span></span>

<span data-ttu-id="9eeeb-604">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-604">Value</span></span>

<span data-ttu-id="9eeeb-605">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-605">Name</span></span>

<span data-ttu-id="9eeeb-606">230</span><span class="sxs-lookup"><span data-stu-id="9eeeb-606">230</span></span>

[<span data-ttu-id="9eeeb-607">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="9eeeb-607">.NET Framework 3.5.1</span></span>](/windows)<br/> [<span data-ttu-id="9eeeb-608">cambio de nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-608">name change</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-609">231</span><span class="sxs-lookup"><span data-stu-id="9eeeb-609">231</span></span>

[<span data-ttu-id="9eeeb-610">Compatibilidad con servidor web (IIS)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-610">Web Server (IIS) Support</span></span>](/windows)

<span data-ttu-id="9eeeb-611">232</span><span class="sxs-lookup"><span data-stu-id="9eeeb-611">232</span></span>

[<span data-ttu-id="9eeeb-612">Acceso de red COM+</span><span class="sxs-lookup"><span data-stu-id="9eeeb-612">COM+ Network Access</span></span>](/windows)

<span data-ttu-id="9eeeb-613">233</span><span class="sxs-lookup"><span data-stu-id="9eeeb-613">233</span></span>

[<span data-ttu-id="9eeeb-614">Uso compartido de puertos TCP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-614">TCP Port Sharing</span></span>](/windows)

<span data-ttu-id="9eeeb-615">234</span><span class="sxs-lookup"><span data-stu-id="9eeeb-615">234</span></span>

[<span data-ttu-id="9eeeb-616">Compatibilidad con el servicio WAS (Windows Process Activation Service)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-616">Windows Process Activation Service Support</span></span>](/windows)

<span data-ttu-id="9eeeb-617">235</span><span class="sxs-lookup"><span data-stu-id="9eeeb-617">235</span></span>

[<span data-ttu-id="9eeeb-618">Activación HTTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-618">HTTP Activation</span></span>](/windows)

<span data-ttu-id="9eeeb-619">236</span><span class="sxs-lookup"><span data-stu-id="9eeeb-619">236</span></span>

[<span data-ttu-id="9eeeb-620">Activación de Message Queue Server</span><span class="sxs-lookup"><span data-stu-id="9eeeb-620">Message Queuing Activation</span></span>](/windows)

<span data-ttu-id="9eeeb-621">237</span><span class="sxs-lookup"><span data-stu-id="9eeeb-621">237</span></span>

[<span data-ttu-id="9eeeb-622">Activación TCP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-622">TCP Activation</span></span>](/windows)

<span data-ttu-id="9eeeb-623">238</span><span class="sxs-lookup"><span data-stu-id="9eeeb-623">238</span></span>

[<span data-ttu-id="9eeeb-624">Activación de canalizaciones con nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-624">Named Pipes Activation</span></span>](/windows)

<span data-ttu-id="9eeeb-625">239</span><span class="sxs-lookup"><span data-stu-id="9eeeb-625">239</span></span>

[<span data-ttu-id="9eeeb-626">Transacciones distribuidas</span><span class="sxs-lookup"><span data-stu-id="9eeeb-626">Distributed Transactions</span></span>](/windows)

<span data-ttu-id="9eeeb-627">240</span><span class="sxs-lookup"><span data-stu-id="9eeeb-627">240</span></span>

[<span data-ttu-id="9eeeb-628">Transacciones remotas entrantes</span><span class="sxs-lookup"><span data-stu-id="9eeeb-628">Incoming Remote Transactions</span></span>](/windows)

<span data-ttu-id="9eeeb-629">241</span><span class="sxs-lookup"><span data-stu-id="9eeeb-629">241</span></span>

[<span data-ttu-id="9eeeb-630">Transacciones remotas salientes</span><span class="sxs-lookup"><span data-stu-id="9eeeb-630">Outgoing Remote Transactions</span></span>](/windows)

<span data-ttu-id="9eeeb-631">242</span><span class="sxs-lookup"><span data-stu-id="9eeeb-631">242</span></span>

[<span data-ttu-id="9eeeb-632">Transacciones WS-Automatic</span><span class="sxs-lookup"><span data-stu-id="9eeeb-632">WS-Automatic Transactions</span></span>](/windows)

<span data-ttu-id="9eeeb-633">353</span><span class="sxs-lookup"><span data-stu-id="9eeeb-633">353</span></span>

[<span data-ttu-id="9eeeb-634">Extensiones de servidor de aplicaciones para .NET 4,0</span><span class="sxs-lookup"><span data-stu-id="9eeeb-634">Application Server Extensions for .NET 4.0</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-635">Servicios de implementación de Windows: rol (19)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-635">Windows Deployment Services - Role (19)</span></span>

<span data-ttu-id="9eeeb-636">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-636">Value</span></span>

<span data-ttu-id="9eeeb-637">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-637">Name</span></span>

<span data-ttu-id="9eeeb-638">251</span><span class="sxs-lookup"><span data-stu-id="9eeeb-638">251</span></span>

<span data-ttu-id="9eeeb-639">Servidor de implementación</span><span class="sxs-lookup"><span data-stu-id="9eeeb-639">Deployment Server</span></span>

<span data-ttu-id="9eeeb-640">252</span><span class="sxs-lookup"><span data-stu-id="9eeeb-640">252</span></span>

<span data-ttu-id="9eeeb-641">Servidor de transporte</span><span class="sxs-lookup"><span data-stu-id="9eeeb-641">Transport Server</span></span>

<span data-ttu-id="9eeeb-642">Active Directory Rights Management Services de servicios de rol (17)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-642">Active Directory Rights Management Services - Role Services (17)</span></span>

<span data-ttu-id="9eeeb-643">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-643">Value</span></span>

<span data-ttu-id="9eeeb-644">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-644">Name</span></span>

<span data-ttu-id="9eeeb-645">253</span><span class="sxs-lookup"><span data-stu-id="9eeeb-645">253</span></span>

<span data-ttu-id="9eeeb-646">Servidor de Active Directory Rights Management</span><span class="sxs-lookup"><span data-stu-id="9eeeb-646">Active Directory Rights Management Server</span></span>

<span data-ttu-id="9eeeb-647">254</span><span class="sxs-lookup"><span data-stu-id="9eeeb-647">254</span></span>

<span data-ttu-id="9eeeb-648">Compatibilidad con la federación de identidades</span><span class="sxs-lookup"><span data-stu-id="9eeeb-648">Identity Federation Support</span></span>

<span data-ttu-id="9eeeb-649">Herramientas de administración remota del servidor (67)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-649">Remote Server Administration Tools (67)</span></span>

<span data-ttu-id="9eeeb-650">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-650">Value</span></span>

<span data-ttu-id="9eeeb-651">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-651">Name</span></span>

<span data-ttu-id="9eeeb-652">256</span><span class="sxs-lookup"><span data-stu-id="9eeeb-652">256</span></span>

[<span data-ttu-id="9eeeb-653">Herramientas de administración de roles</span><span class="sxs-lookup"><span data-stu-id="9eeeb-653">Role Administration Tools</span></span>](/windows)

<span data-ttu-id="9eeeb-654">257</span><span class="sxs-lookup"><span data-stu-id="9eeeb-654">257</span></span>

[<span data-ttu-id="9eeeb-655">Herramientas de AD DS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-655">AD DS Tools</span></span>](/windows)<br/> [<span data-ttu-id="9eeeb-656">cambio de nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-656">name change</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-657">258</span><span class="sxs-lookup"><span data-stu-id="9eeeb-657">258</span></span>

[<span data-ttu-id="9eeeb-658">AD LDS herramientas de Snap-Ins y Command-Line</span><span class="sxs-lookup"><span data-stu-id="9eeeb-658">AD LDS Snap-Ins and Command-Line Tools</span></span>](/windows)<br/> [<span data-ttu-id="9eeeb-659">cambio de nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-659">name change</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-660">259</span><span class="sxs-lookup"><span data-stu-id="9eeeb-660">259</span></span>

<span data-ttu-id="9eeeb-661">Herramientas de servicios de certificados de Active Directory</span><span class="sxs-lookup"><span data-stu-id="9eeeb-661">Active Directory Certificate Services Tools</span></span>

<span data-ttu-id="9eeeb-662">260</span><span class="sxs-lookup"><span data-stu-id="9eeeb-662">260</span></span>

[<span data-ttu-id="9eeeb-663">Network Policy and Access Services</span><span class="sxs-lookup"><span data-stu-id="9eeeb-663">Network Policy and Access Services</span></span>](/windows)

<span data-ttu-id="9eeeb-664">261</span><span class="sxs-lookup"><span data-stu-id="9eeeb-664">261</span></span>

<span data-ttu-id="9eeeb-665">Herramientas de Servicios de impresión y documentos</span><span class="sxs-lookup"><span data-stu-id="9eeeb-665">Print and Document Services Tools</span></span><br/> [<span data-ttu-id="9eeeb-666">cambio de nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-666">name change</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-667">262</span><span class="sxs-lookup"><span data-stu-id="9eeeb-667">262</span></span>

[<span data-ttu-id="9eeeb-668">Active Directory Rights Management Services</span><span class="sxs-lookup"><span data-stu-id="9eeeb-668">Active Directory Rights Management Services</span></span>](/windows)

<span data-ttu-id="9eeeb-669">263</span><span class="sxs-lookup"><span data-stu-id="9eeeb-669">263</span></span>

[<span data-ttu-id="9eeeb-670">Herramientas de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-670">Remote Desktop Services Tools</span></span>](/windows)<br/> [<span data-ttu-id="9eeeb-671">cambio de nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-671">name change</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-672">264</span><span class="sxs-lookup"><span data-stu-id="9eeeb-672">264</span></span>

<span data-ttu-id="9eeeb-673">Herramientas de Servicios de implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="9eeeb-673">Windows Deployment Services Tools</span></span>

<span data-ttu-id="9eeeb-674">265</span><span class="sxs-lookup"><span data-stu-id="9eeeb-674">265</span></span>

[<span data-ttu-id="9eeeb-675">Herramientas de administración de características</span><span class="sxs-lookup"><span data-stu-id="9eeeb-675">Feature Administration Tools</span></span>](/windows)

<span data-ttu-id="9eeeb-676">266</span><span class="sxs-lookup"><span data-stu-id="9eeeb-676">266</span></span>

<span data-ttu-id="9eeeb-677">Herramientas de cifrado de unidad BitLocker</span><span class="sxs-lookup"><span data-stu-id="9eeeb-677">BitLocker Drive Encryption Tools</span></span>

<span data-ttu-id="9eeeb-678">267</span><span class="sxs-lookup"><span data-stu-id="9eeeb-678">267</span></span>

<span data-ttu-id="9eeeb-679">Herramientas de extensiones de servidor BITS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-679">BITS Server Extensions Tools</span></span>

<span data-ttu-id="9eeeb-680">268</span><span class="sxs-lookup"><span data-stu-id="9eeeb-680">268</span></span>

[<span data-ttu-id="9eeeb-681">Herramientas de clústeres de conmutación por error</span><span class="sxs-lookup"><span data-stu-id="9eeeb-681">Failover Clustering Tools</span></span>](/windows)

<span data-ttu-id="9eeeb-682">269</span><span class="sxs-lookup"><span data-stu-id="9eeeb-682">269</span></span>

<span data-ttu-id="9eeeb-683">Herramientas de equilibrio de carga de red</span><span class="sxs-lookup"><span data-stu-id="9eeeb-683">Network Load Balancing Tools</span></span>

<span data-ttu-id="9eeeb-684">270</span><span class="sxs-lookup"><span data-stu-id="9eeeb-684">270</span></span>

<span data-ttu-id="9eeeb-685">Herramientas del servidor SMTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-685">SMTP Server Tools</span></span>

<span data-ttu-id="9eeeb-686">273</span><span class="sxs-lookup"><span data-stu-id="9eeeb-686">273</span></span>

[<span data-ttu-id="9eeeb-687">Herramientas del servidor DNS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-687">DNS Server Tools</span></span>](/windows)

<span data-ttu-id="9eeeb-688">277</span><span class="sxs-lookup"><span data-stu-id="9eeeb-688">277</span></span>

<span data-ttu-id="9eeeb-689">Herramientas de Servicios de archivo</span><span class="sxs-lookup"><span data-stu-id="9eeeb-689">File Services Tools</span></span>

<span data-ttu-id="9eeeb-690">278</span><span class="sxs-lookup"><span data-stu-id="9eeeb-690">278</span></span>

<span data-ttu-id="9eeeb-691">Herramientas de Sistema de archivos distribuido</span><span class="sxs-lookup"><span data-stu-id="9eeeb-691">Distributed File System Tools</span></span>

<span data-ttu-id="9eeeb-692">279</span><span class="sxs-lookup"><span data-stu-id="9eeeb-692">279</span></span>

<span data-ttu-id="9eeeb-693">Herramientas del Administrador de recursos del servidor de archivos</span><span class="sxs-lookup"><span data-stu-id="9eeeb-693">File Server Resource Manager Tools</span></span>

<span data-ttu-id="9eeeb-694">280</span><span class="sxs-lookup"><span data-stu-id="9eeeb-694">280</span></span>

[<span data-ttu-id="9eeeb-695">Servicios para herramientas del sistema de archivos de red</span><span class="sxs-lookup"><span data-stu-id="9eeeb-695">Services For Network File System Tools</span></span>](/windows)

<span data-ttu-id="9eeeb-696">281</span><span class="sxs-lookup"><span data-stu-id="9eeeb-696">281</span></span>

<span data-ttu-id="9eeeb-697">Herramientas del servidor Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-697">Web Server (IIS) Tools</span></span>

<span data-ttu-id="9eeeb-698">284</span><span class="sxs-lookup"><span data-stu-id="9eeeb-698">284</span></span>

[<span data-ttu-id="9eeeb-699">Herramientas del host de sesión Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-699">Remote Desktop Session Host Tools</span></span>](/windows)<br/> [<span data-ttu-id="9eeeb-700">cambio de nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-700">name change</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-701">285</span><span class="sxs-lookup"><span data-stu-id="9eeeb-701">285</span></span>

<span data-ttu-id="9eeeb-702">Herramientas de puerta de enlace de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-702">Remote Desktop Gateway Tools</span></span><br/> [<span data-ttu-id="9eeeb-703">cambio de nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-703">name change</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-704">286</span><span class="sxs-lookup"><span data-stu-id="9eeeb-704">286</span></span>

<span data-ttu-id="9eeeb-705">Herramientas de licencias de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-705">Remote Desktop Licensing Tools</span></span><br/> [<span data-ttu-id="9eeeb-706">cambio de nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-706">name change</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-707">288</span><span class="sxs-lookup"><span data-stu-id="9eeeb-707">288</span></span>

<span data-ttu-id="9eeeb-708">Herramientas del servidor de fax</span><span class="sxs-lookup"><span data-stu-id="9eeeb-708">Fax Server Tools</span></span>

<span data-ttu-id="9eeeb-709">290</span><span class="sxs-lookup"><span data-stu-id="9eeeb-709">290</span></span>

<span data-ttu-id="9eeeb-710">Herramientas del servidor WINS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-710">WINS Server Tools</span></span>

<span data-ttu-id="9eeeb-711">291</span><span class="sxs-lookup"><span data-stu-id="9eeeb-711">291</span></span>

[<span data-ttu-id="9eeeb-712">Herramientas de Servicios UDDI</span><span class="sxs-lookup"><span data-stu-id="9eeeb-712">UDDI Services Tools</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-713">292</span><span class="sxs-lookup"><span data-stu-id="9eeeb-713">292</span></span>

<span data-ttu-id="9eeeb-714">Herramientas de entidad de certificación</span><span class="sxs-lookup"><span data-stu-id="9eeeb-714">Certification Authority Tools</span></span>

<span data-ttu-id="9eeeb-715">293</span><span class="sxs-lookup"><span data-stu-id="9eeeb-715">293</span></span>

<span data-ttu-id="9eeeb-716">Herramientas de respuesta en línea</span><span class="sxs-lookup"><span data-stu-id="9eeeb-716">Online Responder Tools</span></span>

<span data-ttu-id="9eeeb-717">297</span><span class="sxs-lookup"><span data-stu-id="9eeeb-717">297</span></span>

[<span data-ttu-id="9eeeb-718">Herramientas de Servidor para NIS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-718">Server for NIS Tools</span></span>](/windows)

<span data-ttu-id="9eeeb-719">299</span><span class="sxs-lookup"><span data-stu-id="9eeeb-719">299</span></span>

[<span data-ttu-id="9eeeb-720">Complementos y herramientas de línea de comandos de AD DS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-720">AD DS Snap-Ins and Command-Line Tools</span></span>](/windows)<br/> [<span data-ttu-id="9eeeb-721">cambio de nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-721">name change</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-722">300</span><span class="sxs-lookup"><span data-stu-id="9eeeb-722">300</span></span>

[<span data-ttu-id="9eeeb-723">Centro de administración de Active Directory</span><span class="sxs-lookup"><span data-stu-id="9eeeb-723">Active Directory Administrative Center</span></span>](/windows)

<span data-ttu-id="9eeeb-724">301</span><span class="sxs-lookup"><span data-stu-id="9eeeb-724">301</span></span>

<span data-ttu-id="9eeeb-725">Herramientas de Hyper-V</span><span class="sxs-lookup"><span data-stu-id="9eeeb-725">Hyper-V Tools</span></span>

<span data-ttu-id="9eeeb-726">323</span><span class="sxs-lookup"><span data-stu-id="9eeeb-726">323</span></span>

[<span data-ttu-id="9eeeb-727">Visor de contraseñas de recuperación de BitLocker</span><span class="sxs-lookup"><span data-stu-id="9eeeb-727">BitLocker Recovery Password Viewer</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-728">326</span><span class="sxs-lookup"><span data-stu-id="9eeeb-728">326</span></span>

[<span data-ttu-id="9eeeb-729">Utilidades de administración de Cifrado de unidad BitLocker</span><span class="sxs-lookup"><span data-stu-id="9eeeb-729">BitLocker Drive Encryption Administration Utilities</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-730">329</span><span class="sxs-lookup"><span data-stu-id="9eeeb-730">329</span></span>

[<span data-ttu-id="9eeeb-731">Herramientas de AD DS y AD LDS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-731">AD DS and AD LDS Tools</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-732">330</span><span class="sxs-lookup"><span data-stu-id="9eeeb-732">330</span></span>

<span data-ttu-id="9eeeb-733">Centro de administración de Active Directory</span><span class="sxs-lookup"><span data-stu-id="9eeeb-733">Active Directory Administrative Center</span></span><br/>

<span data-ttu-id="9eeeb-734">331</span><span class="sxs-lookup"><span data-stu-id="9eeeb-734">331</span></span>

[<span data-ttu-id="9eeeb-735">Módulo de Active Directory para Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-735">Active Directory module for Windows PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-736">337</span><span class="sxs-lookup"><span data-stu-id="9eeeb-736">337</span></span>

[<span data-ttu-id="9eeeb-737">Herramientas de Conexión a Escritorio remoto Broker</span><span class="sxs-lookup"><span data-stu-id="9eeeb-737">Remote Desktop Connection Broker Tools</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-738">410</span><span class="sxs-lookup"><span data-stu-id="9eeeb-738">410</span></span>

[<span data-ttu-id="9eeeb-739">Cliente de administración de direcciones IP (IPAM)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-739">IP Address Management (IPAM) Client</span></span>](/windows)

<span data-ttu-id="9eeeb-740">450</span><span class="sxs-lookup"><span data-stu-id="9eeeb-740">450</span></span>

[<span data-ttu-id="9eeeb-741">Módulo de Hyper-V para Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-741">Hyper-V Module for Windows PowerShell</span></span>](/windows)

<span data-ttu-id="9eeeb-742">462</span><span class="sxs-lookup"><span data-stu-id="9eeeb-742">462</span></span>

[<span data-ttu-id="9eeeb-743">Herramientas de Active Directory Rights Management Services</span><span class="sxs-lookup"><span data-stu-id="9eeeb-743">Active Directory Rights Management Services Tools</span></span>](/windows)

<span data-ttu-id="9eeeb-744">465</span><span class="sxs-lookup"><span data-stu-id="9eeeb-744">465</span></span>

[<span data-ttu-id="9eeeb-745">Herramienta de administración de almacenamiento y recursos compartidos</span><span class="sxs-lookup"><span data-stu-id="9eeeb-745">Share and Storage Management Tool</span></span>](/windows)

<span data-ttu-id="9eeeb-746">471</span><span class="sxs-lookup"><span data-stu-id="9eeeb-746">471</span></span>

[<span data-ttu-id="9eeeb-747">Herramientas de administración de acceso remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-747">Remote Access Management Tools</span></span>](/windows)

<span data-ttu-id="9eeeb-748">472</span><span class="sxs-lookup"><span data-stu-id="9eeeb-748">472</span></span>

[<span data-ttu-id="9eeeb-749">Módulo de acceso remoto para Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-749">Remote Access module for Windows PowerShell</span></span>](/windows)

<span data-ttu-id="9eeeb-750">473</span><span class="sxs-lookup"><span data-stu-id="9eeeb-750">473</span></span>

[<span data-ttu-id="9eeeb-751">Herramientas de Command-Line y GUI de acceso remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-751">Remote Access GUI and Command-Line Tools</span></span>](/windows)

<span data-ttu-id="9eeeb-752">474</span><span class="sxs-lookup"><span data-stu-id="9eeeb-752">474</span></span>

[<span data-ttu-id="9eeeb-753">Herramientas de Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="9eeeb-753">Windows Server Update Services Tools</span></span>](/windows)

<span data-ttu-id="9eeeb-754">476</span><span class="sxs-lookup"><span data-stu-id="9eeeb-754">476</span></span>

[<span data-ttu-id="9eeeb-755">Herramientas del diagnóstico de licencias de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-755">Remote Desktop Licensing Diagnoser Tools</span></span>](/windows)

<span data-ttu-id="9eeeb-756">479</span><span class="sxs-lookup"><span data-stu-id="9eeeb-756">479</span></span>

[<span data-ttu-id="9eeeb-757">Herramientas de SNMP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-757">SNMP Tools</span></span>](/windows)

<span data-ttu-id="9eeeb-758">480</span><span class="sxs-lookup"><span data-stu-id="9eeeb-758">480</span></span>

[<span data-ttu-id="9eeeb-759">Herramientas de activación de volumen</span><span class="sxs-lookup"><span data-stu-id="9eeeb-759">Volume Activation Tools</span></span>](/windows)

<span data-ttu-id="9eeeb-760">Copias de seguridad de Windows Server-características (39)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-760">Windows Server Backup - Features (39)</span></span>

<span data-ttu-id="9eeeb-761">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-761">Value</span></span>

<span data-ttu-id="9eeeb-762">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-762">Name</span></span>

<span data-ttu-id="9eeeb-763">296</span><span class="sxs-lookup"><span data-stu-id="9eeeb-763">296</span></span>

[<span data-ttu-id="9eeeb-764">Copias de seguridad de Windows Server</span><span class="sxs-lookup"><span data-stu-id="9eeeb-764">Windows Server Backup</span></span>](/windows)

<span data-ttu-id="9eeeb-765">297</span><span class="sxs-lookup"><span data-stu-id="9eeeb-765">297</span></span>

[<span data-ttu-id="9eeeb-766">Herramientas de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="9eeeb-766">Command Line Tools</span></span>](/windows)

<span data-ttu-id="9eeeb-767">Servicios de Escritura con lápiz y Escritura a mano-características (310)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-767">Ink and Handwriting Services - Features (310)</span></span>

<span data-ttu-id="9eeeb-768">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-768">Value</span></span>

<span data-ttu-id="9eeeb-769">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-769">Name</span></span>

<span data-ttu-id="9eeeb-770">311</span><span class="sxs-lookup"><span data-stu-id="9eeeb-770">311</span></span>

[<span data-ttu-id="9eeeb-771">Compatibilidad con entradas manuscritas</span><span class="sxs-lookup"><span data-stu-id="9eeeb-771">Ink Support</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-772">312</span><span class="sxs-lookup"><span data-stu-id="9eeeb-772">312</span></span>

[<span data-ttu-id="9eeeb-773">Reconocimiento de escritura a mano</span><span class="sxs-lookup"><span data-stu-id="9eeeb-773">Handwriting Recognition</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-774">Servicio de transferencia inteligente en segundo plano (BITS)-características (335)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-774">Background Intelligent Transfer Service (BITS) - Features (335)</span></span>

<span data-ttu-id="9eeeb-775">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-775">Value</span></span>

<span data-ttu-id="9eeeb-776">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-776">Name</span></span>

<span data-ttu-id="9eeeb-777">54</span><span class="sxs-lookup"><span data-stu-id="9eeeb-777">54</span></span>

<span data-ttu-id="9eeeb-778">Extensión de servidor IIS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-778">IIS Server Extension</span></span>

<span data-ttu-id="9eeeb-779">332</span><span class="sxs-lookup"><span data-stu-id="9eeeb-779">332</span></span>

[<span data-ttu-id="9eeeb-780">Servidor compacto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-780">Compact Server</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-781">Compatibilidad con WOW64: características (340)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-781">Wow64 Support - Features (340)</span></span>

<span data-ttu-id="9eeeb-782">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-782">Value</span></span>

<span data-ttu-id="9eeeb-783">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-783">Name</span></span>

<span data-ttu-id="9eeeb-784">341</span><span class="sxs-lookup"><span data-stu-id="9eeeb-784">341</span></span>

[<span data-ttu-id="9eeeb-785">WoW64</span><span class="sxs-lookup"><span data-stu-id="9eeeb-785">WoW64</span></span>](#wow64)<br/>

<span data-ttu-id="9eeeb-786">342</span><span class="sxs-lookup"><span data-stu-id="9eeeb-786">342</span></span>

[<span data-ttu-id="9eeeb-787">WoW64 para .NET Framework 2,0 y Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-787">WoW64 for .NET Framework 2.0 and Windows PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-788">343</span><span class="sxs-lookup"><span data-stu-id="9eeeb-788">343</span></span>

[<span data-ttu-id="9eeeb-789">WoW64 para .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="9eeeb-789">WoW64 for .NET Framework 2.0</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-790">344</span><span class="sxs-lookup"><span data-stu-id="9eeeb-790">344</span></span>

[<span data-ttu-id="9eeeb-791">WoW64 para PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-791">WoW64 for PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-792">345</span><span class="sxs-lookup"><span data-stu-id="9eeeb-792">345</span></span>

[<span data-ttu-id="9eeeb-793">WoW64 para .NET Framework 3,0 y 3,5</span><span class="sxs-lookup"><span data-stu-id="9eeeb-793">WoW64 for .NET Framework 3.0 and 3.5</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-794">346</span><span class="sxs-lookup"><span data-stu-id="9eeeb-794">346</span></span>

[<span data-ttu-id="9eeeb-795">WoW64 para servicios de impresión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-795">WoW64 for Print Services</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-796">347</span><span class="sxs-lookup"><span data-stu-id="9eeeb-796">347</span></span>

[<span data-ttu-id="9eeeb-797">WoW64 para clúster de conmutación por error</span><span class="sxs-lookup"><span data-stu-id="9eeeb-797">WoW64 for Failover Clustering</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-798">348</span><span class="sxs-lookup"><span data-stu-id="9eeeb-798">348</span></span>

[<span data-ttu-id="9eeeb-799">WoW64 para el editor de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="9eeeb-799">WoW64 for Input Method Editor</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-800">349</span><span class="sxs-lookup"><span data-stu-id="9eeeb-800">349</span></span>

[<span data-ttu-id="9eeeb-801">WoW64 para Subsystem for UNIX-Based Applications</span><span class="sxs-lookup"><span data-stu-id="9eeeb-801">WoW64 for Subsystem for UNIX-based Applications</span></span>](/windows)<br/>

<span data-ttu-id="9eeeb-802">Interfaces de usuario e infraestructura: servicios de rol (447)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-802">User Interfaces and Infrastructure - Role Services (447)</span></span>

<span data-ttu-id="9eeeb-803">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-803">Value</span></span>

<span data-ttu-id="9eeeb-804">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-804">Name</span></span>

<span data-ttu-id="9eeeb-805">35</span><span class="sxs-lookup"><span data-stu-id="9eeeb-805">35</span></span>

[<span data-ttu-id="9eeeb-806">Experiencia de escritorio</span><span class="sxs-lookup"><span data-stu-id="9eeeb-806">Desktop Experience</span></span>](/windows)

<span data-ttu-id="9eeeb-807">99</span><span class="sxs-lookup"><span data-stu-id="9eeeb-807">99</span></span>

[<span data-ttu-id="9eeeb-808">Shell gráfico de servidor</span><span class="sxs-lookup"><span data-stu-id="9eeeb-808">Server Graphical Shell</span></span>](/windows)

<span data-ttu-id="9eeeb-809">Windows Server Update Services: características (404)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-809">Window Server Update Services - Features (404)</span></span>

<span data-ttu-id="9eeeb-810">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-810">Value</span></span>

<span data-ttu-id="9eeeb-811">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-811">Name</span></span>

<span data-ttu-id="9eeeb-812">405</span><span class="sxs-lookup"><span data-stu-id="9eeeb-812">405</span></span>

[<span data-ttu-id="9eeeb-813">API y cmdlets de PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-813">API and PowerShell cmdlets</span></span>](/windows)

<span data-ttu-id="9eeeb-814">406</span><span class="sxs-lookup"><span data-stu-id="9eeeb-814">406</span></span>

[<span data-ttu-id="9eeeb-815">Conectividad SQL Server</span><span class="sxs-lookup"><span data-stu-id="9eeeb-815">SQL Server Connectivity</span></span>](/windows)

<span data-ttu-id="9eeeb-816">407</span><span class="sxs-lookup"><span data-stu-id="9eeeb-816">407</span></span>

[<span data-ttu-id="9eeeb-817">Servicios WSUS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-817">WSUS Services</span></span>](/windows)

<span data-ttu-id="9eeeb-818">408</span><span class="sxs-lookup"><span data-stu-id="9eeeb-818">408</span></span>

[<span data-ttu-id="9eeeb-819">Consola de administración de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="9eeeb-819">User Interface Management Console</span></span>](/windows)

<span data-ttu-id="9eeeb-820">449</span><span class="sxs-lookup"><span data-stu-id="9eeeb-820">449</span></span>

[<span data-ttu-id="9eeeb-821">Conectividad WID</span><span class="sxs-lookup"><span data-stu-id="9eeeb-821">WID Connectivity</span></span>](/windows)

<span data-ttu-id="9eeeb-822">Windows PowerShell-características (417)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-822">Windows PowerShell - Features (417)</span></span>

<span data-ttu-id="9eeeb-823">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-823">Value</span></span>

<span data-ttu-id="9eeeb-824">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-824">Name</span></span>

<span data-ttu-id="9eeeb-825">411</span><span class="sxs-lookup"><span data-stu-id="9eeeb-825">411</span></span>

[<span data-ttu-id="9eeeb-826">Motor 2,0 de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-826">Windows PowerShell 2.0 Engine</span></span>](/windows)

<span data-ttu-id="9eeeb-827">412</span><span class="sxs-lookup"><span data-stu-id="9eeeb-827">412</span></span>

[<span data-ttu-id="9eeeb-828">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="9eeeb-828">Windows PowerShell 3.0</span></span>](/windows)

<span data-ttu-id="9eeeb-829">448</span><span class="sxs-lookup"><span data-stu-id="9eeeb-829">448</span></span>

[<span data-ttu-id="9eeeb-830">Windows PowerShell Web Access</span><span class="sxs-lookup"><span data-stu-id="9eeeb-830">Windows PowerShell Web Access</span></span>](/windows)

<span data-ttu-id="9eeeb-831">1000</span><span class="sxs-lookup"><span data-stu-id="9eeeb-831">1000</span></span>

[<span data-ttu-id="9eeeb-832">Servicio de configuración de estado deseado de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-832">Windows PowerShell Desired State Configuration Service</span></span>](/windows)

<span data-ttu-id="9eeeb-833">.NET Framework 4,5-características (418)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-833">.NET Framework 4.5 - Features (418)</span></span>

<span data-ttu-id="9eeeb-834">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-834">Value</span></span>

<span data-ttu-id="9eeeb-835">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-835">Name</span></span>

<span data-ttu-id="9eeeb-836">419</span><span class="sxs-lookup"><span data-stu-id="9eeeb-836">419</span></span>

[<span data-ttu-id="9eeeb-837">.NET Framework 4,5 extendido</span><span class="sxs-lookup"><span data-stu-id="9eeeb-837">.NET Framework 4.5 Extended</span></span>](/windows)

<span data-ttu-id="9eeeb-838">420</span><span class="sxs-lookup"><span data-stu-id="9eeeb-838">420</span></span>

[<span data-ttu-id="9eeeb-839">Servicios WCF</span><span class="sxs-lookup"><span data-stu-id="9eeeb-839">WCF Services</span></span>](/windows)

<span data-ttu-id="9eeeb-840">421</span><span class="sxs-lookup"><span data-stu-id="9eeeb-840">421</span></span>

[<span data-ttu-id="9eeeb-841">Activación HTTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-841">HTTP Activation</span></span>](/windows)

<span data-ttu-id="9eeeb-842">422</span><span class="sxs-lookup"><span data-stu-id="9eeeb-842">422</span></span>

[<span data-ttu-id="9eeeb-843">Activación de Message Queuing (MSMQ)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-843">Message Queuing (MSMQ) Activation</span></span>](/windows)

<span data-ttu-id="9eeeb-844">423</span><span class="sxs-lookup"><span data-stu-id="9eeeb-844">423</span></span>

[<span data-ttu-id="9eeeb-845">Activación de canalización con nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-845">Named Pipe Activation</span></span>](/windows)

<span data-ttu-id="9eeeb-846">424</span><span class="sxs-lookup"><span data-stu-id="9eeeb-846">424</span></span>

[<span data-ttu-id="9eeeb-847">Activación TCP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-847">TCP Activation</span></span>](/windows)

<span data-ttu-id="9eeeb-848">425</span><span class="sxs-lookup"><span data-stu-id="9eeeb-848">425</span></span>

[<span data-ttu-id="9eeeb-849">Uso compartido de puertos TCP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-849">TCP Port Sharing</span></span>](/windows)

<span data-ttu-id="9eeeb-850">429</span><span class="sxs-lookup"><span data-stu-id="9eeeb-850">429</span></span>

[<span data-ttu-id="9eeeb-851">ASP.NET 4,5</span><span class="sxs-lookup"><span data-stu-id="9eeeb-851">ASP.NET 4.5</span></span>](/windows)

<span data-ttu-id="9eeeb-852">Acceso remoto: rol (468)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-852">Remote Access - Role (468)</span></span>

<span data-ttu-id="9eeeb-853">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-853">Value</span></span>

<span data-ttu-id="9eeeb-854">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-854">Name</span></span>

<span data-ttu-id="9eeeb-855">469</span><span class="sxs-lookup"><span data-stu-id="9eeeb-855">469</span></span>

[<span data-ttu-id="9eeeb-856">DirectAccess y VPN (RAS)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-856">DirectAccess and VPN (RAS)</span></span>](/windows)

<span data-ttu-id="9eeeb-857">470</span><span class="sxs-lookup"><span data-stu-id="9eeeb-857">470</span></span>

[<span data-ttu-id="9eeeb-858">Enrutamiento</span><span class="sxs-lookup"><span data-stu-id="9eeeb-858">Routing</span></span>](#routing)

<span data-ttu-id="9eeeb-859">Servicios de archivos y almacenamiento: rol (481)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-859">File and Storage Services - Role (481)</span></span>

<span data-ttu-id="9eeeb-860">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-860">Value</span></span>

<span data-ttu-id="9eeeb-861">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-861">Name</span></span>

<span data-ttu-id="9eeeb-862">482</span><span class="sxs-lookup"><span data-stu-id="9eeeb-862">482</span></span>

[<span data-ttu-id="9eeeb-863">Servicios de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="9eeeb-863">Storage Services</span></span>](/windows)

<span data-ttu-id="9eeeb-864">484</span><span class="sxs-lookup"><span data-stu-id="9eeeb-864">484</span></span>

[<span data-ttu-id="9eeeb-865">Herramientas de administración del clúster de conmutación por error</span><span class="sxs-lookup"><span data-stu-id="9eeeb-865">Failover Cluster Management Tools</span></span>](/windows)



 

</dd> <dt>

<span data-ttu-id="9eeeb-866">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="9eeeb-866">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eeeb-867">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9eeeb-867">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9eeeb-868">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9eeeb-868">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9eeeb-869">Nombre para mostrar de la característica de servidor, como "servidor de archivos", "servidor de impresión" o "experiencia de escritorio".</span><span class="sxs-lookup"><span data-stu-id="9eeeb-869">Display name of the server feature, such as "File Server", "Print Server", or "Desktop Experience".</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-870">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9eeeb-870">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eeeb-871">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9eeeb-871">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9eeeb-872">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9eeeb-872">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9eeeb-873">Número de ID. de la característica de servidor principal.</span><span class="sxs-lookup"><span data-stu-id="9eeeb-873">ID number of the parent server feature.</span></span> <span data-ttu-id="9eeeb-874">Esta propiedad es 0 si la característica representada por la instancia actual de la clase no tiene una característica primaria.</span><span class="sxs-lookup"><span data-stu-id="9eeeb-874">This property is 0 if the feature represented by the current instance of the class does not have a parent feature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9eeeb-875">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9eeeb-875">Remarks</span></span>

<span data-ttu-id="9eeeb-876">Lea la [información técnica de administrador del servidor de Windows Server 2008](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753319(v=ws.10)) para obtener información sobre las características de servidor.</span><span class="sxs-lookup"><span data-stu-id="9eeeb-876">Read the [Windows Server 2008 Server Manager Technical Overview](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753319(v=ws.10)) to learn about server features.</span></span>

<span data-ttu-id="9eeeb-877">Las empresas que no usan software de administración que informa de las características del servidor, como System Center Operations Manager con módulos de administración instalados, pueden obtener esa información consultando la clase **\_ ServerFeature de Win32** .</span><span class="sxs-lookup"><span data-stu-id="9eeeb-877">Enterprises that do not use management software that reports server features, such as System Center Operations Manager with management packs installed, can get that information by querying the **Win32\_ServerFeature** class.</span></span>

<span data-ttu-id="9eeeb-878">Puede usar las características de comunicación remota de WMI o WinRM para obtener información de características de servidor de los servidores remotos.</span><span class="sxs-lookup"><span data-stu-id="9eeeb-878">You can use the remoting features of WMI or WinRM to get server feature information from remote servers.</span></span> <span data-ttu-id="9eeeb-879">Para obtener más información acerca de las conexiones remotas DCOM de WMI, consulte [conectarse a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="9eeeb-879">For more information about remote WMI DCOM connections, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="9eeeb-880">Para más información sobre WinRM, consulte Administración remota de Windows.</span><span class="sxs-lookup"><span data-stu-id="9eeeb-880">For more information about WinRM, see Windows Remote Management.</span></span>

<span data-ttu-id="9eeeb-881">Windows Server 2012: **Win32 \_ ServerFeature** está en desuso.</span><span class="sxs-lookup"><span data-stu-id="9eeeb-881">Windows Server 2012: **Win32\_ServerFeature** has been deprecated.</span></span> <span data-ttu-id="9eeeb-882">Para acceder a la información de características de Windows Server mediante programación, puede usar los [cmdlets de administrador del servidor](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee662311(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="9eeeb-882">To access windows server feature information programmatically, you can use the [Server Manager Cmdlets](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee662311(v=technet.10)).</span></span>

### <a name="windows-server-2012-r2"></a><span data-ttu-id="9eeeb-883">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9eeeb-883">Windows Server 2012 R2</span></span>

<dl> <dt>

<span data-ttu-id="9eeeb-884"><span id="Application_Server"></span><span id="application_server"></span><span id="APPLICATION_SERVER"></span>Servidor de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="9eeeb-884"><span id="Application_Server"></span><span id="application_server"></span><span id="APPLICATION_SERVER"></span>Application Server</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-885">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-885">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-886"><span id="Streaming_Media_Services"></span><span id="streaming_media_services"></span><span id="STREAMING_MEDIA_SERVICES"></span>Media Services de streaming</span><span class="sxs-lookup"><span data-stu-id="9eeeb-886"><span id="Streaming_Media_Services"></span><span id="streaming_media_services"></span><span id="STREAMING_MEDIA_SERVICES"></span>Streaming Media Services</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-887">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-887">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-888"><span id="Active_Directory_Federation_Services"></span><span id="active_directory_federation_services"></span><span id="ACTIVE_DIRECTORY_FEDERATION_SERVICES"></span>Servicios de federación de Active Directory (AD FS)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-888"><span id="Active_Directory_Federation_Services"></span><span id="active_directory_federation_services"></span><span id="ACTIVE_DIRECTORY_FEDERATION_SERVICES"></span>Active Directory Federation Services</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-889">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-889">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-890"><span id="DHCP_Server"></span><span id="dhcp_server"></span><span id="DHCP_SERVER"></span>Servidor DHCP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-890"><span id="DHCP_Server"></span><span id="dhcp_server"></span><span id="DHCP_SERVER"></span>DHCP Server</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-891">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-891">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-892"><span id="DNS_Server"></span><span id="dns_server"></span><span id="DNS_SERVER"></span>Servidor DNS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-892"><span id="DNS_Server"></span><span id="dns_server"></span><span id="DNS_SERVER"></span>DNS Server</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-893">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-893">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-894"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-894"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>Remote Desktop Services</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-895">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-895">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-896"><span id="Windows_Server_Update_Services"></span><span id="windows_server_update_services"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="9eeeb-896"><span id="Windows_Server_Update_Services"></span><span id="windows_server_update_services"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-897">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-897">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-898"><span id="Failover_Clustering"></span><span id="failover_clustering"></span><span id="FAILOVER_CLUSTERING"></span>Clústeres de conmutación por error</span><span class="sxs-lookup"><span data-stu-id="9eeeb-898"><span id="Failover_Clustering"></span><span id="failover_clustering"></span><span id="FAILOVER_CLUSTERING"></span>Failover Clustering</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-899">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-899">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-900"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Equilibrio de carga de red</span><span class="sxs-lookup"><span data-stu-id="9eeeb-900"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Network Load Balancing</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-901">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-901">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-902"><span id=".NET_Framework_3.5.1_Features"></span><span id=".net_framework_3.5.1_features"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES"></span>Características de .NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="9eeeb-902"><span id=".NET_Framework_3.5.1_Features"></span><span id=".net_framework_3.5.1_features"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES"></span>.NET Framework 3.5.1 Features</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-903">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-903">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-904"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Administrador de recursos del sistema de Windows</span><span class="sxs-lookup"><span data-stu-id="9eeeb-904"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows System Resource Manager</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-905">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-905">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-906"><span id="Windows_Server_Backup_Features"></span><span id="windows_server_backup_features"></span><span id="WINDOWS_SERVER_BACKUP_FEATURES"></span>Copias de seguridad de Windows Server características</span><span class="sxs-lookup"><span data-stu-id="9eeeb-906"><span id="Windows_Server_Backup_Features"></span><span id="windows_server_backup_features"></span><span id="WINDOWS_SERVER_BACKUP_FEATURES"></span>Windows Server Backup Features</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-907">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-907">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-908"><span id="Remote_Assistance"></span><span id="remote_assistance"></span><span id="REMOTE_ASSISTANCE"></span>Asistencia remota</span><span class="sxs-lookup"><span data-stu-id="9eeeb-908"><span id="Remote_Assistance"></span><span id="remote_assistance"></span><span id="REMOTE_ASSISTANCE"></span>Remote Assistance</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-909">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-909">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-910"><span id="Telnet_Client"></span><span id="telnet_client"></span><span id="TELNET_CLIENT"></span>Cliente Telnet</span><span class="sxs-lookup"><span data-stu-id="9eeeb-910"><span id="Telnet_Client"></span><span id="telnet_client"></span><span id="TELNET_CLIENT"></span>Telnet Client</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-911">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-911">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-912"><span id="Telnet_Server"></span><span id="telnet_server"></span><span id="TELNET_SERVER"></span>Servidor Telnet</span><span class="sxs-lookup"><span data-stu-id="9eeeb-912"><span id="Telnet_Server"></span><span id="telnet_server"></span><span id="TELNET_SERVER"></span>Telnet Server</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-913">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-913">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-914"><span id="Subsystem_For_Unix-based_Applications"></span><span id="subsystem_for_unix-based_applications"></span><span id="SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>Subsystem for UNIX-Based Applications</span><span class="sxs-lookup"><span data-stu-id="9eeeb-914"><span id="Subsystem_For_Unix-based_Applications"></span><span id="subsystem_for_unix-based_applications"></span><span id="SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>Subsystem For Unix-based Applications</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-915">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-915">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-916"><span id="Windows_Internal_Database"></span><span id="windows_internal_database"></span><span id="WINDOWS_INTERNAL_DATABASE"></span>Windows Internal Database</span><span class="sxs-lookup"><span data-stu-id="9eeeb-916"><span id="Windows_Internal_Database"></span><span id="windows_internal_database"></span><span id="WINDOWS_INTERNAL_DATABASE"></span>Windows Internal Database</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-917">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-917">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-918"><span id="Storage_Manager_For_SANs"></span><span id="storage_manager_for_sans"></span><span id="STORAGE_MANAGER_FOR_SANS"></span>Administrador de almacenamiento para redes San</span><span class="sxs-lookup"><span data-stu-id="9eeeb-918"><span id="Storage_Manager_For_SANs"></span><span id="storage_manager_for_sans"></span><span id="STORAGE_MANAGER_FOR_SANS"></span>Storage Manager For SANs</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-919">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-919">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-920"><span id="Internet_Storage_Name_Server"></span><span id="internet_storage_name_server"></span><span id="INTERNET_STORAGE_NAME_SERVER"></span>Servidor de nombres de almacenamiento de Internet</span><span class="sxs-lookup"><span data-stu-id="9eeeb-920"><span id="Internet_Storage_Name_Server"></span><span id="internet_storage_name_server"></span><span id="INTERNET_STORAGE_NAME_SERVER"></span>Internet Storage Name Server</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-921">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-921">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-922"><span id="Multipath_I_O"></span><span id="multipath_i_o"></span><span id="MULTIPATH_I_O"></span>E/s de múltiples rutas</span><span class="sxs-lookup"><span data-stu-id="9eeeb-922"><span id="Multipath_I_O"></span><span id="multipath_i_o"></span><span id="MULTIPATH_I_O"></span>Multipath I/O</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-923">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-923">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-924"><span id="SNMP_Services"></span><span id="snmp_services"></span><span id="SNMP_SERVICES"></span>Servicios SNMP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-924"><span id="SNMP_Services"></span><span id="snmp_services"></span><span id="SNMP_SERVICES"></span>SNMP Services</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-925">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-925">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-926"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Servicios para Network File System</span><span class="sxs-lookup"><span data-stu-id="9eeeb-926"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Services For Network File System</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-927">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-927">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-928"><span id="Peer_Name_Resolution_Protocol"></span><span id="peer_name_resolution_protocol"></span><span id="PEER_NAME_RESOLUTION_PROTOCOL"></span>Protocolo de resolución de nombres de mismo nivel</span><span class="sxs-lookup"><span data-stu-id="9eeeb-928"><span id="Peer_Name_Resolution_Protocol"></span><span id="peer_name_resolution_protocol"></span><span id="PEER_NAME_RESOLUTION_PROTOCOL"></span>Peer Name Resolution Protocol</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-929">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-929">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-930"><span id="Remote_Server_Administration_Tools"></span><span id="remote_server_administration_tools"></span><span id="REMOTE_SERVER_ADMINISTRATION_TOOLS"></span>Herramientas de administración remota del servidor</span><span class="sxs-lookup"><span data-stu-id="9eeeb-930"><span id="Remote_Server_Administration_Tools"></span><span id="remote_server_administration_tools"></span><span id="REMOTE_SERVER_ADMINISTRATION_TOOLS"></span>Remote Server Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-931">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-931">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-932"><span id="Quality_Windows_Audio_Video_Experience"></span><span id="quality_windows_audio_video_experience"></span><span id="QUALITY_WINDOWS_AUDIO_VIDEO_EXPERIENCE"></span>Experiencia de calidad de audio y vídeo de Windows</span><span class="sxs-lookup"><span data-stu-id="9eeeb-932"><span id="Quality_Windows_Audio_Video_Experience"></span><span id="quality_windows_audio_video_experience"></span><span id="QUALITY_WINDOWS_AUDIO_VIDEO_EXPERIENCE"></span>Quality Windows Audio Video Experience</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-933">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-933">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-934"><span id="Group_Policy_Management"></span><span id="group_policy_management"></span><span id="GROUP_POLICY_MANAGEMENT"></span>Administración de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="9eeeb-934"><span id="Group_Policy_Management"></span><span id="group_policy_management"></span><span id="GROUP_POLICY_MANAGEMENT"></span>Group Policy Management</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-935">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-935">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-936"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Servicio de Index Server</span><span class="sxs-lookup"><span data-stu-id="9eeeb-936"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Indexing Service</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-937">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-937">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-938"><span id="File_Server_Resource_Manager__FSRM_"></span><span id="file_server_resource_manager__fsrm_"></span><span id="FILE_SERVER_RESOURCE_MANAGER__FSRM_"></span>Administrador de recursos de servidor de archivos (FSRM)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-938"><span id="File_Server_Resource_Manager__FSRM_"></span><span id="file_server_resource_manager__fsrm_"></span><span id="FILE_SERVER_RESOURCE_MANAGER__FSRM_"></span>File Server Resource Manager (FSRM)</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-939">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-939">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-940"><span id="Windows_Server_Migration_Tools"></span><span id="windows_server_migration_tools"></span><span id="WINDOWS_SERVER_MIGRATION_TOOLS"></span>Herramientas de migración de Windows Server</span><span class="sxs-lookup"><span data-stu-id="9eeeb-940"><span id="Windows_Server_Migration_Tools"></span><span id="windows_server_migration_tools"></span><span id="WINDOWS_SERVER_MIGRATION_TOOLS"></span>Windows Server Migration Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-941">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-941">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-942"><span id="BranchCache"></span><span id="branchcache"></span><span id="BRANCHCACHE"></span>BranchCache</span><span class="sxs-lookup"><span data-stu-id="9eeeb-942"><span id="BranchCache"></span><span id="branchcache"></span><span id="BRANCHCACHE"></span>BranchCache</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-943">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-943">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-944"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>Consola de administración de DirectAccess</span><span class="sxs-lookup"><span data-stu-id="9eeeb-944"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>DirectAccess Management Console</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-945">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-945">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-946"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Servicio de transferencia inteligente en segundo plano (BITS)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-946"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Background Intelligent Transfer Service (BITS)</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-947">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-947">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-948"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>Compatibilidad con WoW64</span><span class="sxs-lookup"><span data-stu-id="9eeeb-948"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>WoW64 Support</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-949">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-949">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-950"><span id="Window_Server_Update_Services"></span><span id="window_server_update_services"></span><span id="WINDOW_SERVER_UPDATE_SERVICES"></span>Servicios de actualización de Windows Server</span><span class="sxs-lookup"><span data-stu-id="9eeeb-950"><span id="Window_Server_Update_Services"></span><span id="window_server_update_services"></span><span id="WINDOW_SERVER_UPDATE_SERVICES"></span>Window Server Update Services</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-951">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-951">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-952"><span id="IP_Address_Management__IPAM__Server"></span><span id="ip_address_management__ipam__server"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>Servidor de administración de direcciones IP (IPAM)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-952"><span id="IP_Address_Management__IPAM__Server"></span><span id="ip_address_management__ipam__server"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>IP Address Management (IPAM) Server</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-953">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-953">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-954"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-954"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-955">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-955">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-956"><span id=".NET_Framework_4.5"></span><span id=".net_framework_4.5"></span><span id=".NET_FRAMEWORK_4.5"></span>.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="9eeeb-956"><span id=".NET_Framework_4.5"></span><span id=".net_framework_4.5"></span><span id=".NET_FRAMEWORK_4.5"></span>.NET Framework 4.5</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-957">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-957">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-958"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Search Service de Windows</span><span class="sxs-lookup"><span data-stu-id="9eeeb-958"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Search Service</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-959">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-959">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-960"><span id="Client_for_NFS"></span><span id="client_for_nfs"></span><span id="CLIENT_FOR_NFS"></span>Cliente para NFS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-960"><span id="Client_for_NFS"></span><span id="client_for_nfs"></span><span id="CLIENT_FOR_NFS"></span>Client for NFS</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-961">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-961">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-962"><span id="BitLocker_Network_Unlock"></span><span id="bitlocker_network_unlock"></span><span id="BITLOCKER_NETWORK_UNLOCK"></span>Desbloqueo de red de BitLocker</span><span class="sxs-lookup"><span data-stu-id="9eeeb-962"><span id="BitLocker_Network_Unlock"></span><span id="bitlocker_network_unlock"></span><span id="BITLOCKER_NETWORK_UNLOCK"></span>BitLocker Network Unlock</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-963">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-963">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-964"><span id="Management_OData_IIS_Extension"></span><span id="management_odata_iis_extension"></span><span id="MANAGEMENT_ODATA_IIS_EXTENSION"></span>Extensión IIS Management OData</span><span class="sxs-lookup"><span data-stu-id="9eeeb-964"><span id="Management_OData_IIS_Extension"></span><span id="management_odata_iis_extension"></span><span id="MANAGEMENT_ODATA_IIS_EXTENSION"></span>Management OData IIS Extension</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-965">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-965">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-966"><span id=".NET_Framework_4.5_Advanced_Services"></span><span id=".net_framework_4.5_advanced_services"></span><span id=".NET_FRAMEWORK_4.5_ADVANCED_SERVICES"></span>.NET Framework 4,5 Advanced Services</span><span class="sxs-lookup"><span data-stu-id="9eeeb-966"><span id=".NET_Framework_4.5_Advanced_Services"></span><span id=".net_framework_4.5_advanced_services"></span><span id=".NET_FRAMEWORK_4.5_ADVANCED_SERVICES"></span>.NET Framework 4.5 Advanced Services</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-967">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-967">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-968"><span id=".NET_Framework_4.5_Features"></span><span id=".net_framework_4.5_features"></span><span id=".NET_FRAMEWORK_4.5_FEATURES"></span>.NET Framework características 4,5</span><span class="sxs-lookup"><span data-stu-id="9eeeb-968"><span id=".NET_Framework_4.5_Features"></span><span id=".net_framework_4.5_features"></span><span id=".NET_FRAMEWORK_4.5_FEATURES"></span>.NET Framework 4.5 Features</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-969">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-969">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-970"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Infraestructura e interfaces de usuario</span><span class="sxs-lookup"><span data-stu-id="9eeeb-970"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>User Interfaces and Infrastructure</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-971">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-971">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-972"><span id="Graphical_Management_Tools_and_Infrastructure"></span><span id="graphical_management_tools_and_infrastructure"></span><span id="GRAPHICAL_MANAGEMENT_TOOLS_AND_INFRASTRUCTURE"></span>Infraestructura y herramientas de administración de gráficos</span><span class="sxs-lookup"><span data-stu-id="9eeeb-972"><span id="Graphical_Management_Tools_and_Infrastructure"></span><span id="graphical_management_tools_and_infrastructure"></span><span id="GRAPHICAL_MANAGEMENT_TOOLS_AND_INFRASTRUCTURE"></span>Graphical Management Tools and Infrastructure</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-973">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-973">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-974"><span id="File_and_Storage_Services"></span><span id="file_and_storage_services"></span><span id="FILE_AND_STORAGE_SERVICES"></span>Servicios de archivos y almacenamiento</span><span class="sxs-lookup"><span data-stu-id="9eeeb-974"><span id="File_and_Storage_Services"></span><span id="file_and_storage_services"></span><span id="FILE_AND_STORAGE_SERVICES"></span>File and Storage Services</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-975">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-975">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-976"><span id="Windows_Server_Essentials_Experience"></span><span id="windows_server_essentials_experience"></span><span id="WINDOWS_SERVER_ESSENTIALS_EXPERIENCE"></span>Experiencia con Windows Server Essentials</span><span class="sxs-lookup"><span data-stu-id="9eeeb-976"><span id="Windows_Server_Essentials_Experience"></span><span id="windows_server_essentials_experience"></span><span id="WINDOWS_SERVER_ESSENTIALS_EXPERIENCE"></span>Windows Server Essentials Experience</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-977">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-977">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-978"><span id="Direct_Play"></span><span id="direct_play"></span><span id="DIRECT_PLAY"></span>Reproducción directa</span><span class="sxs-lookup"><span data-stu-id="9eeeb-978"><span id="Direct_Play"></span><span id="direct_play"></span><span id="DIRECT_PLAY"></span>Direct Play</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-979">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-979">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-980"><span id="Distributed_File_System"></span><span id="distributed_file_system"></span><span id="DISTRIBUTED_FILE_SYSTEM"></span>Sistema de archivos distribuido</span><span class="sxs-lookup"><span data-stu-id="9eeeb-980"><span id="Distributed_File_System"></span><span id="distributed_file_system"></span><span id="DISTRIBUTED_FILE_SYSTEM"></span>Distributed File System</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-981">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-981">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-982"><span id="File_Server_Resource_Manager"></span><span id="file_server_resource_manager"></span><span id="FILE_SERVER_RESOURCE_MANAGER"></span>Administrador de recursos de servidor de archivos</span><span class="sxs-lookup"><span data-stu-id="9eeeb-982"><span id="File_Server_Resource_Manager"></span><span id="file_server_resource_manager"></span><span id="FILE_SERVER_RESOURCE_MANAGER"></span>File Server Resource Manager</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-983">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-983">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-984"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Servicios para Network File System</span><span class="sxs-lookup"><span data-stu-id="9eeeb-984"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Services For Network File System</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-985">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-985">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-986"><span id="Single_Instance_Storage"></span><span id="single_instance_storage"></span><span id="SINGLE_INSTANCE_STORAGE"></span>Almacenamiento de instancia única</span><span class="sxs-lookup"><span data-stu-id="9eeeb-986"><span id="Single_Instance_Storage"></span><span id="single_instance_storage"></span><span id="SINGLE_INSTANCE_STORAGE"></span>Single Instance Storage</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-987">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-987">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-988"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Search Service de Windows</span><span class="sxs-lookup"><span data-stu-id="9eeeb-988"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Search Service</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-989">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-989">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-990"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Servicio de Index Server</span><span class="sxs-lookup"><span data-stu-id="9eeeb-990"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Indexing Service</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-991">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-991">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-992"><span id="iSCSI_Target_Storage_Provider__VDS_and_VSS_hardware_providers_"></span><span id="iscsi_target_storage_provider__vds_and_vss_hardware_providers_"></span><span id="ISCSI_TARGET_STORAGE_PROVIDER__VDS_AND_VSS_HARDWARE_PROVIDERS_"></span>Proveedor de almacenamiento del destino iSCSI (proveedores de hardware de VDS y VSS)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-992"><span id="iSCSI_Target_Storage_Provider__VDS_and_VSS_hardware_providers_"></span><span id="iscsi_target_storage_provider__vds_and_vss_hardware_providers_"></span><span id="ISCSI_TARGET_STORAGE_PROVIDER__VDS_AND_VSS_HARDWARE_PROVIDERS_"></span>iSCSI Target Storage Provider (VDS and VSS hardware providers)</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-993">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-993">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-994"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Carpetas de trabajo</span><span class="sxs-lookup"><span data-stu-id="9eeeb-994"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Work Folders</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-995">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-995">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-996"><span id="Active_Directory_Domain_Controller"></span><span id="active_directory_domain_controller"></span><span id="ACTIVE_DIRECTORY_DOMAIN_CONTROLLER"></span>Controlador de Dominio de Active Directory</span><span class="sxs-lookup"><span data-stu-id="9eeeb-996"><span id="Active_Directory_Domain_Controller"></span><span id="active_directory_domain_controller"></span><span id="ACTIVE_DIRECTORY_DOMAIN_CONTROLLER"></span>Active Directory Domain Controller</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-997">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-997">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-998"><span id="Identity_Management_For_Unix"></span><span id="identity_management_for_unix"></span><span id="IDENTITY_MANAGEMENT_FOR_UNIX"></span>Administración de identidades para UNIX</span><span class="sxs-lookup"><span data-stu-id="9eeeb-998"><span id="Identity_Management_For_Unix"></span><span id="identity_management_for_unix"></span><span id="IDENTITY_MANAGEMENT_FOR_UNIX"></span>Identity Management For Unix</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-999">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-999">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1000"><span id="Server_For_Network_Information_Services"></span><span id="server_for_network_information_services"></span><span id="SERVER_FOR_NETWORK_INFORMATION_SERVICES"></span>Servidor para servicios de información de red</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1000"><span id="Server_For_Network_Information_Services"></span><span id="server_for_network_information_services"></span><span id="SERVER_FOR_NETWORK_INFORMATION_SERVICES"></span>Server For Network Information Services</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1001">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1001">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1002"><span id="Password_Synchronization"></span><span id="password_synchronization"></span><span id="PASSWORD_SYNCHRONIZATION"></span>Sincronización de contraseñas</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1002"><span id="Password_Synchronization"></span><span id="password_synchronization"></span><span id="PASSWORD_SYNCHRONIZATION"></span>Password Synchronization</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1003">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1003">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1004"><span id="Administration_Tools"></span><span id="administration_tools"></span><span id="ADMINISTRATION_TOOLS"></span>Herramientas de administración</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1004"><span id="Administration_Tools"></span><span id="administration_tools"></span><span id="ADMINISTRATION_TOOLS"></span>Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1005">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1005">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1006"><span id="Windows_Media_Server"></span><span id="windows_media_server"></span><span id="WINDOWS_MEDIA_SERVER"></span>Servidor de Windows Media</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1006"><span id="Windows_Media_Server"></span><span id="windows_media_server"></span><span id="WINDOWS_MEDIA_SERVER"></span>Windows Media Server</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1007">Ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1007">No longer supported.</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1008"><span id="Web-based_Administration"></span><span id="web-based_administration"></span><span id="WEB-BASED_ADMINISTRATION"></span>Administración basada en Web</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1008"><span id="Web-based_Administration"></span><span id="web-based_administration"></span><span id="WEB-BASED_ADMINISTRATION"></span>Web-based Administration</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1009">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1009">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1010"><span id="Logging_Agent"></span><span id="logging_agent"></span><span id="LOGGING_AGENT"></span>Agente de registro</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1010"><span id="Logging_Agent"></span><span id="logging_agent"></span><span id="LOGGING_AGENT"></span>Logging Agent</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1011">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1011">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1012"><span id="Federation_Service"></span><span id="federation_service"></span><span id="FEDERATION_SERVICE"></span>Servicio de federación</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1012"><span id="Federation_Service"></span><span id="federation_service"></span><span id="FEDERATION_SERVICE"></span>Federation Service</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1013">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1013">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1014"><span id="Federation_Service_Policy"></span><span id="federation_service_policy"></span><span id="FEDERATION_SERVICE_POLICY"></span>Directiva de Servicio de federación</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1014"><span id="Federation_Service_Policy"></span><span id="federation_service_policy"></span><span id="FEDERATION_SERVICE_POLICY"></span>Federation Service Policy</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1015">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1015">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1016"><span id="AD_FS_Web_Agents"></span><span id="ad_fs_web_agents"></span><span id="AD_FS_WEB_AGENTS"></span>AD FS agentes Web</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1016"><span id="AD_FS_Web_Agents"></span><span id="ad_fs_web_agents"></span><span id="AD_FS_WEB_AGENTS"></span>AD FS Web Agents</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1017">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1017">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1018"><span id="Windows_Token-based_Agent"></span><span id="windows_token-based_agent"></span><span id="WINDOWS_TOKEN-BASED_AGENT"></span>Agente basado en tokens de Windows</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1018"><span id="Windows_Token-based_Agent"></span><span id="windows_token-based_agent"></span><span id="WINDOWS_TOKEN-BASED_AGENT"></span>Windows Token-based Agent</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1019">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1019">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1020"><span id="Remote_Desktop_Licensing"></span><span id="remote_desktop_licensing"></span><span id="REMOTE_DESKTOP_LICENSING"></span>Licencias de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1020"><span id="Remote_Desktop_Licensing"></span><span id="remote_desktop_licensing"></span><span id="REMOTE_DESKTOP_LICENSING"></span>Remote Desktop Licensing</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1021">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1021">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1022"><span id="Network_Policy_Server"></span><span id="network_policy_server"></span><span id="NETWORK_POLICY_SERVER"></span>Servidor de directivas de redes</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1022"><span id="Network_Policy_Server"></span><span id="network_policy_server"></span><span id="NETWORK_POLICY_SERVER"></span>Network Policy Server</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1023">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1023">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1024"><span id="VPN"></span><span id="vpn"></span>PRIVADA</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1024"><span id="VPN"></span><span id="vpn"></span>VPN</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1025">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1025">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1026"><span id="Remote_Access_Services"></span><span id="remote_access_services"></span><span id="REMOTE_ACCESS_SERVICES"></span>Servicios de acceso remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1026"><span id="Remote_Access_Services"></span><span id="remote_access_services"></span><span id="REMOTE_ACCESS_SERVICES"></span>Remote Access Services</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1027">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1027">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1028"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Automático</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1028"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Routing</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1029">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1029">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1030"><span id="Health_Registration_Authority"></span><span id="health_registration_authority"></span><span id="HEALTH_REGISTRATION_AUTHORITY"></span>Autoridad de registro de mantenimiento</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1030"><span id="Health_Registration_Authority"></span><span id="health_registration_authority"></span><span id="HEALTH_REGISTRATION_AUTHORITY"></span>Health Registration Authority</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1031">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1031">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1032"><span id="Host_Credential_Authorization_Protocol"></span><span id="host_credential_authorization_protocol"></span><span id="HOST_CREDENTIAL_AUTHORIZATION_PROTOCOL"></span>Protocolo de autorización de credenciales de host</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1032"><span id="Host_Credential_Authorization_Protocol"></span><span id="host_credential_authorization_protocol"></span><span id="HOST_CREDENTIAL_AUTHORIZATION_PROTOCOL"></span>Host Credential Authorization Protocol</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1033">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1033">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1034"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1034"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1035">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1035">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1036"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>Visor de XPS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1036"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS Viewer</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1037">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1037">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1038"><span id="SNMP_Service"></span><span id="snmp_service"></span><span id="SNMP_SERVICE"></span>Servicio SNMP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1038"><span id="SNMP_Service"></span><span id="snmp_service"></span><span id="SNMP_SERVICE"></span>SNMP Service</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1039">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1039">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1040"><span id="SNMP_WMI_Provider"></span><span id="snmp_wmi_provider"></span><span id="SNMP_WMI_PROVIDER"></span>Proveedor WMI de SNMP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1040"><span id="SNMP_WMI_Provider"></span><span id="snmp_wmi_provider"></span><span id="SNMP_WMI_PROVIDER"></span>SNMP WMI Provider</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1041">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1041">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1042"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1042"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1043">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1043">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1044"><span id="Web_Server__IIS__Support"></span><span id="web_server__iis__support"></span><span id="WEB_SERVER__IIS__SUPPORT"></span>Compatibilidad con servidor Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1044"><span id="Web_Server__IIS__Support"></span><span id="web_server__iis__support"></span><span id="WEB_SERVER__IIS__SUPPORT"></span>Web Server (IIS) Support</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1045">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1045">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1046"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>Acceso de red COM+</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1046"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>COM+ Network Access</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1047">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1047">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1048"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>Uso compartido de puertos TCP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1048"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>TCP Port Sharing</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1049">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1049">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1050"><span id="Windows_Process_Activation_Service_Support"></span><span id="windows_process_activation_service_support"></span><span id="WINDOWS_PROCESS_ACTIVATION_SERVICE_SUPPORT"></span>Compatibilidad con el servicio de activación de procesos de Windows</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1050"><span id="Windows_Process_Activation_Service_Support"></span><span id="windows_process_activation_service_support"></span><span id="WINDOWS_PROCESS_ACTIVATION_SERVICE_SUPPORT"></span>Windows Process Activation Service Support</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1051">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1051">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1052"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>Activación HTTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1052"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>HTTP Activation</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1053">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1053">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1054"><span id="Message_Queuing_Activation"></span><span id="message_queuing_activation"></span><span id="MESSAGE_QUEUING_ACTIVATION"></span>Activación de Message Queue Server</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1054"><span id="Message_Queuing_Activation"></span><span id="message_queuing_activation"></span><span id="MESSAGE_QUEUING_ACTIVATION"></span>Message Queuing Activation</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1055">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1055">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1056"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>Activación de TCP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1056"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>TCP Activation</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1057">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1057">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1058"><span id="Named_Pipes_Activation"></span><span id="named_pipes_activation"></span><span id="NAMED_PIPES_ACTIVATION"></span>Activación de canalizaciones con nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1058"><span id="Named_Pipes_Activation"></span><span id="named_pipes_activation"></span><span id="NAMED_PIPES_ACTIVATION"></span>Named Pipes Activation</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1059">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1059">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1060"><span id="Distributed_Transactions"></span><span id="distributed_transactions"></span><span id="DISTRIBUTED_TRANSACTIONS"></span>Transacciones distribuidas</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1060"><span id="Distributed_Transactions"></span><span id="distributed_transactions"></span><span id="DISTRIBUTED_TRANSACTIONS"></span>Distributed Transactions</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1061">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1061">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1062"><span id="Incoming_Remote_Transactions"></span><span id="incoming_remote_transactions"></span><span id="INCOMING_REMOTE_TRANSACTIONS"></span>Transacciones remotas entrantes</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1062"><span id="Incoming_Remote_Transactions"></span><span id="incoming_remote_transactions"></span><span id="INCOMING_REMOTE_TRANSACTIONS"></span>Incoming Remote Transactions</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1063">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1063">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1064"><span id="Outgoing_Remote_Transactions"></span><span id="outgoing_remote_transactions"></span><span id="OUTGOING_REMOTE_TRANSACTIONS"></span>Transacciones remotas salientes</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1064"><span id="Outgoing_Remote_Transactions"></span><span id="outgoing_remote_transactions"></span><span id="OUTGOING_REMOTE_TRANSACTIONS"></span>Outgoing Remote Transactions</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1065">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1065">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1066"><span id="WS-Automatic_Transactions"></span><span id="ws-automatic_transactions"></span><span id="WS-AUTOMATIC_TRANSACTIONS"></span>Transacciones WS-Automatic</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1066"><span id="WS-Automatic_Transactions"></span><span id="ws-automatic_transactions"></span><span id="WS-AUTOMATIC_TRANSACTIONS"></span>WS-Automatic Transactions</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1067">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1067">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1068"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Extensiones de servidor de aplicaciones para .NET 4,0</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1068"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Application Server Extensions for .NET 4.0</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1069">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1069">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1070"><span id="Role_Administration_Tools"></span><span id="role_administration_tools"></span><span id="ROLE_ADMINISTRATION_TOOLS"></span>Herramientas de administración de roles</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1070"><span id="Role_Administration_Tools"></span><span id="role_administration_tools"></span><span id="ROLE_ADMINISTRATION_TOOLS"></span>Role Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1071">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1071">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1072"><span id="AD_DS_Tools"></span><span id="ad_ds_tools"></span><span id="AD_DS_TOOLS"></span>Herramientas de AD DS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1072"><span id="AD_DS_Tools"></span><span id="ad_ds_tools"></span><span id="AD_DS_TOOLS"></span>AD DS Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1073">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1073">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1074"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_lds_snap-ins_and_command-line_tools"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD LDS herramientas de Snap-Ins y Command-Line</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1074"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_lds_snap-ins_and_command-line_tools"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD LDS Snap-Ins and Command-Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1075">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1075">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1076"><span id="Network_Policy_and_Access_Services"></span><span id="network_policy_and_access_services"></span><span id="NETWORK_POLICY_AND_ACCESS_SERVICES"></span>Servicios de acceso y directivas de redes</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1076"><span id="Network_Policy_and_Access_Services"></span><span id="network_policy_and_access_services"></span><span id="NETWORK_POLICY_AND_ACCESS_SERVICES"></span>Network Policy and Access Services</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1077">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1077">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1078"><span id="Active_Directory_Rights_Management_Services"></span><span id="active_directory_rights_management_services"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES"></span>Active Directory Rights Management Services</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1078"><span id="Active_Directory_Rights_Management_Services"></span><span id="active_directory_rights_management_services"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES"></span>Active Directory Rights Management Services</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1079">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1079">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1080"><span id="Remote_Desktop_Services_Tools"></span><span id="remote_desktop_services_tools"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS"></span>Herramientas de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1080"><span id="Remote_Desktop_Services_Tools"></span><span id="remote_desktop_services_tools"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS"></span>Remote Desktop Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1081">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1081">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1082"><span id="Feature_Administration_Tools"></span><span id="feature_administration_tools"></span><span id="FEATURE_ADMINISTRATION_TOOLS"></span>Herramientas de administración de características</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1082"><span id="Feature_Administration_Tools"></span><span id="feature_administration_tools"></span><span id="FEATURE_ADMINISTRATION_TOOLS"></span>Feature Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1083">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1083">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1084"><span id="Failover_Clustering_Tools"></span><span id="failover_clustering_tools"></span><span id="FAILOVER_CLUSTERING_TOOLS"></span>Herramientas de clúster de conmutación por error</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1084"><span id="Failover_Clustering_Tools"></span><span id="failover_clustering_tools"></span><span id="FAILOVER_CLUSTERING_TOOLS"></span>Failover Clustering Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1085">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1085">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1086"><span id="DNS_Server_Tools"></span><span id="dns_server_tools"></span><span id="DNS_SERVER_TOOLS"></span>Herramientas del servidor DNS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1086"><span id="DNS_Server_Tools"></span><span id="dns_server_tools"></span><span id="DNS_SERVER_TOOLS"></span>DNS Server Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1087">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1087">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1088"><span id="Services_For_Network_File_System_Tools"></span><span id="services_for_network_file_system_tools"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM_TOOLS"></span>Servicios para herramientas del sistema de archivos de red</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1088"><span id="Services_For_Network_File_System_Tools"></span><span id="services_for_network_file_system_tools"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM_TOOLS"></span>Services For Network File System Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1089">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1089">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1090"><span id="Web_Server__IIS__Tools"></span><span id="web_server__iis__tools"></span><span id="WEB_SERVER__IIS__TOOLS"></span>Herramientas del servidor Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1090"><span id="Web_Server__IIS__Tools"></span><span id="web_server__iis__tools"></span><span id="WEB_SERVER__IIS__TOOLS"></span>Web Server (IIS) Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1091">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1091">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1092"><span id="Server_for_NIS_Tools"></span><span id="server_for_nis_tools"></span><span id="SERVER_FOR_NIS_TOOLS"></span>Herramientas de Servidor para NIS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1092"><span id="Server_for_NIS_Tools"></span><span id="server_for_nis_tools"></span><span id="SERVER_FOR_NIS_TOOLS"></span>Server for NIS Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1093">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1093">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1094"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_ds_snap-ins_and_command-line_tools"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD DS herramientas de Snap-Ins y Command-Line</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1094"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_ds_snap-ins_and_command-line_tools"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD DS Snap-Ins and Command-Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1095">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1095">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1096"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Herramientas de AD DS y AD LDS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1096"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS and AD LDS Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1097">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1097">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1098"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Herramientas de Conexión a Escritorio remoto Broker</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1098"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Remote Desktop Connection Broker Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1099">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1099">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1100"><span id="IP_Address_Management__IPAM__Client"></span><span id="ip_address_management__ipam__client"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__CLIENT"></span>Cliente de administración de direcciones IP (IPAM)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1100"><span id="IP_Address_Management__IPAM__Client"></span><span id="ip_address_management__ipam__client"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__CLIENT"></span>IP Address Management (IPAM) Client</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1101">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1101">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1102"><span id="Hyper-V_Module_for_Windows_PowerShell"></span><span id="hyper-v_module_for_windows_powershell"></span><span id="HYPER-V_MODULE_FOR_WINDOWS_POWERSHELL"></span>Módulo de Hyper-V para Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1102"><span id="Hyper-V_Module_for_Windows_PowerShell"></span><span id="hyper-v_module_for_windows_powershell"></span><span id="HYPER-V_MODULE_FOR_WINDOWS_POWERSHELL"></span>Hyper-V Module for Windows PowerShell</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9eeeb-1103"><span id="Active_Directory_Rights_Management_Services_Tool"></span><span id="active_directory_rights_management_services_tool"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOL"></span>Herramienta de Active Directory Rights Management Services</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1103"><span id="Active_Directory_Rights_Management_Services_Tool"></span><span id="active_directory_rights_management_services_tool"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOL"></span>Active Directory Rights Management Services Tool</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1104">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1104">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1105"><span id="Share_and_Storage_Management_Tool"></span><span id="share_and_storage_management_tool"></span><span id="SHARE_AND_STORAGE_MANAGEMENT_TOOL"></span>Herramienta de administración de almacenamiento y recursos compartidos</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1105"><span id="Share_and_Storage_Management_Tool"></span><span id="share_and_storage_management_tool"></span><span id="SHARE_AND_STORAGE_MANAGEMENT_TOOL"></span>Share and Storage Management Tool</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1106">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1106">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1107"><span id="Remote_Access_Management_Tools"></span><span id="remote_access_management_tools"></span><span id="REMOTE_ACCESS_MANAGEMENT_TOOLS"></span>Herramientas de administración de acceso remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1107"><span id="Remote_Access_Management_Tools"></span><span id="remote_access_management_tools"></span><span id="REMOTE_ACCESS_MANAGEMENT_TOOLS"></span>Remote Access Management Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1108">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1108">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1109"><span id="Remote_Access_module_for_Windows_PowerShell"></span><span id="remote_access_module_for_windows_powershell"></span><span id="REMOTE_ACCESS_MODULE_FOR_WINDOWS_POWERSHELL"></span>Módulo de acceso remoto para Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1109"><span id="Remote_Access_module_for_Windows_PowerShell"></span><span id="remote_access_module_for_windows_powershell"></span><span id="REMOTE_ACCESS_MODULE_FOR_WINDOWS_POWERSHELL"></span>Remote Access module for Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1110">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1110">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1111"><span id="Remote_Access_GUI_and_Command-Line_Tools"></span><span id="remote_access_gui_and_command-line_tools"></span><span id="REMOTE_ACCESS_GUI_AND_COMMAND-LINE_TOOLS"></span>Herramientas de Command-Line y GUI de acceso remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1111"><span id="Remote_Access_GUI_and_Command-Line_Tools"></span><span id="remote_access_gui_and_command-line_tools"></span><span id="REMOTE_ACCESS_GUI_AND_COMMAND-LINE_TOOLS"></span>Remote Access GUI and Command-Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1112">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1112">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1113"><span id="Windows_Server_Update_Services_Tools"></span><span id="windows_server_update_services_tools"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES_TOOLS"></span>Herramientas de Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1113"><span id="Windows_Server_Update_Services_Tools"></span><span id="windows_server_update_services_tools"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES_TOOLS"></span>Windows Server Update Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1114">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1114">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1115"><span id="Remote_Desktop_Licensing_Diagnoser_Tools"></span><span id="remote_desktop_licensing_diagnoser_tools"></span><span id="REMOTE_DESKTOP_LICENSING_DIAGNOSER_TOOLS"></span>Herramientas del diagnóstico de licencias de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1115"><span id="Remote_Desktop_Licensing_Diagnoser_Tools"></span><span id="remote_desktop_licensing_diagnoser_tools"></span><span id="REMOTE_DESKTOP_LICENSING_DIAGNOSER_TOOLS"></span>Remote Desktop Licensing Diagnoser Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1116">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1116">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1117"><span id="SNMP_Tools"></span><span id="snmp_tools"></span><span id="SNMP_TOOLS"></span>Herramientas de SNMP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1117"><span id="SNMP_Tools"></span><span id="snmp_tools"></span><span id="SNMP_TOOLS"></span>SNMP Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1118">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1118">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1119"><span id="Volume_Activation_Tools"></span><span id="volume_activation_tools"></span><span id="VOLUME_ACTIVATION_TOOLS"></span>Herramientas de activación de volumen</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1119"><span id="Volume_Activation_Tools"></span><span id="volume_activation_tools"></span><span id="VOLUME_ACTIVATION_TOOLS"></span>Volume Activation Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1120">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1120">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1121"><span id="Windows_Server_Backup"></span><span id="windows_server_backup"></span><span id="WINDOWS_SERVER_BACKUP"></span>Copias de seguridad de Windows Server</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1121"><span id="Windows_Server_Backup"></span><span id="windows_server_backup"></span><span id="WINDOWS_SERVER_BACKUP"></span>Windows Server Backup</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1122">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1122">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1123"><span id="Command_Line_Tools"></span><span id="command_line_tools"></span><span id="COMMAND_LINE_TOOLS"></span>Herramientas de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1123"><span id="Command_Line_Tools"></span><span id="command_line_tools"></span><span id="COMMAND_LINE_TOOLS"></span>Command Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1124">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1124">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1125"><span id="Ink_Support"></span><span id="ink_support"></span><span id="INK_SUPPORT"></span>Compatibilidad con entradas manuscritas</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1125"><span id="Ink_Support"></span><span id="ink_support"></span><span id="INK_SUPPORT"></span>Ink Support</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1126">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1126">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1127"><span id="Handwriting_Recognition"></span><span id="handwriting_recognition"></span><span id="HANDWRITING_RECOGNITION"></span>Reconocimiento de escritura a mano</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1127"><span id="Handwriting_Recognition"></span><span id="handwriting_recognition"></span><span id="HANDWRITING_RECOGNITION"></span>Handwriting Recognition</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1128">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1128">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1129"><span id="Compact_Server"></span><span id="compact_server"></span><span id="COMPACT_SERVER"></span>Servidor compacto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1129"><span id="Compact_Server"></span><span id="compact_server"></span><span id="COMPACT_SERVER"></span>Compact Server</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1130">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1130">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1131"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1131"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1132">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1132">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1133"><span id="WoW64_for_.NET_Framework_2.0_and___________"></span><span id="wow64_for_.net_framework_2.0_and___________"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND___________"></span>WoW64 para .NET Framework 2,0 y PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1133"><span id="WoW64_for_.NET_Framework_2.0_and___________"></span><span id="wow64_for_.net_framework_2.0_and___________"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND___________"></span>WoW64 for .NET Framework 2.0 and PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1134">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1134">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1135"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 para .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1135"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 for .NET Framework 2.0</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1136">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1136">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1137"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 para PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1137"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 for PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1138">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1138">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1139"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 para .NET Framework 3,0 y 3,5</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1139"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 for .NET Framework 3.0 and 3.5</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1140">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1140">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1141"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 para servicios de impresión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1141"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 for Print Services</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1142">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1142">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1143"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 para clúster de conmutación por error</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1143"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 for Failover Clustering</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1144">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1144">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1145"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 para el editor de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1145"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 for Input Method Editor</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1146">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1146">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1147"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 para Subsystem for UNIX-Based Applications</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1147"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 for Subsystem for UNIX-based Applications</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1148">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1148">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1149"><span id="Desktop_Experience"></span><span id="desktop_experience"></span><span id="DESKTOP_EXPERIENCE"></span>Experiencia de escritorio</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1149"><span id="Desktop_Experience"></span><span id="desktop_experience"></span><span id="DESKTOP_EXPERIENCE"></span>Desktop Experience</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1150">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1150">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1151"><span id="Server_Graphical_Shell"></span><span id="server_graphical_shell"></span><span id="SERVER_GRAPHICAL_SHELL"></span>Shell gráfico de servidor</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1151"><span id="Server_Graphical_Shell"></span><span id="server_graphical_shell"></span><span id="SERVER_GRAPHICAL_SHELL"></span>Server Graphical Shell</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1152">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1152">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1153"><span id="API_and_PowerShell_cmdlets"></span><span id="api_and_powershell_cmdlets"></span><span id="API_AND_POWERSHELL_CMDLETS"></span>API y cmdlets de PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1153"><span id="API_and_PowerShell_cmdlets"></span><span id="api_and_powershell_cmdlets"></span><span id="API_AND_POWERSHELL_CMDLETS"></span>API and PowerShell cmdlets</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1154">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1154">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1155"><span id="SQL_Server_Connectivity"></span><span id="sql_server_connectivity"></span><span id="SQL_SERVER_CONNECTIVITY"></span>Conectividad SQL Server</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1155"><span id="SQL_Server_Connectivity"></span><span id="sql_server_connectivity"></span><span id="SQL_SERVER_CONNECTIVITY"></span>SQL Server Connectivity</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1156">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1156">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1157"><span id="WSUS_Services"></span><span id="wsus_services"></span><span id="WSUS_SERVICES"></span>Servicios WSUS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1157"><span id="WSUS_Services"></span><span id="wsus_services"></span><span id="WSUS_SERVICES"></span>WSUS Services</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1158">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1158">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1159"><span id="User_Interface_Management_Console"></span><span id="user_interface_management_console"></span><span id="USER_INTERFACE_MANAGEMENT_CONSOLE"></span>Consola de administración de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1159"><span id="User_Interface_Management_Console"></span><span id="user_interface_management_console"></span><span id="USER_INTERFACE_MANAGEMENT_CONSOLE"></span>User Interface Management Console</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1160">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1160">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1161"><span id="WID_Connectivity"></span><span id="wid_connectivity"></span><span id="WID_CONNECTIVITY"></span>Conectividad WID</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1161"><span id="WID_Connectivity"></span><span id="wid_connectivity"></span><span id="WID_CONNECTIVITY"></span>WID Connectivity</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1162">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1162">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1163"><span id="Windows_PowerShell_2.0_Engine"></span><span id="windows_powershell_2.0_engine"></span><span id="WINDOWS_POWERSHELL_2.0_ENGINE"></span>Motor 2,0 de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1163"><span id="Windows_PowerShell_2.0_Engine"></span><span id="windows_powershell_2.0_engine"></span><span id="WINDOWS_POWERSHELL_2.0_ENGINE"></span>Windows PowerShell 2.0 Engine</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1164">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1164">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1165"><span id="Windows_PowerShell_3.0"></span><span id="windows_powershell_3.0"></span><span id="WINDOWS_POWERSHELL_3.0"></span>Windows PowerShell 3,0</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1165"><span id="Windows_PowerShell_3.0"></span><span id="windows_powershell_3.0"></span><span id="WINDOWS_POWERSHELL_3.0"></span>Windows PowerShell 3.0</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1166">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1166">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1167"><span id="Windows_PowerShell_Web_Access"></span><span id="windows_powershell_web_access"></span><span id="WINDOWS_POWERSHELL_WEB_ACCESS"></span>Windows PowerShell Web Access</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1167"><span id="Windows_PowerShell_Web_Access"></span><span id="windows_powershell_web_access"></span><span id="WINDOWS_POWERSHELL_WEB_ACCESS"></span>Windows PowerShell Web Access</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1168">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1168">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1169"><span id="Windows_PowerShell_Desired_State_Configuration_Service"></span><span id="windows_powershell_desired_state_configuration_service"></span><span id="WINDOWS_POWERSHELL_DESIRED_STATE_CONFIGURATION_SERVICE"></span>Servicio de configuración de estado deseado de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1169"><span id="Windows_PowerShell_Desired_State_Configuration_Service"></span><span id="windows_powershell_desired_state_configuration_service"></span><span id="WINDOWS_POWERSHELL_DESIRED_STATE_CONFIGURATION_SERVICE"></span>Windows PowerShell Desired State Configuration Service</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1170">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1170">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1171"><span id=".NET_Framework_4.5_Extended"></span><span id=".net_framework_4.5_extended"></span><span id=".NET_FRAMEWORK_4.5_EXTENDED"></span>.NET Framework 4,5 extendido</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1171"><span id=".NET_Framework_4.5_Extended"></span><span id=".net_framework_4.5_extended"></span><span id=".NET_FRAMEWORK_4.5_EXTENDED"></span>.NET Framework 4.5 Extended</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1172">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1172">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1173"><span id="WCF_Services"></span><span id="wcf_services"></span><span id="WCF_SERVICES"></span>Servicios WCF</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1173"><span id="WCF_Services"></span><span id="wcf_services"></span><span id="WCF_SERVICES"></span>WCF Services</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1174">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1174">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1175"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>Activación HTTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1175"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>HTTP Activation</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1176">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1176">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1177"><span id="Message_Queuing__MSMQ__Activation"></span><span id="message_queuing__msmq__activation"></span><span id="MESSAGE_QUEUING__MSMQ__ACTIVATION"></span>Activación de Message Queuing (MSMQ)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1177"><span id="Message_Queuing__MSMQ__Activation"></span><span id="message_queuing__msmq__activation"></span><span id="MESSAGE_QUEUING__MSMQ__ACTIVATION"></span>Message Queuing (MSMQ) Activation</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9eeeb-1178"><span id="Named_Pipe_Activation"></span><span id="named_pipe_activation"></span><span id="NAMED_PIPE_ACTIVATION"></span>Activación de canalización con nombre</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1178"><span id="Named_Pipe_Activation"></span><span id="named_pipe_activation"></span><span id="NAMED_PIPE_ACTIVATION"></span>Named Pipe Activation</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1179">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1179">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1180"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>Activación de TCP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1180"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>TCP Activation</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1181">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1181">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1182"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>Uso compartido de puertos TCP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1182"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>TCP Port Sharing</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1183">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1183">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1184"><span id="ASP.NET_4.5"></span><span id="asp.net_4.5"></span>ASP.NET 4,5</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1184"><span id="ASP.NET_4.5"></span><span id="asp.net_4.5"></span>ASP.NET 4.5</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1185">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1185">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1186"><span id=".NET_Extensibility_4.5"></span><span id=".net_extensibility_4.5"></span><span id=".NET_EXTENSIBILITY_4.5"></span>Extensibilidad de .NET 4,5</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1186"><span id=".NET_Extensibility_4.5"></span><span id=".net_extensibility_4.5"></span><span id=".NET_EXTENSIBILITY_4.5"></span>.NET Extensibility 4.5</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1187">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1187">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1188"><span id="DirectAccess_and_VPN__RAS_"></span><span id="directaccess_and_vpn__ras_"></span><span id="DIRECTACCESS_AND_VPN__RAS_"></span>DirectAccess y VPN (RAS)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1188"><span id="DirectAccess_and_VPN__RAS_"></span><span id="directaccess_and_vpn__ras_"></span><span id="DIRECTACCESS_AND_VPN__RAS_"></span>DirectAccess and VPN (RAS)</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1189">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1189">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1190"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Automático</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1190"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Routing</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1191">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1191">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1192"><span id="Storage_Services"></span><span id="storage_services"></span><span id="STORAGE_SERVICES"></span>Servicios de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1192"><span id="Storage_Services"></span><span id="storage_services"></span><span id="STORAGE_SERVICES"></span>Storage Services</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1193">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1193">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1194"><span id="Failover_Cluster_Management_Tools"></span><span id="failover_cluster_management_tools"></span><span id="FAILOVER_CLUSTER_MANAGEMENT_TOOLS"></span>Herramientas de administración del clúster de conmutación por error</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1194"><span id="Failover_Cluster_Management_Tools"></span><span id="failover_cluster_management_tools"></span><span id="FAILOVER_CLUSTER_MANAGEMENT_TOOLS"></span>Failover Cluster Management Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1195">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1195">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1196"><span id="Active_Directory_Rights_Management_Services_Tools"></span><span id="active_directory_rights_management_services_tools"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOLS"></span>Herramientas de Active Directory Rights Management Services</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1196"><span id="Active_Directory_Rights_Management_Services_Tools"></span><span id="active_directory_rights_management_services_tools"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOLS"></span>Active Directory Rights Management Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1197">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1197">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1198"><span id="Application_Initialization"></span><span id="application_initialization"></span><span id="APPLICATION_INITIALIZATION"></span>Inicialización de la aplicación</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1198"><span id="Application_Initialization"></span><span id="application_initialization"></span><span id="APPLICATION_INITIALIZATION"></span>Application Initialization</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1199">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1199">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1200"><span id="Centralized_SSL_Certificate_Support"></span><span id="centralized_ssl_certificate_support"></span><span id="CENTRALIZED_SSL_CERTIFICATE_SUPPORT"></span>Compatibilidad de certificados SSL centralizada</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1200"><span id="Centralized_SSL_Certificate_Support"></span><span id="centralized_ssl_certificate_support"></span><span id="CENTRALIZED_SSL_CERTIFICATE_SUPPORT"></span>Centralized SSL Certificate Support</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1201">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1201">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1202"><span id="Claims-aware_Agent"></span><span id="claims-aware_agent"></span><span id="CLAIMS-AWARE_AGENT"></span>Agente para notificaciones</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1202"><span id="Claims-aware_Agent"></span><span id="claims-aware_agent"></span><span id="CLAIMS-AWARE_AGENT"></span>Claims-aware Agent</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1203">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1203">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1204"><span id="Remote_Desktop_Session_Host_Tools"></span><span id="remote_desktop_session_host_tools"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS"></span>Herramientas del host de sesión Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1204"><span id="Remote_Desktop_Session_Host_Tools"></span><span id="remote_desktop_session_host_tools"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS"></span>Remote Desktop Session Host Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1205">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1205">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1206"><span id="WebSocket_Protocol"></span><span id="websocket_protocol"></span><span id="WEBSOCKET_PROTOCOL"></span>Protocolo WebSocket</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1206"><span id="WebSocket_Protocol"></span><span id="websocket_protocol"></span><span id="WEBSOCKET_PROTOCOL"></span>WebSocket Protocol</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1207">ya no se admite</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1207">no longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1208"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>Acceso de red COM+</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1208"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>COM+ Network Access</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1209">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1209">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1210"><span id="File_and_iSCSI_Services_name_change"></span><span id="file_and_iscsi_services_name_change"></span><span id="FILE_AND_ISCSI_SERVICES_NAME_CHANGE"></span>Cambio de nombre de servicios de iSCSI y archivos</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1210"><span id="File_and_iSCSI_Services_name_change"></span><span id="file_and_iscsi_services_name_change"></span><span id="FILE_AND_ISCSI_SERVICES_NAME_CHANGE"></span>File and iSCSI Services name change</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1211">Cambiado a servicios de archivo</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1211">Changed to File Services</span></span>

</dd> </dl>

### <a name="windows-server-2012"></a><span data-ttu-id="9eeeb-1212">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1212">Windows Server 2012</span></span>

<dl> <dt>

<span data-ttu-id="9eeeb-1213"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Infraestructura e interfaces de usuario</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1213"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>User Interfaces and Infrastructure</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1214">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1214">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1215"><span id="Server_for_NFS"></span><span id="server_for_nfs"></span><span id="SERVER_FOR_NFS"></span>Servidor para NFS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1215"><span id="Server_for_NFS"></span><span id="server_for_nfs"></span><span id="SERVER_FOR_NFS"></span>Server for NFS</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1216">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1216">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1217"><span id="File_Server_VSS_Agent_Service"></span><span id="file_server_vss_agent_service"></span><span id="FILE_SERVER_VSS_AGENT_SERVICE"></span>Servicio del agente VSS del servidor de archivos</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1217"><span id="File_Server_VSS_Agent_Service"></span><span id="file_server_vss_agent_service"></span><span id="FILE_SERVER_VSS_AGENT_SERVICE"></span>File Server VSS Agent Service</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1218">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1218">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1219"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>Servidor de destino iSCSI</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1219"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>iSCSI Target Server</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1220">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1220">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1221"><span id="Data_Deduplication"></span><span id="data_deduplication"></span><span id="DATA_DEDUPLICATION"></span>Desduplicación de datos</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1221"><span id="Data_Deduplication"></span><span id="data_deduplication"></span><span id="DATA_DEDUPLICATION"></span>Data Deduplication</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1222">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1222">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1223"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Carpetas de trabajo</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1223"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Work Folders</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1224">Quitado</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1224">Removed</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1225"><span id="Core_Services"></span><span id="core_services"></span><span id="CORE_SERVICES"></span>Servicios principales</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1225"><span id="Core_Services"></span><span id="core_services"></span><span id="CORE_SERVICES"></span>Core Services</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1226">Agregado solo para esta versión.</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1226">Added for this version only.</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1227"><span id="Remote_Desktop_Virtual_Graphics"></span><span id="remote_desktop_virtual_graphics"></span><span id="REMOTE_DESKTOP_VIRTUAL_GRAPHICS"></span>Escritorio remoto de gráficos virtuales</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1227"><span id="Remote_Desktop_Virtual_Graphics"></span><span id="remote_desktop_virtual_graphics"></span><span id="REMOTE_DESKTOP_VIRTUAL_GRAPHICS"></span>Remote Desktop Virtual Graphics</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1228">Agregado solo para esta versión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1228">Added for this version only</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1229"><span id="Remote_Access"></span><span id="remote_access"></span><span id="REMOTE_ACCESS"></span>Acceso remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1229"><span id="Remote_Access"></span><span id="remote_access"></span><span id="REMOTE_ACCESS"></span>Remote Access</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1230">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1230">Added</span></span>

</dd> </dl>

### <a name="windows-server-2008-r2"></a><span data-ttu-id="9eeeb-1231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1231">Windows Server 2008 R2</span></span>

<dl> <dt>

<span data-ttu-id="9eeeb-1232"><span id="UDDI_Services"></span><span id="uddi_services"></span><span id="UDDI_SERVICES"></span>Servicios UDDI</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1232"><span id="UDDI_Services"></span><span id="uddi_services"></span><span id="UDDI_SERVICES"></span>UDDI Services</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1233">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1233">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1234"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Administrador de recursos del sistema de Windows</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1234"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows System Resource Manager</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1235">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1235">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1236"><span id="Removable_Storage_Manager"></span><span id="removable_storage_manager"></span><span id="REMOVABLE_STORAGE_MANAGER"></span>Administrador de almacenamiento extraíble</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1236"><span id="Removable_Storage_Manager"></span><span id="removable_storage_manager"></span><span id="REMOVABLE_STORAGE_MANAGER"></span>Removable Storage Manager</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1237">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1237">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1238"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1238"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1239">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1239">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1240"><span id="Ink_and_Handwriting_Services"></span><span id="ink_and_handwriting_services"></span><span id="INK_AND_HANDWRITING_SERVICES"></span>Servicios de Escritura con lápiz y Escritura a mano</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1240"><span id="Ink_and_Handwriting_Services"></span><span id="ink_and_handwriting_services"></span><span id="INK_AND_HANDWRITING_SERVICES"></span>Ink and Handwriting Services</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1241">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1241">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1242"><span id="WinRM_IIS_Extension"></span><span id="winrm_iis_extension"></span><span id="WINRM_IIS_EXTENSION"></span>Extensión IIS de WinRM</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1242"><span id="WinRM_IIS_Extension"></span><span id="winrm_iis_extension"></span><span id="WINRM_IIS_EXTENSION"></span>WinRM IIS Extension</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1243">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1243">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1244"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>Consola de administración de DirectAccess</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1244"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>DirectAccess Management Console</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1245">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1245">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1246"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Servicio de transferencia inteligente en segundo plano (BITS)</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1246"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Background Intelligent Transfer Service (BITS)</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1247">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1247">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1248"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>Visor de XPS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1248"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS Viewer</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1249">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1249">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1250"><span id="Windows_Biometric_Framework"></span><span id="windows_biometric_framework"></span><span id="WINDOWS_BIOMETRIC_FRAMEWORK"></span>Plataforma de biometría de Windows</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1250"><span id="Windows_Biometric_Framework"></span><span id="windows_biometric_framework"></span><span id="WINDOWS_BIOMETRIC_FRAMEWORK"></span>Windows Biometric Framework</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1251">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1251">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1252"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>Compatibilidad con WoW64</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1252"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>WoW64 Support</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1253">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1253">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1254"><span id="Windows_PowerShell_Integrated_Scripting_Environment__ISE_"></span><span id="windows_powershell_integrated_scripting_environment__ise_"></span><span id="WINDOWS_POWERSHELL_INTEGRATED_SCRIPTING_ENVIRONMENT__ISE_"></span>Entorno de scripting integrado (ISE) de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1254"><span id="Windows_PowerShell_Integrated_Scripting_Environment__ISE_"></span><span id="windows_powershell_integrated_scripting_environment__ise_"></span><span id="WINDOWS_POWERSHELL_INTEGRATED_SCRIPTING_ENVIRONMENT__ISE_"></span>Windows PowerShell Integrated Scripting Environment (ISE)</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1255">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1255">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1256"><span id="File_Replication_Service"></span><span id="file_replication_service"></span><span id="FILE_REPLICATION_SERVICE"></span>Servicio de replicación de archivos</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1256"><span id="File_Replication_Service"></span><span id="file_replication_service"></span><span id="FILE_REPLICATION_SERVICE"></span>File Replication Service</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1257">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1257">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1258"><span id="BranchCache_for_Network_Files"></span><span id="branchcache_for_network_files"></span><span id="BRANCHCACHE_FOR_NETWORK_FILES"></span>BranchCache para archivos de red</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1258"><span id="BranchCache_for_Network_Files"></span><span id="branchcache_for_network_files"></span><span id="BRANCHCACHE_FOR_NETWORK_FILES"></span>BranchCache for Network Files</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1259">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1259">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1260"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Carpetas de trabajo</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1260"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Work Folders</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1261">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1261">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1262"><span id="Distributed_Scan_Server"></span><span id="distributed_scan_server"></span><span id="DISTRIBUTED_SCAN_SERVER"></span>Servidor de digitalización distribuida</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1262"><span id="Distributed_Scan_Server"></span><span id="distributed_scan_server"></span><span id="DISTRIBUTED_SCAN_SERVER"></span>Distributed Scan Server</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1263">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1263">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1264"><span id="FTP_Publishing_Service"></span><span id="ftp_publishing_service"></span><span id="FTP_PUBLISHING_SERVICE"></span>Servicio de publicación FTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1264"><span id="FTP_Publishing_Service"></span><span id="ftp_publishing_service"></span><span id="FTP_PUBLISHING_SERVICE"></span>FTP Publishing Service</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1265">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1265">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1266"><span id="FTP_Management_Console"></span><span id="ftp_management_console"></span><span id="FTP_MANAGEMENT_CONSOLE"></span>Consola de administración de FTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1266"><span id="FTP_Management_Console"></span><span id="ftp_management_console"></span><span id="FTP_MANAGEMENT_CONSOLE"></span>FTP Management Console</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1267">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1267">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1268"><span id="FTP_Service"></span><span id="ftp_service"></span><span id="FTP_SERVICE"></span>Servicio FTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1268"><span id="FTP_Service"></span><span id="ftp_service"></span><span id="FTP_SERVICE"></span>FTP Service</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1269">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1269">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1270"><span id="FTP_Extensibility"></span><span id="ftp_extensibility"></span><span id="FTP_EXTENSIBILITY"></span>Extensibilidad de FTP</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1270"><span id="FTP_Extensibility"></span><span id="ftp_extensibility"></span><span id="FTP_EXTENSIBILITY"></span>FTP Extensibility</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1271">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1271">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1272"><span id="IIS_Hostable_Web_Core"></span><span id="iis_hostable_web_core"></span><span id="IIS_HOSTABLE_WEB_CORE"></span>Núcleo de web Hospedable de IIS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1272"><span id="IIS_Hostable_Web_Core"></span><span id="iis_hostable_web_core"></span><span id="IIS_HOSTABLE_WEB_CORE"></span>IIS Hostable Web Core</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9eeeb-1273"><span id="Windows_2000_Client_Support"></span><span id="windows_2000_client_support"></span><span id="WINDOWS_2000_CLIENT_SUPPORT"></span>Compatibilidad con clientes de Windows 2000</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1273"><span id="Windows_2000_Client_Support"></span><span id="windows_2000_client_support"></span><span id="WINDOWS_2000_CLIENT_SUPPORT"></span>Windows 2000 Client Support</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1274">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1274">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1275"><span id="Certificate_Enrollment_Web_Service"></span><span id="certificate_enrollment_web_service"></span><span id="CERTIFICATE_ENROLLMENT_WEB_SERVICE"></span>Servicio web de inscripción de certificados</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1275"><span id="Certificate_Enrollment_Web_Service"></span><span id="certificate_enrollment_web_service"></span><span id="CERTIFICATE_ENROLLMENT_WEB_SERVICE"></span>Certificate Enrollment Web Service</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1276">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1276">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1277"><span id="Certificate_Enrollment_Policy_Web_Service"></span><span id="certificate_enrollment_policy_web_service"></span><span id="CERTIFICATE_ENROLLMENT_POLICY_WEB_SERVICE"></span>Servicio web de directiva de inscripción de certificados</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1277"><span id="Certificate_Enrollment_Policy_Web_Service"></span><span id="certificate_enrollment_policy_web_service"></span><span id="CERTIFICATE_ENROLLMENT_POLICY_WEB_SERVICE"></span>Certificate Enrollment Policy Web Service</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1278">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1278">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1279"><span id="UDDI_Services_Web_Application"></span><span id="uddi_services_web_application"></span><span id="UDDI_SERVICES_WEB_APPLICATION"></span>Aplicación Web de servicios UDDI</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1279"><span id="UDDI_Services_Web_Application"></span><span id="uddi_services_web_application"></span><span id="UDDI_SERVICES_WEB_APPLICATION"></span>UDDI Services Web Application</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1280">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1280">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1281"><span id="UDDI_Services_Database"></span><span id="uddi_services_database"></span><span id="UDDI_SERVICES_DATABASE"></span>Base de datos de servicios UDDI</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1281"><span id="UDDI_Services_Database"></span><span id="uddi_services_database"></span><span id="UDDI_SERVICES_DATABASE"></span>UDDI Services Database</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1282">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1282">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1283"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Extensiones de servidor de aplicaciones para .NET 4,0</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1283"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Application Server Extensions for .NET 4.0</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1284">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1284">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1285"><span id="UDDI_Services_Tools"></span><span id="uddi_services_tools"></span><span id="UDDI_SERVICES_TOOLS"></span>Herramientas de servicios UDDI</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1285"><span id="UDDI_Services_Tools"></span><span id="uddi_services_tools"></span><span id="UDDI_SERVICES_TOOLS"></span>UDDI Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1286">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1286">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1287"><span id="BitLocker_Drive_Encryption_Administration_Utilities"></span><span id="bitlocker_drive_encryption_administration_utilities"></span><span id="BITLOCKER_DRIVE_ENCRYPTION_ADMINISTRATION_UTILITIES"></span>Utilidades de administración de Cifrado de unidad BitLocker</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1287"><span id="BitLocker_Drive_Encryption_Administration_Utilities"></span><span id="bitlocker_drive_encryption_administration_utilities"></span><span id="BITLOCKER_DRIVE_ENCRYPTION_ADMINISTRATION_UTILITIES"></span>BitLocker Drive Encryption Administration Utilities</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1288">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1288">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1289"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Herramientas de AD DS y AD LDS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1289"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS and AD LDS Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1290">Ya no dispone de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1290">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1291"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Herramientas de AD DS y AD LDS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1291"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS and AD LDS Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1292">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1292">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1293"><span id="Active_Directory_Administrative_Center"></span><span id="active_directory_administrative_center"></span><span id="ACTIVE_DIRECTORY_ADMINISTRATIVE_CENTER"></span>Centro de administración de Active Directory</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1293"><span id="Active_Directory_Administrative_Center"></span><span id="active_directory_administrative_center"></span><span id="ACTIVE_DIRECTORY_ADMINISTRATIVE_CENTER"></span>Active Directory Administrative Center</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1294">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1294">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1295"><span id="Active_Directory_module_for___________Windows_PowerShell"></span><span id="active_directory_module_for___________windows_powershell"></span><span id="ACTIVE_DIRECTORY_MODULE_FOR___________WINDOWS_POWERSHELL"></span>Módulo de Active Directory para Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1295"><span id="Active_Directory_module_for___________Windows_PowerShell"></span><span id="active_directory_module_for___________windows_powershell"></span><span id="ACTIVE_DIRECTORY_MODULE_FOR___________WINDOWS_POWERSHELL"></span>Active Directory module for Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1296">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1296">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1297"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Herramientas de Conexión a Escritorio remoto Broker</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1297"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Remote Desktop Connection Broker Tools</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1298">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1298">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1299"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1299"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1300">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1300">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1301"><span id="WoW64_for_.NET_Framework_2.0_and_Windows_PowerShell"></span><span id="wow64_for_.net_framework_2.0_and_windows_powershell"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND_WINDOWS_POWERSHELL"></span>WoW64 para .NET Framework 2,0 y Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1301"><span id="WoW64_for_.NET_Framework_2.0_and_Windows_PowerShell"></span><span id="wow64_for_.net_framework_2.0_and_windows_powershell"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND_WINDOWS_POWERSHELL"></span>WoW64 for .NET Framework 2.0 and Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1302">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1302">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1303"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 para .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1303"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 for .NET Framework 2.0</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1304">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1304">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1305"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 para PowerShell</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1305"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 for PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1306">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1306">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1307"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 para .NET Framework 3,0 y 3,5</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1307"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 for .NET Framework 3.0 and 3.5</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1308">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1308">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1309"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 para servicios de impresión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1309"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 for Print Services</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1310">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1310">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1311"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 para clúster de conmutación por error</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1311"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 for Failover Clustering</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1312">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1312">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1313"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 para el editor de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1313"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 for Input Method Editor</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1314">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1314">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1315"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 para Subsystem for UNIX-Based Applications</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1315"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 for Subsystem for UNIX-based Applications</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1316">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1316">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1317"><span id="BitLocker_Recovery_Password_Viewer"></span><span id="bitlocker_recovery_password_viewer"></span><span id="BITLOCKER_RECOVERY_PASSWORD_VIEWER"></span>Visor de contraseñas de recuperación de BitLocker</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1317"><span id="BitLocker_Recovery_Password_Viewer"></span><span id="bitlocker_recovery_password_viewer"></span><span id="BITLOCKER_RECOVERY_PASSWORD_VIEWER"></span>BitLocker Recovery Password Viewer</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1318">Adición</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1318">Added</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1319"><span id="Print_and_Document_Services_name_change"></span><span id="print_and_document_services_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_NAME_CHANGE"></span>Cambio de nombre de Servicios de impresión y documentos</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1319"><span id="Print_and_Document_Services_name_change"></span><span id="print_and_document_services_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_NAME_CHANGE"></span>Print and Document Services name change</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1320">Servicios de impresión con nombre para esta versión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1320">named Print Services for this release</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1321"><span id="Remote_Desktop_Services_name_change"></span><span id="remote_desktop_services_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_NAME_CHANGE"></span>Cambio de nombre de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1321"><span id="Remote_Desktop_Services_name_change"></span><span id="remote_desktop_services_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_NAME_CHANGE"></span>Remote Desktop Services name change</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1322">Terminal Services con nombre en esta versión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1322">named Terminal Services in this release</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1323"><span id=".NET_Framework_3.5.1_Features_name_change"></span><span id=".net_framework_3.5.1_features_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES_NAME_CHANGE"></span>Cambio de nombre de características de .NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1323"><span id=".NET_Framework_3.5.1_Features_name_change"></span><span id=".net_framework_3.5.1_features_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES_NAME_CHANGE"></span>.NET Framework 3.5.1 Features name change</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1324">Características con nombre .NET Framework 3,0 en esta versión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1324">Named .NET Framework 3.0 Features in this release</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1325"><span id="Remote_Desktop_Session_Host_name_change"></span><span id="remote_desktop_session_host_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_NAME_CHANGE"></span>Escritorio remoto cambio de nombre de host de sesión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1325"><span id="Remote_Desktop_Session_Host_name_change"></span><span id="remote_desktop_session_host_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_NAME_CHANGE"></span>Remote Desktop Session Host name change</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1326">Terminal Server con nombre en esta versión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1326">Named Terminal Server in this release</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1327"><span id="Remote_Desktop_Licensing_name_change"></span><span id="remote_desktop_licensing_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_NAME_CHANGE"></span>Escritorio remoto cambio de nombre de licencia</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1327"><span id="Remote_Desktop_Licensing_name_change"></span><span id="remote_desktop_licensing_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_NAME_CHANGE"></span>Remote Desktop Licensing name change</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1328">Licencias de TS con nombre en esta versión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1328">Named TS Licensing in this release</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1329"><span id="Remote_Desktop_Gateway_name_change"></span><span id="remote_desktop_gateway_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_NAME_CHANGE"></span>Escritorio remoto cambio de nombre de puerta de enlace</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1329"><span id="Remote_Desktop_Gateway_name_change"></span><span id="remote_desktop_gateway_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_NAME_CHANGE"></span>Remote Desktop Gateway name change</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1330">Puerta de enlace de TS en esta versión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1330">Named TS Gateway in this release</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1331"><span id="Remote_Desktop_Connection_Broker_name_change"></span><span id="remote_desktop_connection_broker_name_change"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_NAME_CHANGE"></span>Cambio de nombre de agente Conexión a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1331"><span id="Remote_Desktop_Connection_Broker_name_change"></span><span id="remote_desktop_connection_broker_name_change"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_NAME_CHANGE"></span>Remote Desktop Connection Broker name change</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1332">Agente de sesiones de TS con nombre en esta versión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1332">Named TS Session Broker in this release</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1333"><span id="Remote_Desktop_Web_Access_name_change"></span><span id="remote_desktop_web_access_name_change"></span><span id="REMOTE_DESKTOP_WEB_ACCESS_NAME_CHANGE"></span>Escritorio remoto cambio de nombre de acceso web</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1333"><span id="Remote_Desktop_Web_Access_name_change"></span><span id="remote_desktop_web_access_name_change"></span><span id="REMOTE_DESKTOP_WEB_ACCESS_NAME_CHANGE"></span>Remote Desktop Web Access name change</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1334">Llamado acceso web de TS en esta versión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1334">Named TS Web Access in this release</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1335"><span id=".NET_Framework_3.5.1_name_change"></span><span id=".net_framework_3.5.1_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_NAME_CHANGE"></span>Cambio de nombre de .NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1335"><span id=".NET_Framework_3.5.1_name_change"></span><span id=".net_framework_3.5.1_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_NAME_CHANGE"></span>.NET Framework 3.5.1 name change</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1336">(220) con el nombre características de net FX 3,0 en esta versión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1336">(220) Named Net FX 3.0 Features in this release</span></span>

<span data-ttu-id="9eeeb-1337">(230) con el nombre Server Core en esta versión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1337">(230) Named Application Server Core in this release</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1338"><span id="AD_DS_Tools_name_change"></span><span id="ad_ds_tools_name_change"></span><span id="AD_DS_TOOLS_NAME_CHANGE"></span>Cambio de nombre de herramientas de AD DS</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1338"><span id="AD_DS_Tools_name_change"></span><span id="ad_ds_tools_name_change"></span><span id="AD_DS_TOOLS_NAME_CHANGE"></span>AD DS Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1339">Herramientas de Active Directory Domain Services con nombre en esta versión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1339">Named Active Directory Domain Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1340"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_lds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>Cambio de nombre de AD LDS Snap-Ins y Command-Line Tools</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1340"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_lds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD LDS Snap-Ins and Command-Line Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1341">Herramientas de Active Directory Lightweight Directory Services con nombre en esta versión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1341">Named Active Directory Lightweight Directory Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1342"><span id="Print_and_Document_Services_Tools_name_change"></span><span id="print_and_document_services_tools_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_TOOLS_NAME_CHANGE"></span>Cambio de nombre de herramientas de Servicios de impresión y documentos</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1342"><span id="Print_and_Document_Services_Tools_name_change"></span><span id="print_and_document_services_tools_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_TOOLS_NAME_CHANGE"></span>Print and Document Services Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1343">Herramientas de servicios de impresión con nombre en esta versión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1343">Named Print Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1344"><span id="Remote_Desktop_Services_Tools_name_change"></span><span id="remote_desktop_services_tools_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS_NAME_CHANGE"></span>Cambio de nombre de herramientas de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1344"><span id="Remote_Desktop_Services_Tools_name_change"></span><span id="remote_desktop_services_tools_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS_NAME_CHANGE"></span>Remote Desktop Services Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1345">Herramientas de Terminal Services con nombre en esta versión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1345">Named Terminal Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1346"><span id="Remote_Desktop_Session_Host_Tools_name_change"></span><span id="remote_desktop_session_host_tools_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS_NAME_CHANGE"></span>Escritorio remoto cambiar el nombre de las herramientas de host de sesión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1346"><span id="Remote_Desktop_Session_Host_Tools_name_change"></span><span id="remote_desktop_session_host_tools_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS_NAME_CHANGE"></span>Remote Desktop Session Host Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1347">Herramientas de Terminal Server con nombre en esta versión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1347">Named Terminal Server Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1348"><span id="Remote_Desktop_Gateway_Tools_name_change"></span><span id="remote_desktop_gateway_tools_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_TOOLS_NAME_CHANGE"></span>Escritorio remoto cambiar el nombre de las herramientas de puerta de enlace</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1348"><span id="Remote_Desktop_Gateway_Tools_name_change"></span><span id="remote_desktop_gateway_tools_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_TOOLS_NAME_CHANGE"></span>Remote Desktop Gateway Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1349">Herramientas de puerta de enlace de TS en esta versión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1349">Named TS Gateway Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1350"><span id="Remote_Desktop_Licensing_Tools_name_change"></span><span id="remote_desktop_licensing_tools_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_TOOLS_NAME_CHANGE"></span>Cambio de nombre de herramientas de licencias de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1350"><span id="Remote_Desktop_Licensing_Tools_name_change"></span><span id="remote_desktop_licensing_tools_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_TOOLS_NAME_CHANGE"></span>Remote Desktop Licensing Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1351">Herramientas de licencias de TS con nombre en esta versión</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1351">Named TS Licensing Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="9eeeb-1352"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_ds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>Cambio de nombre de AD DS Snap-Ins y Command-Line Tools</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1352"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_ds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD DS Snap-Ins and Command-Line Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="9eeeb-1353">Herramientas del controlador de dominio de Active Directory</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1353">Active Directory Domain Controller Tools</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="9eeeb-1354">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1354">Examples</span></span>

<span data-ttu-id="9eeeb-1355">En el siguiente script se muestran los nombres de todas las características de servidor del equipo denominado "FABRIKAM".</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1355">The following script displays the names of all the server features on the computer named "FABRIKAM".</span></span> <span data-ttu-id="9eeeb-1356">Tenga en cuenta que el equipo de destino debe ejecutar Windows Server 2008 o un sistema operativo de servidor posterior.</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1356">Note that the target computer must be running Windows Server 2008 or a later server operating system.</span></span>


```VB
strComputer = "FABRIKAM"

Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")

Set colFeatureList = objWMIService.ExecQuery("SELECT Name FROM Win32_ServerFeature")

For Each objFeature In colFeatureList
   WScript.Echo objFeature.Name

Next
```



## <a name="requirements"></a><span data-ttu-id="9eeeb-1357">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1357">Requirements</span></span>



| <span data-ttu-id="9eeeb-1358">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1358">Requirement</span></span> | <span data-ttu-id="9eeeb-1359">Value</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1359">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eeeb-1360">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1360">Minimum supported client</span></span><br/> | <span data-ttu-id="9eeeb-1361">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1361">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9eeeb-1362">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1362">Minimum supported server</span></span><br/> | <span data-ttu-id="9eeeb-1363">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1363">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="9eeeb-1364">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1364">Namespace</span></span><br/>                | <span data-ttu-id="9eeeb-1365">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1365">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="9eeeb-1366">MOF</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1366">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9eeeb-1367"><dt>ServerCompProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9eeeb-1367"><dt>ServerCompProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9eeeb-1368">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9eeeb-1368">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9eeeb-1369"><dt>ServerCompProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eeeb-1369"><dt>ServerCompProv.dll</dt></span></span> </dl> |



 

