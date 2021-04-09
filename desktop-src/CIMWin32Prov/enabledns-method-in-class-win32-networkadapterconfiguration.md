---
description: El método estático de la clase WMI habilitada habilita el sistema de nombres de dominio (DNS) para el servicio.
ms.assetid: 083dccb1-eb38-4ae5-a252-0001759c0f50
ms.tgt_platform: multiple
title: Método habilitado de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableDNS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fc217211455d8804de47b2b3ffc761d4328fa49a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153002"
---
# <a name="enabledns-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="41d35-103">Método habilitado de la \_ clase Win32 NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="41d35-103">EnableDNS method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="41d35-104">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **habilitada habilita** el sistema de nombres de dominio (DNS) para el servicio.</span><span class="sxs-lookup"><span data-stu-id="41d35-104">The **EnableDNS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method enables the Domain Name System (DNS) for service.</span></span>

<span data-ttu-id="41d35-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="41d35-105">This topic uses the Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="41d35-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="41d35-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="41d35-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41d35-107">Syntax</span></span>


```mof
uint32 EnableDNS(
  [in, optional] string DNSHostName,
  [in, optional] string DNSDomain,
  [in, optional] string DNSServerSearchOrder[],
  [in, optional] string DNSDomainSuffixSearchOrder[]
);
```



## <a name="parameters"></a><span data-ttu-id="41d35-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="41d35-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41d35-109">*DNSHostName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="41d35-109">*DNSHostName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="41d35-110">Nombre del host DNS que este método habilita.</span><span class="sxs-lookup"><span data-stu-id="41d35-110">Name of the DNS host that this method enables.</span></span>

<span data-ttu-id="41d35-111">Ejemplo: "corpdns"</span><span class="sxs-lookup"><span data-stu-id="41d35-111">Example: "corpdns"</span></span>

</dd> <dt>

<span data-ttu-id="41d35-112">*DNSDomain* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="41d35-112">*DNSDomain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="41d35-113">Representa un nombre de organización seguido de un punto y una extensión que indica el tipo de organización.</span><span class="sxs-lookup"><span data-stu-id="41d35-113">Represents an organization name followed by a period and an extension that indicates the type of organization.</span></span>

<span data-ttu-id="41d35-114">Ejemplo: "microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="41d35-114">Example: "microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="41d35-115">*DNSServerSearchOrder* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="41d35-115">*DNSServerSearchOrder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="41d35-116">Lista de direcciones IP de servidor para consultar los servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="41d35-116">List of server IP addresses to query for DNS servers.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-117">*DNSDomainSuffixSearchOrder* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="41d35-117">*DNSDomainSuffixSearchOrder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="41d35-118">Sufijo de dominio DNS que se anexa a un nombre de host durante la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="41d35-118">DNS domain suffix that is appended to a host name during name resolution.</span></span> <span data-ttu-id="41d35-119">Al resolver un nombre de dominio completo (FQDN) de un nombre de host único, el sistema anexa el nombre de dominio local.</span><span class="sxs-lookup"><span data-stu-id="41d35-119">When resolving a fully qualified domain name (FQDN) from a host-only name, the system appends the local domain name.</span></span> <span data-ttu-id="41d35-120">Si la resolución de nombres no se realiza correctamente, el sistema utiliza la lista de sufijos de dominio para crear FQDN adicionales en el orden indicado y, a continuación, consulta los servidores DNS para cada uno.</span><span class="sxs-lookup"><span data-stu-id="41d35-120">If the name resolution is not successful, the system uses the domain suffix list to create additional FQDNs in the order listed, and then queries DNS servers for each one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41d35-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41d35-121">Return value</span></span>

<span data-ttu-id="41d35-122">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere un reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y cualquier otro número si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="41d35-122">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="41d35-123">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="41d35-123">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="41d35-124">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="41d35-124">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="41d35-125">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="41d35-125">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-126">0</span><span class="sxs-lookup"><span data-stu-id="41d35-126">0</span></span>

<span data-ttu-id="41d35-127">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="41d35-127">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-128">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="41d35-128">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-129">1</span><span class="sxs-lookup"><span data-stu-id="41d35-129">1</span></span>

<span data-ttu-id="41d35-130">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="41d35-130">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-131">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="41d35-131">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-132">64</span><span class="sxs-lookup"><span data-stu-id="41d35-132">64</span></span>

<span data-ttu-id="41d35-133">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="41d35-133">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-134">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="41d35-134">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-135">65</span><span class="sxs-lookup"><span data-stu-id="41d35-135">65</span></span>

