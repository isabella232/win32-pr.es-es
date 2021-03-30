---
description: El método de clase WMI EnableStatic habilita el direccionamiento TCP/IP estático para el adaptador de red de destino. Como resultado, se deshabilita DHCP para este adaptador de red.
ms.assetid: d0076424-58c0-4cfe-b55b-44c0f2620388
ms.tgt_platform: multiple
title: Método EnableStatic de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableStatic
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 74a7b9ca8c8016cca5a78f2e7fe753f00398193e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807256"
---
# <a name="enablestatic-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="45351-104">Método EnableStatic de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="45351-104">EnableStatic method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="45351-105">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableStatic** habilita el direccionamiento TCP/IP estático para el adaptador de red de destino.</span><span class="sxs-lookup"><span data-stu-id="45351-105">The **EnableStatic** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method enables static TCP/IP addressing for the target network adapter.</span></span> <span data-ttu-id="45351-106">Como resultado, se deshabilita DHCP para este adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="45351-106">As a result, DHCP for this network adapter is disabled.</span></span>

<span data-ttu-id="45351-107">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="45351-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="45351-108">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="45351-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="45351-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45351-109">Syntax</span></span>


```mof
uint32 EnableStatic(
  [in] string IPAddress[],
  [in] string SubnetMask[]
);
```



## <a name="parameters"></a><span data-ttu-id="45351-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45351-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45351-111">*Dirección IP* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45351-111">*IPAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45351-112">Muestra todas las direcciones IP estáticas para el adaptador de red actual.</span><span class="sxs-lookup"><span data-stu-id="45351-112">Lists all of the static IP addresses for the current network adapter.</span></span>

<span data-ttu-id="45351-113">Ejemplo: 155.34.22.0.</span><span class="sxs-lookup"><span data-stu-id="45351-113">Example: 155.34.22.0.</span></span>

</dd> <dt>

<span data-ttu-id="45351-114">*Máscaradesubred* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45351-114">*SubnetMask* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45351-115">Máscaras de subred que complementan los valores del parámetro *IPAddress* .</span><span class="sxs-lookup"><span data-stu-id="45351-115">Subnet masks that complement the values in the *IPAddress* parameter.</span></span>

<span data-ttu-id="45351-116">Ejemplo: 255.255.0.0.</span><span class="sxs-lookup"><span data-stu-id="45351-116">Example: 255.255.0.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45351-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45351-117">Return value</span></span>

<span data-ttu-id="45351-118">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere un reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y cualquier otro número si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="45351-118">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="45351-119">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="45351-119">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="45351-120">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="45351-120">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="45351-121">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="45351-121">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="45351-122">0</span><span class="sxs-lookup"><span data-stu-id="45351-122">0</span></span>

<span data-ttu-id="45351-123">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="45351-123">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="45351-124">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="45351-124">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="45351-125">1</span><span class="sxs-lookup"><span data-stu-id="45351-125">1</span></span>

<span data-ttu-id="45351-126">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="45351-126">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="45351-127">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="45351-127">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="45351-128">64</span><span class="sxs-lookup"><span data-stu-id="45351-128">64</span></span>

<span data-ttu-id="45351-129">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="45351-129">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="45351-130">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="45351-130">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="45351-131">65</span><span class="sxs-lookup"><span data-stu-id="45351-131">65</span></span>

<span data-ttu-id="45351-132">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="45351-132">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="45351-133">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="45351-133">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="45351-134">66</span><span class="sxs-lookup"><span data-stu-id="45351-134">66</span></span>

<span data-ttu-id="45351-135">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="45351-135">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="45351-136">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="45351-136">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="45351-137">67</span><span class="sxs-lookup"><span data-stu-id="45351-137">67</span></span>

<span data-ttu-id="45351-138">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="45351-138">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="45351-139">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="45351-139">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="45351-140">68</span><span class="sxs-lookup"><span data-stu-id="45351-140">68</span></span>

<span data-ttu-id="45351-141">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="45351-141">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="45351-142">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="45351-142">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="45351-143">69</span><span class="sxs-lookup"><span data-stu-id="45351-143">69</span></span>

<span data-ttu-id="45351-144">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="45351-144">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="45351-145">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="45351-145">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="45351-146">70</span><span class="sxs-lookup"><span data-stu-id="45351-146">70</span></span>

<span data-ttu-id="45351-147">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="45351-147">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="45351-148">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="45351-148">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="45351-149">71</span><span class="sxs-lookup"><span data-stu-id="45351-149">71</span></span>

