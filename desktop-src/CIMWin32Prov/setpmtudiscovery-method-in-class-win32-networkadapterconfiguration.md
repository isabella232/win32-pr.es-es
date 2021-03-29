---
description: El método estático de la clase WMI SetPMTUDiscovery se usa para habilitar la detección de la unidad de transmisión máxima (MTU) a través de la ruta de acceso a un host remoto.
ms.assetid: 43c640bb-c4e7-4b4b-9c18-6cc426229954
ms.tgt_platform: multiple
title: Método SetPMTUDiscovery de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetPMTUDiscovery
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ef3bc9ad5d6203077275f3665c4b0efc98265fbe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807573"
---
# <a name="setpmtudiscovery-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="718c2-103">Método SetPMTUDiscovery de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="718c2-103">SetPMTUDiscovery method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="718c2-104">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetPMTUDiscovery** se usa para habilitar la detección de la unidad de transmisión máxima (MTU) a través de la ruta de acceso a un host remoto.</span><span class="sxs-lookup"><span data-stu-id="718c2-104">The **SetPMTUDiscovery** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable Maximum Transmission Unit (MTU) discovery over the path to a remote host.</span></span>

<span data-ttu-id="718c2-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="718c2-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="718c2-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="718c2-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="718c2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="718c2-107">Syntax</span></span>


