---
description: El método estático de la clase WMI SetArpAlwaysSourceRoute se usa para establecer la transmisión de consultas ARP por TCP/IP.
ms.assetid: bbff4e2e-aea6-400e-8bd8-f62aaa9fa601
ms.tgt_platform: multiple
title: Método SetArpAlwaysSourceRoute de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetArpAlwaysSourceRoute
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7151fbbd13d3ac6fdf4ac3b129cdcb438abe73a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152924"
---
# <a name="setarpalwayssourceroute-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="68b2e-103">Método SetArpAlwaysSourceRoute de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="68b2e-103">SetArpAlwaysSourceRoute method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="68b2e-104">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetArpAlwaysSourceRoute** se usa para establecer la transmisión de consultas ARP por TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="68b2e-104">The **SetArpAlwaysSourceRoute** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the transmission of ARP queries by TCP/IP.</span></span>

<span data-ttu-id="68b2e-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="68b2e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="68b2e-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="68b2e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="68b2e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68b2e-107">Syntax</span></span>


```mof
uint32 SetArpAlwaysSourceRoute(
  [in] boolean ArpAlwaysSourceRoute
);
```



## <a name="parameters"></a><span data-ttu-id="68b2e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68b2e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68b2e-109">*ArpAlwaysSourceRoute* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="68b2e-109">*ArpAlwaysSourceRoute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-110">Si **es true**, se fuerza a TCP/IP a transmitir consultas ARP con enrutamiento de origen habilitado en redes token ring.</span><span class="sxs-lookup"><span data-stu-id="68b2e-110">If **true**, TCP/IP is forced to transmit ARP queries with source routing enabled on Token Ring networks.</span></span> <span data-ttu-id="68b2e-111">De forma predeterminada, la pila transmite las consultas ARP sin el enrutamiento de origen primero y, a continuación, vuelve a intentarlo con el enrutamiento de origen habilitado si no se recibe ninguna respuesta.</span><span class="sxs-lookup"><span data-stu-id="68b2e-111">By default, the stack transmits ARP queries without source routing first, then retries with source routing enabled if no reply is received.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68b2e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68b2e-112">Return value</span></span>

<span data-ttu-id="68b2e-113">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="68b2e-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="68b2e-114">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="68b2e-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="68b2e-115">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="68b2e-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="68b2e-116">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="68b2e-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-117">0</span><span class="sxs-lookup"><span data-stu-id="68b2e-117">0</span></span>

<span data-ttu-id="68b2e-118">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="68b2e-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-119">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="68b2e-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-120">1</span><span class="sxs-lookup"><span data-stu-id="68b2e-120">1</span></span>

<span data-ttu-id="68b2e-121">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="68b2e-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-122">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="68b2e-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-123">64</span><span class="sxs-lookup"><span data-stu-id="68b2e-123">64</span></span>

<span data-ttu-id="68b2e-124">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="68b2e-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-125">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="68b2e-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-126">65</span><span class="sxs-lookup"><span data-stu-id="68b2e-126">65</span></span>

<span data-ttu-id="68b2e-127">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="68b2e-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-128">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="68b2e-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-129">66</span><span class="sxs-lookup"><span data-stu-id="68b2e-129">66</span></span>

<span data-ttu-id="68b2e-130">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="68b2e-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-131">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="68b2e-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-132">67</span><span class="sxs-lookup"><span data-stu-id="68b2e-132">67</span></span>

<span data-ttu-id="68b2e-133">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="68b2e-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-134">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="68b2e-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-135">68</span><span class="sxs-lookup"><span data-stu-id="68b2e-135">68</span></span>

<span data-ttu-id="68b2e-136">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="68b2e-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-137">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="68b2e-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-138">69</span><span class="sxs-lookup"><span data-stu-id="68b2e-138">69</span></span>

<span data-ttu-id="68b2e-139">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="68b2e-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-140">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="68b2e-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-141">70</span><span class="sxs-lookup"><span data-stu-id="68b2e-141">70</span></span>

