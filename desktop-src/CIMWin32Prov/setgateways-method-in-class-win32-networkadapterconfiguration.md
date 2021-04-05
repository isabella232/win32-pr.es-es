---
description: SetGateways &\# 32; Método de clase WMI especifica una lista de puertas de enlace para enrutar paquetes a una subred diferente de la subred a la que está conectado el adaptador de red.
ms.assetid: 240f7aff-7a07-4e0d-af30-7bcabb68c736
ms.tgt_platform: multiple
title: Método SetGateways de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetGateways
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 215bfa736a0f9d67ae587ac1f0e1b4aa394b85d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907324"
---
# <a name="setgateways-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="f2577-103">Método SetGateways de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="f2577-103">SetGateways method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="f2577-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetGateways** especifica una lista de puertas de enlace para enrutar paquetes a una subred diferente de la subred a la que está conectado el adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="f2577-104">The **SetGateways** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method specifies a list of gateways for routing packets to a subnet that is different from the subnet that the network adapter is connected to.</span></span>

<span data-ttu-id="f2577-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f2577-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f2577-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f2577-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f2577-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2577-107">Syntax</span></span>


```mof
uint32 SetGateways(
  [in]           string DefaultIPGateway[],
  [in, optional] uint16 GatewayCostMetric[]
);
```



## <a name="parameters"></a><span data-ttu-id="f2577-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2577-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2577-109">*DefaultIPGateway* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2577-109">*DefaultIPGateway* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2577-110">Lista de direcciones IP a las puertas de enlace en las que se enrutan los paquetes de red.</span><span class="sxs-lookup"><span data-stu-id="f2577-110">List of IP addresses to gateways where network packets are routed.</span></span>

</dd> <dt>

<span data-ttu-id="f2577-111">*GatewayCostMetric* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f2577-111">*GatewayCostMetric* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f2577-112">Asigna un valor que oscila entre 1 y 9999, que se usa para calcular las rutas más rápidas y confiables.</span><span class="sxs-lookup"><span data-stu-id="f2577-112">Assigns a value that ranges from 1 to 9999, which is used to calculate the fastest and most reliable routes.</span></span> <span data-ttu-id="f2577-113">Los valores de este parámetro se corresponden con los valores del parámetro *DefaultIPGateway* .</span><span class="sxs-lookup"><span data-stu-id="f2577-113">The values of this parameter correspond with the values in the *DefaultIPGateway* parameter.</span></span> <span data-ttu-id="f2577-114">El valor predeterminado de una puerta de enlace es 1.</span><span class="sxs-lookup"><span data-stu-id="f2577-114">The default value for a gateway is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2577-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2577-115">Return value</span></span>

<span data-ttu-id="f2577-116">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere un reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y cualquier otro valor si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="f2577-116">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other value if there is an error.</span></span> <span data-ttu-id="f2577-117">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f2577-117">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f2577-118">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f2577-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f2577-119">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="f2577-119">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-120">0</span><span class="sxs-lookup"><span data-stu-id="f2577-120">0</span></span>

</dd> <dt>

<span data-ttu-id="f2577-121">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="f2577-121">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-122">1</span><span class="sxs-lookup"><span data-stu-id="f2577-122">1</span></span>

</dd> <dt>

<span data-ttu-id="f2577-123">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="f2577-123">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-124">64</span><span class="sxs-lookup"><span data-stu-id="f2577-124">64</span></span>

<span data-ttu-id="f2577-125">El método no se admite cuando la NIC está en modo DHCP.</span><span class="sxs-lookup"><span data-stu-id="f2577-125">Method not supported when the NIC is in DHCP mode.</span></span>

</dd> <dt>

<span data-ttu-id="f2577-126">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="f2577-126">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-127">65</span><span class="sxs-lookup"><span data-stu-id="f2577-127">65</span></span>

</dd> <dt>

<span data-ttu-id="f2577-128">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="f2577-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-129">66</span><span class="sxs-lookup"><span data-stu-id="f2577-129">66</span></span>

</dd> <dt>

<span data-ttu-id="f2577-130">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="f2577-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-131">67</span><span class="sxs-lookup"><span data-stu-id="f2577-131">67</span></span>

</dd> <dt>

<span data-ttu-id="f2577-132">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="f2577-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-133">68</span><span class="sxs-lookup"><span data-stu-id="f2577-133">68</span></span>

