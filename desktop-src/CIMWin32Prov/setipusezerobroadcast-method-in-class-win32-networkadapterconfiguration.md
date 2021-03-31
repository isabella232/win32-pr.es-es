---
description: El método estático de la clase WMI SetIPUseZeroBroadcast se usa para establecer el uso de la difusión IP cero.
ms.assetid: d20ac6fc-a5d5-4ad9-a2a5-65142b4c7d02
ms.tgt_platform: multiple
title: Método SetIPUseZeroBroadcast de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPUseZeroBroadcast
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 564f122242407f4d6f5dd28da9fd4d151ab6b47f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153219"
---
# <a name="setipusezerobroadcast-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="62a28-103">Método SetIPUseZeroBroadcast de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="62a28-103">SetIPUseZeroBroadcast method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="62a28-104">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetIPUseZeroBroadcast** se usa para establecer el uso de la difusión IP cero.</span><span class="sxs-lookup"><span data-stu-id="62a28-104">The **SetIPUseZeroBroadcast** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set IP zero broadcast usage.</span></span>

<span data-ttu-id="62a28-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="62a28-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="62a28-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="62a28-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="62a28-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62a28-107">Syntax</span></span>


```mof
uint32 SetIPUseZeroBroadcast(
  [in] boolean IPUseZeroBroadcast
);
```



## <a name="parameters"></a><span data-ttu-id="62a28-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62a28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62a28-109">*IPUseZeroBroadcast* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="62a28-109">*IPUseZeroBroadcast* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62a28-110">Si es **true**, se utiliza la difusión de cero IP.</span><span class="sxs-lookup"><span data-stu-id="62a28-110">If **true**, IP zero broadcast is used.</span></span> <span data-ttu-id="62a28-111">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="62a28-111">The default is **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62a28-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62a28-112">Return value</span></span>

<span data-ttu-id="62a28-113">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="62a28-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="62a28-114">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="62a28-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="62a28-115">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="62a28-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="62a28-116">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="62a28-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-117">0</span><span class="sxs-lookup"><span data-stu-id="62a28-117">0</span></span>

<span data-ttu-id="62a28-118">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="62a28-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-119">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="62a28-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-120">1</span><span class="sxs-lookup"><span data-stu-id="62a28-120">1</span></span>

<span data-ttu-id="62a28-121">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="62a28-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-122">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="62a28-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-123">64</span><span class="sxs-lookup"><span data-stu-id="62a28-123">64</span></span>

<span data-ttu-id="62a28-124">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="62a28-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-125">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="62a28-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-126">65</span><span class="sxs-lookup"><span data-stu-id="62a28-126">65</span></span>

<span data-ttu-id="62a28-127">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="62a28-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-128">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="62a28-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-129">66</span><span class="sxs-lookup"><span data-stu-id="62a28-129">66</span></span>

<span data-ttu-id="62a28-130">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="62a28-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-131">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="62a28-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-132">67</span><span class="sxs-lookup"><span data-stu-id="62a28-132">67</span></span>

<span data-ttu-id="62a28-133">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="62a28-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-134">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="62a28-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-135">68</span><span class="sxs-lookup"><span data-stu-id="62a28-135">68</span></span>

<span data-ttu-id="62a28-136">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="62a28-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-137">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="62a28-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-138">69</span><span class="sxs-lookup"><span data-stu-id="62a28-138">69</span></span>

<span data-ttu-id="62a28-139">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="62a28-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-140">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="62a28-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-141">70</span><span class="sxs-lookup"><span data-stu-id="62a28-141">70</span></span>

<span data-ttu-id="62a28-142">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="62a28-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-143">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="62a28-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-144">71</span><span class="sxs-lookup"><span data-stu-id="62a28-144">71</span></span>

<span data-ttu-id="62a28-145">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="62a28-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-146">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="62a28-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-147">72</span><span class="sxs-lookup"><span data-stu-id="62a28-147">72</span></span>

<span data-ttu-id="62a28-148">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="62a28-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-149">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="62a28-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-150">73</span><span class="sxs-lookup"><span data-stu-id="62a28-150">73</span></span>

