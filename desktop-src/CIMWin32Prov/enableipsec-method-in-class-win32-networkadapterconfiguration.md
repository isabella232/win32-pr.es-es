---
description: EnableIPSec&\# 8194; El método de clase WMI habilita el protocolo de seguridad de Internet (IPsec) en un adaptador de red habilitado para TCP/IP.
ms.assetid: 0a45d864-606d-4adb-9b51-62d46a0d68b1
ms.tgt_platform: multiple
title: Método EnableIPSec de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableIPSec
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6988d68f9939752e3c8c2c9ace063b895a2d3720
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907144"
---
# <a name="enableipsec-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="dd196-103">Método EnableIPSec de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="dd196-103">EnableIPSec method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="dd196-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableIPSec** habilita el protocolo de seguridad de Internet (IPSec) en un adaptador de red habilitado para TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="dd196-104">The **EnableIPSec** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method enables Internet Protocol security (IPsec) on a TCP/IP-enabled network adapter.</span></span>

<span data-ttu-id="dd196-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="dd196-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="dd196-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="dd196-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="dd196-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd196-107">Syntax</span></span>


```mof
uint32 EnableIPSec(
  [in] string IPSecPermitTCPPorts[],
  [in] string IPSecPermitUDPPorts[],
  [in] string IPSecPermitIPProtocols[]
);
```



## <a name="parameters"></a><span data-ttu-id="dd196-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd196-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd196-109">*IPSecPermitTCPPorts* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dd196-109">*IPSecPermitTCPPorts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd196-110">Lista de puertos a los que se va a conceder el permiso de acceso para TCP.</span><span class="sxs-lookup"><span data-stu-id="dd196-110">List of ports to be granted access permission for TCP.</span></span> <span data-ttu-id="dd196-111">Un valor numérico de 0 (cero) indica que se concede permiso de acceso para todos los puertos.</span><span class="sxs-lookup"><span data-stu-id="dd196-111">A numeric value of 0 (zero) indicates access permission is granted for all ports.</span></span> <span data-ttu-id="dd196-112">Una matriz vacía indica que no se va a conceder permiso de acceso a ningún puerto.</span><span class="sxs-lookup"><span data-stu-id="dd196-112">An empty array indicates that no ports are to be granted access permission.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-113">*IPSecPermitUDPPorts* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dd196-113">*IPSecPermitUDPPorts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd196-114">Lista de puertos a los que se va a conceder el permiso de acceso para UDP.</span><span class="sxs-lookup"><span data-stu-id="dd196-114">List of ports to be granted access permission for UDP.</span></span> <span data-ttu-id="dd196-115">Un valor numérico de 0 (cero) indica que se concede permiso de acceso para todos los puertos.</span><span class="sxs-lookup"><span data-stu-id="dd196-115">A numeric value of 0 (zero) indicates access permission is granted for all ports.</span></span> <span data-ttu-id="dd196-116">Una matriz vacía indica que no se va a conceder permiso de acceso a ningún puerto.</span><span class="sxs-lookup"><span data-stu-id="dd196-116">An empty array indicates that no ports are to be granted access permission.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-117">*IPSecPermitIPProtocols* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dd196-117">*IPSecPermitIPProtocols* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd196-118">Lista de protocolos que se pueden ejecutar a través de la dirección IP.</span><span class="sxs-lookup"><span data-stu-id="dd196-118">List of protocols permitted to run over the IP.</span></span> <span data-ttu-id="dd196-119">Un valor numérico de 0 (cero) indica que se concede permiso de acceso para todos los protocolos.</span><span class="sxs-lookup"><span data-stu-id="dd196-119">A numeric value of 0 (zero) indicates access permission is granted for all protocols.</span></span> <span data-ttu-id="dd196-120">Una matriz vacía indica que no se concede permiso de acceso a ningún protocolo.</span><span class="sxs-lookup"><span data-stu-id="dd196-120">An empty array indicates that no protocols are granted access permission.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd196-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd196-121">Return value</span></span>

<span data-ttu-id="dd196-122">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere un reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y cualquier otro número si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="dd196-122">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="dd196-123">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="dd196-123">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="dd196-124">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="dd196-124">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="dd196-125">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="dd196-125">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-126">0</span><span class="sxs-lookup"><span data-stu-id="dd196-126">0</span></span>

<span data-ttu-id="dd196-127">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="dd196-127">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-128">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="dd196-128">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-129">1</span><span class="sxs-lookup"><span data-stu-id="dd196-129">1</span></span>

<span data-ttu-id="dd196-130">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="dd196-130">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-131">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="dd196-131">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-132">64</span><span class="sxs-lookup"><span data-stu-id="dd196-132">64</span></span>

