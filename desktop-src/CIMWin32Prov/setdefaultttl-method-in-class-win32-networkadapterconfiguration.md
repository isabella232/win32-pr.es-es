---
description: El método estático de la clase WMI SetDefaultTTL se usa para establecer el valor de período de vida (TTL) predeterminado en el encabezado de los paquetes IP salientes.
ms.assetid: 74b060de-512c-407e-9f93-c3b496f8d09d
ms.tgt_platform: multiple
title: Método SetDefaultTTL de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDefaultTTL
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 253048b44a836f92646124fb972fe32c135e3b9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906942"
---
# <a name="setdefaultttl-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="95d19-103">Método SetDefaultTTL de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="95d19-103">SetDefaultTTL method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="95d19-104">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDefaultTTL** se usa para establecer el valor de período de vida (TTL) predeterminado en el encabezado de los paquetes IP salientes.</span><span class="sxs-lookup"><span data-stu-id="95d19-104">The **SetDefaultTTL** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the default Time to Live (TTL) value in the header of outgoing IP packets.</span></span>

<span data-ttu-id="95d19-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="95d19-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="95d19-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="95d19-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="95d19-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95d19-107">Syntax</span></span>


```mof
uint32 SetDefaultTTL(
  [in] uint8 DefaultTTL
);
```



## <a name="parameters"></a><span data-ttu-id="95d19-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95d19-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95d19-109">*DefaultTTL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="95d19-109">*DefaultTTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95d19-110">Valor de período de vida establecido en el encabezado de los paquetes IP salientes.</span><span class="sxs-lookup"><span data-stu-id="95d19-110">Time to Live value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="95d19-111">El valor predeterminado es 32; Intervalo válido: 1-255</span><span class="sxs-lookup"><span data-stu-id="95d19-111">The default value is 32; Valid range: 1 - 255</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95d19-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95d19-112">Return value</span></span>

<span data-ttu-id="95d19-113">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="95d19-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="95d19-114">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="95d19-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="95d19-115">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="95d19-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="95d19-116">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="95d19-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-117">0</span><span class="sxs-lookup"><span data-stu-id="95d19-117">0</span></span>

<span data-ttu-id="95d19-118">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="95d19-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-119">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="95d19-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-120">1</span><span class="sxs-lookup"><span data-stu-id="95d19-120">1</span></span>

<span data-ttu-id="95d19-121">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="95d19-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-122">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="95d19-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-123">64</span><span class="sxs-lookup"><span data-stu-id="95d19-123">64</span></span>

<span data-ttu-id="95d19-124">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="95d19-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-125">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="95d19-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-126">65</span><span class="sxs-lookup"><span data-stu-id="95d19-126">65</span></span>

<span data-ttu-id="95d19-127">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="95d19-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-128">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="95d19-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-129">66</span><span class="sxs-lookup"><span data-stu-id="95d19-129">66</span></span>

<span data-ttu-id="95d19-130">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="95d19-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-131">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="95d19-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-132">67</span><span class="sxs-lookup"><span data-stu-id="95d19-132">67</span></span>

<span data-ttu-id="95d19-133">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="95d19-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-134">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="95d19-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-135">68</span><span class="sxs-lookup"><span data-stu-id="95d19-135">68</span></span>

<span data-ttu-id="95d19-136">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="95d19-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-137">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="95d19-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-138">69</span><span class="sxs-lookup"><span data-stu-id="95d19-138">69</span></span>

<span data-ttu-id="95d19-139">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="95d19-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-140">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="95d19-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-141">70</span><span class="sxs-lookup"><span data-stu-id="95d19-141">70</span></span>

<span data-ttu-id="95d19-142">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="95d19-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-143">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="95d19-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-144">71</span><span class="sxs-lookup"><span data-stu-id="95d19-144">71</span></span>

<span data-ttu-id="95d19-145">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="95d19-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-146">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="95d19-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-147">72</span><span class="sxs-lookup"><span data-stu-id="95d19-147">72</span></span>