<span data-ttu-id="41d35-136">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="41d35-136">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-137">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="41d35-137">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-138">66</span><span class="sxs-lookup"><span data-stu-id="41d35-138">66</span></span>

<span data-ttu-id="41d35-139">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="41d35-139">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-140">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="41d35-140">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-141">67</span><span class="sxs-lookup"><span data-stu-id="41d35-141">67</span></span>

<span data-ttu-id="41d35-142">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="41d35-142">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-143">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="41d35-143">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-144">68</span><span class="sxs-lookup"><span data-stu-id="41d35-144">68</span></span>

<span data-ttu-id="41d35-145">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="41d35-145">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-146">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="41d35-146">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-147">69</span><span class="sxs-lookup"><span data-stu-id="41d35-147">69</span></span>

<span data-ttu-id="41d35-148">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="41d35-148">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-149">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="41d35-149">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-150">70</span><span class="sxs-lookup"><span data-stu-id="41d35-150">70</span></span>

<span data-ttu-id="41d35-151">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="41d35-151">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-152">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="41d35-152">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-153">71</span><span class="sxs-lookup"><span data-stu-id="41d35-153">71</span></span>

<span data-ttu-id="41d35-154">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="41d35-154">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-155">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="41d35-155">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-156">72</span><span class="sxs-lookup"><span data-stu-id="41d35-156">72</span></span>

<span data-ttu-id="41d35-157">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="41d35-157">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-158">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="41d35-158">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-159">73</span><span class="sxs-lookup"><span data-stu-id="41d35-159">73</span></span>

<span data-ttu-id="41d35-160">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="41d35-160">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-161">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="41d35-161">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-162">74</span><span class="sxs-lookup"><span data-stu-id="41d35-162">74</span></span>

<span data-ttu-id="41d35-163">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="41d35-163">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-164">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="41d35-164">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-165">75</span><span class="sxs-lookup"><span data-stu-id="41d35-165">75</span></span>

<span data-ttu-id="41d35-166">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="41d35-166">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-167">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="41d35-167">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-168">76</span><span class="sxs-lookup"><span data-stu-id="41d35-168">76</span></span>

<span data-ttu-id="41d35-169">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="41d35-169">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-170">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="41d35-170">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-171">77</span><span class="sxs-lookup"><span data-stu-id="41d35-171">77</span></span>

<span data-ttu-id="41d35-172">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="41d35-172">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-173">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="41d35-173">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-174">78</span><span class="sxs-lookup"><span data-stu-id="41d35-174">78</span></span>

<span data-ttu-id="41d35-175">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="41d35-175">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-176">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="41d35-176">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-177">79</span><span class="sxs-lookup"><span data-stu-id="41d35-177">79</span></span>

<span data-ttu-id="41d35-178">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="41d35-178">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-179">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="41d35-179">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-180">80</span><span class="sxs-lookup"><span data-stu-id="41d35-180">80</span></span>

<span data-ttu-id="41d35-181">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="41d35-181">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-182">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="41d35-182">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-183">81</span><span class="sxs-lookup"><span data-stu-id="41d35-183">81</span></span>

<span data-ttu-id="41d35-184">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="41d35-184">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-185">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="41d35-185">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-186">82</span><span class="sxs-lookup"><span data-stu-id="41d35-186">82</span></span>

<span data-ttu-id="41d35-187">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="41d35-187">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-188">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="41d35-188">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-189">83</span><span class="sxs-lookup"><span data-stu-id="41d35-189">83</span></span>

<span data-ttu-id="41d35-190">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="41d35-190">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-191">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="41d35-191">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-192">84</span><span class="sxs-lookup"><span data-stu-id="41d35-192">84</span></span>

<span data-ttu-id="41d35-193">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="41d35-193">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-194">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="41d35-194">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-195">85</span><span class="sxs-lookup"><span data-stu-id="41d35-195">85</span></span>

<span data-ttu-id="41d35-196">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="41d35-196">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-197">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="41d35-197">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-198">86</span><span class="sxs-lookup"><span data-stu-id="41d35-198">86</span></span>

<span data-ttu-id="41d35-199">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="41d35-199">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-200">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="41d35-200">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-201">87</span><span class="sxs-lookup"><span data-stu-id="41d35-201">87</span></span>

<span data-ttu-id="41d35-202">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="41d35-202">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-203">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="41d35-203">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-204">88</span><span class="sxs-lookup"><span data-stu-id="41d35-204">88</span></span>

<span data-ttu-id="41d35-205">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="41d35-205">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-206">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="41d35-206">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-207">89</span><span class="sxs-lookup"><span data-stu-id="41d35-207">89</span></span>

