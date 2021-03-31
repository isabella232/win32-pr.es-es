---
description: El método estático de la clase WMI SetMTU se usa para establecer la unidad de transmisión máxima (MTU) predeterminada para una interfaz de red.
ms.assetid: 262c8bd7-1057-4204-80ab-725c60fc9c52
ms.tgt_platform: multiple
title: Método SetMTU de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetMTU
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 466c344892f2c4bf4a1e979ac9c1f50cd709325a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807579"
---
# <a name="setmtu-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="614ce-103">Método SetMTU de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="614ce-103">SetMTU method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="614ce-104">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetMTU** se usa para establecer la unidad de transmisión máxima (MTU) predeterminada para una interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="614ce-104">The **SetMTU** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the default Maximum Transmission Unit (MTU) for a network interface.</span></span>

<span data-ttu-id="614ce-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="614ce-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="614ce-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="614ce-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="614ce-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="614ce-107">Syntax</span></span>


```mof
uint32 SetMTU(
  [in] uint32 MTU
);
```



## <a name="parameters"></a><span data-ttu-id="614ce-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="614ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="614ce-109">*MTU* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="614ce-109">*MTU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="614ce-110">Unidad de transmisión máxima (MTU) predeterminada para una interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="614ce-110">Default Maximum Transmission Unit (MTU) for a network interface.</span></span> <span data-ttu-id="614ce-111">El intervalo de este valor abarca el tamaño de paquete mínimo (68) a la MTU compatible con la red subyacente.</span><span class="sxs-lookup"><span data-stu-id="614ce-111">The range of this value spans the minimum packet size (68) to the MTU supported by the underlying network.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="614ce-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="614ce-112">Return value</span></span>

<span data-ttu-id="614ce-113">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="614ce-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="614ce-114">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="614ce-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="614ce-115">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="614ce-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="614ce-116">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="614ce-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-117">0</span><span class="sxs-lookup"><span data-stu-id="614ce-117">0</span></span>

<span data-ttu-id="614ce-118">Finalización correcta.</span><span class="sxs-lookup"><span data-stu-id="614ce-118">Successful completion.</span></span> <span data-ttu-id="614ce-119">No es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="614ce-119">No reboot is required.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-120">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="614ce-120">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-121">1</span><span class="sxs-lookup"><span data-stu-id="614ce-121">1</span></span>

<span data-ttu-id="614ce-122">Finalización correcta.</span><span class="sxs-lookup"><span data-stu-id="614ce-122">Successful completion.</span></span> <span data-ttu-id="614ce-123">Es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="614ce-123">Reboot is required.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-124">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="614ce-124">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-125">64</span><span class="sxs-lookup"><span data-stu-id="614ce-125">64</span></span>

<span data-ttu-id="614ce-126">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="614ce-126">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-127">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="614ce-127">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-128">65</span><span class="sxs-lookup"><span data-stu-id="614ce-128">65</span></span>

<span data-ttu-id="614ce-129">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="614ce-129">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-130">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="614ce-130">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-131">66</span><span class="sxs-lookup"><span data-stu-id="614ce-131">66</span></span>

<span data-ttu-id="614ce-132">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="614ce-132">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-133">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="614ce-133">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-134">67</span><span class="sxs-lookup"><span data-stu-id="614ce-134">67</span></span>

<span data-ttu-id="614ce-135">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="614ce-135">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-136">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="614ce-136">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-137">68</span><span class="sxs-lookup"><span data-stu-id="614ce-137">68</span></span>

<span data-ttu-id="614ce-138">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="614ce-138">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-139">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="614ce-139">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-140">69</span><span class="sxs-lookup"><span data-stu-id="614ce-140">69</span></span>

<span data-ttu-id="614ce-141">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="614ce-141">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-142">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="614ce-142">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-143">70</span><span class="sxs-lookup"><span data-stu-id="614ce-143">70</span></span>

<span data-ttu-id="614ce-144">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="614ce-144">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-145">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="614ce-145">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-146">71</span><span class="sxs-lookup"><span data-stu-id="614ce-146">71</span></span>

<span data-ttu-id="614ce-147">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="614ce-147">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-148">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="614ce-148">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-149">72</span><span class="sxs-lookup"><span data-stu-id="614ce-149">72</span></span>

<span data-ttu-id="614ce-150">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="614ce-150">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-151">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="614ce-151">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-152">73</span><span class="sxs-lookup"><span data-stu-id="614ce-152">73</span></span>

