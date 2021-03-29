---
description: El método estático de la clase WMI SetTcpNumConnections se usa para establecer el número máximo de conexiones que TCP puede tener abiertas simultáneamente.
ms.assetid: 50458161-1f28-47f9-b395-09586e859d5d
ms.tgt_platform: multiple
title: Método SetTcpNumConnections de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpNumConnections
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5708c7ce80930c0924b560cc7b84e5af45ad7962
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153116"
---
# <a name="settcpnumconnections-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="86ae7-103">Método SetTcpNumConnections de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="86ae7-103">SetTcpNumConnections method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="86ae7-104">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetTcpNumConnections** se usa para establecer el número máximo de conexiones que TCP puede tener abiertas simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="86ae7-104">The **SetTcpNumConnections** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the maximum number of connections that TCP may have open simultaneously.</span></span>

<span data-ttu-id="86ae7-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="86ae7-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="86ae7-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="86ae7-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="86ae7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86ae7-107">Syntax</span></span>


```mof
uint32 SetTcpNumConnections(
  [in] uint32 TcpNumConnections
);
```



## <a name="parameters"></a><span data-ttu-id="86ae7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86ae7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86ae7-109">*TcpNumConnections* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86ae7-109">*TcpNumConnections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-110">Número máximo de conexiones que TCP puede haber abierto simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="86ae7-110">Maximum number of connections that TCP may have open simultaneously.</span></span> <span data-ttu-id="86ae7-111">El intervalo válido de valores es 0-0xFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="86ae7-111">The valid range of values is 0 - 0xFFFFFE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86ae7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86ae7-112">Return value</span></span>

<span data-ttu-id="86ae7-113">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="86ae7-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="86ae7-114">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="86ae7-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="86ae7-115">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="86ae7-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="86ae7-116">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="86ae7-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-117">0</span><span class="sxs-lookup"><span data-stu-id="86ae7-117">0</span></span>

<span data-ttu-id="86ae7-118">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="86ae7-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-119">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="86ae7-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-120">1</span><span class="sxs-lookup"><span data-stu-id="86ae7-120">1</span></span>

<span data-ttu-id="86ae7-121">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="86ae7-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-122">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="86ae7-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-123">64</span><span class="sxs-lookup"><span data-stu-id="86ae7-123">64</span></span>

<span data-ttu-id="86ae7-124">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="86ae7-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-125">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="86ae7-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-126">65</span><span class="sxs-lookup"><span data-stu-id="86ae7-126">65</span></span>

<span data-ttu-id="86ae7-127">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="86ae7-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-128">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="86ae7-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-129">66</span><span class="sxs-lookup"><span data-stu-id="86ae7-129">66</span></span>

<span data-ttu-id="86ae7-130">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="86ae7-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-131">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="86ae7-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-132">67</span><span class="sxs-lookup"><span data-stu-id="86ae7-132">67</span></span>

<span data-ttu-id="86ae7-133">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="86ae7-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-134">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="86ae7-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-135">68</span><span class="sxs-lookup"><span data-stu-id="86ae7-135">68</span></span>

<span data-ttu-id="86ae7-136">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="86ae7-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-137">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="86ae7-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-138">69</span><span class="sxs-lookup"><span data-stu-id="86ae7-138">69</span></span>

<span data-ttu-id="86ae7-139">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="86ae7-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-140">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="86ae7-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-141">70</span><span class="sxs-lookup"><span data-stu-id="86ae7-141">70</span></span>

<span data-ttu-id="86ae7-142">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="86ae7-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-143">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="86ae7-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-144">71</span><span class="sxs-lookup"><span data-stu-id="86ae7-144">71</span></span>

<span data-ttu-id="86ae7-145">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="86ae7-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-146">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="86ae7-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-147">72</span><span class="sxs-lookup"><span data-stu-id="86ae7-147">72</span></span>

<span data-ttu-id="86ae7-148">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="86ae7-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-149">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="86ae7-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-150">73</span><span class="sxs-lookup"><span data-stu-id="86ae7-150">73</span></span>

<span data-ttu-id="86ae7-151">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="86ae7-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-152">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="86ae7-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-153">74</span><span class="sxs-lookup"><span data-stu-id="86ae7-153">74</span></span>

<span data-ttu-id="86ae7-154">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="86ae7-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-155">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="86ae7-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-156">75</span><span class="sxs-lookup"><span data-stu-id="86ae7-156">75</span></span>

<span data-ttu-id="86ae7-157">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="86ae7-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-158">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="86ae7-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-159">76</span><span class="sxs-lookup"><span data-stu-id="86ae7-159">76</span></span>

<span data-ttu-id="86ae7-160">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="86ae7-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-161">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="86ae7-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-162">77</span><span class="sxs-lookup"><span data-stu-id="86ae7-162">77</span></span>

<span data-ttu-id="86ae7-163">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="86ae7-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-164">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="86ae7-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-165">78</span><span class="sxs-lookup"><span data-stu-id="86ae7-165">78</span></span>

<span data-ttu-id="86ae7-166">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="86ae7-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-167">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="86ae7-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-168">79</span><span class="sxs-lookup"><span data-stu-id="86ae7-168">79</span></span>

<span data-ttu-id="86ae7-169">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="86ae7-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-170">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="86ae7-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-171">80</span><span class="sxs-lookup"><span data-stu-id="86ae7-171">80</span></span>

<span data-ttu-id="86ae7-172">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="86ae7-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-173">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="86ae7-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-174">81</span><span class="sxs-lookup"><span data-stu-id="86ae7-174">81</span></span>

<span data-ttu-id="86ae7-175">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="86ae7-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-176">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="86ae7-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-177">82</span><span class="sxs-lookup"><span data-stu-id="86ae7-177">82</span></span>

