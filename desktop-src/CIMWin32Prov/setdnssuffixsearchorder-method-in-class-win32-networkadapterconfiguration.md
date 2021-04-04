---
description: El método estático de la clase WMI SetDNSSuffixSearchOrder utiliza una matriz de elementos de cadena para establecer el orden de búsqueda de sufijos.
ms.assetid: 1ad9fc99-8c57-43d4-92d2-b12f2c1451cb
ms.tgt_platform: multiple
title: Método SetDNSSuffixSearchOrder de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSSuffixSearchOrder
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10088b1d0722f968e5d3742984baa91ec3e423aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907357"
---
# <a name="setdnssuffixsearchorder-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="072b0-103">Método SetDNSSuffixSearchOrder de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="072b0-103">SetDNSSuffixSearchOrder method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="072b0-104">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDNSSuffixSearchOrder** utiliza una matriz de elementos de cadena para establecer el orden de búsqueda de sufijos.</span><span class="sxs-lookup"><span data-stu-id="072b0-104">The **SetDNSSuffixSearchOrder** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method uses an array of string elements to set the suffix search order.</span></span>

<span data-ttu-id="072b0-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="072b0-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="072b0-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="072b0-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="072b0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="072b0-107">Syntax</span></span>


```mof
uint32 SetDNSSuffixSearchOrder(
  [in] string DNSDomainSuffixSearchOrder[]
);
```



## <a name="parameters"></a><span data-ttu-id="072b0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="072b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="072b0-109">*DNSDomainSuffixSearchOrder* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="072b0-109">*DNSDomainSuffixSearchOrder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="072b0-110">Lista de sufijos de servidor para consultar los servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="072b0-110">List of server suffixes to query for DNS servers.</span></span> <span data-ttu-id="072b0-111">La ubicación del registro del sufijo DNS es **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **TCPIP \| nameserver**</span><span class="sxs-lookup"><span data-stu-id="072b0-111">The registry location of the DNS suffix is **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**Tcpip\|NameServer**</span></span>

<span data-ttu-id="072b0-112">Ejemplo: "suffix1.company.com", "suffix2.company.com"</span><span class="sxs-lookup"><span data-stu-id="072b0-112">Example: "suffix1.company.com", "suffix2.company.com"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="072b0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="072b0-113">Return value</span></span>

<span data-ttu-id="072b0-114">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="072b0-114">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="072b0-115">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="072b0-115">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="072b0-116">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="072b0-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="072b0-117">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="072b0-117">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-118">0</span><span class="sxs-lookup"><span data-stu-id="072b0-118">0</span></span>

<span data-ttu-id="072b0-119">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="072b0-119">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-120">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="072b0-120">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-121">1</span><span class="sxs-lookup"><span data-stu-id="072b0-121">1</span></span>

<span data-ttu-id="072b0-122">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="072b0-122">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-123">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="072b0-123">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-124">64</span><span class="sxs-lookup"><span data-stu-id="072b0-124">64</span></span>

<span data-ttu-id="072b0-125">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="072b0-125">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-126">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="072b0-126">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-127">65</span><span class="sxs-lookup"><span data-stu-id="072b0-127">65</span></span>

<span data-ttu-id="072b0-128">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="072b0-128">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-129">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="072b0-129">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-130">66</span><span class="sxs-lookup"><span data-stu-id="072b0-130">66</span></span>

<span data-ttu-id="072b0-131">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="072b0-131">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-132">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="072b0-132">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-133">67</span><span class="sxs-lookup"><span data-stu-id="072b0-133">67</span></span>

<span data-ttu-id="072b0-134">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="072b0-134">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-135">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="072b0-135">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-136">68</span><span class="sxs-lookup"><span data-stu-id="072b0-136">68</span></span>

<span data-ttu-id="072b0-137">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="072b0-137">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-138">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="072b0-138">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-139">69</span><span class="sxs-lookup"><span data-stu-id="072b0-139">69</span></span>

<span data-ttu-id="072b0-140">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="072b0-140">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-141">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="072b0-141">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-142">70</span><span class="sxs-lookup"><span data-stu-id="072b0-142">70</span></span>

<span data-ttu-id="072b0-143">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="072b0-143">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-144">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="072b0-144">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-145">71</span><span class="sxs-lookup"><span data-stu-id="072b0-145">71</span></span>

<span data-ttu-id="072b0-146">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="072b0-146">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-147">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="072b0-147">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-148">72</span><span class="sxs-lookup"><span data-stu-id="072b0-148">72</span></span>

