---
description: El método estático de la clase WMI SetPMTUBHDetect se usa para habilitar la detección de enrutadores de agujeros negros mientras se realiza la detección de MTU de ruta de acceso.
ms.assetid: a1e45ed9-85a9-4fdd-890a-d578c3f94b72
ms.tgt_platform: multiple
title: Método SetPMTUBHDetect de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetPMTUBHDetect
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 098652c6ea0a53f9d3b1f616def3dd8b5e7228af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153216"
---
# <a name="setpmtubhdetect-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="98bfb-103">Método SetPMTUBHDetect de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="98bfb-103">SetPMTUBHDetect method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="98bfb-104">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetPMTUBHDetect** se usa para habilitar la detección de enrutadores de agujeros negros mientras se realiza la detección de MTU de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="98bfb-104">The **SetPMTUBHDetect** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable the detection of Black Hole routers while doing Path MTU Discovery.</span></span>

<span data-ttu-id="98bfb-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="98bfb-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="98bfb-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="98bfb-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="98bfb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98bfb-107">Syntax</span></span>


```mof
uint32 SetPMTUBHDetect(
  [in] boolean PMTUBHDetectEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="98bfb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98bfb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98bfb-109">*PMTUBHDetectEnabled* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="98bfb-109">*PMTUBHDetectEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-110">Si **es true**, TCP intenta detectar agujeros negros y enrutar los paquetes en rutas de acceso de red diferentes.</span><span class="sxs-lookup"><span data-stu-id="98bfb-110">If **true**, TCP attempts to discover Black Hole and route packets in different network paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98bfb-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98bfb-111">Return value</span></span>

<span data-ttu-id="98bfb-112">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="98bfb-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="98bfb-113">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="98bfb-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="98bfb-114">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="98bfb-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="98bfb-115">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="98bfb-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-116">0</span><span class="sxs-lookup"><span data-stu-id="98bfb-116">0</span></span>

<span data-ttu-id="98bfb-117">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="98bfb-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-118">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="98bfb-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-119">1</span><span class="sxs-lookup"><span data-stu-id="98bfb-119">1</span></span>

<span data-ttu-id="98bfb-120">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="98bfb-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-121">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="98bfb-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-122">64</span><span class="sxs-lookup"><span data-stu-id="98bfb-122">64</span></span>

<span data-ttu-id="98bfb-123">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="98bfb-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-124">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="98bfb-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-125">65</span><span class="sxs-lookup"><span data-stu-id="98bfb-125">65</span></span>

<span data-ttu-id="98bfb-126">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="98bfb-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-127">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="98bfb-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-128">66</span><span class="sxs-lookup"><span data-stu-id="98bfb-128">66</span></span>

<span data-ttu-id="98bfb-129">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="98bfb-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-130">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="98bfb-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-131">67</span><span class="sxs-lookup"><span data-stu-id="98bfb-131">67</span></span>

<span data-ttu-id="98bfb-132">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="98bfb-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-133">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="98bfb-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-134">68</span><span class="sxs-lookup"><span data-stu-id="98bfb-134">68</span></span>

<span data-ttu-id="98bfb-135">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="98bfb-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-136">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="98bfb-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-137">69</span><span class="sxs-lookup"><span data-stu-id="98bfb-137">69</span></span>

<span data-ttu-id="98bfb-138">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="98bfb-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-139">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="98bfb-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-140">70</span><span class="sxs-lookup"><span data-stu-id="98bfb-140">70</span></span>

<span data-ttu-id="98bfb-141">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="98bfb-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-142">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="98bfb-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-143">71</span><span class="sxs-lookup"><span data-stu-id="98bfb-143">71</span></span>

<span data-ttu-id="98bfb-144">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="98bfb-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-145">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="98bfb-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-146">72</span><span class="sxs-lookup"><span data-stu-id="98bfb-146">72</span></span>

<span data-ttu-id="98bfb-147">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="98bfb-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-148">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="98bfb-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-149">73</span><span class="sxs-lookup"><span data-stu-id="98bfb-149">73</span></span>

<span data-ttu-id="98bfb-150">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="98bfb-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-151">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="98bfb-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-152">74</span><span class="sxs-lookup"><span data-stu-id="98bfb-152">74</span></span>

<span data-ttu-id="98bfb-153">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="98bfb-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-154">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="98bfb-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-155">75</span><span class="sxs-lookup"><span data-stu-id="98bfb-155">75</span></span>

<span data-ttu-id="98bfb-156">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="98bfb-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-157">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="98bfb-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-158">76</span><span class="sxs-lookup"><span data-stu-id="98bfb-158">76</span></span>

<span data-ttu-id="98bfb-159">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="98bfb-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-160">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="98bfb-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-161">77</span><span class="sxs-lookup"><span data-stu-id="98bfb-161">77</span></span>

<span data-ttu-id="98bfb-162">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="98bfb-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-163">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="98bfb-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-164">78</span><span class="sxs-lookup"><span data-stu-id="98bfb-164">78</span></span>

<span data-ttu-id="98bfb-165">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="98bfb-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-166">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="98bfb-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-167">79</span><span class="sxs-lookup"><span data-stu-id="98bfb-167">79</span></span>

<span data-ttu-id="98bfb-168">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="98bfb-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-169">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="98bfb-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-170">80</span><span class="sxs-lookup"><span data-stu-id="98bfb-170">80</span></span>

<span data-ttu-id="98bfb-171">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="98bfb-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-172">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="98bfb-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-173">81</span><span class="sxs-lookup"><span data-stu-id="98bfb-173">81</span></span>

<span data-ttu-id="98bfb-174">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="98bfb-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-175">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="98bfb-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-176">82</span><span class="sxs-lookup"><span data-stu-id="98bfb-176">82</span></span>

<span data-ttu-id="98bfb-177">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="98bfb-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-178">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="98bfb-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-179">83</span><span class="sxs-lookup"><span data-stu-id="98bfb-179">83</span></span>

<span data-ttu-id="98bfb-180">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="98bfb-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-181">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="98bfb-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-182">84</span><span class="sxs-lookup"><span data-stu-id="98bfb-182">84</span></span>

<span data-ttu-id="98bfb-183">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="98bfb-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-184">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="98bfb-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-185">85</span><span class="sxs-lookup"><span data-stu-id="98bfb-185">85</span></span>

<span data-ttu-id="98bfb-186">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="98bfb-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-187">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="98bfb-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-188">86</span><span class="sxs-lookup"><span data-stu-id="98bfb-188">86</span></span>

<span data-ttu-id="98bfb-189">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="98bfb-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-190">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="98bfb-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-191">87</span><span class="sxs-lookup"><span data-stu-id="98bfb-191">87</span></span>

<span data-ttu-id="98bfb-192">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="98bfb-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-193">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="98bfb-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-194">88</span><span class="sxs-lookup"><span data-stu-id="98bfb-194">88</span></span>

<span data-ttu-id="98bfb-195">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="98bfb-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-196">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="98bfb-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-197">89</span><span class="sxs-lookup"><span data-stu-id="98bfb-197">89</span></span>

<span data-ttu-id="98bfb-198">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="98bfb-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-199">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="98bfb-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-200">90</span><span class="sxs-lookup"><span data-stu-id="98bfb-200">90</span></span>

<span data-ttu-id="98bfb-201">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="98bfb-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-202">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="98bfb-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-203">91</span><span class="sxs-lookup"><span data-stu-id="98bfb-203">91</span></span>

<span data-ttu-id="98bfb-204">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="98bfb-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-205">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="98bfb-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-206">92</span><span class="sxs-lookup"><span data-stu-id="98bfb-206">92</span></span>

<span data-ttu-id="98bfb-207">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="98bfb-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-208">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="98bfb-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-209">93</span><span class="sxs-lookup"><span data-stu-id="98bfb-209">93</span></span>

<span data-ttu-id="98bfb-210">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="98bfb-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-211">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="98bfb-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-212">94</span><span class="sxs-lookup"><span data-stu-id="98bfb-212">94</span></span>

<span data-ttu-id="98bfb-213">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="98bfb-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-214">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="98bfb-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-215">95</span><span class="sxs-lookup"><span data-stu-id="98bfb-215">95</span></span>

<span data-ttu-id="98bfb-216">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="98bfb-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-217">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="98bfb-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-218">96</span><span class="sxs-lookup"><span data-stu-id="98bfb-218">96</span></span>

<span data-ttu-id="98bfb-219">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="98bfb-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-220">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="98bfb-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-221">97</span><span class="sxs-lookup"><span data-stu-id="98bfb-221">97</span></span>

<span data-ttu-id="98bfb-222">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="98bfb-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-223">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="98bfb-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-224">98</span><span class="sxs-lookup"><span data-stu-id="98bfb-224">98</span></span>

<span data-ttu-id="98bfb-225">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="98bfb-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-226">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="98bfb-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-227">100</span><span class="sxs-lookup"><span data-stu-id="98bfb-227">100</span></span>

<span data-ttu-id="98bfb-228">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="98bfb-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-229">**Otros**</span><span class="sxs-lookup"><span data-stu-id="98bfb-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="98bfb-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="98bfb-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98bfb-231">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98bfb-231">Remarks</span></span>

<span data-ttu-id="98bfb-232">Un enrutador de agujeros negros no devuelve los mensajes inaccesibles de destino del Protocolo de mensajes de control de Internet (ICMP) cuando es necesario fragmentar un datagrama IP con el bit de no fragmentación establecido.</span><span class="sxs-lookup"><span data-stu-id="98bfb-232">A Black Hole router does not return the Internet Control Message Protocol (ICMP) Destination Unreachable messages when it needs to fragment an IP datagram with the Don't Fragment bit set.</span></span> <span data-ttu-id="98bfb-233">TCP depende de la recepción de estos mensajes para realizar la detección de MTU de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="98bfb-233">TCP depends on receiving these messages to perform Path MTU Discovery.</span></span>

<span data-ttu-id="98bfb-234">Con esta característica habilitada, TCP intentará enviar segmentos sin el bit de no fragmentación establecido si varias retransmisiones de un segmento van a no confirmarse.</span><span class="sxs-lookup"><span data-stu-id="98bfb-234">With this feature enabled, TCP will try to send segments without the Don't Fragment bit set if several retransmissions of a segment go unacknowledged.</span></span> <span data-ttu-id="98bfb-235">Si el segmento se confirma como resultado, se reducirá el tamaño máximo del segmento (MSS) y el bit no fragmentar se establecerá en paquetes futuros en la conexión.</span><span class="sxs-lookup"><span data-stu-id="98bfb-235">If the segment is acknowledged as a result, the maximum segment size (MSS) will be decreased and the Don't Fragment bit will be set in future packets on the connection.</span></span> <span data-ttu-id="98bfb-236">La habilitación de la detección de agujeros negros aumenta el número máximo de retransmisiones realizadas para un segmento determinado.</span><span class="sxs-lookup"><span data-stu-id="98bfb-236">Enabling black hole detection increases the maximum number of retransmissions performed for a given segment.</span></span>

## <a name="examples"></a><span data-ttu-id="98bfb-237">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="98bfb-237">Examples</span></span>

<span data-ttu-id="98bfb-238">La [detección de modificación de PMTUBH en todos los adaptadores de red](https://Gallery.TechNet.Microsoft.Com/a576d97b-38fe-437e-a632-d2f7e122301c) permite la detección automática de enrutadores de agujeros negros al determinar la unidad de transmisión máxima de una red.</span><span class="sxs-lookup"><span data-stu-id="98bfb-238">The [Modify PMTUBH Detection on All Network Adapters](https://Gallery.TechNet.Microsoft.Com/a576d97b-38fe-437e-a632-d2f7e122301c) enables the auto-discovery of black hole routers when determining the maximum transmission unit on a network.</span></span>

## <a name="requirements"></a><span data-ttu-id="98bfb-239">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98bfb-239">Requirements</span></span>



| <span data-ttu-id="98bfb-240">Requisito</span><span class="sxs-lookup"><span data-stu-id="98bfb-240">Requirement</span></span> | <span data-ttu-id="98bfb-241">Value</span><span class="sxs-lookup"><span data-stu-id="98bfb-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98bfb-242">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98bfb-242">Minimum supported client</span></span><br/> | <span data-ttu-id="98bfb-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98bfb-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="98bfb-244">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98bfb-244">Minimum supported server</span></span><br/> | <span data-ttu-id="98bfb-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98bfb-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="98bfb-246">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="98bfb-246">Namespace</span></span><br/>                | <span data-ttu-id="98bfb-247">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="98bfb-247">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="98bfb-248">MOF</span><span class="sxs-lookup"><span data-stu-id="98bfb-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98bfb-249"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98bfb-249"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="98bfb-250">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="98bfb-250">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98bfb-251"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98bfb-251"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98bfb-252">Vea también</span><span class="sxs-lookup"><span data-stu-id="98bfb-252">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98bfb-253">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="98bfb-253">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="98bfb-254">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="98bfb-254">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="98bfb-255">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="98bfb-255">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="98bfb-256">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="98bfb-256">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="98bfb-257">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="98bfb-257">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