<span data-ttu-id="95d19-148">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="95d19-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-149">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="95d19-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-150">73</span><span class="sxs-lookup"><span data-stu-id="95d19-150">73</span></span>

<span data-ttu-id="95d19-151">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="95d19-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-152">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="95d19-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-153">74</span><span class="sxs-lookup"><span data-stu-id="95d19-153">74</span></span>

<span data-ttu-id="95d19-154">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="95d19-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-155">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="95d19-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-156">75</span><span class="sxs-lookup"><span data-stu-id="95d19-156">75</span></span>

<span data-ttu-id="95d19-157">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="95d19-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-158">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="95d19-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-159">76</span><span class="sxs-lookup"><span data-stu-id="95d19-159">76</span></span>

<span data-ttu-id="95d19-160">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="95d19-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-161">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="95d19-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-162">77</span><span class="sxs-lookup"><span data-stu-id="95d19-162">77</span></span>

<span data-ttu-id="95d19-163">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="95d19-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-164">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="95d19-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-165">78</span><span class="sxs-lookup"><span data-stu-id="95d19-165">78</span></span>

<span data-ttu-id="95d19-166">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="95d19-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-167">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="95d19-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-168">79</span><span class="sxs-lookup"><span data-stu-id="95d19-168">79</span></span>

<span data-ttu-id="95d19-169">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="95d19-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-170">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="95d19-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-171">80</span><span class="sxs-lookup"><span data-stu-id="95d19-171">80</span></span>

<span data-ttu-id="95d19-172">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="95d19-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-173">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="95d19-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-174">81</span><span class="sxs-lookup"><span data-stu-id="95d19-174">81</span></span>

<span data-ttu-id="95d19-175">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="95d19-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-176">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="95d19-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-177">82</span><span class="sxs-lookup"><span data-stu-id="95d19-177">82</span></span>

<span data-ttu-id="95d19-178">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="95d19-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-179">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="95d19-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-180">83</span><span class="sxs-lookup"><span data-stu-id="95d19-180">83</span></span>

<span data-ttu-id="95d19-181">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="95d19-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-182">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="95d19-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-183">84</span><span class="sxs-lookup"><span data-stu-id="95d19-183">84</span></span>

<span data-ttu-id="95d19-184">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="95d19-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-185">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="95d19-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-186">85</span><span class="sxs-lookup"><span data-stu-id="95d19-186">85</span></span>

<span data-ttu-id="95d19-187">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="95d19-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-188">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="95d19-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-189">86</span><span class="sxs-lookup"><span data-stu-id="95d19-189">86</span></span>

<span data-ttu-id="95d19-190">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="95d19-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-191">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="95d19-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-192">87</span><span class="sxs-lookup"><span data-stu-id="95d19-192">87</span></span>

<span data-ttu-id="95d19-193">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="95d19-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-194">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="95d19-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-195">88</span><span class="sxs-lookup"><span data-stu-id="95d19-195">88</span></span>

<span data-ttu-id="95d19-196">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="95d19-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-197">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="95d19-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-198">89</span><span class="sxs-lookup"><span data-stu-id="95d19-198">89</span></span>

<span data-ttu-id="95d19-199">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="95d19-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-200">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="95d19-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-201">90</span><span class="sxs-lookup"><span data-stu-id="95d19-201">90</span></span>

<span data-ttu-id="95d19-202">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="95d19-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-203">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="95d19-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-204">91</span><span class="sxs-lookup"><span data-stu-id="95d19-204">91</span></span>

<span data-ttu-id="95d19-205">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="95d19-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-206">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="95d19-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-207">92</span><span class="sxs-lookup"><span data-stu-id="95d19-207">92</span></span>

<span data-ttu-id="95d19-208">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="95d19-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-209">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="95d19-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-210">93</span><span class="sxs-lookup"><span data-stu-id="95d19-210">93</span></span>