<span data-ttu-id="41d35-208">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="41d35-208">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-209">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="41d35-209">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-210">90</span><span class="sxs-lookup"><span data-stu-id="41d35-210">90</span></span>

<span data-ttu-id="41d35-211">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="41d35-211">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-212">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="41d35-212">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-213">91</span><span class="sxs-lookup"><span data-stu-id="41d35-213">91</span></span>

<span data-ttu-id="41d35-214">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="41d35-214">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-215">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="41d35-215">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-216">92</span><span class="sxs-lookup"><span data-stu-id="41d35-216">92</span></span>

<span data-ttu-id="41d35-217">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="41d35-217">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-218">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="41d35-218">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-219">93</span><span class="sxs-lookup"><span data-stu-id="41d35-219">93</span></span>

<span data-ttu-id="41d35-220">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="41d35-220">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-221">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="41d35-221">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-222">94</span><span class="sxs-lookup"><span data-stu-id="41d35-222">94</span></span>

<span data-ttu-id="41d35-223">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="41d35-223">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-224">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="41d35-224">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-225">95</span><span class="sxs-lookup"><span data-stu-id="41d35-225">95</span></span>

<span data-ttu-id="41d35-226">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="41d35-226">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-227">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="41d35-227">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-228">96</span><span class="sxs-lookup"><span data-stu-id="41d35-228">96</span></span>

<span data-ttu-id="41d35-229">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="41d35-229">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-230">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="41d35-230">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-231">97</span><span class="sxs-lookup"><span data-stu-id="41d35-231">97</span></span>

<span data-ttu-id="41d35-232">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="41d35-232">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-233">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="41d35-233">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-234">98</span><span class="sxs-lookup"><span data-stu-id="41d35-234">98</span></span>

<span data-ttu-id="41d35-235">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="41d35-235">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-236">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="41d35-236">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-237">100</span><span class="sxs-lookup"><span data-stu-id="41d35-237">100</span></span>

<span data-ttu-id="41d35-238">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="41d35-238">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="41d35-239">**Otros**</span><span class="sxs-lookup"><span data-stu-id="41d35-239">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="41d35-240">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="41d35-240">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="41d35-241">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="41d35-241">Examples</span></span>

<span data-ttu-id="41d35-242">El siguiente ejemplo de código, tomado del ejemplo de código de VBScript [habilitar DNS en todos los adaptadores de red](https://Gallery.TechNet.Microsoft.Com/c5736a48-71cc-4483-9605-d71d222740ac) de la galería de TechNet, habilita DNS para todos los adaptadores de red de un equipo.</span><span class="sxs-lookup"><span data-stu-id="41d35-242">The following code sample, taken from the [Enable DNS on All Network Adapters](https://Gallery.TechNet.Microsoft.Com/c5736a48-71cc-4483-9605-d71d222740ac) VBScript code sample on TechNet Gallery, enables DNS for all network adapters on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objNetworkSettings = objWMIService.Get("Win32_NetworkAdapterConfiguration") 
strHostName = "fabrikam1" 
arrDNSSuffixes = Array("hr.fabrikam.com", "research.fabrikam.com") 
objNetworkSettings.EnableDNS strHostName, , , arrDNSSuffixes 
```



## <a name="requirements"></a><span data-ttu-id="41d35-243">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41d35-243">Requirements</span></span>



| <span data-ttu-id="41d35-244">Requisito</span><span class="sxs-lookup"><span data-stu-id="41d35-244">Requirement</span></span> | <span data-ttu-id="41d35-245">Value</span><span class="sxs-lookup"><span data-stu-id="41d35-245">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41d35-246">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41d35-246">Minimum supported client</span></span><br/> | <span data-ttu-id="41d35-247">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41d35-247">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="41d35-248">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41d35-248">Minimum supported server</span></span><br/> | <span data-ttu-id="41d35-249">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41d35-249">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="41d35-250">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="41d35-250">Namespace</span></span><br/>                | <span data-ttu-id="41d35-251">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="41d35-251">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="41d35-252">MOF</span><span class="sxs-lookup"><span data-stu-id="41d35-252">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41d35-253"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41d35-253"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="41d35-254">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="41d35-254">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41d35-255"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41d35-255"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41d35-256">Vea también</span><span class="sxs-lookup"><span data-stu-id="41d35-256">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41d35-257">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="41d35-257">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="41d35-258">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="41d35-258">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="41d35-259">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="41d35-259">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="41d35-260">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="41d35-260">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="41d35-261">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="41d35-261">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

