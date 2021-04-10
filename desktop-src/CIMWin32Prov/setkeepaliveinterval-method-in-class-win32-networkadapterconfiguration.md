---
description: El método estático de la clase WMI SetKeepAliveInterval se usa para establecer el intervalo que separa las retransmisiones Keep Alive hasta que se reciba una respuesta.
ms.assetid: 83415000-124a-44a7-93cc-92ce9df143aa
ms.tgt_platform: multiple
title: Método SetKeepAliveInterval de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetKeepAliveInterval
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2ce6a1491fd9e414f503d0165216794c67db0e97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153217"
---
# <a name="setkeepaliveinterval-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="05744-103">Método SetKeepAliveInterval de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="05744-103">SetKeepAliveInterval method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="05744-104">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetKeepAliveInterval** se usa para establecer el intervalo que separa las retransmisiones Keep Alive hasta que se reciba una respuesta.</span><span class="sxs-lookup"><span data-stu-id="05744-104">The **SetKeepAliveInterval** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the interval separating Keep Alive Retransmissions until a response is received.</span></span>

<span data-ttu-id="05744-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="05744-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="05744-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="05744-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="05744-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05744-107">Syntax</span></span>


```mof
uint32 SetKeepAliveInterval(
  [in] uint32 KeepAliveInterval
);
```



## <a name="parameters"></a><span data-ttu-id="05744-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05744-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05744-109">*KeepAliveInterval* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="05744-109">*KeepAliveInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05744-110">Valor, en milisegundos, para el intervalo que separa las retransmisiones Keep Alive hasta que se reciba una respuesta.</span><span class="sxs-lookup"><span data-stu-id="05744-110">Value, in milliseconds, for the interval separating Keep Alive Retransmissions until a response is received.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05744-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05744-111">Return value</span></span>

<span data-ttu-id="05744-112">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="05744-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="05744-113">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="05744-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="05744-114">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="05744-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="05744-115">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="05744-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="05744-116">0</span><span class="sxs-lookup"><span data-stu-id="05744-116">0</span></span>

<span data-ttu-id="05744-117">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="05744-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="05744-118">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="05744-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="05744-119">1</span><span class="sxs-lookup"><span data-stu-id="05744-119">1</span></span>

<span data-ttu-id="05744-120">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="05744-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="05744-121">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="05744-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="05744-122">64</span><span class="sxs-lookup"><span data-stu-id="05744-122">64</span></span>

<span data-ttu-id="05744-123">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="05744-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="05744-124">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="05744-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="05744-125">65</span><span class="sxs-lookup"><span data-stu-id="05744-125">65</span></span>

<span data-ttu-id="05744-126">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="05744-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="05744-127">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="05744-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="05744-128">66</span><span class="sxs-lookup"><span data-stu-id="05744-128">66</span></span>

<span data-ttu-id="05744-129">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="05744-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="05744-130">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="05744-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="05744-131">67</span><span class="sxs-lookup"><span data-stu-id="05744-131">67</span></span>

<span data-ttu-id="05744-132">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="05744-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="05744-133">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="05744-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="05744-134">68</span><span class="sxs-lookup"><span data-stu-id="05744-134">68</span></span>

<span data-ttu-id="05744-135">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="05744-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="05744-136">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="05744-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="05744-137">69</span><span class="sxs-lookup"><span data-stu-id="05744-137">69</span></span>

<span data-ttu-id="05744-138">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="05744-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="05744-139">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="05744-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="05744-140">70</span><span class="sxs-lookup"><span data-stu-id="05744-140">70</span></span>

<span data-ttu-id="05744-141">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="05744-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="05744-142">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="05744-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="05744-143">71</span><span class="sxs-lookup"><span data-stu-id="05744-143">71</span></span>

<span data-ttu-id="05744-144">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="05744-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="05744-145">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="05744-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="05744-146">72</span><span class="sxs-lookup"><span data-stu-id="05744-146">72</span></span>