<span data-ttu-id="95d19-211">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="95d19-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-212">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="95d19-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-213">94</span><span class="sxs-lookup"><span data-stu-id="95d19-213">94</span></span>

<span data-ttu-id="95d19-214">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="95d19-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-215">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="95d19-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-216">95</span><span class="sxs-lookup"><span data-stu-id="95d19-216">95</span></span>

<span data-ttu-id="95d19-217">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="95d19-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-218">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="95d19-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-219">96</span><span class="sxs-lookup"><span data-stu-id="95d19-219">96</span></span>

<span data-ttu-id="95d19-220">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="95d19-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-221">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="95d19-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-222">97</span><span class="sxs-lookup"><span data-stu-id="95d19-222">97</span></span>

<span data-ttu-id="95d19-223">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="95d19-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-224">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="95d19-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-225">98</span><span class="sxs-lookup"><span data-stu-id="95d19-225">98</span></span>

<span data-ttu-id="95d19-226">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="95d19-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-227">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="95d19-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-228">100</span><span class="sxs-lookup"><span data-stu-id="95d19-228">100</span></span>

<span data-ttu-id="95d19-229">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="95d19-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="95d19-230">**Otros**</span><span class="sxs-lookup"><span data-stu-id="95d19-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="95d19-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="95d19-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95d19-232">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95d19-232">Remarks</span></span>

<span data-ttu-id="95d19-233">El TTL especifica el número de enrutadores que puede atravesar un paquete IP para llegar a su destino antes de que se descarten.</span><span class="sxs-lookup"><span data-stu-id="95d19-233">The TTL specifies the number of routers an IP packet may pass through to reach its destination before being discarded.</span></span> <span data-ttu-id="95d19-234">Cada enrutador reduce el número de TTL de un paquete en uno y descarta los paquetes con un TTL de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="95d19-234">Each router decrements the TTL count of a packet by one and discards the packets with a TTL of 0 (zero).</span></span>

## <a name="examples"></a><span data-ttu-id="95d19-235">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="95d19-235">Examples</span></span>

<span data-ttu-id="95d19-236">El ejemplo de configuración [modificar el período de vida predeterminado para todos los adaptadores de red](https://Gallery.TechNet.Microsoft.Com/scriptcenter/3a228fb8-5517-4e23-800e-2a15f427d05d) usa **SetDefaultTTL** para establecer el valor de período de vida predeterminado en el encabezado de los paquetes IP salientes en 64</span><span class="sxs-lookup"><span data-stu-id="95d19-236">The [Modify the Default Time-to-Live for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/scriptcenter/3a228fb8-5517-4e23-800e-2a15f427d05d) VBScript sample uses **SetDefaultTTL** to set the default time-to-live value in the header of outgoing IP packets to 64</span></span>

## <a name="requirements"></a><span data-ttu-id="95d19-237">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95d19-237">Requirements</span></span>



| <span data-ttu-id="95d19-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="95d19-238">Requirement</span></span> | <span data-ttu-id="95d19-239">Value</span><span class="sxs-lookup"><span data-stu-id="95d19-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95d19-240">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95d19-240">Minimum supported client</span></span><br/> | <span data-ttu-id="95d19-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95d19-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="95d19-242">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95d19-242">Minimum supported server</span></span><br/> | <span data-ttu-id="95d19-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95d19-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="95d19-244">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="95d19-244">Namespace</span></span><br/>                | <span data-ttu-id="95d19-245">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="95d19-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="95d19-246">MOF</span><span class="sxs-lookup"><span data-stu-id="95d19-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95d19-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95d19-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="95d19-248">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="95d19-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95d19-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95d19-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95d19-250">Vea también</span><span class="sxs-lookup"><span data-stu-id="95d19-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95d19-251">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="95d19-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="95d19-252">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="95d19-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="95d19-253">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="95d19-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="95d19-254">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="95d19-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="95d19-255">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="95d19-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