<span data-ttu-id="072b0-149">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="072b0-149">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-150">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="072b0-150">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-151">73</span><span class="sxs-lookup"><span data-stu-id="072b0-151">73</span></span>

<span data-ttu-id="072b0-152">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="072b0-152">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-153">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="072b0-153">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-154">74</span><span class="sxs-lookup"><span data-stu-id="072b0-154">74</span></span>

<span data-ttu-id="072b0-155">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="072b0-155">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-156">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="072b0-156">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-157">75</span><span class="sxs-lookup"><span data-stu-id="072b0-157">75</span></span>

<span data-ttu-id="072b0-158">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="072b0-158">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-159">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="072b0-159">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-160">76</span><span class="sxs-lookup"><span data-stu-id="072b0-160">76</span></span>

<span data-ttu-id="072b0-161">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="072b0-161">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-162">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="072b0-162">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-163">77</span><span class="sxs-lookup"><span data-stu-id="072b0-163">77</span></span>

<span data-ttu-id="072b0-164">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="072b0-164">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-165">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="072b0-165">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-166">78</span><span class="sxs-lookup"><span data-stu-id="072b0-166">78</span></span>

<span data-ttu-id="072b0-167">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="072b0-167">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-168">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="072b0-168">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-169">79</span><span class="sxs-lookup"><span data-stu-id="072b0-169">79</span></span>

<span data-ttu-id="072b0-170">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="072b0-170">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-171">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="072b0-171">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-172">80</span><span class="sxs-lookup"><span data-stu-id="072b0-172">80</span></span>

<span data-ttu-id="072b0-173">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="072b0-173">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-174">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="072b0-174">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-175">81</span><span class="sxs-lookup"><span data-stu-id="072b0-175">81</span></span>

<span data-ttu-id="072b0-176">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="072b0-176">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-177">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="072b0-177">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-178">82</span><span class="sxs-lookup"><span data-stu-id="072b0-178">82</span></span>

<span data-ttu-id="072b0-179">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="072b0-179">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-180">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="072b0-180">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-181">83</span><span class="sxs-lookup"><span data-stu-id="072b0-181">83</span></span>

<span data-ttu-id="072b0-182">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="072b0-182">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-183">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="072b0-183">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-184">84</span><span class="sxs-lookup"><span data-stu-id="072b0-184">84</span></span>

<span data-ttu-id="072b0-185">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="072b0-185">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-186">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="072b0-186">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-187">85</span><span class="sxs-lookup"><span data-stu-id="072b0-187">85</span></span>

<span data-ttu-id="072b0-188">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="072b0-188">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-189">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="072b0-189">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-190">86</span><span class="sxs-lookup"><span data-stu-id="072b0-190">86</span></span>

<span data-ttu-id="072b0-191">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="072b0-191">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-192">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="072b0-192">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-193">87</span><span class="sxs-lookup"><span data-stu-id="072b0-193">87</span></span>

<span data-ttu-id="072b0-194">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="072b0-194">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-195">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="072b0-195">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-196">88</span><span class="sxs-lookup"><span data-stu-id="072b0-196">88</span></span>

<span data-ttu-id="072b0-197">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="072b0-197">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-198">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="072b0-198">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-199">89</span><span class="sxs-lookup"><span data-stu-id="072b0-199">89</span></span>

<span data-ttu-id="072b0-200">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="072b0-200">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-201">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="072b0-201">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-202">90</span><span class="sxs-lookup"><span data-stu-id="072b0-202">90</span></span>

<span data-ttu-id="072b0-203">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="072b0-203">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-204">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="072b0-204">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-205">91</span><span class="sxs-lookup"><span data-stu-id="072b0-205">91</span></span>

<span data-ttu-id="072b0-206">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="072b0-206">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-207">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="072b0-207">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-208">92</span><span class="sxs-lookup"><span data-stu-id="072b0-208">92</span></span>

<span data-ttu-id="072b0-209">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="072b0-209">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-210">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="072b0-210">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-211">93</span><span class="sxs-lookup"><span data-stu-id="072b0-211">93</span></span>

<span data-ttu-id="072b0-212">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="072b0-212">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-213">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="072b0-213">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-214">94</span><span class="sxs-lookup"><span data-stu-id="072b0-214">94</span></span>

<span data-ttu-id="072b0-215">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="072b0-215">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-216">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="072b0-216">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-217">95</span><span class="sxs-lookup"><span data-stu-id="072b0-217">95</span></span>

<span data-ttu-id="072b0-218">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="072b0-218">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-219">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="072b0-219">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-220">96</span><span class="sxs-lookup"><span data-stu-id="072b0-220">96</span></span>