</dd> <dt>

<span data-ttu-id="f2577-134">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="f2577-134">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-135">69</span><span class="sxs-lookup"><span data-stu-id="f2577-135">69</span></span>

</dd> <dt>

<span data-ttu-id="f2577-136">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="f2577-136">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-137">70</span><span class="sxs-lookup"><span data-stu-id="f2577-137">70</span></span>

</dd> <dt>

<span data-ttu-id="f2577-138">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="f2577-138">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-139">71</span><span class="sxs-lookup"><span data-stu-id="f2577-139">71</span></span>

</dd> <dt>

<span data-ttu-id="f2577-140">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="f2577-140">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-141">72</span><span class="sxs-lookup"><span data-stu-id="f2577-141">72</span></span>

</dd> <dt>

<span data-ttu-id="f2577-142">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="f2577-142">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-143">73</span><span class="sxs-lookup"><span data-stu-id="f2577-143">73</span></span>

</dd> <dt>

<span data-ttu-id="f2577-144">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="f2577-144">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-145">74</span><span class="sxs-lookup"><span data-stu-id="f2577-145">74</span></span>

</dd> <dt>

<span data-ttu-id="f2577-146">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="f2577-146">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-147">75</span><span class="sxs-lookup"><span data-stu-id="f2577-147">75</span></span>

</dd> <dt>

<span data-ttu-id="f2577-148">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="f2577-148">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-149">76</span><span class="sxs-lookup"><span data-stu-id="f2577-149">76</span></span>

</dd> <dt>

<span data-ttu-id="f2577-150">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="f2577-150">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-151">77</span><span class="sxs-lookup"><span data-stu-id="f2577-151">77</span></span>

</dd> <dt>

<span data-ttu-id="f2577-152">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="f2577-152">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-153">78</span><span class="sxs-lookup"><span data-stu-id="f2577-153">78</span></span>

</dd> <dt>

<span data-ttu-id="f2577-154">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="f2577-154">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-155">79</span><span class="sxs-lookup"><span data-stu-id="f2577-155">79</span></span>

</dd> <dt>

<span data-ttu-id="f2577-156">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="f2577-156">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-157">80</span><span class="sxs-lookup"><span data-stu-id="f2577-157">80</span></span>

</dd> <dt>

<span data-ttu-id="f2577-158">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="f2577-158">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-159">81</span><span class="sxs-lookup"><span data-stu-id="f2577-159">81</span></span>

</dd> <dt>

<span data-ttu-id="f2577-160">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="f2577-160">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-161">82</span><span class="sxs-lookup"><span data-stu-id="f2577-161">82</span></span>

</dd> <dt>

<span data-ttu-id="f2577-162">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="f2577-162">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-163">83</span><span class="sxs-lookup"><span data-stu-id="f2577-163">83</span></span>

</dd> <dt>

<span data-ttu-id="f2577-164">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="f2577-164">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-165">84</span><span class="sxs-lookup"><span data-stu-id="f2577-165">84</span></span>

</dd> <dt>

<span data-ttu-id="f2577-166">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="f2577-166">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-167">85</span><span class="sxs-lookup"><span data-stu-id="f2577-167">85</span></span>

</dd> <dt>

<span data-ttu-id="f2577-168">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="f2577-168">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-169">86</span><span class="sxs-lookup"><span data-stu-id="f2577-169">86</span></span>

</dd> <dt>

<span data-ttu-id="f2577-170">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="f2577-170">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-171">87</span><span class="sxs-lookup"><span data-stu-id="f2577-171">87</span></span>

</dd> <dt>

<span data-ttu-id="f2577-172">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="f2577-172">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-173">88</span><span class="sxs-lookup"><span data-stu-id="f2577-173">88</span></span>

</dd> <dt>

<span data-ttu-id="f2577-174">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="f2577-174">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-175">89</span><span class="sxs-lookup"><span data-stu-id="f2577-175">89</span></span>

</dd> <dt>

<span data-ttu-id="f2577-176">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="f2577-176">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-177">90</span><span class="sxs-lookup"><span data-stu-id="f2577-177">90</span></span>

</dd> <dt>

<span data-ttu-id="f2577-178">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="f2577-178">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-179">91</span><span class="sxs-lookup"><span data-stu-id="f2577-179">91</span></span>

