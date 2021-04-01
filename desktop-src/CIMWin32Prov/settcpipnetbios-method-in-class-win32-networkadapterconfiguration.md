---
description: El método SetTcpipNetbios se usa para establecer la operación predeterminada de NetBIOS a través de TCP/IP.
ms.assetid: 2c639595-da13-400d-b4d0-432b39460554
ms.tgt_platform: multiple
title: Método SetTcpipNetbios de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpipNetbios
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 20ecab5918d00dc5f189464becc0252f2a8c0569
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907529"
---
# <a name="settcpipnetbios-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="32688-103">Método SetTcpipNetbios de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="32688-103">SetTcpipNetbios method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="32688-104">El método **SetTcpipNetbios** se usa para establecer la operación predeterminada de NetBIOS a través de TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="32688-104">The **SetTcpipNetbios** method is used to set the default operation of NetBIOS over TCP/IP.</span></span>

<span data-ttu-id="32688-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="32688-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="32688-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="32688-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="32688-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32688-107">Syntax</span></span>


```mof
uint32 SetTcpipNetbios(
  [in] uint32 TcpipNetbiosOptions
);
```



## <a name="parameters"></a><span data-ttu-id="32688-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32688-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32688-109">*TcpipNetbiosOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="32688-109">*TcpipNetbiosOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32688-110">Valor que especifica los valores posibles relacionados con NetBIOS a través de TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="32688-110">Value that specifies the possible settings related to NetBIOS over TCP/IP.</span></span>

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

<span data-ttu-id="32688-111"><span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>**EnableNetbiosViaDhcp** (0)</span><span class="sxs-lookup"><span data-stu-id="32688-111"><span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>**EnableNetbiosViaDhcp** (0)</span></span>


</dt> <dd>

<span data-ttu-id="32688-112">Habilitar NetBIOS a través de DHCP</span><span class="sxs-lookup"><span data-stu-id="32688-112">Enable Netbios via DHCP</span></span>

</dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

<span data-ttu-id="32688-113"><span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>**Parámetro enablenetbios** (1)</span><span class="sxs-lookup"><span data-stu-id="32688-113"><span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>**EnableNetbios** (1)</span></span>


</dt> <dd>

<span data-ttu-id="32688-114">Habilitar NetBIOS</span><span class="sxs-lookup"><span data-stu-id="32688-114">Enable Netbios</span></span>

</dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

<span data-ttu-id="32688-115"><span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>**DisableNetbios** (2)</span><span class="sxs-lookup"><span data-stu-id="32688-115"><span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>**DisableNetbios** (2)</span></span>


</dt> <dd>

<span data-ttu-id="32688-116">Deshabilitar NetBIOS</span><span class="sxs-lookup"><span data-stu-id="32688-116">Disable Netbios</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32688-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32688-117">Return value</span></span>

<span data-ttu-id="32688-118">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="32688-118">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="32688-119">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="32688-119">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="32688-120">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="32688-120">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="32688-121">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="32688-121">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="32688-122">0</span><span class="sxs-lookup"><span data-stu-id="32688-122">0</span></span>

<span data-ttu-id="32688-123">Finalización correcta.</span><span class="sxs-lookup"><span data-stu-id="32688-123">Successful completion.</span></span> <span data-ttu-id="32688-124">No es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="32688-124">No reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="32688-125">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="32688-125">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="32688-126">1</span><span class="sxs-lookup"><span data-stu-id="32688-126">1</span></span>

<span data-ttu-id="32688-127">Finalización correcta.</span><span class="sxs-lookup"><span data-stu-id="32688-127">Successful completion.</span></span> <span data-ttu-id="32688-128">Se requiere reiniciar.</span><span class="sxs-lookup"><span data-stu-id="32688-128">Reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="32688-129">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="32688-129">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="32688-130">64</span><span class="sxs-lookup"><span data-stu-id="32688-130">64</span></span>

<span data-ttu-id="32688-131">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="32688-131">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="32688-132">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="32688-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="32688-133">65</span><span class="sxs-lookup"><span data-stu-id="32688-133">65</span></span>

<span data-ttu-id="32688-134">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="32688-134">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="32688-135">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="32688-135">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="32688-136">66</span><span class="sxs-lookup"><span data-stu-id="32688-136">66</span></span>

