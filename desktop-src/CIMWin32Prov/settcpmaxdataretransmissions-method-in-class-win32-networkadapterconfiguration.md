---
description: El método estático de la clase WMI SetTcpMaxDataRetransmissions se usa para establecer el número de veces que TCP retransmite un segmento de datos individual antes de anular la conexión.
ms.assetid: 1b5407ee-8e2b-4aed-a17a-58d960f976f2
ms.tgt_platform: multiple
title: Método SetTcpMaxDataRetransmissions de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpMaxDataRetransmissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 59998888eb2aed170b626fb4cb61780cbe0cb6e4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153552"
---
# <a name="settcpmaxdataretransmissions-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="f5260-103">Método SetTcpMaxDataRetransmissions de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="f5260-103">SetTcpMaxDataRetransmissions method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="f5260-104">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetTcpMaxDataRetransmissions** se usa para establecer el número de veces que TCP retransmite un segmento de datos individual antes de anular la conexión.</span><span class="sxs-lookup"><span data-stu-id="f5260-104">The **SetTcpMaxDataRetransmissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the number of times TCP retransmits an individual data segment before aborting the connection.</span></span>

<span data-ttu-id="f5260-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f5260-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f5260-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f5260-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f5260-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5260-107">Syntax</span></span>


```mof
uint32 SetTcpMaxDataRetransmissions(
  [in] uint32 TcpMaxDataRetransmissions
);
```



## <a name="parameters"></a><span data-ttu-id="f5260-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5260-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5260-109">*TcpMaxDataRetransmissions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f5260-109">*TcpMaxDataRetransmissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5260-110">Número de veces que TCP retransmite un segmento de datos individual antes de anular la conexión.</span><span class="sxs-lookup"><span data-stu-id="f5260-110">Number of times TCP retransmits an individual data segment before aborting the connection.</span></span> <span data-ttu-id="f5260-111">Intervalo válido: 0-0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="f5260-111">Valid range: 0 - 0xFFFFFFFF.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5260-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5260-112">Return value</span></span>

<span data-ttu-id="f5260-113">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="f5260-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="f5260-114">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f5260-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f5260-115">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f5260-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f5260-116">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="f5260-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-117">0</span><span class="sxs-lookup"><span data-stu-id="f5260-117">0</span></span>

<span data-ttu-id="f5260-118">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="f5260-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-119">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="f5260-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-120">1</span><span class="sxs-lookup"><span data-stu-id="f5260-120">1</span></span>

<span data-ttu-id="f5260-121">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="f5260-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-122">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="f5260-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-123">64</span><span class="sxs-lookup"><span data-stu-id="f5260-123">64</span></span>

<span data-ttu-id="f5260-124">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="f5260-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-125">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="f5260-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-126">65</span><span class="sxs-lookup"><span data-stu-id="f5260-126">65</span></span>

<span data-ttu-id="f5260-127">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="f5260-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-128">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="f5260-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-129">66</span><span class="sxs-lookup"><span data-stu-id="f5260-129">66</span></span>

<span data-ttu-id="f5260-130">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="f5260-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-131">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="f5260-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-132">67</span><span class="sxs-lookup"><span data-stu-id="f5260-132">67</span></span>

<span data-ttu-id="f5260-133">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="f5260-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-134">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="f5260-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-135">68</span><span class="sxs-lookup"><span data-stu-id="f5260-135">68</span></span>

<span data-ttu-id="f5260-136">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="f5260-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-137">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="f5260-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-138">69</span><span class="sxs-lookup"><span data-stu-id="f5260-138">69</span></span>

<span data-ttu-id="f5260-139">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="f5260-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-140">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="f5260-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-141">70</span><span class="sxs-lookup"><span data-stu-id="f5260-141">70</span></span>

<span data-ttu-id="f5260-142">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="f5260-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-143">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="f5260-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-144">71</span><span class="sxs-lookup"><span data-stu-id="f5260-144">71</span></span>

<span data-ttu-id="f5260-145">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="f5260-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-146">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="f5260-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-147">72</span><span class="sxs-lookup"><span data-stu-id="f5260-147">72</span></span>

<span data-ttu-id="f5260-148">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="f5260-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-149">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="f5260-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-150">73</span><span class="sxs-lookup"><span data-stu-id="f5260-150">73</span></span>

<span data-ttu-id="f5260-151">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="f5260-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-152">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="f5260-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-153">74</span><span class="sxs-lookup"><span data-stu-id="f5260-153">74</span></span>

<span data-ttu-id="f5260-154">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="f5260-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-155">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="f5260-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-156">75</span><span class="sxs-lookup"><span data-stu-id="f5260-156">75</span></span>

<span data-ttu-id="f5260-157">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="f5260-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-158">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="f5260-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-159">76</span><span class="sxs-lookup"><span data-stu-id="f5260-159">76</span></span>

<span data-ttu-id="f5260-160">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="f5260-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-161">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="f5260-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-162">77</span><span class="sxs-lookup"><span data-stu-id="f5260-162">77</span></span>

<span data-ttu-id="f5260-163">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="f5260-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-164">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="f5260-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-165">78</span><span class="sxs-lookup"><span data-stu-id="f5260-165">78</span></span>

<span data-ttu-id="f5260-166">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="f5260-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-167">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="f5260-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-168">79</span><span class="sxs-lookup"><span data-stu-id="f5260-168">79</span></span>

<span data-ttu-id="f5260-169">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="f5260-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-170">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="f5260-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-171">80</span><span class="sxs-lookup"><span data-stu-id="f5260-171">80</span></span>

<span data-ttu-id="f5260-172">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f5260-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-173">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="f5260-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-174">81</span><span class="sxs-lookup"><span data-stu-id="f5260-174">81</span></span>

