---
description: El método estático de la clase WMI SetDatabasePath establece la ruta de acceso a los archivos de base de datos de Internet estándar (hosts, LMHOSTs, redes y protocolos).
ms.assetid: 373fef0f-9cdf-4785-8d73-3f00bbd60ae2
ms.tgt_platform: multiple
title: Método SetDatabasePath de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDatabasePath
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b66a9979ec97d4ceda16acad6488d3b84d5d3a54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539339"
---
# <a name="setdatabasepath-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="9ed6f-103">Método SetDatabasePath de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="9ed6f-103">SetDatabasePath method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="9ed6f-104">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDatabasePath** establece la ruta de acceso a los archivos de base de datos de Internet estándar (hosts, lmhosts, redes y protocolos).</span><span class="sxs-lookup"><span data-stu-id="9ed6f-104">The **SetDatabasePath** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method sets the path to the standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS).</span></span>

<span data-ttu-id="9ed6f-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="9ed6f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9ed6f-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9ed6f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9ed6f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ed6f-107">Syntax</span></span>


```mof
uint32 SetDatabasePath(
  [in] string DatabasePath
);
```



## <a name="parameters"></a><span data-ttu-id="9ed6f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ed6f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ed6f-109">*DatabasePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9ed6f-109">*DatabasePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-110">Ruta de acceso de archivo válida a los archivos de base de datos de Internet estándar (hosts, LMHOSTs, redes y protocolos) usados por la interfaz de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-110">Valid file path to standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS) used by the Windows Sockets interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ed6f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ed6f-111">Return value</span></span>

<span data-ttu-id="9ed6f-112">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, a different number if there is an error.</span></span> <span data-ttu-id="9ed6f-113">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="9ed6f-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="9ed6f-114">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="9ed6f-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="9ed6f-115">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-116">0</span><span class="sxs-lookup"><span data-stu-id="9ed6f-116">0</span></span>

<span data-ttu-id="9ed6f-117">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-118">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-119">1</span><span class="sxs-lookup"><span data-stu-id="9ed6f-119">1</span></span>

<span data-ttu-id="9ed6f-120">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-121">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-122">64</span><span class="sxs-lookup"><span data-stu-id="9ed6f-122">64</span></span>

<span data-ttu-id="9ed6f-123">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-124">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-125">65</span><span class="sxs-lookup"><span data-stu-id="9ed6f-125">65</span></span>

<span data-ttu-id="9ed6f-126">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-127">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-128">66</span><span class="sxs-lookup"><span data-stu-id="9ed6f-128">66</span></span>

<span data-ttu-id="9ed6f-129">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-130">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-131">67</span><span class="sxs-lookup"><span data-stu-id="9ed6f-131">67</span></span>

<span data-ttu-id="9ed6f-132">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-133">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-134">68</span><span class="sxs-lookup"><span data-stu-id="9ed6f-134">68</span></span>

<span data-ttu-id="9ed6f-135">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-136">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-137">69</span><span class="sxs-lookup"><span data-stu-id="9ed6f-137">69</span></span>

<span data-ttu-id="9ed6f-138">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-139">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-140">70</span><span class="sxs-lookup"><span data-stu-id="9ed6f-140">70</span></span>

<span data-ttu-id="9ed6f-141">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-142">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-143">71</span><span class="sxs-lookup"><span data-stu-id="9ed6f-143">71</span></span>

<span data-ttu-id="9ed6f-144">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-145">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-146">72</span><span class="sxs-lookup"><span data-stu-id="9ed6f-146">72</span></span>

<span data-ttu-id="9ed6f-147">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-148">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-149">73</span><span class="sxs-lookup"><span data-stu-id="9ed6f-149">73</span></span>

<span data-ttu-id="9ed6f-150">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-151">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-152">74</span><span class="sxs-lookup"><span data-stu-id="9ed6f-152">74</span></span>

<span data-ttu-id="9ed6f-153">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-154">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-155">75</span><span class="sxs-lookup"><span data-stu-id="9ed6f-155">75</span></span>

<span data-ttu-id="9ed6f-156">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-157">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-158">76</span><span class="sxs-lookup"><span data-stu-id="9ed6f-158">76</span></span>

<span data-ttu-id="9ed6f-159">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-160">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-161">77</span><span class="sxs-lookup"><span data-stu-id="9ed6f-161">77</span></span>

<span data-ttu-id="9ed6f-162">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-163">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-164">78</span><span class="sxs-lookup"><span data-stu-id="9ed6f-164">78</span></span>

<span data-ttu-id="9ed6f-165">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-166">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-167">79</span><span class="sxs-lookup"><span data-stu-id="9ed6f-167">79</span></span>

<span data-ttu-id="9ed6f-168">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-169">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-170">80</span><span class="sxs-lookup"><span data-stu-id="9ed6f-170">80</span></span>

<span data-ttu-id="9ed6f-171">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-172">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-173">81</span><span class="sxs-lookup"><span data-stu-id="9ed6f-173">81</span></span>

<span data-ttu-id="9ed6f-174">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-175">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-176">82</span><span class="sxs-lookup"><span data-stu-id="9ed6f-176">82</span></span>

<span data-ttu-id="9ed6f-177">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-178">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-179">83</span><span class="sxs-lookup"><span data-stu-id="9ed6f-179">83</span></span>