<span data-ttu-id="45351-150">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="45351-150">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="45351-151">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="45351-151">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="45351-152">72</span><span class="sxs-lookup"><span data-stu-id="45351-152">72</span></span>

<span data-ttu-id="45351-153">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="45351-153">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="45351-154">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="45351-154">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="45351-155">73</span><span class="sxs-lookup"><span data-stu-id="45351-155">73</span></span>

<span data-ttu-id="45351-156">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="45351-156">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="45351-157">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="45351-157">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="45351-158">74</span><span class="sxs-lookup"><span data-stu-id="45351-158">74</span></span>

<span data-ttu-id="45351-159">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="45351-159">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="45351-160">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="45351-160">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="45351-161">75</span><span class="sxs-lookup"><span data-stu-id="45351-161">75</span></span>

<span data-ttu-id="45351-162">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="45351-162">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="45351-163">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="45351-163">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="45351-164">76</span><span class="sxs-lookup"><span data-stu-id="45351-164">76</span></span>

<span data-ttu-id="45351-165">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="45351-165">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="45351-166">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="45351-166">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="45351-167">77</span><span class="sxs-lookup"><span data-stu-id="45351-167">77</span></span>

<span data-ttu-id="45351-168">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="45351-168">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="45351-169">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="45351-169">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="45351-170">78</span><span class="sxs-lookup"><span data-stu-id="45351-170">78</span></span>

<span data-ttu-id="45351-171">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="45351-171">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="45351-172">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="45351-172">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="45351-173">79</span><span class="sxs-lookup"><span data-stu-id="45351-173">79</span></span>

<span data-ttu-id="45351-174">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="45351-174">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="45351-175">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="45351-175">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="45351-176">80</span><span class="sxs-lookup"><span data-stu-id="45351-176">80</span></span>

<span data-ttu-id="45351-177">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="45351-177">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="45351-178">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="45351-178">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="45351-179">81</span><span class="sxs-lookup"><span data-stu-id="45351-179">81</span></span>

<span data-ttu-id="45351-180">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="45351-180">Unable to configure DHCP service.</span></span> <span data-ttu-id="45351-181">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="45351-181">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="45351-182">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="45351-182">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="45351-183">82</span><span class="sxs-lookup"><span data-stu-id="45351-183">82</span></span>

<span data-ttu-id="45351-184">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="45351-184">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="45351-185">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="45351-185">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="45351-186">83</span><span class="sxs-lookup"><span data-stu-id="45351-186">83</span></span>

<span data-ttu-id="45351-187">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="45351-187">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="45351-188">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="45351-188">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="45351-189">84</span><span class="sxs-lookup"><span data-stu-id="45351-189">84</span></span>

<span data-ttu-id="45351-190">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="45351-190">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="45351-191">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="45351-191">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="45351-192">85</span><span class="sxs-lookup"><span data-stu-id="45351-192">85</span></span>

<span data-ttu-id="45351-193">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="45351-193">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="45351-194">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="45351-194">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="45351-195">86</span><span class="sxs-lookup"><span data-stu-id="45351-195">86</span></span>

<span data-ttu-id="45351-196">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="45351-196">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="45351-197">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="45351-197">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="45351-198">87</span><span class="sxs-lookup"><span data-stu-id="45351-198">87</span></span>

<span data-ttu-id="45351-199">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="45351-199">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="45351-200">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="45351-200">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="45351-201">88</span><span class="sxs-lookup"><span data-stu-id="45351-201">88</span></span>

<span data-ttu-id="45351-202">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="45351-202">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="45351-203">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="45351-203">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="45351-204">89</span><span class="sxs-lookup"><span data-stu-id="45351-204">89</span></span>

<span data-ttu-id="45351-205">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="45351-205">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="45351-206">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="45351-206">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="45351-207">90</span><span class="sxs-lookup"><span data-stu-id="45351-207">90</span></span>

<span data-ttu-id="45351-208">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="45351-208">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="45351-209">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="45351-209">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="45351-210">91</span><span class="sxs-lookup"><span data-stu-id="45351-210">91</span></span>

<span data-ttu-id="45351-211">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="45351-211">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="45351-212">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="45351-212">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="45351-213">92</span><span class="sxs-lookup"><span data-stu-id="45351-213">92</span></span>

<span data-ttu-id="45351-214">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="45351-214">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="45351-215">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="45351-215">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="45351-216">93</span><span class="sxs-lookup"><span data-stu-id="45351-216">93</span></span>