</dd> <dt>

<span data-ttu-id="f2577-180">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="f2577-180">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-181">92</span><span class="sxs-lookup"><span data-stu-id="f2577-181">92</span></span>

</dd> <dt>

<span data-ttu-id="f2577-182">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="f2577-182">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-183">93</span><span class="sxs-lookup"><span data-stu-id="f2577-183">93</span></span>

</dd> <dt>

<span data-ttu-id="f2577-184">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="f2577-184">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-185">94</span><span class="sxs-lookup"><span data-stu-id="f2577-185">94</span></span>

</dd> <dt>

<span data-ttu-id="f2577-186">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="f2577-186">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-187">95</span><span class="sxs-lookup"><span data-stu-id="f2577-187">95</span></span>

</dd> <dt>

<span data-ttu-id="f2577-188">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="f2577-188">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-189">96</span><span class="sxs-lookup"><span data-stu-id="f2577-189">96</span></span>

</dd> <dt>

<span data-ttu-id="f2577-190">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="f2577-190">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-191">97</span><span class="sxs-lookup"><span data-stu-id="f2577-191">97</span></span>

</dd> <dt>

<span data-ttu-id="f2577-192">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="f2577-192">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-193">98</span><span class="sxs-lookup"><span data-stu-id="f2577-193">98</span></span>

</dd> <dt>

<span data-ttu-id="f2577-194">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="f2577-194">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-195">100</span><span class="sxs-lookup"><span data-stu-id="f2577-195">100</span></span>

</dd> <dt>

<span data-ttu-id="f2577-196">**Otros**</span><span class="sxs-lookup"><span data-stu-id="f2577-196">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="f2577-197">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="f2577-197">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2577-198">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2577-198">Remarks</span></span>

<span data-ttu-id="f2577-199">Este método solo funciona cuando la tarjeta de interfaz de red (NIC) está en modo de dirección IP estática.</span><span class="sxs-lookup"><span data-stu-id="f2577-199">This method only works when the Network Interface Card (NIC) is in the static IP mode.</span></span>

<span data-ttu-id="f2577-200">Para borrar la puerta de enlace, establezca la puerta de enlace en la misma dirección IP que usa en [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="f2577-200">To clear the gateway, set your gateway to the same IP you use on [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f2577-201">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f2577-201">Examples</span></span>

<span data-ttu-id="f2577-202">En el ejemplo de VBScript [modificar las puertas de enlace para un adaptador de red](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f) se configuran dos puertas de enlace para un adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="f2577-202">The [Modify the Gateways for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f) VBScript sample configures two gateways for a network adapter.</span></span>

<span data-ttu-id="f2577-203">En el ejemplo de la [asignación de una dirección IP estática](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) de VBScript se establece la dirección IP y la puerta de enlace de un equipo.</span><span class="sxs-lookup"><span data-stu-id="f2577-203">The [Assign a Static IP Address](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) VBScript sample sets the IP address and gateway of a computer.</span></span>

<span data-ttu-id="f2577-204">La [dirección IP estática y, a continuación, unirse a un dominio](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) de ejemplo de PowerShell ayuda en la reconstrucción de máquinas.</span><span class="sxs-lookup"><span data-stu-id="f2577-204">The [Static IP and then join to a domain](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) PowerShell sample assists in rebuilding machines.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2577-205">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2577-205">Requirements</span></span>



| <span data-ttu-id="f2577-206">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2577-206">Requirement</span></span> | <span data-ttu-id="f2577-207">Value</span><span class="sxs-lookup"><span data-stu-id="f2577-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2577-208">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2577-208">Minimum supported client</span></span><br/> | <span data-ttu-id="f2577-209">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2577-209">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f2577-210">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2577-210">Minimum supported server</span></span><br/> | <span data-ttu-id="f2577-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2577-211">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f2577-212">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f2577-212">Namespace</span></span><br/>                | <span data-ttu-id="f2577-213">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f2577-213">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f2577-214">MOF</span><span class="sxs-lookup"><span data-stu-id="f2577-214">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2577-215"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2577-215"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2577-216">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f2577-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2577-217"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2577-217"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2577-218">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2577-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2577-219">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="f2577-219">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="f2577-220">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="f2577-220">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="f2577-221">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="f2577-221">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="f2577-222">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="f2577-222">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="f2577-223">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="f2577-223">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

