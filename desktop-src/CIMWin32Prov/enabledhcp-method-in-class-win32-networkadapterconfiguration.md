---
description: El método de clase de WMI EnableDHCP habilita el protocolo de configuración dinámica de host (DHCP) para el servicio con este adaptador de red. DHCP permite que las direcciones IP se asignen dinámicamente.
ms.assetid: 8c61d731-77a3-4ef4-bad9-26edaca60892
ms.tgt_platform: multiple
title: Método EnableDHCP de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableDHCP
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 002dedd3b0165053fea98dda035316676af638f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998238"
---
# <a name="enabledhcp-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="d215b-104">Método EnableDHCP de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="d215b-104">EnableDHCP method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="d215b-105">El método de [clase de WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableDHCP** habilita el protocolo de configuración dinámica de host (DHCP) para el servicio con este adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="d215b-105">The **EnableDHCP** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method enables the Dynamic Host Configuration Protocol (DHCP) for service with this network adapter.</span></span> <span data-ttu-id="d215b-106">DHCP permite que las direcciones IP se asignen dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="d215b-106">DHCP allows IP addresses to be dynamically allocated.</span></span>

<span data-ttu-id="d215b-107">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="d215b-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d215b-108">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d215b-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d215b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d215b-109">Syntax</span></span>


```mof
uint32 EnableDHCP();
```



## <a name="parameters"></a><span data-ttu-id="d215b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d215b-110">Parameters</span></span>

<span data-ttu-id="d215b-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d215b-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d215b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d215b-112">Return value</span></span>

<span data-ttu-id="d215b-113">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere un reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y cualquier otro número si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="d215b-113">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="d215b-114">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d215b-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d215b-115">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d215b-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d215b-116">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="d215b-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-117">0</span><span class="sxs-lookup"><span data-stu-id="d215b-117">0</span></span>

<span data-ttu-id="d215b-118">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="d215b-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-119">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="d215b-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-120">1</span><span class="sxs-lookup"><span data-stu-id="d215b-120">1</span></span>

<span data-ttu-id="d215b-121">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="d215b-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-122">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="d215b-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-123">64</span><span class="sxs-lookup"><span data-stu-id="d215b-123">64</span></span>

<span data-ttu-id="d215b-124">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="d215b-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-125">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="d215b-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-126">65</span><span class="sxs-lookup"><span data-stu-id="d215b-126">65</span></span>

<span data-ttu-id="d215b-127">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="d215b-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-128">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="d215b-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-129">66</span><span class="sxs-lookup"><span data-stu-id="d215b-129">66</span></span>

<span data-ttu-id="d215b-130">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="d215b-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-131">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="d215b-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-132">67</span><span class="sxs-lookup"><span data-stu-id="d215b-132">67</span></span>

<span data-ttu-id="d215b-133">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="d215b-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-134">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="d215b-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-135">68</span><span class="sxs-lookup"><span data-stu-id="d215b-135">68</span></span>

<span data-ttu-id="d215b-136">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="d215b-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-137">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="d215b-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-138">69</span><span class="sxs-lookup"><span data-stu-id="d215b-138">69</span></span>

<span data-ttu-id="d215b-139">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="d215b-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-140">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="d215b-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-141">70</span><span class="sxs-lookup"><span data-stu-id="d215b-141">70</span></span>

<span data-ttu-id="d215b-142">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="d215b-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-143">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="d215b-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-144">71</span><span class="sxs-lookup"><span data-stu-id="d215b-144">71</span></span>

<span data-ttu-id="d215b-145">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="d215b-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-146">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="d215b-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-147">72</span><span class="sxs-lookup"><span data-stu-id="d215b-147">72</span></span>

<span data-ttu-id="d215b-148">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="d215b-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-149">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="d215b-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-150">73</span><span class="sxs-lookup"><span data-stu-id="d215b-150">73</span></span>

<span data-ttu-id="d215b-151">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="d215b-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-152">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="d215b-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-153">74</span><span class="sxs-lookup"><span data-stu-id="d215b-153">74</span></span>

<span data-ttu-id="d215b-154">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="d215b-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-155">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="d215b-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-156">75</span><span class="sxs-lookup"><span data-stu-id="d215b-156">75</span></span>

<span data-ttu-id="d215b-157">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="d215b-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-158">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="d215b-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-159">76</span><span class="sxs-lookup"><span data-stu-id="d215b-159">76</span></span>