<span data-ttu-id="32688-137">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="32688-137">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="32688-138">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="32688-138">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="32688-139">67</span><span class="sxs-lookup"><span data-stu-id="32688-139">67</span></span>

<span data-ttu-id="32688-140">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="32688-140">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="32688-141">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="32688-141">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="32688-142">68</span><span class="sxs-lookup"><span data-stu-id="32688-142">68</span></span>

<span data-ttu-id="32688-143">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="32688-143">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="32688-144">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="32688-144">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="32688-145">69</span><span class="sxs-lookup"><span data-stu-id="32688-145">69</span></span>

<span data-ttu-id="32688-146">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="32688-146">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="32688-147">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="32688-147">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="32688-148">70</span><span class="sxs-lookup"><span data-stu-id="32688-148">70</span></span>

<span data-ttu-id="32688-149">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="32688-149">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="32688-150">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="32688-150">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="32688-151">71</span><span class="sxs-lookup"><span data-stu-id="32688-151">71</span></span>

<span data-ttu-id="32688-152">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="32688-152">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="32688-153">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="32688-153">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="32688-154">72</span><span class="sxs-lookup"><span data-stu-id="32688-154">72</span></span>

<span data-ttu-id="32688-155">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="32688-155">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="32688-156">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="32688-156">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="32688-157">73</span><span class="sxs-lookup"><span data-stu-id="32688-157">73</span></span>

<span data-ttu-id="32688-158">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="32688-158">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="32688-159">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="32688-159">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="32688-160">74</span><span class="sxs-lookup"><span data-stu-id="32688-160">74</span></span>

<span data-ttu-id="32688-161">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="32688-161">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="32688-162">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="32688-162">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="32688-163">75</span><span class="sxs-lookup"><span data-stu-id="32688-163">75</span></span>

<span data-ttu-id="32688-164">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="32688-164">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="32688-165">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="32688-165">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="32688-166">76</span><span class="sxs-lookup"><span data-stu-id="32688-166">76</span></span>

<span data-ttu-id="32688-167">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="32688-167">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="32688-168">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="32688-168">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="32688-169">77</span><span class="sxs-lookup"><span data-stu-id="32688-169">77</span></span>

<span data-ttu-id="32688-170">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="32688-170">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="32688-171">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="32688-171">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="32688-172">78</span><span class="sxs-lookup"><span data-stu-id="32688-172">78</span></span>

<span data-ttu-id="32688-173">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="32688-173">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="32688-174">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="32688-174">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="32688-175">79</span><span class="sxs-lookup"><span data-stu-id="32688-175">79</span></span>

<span data-ttu-id="32688-176">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="32688-176">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="32688-177">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="32688-177">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="32688-178">80</span><span class="sxs-lookup"><span data-stu-id="32688-178">80</span></span>

<span data-ttu-id="32688-179">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="32688-179">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="32688-180">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="32688-180">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="32688-181">81</span><span class="sxs-lookup"><span data-stu-id="32688-181">81</span></span>

<span data-ttu-id="32688-182">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="32688-182">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="32688-183">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="32688-183">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="32688-184">82</span><span class="sxs-lookup"><span data-stu-id="32688-184">82</span></span>

<span data-ttu-id="32688-185">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="32688-185">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="32688-186">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="32688-186">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="32688-187">83</span><span class="sxs-lookup"><span data-stu-id="32688-187">83</span></span>

<span data-ttu-id="32688-188">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="32688-188">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="32688-189">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="32688-189">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="32688-190">84</span><span class="sxs-lookup"><span data-stu-id="32688-190">84</span></span>

<span data-ttu-id="32688-191">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="32688-191">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="32688-192">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="32688-192">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="32688-193">85</span><span class="sxs-lookup"><span data-stu-id="32688-193">85</span></span>

<span data-ttu-id="32688-194">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="32688-194">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="32688-195">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="32688-195">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="32688-196">86</span><span class="sxs-lookup"><span data-stu-id="32688-196">86</span></span>

<span data-ttu-id="32688-197">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="32688-197">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="32688-198">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="32688-198">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="32688-199">87</span><span class="sxs-lookup"><span data-stu-id="32688-199">87</span></span>

<span data-ttu-id="32688-200">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="32688-200">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="32688-201">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="32688-201">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="32688-202">88</span><span class="sxs-lookup"><span data-stu-id="32688-202">88</span></span>