<span data-ttu-id="dd196-133">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="dd196-133">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-134">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="dd196-134">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-135">65</span><span class="sxs-lookup"><span data-stu-id="dd196-135">65</span></span>

<span data-ttu-id="dd196-136">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="dd196-136">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-137">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="dd196-137">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-138">66</span><span class="sxs-lookup"><span data-stu-id="dd196-138">66</span></span>

<span data-ttu-id="dd196-139">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="dd196-139">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-140">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="dd196-140">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-141">67</span><span class="sxs-lookup"><span data-stu-id="dd196-141">67</span></span>

<span data-ttu-id="dd196-142">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="dd196-142">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-143">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="dd196-143">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-144">68</span><span class="sxs-lookup"><span data-stu-id="dd196-144">68</span></span>

<span data-ttu-id="dd196-145">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="dd196-145">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-146">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="dd196-146">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-147">69</span><span class="sxs-lookup"><span data-stu-id="dd196-147">69</span></span>

<span data-ttu-id="dd196-148">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="dd196-148">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-149">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="dd196-149">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-150">70</span><span class="sxs-lookup"><span data-stu-id="dd196-150">70</span></span>

<span data-ttu-id="dd196-151">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="dd196-151">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-152">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="dd196-152">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-153">71</span><span class="sxs-lookup"><span data-stu-id="dd196-153">71</span></span>

<span data-ttu-id="dd196-154">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="dd196-154">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-155">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="dd196-155">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-156">72</span><span class="sxs-lookup"><span data-stu-id="dd196-156">72</span></span>

<span data-ttu-id="dd196-157">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="dd196-157">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-158">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="dd196-158">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-159">73</span><span class="sxs-lookup"><span data-stu-id="dd196-159">73</span></span>

<span data-ttu-id="dd196-160">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="dd196-160">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-161">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="dd196-161">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-162">74</span><span class="sxs-lookup"><span data-stu-id="dd196-162">74</span></span>

<span data-ttu-id="dd196-163">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="dd196-163">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-164">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="dd196-164">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-165">75</span><span class="sxs-lookup"><span data-stu-id="dd196-165">75</span></span>

<span data-ttu-id="dd196-166">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="dd196-166">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-167">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="dd196-167">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-168">76</span><span class="sxs-lookup"><span data-stu-id="dd196-168">76</span></span>

<span data-ttu-id="dd196-169">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="dd196-169">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-170">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="dd196-170">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-171">77</span><span class="sxs-lookup"><span data-stu-id="dd196-171">77</span></span>

<span data-ttu-id="dd196-172">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="dd196-172">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-173">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="dd196-173">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-174">78</span><span class="sxs-lookup"><span data-stu-id="dd196-174">78</span></span>

<span data-ttu-id="dd196-175">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="dd196-175">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-176">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="dd196-176">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-177">79</span><span class="sxs-lookup"><span data-stu-id="dd196-177">79</span></span>

<span data-ttu-id="dd196-178">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="dd196-178">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-179">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="dd196-179">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-180">80</span><span class="sxs-lookup"><span data-stu-id="dd196-180">80</span></span>

<span data-ttu-id="dd196-181">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="dd196-181">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-182">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="dd196-182">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-183">81</span><span class="sxs-lookup"><span data-stu-id="dd196-183">81</span></span>

<span data-ttu-id="dd196-184">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="dd196-184">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-185">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="dd196-185">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-186">82</span><span class="sxs-lookup"><span data-stu-id="dd196-186">82</span></span>

<span data-ttu-id="dd196-187">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="dd196-187">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-188">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="dd196-188">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-189">83</span><span class="sxs-lookup"><span data-stu-id="dd196-189">83</span></span>

<span data-ttu-id="dd196-190">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="dd196-190">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-191">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="dd196-191">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-192">84</span><span class="sxs-lookup"><span data-stu-id="dd196-192">84</span></span>

<span data-ttu-id="dd196-193">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="dd196-193">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-194">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="dd196-194">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-195">85</span><span class="sxs-lookup"><span data-stu-id="dd196-195">85</span></span>

<span data-ttu-id="dd196-196">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="dd196-196">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-197">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="dd196-197">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-198">86</span><span class="sxs-lookup"><span data-stu-id="dd196-198">86</span></span>

<span data-ttu-id="dd196-199">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="dd196-199">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-200">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="dd196-200">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-201">87</span><span class="sxs-lookup"><span data-stu-id="dd196-201">87</span></span>