<span data-ttu-id="45351-217">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="45351-217">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="45351-218">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="45351-218">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="45351-219">94</span><span class="sxs-lookup"><span data-stu-id="45351-219">94</span></span>

<span data-ttu-id="45351-220">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="45351-220">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="45351-221">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="45351-221">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="45351-222">95</span><span class="sxs-lookup"><span data-stu-id="45351-222">95</span></span>

<span data-ttu-id="45351-223">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="45351-223">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="45351-224">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="45351-224">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="45351-225">96</span><span class="sxs-lookup"><span data-stu-id="45351-225">96</span></span>

<span data-ttu-id="45351-226">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="45351-226">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="45351-227">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="45351-227">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="45351-228">97</span><span class="sxs-lookup"><span data-stu-id="45351-228">97</span></span>

<span data-ttu-id="45351-229">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="45351-229">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="45351-230">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="45351-230">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="45351-231">98</span><span class="sxs-lookup"><span data-stu-id="45351-231">98</span></span>

<span data-ttu-id="45351-232">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="45351-232">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="45351-233">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="45351-233">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="45351-234">100</span><span class="sxs-lookup"><span data-stu-id="45351-234">100</span></span>

<span data-ttu-id="45351-235">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="45351-235">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="45351-236">**2147786788**</span><span class="sxs-lookup"><span data-stu-id="45351-236">**2147786788**</span></span>
</dt> <dd>

