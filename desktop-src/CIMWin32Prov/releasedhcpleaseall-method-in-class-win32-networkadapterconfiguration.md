---
description: El método estático de la clase WMI ReleaseDHCPLeaseAll libera las direcciones IP enlazadas a todos los adaptadores de red habilitados para DHCP.
ms.assetid: d9f83953-f3da-419d-8c84-649c39b4945e
ms.tgt_platform: multiple
title: Método ReleaseDHCPLeaseAll de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.ReleaseDHCPLeaseAll
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3e7b1f7cf2f09fa20f7bf19b15e82f536ca0aa50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659683"
---
# <a name="releasedhcpleaseall-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="62e07-103">Método ReleaseDHCPLeaseAll de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="62e07-103">ReleaseDHCPLeaseAll method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="62e07-104">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ReleaseDHCPLeaseAll** libera las direcciones IP enlazadas a todos los adaptadores de red habilitados para DHCP.</span><span class="sxs-lookup"><span data-stu-id="62e07-104">The **ReleaseDHCPLeaseAll** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method releases the IP addresses bound to all DHCP-enabled network adapters.</span></span>

> [!Note]  
> <span data-ttu-id="62e07-105">ADVERTENCIA Si DHCP está habilitado en el sistema del equipo local, la opción terminará todas las conexiones TCP/IP de DHCP.</span><span class="sxs-lookup"><span data-stu-id="62e07-105">Warning If DHCP is enabled on the local computer system, the option will terminate all DHCP TCP/IP connections.</span></span>

 

<span data-ttu-id="62e07-106">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="62e07-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="62e07-107">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="62e07-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="62e07-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62e07-108">Syntax</span></span>


```mof
uint32 ReleaseDHCPLeaseAll();
```



## <a name="parameters"></a><span data-ttu-id="62e07-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62e07-109">Parameters</span></span>

<span data-ttu-id="62e07-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="62e07-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="62e07-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62e07-111">Return value</span></span>

<span data-ttu-id="62e07-112">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="62e07-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="62e07-113">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="62e07-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="62e07-114">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="62e07-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="62e07-115">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="62e07-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-116">0</span><span class="sxs-lookup"><span data-stu-id="62e07-116">0</span></span>

<span data-ttu-id="62e07-117">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="62e07-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-118">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="62e07-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-119">1</span><span class="sxs-lookup"><span data-stu-id="62e07-119">1</span></span>

<span data-ttu-id="62e07-120">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="62e07-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-121">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="62e07-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-122">64</span><span class="sxs-lookup"><span data-stu-id="62e07-122">64</span></span>

<span data-ttu-id="62e07-123">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="62e07-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-124">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="62e07-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-125">65</span><span class="sxs-lookup"><span data-stu-id="62e07-125">65</span></span>

<span data-ttu-id="62e07-126">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="62e07-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-127">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="62e07-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-128">66</span><span class="sxs-lookup"><span data-stu-id="62e07-128">66</span></span>

<span data-ttu-id="62e07-129">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="62e07-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-130">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="62e07-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-131">67</span><span class="sxs-lookup"><span data-stu-id="62e07-131">67</span></span>

<span data-ttu-id="62e07-132">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="62e07-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-133">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="62e07-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-134">68</span><span class="sxs-lookup"><span data-stu-id="62e07-134">68</span></span>

<span data-ttu-id="62e07-135">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="62e07-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-136">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="62e07-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-137">69</span><span class="sxs-lookup"><span data-stu-id="62e07-137">69</span></span>

<span data-ttu-id="62e07-138">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="62e07-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-139">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="62e07-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-140">70</span><span class="sxs-lookup"><span data-stu-id="62e07-140">70</span></span>

<span data-ttu-id="62e07-141">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="62e07-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-142">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="62e07-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-143">71</span><span class="sxs-lookup"><span data-stu-id="62e07-143">71</span></span>

<span data-ttu-id="62e07-144">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="62e07-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-145">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="62e07-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-146">72</span><span class="sxs-lookup"><span data-stu-id="62e07-146">72</span></span>

<span data-ttu-id="62e07-147">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="62e07-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-148">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="62e07-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-149">73</span><span class="sxs-lookup"><span data-stu-id="62e07-149">73</span></span>

<span data-ttu-id="62e07-150">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="62e07-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-151">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="62e07-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-152">74</span><span class="sxs-lookup"><span data-stu-id="62e07-152">74</span></span>

<span data-ttu-id="62e07-153">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="62e07-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-154">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="62e07-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-155">75</span><span class="sxs-lookup"><span data-stu-id="62e07-155">75</span></span>

<span data-ttu-id="62e07-156">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="62e07-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-157">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="62e07-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-158">76</span><span class="sxs-lookup"><span data-stu-id="62e07-158">76</span></span>

<span data-ttu-id="62e07-159">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="62e07-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-160">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="62e07-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-161">77</span><span class="sxs-lookup"><span data-stu-id="62e07-161">77</span></span>

<span data-ttu-id="62e07-162">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="62e07-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-163">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="62e07-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-164">78</span><span class="sxs-lookup"><span data-stu-id="62e07-164">78</span></span>

<span data-ttu-id="62e07-165">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="62e07-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-166">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="62e07-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-167">79</span><span class="sxs-lookup"><span data-stu-id="62e07-167">79</span></span>

<span data-ttu-id="62e07-168">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="62e07-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-169">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="62e07-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-170">80</span><span class="sxs-lookup"><span data-stu-id="62e07-170">80</span></span>

