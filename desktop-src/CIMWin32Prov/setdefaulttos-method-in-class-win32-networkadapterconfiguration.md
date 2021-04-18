---
description: Este método está obsoleto. Las aplicaciones deben usar la API de calidad de servicio (QoS) para manipular los bits de tipo de servicio (TOS).
ms.assetid: 18860c13-7324-4a37-b83c-f3d15c425acb
ms.tgt_platform: multiple
title: Método SetDefaultTOS de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDefaultTOS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5df55ff88c87047a48a84a122c8e58c8148a7cff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659718"
---
# <a name="setdefaulttos-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="8e1de-104">Método SetDefaultTOS de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="8e1de-104">SetDefaultTOS method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="8e1de-105">Este método está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="8e1de-105">This method is obsolete.</span></span> <span data-ttu-id="8e1de-106">Las aplicaciones deben usar la API de calidad de servicio (QoS) para manipular los bits de tipo de servicio (TOS).</span><span class="sxs-lookup"><span data-stu-id="8e1de-106">Applications should use the Quality of Service (QoS) API to manipulate Type of Service (TOS) bits.</span></span> <span data-ttu-id="8e1de-107">Para obtener más información, consulte [calidad de servicio](/previous-versions/windows/desktop/qos/qos-start-page).</span><span class="sxs-lookup"><span data-stu-id="8e1de-107">For more information, see [Quality of Service](/previous-versions/windows/desktop/qos/qos-start-page).</span></span>

<span data-ttu-id="8e1de-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="8e1de-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8e1de-109">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8e1de-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8e1de-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e1de-110">Syntax</span></span>


```mof
uint32 SetDefaultTOS(
  [in] uint8 DefaultTOS
);
```



## <a name="parameters"></a><span data-ttu-id="8e1de-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e1de-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e1de-112">*DefaultTOS* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e1de-112">*DefaultTOS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-113">El valor de tipo de servicio (TOS) se coloca en el encabezado de los paquetes IP salientes.</span><span class="sxs-lookup"><span data-stu-id="8e1de-113">Type of Service (TOS) value put in the header of outgoing IP packets.</span></span> <span data-ttu-id="8e1de-114">Para obtener una definición de los valores, consulte RFC 791.</span><span class="sxs-lookup"><span data-stu-id="8e1de-114">For a definition of the values, see RFC 791.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e1de-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e1de-115">Return value</span></span>

<span data-ttu-id="8e1de-116">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="8e1de-116">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="8e1de-117">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8e1de-117">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8e1de-118">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8e1de-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8e1de-119">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="8e1de-119">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-120">0</span><span class="sxs-lookup"><span data-stu-id="8e1de-120">0</span></span>

<span data-ttu-id="8e1de-121">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="8e1de-121">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-122">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="8e1de-122">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-123">1</span><span class="sxs-lookup"><span data-stu-id="8e1de-123">1</span></span>

<span data-ttu-id="8e1de-124">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="8e1de-124">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-125">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="8e1de-125">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-126">64</span><span class="sxs-lookup"><span data-stu-id="8e1de-126">64</span></span>

<span data-ttu-id="8e1de-127">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="8e1de-127">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-128">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="8e1de-128">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-129">65</span><span class="sxs-lookup"><span data-stu-id="8e1de-129">65</span></span>

<span data-ttu-id="8e1de-130">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="8e1de-130">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-131">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="8e1de-131">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-132">66</span><span class="sxs-lookup"><span data-stu-id="8e1de-132">66</span></span>

<span data-ttu-id="8e1de-133">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="8e1de-133">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-134">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="8e1de-134">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-135">67</span><span class="sxs-lookup"><span data-stu-id="8e1de-135">67</span></span>

<span data-ttu-id="8e1de-136">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="8e1de-136">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-137">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="8e1de-137">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-138">68</span><span class="sxs-lookup"><span data-stu-id="8e1de-138">68</span></span>