<span data-ttu-id="614ce-153">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="614ce-153">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-154">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="614ce-154">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-155">74</span><span class="sxs-lookup"><span data-stu-id="614ce-155">74</span></span>

<span data-ttu-id="614ce-156">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="614ce-156">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-157">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="614ce-157">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-158">75</span><span class="sxs-lookup"><span data-stu-id="614ce-158">75</span></span>

<span data-ttu-id="614ce-159">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="614ce-159">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-160">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="614ce-160">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-161">76</span><span class="sxs-lookup"><span data-stu-id="614ce-161">76</span></span>

<span data-ttu-id="614ce-162">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="614ce-162">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-163">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="614ce-163">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-164">77</span><span class="sxs-lookup"><span data-stu-id="614ce-164">77</span></span>

<span data-ttu-id="614ce-165">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="614ce-165">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-166">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="614ce-166">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-167">78</span><span class="sxs-lookup"><span data-stu-id="614ce-167">78</span></span>

<span data-ttu-id="614ce-168">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="614ce-168">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-169">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="614ce-169">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-170">79</span><span class="sxs-lookup"><span data-stu-id="614ce-170">79</span></span>

<span data-ttu-id="614ce-171">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="614ce-171">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-172">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="614ce-172">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-173">80</span><span class="sxs-lookup"><span data-stu-id="614ce-173">80</span></span>

<span data-ttu-id="614ce-174">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="614ce-174">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-175">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="614ce-175">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-176">81</span><span class="sxs-lookup"><span data-stu-id="614ce-176">81</span></span>

<span data-ttu-id="614ce-177">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="614ce-177">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-178">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="614ce-178">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-179">82</span><span class="sxs-lookup"><span data-stu-id="614ce-179">82</span></span>

<span data-ttu-id="614ce-180">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="614ce-180">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-181">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="614ce-181">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-182">83</span><span class="sxs-lookup"><span data-stu-id="614ce-182">83</span></span>

<span data-ttu-id="614ce-183">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="614ce-183">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-184">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="614ce-184">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-185">84</span><span class="sxs-lookup"><span data-stu-id="614ce-185">84</span></span>

<span data-ttu-id="614ce-186">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="614ce-186">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-187">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="614ce-187">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-188">85</span><span class="sxs-lookup"><span data-stu-id="614ce-188">85</span></span>

<span data-ttu-id="614ce-189">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="614ce-189">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-190">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="614ce-190">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-191">86</span><span class="sxs-lookup"><span data-stu-id="614ce-191">86</span></span>

<span data-ttu-id="614ce-192">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="614ce-192">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-193">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="614ce-193">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-194">87</span><span class="sxs-lookup"><span data-stu-id="614ce-194">87</span></span>

<span data-ttu-id="614ce-195">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="614ce-195">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-196">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="614ce-196">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-197">88</span><span class="sxs-lookup"><span data-stu-id="614ce-197">88</span></span>

<span data-ttu-id="614ce-198">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="614ce-198">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-199">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="614ce-199">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-200">89</span><span class="sxs-lookup"><span data-stu-id="614ce-200">89</span></span>

<span data-ttu-id="614ce-201">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="614ce-201">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-202">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="614ce-202">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-203">90</span><span class="sxs-lookup"><span data-stu-id="614ce-203">90</span></span>

<span data-ttu-id="614ce-204">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="614ce-204">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-205">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="614ce-205">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-206">91</span><span class="sxs-lookup"><span data-stu-id="614ce-206">91</span></span>

<span data-ttu-id="614ce-207">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="614ce-207">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-208">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="614ce-208">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-209">92</span><span class="sxs-lookup"><span data-stu-id="614ce-209">92</span></span>

<span data-ttu-id="614ce-210">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="614ce-210">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-211">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="614ce-211">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-212">93</span><span class="sxs-lookup"><span data-stu-id="614ce-212">93</span></span>

<span data-ttu-id="614ce-213">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="614ce-213">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-214">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="614ce-214">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-215">94</span><span class="sxs-lookup"><span data-stu-id="614ce-215">94</span></span>

<span data-ttu-id="614ce-216">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="614ce-216">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-217">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="614ce-217">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-218">95</span><span class="sxs-lookup"><span data-stu-id="614ce-218">95</span></span>

