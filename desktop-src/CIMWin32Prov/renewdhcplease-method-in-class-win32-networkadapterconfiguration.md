---
description: El método de clase WMI RenewDHCPLease renueva la dirección IP en determinados adaptadores de red habilitados para DHCP.
ms.assetid: b6e5d1fb-db3f-4491-bbac-46b1f2e7206e
ms.tgt_platform: multiple
title: Método RenewDHCPLease de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.RenewDHCPLease
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4603f013c6b4c2c80edd555608b5f59325b6a6d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080296"
---
# <a name="renewdhcplease-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="903de-103">Método RenewDHCPLease de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="903de-103">RenewDHCPLease method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="903de-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **RenewDHCPLease** renueva la dirección IP en determinados adaptadores de red habilitados para DHCP.</span><span class="sxs-lookup"><span data-stu-id="903de-104">The **RenewDHCPLease** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renews the IP address on specific DHCP-enabled network adapters.</span></span>

<span data-ttu-id="903de-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="903de-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="903de-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="903de-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="903de-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="903de-107">Syntax</span></span>


```mof
uint32 RenewDHCPLease();
```



## <a name="parameters"></a><span data-ttu-id="903de-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="903de-108">Parameters</span></span>

<span data-ttu-id="903de-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="903de-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="903de-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="903de-110">Return value</span></span>

<span data-ttu-id="903de-111">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="903de-111">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="903de-112">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="903de-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="903de-113">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="903de-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="903de-114">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="903de-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="903de-115">0</span><span class="sxs-lookup"><span data-stu-id="903de-115">0</span></span>

<span data-ttu-id="903de-116">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="903de-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="903de-117">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="903de-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="903de-118">1</span><span class="sxs-lookup"><span data-stu-id="903de-118">1</span></span>

<span data-ttu-id="903de-119">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="903de-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="903de-120">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="903de-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="903de-121">64</span><span class="sxs-lookup"><span data-stu-id="903de-121">64</span></span>

<span data-ttu-id="903de-122">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="903de-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="903de-123">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="903de-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="903de-124">65</span><span class="sxs-lookup"><span data-stu-id="903de-124">65</span></span>

<span data-ttu-id="903de-125">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="903de-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="903de-126">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="903de-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="903de-127">66</span><span class="sxs-lookup"><span data-stu-id="903de-127">66</span></span>

<span data-ttu-id="903de-128">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="903de-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="903de-129">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="903de-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="903de-130">67</span><span class="sxs-lookup"><span data-stu-id="903de-130">67</span></span>

<span data-ttu-id="903de-131">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="903de-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="903de-132">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="903de-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="903de-133">68</span><span class="sxs-lookup"><span data-stu-id="903de-133">68</span></span>

<span data-ttu-id="903de-134">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="903de-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="903de-135">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="903de-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="903de-136">69</span><span class="sxs-lookup"><span data-stu-id="903de-136">69</span></span>

<span data-ttu-id="903de-137">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="903de-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="903de-138">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="903de-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="903de-139">70</span><span class="sxs-lookup"><span data-stu-id="903de-139">70</span></span>

<span data-ttu-id="903de-140">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="903de-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="903de-141">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="903de-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="903de-142">71</span><span class="sxs-lookup"><span data-stu-id="903de-142">71</span></span>

<span data-ttu-id="903de-143">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="903de-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="903de-144">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="903de-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="903de-145">72</span><span class="sxs-lookup"><span data-stu-id="903de-145">72</span></span>

<span data-ttu-id="903de-146">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="903de-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="903de-147">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="903de-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="903de-148">73</span><span class="sxs-lookup"><span data-stu-id="903de-148">73</span></span>

<span data-ttu-id="903de-149">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="903de-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="903de-150">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="903de-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="903de-151">74</span><span class="sxs-lookup"><span data-stu-id="903de-151">74</span></span>