<span data-ttu-id="072b0-221">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="072b0-221">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-222">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="072b0-222">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-223">97</span><span class="sxs-lookup"><span data-stu-id="072b0-223">97</span></span>

<span data-ttu-id="072b0-224">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="072b0-224">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-225">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="072b0-225">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-226">98</span><span class="sxs-lookup"><span data-stu-id="072b0-226">98</span></span>

<span data-ttu-id="072b0-227">No todas las concesiones DHCP se liberan o se renuevan.</span><span class="sxs-lookup"><span data-stu-id="072b0-227">Not all DHCP leases are released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-228">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="072b0-228">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-229">100</span><span class="sxs-lookup"><span data-stu-id="072b0-229">100</span></span>

<span data-ttu-id="072b0-230">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="072b0-230">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="072b0-231">**Otros**</span><span class="sxs-lookup"><span data-stu-id="072b0-231">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="072b0-232">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="072b0-232">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="072b0-233">Observaciones</span><span class="sxs-lookup"><span data-stu-id="072b0-233">Remarks</span></span>

<span data-ttu-id="072b0-234">Se trata de una llamada independiente de la instancia que se aplica a todos los adaptadores, pero solo para Windows.</span><span class="sxs-lookup"><span data-stu-id="072b0-234">This is an instance-independent call that applies to all adapters but only for Windows.</span></span>

## <a name="examples"></a><span data-ttu-id="072b0-235">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="072b0-235">Examples</span></span>

<span data-ttu-id="072b0-236">El ejemplo de código [modificar el orden de búsqueda de sufijos DNS para todos los adaptadores de red de](https://Gallery.TechNet.Microsoft.Com/2857b7b0-1327-4ce2-9f2b-b662cce387c6) VBScript configura un equipo para que use dos sufijos DNS al realizar búsquedas de DNS.</span><span class="sxs-lookup"><span data-stu-id="072b0-236">The [Modify the DNS Suffix Search Order for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/2857b7b0-1327-4ce2-9f2b-b662cce387c6) VBScript code sample configures a computer to use two DNS suffixes when performing DNS searches.</span></span>

<span data-ttu-id="072b0-237">En el ejemplo de VBScript [Habilitar la configuración de DHCP en un equipo](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) se configuran todas las opciones que suelen ser necesarias para habilitar DHCP en un equipo.</span><span class="sxs-lookup"><span data-stu-id="072b0-237">The [Enable DHCP Settings on a Computer](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) VBScript sample configures all the settings typically required to enable DHCP on a computer.</span></span>

<span data-ttu-id="072b0-238">El siguiente código de PowerShell establece el orden de búsqueda de sufijos DNS.</span><span class="sxs-lookup"><span data-stu-id="072b0-238">The following PowerShell code sets the DNS suffix search order.</span></span>


```PowerShell
#First store the suffixes to set in a variable
$suffixes = 'microsoft.com', 'google.com', 'yahoo.com'

#Since this is a static method, get a class object and then call the method. 
$class = [wmiclass]'Win32_NetworkAdapterConfiguration'
$class.SetDNSSuffixSearchOrder($suffixes)
```



## <a name="requirements"></a><span data-ttu-id="072b0-239">Requisitos</span><span class="sxs-lookup"><span data-stu-id="072b0-239">Requirements</span></span>



| <span data-ttu-id="072b0-240">Requisito</span><span class="sxs-lookup"><span data-stu-id="072b0-240">Requirement</span></span> | <span data-ttu-id="072b0-241">Value</span><span class="sxs-lookup"><span data-stu-id="072b0-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="072b0-242">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="072b0-242">Minimum supported client</span></span><br/> | <span data-ttu-id="072b0-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="072b0-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="072b0-244">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="072b0-244">Minimum supported server</span></span><br/> | <span data-ttu-id="072b0-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="072b0-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="072b0-246">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="072b0-246">Namespace</span></span><br/>                | <span data-ttu-id="072b0-247">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="072b0-247">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="072b0-248">MOF</span><span class="sxs-lookup"><span data-stu-id="072b0-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="072b0-249"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="072b0-249"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="072b0-250">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="072b0-250">DLL</span></span><br/>                      | <dl> <span data-ttu-id="072b0-251"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="072b0-251"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="072b0-252">Vea también</span><span class="sxs-lookup"><span data-stu-id="072b0-252">See also</span></span>

<dl> <dt>

[<span data-ttu-id="072b0-253">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="072b0-253">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="072b0-254">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="072b0-254">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="072b0-255">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="072b0-255">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="072b0-256">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="072b0-256">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="072b0-257">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="072b0-257">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