<span data-ttu-id="45351-237">Bloqueo de escritura no habilitado.</span><span class="sxs-lookup"><span data-stu-id="45351-237">Write lock not enabled.</span></span> <span data-ttu-id="45351-238">Para obtener más información, vea [**INetCfgLock:: AcquireWriteLock**](/previous-versions/windows/hardware/network/ff547914(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="45351-238">For more information, see [**INetCfgLock::AcquireWriteLock**](/previous-versions/windows/hardware/network/ff547914(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="45351-239">**Otros**</span><span class="sxs-lookup"><span data-stu-id="45351-239">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="45351-240">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="45351-240">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45351-241">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45351-241">Remarks</span></span>

<span data-ttu-id="45351-242">Cuando se usa **EnableStatic** para cambiar la dirección IP del equipo remoto, mientras se está conectando a través de ese adaptador, es probable que se pierda la conexión al equipo remoto y reciba un mensaje de error de RPC no disponible.</span><span class="sxs-lookup"><span data-stu-id="45351-242">When using **EnableStatic** to change the IP address of the remote computer, while being connected through that adapter, you will likely loose connection to the remote computer, and receive an RPC not available error-message.</span></span> <span data-ttu-id="45351-243">(sin embargo, se cambia la configuración).</span><span class="sxs-lookup"><span data-stu-id="45351-243">(the settings are changed however).</span></span> <span data-ttu-id="45351-244">Para evitar este escenario, considere la posibilidad de cambiar la configuración de la puerta de enlace o DNS antes de establecer la dirección IP del adaptador.</span><span class="sxs-lookup"><span data-stu-id="45351-244">To avoid this scenario, consider changing the Gateway and/or DNS-settings prior to setting the adapter's IP-address.</span></span>

<span data-ttu-id="45351-245">Cuando se usa **EnableStatic** para conceder a un adaptador una configuración de IP estática, la función devuelve un "81: no se puede configurar el servicio DHCP" si el adaptador ya está configurado con una dirección estática.</span><span class="sxs-lookup"><span data-stu-id="45351-245">When using **EnableStatic** to give an adapter a static IP configuration, the function returns an "81 - Unable to configure DHCP service" if the adapter is already configured with a static address.</span></span> <span data-ttu-id="45351-246">Sin embargo, la función todavía se ejecuta correctamente con la nueva operación.</span><span class="sxs-lookup"><span data-stu-id="45351-246">However, the function still succeeds in setting with the new operation.</span></span>

## <a name="examples"></a><span data-ttu-id="45351-247">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="45351-247">Examples</span></span>

<span data-ttu-id="45351-248">La [dirección IP estática y, a continuación, unirse a un](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) ejemplo de código de PowerShell de dominio, en la galería de TechNet, usa **EnableStatic** para agregar una dirección IP estática a una máquina local.</span><span class="sxs-lookup"><span data-stu-id="45351-248">The [Static IP and then join to a domain](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) PowerShell code sample, on TechNet Gallery, uses **EnableStatic** to add a static IP to a local machine.</span></span>

<span data-ttu-id="45351-249">En el ejemplo de código de VBScript [asignar una dirección IP estática](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) , en la galería de TechNet, usa **EnableStatic** para establecer la dirección IP de un equipo.</span><span class="sxs-lookup"><span data-stu-id="45351-249">The [Assign a Static IP Address](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) VBScript code example, on TechNet Gallery, uses **EnableStatic** to set the IP address of a computer.</span></span>

<span data-ttu-id="45351-250">En el siguiente ejemplo de VBScript se muestra cómo deshabilitar el uso de DHCP en una instancia de [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="45351-250">The following VBScript sample demonstrates how to disable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span></span> <span data-ttu-id="45351-251">En este caso, especificamos el adaptador con un índice de 0.</span><span class="sxs-lookup"><span data-stu-id="45351-251">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="45351-252">Se debe seleccionar el índice correcto en \_ las instancias de Win32 para otras interfaces.</span><span class="sxs-lookup"><span data-stu-id="45351-252">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="45351-253">Este script solo se aplica a los sistemas basados en NT. cambie las variables DirIP y Subnet siguientes a los valores que desee aplicar al adaptador.</span><span class="sxs-lookup"><span data-stu-id="45351-253">This script only applies to NT-based systems Change the ipaddr and subnet variables below to the values you wish to apply to the adapter.</span></span>

 


```VB
Set Adapter = GetObject("winmgmts:Win32_NetworkAdapterConfiguration=1")

ipaddr = Array("1.1.1.1")
subnet = Array("255.255.255.0")


RetVal = Adapter.EnableStatic(ipaddr,subnet)

if RetVal = 0 then 
 WScript.Echo "DHCP disabled, using static IP address"
else 
 WScript.Echo "DHCP disable failed"
end if
```



<span data-ttu-id="45351-254">En el siguiente ejemplo de Perl se muestra cómo deshabilitar el uso de DHCP en una instancia de [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="45351-254">The following Perl sample demonstrates how to disable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span></span> <span data-ttu-id="45351-255">En este caso, especificamos el adaptador con un índice de 0.</span><span class="sxs-lookup"><span data-stu-id="45351-255">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="45351-256">Se debe seleccionar el índice correcto en \_ las instancias de Win32 para otras interfaces.</span><span class="sxs-lookup"><span data-stu-id="45351-256">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="45351-257">Este script solo se aplica a los sistemas basados en NT. cambie las variables DirIP y Subnet siguientes a los valores que desee aplicar al adaptador.</span><span class="sxs-lookup"><span data-stu-id="45351-257">This script only applies to NT-based systems Change the ipaddr and subnet variables below to the values you wish to apply to the adapter.</span></span>

 


```
use strict;
use Win32::OLE;

my ($Adapter, @ipaddr, @subnet, $RetVal);  
eval { $Adapter = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2:Win32_NetworkAdapterConfiguration.Index=\"0\""); };

unless ($@) 
{
 push @ipaddr, "192.168.144.107";
 push @subnet, "255.255.255.0";

 $RetVal = $Adapter->EnableStatic(\@ipaddr, \@subnet);

 if ($RetVal == 0) 
 {
  print "\nDHCP disabled, using static IP address\n";
 }
 else 
 {
  print "\nDHCP disable failed\n";
 }
}
else
{
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="45351-258">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45351-258">Requirements</span></span>



| <span data-ttu-id="45351-259">Requisito</span><span class="sxs-lookup"><span data-stu-id="45351-259">Requirement</span></span> | <span data-ttu-id="45351-260">Value</span><span class="sxs-lookup"><span data-stu-id="45351-260">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45351-261">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45351-261">Minimum supported client</span></span><br/> | <span data-ttu-id="45351-262">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45351-262">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="45351-263">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45351-263">Minimum supported server</span></span><br/> | <span data-ttu-id="45351-264">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45351-264">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="45351-265">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="45351-265">Namespace</span></span><br/>                | <span data-ttu-id="45351-266">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="45351-266">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="45351-267">MOF</span><span class="sxs-lookup"><span data-stu-id="45351-267">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45351-268"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45351-268"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="45351-269">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="45351-269">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45351-270"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45351-270"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45351-271">Vea también</span><span class="sxs-lookup"><span data-stu-id="45351-271">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45351-272">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="45351-272">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="45351-273">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="45351-273">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="45351-274">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="45351-274">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="45351-275">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="45351-275">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="45351-276">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="45351-276">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