<span data-ttu-id="86ae7-178">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="86ae7-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-179">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="86ae7-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-180">83</span><span class="sxs-lookup"><span data-stu-id="86ae7-180">83</span></span>

<span data-ttu-id="86ae7-181">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="86ae7-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-182">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="86ae7-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-183">84</span><span class="sxs-lookup"><span data-stu-id="86ae7-183">84</span></span>

<span data-ttu-id="86ae7-184">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="86ae7-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-185">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="86ae7-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-186">85</span><span class="sxs-lookup"><span data-stu-id="86ae7-186">85</span></span>

<span data-ttu-id="86ae7-187">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="86ae7-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-188">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="86ae7-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-189">86</span><span class="sxs-lookup"><span data-stu-id="86ae7-189">86</span></span>

<span data-ttu-id="86ae7-190">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="86ae7-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-191">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="86ae7-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-192">87</span><span class="sxs-lookup"><span data-stu-id="86ae7-192">87</span></span>

<span data-ttu-id="86ae7-193">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="86ae7-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-194">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="86ae7-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-195">88</span><span class="sxs-lookup"><span data-stu-id="86ae7-195">88</span></span>

<span data-ttu-id="86ae7-196">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="86ae7-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-197">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="86ae7-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-198">89</span><span class="sxs-lookup"><span data-stu-id="86ae7-198">89</span></span>

<span data-ttu-id="86ae7-199">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="86ae7-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-200">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="86ae7-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-201">90</span><span class="sxs-lookup"><span data-stu-id="86ae7-201">90</span></span>

<span data-ttu-id="86ae7-202">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="86ae7-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-203">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="86ae7-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-204">91</span><span class="sxs-lookup"><span data-stu-id="86ae7-204">91</span></span>

<span data-ttu-id="86ae7-205">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="86ae7-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-206">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="86ae7-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-207">92</span><span class="sxs-lookup"><span data-stu-id="86ae7-207">92</span></span>

<span data-ttu-id="86ae7-208">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="86ae7-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-209">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="86ae7-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-210">93</span><span class="sxs-lookup"><span data-stu-id="86ae7-210">93</span></span>

<span data-ttu-id="86ae7-211">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="86ae7-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-212">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="86ae7-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-213">94</span><span class="sxs-lookup"><span data-stu-id="86ae7-213">94</span></span>

<span data-ttu-id="86ae7-214">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="86ae7-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-215">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="86ae7-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-216">95</span><span class="sxs-lookup"><span data-stu-id="86ae7-216">95</span></span>

<span data-ttu-id="86ae7-217">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="86ae7-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-218">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="86ae7-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-219">96</span><span class="sxs-lookup"><span data-stu-id="86ae7-219">96</span></span>

<span data-ttu-id="86ae7-220">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="86ae7-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-221">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="86ae7-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-222">97</span><span class="sxs-lookup"><span data-stu-id="86ae7-222">97</span></span>

<span data-ttu-id="86ae7-223">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="86ae7-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-224">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="86ae7-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-225">98</span><span class="sxs-lookup"><span data-stu-id="86ae7-225">98</span></span>

<span data-ttu-id="86ae7-226">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="86ae7-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-227">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="86ae7-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-228">100</span><span class="sxs-lookup"><span data-stu-id="86ae7-228">100</span></span>

<span data-ttu-id="86ae7-229">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="86ae7-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="86ae7-230">**Otros**</span><span class="sxs-lookup"><span data-stu-id="86ae7-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="86ae7-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="86ae7-231">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="86ae7-232">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="86ae7-232">Examples</span></span>

<span data-ttu-id="86ae7-233">En el ejemplo [modificar el número permitido de conexiones TCP de](https://Gallery.TechNet.Microsoft.Com/016d09f3-28aa-47eb-b439-100b89999bab) VBScript se establece el número máximo permitido de conexiones TCP abiertas simultáneamente en un equipo en 10.</span><span class="sxs-lookup"><span data-stu-id="86ae7-233">The [Modify the Allowed Number of TCP Connections](https://Gallery.TechNet.Microsoft.Com/016d09f3-28aa-47eb-b439-100b89999bab) VBScript sample sets the maximum allowed number of simultaneously-opened TCP connections on a computer to 10.</span></span>

## <a name="requirements"></a><span data-ttu-id="86ae7-234">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86ae7-234">Requirements</span></span>



| <span data-ttu-id="86ae7-235">Requisito</span><span class="sxs-lookup"><span data-stu-id="86ae7-235">Requirement</span></span> | <span data-ttu-id="86ae7-236">Value</span><span class="sxs-lookup"><span data-stu-id="86ae7-236">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86ae7-237">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86ae7-237">Minimum supported client</span></span><br/> | <span data-ttu-id="86ae7-238">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86ae7-238">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="86ae7-239">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86ae7-239">Minimum supported server</span></span><br/> | <span data-ttu-id="86ae7-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86ae7-240">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="86ae7-241">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="86ae7-241">Namespace</span></span><br/>                | <span data-ttu-id="86ae7-242">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="86ae7-242">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="86ae7-243">MOF</span><span class="sxs-lookup"><span data-stu-id="86ae7-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86ae7-244"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="86ae7-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="86ae7-245">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="86ae7-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86ae7-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86ae7-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86ae7-247">Vea también</span><span class="sxs-lookup"><span data-stu-id="86ae7-247">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86ae7-248">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="86ae7-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="86ae7-249">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="86ae7-249">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="86ae7-250">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="86ae7-250">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="86ae7-251">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="86ae7-251">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="86ae7-252">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="86ae7-252">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

