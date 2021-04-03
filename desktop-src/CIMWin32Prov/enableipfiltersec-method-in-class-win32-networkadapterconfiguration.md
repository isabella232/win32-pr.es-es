---
description: El método estático de la clase WMI EnableIPFilterSec se usa para habilitar el protocolo de seguridad de Internet (IPsec) globalmente en todos los adaptadores de red enlazados a IP.
ms.assetid: 565acc18-61e7-473e-b2cc-41f0e8c29193
ms.tgt_platform: multiple
title: Método EnableIPFilterSec de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableIPFilterSec
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3429e2c2ba78e013da9195961b76ff84ffda9b68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907145"
---
# <a name="enableipfiltersec-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="d48fa-103">Método EnableIPFilterSec de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="d48fa-103">EnableIPFilterSec method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="d48fa-104">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableIPFilterSec** se usa para habilitar el protocolo de seguridad de Internet (IPSec) globalmente en todos los adaptadores de red enlazados a IP.</span><span class="sxs-lookup"><span data-stu-id="d48fa-104">The **EnableIPFilterSec** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable Internet Protocol security (IPsec) globally across all IP-bound network adapters.</span></span>

<span data-ttu-id="d48fa-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="d48fa-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d48fa-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d48fa-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d48fa-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d48fa-107">Syntax</span></span>


