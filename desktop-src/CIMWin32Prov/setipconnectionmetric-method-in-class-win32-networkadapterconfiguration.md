---
description: El método SetIPConnectionMetric se usa para establecer la métrica de enrutamiento asociada a este adaptador de enlace de IP.
ms.assetid: d7f7c0df-51e3-4dc8-8a53-977ecde075df
ms.tgt_platform: multiple
title: Método SetIPConnectionMetric de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPConnectionMetric
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73d6dde0a8faea2aeaf0982459e3c377bb1ac51d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153220"
---
# <a name="setipconnectionmetric-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="ce2fb-103">Método SetIPConnectionMetric de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="ce2fb-103">SetIPConnectionMetric method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="ce2fb-104">El método **SetIPConnectionMetric** se usa para establecer la métrica de enrutamiento asociada a este adaptador de enlace de IP.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-104">The **SetIPConnectionMetric** method is used to set the routing metric associated with this IP-bound adapter.</span></span>

<span data-ttu-id="ce2fb-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="ce2fb-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ce2fb-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ce2fb-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ce2fb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce2fb-107">Syntax</span></span>


```mof
uint32 SetIPConnectionMetric(
  [in] uint32 IPConnectionMetric
);
```



## <a name="parameters"></a><span data-ttu-id="ce2fb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce2fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce2fb-109">*IPConnectionMetric* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ce2fb-109">*IPConnectionMetric* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-110">Indica el costo de usar las rutas configuradas para este adaptador de enlace de IP.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-110">Indicates the cost of using the configured routes for this IP-bound adapter.</span></span> <span data-ttu-id="ce2fb-111">El valor se pondera en las rutas de la tabla de enrutamiento IP.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-111">The value is weighted for those routes in the IP routing table.</span></span> <span data-ttu-id="ce2fb-112">Si hay varias rutas a un destino en la tabla de enrutamiento, se usa la ruta con la métrica más baja.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-112">If there are multiple routes to a destination in the routing table, the route with the lowest metric is used.</span></span> <span data-ttu-id="ce2fb-113">El intervalo de valores válidos es de 1 a 9999.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-113">The range of valid values is 1 through 9999.</span></span> <span data-ttu-id="ce2fb-114">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-114">The default value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce2fb-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce2fb-115">Return value</span></span>

<span data-ttu-id="ce2fb-116">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-116">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="ce2fb-117">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ce2fb-117">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ce2fb-118">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ce2fb-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ce2fb-119">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-119">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-120">0</span><span class="sxs-lookup"><span data-stu-id="ce2fb-120">0</span></span>

<span data-ttu-id="ce2fb-121">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-121">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-122">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-122">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-123">1</span><span class="sxs-lookup"><span data-stu-id="ce2fb-123">1</span></span>

<span data-ttu-id="ce2fb-124">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-124">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-125">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-125">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-126">64</span><span class="sxs-lookup"><span data-stu-id="ce2fb-126">64</span></span>

<span data-ttu-id="ce2fb-127">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-127">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-128">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-128">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-129">65</span><span class="sxs-lookup"><span data-stu-id="ce2fb-129">65</span></span>

<span data-ttu-id="ce2fb-130">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-130">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-131">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-131">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-132">66</span><span class="sxs-lookup"><span data-stu-id="ce2fb-132">66</span></span>

<span data-ttu-id="ce2fb-133">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-133">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-134">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-134">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-135">67</span><span class="sxs-lookup"><span data-stu-id="ce2fb-135">67</span></span>

<span data-ttu-id="ce2fb-136">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-136">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-137">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-137">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-138">68</span><span class="sxs-lookup"><span data-stu-id="ce2fb-138">68</span></span>

<span data-ttu-id="ce2fb-139">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-139">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-140">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-140">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-141">69</span><span class="sxs-lookup"><span data-stu-id="ce2fb-141">69</span></span>

<span data-ttu-id="ce2fb-142">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-142">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-143">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-143">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-144">70</span><span class="sxs-lookup"><span data-stu-id="ce2fb-144">70</span></span>

<span data-ttu-id="ce2fb-145">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-145">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-146">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-146">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-147">71</span><span class="sxs-lookup"><span data-stu-id="ce2fb-147">71</span></span>

<span data-ttu-id="ce2fb-148">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-148">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-149">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-149">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-150">72</span><span class="sxs-lookup"><span data-stu-id="ce2fb-150">72</span></span>

<span data-ttu-id="ce2fb-151">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-151">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-152">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-152">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-153">73</span><span class="sxs-lookup"><span data-stu-id="ce2fb-153">73</span></span>

<span data-ttu-id="ce2fb-154">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-154">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-155">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-155">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-156">74</span><span class="sxs-lookup"><span data-stu-id="ce2fb-156">74</span></span>

<span data-ttu-id="ce2fb-157">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-157">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-158">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-158">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-159">75</span><span class="sxs-lookup"><span data-stu-id="ce2fb-159">75</span></span>

<span data-ttu-id="ce2fb-160">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-160">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-161">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-161">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-162">76</span><span class="sxs-lookup"><span data-stu-id="ce2fb-162">76</span></span>

<span data-ttu-id="ce2fb-163">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-163">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-164">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-164">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-165">77</span><span class="sxs-lookup"><span data-stu-id="ce2fb-165">77</span></span>

<span data-ttu-id="ce2fb-166">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-166">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-167">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-167">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-168">78</span><span class="sxs-lookup"><span data-stu-id="ce2fb-168">78</span></span>

<span data-ttu-id="ce2fb-169">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-169">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-170">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-170">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-171">79</span><span class="sxs-lookup"><span data-stu-id="ce2fb-171">79</span></span>

<span data-ttu-id="ce2fb-172">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-172">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-173">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-173">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-174">80</span><span class="sxs-lookup"><span data-stu-id="ce2fb-174">80</span></span>