<span data-ttu-id="62e07-171">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="62e07-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-172">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="62e07-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-173">81</span><span class="sxs-lookup"><span data-stu-id="62e07-173">81</span></span>

<span data-ttu-id="62e07-174">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="62e07-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-175">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="62e07-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-176">82</span><span class="sxs-lookup"><span data-stu-id="62e07-176">82</span></span>

<span data-ttu-id="62e07-177">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="62e07-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-178">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="62e07-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-179">83</span><span class="sxs-lookup"><span data-stu-id="62e07-179">83</span></span>

<span data-ttu-id="62e07-180">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="62e07-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-181">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="62e07-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-182">84</span><span class="sxs-lookup"><span data-stu-id="62e07-182">84</span></span>

<span data-ttu-id="62e07-183">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="62e07-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-184">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="62e07-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-185">85</span><span class="sxs-lookup"><span data-stu-id="62e07-185">85</span></span>

<span data-ttu-id="62e07-186">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="62e07-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-187">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="62e07-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-188">86</span><span class="sxs-lookup"><span data-stu-id="62e07-188">86</span></span>

<span data-ttu-id="62e07-189">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="62e07-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-190">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="62e07-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-191">87</span><span class="sxs-lookup"><span data-stu-id="62e07-191">87</span></span>

<span data-ttu-id="62e07-192">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="62e07-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-193">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="62e07-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-194">88</span><span class="sxs-lookup"><span data-stu-id="62e07-194">88</span></span>

<span data-ttu-id="62e07-195">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="62e07-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-196">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="62e07-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-197">89</span><span class="sxs-lookup"><span data-stu-id="62e07-197">89</span></span>

<span data-ttu-id="62e07-198">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="62e07-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-199">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="62e07-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-200">90</span><span class="sxs-lookup"><span data-stu-id="62e07-200">90</span></span>

<span data-ttu-id="62e07-201">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="62e07-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-202">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="62e07-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-203">91</span><span class="sxs-lookup"><span data-stu-id="62e07-203">91</span></span>

<span data-ttu-id="62e07-204">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="62e07-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-205">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="62e07-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-206">92</span><span class="sxs-lookup"><span data-stu-id="62e07-206">92</span></span>

<span data-ttu-id="62e07-207">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="62e07-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-208">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="62e07-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-209">93</span><span class="sxs-lookup"><span data-stu-id="62e07-209">93</span></span>

<span data-ttu-id="62e07-210">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="62e07-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-211">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="62e07-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-212">94</span><span class="sxs-lookup"><span data-stu-id="62e07-212">94</span></span>

<span data-ttu-id="62e07-213">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="62e07-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-214">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="62e07-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-215">95</span><span class="sxs-lookup"><span data-stu-id="62e07-215">95</span></span>

<span data-ttu-id="62e07-216">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="62e07-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-217">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="62e07-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-218">96</span><span class="sxs-lookup"><span data-stu-id="62e07-218">96</span></span>

<span data-ttu-id="62e07-219">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="62e07-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-220">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="62e07-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-221">97</span><span class="sxs-lookup"><span data-stu-id="62e07-221">97</span></span>

<span data-ttu-id="62e07-222">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="62e07-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-223">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="62e07-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-224">98</span><span class="sxs-lookup"><span data-stu-id="62e07-224">98</span></span>

<span data-ttu-id="62e07-225">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="62e07-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-226">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="62e07-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-227">100</span><span class="sxs-lookup"><span data-stu-id="62e07-227">100</span></span>

<span data-ttu-id="62e07-228">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="62e07-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="62e07-229">**Otros**</span><span class="sxs-lookup"><span data-stu-id="62e07-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="62e07-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="62e07-230">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="62e07-231">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="62e07-231">Examples</span></span>

<span data-ttu-id="62e07-232">El siguiente ejemplo de código de VBScript libera todas las concesiones DHCP actualmente en uso en un equipo.</span><span class="sxs-lookup"><span data-stu-id="62e07-232">The following VBScript code sample releases all the DHCP leases currently in use on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objNetworkSettings = objWMIService.Get("Win32_NetworkAdapterConfiguration") 
objNetworkSettings.ReleaseDHCPLeaseAll() 
```



## <a name="requirements"></a><span data-ttu-id="62e07-233">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62e07-233">Requirements</span></span>



| <span data-ttu-id="62e07-234">Requisito</span><span class="sxs-lookup"><span data-stu-id="62e07-234">Requirement</span></span> | <span data-ttu-id="62e07-235">Value</span><span class="sxs-lookup"><span data-stu-id="62e07-235">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62e07-236">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62e07-236">Minimum supported client</span></span><br/> | <span data-ttu-id="62e07-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62e07-237">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="62e07-238">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62e07-238">Minimum supported server</span></span><br/> | <span data-ttu-id="62e07-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62e07-239">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="62e07-240">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="62e07-240">Namespace</span></span><br/>                | <span data-ttu-id="62e07-241">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="62e07-241">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="62e07-242">MOF</span><span class="sxs-lookup"><span data-stu-id="62e07-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62e07-243"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62e07-243"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="62e07-244">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="62e07-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62e07-245"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62e07-245"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62e07-246">Vea también</span><span class="sxs-lookup"><span data-stu-id="62e07-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62e07-247">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="62e07-247">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="62e07-248">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="62e07-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="62e07-249">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="62e07-249">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="62e07-250">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="62e07-250">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="62e07-251">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="62e07-251">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

