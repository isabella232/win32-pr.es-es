---
description: El método estático de la clase WMI SetForwardBufferMemory se usa para especificar cuánta memoria IP asigna para almacenar los datos del paquete en la cola de paquetes del enrutador.
ms.assetid: e76452e8-2ee8-4d39-9405-33b0aeeac74d
ms.tgt_platform: multiple
title: Método SetForwardBufferMemory de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetForwardBufferMemory
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 30179610e6eee121a86119fa347067b40ef04c2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907325"
---
# <a name="setforwardbuffermemory-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="61c88-103">Método SetForwardBufferMemory de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="61c88-103">SetForwardBufferMemory method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="61c88-104">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetForwardBufferMemory** se usa para especificar cuánta memoria IP asigna para almacenar los datos del paquete en la cola de paquetes del enrutador.</span><span class="sxs-lookup"><span data-stu-id="61c88-104">The **SetForwardBufferMemory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to specify how much memory IP allocates to store packet data in the router packet queue.</span></span>

<span data-ttu-id="61c88-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="61c88-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="61c88-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="61c88-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="61c88-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61c88-107">Syntax</span></span>


```mof
uint32 SetForwardBufferMemory(
  [in] uint32 ForwardBufferMemory
);
```



## <a name="parameters"></a><span data-ttu-id="61c88-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61c88-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61c88-109">*ForwardBufferMemory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="61c88-109">*ForwardBufferMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61c88-110">Tamaño, en bytes, de la cola de paquetes del enrutador usada para almacenar los datos del paquete.</span><span class="sxs-lookup"><span data-stu-id="61c88-110">Size, in bytes, of the router packet queue used to store packet data.</span></span> <span data-ttu-id="61c88-111">El valor predeterminado es 74240 (paquetes de 50 1480 bytes, redondeado a un múltiplo de 256).</span><span class="sxs-lookup"><span data-stu-id="61c88-111">The default value is 74240 (fifty 1480-byte packets, rounded to a multiple of 256).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61c88-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61c88-112">Return value</span></span>

<span data-ttu-id="61c88-113">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="61c88-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="61c88-114">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="61c88-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="61c88-115">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="61c88-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="61c88-116">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="61c88-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-117">0</span><span class="sxs-lookup"><span data-stu-id="61c88-117">0</span></span>

<span data-ttu-id="61c88-118">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="61c88-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-119">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="61c88-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-120">1</span><span class="sxs-lookup"><span data-stu-id="61c88-120">1</span></span>

<span data-ttu-id="61c88-121">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="61c88-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-122">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="61c88-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-123">64</span><span class="sxs-lookup"><span data-stu-id="61c88-123">64</span></span>

<span data-ttu-id="61c88-124">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="61c88-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-125">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="61c88-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-126">65</span><span class="sxs-lookup"><span data-stu-id="61c88-126">65</span></span>

<span data-ttu-id="61c88-127">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="61c88-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-128">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="61c88-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-129">66</span><span class="sxs-lookup"><span data-stu-id="61c88-129">66</span></span>

<span data-ttu-id="61c88-130">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="61c88-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-131">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="61c88-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-132">67</span><span class="sxs-lookup"><span data-stu-id="61c88-132">67</span></span>

<span data-ttu-id="61c88-133">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="61c88-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-134">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="61c88-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-135">68</span><span class="sxs-lookup"><span data-stu-id="61c88-135">68</span></span>

<span data-ttu-id="61c88-136">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="61c88-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-137">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="61c88-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-138">69</span><span class="sxs-lookup"><span data-stu-id="61c88-138">69</span></span>

<span data-ttu-id="61c88-139">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="61c88-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-140">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="61c88-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-141">70</span><span class="sxs-lookup"><span data-stu-id="61c88-141">70</span></span>

<span data-ttu-id="61c88-142">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="61c88-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-143">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="61c88-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-144">71</span><span class="sxs-lookup"><span data-stu-id="61c88-144">71</span></span>

<span data-ttu-id="61c88-145">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="61c88-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-146">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="61c88-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-147">72</span><span class="sxs-lookup"><span data-stu-id="61c88-147">72</span></span>

<span data-ttu-id="61c88-148">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="61c88-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-149">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="61c88-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-150">73</span><span class="sxs-lookup"><span data-stu-id="61c88-150">73</span></span>