<span data-ttu-id="8e1de-139">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="8e1de-139">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-140">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="8e1de-140">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-141">69</span><span class="sxs-lookup"><span data-stu-id="8e1de-141">69</span></span>

<span data-ttu-id="8e1de-142">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="8e1de-142">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-143">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="8e1de-143">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-144">70</span><span class="sxs-lookup"><span data-stu-id="8e1de-144">70</span></span>

<span data-ttu-id="8e1de-145">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="8e1de-145">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-146">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="8e1de-146">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-147">71</span><span class="sxs-lookup"><span data-stu-id="8e1de-147">71</span></span>

<span data-ttu-id="8e1de-148">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="8e1de-148">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-149">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="8e1de-149">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-150">72</span><span class="sxs-lookup"><span data-stu-id="8e1de-150">72</span></span>

<span data-ttu-id="8e1de-151">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="8e1de-151">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-152">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="8e1de-152">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-153">73</span><span class="sxs-lookup"><span data-stu-id="8e1de-153">73</span></span>

<span data-ttu-id="8e1de-154">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="8e1de-154">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-155">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="8e1de-155">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-156">74</span><span class="sxs-lookup"><span data-stu-id="8e1de-156">74</span></span>

<span data-ttu-id="8e1de-157">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="8e1de-157">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-158">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="8e1de-158">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-159">75</span><span class="sxs-lookup"><span data-stu-id="8e1de-159">75</span></span>

<span data-ttu-id="8e1de-160">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="8e1de-160">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-161">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="8e1de-161">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-162">76</span><span class="sxs-lookup"><span data-stu-id="8e1de-162">76</span></span>

<span data-ttu-id="8e1de-163">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="8e1de-163">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-164">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="8e1de-164">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-165">77</span><span class="sxs-lookup"><span data-stu-id="8e1de-165">77</span></span>

<span data-ttu-id="8e1de-166">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="8e1de-166">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-167">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="8e1de-167">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-168">78</span><span class="sxs-lookup"><span data-stu-id="8e1de-168">78</span></span>

<span data-ttu-id="8e1de-169">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="8e1de-169">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-170">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="8e1de-170">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-171">79</span><span class="sxs-lookup"><span data-stu-id="8e1de-171">79</span></span>

<span data-ttu-id="8e1de-172">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="8e1de-172">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-173">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="8e1de-173">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-174">80</span><span class="sxs-lookup"><span data-stu-id="8e1de-174">80</span></span>

<span data-ttu-id="8e1de-175">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="8e1de-175">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-176">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="8e1de-176">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-177">81</span><span class="sxs-lookup"><span data-stu-id="8e1de-177">81</span></span>

<span data-ttu-id="8e1de-178">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="8e1de-178">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-179">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="8e1de-179">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-180">82</span><span class="sxs-lookup"><span data-stu-id="8e1de-180">82</span></span>

<span data-ttu-id="8e1de-181">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="8e1de-181">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-182">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="8e1de-182">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-183">83</span><span class="sxs-lookup"><span data-stu-id="8e1de-183">83</span></span>

<span data-ttu-id="8e1de-184">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="8e1de-184">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-185">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="8e1de-185">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-186">84</span><span class="sxs-lookup"><span data-stu-id="8e1de-186">84</span></span>

<span data-ttu-id="8e1de-187">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="8e1de-187">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-188">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="8e1de-188">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-189">85</span><span class="sxs-lookup"><span data-stu-id="8e1de-189">85</span></span>

<span data-ttu-id="8e1de-190">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="8e1de-190">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-191">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="8e1de-191">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-192">86</span><span class="sxs-lookup"><span data-stu-id="8e1de-192">86</span></span>

<span data-ttu-id="8e1de-193">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="8e1de-193">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-194">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="8e1de-194">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-195">87</span><span class="sxs-lookup"><span data-stu-id="8e1de-195">87</span></span>

<span data-ttu-id="8e1de-196">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="8e1de-196">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-197">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="8e1de-197">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-198">88</span><span class="sxs-lookup"><span data-stu-id="8e1de-198">88</span></span>