<span data-ttu-id="62a28-151">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="62a28-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-152">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="62a28-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-153">74</span><span class="sxs-lookup"><span data-stu-id="62a28-153">74</span></span>

<span data-ttu-id="62a28-154">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="62a28-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-155">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="62a28-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-156">75</span><span class="sxs-lookup"><span data-stu-id="62a28-156">75</span></span>

<span data-ttu-id="62a28-157">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="62a28-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-158">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="62a28-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-159">76</span><span class="sxs-lookup"><span data-stu-id="62a28-159">76</span></span>

<span data-ttu-id="62a28-160">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="62a28-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-161">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="62a28-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-162">77</span><span class="sxs-lookup"><span data-stu-id="62a28-162">77</span></span>

<span data-ttu-id="62a28-163">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="62a28-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-164">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="62a28-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-165">78</span><span class="sxs-lookup"><span data-stu-id="62a28-165">78</span></span>

<span data-ttu-id="62a28-166">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="62a28-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-167">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="62a28-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-168">79</span><span class="sxs-lookup"><span data-stu-id="62a28-168">79</span></span>

<span data-ttu-id="62a28-169">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="62a28-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-170">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="62a28-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-171">80</span><span class="sxs-lookup"><span data-stu-id="62a28-171">80</span></span>

<span data-ttu-id="62a28-172">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="62a28-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-173">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="62a28-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-174">81</span><span class="sxs-lookup"><span data-stu-id="62a28-174">81</span></span>

<span data-ttu-id="62a28-175">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="62a28-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-176">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="62a28-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-177">82</span><span class="sxs-lookup"><span data-stu-id="62a28-177">82</span></span>

<span data-ttu-id="62a28-178">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="62a28-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-179">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="62a28-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-180">83</span><span class="sxs-lookup"><span data-stu-id="62a28-180">83</span></span>

<span data-ttu-id="62a28-181">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="62a28-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-182">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="62a28-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-183">84</span><span class="sxs-lookup"><span data-stu-id="62a28-183">84</span></span>

<span data-ttu-id="62a28-184">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="62a28-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-185">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="62a28-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-186">85</span><span class="sxs-lookup"><span data-stu-id="62a28-186">85</span></span>

<span data-ttu-id="62a28-187">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="62a28-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-188">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="62a28-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-189">86</span><span class="sxs-lookup"><span data-stu-id="62a28-189">86</span></span>

<span data-ttu-id="62a28-190">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="62a28-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-191">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="62a28-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-192">87</span><span class="sxs-lookup"><span data-stu-id="62a28-192">87</span></span>

<span data-ttu-id="62a28-193">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="62a28-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-194">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="62a28-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-195">88</span><span class="sxs-lookup"><span data-stu-id="62a28-195">88</span></span>

<span data-ttu-id="62a28-196">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="62a28-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-197">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="62a28-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-198">89</span><span class="sxs-lookup"><span data-stu-id="62a28-198">89</span></span>

<span data-ttu-id="62a28-199">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="62a28-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-200">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="62a28-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-201">90</span><span class="sxs-lookup"><span data-stu-id="62a28-201">90</span></span>

<span data-ttu-id="62a28-202">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="62a28-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-203">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="62a28-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-204">91</span><span class="sxs-lookup"><span data-stu-id="62a28-204">91</span></span>

<span data-ttu-id="62a28-205">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="62a28-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-206">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="62a28-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-207">92</span><span class="sxs-lookup"><span data-stu-id="62a28-207">92</span></span>

<span data-ttu-id="62a28-208">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="62a28-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-209">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="62a28-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-210">93</span><span class="sxs-lookup"><span data-stu-id="62a28-210">93</span></span>

<span data-ttu-id="62a28-211">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="62a28-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-212">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="62a28-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-213">94</span><span class="sxs-lookup"><span data-stu-id="62a28-213">94</span></span>

<span data-ttu-id="62a28-214">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="62a28-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-215">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="62a28-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-216">95</span><span class="sxs-lookup"><span data-stu-id="62a28-216">95</span></span>