<span data-ttu-id="32688-203">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="32688-203">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="32688-204">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="32688-204">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="32688-205">89</span><span class="sxs-lookup"><span data-stu-id="32688-205">89</span></span>

<span data-ttu-id="32688-206">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="32688-206">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="32688-207">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="32688-207">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="32688-208">90</span><span class="sxs-lookup"><span data-stu-id="32688-208">90</span></span>

<span data-ttu-id="32688-209">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="32688-209">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="32688-210">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="32688-210">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="32688-211">91</span><span class="sxs-lookup"><span data-stu-id="32688-211">91</span></span>

<span data-ttu-id="32688-212">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="32688-212">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="32688-213">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="32688-213">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="32688-214">92</span><span class="sxs-lookup"><span data-stu-id="32688-214">92</span></span>

<span data-ttu-id="32688-215">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="32688-215">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="32688-216">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="32688-216">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="32688-217">93</span><span class="sxs-lookup"><span data-stu-id="32688-217">93</span></span>

<span data-ttu-id="32688-218">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="32688-218">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="32688-219">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="32688-219">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="32688-220">94</span><span class="sxs-lookup"><span data-stu-id="32688-220">94</span></span>

<span data-ttu-id="32688-221">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="32688-221">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="32688-222">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="32688-222">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="32688-223">95</span><span class="sxs-lookup"><span data-stu-id="32688-223">95</span></span>

<span data-ttu-id="32688-224">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="32688-224">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="32688-225">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="32688-225">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="32688-226">96</span><span class="sxs-lookup"><span data-stu-id="32688-226">96</span></span>

<span data-ttu-id="32688-227">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="32688-227">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="32688-228">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="32688-228">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="32688-229">97</span><span class="sxs-lookup"><span data-stu-id="32688-229">97</span></span>

<span data-ttu-id="32688-230">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="32688-230">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="32688-231">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="32688-231">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="32688-232">98</span><span class="sxs-lookup"><span data-stu-id="32688-232">98</span></span>

<span data-ttu-id="32688-233">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="32688-233">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="32688-234">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="32688-234">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="32688-235">100</span><span class="sxs-lookup"><span data-stu-id="32688-235">100</span></span>

<span data-ttu-id="32688-236">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="32688-236">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="32688-237">**Otros**</span><span class="sxs-lookup"><span data-stu-id="32688-237">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="32688-238">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="32688-238">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="32688-239">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="32688-239">Examples</span></span>

<span data-ttu-id="32688-240">El ejemplo de la [modificación del uso de NetBIOS en un adaptador de red](https://Gallery.TechNet.Microsoft.Com/01d541f7-5c0d-46d3-8619-28aaab154dc0) de VBScript habilita NetBIOS para un adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="32688-240">The [Modify NetBIOS Use on a Network Adapter](https://Gallery.TechNet.Microsoft.Com/01d541f7-5c0d-46d3-8619-28aaab154dc0) VBScript sample enables NetBIOS for a network adapter.</span></span>

<span data-ttu-id="32688-241">El ejemplo de configuración de [tarjetas de red iSCSI según prácticas recomendadas de Microsoft](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) automatiza la configuración de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="32688-241">The [Configure iSCSI Network Cards as per Microsoft Best Practices PowerShell](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) sample automates the configuration settings for a Virtual Machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="32688-242">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32688-242">Requirements</span></span>



| <span data-ttu-id="32688-243">Requisito</span><span class="sxs-lookup"><span data-stu-id="32688-243">Requirement</span></span> | <span data-ttu-id="32688-244">Value</span><span class="sxs-lookup"><span data-stu-id="32688-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32688-245">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32688-245">Minimum supported client</span></span><br/> | <span data-ttu-id="32688-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32688-246">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="32688-247">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32688-247">Minimum supported server</span></span><br/> | <span data-ttu-id="32688-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32688-248">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="32688-249">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="32688-249">Namespace</span></span><br/>                | <span data-ttu-id="32688-250">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="32688-250">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="32688-251">MOF</span><span class="sxs-lookup"><span data-stu-id="32688-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32688-252"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32688-252"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="32688-253">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="32688-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32688-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32688-254"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32688-255">Vea también</span><span class="sxs-lookup"><span data-stu-id="32688-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32688-256">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="32688-256">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="32688-257">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="32688-257">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="32688-258">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="32688-258">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="32688-259">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="32688-259">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="32688-260">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="32688-260">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