```mof
uint32 SetPMTUDiscovery(
  [in] boolean PMTUDiscoveryEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="718c2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="718c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="718c2-109">*PMTUDiscoveryEnabled* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="718c2-109">*PMTUDiscoveryEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="718c2-110">Si es **true**, TCP está habilitado para intentar detectar la unidad de transmisión máxima (MTU) o el tamaño de paquete más grande a través de la ruta de acceso a un host remoto.</span><span class="sxs-lookup"><span data-stu-id="718c2-110">If **true**, TCP is enabled to attempt to discover the Maximum Transmission Unit (MTU) or largest packet size over the path to a remote host.</span></span> <span data-ttu-id="718c2-111">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="718c2-111">The default is **true**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="718c2-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="718c2-112">Return value</span></span>

<span data-ttu-id="718c2-113">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="718c2-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="718c2-114">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="718c2-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="718c2-115">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="718c2-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="718c2-116">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="718c2-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-117">0</span><span class="sxs-lookup"><span data-stu-id="718c2-117">0</span></span>

<span data-ttu-id="718c2-118">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="718c2-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-119">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="718c2-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-120">1</span><span class="sxs-lookup"><span data-stu-id="718c2-120">1</span></span>

<span data-ttu-id="718c2-121">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="718c2-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-122">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="718c2-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-123">64</span><span class="sxs-lookup"><span data-stu-id="718c2-123">64</span></span>

<span data-ttu-id="718c2-124">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="718c2-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-125">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="718c2-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-126">65</span><span class="sxs-lookup"><span data-stu-id="718c2-126">65</span></span>

<span data-ttu-id="718c2-127">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="718c2-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-128">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="718c2-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-129">66</span><span class="sxs-lookup"><span data-stu-id="718c2-129">66</span></span>

<span data-ttu-id="718c2-130">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="718c2-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-131">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="718c2-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-132">67</span><span class="sxs-lookup"><span data-stu-id="718c2-132">67</span></span>

<span data-ttu-id="718c2-133">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="718c2-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-134">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="718c2-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-135">68</span><span class="sxs-lookup"><span data-stu-id="718c2-135">68</span></span>

<span data-ttu-id="718c2-136">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="718c2-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-137">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="718c2-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-138">69</span><span class="sxs-lookup"><span data-stu-id="718c2-138">69</span></span>

<span data-ttu-id="718c2-139">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="718c2-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-140">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="718c2-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-141">70</span><span class="sxs-lookup"><span data-stu-id="718c2-141">70</span></span>

<span data-ttu-id="718c2-142">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="718c2-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-143">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="718c2-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-144">71</span><span class="sxs-lookup"><span data-stu-id="718c2-144">71</span></span>

<span data-ttu-id="718c2-145">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="718c2-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-146">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="718c2-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-147">72</span><span class="sxs-lookup"><span data-stu-id="718c2-147">72</span></span>

<span data-ttu-id="718c2-148">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="718c2-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-149">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="718c2-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-150">73</span><span class="sxs-lookup"><span data-stu-id="718c2-150">73</span></span>

<span data-ttu-id="718c2-151">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="718c2-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-152">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="718c2-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-153">74</span><span class="sxs-lookup"><span data-stu-id="718c2-153">74</span></span>

<span data-ttu-id="718c2-154">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="718c2-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-155">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="718c2-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-156">75</span><span class="sxs-lookup"><span data-stu-id="718c2-156">75</span></span>

<span data-ttu-id="718c2-157">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="718c2-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-158">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="718c2-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-159">76</span><span class="sxs-lookup"><span data-stu-id="718c2-159">76</span></span>

<span data-ttu-id="718c2-160">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="718c2-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-161">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="718c2-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-162">77</span><span class="sxs-lookup"><span data-stu-id="718c2-162">77</span></span>

<span data-ttu-id="718c2-163">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="718c2-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-164">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="718c2-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-165">78</span><span class="sxs-lookup"><span data-stu-id="718c2-165">78</span></span>

<span data-ttu-id="718c2-166">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="718c2-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-167">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="718c2-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-168">79</span><span class="sxs-lookup"><span data-stu-id="718c2-168">79</span></span>

<span data-ttu-id="718c2-169">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="718c2-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-170">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="718c2-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-171">80</span><span class="sxs-lookup"><span data-stu-id="718c2-171">80</span></span>

<span data-ttu-id="718c2-172">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="718c2-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-173">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="718c2-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-174">81</span><span class="sxs-lookup"><span data-stu-id="718c2-174">81</span></span>

<span data-ttu-id="718c2-175">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="718c2-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-176">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="718c2-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-177">82</span><span class="sxs-lookup"><span data-stu-id="718c2-177">82</span></span>

<span data-ttu-id="718c2-178">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="718c2-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-179">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="718c2-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-180">83</span><span class="sxs-lookup"><span data-stu-id="718c2-180">83</span></span>

<span data-ttu-id="718c2-181">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="718c2-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-182">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="718c2-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-183">84</span><span class="sxs-lookup"><span data-stu-id="718c2-183">84</span></span>

<span data-ttu-id="718c2-184">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="718c2-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-185">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="718c2-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-186">85</span><span class="sxs-lookup"><span data-stu-id="718c2-186">85</span></span>

<span data-ttu-id="718c2-187">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="718c2-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-188">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="718c2-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-189">86</span><span class="sxs-lookup"><span data-stu-id="718c2-189">86</span></span>

<span data-ttu-id="718c2-190">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="718c2-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-191">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="718c2-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-192">87</span><span class="sxs-lookup"><span data-stu-id="718c2-192">87</span></span>

<span data-ttu-id="718c2-193">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="718c2-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-194">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="718c2-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-195">88</span><span class="sxs-lookup"><span data-stu-id="718c2-195">88</span></span>

<span data-ttu-id="718c2-196">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="718c2-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-197">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="718c2-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-198">89</span><span class="sxs-lookup"><span data-stu-id="718c2-198">89</span></span>

<span data-ttu-id="718c2-199">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="718c2-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-200">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="718c2-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-201">90</span><span class="sxs-lookup"><span data-stu-id="718c2-201">90</span></span>

<span data-ttu-id="718c2-202">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="718c2-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-203">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="718c2-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-204">91</span><span class="sxs-lookup"><span data-stu-id="718c2-204">91</span></span>

<span data-ttu-id="718c2-205">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="718c2-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-206">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="718c2-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-207">92</span><span class="sxs-lookup"><span data-stu-id="718c2-207">92</span></span>

<span data-ttu-id="718c2-208">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="718c2-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-209">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="718c2-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-210">93</span><span class="sxs-lookup"><span data-stu-id="718c2-210">93</span></span>

<span data-ttu-id="718c2-211">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="718c2-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-212">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="718c2-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-213">94</span><span class="sxs-lookup"><span data-stu-id="718c2-213">94</span></span>

<span data-ttu-id="718c2-214">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="718c2-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-215">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="718c2-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-216">95</span><span class="sxs-lookup"><span data-stu-id="718c2-216">95</span></span>

<span data-ttu-id="718c2-217">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="718c2-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-218">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="718c2-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-219">96</span><span class="sxs-lookup"><span data-stu-id="718c2-219">96</span></span>

<span data-ttu-id="718c2-220">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="718c2-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-221">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="718c2-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-222">97</span><span class="sxs-lookup"><span data-stu-id="718c2-222">97</span></span>

<span data-ttu-id="718c2-223">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="718c2-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-224">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="718c2-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-225">98</span><span class="sxs-lookup"><span data-stu-id="718c2-225">98</span></span>

<span data-ttu-id="718c2-226">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="718c2-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-227">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="718c2-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-228">100</span><span class="sxs-lookup"><span data-stu-id="718c2-228">100</span></span>

<span data-ttu-id="718c2-229">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="718c2-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="718c2-230">**Otros**</span><span class="sxs-lookup"><span data-stu-id="718c2-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="718c2-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="718c2-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="718c2-232">Observaciones</span><span class="sxs-lookup"><span data-stu-id="718c2-232">Remarks</span></span>

<span data-ttu-id="718c2-233">Al detectar la MTU de la ruta de acceso y limitar los segmentos TCP a este tamaño, TCP puede eliminar la fragmentación en los enrutadores a lo largo de la ruta de acceso que conecta las redes con diferentes MTU.</span><span class="sxs-lookup"><span data-stu-id="718c2-233">By discovering the Path MTU and limiting TCP segments to this size, TCP can eliminate fragmentation at routers along the path that connect networks with different MTUs.</span></span> <span data-ttu-id="718c2-234">La fragmentación afecta negativamente al rendimiento TCP y a la congestión de la red.</span><span class="sxs-lookup"><span data-stu-id="718c2-234">Fragmentation adversely affects TCP throughput and network congestion.</span></span> <span data-ttu-id="718c2-235">Si se establece este parámetro en **false** , se usará una MTU de 576 bytes para todas las conexiones que no sean equipos de la subred local.</span><span class="sxs-lookup"><span data-stu-id="718c2-235">Setting this parameter to **FALSE** causes an MTU of 576 bytes to be used for all connections that are not to machines on the local subnet</span></span>

## <a name="examples"></a><span data-ttu-id="718c2-236">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="718c2-236">Examples</span></span>

<span data-ttu-id="718c2-237">El ejemplo de la [habilitación de la detección de PMTU en todos los adaptadores de red](https://Gallery.TechNet.Microsoft.Com/dd68dc8d-d452-484c-add7-2da5c87c3568) de VBScript permite que un equipo detecte automáticamente la unidad de transmisión máxima en una red.</span><span class="sxs-lookup"><span data-stu-id="718c2-237">The [Enable PMTU Discovery on all Network Adapters](https://Gallery.TechNet.Microsoft.Com/dd68dc8d-d452-484c-add7-2da5c87c3568) VBScript sample enables a computer to automatically discover the maximum transmission unit on a network.</span></span>

## <a name="requirements"></a><span data-ttu-id="718c2-238">Requisitos</span><span class="sxs-lookup"><span data-stu-id="718c2-238">Requirements</span></span>



| <span data-ttu-id="718c2-239">Requisito</span><span class="sxs-lookup"><span data-stu-id="718c2-239">Requirement</span></span> | <span data-ttu-id="718c2-240">Value</span><span class="sxs-lookup"><span data-stu-id="718c2-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="718c2-241">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="718c2-241">Minimum supported client</span></span><br/> | <span data-ttu-id="718c2-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="718c2-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="718c2-243">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="718c2-243">Minimum supported server</span></span><br/> | <span data-ttu-id="718c2-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="718c2-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="718c2-245">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="718c2-245">Namespace</span></span><br/>                | <span data-ttu-id="718c2-246">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="718c2-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="718c2-247">MOF</span><span class="sxs-lookup"><span data-stu-id="718c2-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="718c2-248"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="718c2-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="718c2-249">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="718c2-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="718c2-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="718c2-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="718c2-251">Vea también</span><span class="sxs-lookup"><span data-stu-id="718c2-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="718c2-252">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="718c2-252">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="718c2-253">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="718c2-253">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="718c2-254">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="718c2-254">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="718c2-255">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="718c2-255">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="718c2-256">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="718c2-256">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