<span data-ttu-id="ce2fb-175">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-175">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-176">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-176">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-177">81</span><span class="sxs-lookup"><span data-stu-id="ce2fb-177">81</span></span>

<span data-ttu-id="ce2fb-178">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-178">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-179">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-179">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-180">82</span><span class="sxs-lookup"><span data-stu-id="ce2fb-180">82</span></span>

<span data-ttu-id="ce2fb-181">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-181">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-182">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-182">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-183">83</span><span class="sxs-lookup"><span data-stu-id="ce2fb-183">83</span></span>

<span data-ttu-id="ce2fb-184">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-184">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-185">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-185">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-186">84</span><span class="sxs-lookup"><span data-stu-id="ce2fb-186">84</span></span>

<span data-ttu-id="ce2fb-187">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-187">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-188">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-188">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-189">85</span><span class="sxs-lookup"><span data-stu-id="ce2fb-189">85</span></span>

<span data-ttu-id="ce2fb-190">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-190">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-191">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-191">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-192">86</span><span class="sxs-lookup"><span data-stu-id="ce2fb-192">86</span></span>

<span data-ttu-id="ce2fb-193">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-193">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-194">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-194">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-195">87</span><span class="sxs-lookup"><span data-stu-id="ce2fb-195">87</span></span>

<span data-ttu-id="ce2fb-196">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-196">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-197">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-197">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-198">88</span><span class="sxs-lookup"><span data-stu-id="ce2fb-198">88</span></span>

<span data-ttu-id="ce2fb-199">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-199">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-200">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-200">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-201">89</span><span class="sxs-lookup"><span data-stu-id="ce2fb-201">89</span></span>

<span data-ttu-id="ce2fb-202">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-202">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-203">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-203">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-204">90</span><span class="sxs-lookup"><span data-stu-id="ce2fb-204">90</span></span>

<span data-ttu-id="ce2fb-205">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-205">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-206">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-206">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-207">91</span><span class="sxs-lookup"><span data-stu-id="ce2fb-207">91</span></span>

<span data-ttu-id="ce2fb-208">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-208">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-209">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-209">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-210">92</span><span class="sxs-lookup"><span data-stu-id="ce2fb-210">92</span></span>

<span data-ttu-id="ce2fb-211">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="ce2fb-211">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-212">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-212">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-213">93</span><span class="sxs-lookup"><span data-stu-id="ce2fb-213">93</span></span>

<span data-ttu-id="ce2fb-214">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-214">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-215">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-215">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-216">94</span><span class="sxs-lookup"><span data-stu-id="ce2fb-216">94</span></span>

<span data-ttu-id="ce2fb-217">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-217">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-218">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-218">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-219">95</span><span class="sxs-lookup"><span data-stu-id="ce2fb-219">95</span></span>

<span data-ttu-id="ce2fb-220">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-220">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-221">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-221">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-222">96</span><span class="sxs-lookup"><span data-stu-id="ce2fb-222">96</span></span>

<span data-ttu-id="ce2fb-223">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-223">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-224">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-224">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-225">97</span><span class="sxs-lookup"><span data-stu-id="ce2fb-225">97</span></span>

<span data-ttu-id="ce2fb-226">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-226">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-227">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-227">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-228">98</span><span class="sxs-lookup"><span data-stu-id="ce2fb-228">98</span></span>

<span data-ttu-id="ce2fb-229">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-229">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-230">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-230">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-231">100</span><span class="sxs-lookup"><span data-stu-id="ce2fb-231">100</span></span>

<span data-ttu-id="ce2fb-232">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-232">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fb-233">**Otros**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-233">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="ce2fb-234">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="ce2fb-234">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="ce2fb-235">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ce2fb-235">Examples</span></span>

<span data-ttu-id="ce2fb-236">En el ejemplo de VBScript [modificar la métrica de conexión IP para un adaptador de red](https://Gallery.TechNet.Microsoft.Com/73367c75-7a39-44dc-a8d7-eb2359030969) se establece la métrica de conexión IP para un adaptador de red en 100.</span><span class="sxs-lookup"><span data-stu-id="ce2fb-236">The [Modify the IP Connection Metric for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/73367c75-7a39-44dc-a8d7-eb2359030969) VBScript sample sets the IP connection metric for a network adapter to 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce2fb-237">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce2fb-237">Requirements</span></span>



| <span data-ttu-id="ce2fb-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce2fb-238">Requirement</span></span> | <span data-ttu-id="ce2fb-239">Value</span><span class="sxs-lookup"><span data-stu-id="ce2fb-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce2fb-240">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce2fb-240">Minimum supported client</span></span><br/> | <span data-ttu-id="ce2fb-241">Windows Vista, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce2fb-241">Windows Vista, Windows Vista</span></span><br/>                                                 |
| <span data-ttu-id="ce2fb-242">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce2fb-242">Minimum supported server</span></span><br/> | <span data-ttu-id="ce2fb-243">Windows Server 2008, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce2fb-243">Windows Server 2008, Windows Server 2008</span></span><br/>                                     |
| <span data-ttu-id="ce2fb-244">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ce2fb-244">Namespace</span></span><br/>                | <span data-ttu-id="ce2fb-245">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ce2fb-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ce2fb-246">MOF</span><span class="sxs-lookup"><span data-stu-id="ce2fb-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce2fb-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ce2fb-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ce2fb-248">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ce2fb-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce2fb-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce2fb-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce2fb-250">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce2fb-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce2fb-251">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="ce2fb-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="ce2fb-252">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="ce2fb-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="ce2fb-253">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="ce2fb-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="ce2fb-254">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="ce2fb-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="ce2fb-255">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="ce2fb-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