<span data-ttu-id="8e1de-199">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="8e1de-199">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-200">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="8e1de-200">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-201">89</span><span class="sxs-lookup"><span data-stu-id="8e1de-201">89</span></span>

<span data-ttu-id="8e1de-202">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="8e1de-202">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-203">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="8e1de-203">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-204">90</span><span class="sxs-lookup"><span data-stu-id="8e1de-204">90</span></span>

<span data-ttu-id="8e1de-205">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="8e1de-205">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-206">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="8e1de-206">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-207">91</span><span class="sxs-lookup"><span data-stu-id="8e1de-207">91</span></span>

<span data-ttu-id="8e1de-208">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="8e1de-208">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-209">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="8e1de-209">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-210">92</span><span class="sxs-lookup"><span data-stu-id="8e1de-210">92</span></span>

<span data-ttu-id="8e1de-211">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="8e1de-211">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-212">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="8e1de-212">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-213">93</span><span class="sxs-lookup"><span data-stu-id="8e1de-213">93</span></span>

<span data-ttu-id="8e1de-214">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="8e1de-214">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-215">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="8e1de-215">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-216">94</span><span class="sxs-lookup"><span data-stu-id="8e1de-216">94</span></span>

<span data-ttu-id="8e1de-217">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="8e1de-217">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-218">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="8e1de-218">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-219">95</span><span class="sxs-lookup"><span data-stu-id="8e1de-219">95</span></span>

<span data-ttu-id="8e1de-220">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="8e1de-220">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-221">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="8e1de-221">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-222">96</span><span class="sxs-lookup"><span data-stu-id="8e1de-222">96</span></span>

<span data-ttu-id="8e1de-223">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="8e1de-223">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-224">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="8e1de-224">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-225">97</span><span class="sxs-lookup"><span data-stu-id="8e1de-225">97</span></span>

<span data-ttu-id="8e1de-226">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="8e1de-226">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-227">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="8e1de-227">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-228">98</span><span class="sxs-lookup"><span data-stu-id="8e1de-228">98</span></span>

<span data-ttu-id="8e1de-229">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="8e1de-229">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-230">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="8e1de-230">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-231">100</span><span class="sxs-lookup"><span data-stu-id="8e1de-231">100</span></span>

<span data-ttu-id="8e1de-232">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="8e1de-232">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8e1de-233">**Otros**</span><span class="sxs-lookup"><span data-stu-id="8e1de-233">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="8e1de-234">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="8e1de-234">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e1de-235">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e1de-235">Remarks</span></span>

<span data-ttu-id="8e1de-236">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDefaultTOS** se usa para establecer el valor predeterminado del tos en el encabezado de los paquetes IP salientes.</span><span class="sxs-lookup"><span data-stu-id="8e1de-236">The **SetDefaultTOS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the default TOS value in the header of outgoing IP packets.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e1de-237">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e1de-237">Requirements</span></span>



| <span data-ttu-id="8e1de-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e1de-238">Requirement</span></span> | <span data-ttu-id="8e1de-239">Value</span><span class="sxs-lookup"><span data-stu-id="8e1de-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e1de-240">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e1de-240">Minimum supported client</span></span><br/> | <span data-ttu-id="8e1de-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e1de-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e1de-242">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e1de-242">Minimum supported server</span></span><br/> | <span data-ttu-id="8e1de-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e1de-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e1de-244">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8e1de-244">Namespace</span></span><br/>                | <span data-ttu-id="8e1de-245">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8e1de-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8e1de-246">MOF</span><span class="sxs-lookup"><span data-stu-id="8e1de-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e1de-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e1de-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e1de-248">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8e1de-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e1de-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e1de-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e1de-250">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e1de-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e1de-251">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="8e1de-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="8e1de-252">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="8e1de-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="8e1de-253">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="8e1de-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="8e1de-254">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="8e1de-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="8e1de-255">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="8e1de-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