<span data-ttu-id="614ce-219">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="614ce-219">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-220">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="614ce-220">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-221">96</span><span class="sxs-lookup"><span data-stu-id="614ce-221">96</span></span>

<span data-ttu-id="614ce-222">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="614ce-222">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-223">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="614ce-223">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-224">97</span><span class="sxs-lookup"><span data-stu-id="614ce-224">97</span></span>

<span data-ttu-id="614ce-225">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="614ce-225">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-226">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="614ce-226">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-227">98</span><span class="sxs-lookup"><span data-stu-id="614ce-227">98</span></span>

<span data-ttu-id="614ce-228">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="614ce-228">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-229">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="614ce-229">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-230">100</span><span class="sxs-lookup"><span data-stu-id="614ce-230">100</span></span>

<span data-ttu-id="614ce-231">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="614ce-231">DHCP is not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="614ce-232">**Otros**</span><span class="sxs-lookup"><span data-stu-id="614ce-232">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="614ce-233">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="614ce-233">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="614ce-234">Observaciones</span><span class="sxs-lookup"><span data-stu-id="614ce-234">Remarks</span></span>

<span data-ttu-id="614ce-235">La MTU es el tamaño de paquete máximo (en bytes) que un transporte transmitirá a través de la red subyacente.</span><span class="sxs-lookup"><span data-stu-id="614ce-235">The MTU is the maximum packet size (in bytes) that a transport will transmit over the underlying network.</span></span> <span data-ttu-id="614ce-236">El tamaño incluye el encabezado de transporte.</span><span class="sxs-lookup"><span data-stu-id="614ce-236">The size includes the transport header.</span></span>

<span data-ttu-id="614ce-237">Tenga en cuenta que un datagrama IP puede abarcar varios paquetes.</span><span class="sxs-lookup"><span data-stu-id="614ce-237">Note that an IP datagram can span multiple packets.</span></span> <span data-ttu-id="614ce-238">Los valores mayores que el valor predeterminado para la red subyacente dan lugar al transporte mediante la MTU predeterminada de la red.</span><span class="sxs-lookup"><span data-stu-id="614ce-238">Values larger than the default for the underlying network result in the transport using the network default MTU.</span></span> <span data-ttu-id="614ce-239">Los valores menores que 68 dan como resultado el transporte con una MTU de 68.</span><span class="sxs-lookup"><span data-stu-id="614ce-239">Values smaller than 68 result in the transport using an MTU of 68.</span></span>

## <a name="examples"></a><span data-ttu-id="614ce-240">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="614ce-240">Examples</span></span>

<span data-ttu-id="614ce-241">En el ejemplo de VBScript [Modify the MTU for All Network adapters](https://Gallery.TechNet.Microsoft.Com/49c26363-d46c-4288-9c8d-feb0a1982998) se configura la unidad de transmisión máxima para todos los adaptadores de red instalados en un equipo.</span><span class="sxs-lookup"><span data-stu-id="614ce-241">The [Modify the MTU for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/49c26363-d46c-4288-9c8d-feb0a1982998) VBScript sample configures the maximum transmission unit for all network adapters installed in a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="614ce-242">Requisitos</span><span class="sxs-lookup"><span data-stu-id="614ce-242">Requirements</span></span>



| <span data-ttu-id="614ce-243">Requisito</span><span class="sxs-lookup"><span data-stu-id="614ce-243">Requirement</span></span> | <span data-ttu-id="614ce-244">Value</span><span class="sxs-lookup"><span data-stu-id="614ce-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="614ce-245">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="614ce-245">Minimum supported client</span></span><br/> | <span data-ttu-id="614ce-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="614ce-246">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="614ce-247">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="614ce-247">Minimum supported server</span></span><br/> | <span data-ttu-id="614ce-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="614ce-248">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="614ce-249">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="614ce-249">Namespace</span></span><br/>                | <span data-ttu-id="614ce-250">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="614ce-250">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="614ce-251">MOF</span><span class="sxs-lookup"><span data-stu-id="614ce-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="614ce-252"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="614ce-252"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="614ce-253">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="614ce-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="614ce-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="614ce-254"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="614ce-255">Vea también</span><span class="sxs-lookup"><span data-stu-id="614ce-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="614ce-256">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="614ce-256">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="614ce-257">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="614ce-257">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="614ce-258">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="614ce-258">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="614ce-259">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="614ce-259">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="614ce-260">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="614ce-260">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