<span data-ttu-id="903de-152">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="903de-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="903de-153">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="903de-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="903de-154">75</span><span class="sxs-lookup"><span data-stu-id="903de-154">75</span></span>

<span data-ttu-id="903de-155">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="903de-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="903de-156">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="903de-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="903de-157">76</span><span class="sxs-lookup"><span data-stu-id="903de-157">76</span></span>

<span data-ttu-id="903de-158">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="903de-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="903de-159">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="903de-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="903de-160">77</span><span class="sxs-lookup"><span data-stu-id="903de-160">77</span></span>

<span data-ttu-id="903de-161">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="903de-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="903de-162">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="903de-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="903de-163">78</span><span class="sxs-lookup"><span data-stu-id="903de-163">78</span></span>

<span data-ttu-id="903de-164">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="903de-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="903de-165">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="903de-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="903de-166">79</span><span class="sxs-lookup"><span data-stu-id="903de-166">79</span></span>

<span data-ttu-id="903de-167">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="903de-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="903de-168">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="903de-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="903de-169">80</span><span class="sxs-lookup"><span data-stu-id="903de-169">80</span></span>

<span data-ttu-id="903de-170">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="903de-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="903de-171">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="903de-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="903de-172">81</span><span class="sxs-lookup"><span data-stu-id="903de-172">81</span></span>

<span data-ttu-id="903de-173">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="903de-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="903de-174">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="903de-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="903de-175">82</span><span class="sxs-lookup"><span data-stu-id="903de-175">82</span></span>

<span data-ttu-id="903de-176">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="903de-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="903de-177">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="903de-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="903de-178">83</span><span class="sxs-lookup"><span data-stu-id="903de-178">83</span></span>

<span data-ttu-id="903de-179">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="903de-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="903de-180">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="903de-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="903de-181">84</span><span class="sxs-lookup"><span data-stu-id="903de-181">84</span></span>

<span data-ttu-id="903de-182">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="903de-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="903de-183">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="903de-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="903de-184">85</span><span class="sxs-lookup"><span data-stu-id="903de-184">85</span></span>

<span data-ttu-id="903de-185">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="903de-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="903de-186">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="903de-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="903de-187">86</span><span class="sxs-lookup"><span data-stu-id="903de-187">86</span></span>

<span data-ttu-id="903de-188">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="903de-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="903de-189">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="903de-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="903de-190">87</span><span class="sxs-lookup"><span data-stu-id="903de-190">87</span></span>

<span data-ttu-id="903de-191">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="903de-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="903de-192">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="903de-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="903de-193">88</span><span class="sxs-lookup"><span data-stu-id="903de-193">88</span></span>

<span data-ttu-id="903de-194">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="903de-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="903de-195">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="903de-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="903de-196">89</span><span class="sxs-lookup"><span data-stu-id="903de-196">89</span></span>

<span data-ttu-id="903de-197">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="903de-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="903de-198">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="903de-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="903de-199">90</span><span class="sxs-lookup"><span data-stu-id="903de-199">90</span></span>

<span data-ttu-id="903de-200">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="903de-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="903de-201">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="903de-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="903de-202">91</span><span class="sxs-lookup"><span data-stu-id="903de-202">91</span></span>

<span data-ttu-id="903de-203">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="903de-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="903de-204">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="903de-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="903de-205">92</span><span class="sxs-lookup"><span data-stu-id="903de-205">92</span></span>

<span data-ttu-id="903de-206">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="903de-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="903de-207">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="903de-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="903de-208">93</span><span class="sxs-lookup"><span data-stu-id="903de-208">93</span></span>

<span data-ttu-id="903de-209">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="903de-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="903de-210">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="903de-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="903de-211">94</span><span class="sxs-lookup"><span data-stu-id="903de-211">94</span></span>

<span data-ttu-id="903de-212">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="903de-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="903de-213">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="903de-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="903de-214">95</span><span class="sxs-lookup"><span data-stu-id="903de-214">95</span></span>