<span data-ttu-id="f5260-175">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="f5260-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-176">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="f5260-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-177">82</span><span class="sxs-lookup"><span data-stu-id="f5260-177">82</span></span>

<span data-ttu-id="f5260-178">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="f5260-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-179">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="f5260-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-180">83</span><span class="sxs-lookup"><span data-stu-id="f5260-180">83</span></span>

<span data-ttu-id="f5260-181">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="f5260-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-182">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="f5260-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-183">84</span><span class="sxs-lookup"><span data-stu-id="f5260-183">84</span></span>

<span data-ttu-id="f5260-184">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="f5260-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-185">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="f5260-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-186">85</span><span class="sxs-lookup"><span data-stu-id="f5260-186">85</span></span>

<span data-ttu-id="f5260-187">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="f5260-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-188">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="f5260-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-189">86</span><span class="sxs-lookup"><span data-stu-id="f5260-189">86</span></span>

<span data-ttu-id="f5260-190">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="f5260-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-191">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="f5260-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-192">87</span><span class="sxs-lookup"><span data-stu-id="f5260-192">87</span></span>

<span data-ttu-id="f5260-193">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="f5260-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-194">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="f5260-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-195">88</span><span class="sxs-lookup"><span data-stu-id="f5260-195">88</span></span>

<span data-ttu-id="f5260-196">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="f5260-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-197">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="f5260-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-198">89</span><span class="sxs-lookup"><span data-stu-id="f5260-198">89</span></span>

<span data-ttu-id="f5260-199">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="f5260-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-200">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="f5260-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-201">90</span><span class="sxs-lookup"><span data-stu-id="f5260-201">90</span></span>

<span data-ttu-id="f5260-202">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="f5260-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-203">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="f5260-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-204">91</span><span class="sxs-lookup"><span data-stu-id="f5260-204">91</span></span>

<span data-ttu-id="f5260-205">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="f5260-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-206">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="f5260-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-207">92</span><span class="sxs-lookup"><span data-stu-id="f5260-207">92</span></span>

<span data-ttu-id="f5260-208">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="f5260-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-209">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="f5260-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-210">93</span><span class="sxs-lookup"><span data-stu-id="f5260-210">93</span></span>

<span data-ttu-id="f5260-211">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="f5260-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-212">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="f5260-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-213">94</span><span class="sxs-lookup"><span data-stu-id="f5260-213">94</span></span>

<span data-ttu-id="f5260-214">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="f5260-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-215">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="f5260-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-216">95</span><span class="sxs-lookup"><span data-stu-id="f5260-216">95</span></span>

<span data-ttu-id="f5260-217">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="f5260-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-218">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="f5260-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-219">96</span><span class="sxs-lookup"><span data-stu-id="f5260-219">96</span></span>

<span data-ttu-id="f5260-220">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="f5260-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-221">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="f5260-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-222">97</span><span class="sxs-lookup"><span data-stu-id="f5260-222">97</span></span>

<span data-ttu-id="f5260-223">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="f5260-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-224">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="f5260-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-225">98</span><span class="sxs-lookup"><span data-stu-id="f5260-225">98</span></span>

<span data-ttu-id="f5260-226">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="f5260-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-227">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="f5260-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-228">100</span><span class="sxs-lookup"><span data-stu-id="f5260-228">100</span></span>

<span data-ttu-id="f5260-229">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="f5260-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f5260-230">**Otros**</span><span class="sxs-lookup"><span data-stu-id="f5260-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="f5260-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="f5260-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5260-232">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5260-232">Remarks</span></span>

<span data-ttu-id="f5260-233">El tiempo de espera de la retransmisión se duplica con cada retransmisión sucesiva en una conexión.</span><span class="sxs-lookup"><span data-stu-id="f5260-233">The retransmission timeout doubles with each successive retransmission on a connection.</span></span>

## <a name="examples"></a><span data-ttu-id="f5260-234">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f5260-234">Examples</span></span>

<span data-ttu-id="f5260-235">En el ejemplo de VBScript de la opción [modificar el máximo permitido de retransmisiones de datos TCP](https://Gallery.TechNet.Microsoft.Com/8a581692-7950-412e-bd28-74f223b27827) se configura el número de veces que TCP intentará retransmitir un segmento de datos individual antes de abandonar el esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="f5260-235">The [Modify the Maximum Allowed TCP Data Retransmissions](https://Gallery.TechNet.Microsoft.Com/8a581692-7950-412e-bd28-74f223b27827) VBScript sample configures the number of times TCP will attempt to retransmit an individual data segment before abandoning the effort.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5260-236">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5260-236">Requirements</span></span>



| <span data-ttu-id="f5260-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5260-237">Requirement</span></span> | <span data-ttu-id="f5260-238">Value</span><span class="sxs-lookup"><span data-stu-id="f5260-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5260-239">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5260-239">Minimum supported client</span></span><br/> | <span data-ttu-id="f5260-240">Windows Vista, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5260-240">Windows Vista, Windows Vista</span></span><br/>                                                 |
| <span data-ttu-id="f5260-241">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5260-241">Minimum supported server</span></span><br/> | <span data-ttu-id="f5260-242">Windows Server 2008, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5260-242">Windows Server 2008, Windows Server 2008</span></span><br/>                                     |
| <span data-ttu-id="f5260-243">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f5260-243">Namespace</span></span><br/>                | <span data-ttu-id="f5260-244">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f5260-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f5260-245">MOF</span><span class="sxs-lookup"><span data-stu-id="f5260-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5260-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5260-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5260-247">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f5260-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5260-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5260-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5260-249">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5260-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5260-250">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="f5260-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="f5260-251">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="f5260-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="f5260-252">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="f5260-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="f5260-253">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="f5260-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="f5260-254">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="f5260-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