<span data-ttu-id="61c88-151">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="61c88-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-152">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="61c88-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-153">74</span><span class="sxs-lookup"><span data-stu-id="61c88-153">74</span></span>

<span data-ttu-id="61c88-154">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="61c88-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-155">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="61c88-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-156">75</span><span class="sxs-lookup"><span data-stu-id="61c88-156">75</span></span>

<span data-ttu-id="61c88-157">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="61c88-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-158">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="61c88-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-159">76</span><span class="sxs-lookup"><span data-stu-id="61c88-159">76</span></span>

<span data-ttu-id="61c88-160">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="61c88-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-161">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="61c88-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-162">77</span><span class="sxs-lookup"><span data-stu-id="61c88-162">77</span></span>

<span data-ttu-id="61c88-163">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="61c88-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-164">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="61c88-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-165">78</span><span class="sxs-lookup"><span data-stu-id="61c88-165">78</span></span>

<span data-ttu-id="61c88-166">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="61c88-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-167">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="61c88-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-168">79</span><span class="sxs-lookup"><span data-stu-id="61c88-168">79</span></span>

<span data-ttu-id="61c88-169">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="61c88-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-170">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="61c88-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-171">80</span><span class="sxs-lookup"><span data-stu-id="61c88-171">80</span></span>

<span data-ttu-id="61c88-172">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="61c88-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-173">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="61c88-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-174">81</span><span class="sxs-lookup"><span data-stu-id="61c88-174">81</span></span>

<span data-ttu-id="61c88-175">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="61c88-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-176">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="61c88-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-177">82</span><span class="sxs-lookup"><span data-stu-id="61c88-177">82</span></span>

<span data-ttu-id="61c88-178">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="61c88-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-179">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="61c88-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-180">83</span><span class="sxs-lookup"><span data-stu-id="61c88-180">83</span></span>

<span data-ttu-id="61c88-181">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="61c88-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-182">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="61c88-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-183">84</span><span class="sxs-lookup"><span data-stu-id="61c88-183">84</span></span>

<span data-ttu-id="61c88-184">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="61c88-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-185">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="61c88-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-186">85</span><span class="sxs-lookup"><span data-stu-id="61c88-186">85</span></span>

<span data-ttu-id="61c88-187">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="61c88-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-188">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="61c88-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-189">86</span><span class="sxs-lookup"><span data-stu-id="61c88-189">86</span></span>

<span data-ttu-id="61c88-190">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="61c88-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-191">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="61c88-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-192">87</span><span class="sxs-lookup"><span data-stu-id="61c88-192">87</span></span>

<span data-ttu-id="61c88-193">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="61c88-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-194">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="61c88-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-195">88</span><span class="sxs-lookup"><span data-stu-id="61c88-195">88</span></span>

<span data-ttu-id="61c88-196">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="61c88-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-197">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="61c88-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-198">89</span><span class="sxs-lookup"><span data-stu-id="61c88-198">89</span></span>

<span data-ttu-id="61c88-199">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="61c88-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-200">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="61c88-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-201">90</span><span class="sxs-lookup"><span data-stu-id="61c88-201">90</span></span>

<span data-ttu-id="61c88-202">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="61c88-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-203">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="61c88-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-204">91</span><span class="sxs-lookup"><span data-stu-id="61c88-204">91</span></span>

<span data-ttu-id="61c88-205">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="61c88-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-206">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="61c88-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-207">92</span><span class="sxs-lookup"><span data-stu-id="61c88-207">92</span></span>

<span data-ttu-id="61c88-208">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="61c88-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-209">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="61c88-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-210">93</span><span class="sxs-lookup"><span data-stu-id="61c88-210">93</span></span>

<span data-ttu-id="61c88-211">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="61c88-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-212">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="61c88-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-213">94</span><span class="sxs-lookup"><span data-stu-id="61c88-213">94</span></span>

<span data-ttu-id="61c88-214">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="61c88-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-215">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="61c88-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-216">95</span><span class="sxs-lookup"><span data-stu-id="61c88-216">95</span></span>

<span data-ttu-id="61c88-217">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="61c88-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-218">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="61c88-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-219">96</span><span class="sxs-lookup"><span data-stu-id="61c88-219">96</span></span>