<span data-ttu-id="d215b-160">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="d215b-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-161">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="d215b-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-162">77</span><span class="sxs-lookup"><span data-stu-id="d215b-162">77</span></span>

<span data-ttu-id="d215b-163">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="d215b-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-164">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="d215b-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-165">78</span><span class="sxs-lookup"><span data-stu-id="d215b-165">78</span></span>

<span data-ttu-id="d215b-166">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="d215b-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-167">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="d215b-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-168">79</span><span class="sxs-lookup"><span data-stu-id="d215b-168">79</span></span>

<span data-ttu-id="d215b-169">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="d215b-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-170">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="d215b-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-171">80</span><span class="sxs-lookup"><span data-stu-id="d215b-171">80</span></span>

<span data-ttu-id="d215b-172">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d215b-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-173">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="d215b-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-174">81</span><span class="sxs-lookup"><span data-stu-id="d215b-174">81</span></span>

<span data-ttu-id="d215b-175">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="d215b-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-176">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="d215b-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-177">82</span><span class="sxs-lookup"><span data-stu-id="d215b-177">82</span></span>

<span data-ttu-id="d215b-178">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="d215b-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-179">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="d215b-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-180">83</span><span class="sxs-lookup"><span data-stu-id="d215b-180">83</span></span>

<span data-ttu-id="d215b-181">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="d215b-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-182">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="d215b-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-183">84</span><span class="sxs-lookup"><span data-stu-id="d215b-183">84</span></span>

<span data-ttu-id="d215b-184">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="d215b-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-185">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="d215b-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-186">85</span><span class="sxs-lookup"><span data-stu-id="d215b-186">85</span></span>

<span data-ttu-id="d215b-187">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="d215b-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-188">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="d215b-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-189">86</span><span class="sxs-lookup"><span data-stu-id="d215b-189">86</span></span>

<span data-ttu-id="d215b-190">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="d215b-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-191">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="d215b-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-192">87</span><span class="sxs-lookup"><span data-stu-id="d215b-192">87</span></span>

<span data-ttu-id="d215b-193">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="d215b-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-194">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="d215b-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-195">88</span><span class="sxs-lookup"><span data-stu-id="d215b-195">88</span></span>

<span data-ttu-id="d215b-196">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="d215b-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-197">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="d215b-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-198">89</span><span class="sxs-lookup"><span data-stu-id="d215b-198">89</span></span>

<span data-ttu-id="d215b-199">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="d215b-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-200">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="d215b-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-201">90</span><span class="sxs-lookup"><span data-stu-id="d215b-201">90</span></span>

<span data-ttu-id="d215b-202">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="d215b-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-203">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="d215b-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-204">91</span><span class="sxs-lookup"><span data-stu-id="d215b-204">91</span></span>

<span data-ttu-id="d215b-205">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="d215b-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-206">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="d215b-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-207">92</span><span class="sxs-lookup"><span data-stu-id="d215b-207">92</span></span>

<span data-ttu-id="d215b-208">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="d215b-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-209">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="d215b-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-210">93</span><span class="sxs-lookup"><span data-stu-id="d215b-210">93</span></span>

<span data-ttu-id="d215b-211">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="d215b-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-212">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="d215b-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-213">94</span><span class="sxs-lookup"><span data-stu-id="d215b-213">94</span></span>

<span data-ttu-id="d215b-214">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="d215b-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-215">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="d215b-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-216">95</span><span class="sxs-lookup"><span data-stu-id="d215b-216">95</span></span>

<span data-ttu-id="d215b-217">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="d215b-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-218">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="d215b-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-219">96</span><span class="sxs-lookup"><span data-stu-id="d215b-219">96</span></span>

<span data-ttu-id="d215b-220">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="d215b-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-221">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="d215b-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-222">97</span><span class="sxs-lookup"><span data-stu-id="d215b-222">97</span></span>

<span data-ttu-id="d215b-223">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="d215b-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-224">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="d215b-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-225">98</span><span class="sxs-lookup"><span data-stu-id="d215b-225">98</span></span>

<span data-ttu-id="d215b-226">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="d215b-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-227">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="d215b-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-228">100</span><span class="sxs-lookup"><span data-stu-id="d215b-228">100</span></span>

<span data-ttu-id="d215b-229">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="d215b-229">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d215b-230">**Otros**</span><span class="sxs-lookup"><span data-stu-id="d215b-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="d215b-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="d215b-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d215b-232">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d215b-232">Remarks</span></span>