<span data-ttu-id="05744-147">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="05744-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="05744-148">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="05744-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="05744-149">73</span><span class="sxs-lookup"><span data-stu-id="05744-149">73</span></span>

<span data-ttu-id="05744-150">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="05744-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="05744-151">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="05744-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="05744-152">74</span><span class="sxs-lookup"><span data-stu-id="05744-152">74</span></span>

<span data-ttu-id="05744-153">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="05744-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="05744-154">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="05744-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="05744-155">75</span><span class="sxs-lookup"><span data-stu-id="05744-155">75</span></span>

<span data-ttu-id="05744-156">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="05744-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="05744-157">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="05744-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="05744-158">76</span><span class="sxs-lookup"><span data-stu-id="05744-158">76</span></span>

<span data-ttu-id="05744-159">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="05744-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="05744-160">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="05744-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="05744-161">77</span><span class="sxs-lookup"><span data-stu-id="05744-161">77</span></span>

<span data-ttu-id="05744-162">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="05744-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="05744-163">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="05744-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="05744-164">78</span><span class="sxs-lookup"><span data-stu-id="05744-164">78</span></span>

<span data-ttu-id="05744-165">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="05744-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="05744-166">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="05744-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="05744-167">79</span><span class="sxs-lookup"><span data-stu-id="05744-167">79</span></span>

<span data-ttu-id="05744-168">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="05744-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="05744-169">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="05744-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="05744-170">80</span><span class="sxs-lookup"><span data-stu-id="05744-170">80</span></span>

<span data-ttu-id="05744-171">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="05744-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="05744-172">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="05744-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="05744-173">81</span><span class="sxs-lookup"><span data-stu-id="05744-173">81</span></span>

<span data-ttu-id="05744-174">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="05744-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="05744-175">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="05744-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="05744-176">82</span><span class="sxs-lookup"><span data-stu-id="05744-176">82</span></span>

<span data-ttu-id="05744-177">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="05744-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="05744-178">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="05744-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="05744-179">83</span><span class="sxs-lookup"><span data-stu-id="05744-179">83</span></span>

<span data-ttu-id="05744-180">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="05744-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="05744-181">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="05744-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="05744-182">84</span><span class="sxs-lookup"><span data-stu-id="05744-182">84</span></span>

<span data-ttu-id="05744-183">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="05744-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="05744-184">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="05744-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="05744-185">85</span><span class="sxs-lookup"><span data-stu-id="05744-185">85</span></span>

<span data-ttu-id="05744-186">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="05744-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="05744-187">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="05744-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="05744-188">86</span><span class="sxs-lookup"><span data-stu-id="05744-188">86</span></span>

<span data-ttu-id="05744-189">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="05744-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="05744-190">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="05744-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="05744-191">87</span><span class="sxs-lookup"><span data-stu-id="05744-191">87</span></span>

<span data-ttu-id="05744-192">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="05744-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="05744-193">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="05744-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="05744-194">88</span><span class="sxs-lookup"><span data-stu-id="05744-194">88</span></span>

<span data-ttu-id="05744-195">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="05744-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="05744-196">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="05744-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="05744-197">89</span><span class="sxs-lookup"><span data-stu-id="05744-197">89</span></span>

<span data-ttu-id="05744-198">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="05744-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="05744-199">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="05744-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="05744-200">90</span><span class="sxs-lookup"><span data-stu-id="05744-200">90</span></span>

<span data-ttu-id="05744-201">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="05744-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="05744-202">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="05744-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="05744-203">91</span><span class="sxs-lookup"><span data-stu-id="05744-203">91</span></span>

<span data-ttu-id="05744-204">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="05744-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="05744-205">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="05744-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="05744-206">92</span><span class="sxs-lookup"><span data-stu-id="05744-206">92</span></span>

<span data-ttu-id="05744-207">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="05744-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="05744-208">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="05744-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="05744-209">93</span><span class="sxs-lookup"><span data-stu-id="05744-209">93</span></span>