<span data-ttu-id="61c88-220">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="61c88-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-221">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="61c88-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-222">97</span><span class="sxs-lookup"><span data-stu-id="61c88-222">97</span></span>

<span data-ttu-id="61c88-223">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="61c88-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-224">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="61c88-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-225">98</span><span class="sxs-lookup"><span data-stu-id="61c88-225">98</span></span>

<span data-ttu-id="61c88-226">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="61c88-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-227">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="61c88-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-228">100</span><span class="sxs-lookup"><span data-stu-id="61c88-228">100</span></span>

<span data-ttu-id="61c88-229">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="61c88-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="61c88-230">**Otros**</span><span class="sxs-lookup"><span data-stu-id="61c88-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="61c88-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="61c88-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61c88-232">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61c88-232">Remarks</span></span>

<span data-ttu-id="61c88-233">Cuando se rellena este espacio de búfer, el enrutador comienza a descartar los paquetes de forma aleatoria de su cola.</span><span class="sxs-lookup"><span data-stu-id="61c88-233">When this buffer space is filled, the router begins discarding packets at random from its queue.</span></span>

<span data-ttu-id="61c88-234">Los búferes de datos de cola de paquetes tienen una longitud de 256 bytes, por lo que el valor del parámetro *ForwardBufferMemory* debe ser un múltiplo de 256.</span><span class="sxs-lookup"><span data-stu-id="61c88-234">Packet queue data buffers are 256 bytes in length, so the value of the *ForwardBufferMemory* parameter should be a multiple of 256.</span></span> <span data-ttu-id="61c88-235">Varios búferes están encadenados juntos para paquetes más grandes.</span><span class="sxs-lookup"><span data-stu-id="61c88-235">Multiple buffers are chained together for larger packets.</span></span> <span data-ttu-id="61c88-236">El encabezado IP de un paquete se almacena por separado.</span><span class="sxs-lookup"><span data-stu-id="61c88-236">The IP header for a packet is stored separately.</span></span> <span data-ttu-id="61c88-237">Este parámetro se omite y no se asigna ningún búfer si el enrutador IP no está habilitado.</span><span class="sxs-lookup"><span data-stu-id="61c88-237">This parameter is ignored and no buffers are allocated if the IP router is not enabled.</span></span> <span data-ttu-id="61c88-238">El tamaño del búfer puede oscilar entre la unidad de transmisión máxima (MTU) de la red y un valor menor que 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="61c88-238">The buffer size can range from the network Maximum Transmission Unit (MTU) to a value smaller than 0xFFFFFFFF.</span></span>

## <a name="examples"></a><span data-ttu-id="61c88-239">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="61c88-239">Examples</span></span>

<span data-ttu-id="61c88-240">En el ejemplo de VBScript [modificar la memoria del búfer de reenvío para todos los adaptadores de red](https://Gallery.TechNet.Microsoft.Com/da5712dc-f854-4099-98a9-59c0ff20a524) se configura la memoria del búfer de reenvío para todos los adaptadores de red de un equipo.</span><span class="sxs-lookup"><span data-stu-id="61c88-240">The [Modify the Forward Buffer Memory for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/da5712dc-f854-4099-98a9-59c0ff20a524) VBScript sample configures the forward buffer memory for all network adapters on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="61c88-241">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61c88-241">Requirements</span></span>



| <span data-ttu-id="61c88-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="61c88-242">Requirement</span></span> | <span data-ttu-id="61c88-243">Value</span><span class="sxs-lookup"><span data-stu-id="61c88-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61c88-244">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61c88-244">Minimum supported client</span></span><br/> | <span data-ttu-id="61c88-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61c88-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="61c88-246">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61c88-246">Minimum supported server</span></span><br/> | <span data-ttu-id="61c88-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61c88-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="61c88-248">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="61c88-248">Namespace</span></span><br/>                | <span data-ttu-id="61c88-249">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="61c88-249">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="61c88-250">MOF</span><span class="sxs-lookup"><span data-stu-id="61c88-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61c88-251"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61c88-251"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="61c88-252">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="61c88-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61c88-253"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61c88-253"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61c88-254">Vea también</span><span class="sxs-lookup"><span data-stu-id="61c88-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61c88-255">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="61c88-255">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="61c88-256">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="61c88-256">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="61c88-257">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="61c88-257">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="61c88-258">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="61c88-258">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="61c88-259">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="61c88-259">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