```mof
uint32 EnableIPFilterSec(
  [in] boolean IPFilterSecurityEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="d48fa-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d48fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d48fa-109">*IPFilterSecurityEnabled* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d48fa-109">*IPFilterSecurityEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-110">Si es **true**, IPSec está habilitado globalmente en todos los adaptadores de red enlazados a IP.</span><span class="sxs-lookup"><span data-stu-id="d48fa-110">If **true**, IPsec is enabled globally across all IP-bound network adapters.</span></span> <span data-ttu-id="d48fa-111">Si es **false**, se permite que el tráfico de puertos y protocolos fluya sin filtrar.</span><span class="sxs-lookup"><span data-stu-id="d48fa-111">If **false**, all port and protocol traffic is allowed to flow unfiltered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d48fa-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d48fa-112">Return value</span></span>

<span data-ttu-id="d48fa-113">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere un reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y cualquier otro número si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="d48fa-113">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="d48fa-114">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d48fa-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d48fa-115">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d48fa-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d48fa-116">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="d48fa-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-117">0</span><span class="sxs-lookup"><span data-stu-id="d48fa-117">0</span></span>

<span data-ttu-id="d48fa-118">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="d48fa-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-119">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="d48fa-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-120">1</span><span class="sxs-lookup"><span data-stu-id="d48fa-120">1</span></span>

<span data-ttu-id="d48fa-121">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="d48fa-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-122">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="d48fa-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-123">64</span><span class="sxs-lookup"><span data-stu-id="d48fa-123">64</span></span>

<span data-ttu-id="d48fa-124">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="d48fa-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-125">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="d48fa-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-126">65</span><span class="sxs-lookup"><span data-stu-id="d48fa-126">65</span></span>

<span data-ttu-id="d48fa-127">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="d48fa-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-128">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="d48fa-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-129">66</span><span class="sxs-lookup"><span data-stu-id="d48fa-129">66</span></span>

<span data-ttu-id="d48fa-130">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="d48fa-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-131">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="d48fa-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-132">67</span><span class="sxs-lookup"><span data-stu-id="d48fa-132">67</span></span>

<span data-ttu-id="d48fa-133">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="d48fa-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-134">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="d48fa-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-135">68</span><span class="sxs-lookup"><span data-stu-id="d48fa-135">68</span></span>

<span data-ttu-id="d48fa-136">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="d48fa-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-137">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="d48fa-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-138">69</span><span class="sxs-lookup"><span data-stu-id="d48fa-138">69</span></span>

<span data-ttu-id="d48fa-139">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="d48fa-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-140">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="d48fa-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-141">70</span><span class="sxs-lookup"><span data-stu-id="d48fa-141">70</span></span>

<span data-ttu-id="d48fa-142">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="d48fa-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-143">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="d48fa-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-144">71</span><span class="sxs-lookup"><span data-stu-id="d48fa-144">71</span></span>

<span data-ttu-id="d48fa-145">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="d48fa-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-146">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="d48fa-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-147">72</span><span class="sxs-lookup"><span data-stu-id="d48fa-147">72</span></span>

<span data-ttu-id="d48fa-148">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="d48fa-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-149">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="d48fa-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-150">73</span><span class="sxs-lookup"><span data-stu-id="d48fa-150">73</span></span>

<span data-ttu-id="d48fa-151">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="d48fa-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-152">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="d48fa-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-153">74</span><span class="sxs-lookup"><span data-stu-id="d48fa-153">74</span></span>

<span data-ttu-id="d48fa-154">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="d48fa-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-155">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="d48fa-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-156">75</span><span class="sxs-lookup"><span data-stu-id="d48fa-156">75</span></span>

<span data-ttu-id="d48fa-157">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="d48fa-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-158">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="d48fa-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-159">76</span><span class="sxs-lookup"><span data-stu-id="d48fa-159">76</span></span>

<span data-ttu-id="d48fa-160">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="d48fa-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-161">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="d48fa-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-162">77</span><span class="sxs-lookup"><span data-stu-id="d48fa-162">77</span></span>

<span data-ttu-id="d48fa-163">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="d48fa-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-164">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="d48fa-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-165">78</span><span class="sxs-lookup"><span data-stu-id="d48fa-165">78</span></span>

<span data-ttu-id="d48fa-166">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="d48fa-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-167">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="d48fa-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-168">79</span><span class="sxs-lookup"><span data-stu-id="d48fa-168">79</span></span>

<span data-ttu-id="d48fa-169">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="d48fa-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-170">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="d48fa-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-171">80</span><span class="sxs-lookup"><span data-stu-id="d48fa-171">80</span></span>

<span data-ttu-id="d48fa-172">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d48fa-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-173">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="d48fa-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-174">81</span><span class="sxs-lookup"><span data-stu-id="d48fa-174">81</span></span>

<span data-ttu-id="d48fa-175">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="d48fa-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-176">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="d48fa-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-177">82</span><span class="sxs-lookup"><span data-stu-id="d48fa-177">82</span></span>

<span data-ttu-id="d48fa-178">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="d48fa-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-179">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="d48fa-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-180">83</span><span class="sxs-lookup"><span data-stu-id="d48fa-180">83</span></span>

<span data-ttu-id="d48fa-181">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="d48fa-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-182">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="d48fa-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-183">84</span><span class="sxs-lookup"><span data-stu-id="d48fa-183">84</span></span>

<span data-ttu-id="d48fa-184">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="d48fa-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-185">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="d48fa-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-186">85</span><span class="sxs-lookup"><span data-stu-id="d48fa-186">85</span></span>

<span data-ttu-id="d48fa-187">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="d48fa-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-188">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="d48fa-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-189">86</span><span class="sxs-lookup"><span data-stu-id="d48fa-189">86</span></span>

<span data-ttu-id="d48fa-190">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="d48fa-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-191">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="d48fa-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-192">87</span><span class="sxs-lookup"><span data-stu-id="d48fa-192">87</span></span>

<span data-ttu-id="d48fa-193">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="d48fa-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-194">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="d48fa-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-195">88</span><span class="sxs-lookup"><span data-stu-id="d48fa-195">88</span></span>

<span data-ttu-id="d48fa-196">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="d48fa-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-197">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="d48fa-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-198">89</span><span class="sxs-lookup"><span data-stu-id="d48fa-198">89</span></span>

<span data-ttu-id="d48fa-199">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="d48fa-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-200">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="d48fa-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-201">90</span><span class="sxs-lookup"><span data-stu-id="d48fa-201">90</span></span>

<span data-ttu-id="d48fa-202">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="d48fa-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-203">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="d48fa-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-204">91</span><span class="sxs-lookup"><span data-stu-id="d48fa-204">91</span></span>

<span data-ttu-id="d48fa-205">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="d48fa-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-206">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="d48fa-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-207">92</span><span class="sxs-lookup"><span data-stu-id="d48fa-207">92</span></span>

<span data-ttu-id="d48fa-208">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="d48fa-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-209">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="d48fa-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-210">93</span><span class="sxs-lookup"><span data-stu-id="d48fa-210">93</span></span>

<span data-ttu-id="d48fa-211">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="d48fa-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-212">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="d48fa-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-213">94</span><span class="sxs-lookup"><span data-stu-id="d48fa-213">94</span></span>

<span data-ttu-id="d48fa-214">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="d48fa-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-215">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="d48fa-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-216">95</span><span class="sxs-lookup"><span data-stu-id="d48fa-216">95</span></span>

<span data-ttu-id="d48fa-217">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="d48fa-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-218">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="d48fa-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-219">96</span><span class="sxs-lookup"><span data-stu-id="d48fa-219">96</span></span>

<span data-ttu-id="d48fa-220">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="d48fa-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-221">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="d48fa-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-222">97</span><span class="sxs-lookup"><span data-stu-id="d48fa-222">97</span></span>

<span data-ttu-id="d48fa-223">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="d48fa-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-224">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="d48fa-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-225">98</span><span class="sxs-lookup"><span data-stu-id="d48fa-225">98</span></span>

<span data-ttu-id="d48fa-226">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="d48fa-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-227">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="d48fa-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-228">100</span><span class="sxs-lookup"><span data-stu-id="d48fa-228">100</span></span>

<span data-ttu-id="d48fa-229">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="d48fa-229">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d48fa-230">**Otros**</span><span class="sxs-lookup"><span data-stu-id="d48fa-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="d48fa-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="d48fa-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d48fa-232">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d48fa-232">Remarks</span></span>

<span data-ttu-id="d48fa-233">Con la seguridad habilitada, las características de seguridad operativa de cualquier adaptador de red se pueden controlar mediante el método [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) específico del adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="d48fa-233">With security enabled, the operational security characteristics for any one network adapter can be controlled by using the network adapter-specific [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="d48fa-234">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d48fa-234">Examples</span></span>

<span data-ttu-id="d48fa-235">El siguiente código, tomado del ejemplo de [habilitación de la seguridad de IPFilter en todos los adaptadores de red](https://Gallery.TechNet.Microsoft.Com/f8e56021-5a54-4554-b7b6-d76cc40d8d1d) de la galería de TechNet, habilita la seguridad de filtros IP para todos los adaptadores de red instalados en un equipo.</span><span class="sxs-lookup"><span data-stu-id="d48fa-235">The following code, taken from the [Enable IPFilter Security on All Network Adapters](https://Gallery.TechNet.Microsoft.Com/f8e56021-5a54-4554-b7b6-d76cc40d8d1d) sample on TechNet Gallery, enables IP filter security for all the network adapters installed in a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objNetworkSettings = objWMIService.Get("Win32_NetworkAdapterConfiguration") 
objNetworkSettings.EnableIPFilterSec(True)
```



## <a name="requirements"></a><span data-ttu-id="d48fa-236">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d48fa-236">Requirements</span></span>



| <span data-ttu-id="d48fa-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="d48fa-237">Requirement</span></span> | <span data-ttu-id="d48fa-238">Value</span><span class="sxs-lookup"><span data-stu-id="d48fa-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d48fa-239">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d48fa-239">Minimum supported client</span></span><br/> | <span data-ttu-id="d48fa-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d48fa-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d48fa-241">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d48fa-241">Minimum supported server</span></span><br/> | <span data-ttu-id="d48fa-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d48fa-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d48fa-243">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d48fa-243">Namespace</span></span><br/>                | <span data-ttu-id="d48fa-244">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d48fa-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d48fa-245">MOF</span><span class="sxs-lookup"><span data-stu-id="d48fa-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d48fa-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d48fa-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d48fa-247">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d48fa-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d48fa-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d48fa-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d48fa-249">Vea también</span><span class="sxs-lookup"><span data-stu-id="d48fa-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d48fa-250">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="d48fa-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d48fa-251">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="d48fa-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="d48fa-252">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="d48fa-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="d48fa-253">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="d48fa-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="d48fa-254">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="d48fa-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

