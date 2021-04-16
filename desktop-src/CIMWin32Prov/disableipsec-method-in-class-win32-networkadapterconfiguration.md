---
description: El método de clase WMI DisableIPSec se usa para deshabilitar el protocolo de seguridad de Internet (IPsec) en este adaptador de red habilitado para TCP/IP.
ms.assetid: 6fff2721-1ee2-42b4-bbf9-fd36b97318e3
ms.tgt_platform: multiple
title: Método DisableIPSec de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.DisableIPSec
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b2a17bbfa0f10c08edb581b4a4bf51173facfea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659490"
---
# <a name="disableipsec-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="fea9a-103">Método DisableIPSec de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="fea9a-103">DisableIPSec method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="fea9a-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **DisableIPSec** se usa para deshabilitar el protocolo de seguridad de Internet (IPSec) en este adaptador de red habilitado para TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="fea9a-104">The **DisableIPSec** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method is used to disable Internet Protocol security (IPsec) on this TCP/IP-enabled network adapter.</span></span>

<span data-ttu-id="fea9a-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="fea9a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fea9a-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fea9a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fea9a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fea9a-107">Syntax</span></span>


```mof
uint32 DisableIPSec();
```



## <a name="parameters"></a><span data-ttu-id="fea9a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fea9a-108">Parameters</span></span>

<span data-ttu-id="fea9a-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fea9a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fea9a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fea9a-110">Return value</span></span>

<span data-ttu-id="fea9a-111">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere un reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y cualquier otro número si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="fea9a-111">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="fea9a-112">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="fea9a-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="fea9a-113">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="fea9a-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="fea9a-114">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="fea9a-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-115">0</span><span class="sxs-lookup"><span data-stu-id="fea9a-115">0</span></span>

<span data-ttu-id="fea9a-116">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="fea9a-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-117">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="fea9a-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-118">1</span><span class="sxs-lookup"><span data-stu-id="fea9a-118">1</span></span>

<span data-ttu-id="fea9a-119">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="fea9a-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-120">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="fea9a-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-121">64</span><span class="sxs-lookup"><span data-stu-id="fea9a-121">64</span></span>

<span data-ttu-id="fea9a-122">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="fea9a-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-123">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="fea9a-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-124">65</span><span class="sxs-lookup"><span data-stu-id="fea9a-124">65</span></span>

<span data-ttu-id="fea9a-125">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="fea9a-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-126">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="fea9a-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-127">66</span><span class="sxs-lookup"><span data-stu-id="fea9a-127">66</span></span>

<span data-ttu-id="fea9a-128">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="fea9a-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-129">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="fea9a-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-130">67</span><span class="sxs-lookup"><span data-stu-id="fea9a-130">67</span></span>

<span data-ttu-id="fea9a-131">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="fea9a-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-132">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="fea9a-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-133">68</span><span class="sxs-lookup"><span data-stu-id="fea9a-133">68</span></span>

<span data-ttu-id="fea9a-134">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="fea9a-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-135">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="fea9a-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-136">69</span><span class="sxs-lookup"><span data-stu-id="fea9a-136">69</span></span>

<span data-ttu-id="fea9a-137">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="fea9a-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-138">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="fea9a-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-139">70</span><span class="sxs-lookup"><span data-stu-id="fea9a-139">70</span></span>

<span data-ttu-id="fea9a-140">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="fea9a-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-141">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="fea9a-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-142">71</span><span class="sxs-lookup"><span data-stu-id="fea9a-142">71</span></span>

<span data-ttu-id="fea9a-143">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="fea9a-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-144">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="fea9a-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-145">72</span><span class="sxs-lookup"><span data-stu-id="fea9a-145">72</span></span>

<span data-ttu-id="fea9a-146">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="fea9a-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-147">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="fea9a-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-148">73</span><span class="sxs-lookup"><span data-stu-id="fea9a-148">73</span></span>

<span data-ttu-id="fea9a-149">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="fea9a-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-150">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="fea9a-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-151">74</span><span class="sxs-lookup"><span data-stu-id="fea9a-151">74</span></span>

<span data-ttu-id="fea9a-152">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="fea9a-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-153">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="fea9a-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-154">75</span><span class="sxs-lookup"><span data-stu-id="fea9a-154">75</span></span>

<span data-ttu-id="fea9a-155">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="fea9a-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-156">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="fea9a-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-157">76</span><span class="sxs-lookup"><span data-stu-id="fea9a-157">76</span></span>

<span data-ttu-id="fea9a-158">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="fea9a-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-159">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="fea9a-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-160">77</span><span class="sxs-lookup"><span data-stu-id="fea9a-160">77</span></span>

<span data-ttu-id="fea9a-161">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="fea9a-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-162">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="fea9a-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-163">78</span><span class="sxs-lookup"><span data-stu-id="fea9a-163">78</span></span>

<span data-ttu-id="fea9a-164">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="fea9a-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-165">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="fea9a-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-166">79</span><span class="sxs-lookup"><span data-stu-id="fea9a-166">79</span></span>

<span data-ttu-id="fea9a-167">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="fea9a-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-168">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="fea9a-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-169">80</span><span class="sxs-lookup"><span data-stu-id="fea9a-169">80</span></span>

<span data-ttu-id="fea9a-170">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="fea9a-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-171">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="fea9a-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-172">81</span><span class="sxs-lookup"><span data-stu-id="fea9a-172">81</span></span>

<span data-ttu-id="fea9a-173">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="fea9a-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-174">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="fea9a-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-175">82</span><span class="sxs-lookup"><span data-stu-id="fea9a-175">82</span></span>