<span data-ttu-id="62a28-217">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="62a28-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-218">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="62a28-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-219">96</span><span class="sxs-lookup"><span data-stu-id="62a28-219">96</span></span>

<span data-ttu-id="62a28-220">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="62a28-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-221">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="62a28-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-222">97</span><span class="sxs-lookup"><span data-stu-id="62a28-222">97</span></span>

<span data-ttu-id="62a28-223">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="62a28-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-224">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="62a28-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-225">98</span><span class="sxs-lookup"><span data-stu-id="62a28-225">98</span></span>

<span data-ttu-id="62a28-226">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="62a28-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-227">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="62a28-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-228">100</span><span class="sxs-lookup"><span data-stu-id="62a28-228">100</span></span>

<span data-ttu-id="62a28-229">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="62a28-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="62a28-230">**Otros**</span><span class="sxs-lookup"><span data-stu-id="62a28-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="62a28-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="62a28-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62a28-232">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62a28-232">Remarks</span></span>

<span data-ttu-id="62a28-233">Si el parámetro *IPUseZeroBroadcast* se establece en **true**, la dirección IP usará difusiones de cero (0.0.0.0) en lugar de una sola difusión (255.255.255.255).</span><span class="sxs-lookup"><span data-stu-id="62a28-233">If the *IPUseZeroBroadcast* parameter is set to **TRUE**, then IP will use zero-broadcasts (0.0.0.0) instead of one-broadcasts (255.255.255.255).</span></span> <span data-ttu-id="62a28-234">La mayoría de los sistemas usan difusiones monotales, pero los sistemas derivados de las implementaciones de BSD usan difusiones de cero.</span><span class="sxs-lookup"><span data-stu-id="62a28-234">Most systems use one-broadcasts, but systems derived from BSD implementations use zero-broadcasts.</span></span> <span data-ttu-id="62a28-235">Los sistemas que utilizan distintas difusiones no interoperarán en la misma red.</span><span class="sxs-lookup"><span data-stu-id="62a28-235">Systems that use different broadcasts will not interoperate on the same network.</span></span>

## <a name="examples"></a><span data-ttu-id="62a28-236">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="62a28-236">Examples</span></span>

<span data-ttu-id="62a28-237">En el ejemplo de VBScript [Modify Zero-Broadcast use para todos los adaptadores de red](https://Gallery.TechNet.Microsoft.Com/3d1ec74a-bf96-41cf-bb90-f98cd6494fb3) se configura un equipo para que use difusiones de cero (0.0.0.0) en lugar de una sola difusión (255.255.255.255).</span><span class="sxs-lookup"><span data-stu-id="62a28-237">The [Modify Zero-Broadcast Use for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/3d1ec74a-bf96-41cf-bb90-f98cd6494fb3) VBScript sample configures a computer to use zero-broadcasts (0.0.0.0) rather than one-broadcasts (255.255.255.255).</span></span>

## <a name="requirements"></a><span data-ttu-id="62a28-238">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62a28-238">Requirements</span></span>



| <span data-ttu-id="62a28-239">Requisito</span><span class="sxs-lookup"><span data-stu-id="62a28-239">Requirement</span></span> | <span data-ttu-id="62a28-240">Value</span><span class="sxs-lookup"><span data-stu-id="62a28-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62a28-241">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62a28-241">Minimum supported client</span></span><br/> | <span data-ttu-id="62a28-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62a28-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="62a28-243">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62a28-243">Minimum supported server</span></span><br/> | <span data-ttu-id="62a28-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62a28-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="62a28-245">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="62a28-245">Namespace</span></span><br/>                | <span data-ttu-id="62a28-246">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="62a28-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="62a28-247">MOF</span><span class="sxs-lookup"><span data-stu-id="62a28-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62a28-248"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62a28-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="62a28-249">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="62a28-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62a28-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62a28-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62a28-251">Vea también</span><span class="sxs-lookup"><span data-stu-id="62a28-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62a28-252">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="62a28-252">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="62a28-253">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="62a28-253">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="62a28-254">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="62a28-254">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="62a28-255">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="62a28-255">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="62a28-256">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="62a28-256">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