<span data-ttu-id="903de-215">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="903de-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="903de-216">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="903de-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="903de-217">96</span><span class="sxs-lookup"><span data-stu-id="903de-217">96</span></span>

<span data-ttu-id="903de-218">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="903de-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="903de-219">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="903de-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="903de-220">97</span><span class="sxs-lookup"><span data-stu-id="903de-220">97</span></span>

<span data-ttu-id="903de-221">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="903de-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="903de-222">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="903de-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="903de-223">98</span><span class="sxs-lookup"><span data-stu-id="903de-223">98</span></span>

<span data-ttu-id="903de-224">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="903de-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="903de-225">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="903de-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="903de-226">100</span><span class="sxs-lookup"><span data-stu-id="903de-226">100</span></span>

<span data-ttu-id="903de-227">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="903de-227">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="903de-228">**Otros**</span><span class="sxs-lookup"><span data-stu-id="903de-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="903de-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="903de-229">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="903de-230">Observaciones</span><span class="sxs-lookup"><span data-stu-id="903de-230">Remarks</span></span>

<span data-ttu-id="903de-231">La concesión de la dirección IP asignada por un servidor DHCP tiene una fecha de expiración que el cliente debe renovar si intenta seguir usando la dirección IP asignada.</span><span class="sxs-lookup"><span data-stu-id="903de-231">The lease for the IP address assigned by a DHCP server has an expiration date that the client must renew if it intends to continue use of the assigned IP address.</span></span>

## <a name="examples"></a><span data-ttu-id="903de-232">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="903de-232">Examples</span></span>

<span data-ttu-id="903de-233">En el ejemplo [Release Renew IP Addressing Using PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell en la galería de TechNet se usa **RenewDHCPLease** para liberar y renovar una dirección IP.</span><span class="sxs-lookup"><span data-stu-id="903de-233">The [Release Renew IP Adresses Using PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell example on TechNet Gallery uses **RenewDHCPLease** to release and renew an IP address.</span></span>

<span data-ttu-id="903de-234">En el ejemplo de VBScript [renueva concesión de DHCP para un adaptador de red](https://Gallery.TechNet.Microsoft.Com/39443fd7-0152-4c0a-89e9-e2753049b203) de la galería de TechNet se usa **RenewDHCPLease** para renovar la concesión DHCP de cada adaptador de red enlazado a TCP/IP en un equipo.</span><span class="sxs-lookup"><span data-stu-id="903de-234">The [Renew the DHCP Lease for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/39443fd7-0152-4c0a-89e9-e2753049b203) VBScript sample on TechNet Gallery uses **RenewDHCPLease** to renew the DHCP lease for each TCP/IP-bound network adapter in a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="903de-235">Requisitos</span><span class="sxs-lookup"><span data-stu-id="903de-235">Requirements</span></span>



| <span data-ttu-id="903de-236">Requisito</span><span class="sxs-lookup"><span data-stu-id="903de-236">Requirement</span></span> | <span data-ttu-id="903de-237">Value</span><span class="sxs-lookup"><span data-stu-id="903de-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="903de-238">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="903de-238">Minimum supported client</span></span><br/> | <span data-ttu-id="903de-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="903de-239">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="903de-240">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="903de-240">Minimum supported server</span></span><br/> | <span data-ttu-id="903de-241">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="903de-241">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="903de-242">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="903de-242">Namespace</span></span><br/>                | <span data-ttu-id="903de-243">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="903de-243">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="903de-244">MOF</span><span class="sxs-lookup"><span data-stu-id="903de-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="903de-245"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="903de-245"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="903de-246">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="903de-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="903de-247"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="903de-247"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="903de-248">Vea también</span><span class="sxs-lookup"><span data-stu-id="903de-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="903de-249">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="903de-249">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="903de-250">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="903de-250">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="903de-251">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="903de-251">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="903de-252">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="903de-252">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="903de-253">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="903de-253">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