<span data-ttu-id="05744-210">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="05744-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="05744-211">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="05744-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="05744-212">94</span><span class="sxs-lookup"><span data-stu-id="05744-212">94</span></span>

<span data-ttu-id="05744-213">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="05744-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="05744-214">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="05744-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="05744-215">95</span><span class="sxs-lookup"><span data-stu-id="05744-215">95</span></span>

<span data-ttu-id="05744-216">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="05744-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="05744-217">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="05744-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="05744-218">96</span><span class="sxs-lookup"><span data-stu-id="05744-218">96</span></span>

<span data-ttu-id="05744-219">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="05744-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="05744-220">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="05744-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="05744-221">97</span><span class="sxs-lookup"><span data-stu-id="05744-221">97</span></span>

<span data-ttu-id="05744-222">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="05744-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="05744-223">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="05744-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="05744-224">98</span><span class="sxs-lookup"><span data-stu-id="05744-224">98</span></span>

<span data-ttu-id="05744-225">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="05744-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="05744-226">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="05744-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="05744-227">100</span><span class="sxs-lookup"><span data-stu-id="05744-227">100</span></span>

<span data-ttu-id="05744-228">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="05744-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="05744-229">**Otros**</span><span class="sxs-lookup"><span data-stu-id="05744-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="05744-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="05744-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05744-231">Observaciones</span><span class="sxs-lookup"><span data-stu-id="05744-231">Remarks</span></span>

<span data-ttu-id="05744-232">Después de recibir una respuesta, el retraso hasta la siguiente transmisión de mantenimiento de conexión vuelve a controlarse mediante el valor de la propiedad [**KeepAliveTime**](win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="05744-232">After a response is received, the delay until the next Keep Alive Transmission is again controlled by the value of the [**KeepAliveTime**](win32-networkadapterconfiguration.md) property.</span></span> <span data-ttu-id="05744-233">La conexión se termina después de que el número de retransmisiones especificado por la propiedad **TcpMaxDataRetransmissions** no se ha respondido.</span><span class="sxs-lookup"><span data-stu-id="05744-233">The connection is terminated after the number of retransmissions specified by the **TcpMaxDataRetransmissions** property have gone unanswered</span></span>

## <a name="examples"></a><span data-ttu-id="05744-234">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="05744-234">Examples</span></span>

<span data-ttu-id="05744-235">En el ejemplo de VBScript [modificar el intervalo de mantenimiento de conexión para todos los adaptadores de red](https://Gallery.TechNet.Microsoft.Com/f6d4a0e7-5b59-42e3-888d-82a028e2bf35) se configura el intervalo de mantenimiento de conexión para todos los adaptadores de red de un equipo en 300 milisegundos (5 minutos).</span><span class="sxs-lookup"><span data-stu-id="05744-235">The [Modify the Keep Alive Interval for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/f6d4a0e7-5b59-42e3-888d-82a028e2bf35) VBScript sample configures the keep alive interval for all network adapters on a computer to 300,00 milliseconds (5 minutes).</span></span>

## <a name="requirements"></a><span data-ttu-id="05744-236">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05744-236">Requirements</span></span>



| <span data-ttu-id="05744-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="05744-237">Requirement</span></span> | <span data-ttu-id="05744-238">Value</span><span class="sxs-lookup"><span data-stu-id="05744-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05744-239">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05744-239">Minimum supported client</span></span><br/> | <span data-ttu-id="05744-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05744-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="05744-241">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05744-241">Minimum supported server</span></span><br/> | <span data-ttu-id="05744-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05744-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="05744-243">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="05744-243">Namespace</span></span><br/>                | <span data-ttu-id="05744-244">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="05744-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="05744-245">MOF</span><span class="sxs-lookup"><span data-stu-id="05744-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05744-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="05744-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="05744-247">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="05744-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05744-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05744-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05744-249">Vea también</span><span class="sxs-lookup"><span data-stu-id="05744-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05744-250">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="05744-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="05744-251">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="05744-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="05744-252">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="05744-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="05744-253">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="05744-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="05744-254">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="05744-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