<span data-ttu-id="d215b-233">Este método no borra las puertas de enlace predeterminadas estáticas presentes en la máquina.</span><span class="sxs-lookup"><span data-stu-id="d215b-233">This method does not clears any static default gateways present on the machine.</span></span>

## <a name="examples"></a><span data-ttu-id="d215b-234">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d215b-234">Examples</span></span>

<span data-ttu-id="d215b-235">En el ejemplo de código de VBScript [Habilitar DHCP y asignar servidores DNS](https://Gallery.TechNet.Microsoft.Com/7b1cec46-bdb8-4afc-b240-9789eefce6de) en la galería de TechNet se usa EnableDHCP para habilitar DHCP y asignar servidores DNS a un equipo.</span><span class="sxs-lookup"><span data-stu-id="d215b-235">The [Enable DHCP and Assign DNS Servers](https://Gallery.TechNet.Microsoft.Com/7b1cec46-bdb8-4afc-b240-9789eefce6de) VBScript code sample on TechNet Gallery uses EnableDHCP to enable DHCP and assign DNS servers to a computer.</span></span>

<span data-ttu-id="d215b-236">El siguiente ejemplo de código VBScript muestra cómo habilitar el uso de DHCP en una instancia de [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="d215b-236">The following VBScript code sample demonstrates how to enable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span></span> <span data-ttu-id="d215b-237">En este caso, especificamos el adaptador con un índice de 0.</span><span class="sxs-lookup"><span data-stu-id="d215b-237">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="d215b-238">Se debe seleccionar el índice correcto en \_ las instancias de Win32 para otras interfaces.</span><span class="sxs-lookup"><span data-stu-id="d215b-238">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="d215b-239">Solo se admite en plataformas NT.</span><span class="sxs-lookup"><span data-stu-id="d215b-239">Supported on NT platforms only.</span></span>

 


```VB
Set Adapter = GetObject("winmgmts:Win32_NetworkAdapterConfiguration=0")

RetVal = Adapter.EnableDHCP()

if RetVal = 0 then 
 WScript.Echo "DHCP Enabled"
else 
 WScript.Echo "DHCP enable failed"
end if
```



<span data-ttu-id="d215b-240">El siguiente ejemplo de código Perl muestra cómo habilitar el uso de DHCP en una instancia de [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="d215b-240">The following Perl code sample demonstrates how to enable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span></span> <span data-ttu-id="d215b-241">En este caso, especificamos el adaptador con un índice de 0.</span><span class="sxs-lookup"><span data-stu-id="d215b-241">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="d215b-242">Se debe seleccionar el índice correcto en \_ las instancias de Win32 para otras interfaces.</span><span class="sxs-lookup"><span data-stu-id="d215b-242">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="d215b-243">Solo se admite en plataformas NT.</span><span class="sxs-lookup"><span data-stu-id="d215b-243">Supported on NT platforms only.</span></span>

 


```
use strict;
use Win32::OLE;

my ( $Adapter, $RetVal );

eval { $Adapter = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
       Get("Win32_NetworkAdapterConfiguration=0"); };
unless ($@)
{
 print "\n";
 $RetVal = $Adapter->EnableDHCP();
 if ( $RetVal == 0)
 {
  print "DHCP Enabled\n";
 }
 else
 {
  print "DHCP enable failed\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="d215b-244">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d215b-244">Requirements</span></span>



| <span data-ttu-id="d215b-245">Requisito</span><span class="sxs-lookup"><span data-stu-id="d215b-245">Requirement</span></span> | <span data-ttu-id="d215b-246">Value</span><span class="sxs-lookup"><span data-stu-id="d215b-246">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d215b-247">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d215b-247">Minimum supported client</span></span><br/> | <span data-ttu-id="d215b-248">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d215b-248">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d215b-249">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d215b-249">Minimum supported server</span></span><br/> | <span data-ttu-id="d215b-250">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d215b-250">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d215b-251">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d215b-251">Namespace</span></span><br/>                | <span data-ttu-id="d215b-252">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d215b-252">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d215b-253">MOF</span><span class="sxs-lookup"><span data-stu-id="d215b-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d215b-254"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d215b-254"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d215b-255">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d215b-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d215b-256"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d215b-256"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d215b-257">Vea también</span><span class="sxs-lookup"><span data-stu-id="d215b-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d215b-258">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="d215b-258">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d215b-259">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="d215b-259">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="d215b-260">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="d215b-260">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="d215b-261">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="d215b-261">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="d215b-262">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="d215b-262">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