<span data-ttu-id="68b2e-142">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="68b2e-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-143">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="68b2e-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-144">71</span><span class="sxs-lookup"><span data-stu-id="68b2e-144">71</span></span>

<span data-ttu-id="68b2e-145">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="68b2e-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-146">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="68b2e-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-147">72</span><span class="sxs-lookup"><span data-stu-id="68b2e-147">72</span></span>

<span data-ttu-id="68b2e-148">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="68b2e-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-149">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="68b2e-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-150">73</span><span class="sxs-lookup"><span data-stu-id="68b2e-150">73</span></span>

<span data-ttu-id="68b2e-151">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="68b2e-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-152">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="68b2e-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-153">74</span><span class="sxs-lookup"><span data-stu-id="68b2e-153">74</span></span>

<span data-ttu-id="68b2e-154">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="68b2e-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-155">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="68b2e-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-156">75</span><span class="sxs-lookup"><span data-stu-id="68b2e-156">75</span></span>

<span data-ttu-id="68b2e-157">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="68b2e-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-158">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="68b2e-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-159">76</span><span class="sxs-lookup"><span data-stu-id="68b2e-159">76</span></span>

<span data-ttu-id="68b2e-160">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="68b2e-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-161">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="68b2e-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-162">77</span><span class="sxs-lookup"><span data-stu-id="68b2e-162">77</span></span>

<span data-ttu-id="68b2e-163">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="68b2e-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-164">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="68b2e-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-165">78</span><span class="sxs-lookup"><span data-stu-id="68b2e-165">78</span></span>

<span data-ttu-id="68b2e-166">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="68b2e-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-167">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="68b2e-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-168">79</span><span class="sxs-lookup"><span data-stu-id="68b2e-168">79</span></span>

<span data-ttu-id="68b2e-169">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="68b2e-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-170">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="68b2e-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-171">80</span><span class="sxs-lookup"><span data-stu-id="68b2e-171">80</span></span>

<span data-ttu-id="68b2e-172">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="68b2e-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-173">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="68b2e-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-174">81</span><span class="sxs-lookup"><span data-stu-id="68b2e-174">81</span></span>

<span data-ttu-id="68b2e-175">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="68b2e-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-176">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="68b2e-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-177">82</span><span class="sxs-lookup"><span data-stu-id="68b2e-177">82</span></span>

<span data-ttu-id="68b2e-178">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="68b2e-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-179">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="68b2e-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-180">83</span><span class="sxs-lookup"><span data-stu-id="68b2e-180">83</span></span>

<span data-ttu-id="68b2e-181">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="68b2e-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-182">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="68b2e-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-183">84</span><span class="sxs-lookup"><span data-stu-id="68b2e-183">84</span></span>

<span data-ttu-id="68b2e-184">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="68b2e-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-185">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="68b2e-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-186">85</span><span class="sxs-lookup"><span data-stu-id="68b2e-186">85</span></span>

<span data-ttu-id="68b2e-187">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="68b2e-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-188">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="68b2e-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-189">86</span><span class="sxs-lookup"><span data-stu-id="68b2e-189">86</span></span>

<span data-ttu-id="68b2e-190">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="68b2e-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-191">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="68b2e-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-192">87</span><span class="sxs-lookup"><span data-stu-id="68b2e-192">87</span></span>

<span data-ttu-id="68b2e-193">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="68b2e-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-194">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="68b2e-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-195">88</span><span class="sxs-lookup"><span data-stu-id="68b2e-195">88</span></span>

<span data-ttu-id="68b2e-196">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="68b2e-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-197">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="68b2e-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-198">89</span><span class="sxs-lookup"><span data-stu-id="68b2e-198">89</span></span>

<span data-ttu-id="68b2e-199">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="68b2e-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-200">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="68b2e-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-201">90</span><span class="sxs-lookup"><span data-stu-id="68b2e-201">90</span></span>

<span data-ttu-id="68b2e-202">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="68b2e-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-203">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="68b2e-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-204">91</span><span class="sxs-lookup"><span data-stu-id="68b2e-204">91</span></span>