<span data-ttu-id="fea9a-176">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="fea9a-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-177">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="fea9a-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-178">83</span><span class="sxs-lookup"><span data-stu-id="fea9a-178">83</span></span>

<span data-ttu-id="fea9a-179">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="fea9a-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-180">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="fea9a-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-181">84</span><span class="sxs-lookup"><span data-stu-id="fea9a-181">84</span></span>

<span data-ttu-id="fea9a-182">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="fea9a-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-183">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="fea9a-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-184">85</span><span class="sxs-lookup"><span data-stu-id="fea9a-184">85</span></span>

<span data-ttu-id="fea9a-185">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="fea9a-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-186">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="fea9a-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-187">86</span><span class="sxs-lookup"><span data-stu-id="fea9a-187">86</span></span>

<span data-ttu-id="fea9a-188">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="fea9a-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-189">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="fea9a-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-190">87</span><span class="sxs-lookup"><span data-stu-id="fea9a-190">87</span></span>

<span data-ttu-id="fea9a-191">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="fea9a-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-192">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="fea9a-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-193">88</span><span class="sxs-lookup"><span data-stu-id="fea9a-193">88</span></span>

<span data-ttu-id="fea9a-194">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="fea9a-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-195">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="fea9a-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-196">89</span><span class="sxs-lookup"><span data-stu-id="fea9a-196">89</span></span>

<span data-ttu-id="fea9a-197">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="fea9a-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-198">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="fea9a-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-199">90</span><span class="sxs-lookup"><span data-stu-id="fea9a-199">90</span></span>

<span data-ttu-id="fea9a-200">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="fea9a-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-201">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="fea9a-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-202">91</span><span class="sxs-lookup"><span data-stu-id="fea9a-202">91</span></span>

<span data-ttu-id="fea9a-203">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="fea9a-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-204">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="fea9a-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-205">92</span><span class="sxs-lookup"><span data-stu-id="fea9a-205">92</span></span>

<span data-ttu-id="fea9a-206">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="fea9a-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-207">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="fea9a-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-208">93</span><span class="sxs-lookup"><span data-stu-id="fea9a-208">93</span></span>

<span data-ttu-id="fea9a-209">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="fea9a-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-210">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="fea9a-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-211">94</span><span class="sxs-lookup"><span data-stu-id="fea9a-211">94</span></span>

<span data-ttu-id="fea9a-212">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="fea9a-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-213">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="fea9a-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-214">95</span><span class="sxs-lookup"><span data-stu-id="fea9a-214">95</span></span>

<span data-ttu-id="fea9a-215">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="fea9a-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-216">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="fea9a-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-217">96</span><span class="sxs-lookup"><span data-stu-id="fea9a-217">96</span></span>

<span data-ttu-id="fea9a-218">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="fea9a-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-219">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="fea9a-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-220">97</span><span class="sxs-lookup"><span data-stu-id="fea9a-220">97</span></span>

<span data-ttu-id="fea9a-221">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="fea9a-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-222">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="fea9a-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-223">98</span><span class="sxs-lookup"><span data-stu-id="fea9a-223">98</span></span>

<span data-ttu-id="fea9a-224">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="fea9a-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-225">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="fea9a-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-226">100</span><span class="sxs-lookup"><span data-stu-id="fea9a-226">100</span></span>

<span data-ttu-id="fea9a-227">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="fea9a-227">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="fea9a-228">**Otros**</span><span class="sxs-lookup"><span data-stu-id="fea9a-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="fea9a-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="fea9a-229">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="fea9a-230">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fea9a-230">Examples</span></span>

<span data-ttu-id="fea9a-231">El siguiente ejemplo de VBScript deshabilita la seguridad IP en un equipo.</span><span class="sxs-lookup"><span data-stu-id="fea9a-231">The following VBScript sample disables the IP Security on a computer.</span></span> <span data-ttu-id="fea9a-232">Tenga en cuenta que la llamada real a DisableIPSec se marca como comentario, por motivos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fea9a-232">Note that the actual call to DisableIPSec is commented out, for safety purposes.</span></span>


```VB
strServer = "."

Set objWMI = GetObject("winmgmts:\\" & strServer & "\root\cimv2")

strWQL = "select * from Win32_NetworkAdapterConfiguration"
Set objInstances = objWMI.ExecQuery(strWQL,,48)

For Each objInstance in objInstances

 ' Uncomment next line to disable security
 ' intResult = objInstance.DisableIPSec

Next
```



## <a name="requirements"></a><span data-ttu-id="fea9a-233">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fea9a-233">Requirements</span></span>



| <span data-ttu-id="fea9a-234">Requisito</span><span class="sxs-lookup"><span data-stu-id="fea9a-234">Requirement</span></span> | <span data-ttu-id="fea9a-235">Value</span><span class="sxs-lookup"><span data-stu-id="fea9a-235">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fea9a-236">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fea9a-236">Minimum supported client</span></span><br/> | <span data-ttu-id="fea9a-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fea9a-237">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fea9a-238">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fea9a-238">Minimum supported server</span></span><br/> | <span data-ttu-id="fea9a-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fea9a-239">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fea9a-240">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fea9a-240">Namespace</span></span><br/>                | <span data-ttu-id="fea9a-241">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="fea9a-241">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fea9a-242">MOF</span><span class="sxs-lookup"><span data-stu-id="fea9a-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fea9a-243"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fea9a-243"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fea9a-244">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fea9a-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fea9a-245"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fea9a-245"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fea9a-246">Vea también</span><span class="sxs-lookup"><span data-stu-id="fea9a-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fea9a-247">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="fea9a-247">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="fea9a-248">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="fea9a-248">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="fea9a-249">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="fea9a-249">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="fea9a-250">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="fea9a-250">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="fea9a-251">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="fea9a-251">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