<span data-ttu-id="dd196-202">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="dd196-202">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-203">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="dd196-203">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-204">88</span><span class="sxs-lookup"><span data-stu-id="dd196-204">88</span></span>

<span data-ttu-id="dd196-205">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="dd196-205">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-206">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="dd196-206">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-207">89</span><span class="sxs-lookup"><span data-stu-id="dd196-207">89</span></span>

<span data-ttu-id="dd196-208">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="dd196-208">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-209">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="dd196-209">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-210">90</span><span class="sxs-lookup"><span data-stu-id="dd196-210">90</span></span>

<span data-ttu-id="dd196-211">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="dd196-211">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-212">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="dd196-212">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-213">91</span><span class="sxs-lookup"><span data-stu-id="dd196-213">91</span></span>

<span data-ttu-id="dd196-214">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="dd196-214">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-215">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="dd196-215">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-216">92</span><span class="sxs-lookup"><span data-stu-id="dd196-216">92</span></span>

<span data-ttu-id="dd196-217">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="dd196-217">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-218">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="dd196-218">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-219">93</span><span class="sxs-lookup"><span data-stu-id="dd196-219">93</span></span>

<span data-ttu-id="dd196-220">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="dd196-220">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-221">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="dd196-221">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-222">94</span><span class="sxs-lookup"><span data-stu-id="dd196-222">94</span></span>

<span data-ttu-id="dd196-223">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="dd196-223">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-224">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="dd196-224">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-225">95</span><span class="sxs-lookup"><span data-stu-id="dd196-225">95</span></span>

<span data-ttu-id="dd196-226">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="dd196-226">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-227">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="dd196-227">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-228">96</span><span class="sxs-lookup"><span data-stu-id="dd196-228">96</span></span>

<span data-ttu-id="dd196-229">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="dd196-229">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-230">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="dd196-230">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-231">97</span><span class="sxs-lookup"><span data-stu-id="dd196-231">97</span></span>

<span data-ttu-id="dd196-232">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="dd196-232">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-233">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="dd196-233">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-234">98</span><span class="sxs-lookup"><span data-stu-id="dd196-234">98</span></span>

<span data-ttu-id="dd196-235">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="dd196-235">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-236">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="dd196-236">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-237">100</span><span class="sxs-lookup"><span data-stu-id="dd196-237">100</span></span>

<span data-ttu-id="dd196-238">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="dd196-238">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="dd196-239">**Otros**</span><span class="sxs-lookup"><span data-stu-id="dd196-239">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="dd196-240">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="dd196-240">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd196-241">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd196-241">Remarks</span></span>

<span data-ttu-id="dd196-242">Los puertos están protegidos solo cuando la propiedad **IPFilterSecurityEnabled** en [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) es **true**.</span><span class="sxs-lookup"><span data-stu-id="dd196-242">Ports are secured only when the **IPFilterSecurityEnabled** property in [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) is **true**.</span></span>

## <a name="examples"></a><span data-ttu-id="dd196-243">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="dd196-243">Examples</span></span>

<span data-ttu-id="dd196-244">En el ejemplo de VBScript [Habilitar IPSec en un adaptador de red](https://Gallery.TechNet.Microsoft.Com/ff821218-c392-42fb-a77c-c3eab899587c) , en la galería de TechNet, se usa **EnableIPSec** para habilitar la seguridad IP para un adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="dd196-244">The [Enable IPSec on a Network Adapter](https://Gallery.TechNet.Microsoft.Com/ff821218-c392-42fb-a77c-c3eab899587c) VBScript sample, on TechNet Gallery, uses **EnableIPSec** to enable IP security for a network adapter.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd196-245">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd196-245">Requirements</span></span>



| <span data-ttu-id="dd196-246">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd196-246">Requirement</span></span> | <span data-ttu-id="dd196-247">Value</span><span class="sxs-lookup"><span data-stu-id="dd196-247">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd196-248">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd196-248">Minimum supported client</span></span><br/> | <span data-ttu-id="dd196-249">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd196-249">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dd196-250">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd196-250">Minimum supported server</span></span><br/> | <span data-ttu-id="dd196-251">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd196-251">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dd196-252">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dd196-252">Namespace</span></span><br/>                | <span data-ttu-id="dd196-253">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="dd196-253">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dd196-254">MOF</span><span class="sxs-lookup"><span data-stu-id="dd196-254">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd196-255"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd196-255"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd196-256">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dd196-256">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd196-257"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd196-257"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd196-258">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd196-258">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd196-259">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="dd196-259">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="dd196-260">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="dd196-260">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="dd196-261">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="dd196-261">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="dd196-262">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="dd196-262">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="dd196-263">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="dd196-263">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