<span data-ttu-id="68b2e-205">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="68b2e-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-206">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="68b2e-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-207">92</span><span class="sxs-lookup"><span data-stu-id="68b2e-207">92</span></span>

<span data-ttu-id="68b2e-208">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="68b2e-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-209">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="68b2e-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-210">93</span><span class="sxs-lookup"><span data-stu-id="68b2e-210">93</span></span>

<span data-ttu-id="68b2e-211">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="68b2e-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-212">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="68b2e-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-213">94</span><span class="sxs-lookup"><span data-stu-id="68b2e-213">94</span></span>

<span data-ttu-id="68b2e-214">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="68b2e-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-215">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="68b2e-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-216">95</span><span class="sxs-lookup"><span data-stu-id="68b2e-216">95</span></span>

<span data-ttu-id="68b2e-217">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="68b2e-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-218">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="68b2e-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-219">96</span><span class="sxs-lookup"><span data-stu-id="68b2e-219">96</span></span>

<span data-ttu-id="68b2e-220">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="68b2e-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-221">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="68b2e-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-222">97</span><span class="sxs-lookup"><span data-stu-id="68b2e-222">97</span></span>

<span data-ttu-id="68b2e-223">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="68b2e-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-224">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="68b2e-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-225">98</span><span class="sxs-lookup"><span data-stu-id="68b2e-225">98</span></span>

<span data-ttu-id="68b2e-226">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="68b2e-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-227">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="68b2e-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-228">100</span><span class="sxs-lookup"><span data-stu-id="68b2e-228">100</span></span>

<span data-ttu-id="68b2e-229">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="68b2e-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="68b2e-230">**Otros**</span><span class="sxs-lookup"><span data-stu-id="68b2e-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="68b2e-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="68b2e-231">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="68b2e-232">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="68b2e-232">Examples</span></span>

<span data-ttu-id="68b2e-233">El ejemplo de [modificación de consultas ARP para usar el enrutamiento de origen](https://Gallery.TechNet.Microsoft.Com/e0298c96-acc2-4809-9365-fce3000db00e) de VBScript en la galería de TechNet usa **SETARPALWAYSSOURCEROUTE** para configurar TCP/IP para usar siempre el enrutamiento de origen en todas las redes de token ring.</span><span class="sxs-lookup"><span data-stu-id="68b2e-233">The [Modify ARP Queries to Use Source Routing](https://Gallery.TechNet.Microsoft.Com/e0298c96-acc2-4809-9365-fce3000db00e) VBScript sample on TechNet Gallery uses **SetArpAlwaysSourceRoute** to configure TCP/IP to always use source routing on all Token Ring networks.</span></span>

## <a name="requirements"></a><span data-ttu-id="68b2e-234">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68b2e-234">Requirements</span></span>



| <span data-ttu-id="68b2e-235">Requisito</span><span class="sxs-lookup"><span data-stu-id="68b2e-235">Requirement</span></span> | <span data-ttu-id="68b2e-236">Value</span><span class="sxs-lookup"><span data-stu-id="68b2e-236">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68b2e-237">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68b2e-237">Minimum supported client</span></span><br/> | <span data-ttu-id="68b2e-238">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68b2e-238">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68b2e-239">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68b2e-239">Minimum supported server</span></span><br/> | <span data-ttu-id="68b2e-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68b2e-240">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68b2e-241">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="68b2e-241">Namespace</span></span><br/>                | <span data-ttu-id="68b2e-242">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="68b2e-242">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="68b2e-243">MOF</span><span class="sxs-lookup"><span data-stu-id="68b2e-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68b2e-244"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68b2e-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="68b2e-245">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68b2e-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68b2e-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68b2e-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68b2e-247">Vea también</span><span class="sxs-lookup"><span data-stu-id="68b2e-247">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68b2e-248">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="68b2e-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="68b2e-249">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="68b2e-249">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="68b2e-250">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="68b2e-250">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="68b2e-251">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="68b2e-251">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="68b2e-252">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="68b2e-252">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