<span data-ttu-id="9ed6f-180">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-181">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-182">84</span><span class="sxs-lookup"><span data-stu-id="9ed6f-182">84</span></span>

<span data-ttu-id="9ed6f-183">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-184">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-185">85</span><span class="sxs-lookup"><span data-stu-id="9ed6f-185">85</span></span>

<span data-ttu-id="9ed6f-186">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-187">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-188">86</span><span class="sxs-lookup"><span data-stu-id="9ed6f-188">86</span></span>

<span data-ttu-id="9ed6f-189">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-190">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-191">87</span><span class="sxs-lookup"><span data-stu-id="9ed6f-191">87</span></span>

<span data-ttu-id="9ed6f-192">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-193">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-194">88</span><span class="sxs-lookup"><span data-stu-id="9ed6f-194">88</span></span>

<span data-ttu-id="9ed6f-195">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-196">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-197">89</span><span class="sxs-lookup"><span data-stu-id="9ed6f-197">89</span></span>

<span data-ttu-id="9ed6f-198">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-199">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-200">90</span><span class="sxs-lookup"><span data-stu-id="9ed6f-200">90</span></span>

<span data-ttu-id="9ed6f-201">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-202">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-203">91</span><span class="sxs-lookup"><span data-stu-id="9ed6f-203">91</span></span>

<span data-ttu-id="9ed6f-204">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-205">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-206">92</span><span class="sxs-lookup"><span data-stu-id="9ed6f-206">92</span></span>

<span data-ttu-id="9ed6f-207">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="9ed6f-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-208">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-209">93</span><span class="sxs-lookup"><span data-stu-id="9ed6f-209">93</span></span>

<span data-ttu-id="9ed6f-210">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-211">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-212">94</span><span class="sxs-lookup"><span data-stu-id="9ed6f-212">94</span></span>

<span data-ttu-id="9ed6f-213">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-214">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-215">95</span><span class="sxs-lookup"><span data-stu-id="9ed6f-215">95</span></span>

<span data-ttu-id="9ed6f-216">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-217">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-218">96</span><span class="sxs-lookup"><span data-stu-id="9ed6f-218">96</span></span>

<span data-ttu-id="9ed6f-219">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-220">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-221">97</span><span class="sxs-lookup"><span data-stu-id="9ed6f-221">97</span></span>

<span data-ttu-id="9ed6f-222">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-223">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-224">98</span><span class="sxs-lookup"><span data-stu-id="9ed6f-224">98</span></span>

<span data-ttu-id="9ed6f-225">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-226">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-227">100</span><span class="sxs-lookup"><span data-stu-id="9ed6f-227">100</span></span>

<span data-ttu-id="9ed6f-228">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9ed6f-229">**Otros**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="9ed6f-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="9ed6f-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ed6f-231">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ed6f-231">Remarks</span></span>

<span data-ttu-id="9ed6f-232">Este método lo usa la interfaz de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-232">This method is used by the Windows Sockets interface.</span></span> <span data-ttu-id="9ed6f-233">La ruta de acceso predeterminada es% SystemRoot% \\ system32 \\ drivers \\ .</span><span class="sxs-lookup"><span data-stu-id="9ed6f-233">The default path is %SystemRoot%\\system32\\drivers\\ .</span></span>

## <a name="examples"></a><span data-ttu-id="9ed6f-234">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9ed6f-234">Examples</span></span>

<span data-ttu-id="9ed6f-235">En el ejemplo de la galería de TechNet sobre cómo [modificar la ruta de acceso de la base de datos para todos los adaptadores de red](https://Gallery.TechNet.Microsoft.Com/94bfa42f-f6a3-482f-8d5a-5445a2475bee) se usa **SetDatabasePath** para establecer la ruta de acceso a los archivos de base de datos de Internet estándar (hosts, lmhosts, redes, protocolos) usados por la interfaz de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="9ed6f-235">The [Modify the Database Path for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/94bfa42f-f6a3-482f-8d5a-5445a2475bee) VBScript sample on TechNet Gallery uses **SetDatabasePath** to set the path to the standard Internet database files (HOSTS, LMHOSTS, NETWORKS, PROTOCOLS) used by the Windows Sockets interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ed6f-236">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ed6f-236">Requirements</span></span>



| <span data-ttu-id="9ed6f-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ed6f-237">Requirement</span></span> | <span data-ttu-id="9ed6f-238">Value</span><span class="sxs-lookup"><span data-stu-id="9ed6f-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ed6f-239">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ed6f-239">Minimum supported client</span></span><br/> | <span data-ttu-id="9ed6f-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ed6f-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9ed6f-241">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ed6f-241">Minimum supported server</span></span><br/> | <span data-ttu-id="9ed6f-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ed6f-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9ed6f-243">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9ed6f-243">Namespace</span></span><br/>                | <span data-ttu-id="9ed6f-244">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9ed6f-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9ed6f-245">MOF</span><span class="sxs-lookup"><span data-stu-id="9ed6f-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ed6f-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ed6f-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ed6f-247">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9ed6f-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ed6f-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ed6f-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ed6f-249">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ed6f-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ed6f-250">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="9ed6f-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="9ed6f-251">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="9ed6f-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="9ed6f-252">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="9ed6f-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="9ed6f-253">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="9ed6f-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="9ed6f-254">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="9ed6f-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

