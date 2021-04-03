---
description: El método estático de la clase WMI SetArpUseEtherSNAP se usa para permitir que los paquetes Ethernet usen la codificación de ajuste 802,3.
ms.assetid: 437954c0-ea6b-4559-a4cb-1f66630e70fe
ms.tgt_platform: multiple
title: Método SetArpUseEtherSNAP de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetArpUseEtherSNAP
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 52e3ce42948d5c40bbde3329b37ee3fa506c47ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907500"
---
# <a name="setarpuseethersnap-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="f21b6-103">Método SetArpUseEtherSNAP de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="f21b6-103">SetArpUseEtherSNAP method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="f21b6-104">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetArpUseEtherSNAP** se usa para permitir que los paquetes Ethernet usen la codificación de ajuste 802,3.</span><span class="sxs-lookup"><span data-stu-id="f21b6-104">The **SetArpUseEtherSNAP** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable ethernet packets to use 802.3 SNAP encoding.</span></span>

<span data-ttu-id="f21b6-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f21b6-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f21b6-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f21b6-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f21b6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f21b6-107">Syntax</span></span>


```mof
uint32 SetArpUseEtherSNAP(
  [in] boolean ArpUseEtherSNAP
);
```



## <a name="parameters"></a><span data-ttu-id="f21b6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f21b6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f21b6-109">*ArpUseEtherSNAP* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f21b6-109">*ArpUseEtherSNAP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-110">Si **es true** , se habilita TCP/IP para transmitir paquetes Ethernet mediante la codificación de ajuste 802,3.</span><span class="sxs-lookup"><span data-stu-id="f21b6-110">If **true** enables TCP/IP to transmit Ethernet packets using 802.3 SNAP encoding.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f21b6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f21b6-111">Return value</span></span>

<span data-ttu-id="f21b6-112">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="f21b6-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="f21b6-113">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f21b6-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f21b6-114">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f21b6-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f21b6-115">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="f21b6-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-116">0</span><span class="sxs-lookup"><span data-stu-id="f21b6-116">0</span></span>

<span data-ttu-id="f21b6-117">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="f21b6-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-118">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="f21b6-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-119">1</span><span class="sxs-lookup"><span data-stu-id="f21b6-119">1</span></span>

<span data-ttu-id="f21b6-120">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="f21b6-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-121">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="f21b6-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-122">64</span><span class="sxs-lookup"><span data-stu-id="f21b6-122">64</span></span>

<span data-ttu-id="f21b6-123">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="f21b6-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-124">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="f21b6-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-125">65</span><span class="sxs-lookup"><span data-stu-id="f21b6-125">65</span></span>

<span data-ttu-id="f21b6-126">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="f21b6-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-127">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="f21b6-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-128">66</span><span class="sxs-lookup"><span data-stu-id="f21b6-128">66</span></span>

<span data-ttu-id="f21b6-129">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="f21b6-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-130">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="f21b6-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-131">67</span><span class="sxs-lookup"><span data-stu-id="f21b6-131">67</span></span>

<span data-ttu-id="f21b6-132">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="f21b6-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-133">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="f21b6-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-134">68</span><span class="sxs-lookup"><span data-stu-id="f21b6-134">68</span></span>

<span data-ttu-id="f21b6-135">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="f21b6-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-136">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="f21b6-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-137">69</span><span class="sxs-lookup"><span data-stu-id="f21b6-137">69</span></span>

<span data-ttu-id="f21b6-138">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="f21b6-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-139">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="f21b6-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-140">70</span><span class="sxs-lookup"><span data-stu-id="f21b6-140">70</span></span>

<span data-ttu-id="f21b6-141">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="f21b6-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-142">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="f21b6-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-143">71</span><span class="sxs-lookup"><span data-stu-id="f21b6-143">71</span></span>

<span data-ttu-id="f21b6-144">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="f21b6-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-145">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="f21b6-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-146">72</span><span class="sxs-lookup"><span data-stu-id="f21b6-146">72</span></span>

<span data-ttu-id="f21b6-147">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="f21b6-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-148">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="f21b6-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-149">73</span><span class="sxs-lookup"><span data-stu-id="f21b6-149">73</span></span>

<span data-ttu-id="f21b6-150">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="f21b6-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-151">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="f21b6-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-152">74</span><span class="sxs-lookup"><span data-stu-id="f21b6-152">74</span></span>

<span data-ttu-id="f21b6-153">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="f21b6-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-154">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="f21b6-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-155">75</span><span class="sxs-lookup"><span data-stu-id="f21b6-155">75</span></span>

<span data-ttu-id="f21b6-156">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="f21b6-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-157">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="f21b6-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-158">76</span><span class="sxs-lookup"><span data-stu-id="f21b6-158">76</span></span>

<span data-ttu-id="f21b6-159">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="f21b6-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-160">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="f21b6-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-161">77</span><span class="sxs-lookup"><span data-stu-id="f21b6-161">77</span></span>

<span data-ttu-id="f21b6-162">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="f21b6-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-163">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="f21b6-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-164">78</span><span class="sxs-lookup"><span data-stu-id="f21b6-164">78</span></span>

<span data-ttu-id="f21b6-165">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="f21b6-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-166">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="f21b6-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-167">79</span><span class="sxs-lookup"><span data-stu-id="f21b6-167">79</span></span>

<span data-ttu-id="f21b6-168">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="f21b6-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-169">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="f21b6-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-170">80</span><span class="sxs-lookup"><span data-stu-id="f21b6-170">80</span></span>

<span data-ttu-id="f21b6-171">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f21b6-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-172">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="f21b6-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-173">81</span><span class="sxs-lookup"><span data-stu-id="f21b6-173">81</span></span>

<span data-ttu-id="f21b6-174">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="f21b6-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-175">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="f21b6-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-176">82</span><span class="sxs-lookup"><span data-stu-id="f21b6-176">82</span></span>

<span data-ttu-id="f21b6-177">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="f21b6-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-178">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="f21b6-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-179">83</span><span class="sxs-lookup"><span data-stu-id="f21b6-179">83</span></span>

<span data-ttu-id="f21b6-180">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="f21b6-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-181">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="f21b6-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-182">84</span><span class="sxs-lookup"><span data-stu-id="f21b6-182">84</span></span>

<span data-ttu-id="f21b6-183">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="f21b6-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-184">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="f21b6-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-185">85</span><span class="sxs-lookup"><span data-stu-id="f21b6-185">85</span></span>

<span data-ttu-id="f21b6-186">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="f21b6-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-187">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="f21b6-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-188">86</span><span class="sxs-lookup"><span data-stu-id="f21b6-188">86</span></span>

<span data-ttu-id="f21b6-189">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="f21b6-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-190">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="f21b6-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-191">87</span><span class="sxs-lookup"><span data-stu-id="f21b6-191">87</span></span>

<span data-ttu-id="f21b6-192">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="f21b6-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-193">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="f21b6-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-194">88</span><span class="sxs-lookup"><span data-stu-id="f21b6-194">88</span></span>

<span data-ttu-id="f21b6-195">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="f21b6-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-196">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="f21b6-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-197">89</span><span class="sxs-lookup"><span data-stu-id="f21b6-197">89</span></span>

<span data-ttu-id="f21b6-198">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="f21b6-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-199">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="f21b6-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-200">90</span><span class="sxs-lookup"><span data-stu-id="f21b6-200">90</span></span>

<span data-ttu-id="f21b6-201">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="f21b6-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-202">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="f21b6-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-203">91</span><span class="sxs-lookup"><span data-stu-id="f21b6-203">91</span></span>

<span data-ttu-id="f21b6-204">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="f21b6-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-205">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="f21b6-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-206">92</span><span class="sxs-lookup"><span data-stu-id="f21b6-206">92</span></span>

<span data-ttu-id="f21b6-207">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="f21b6-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-208">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="f21b6-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-209">93</span><span class="sxs-lookup"><span data-stu-id="f21b6-209">93</span></span>

<span data-ttu-id="f21b6-210">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="f21b6-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-211">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="f21b6-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-212">94</span><span class="sxs-lookup"><span data-stu-id="f21b6-212">94</span></span>

<span data-ttu-id="f21b6-213">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="f21b6-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-214">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="f21b6-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-215">95</span><span class="sxs-lookup"><span data-stu-id="f21b6-215">95</span></span>

<span data-ttu-id="f21b6-216">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="f21b6-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-217">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="f21b6-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-218">96</span><span class="sxs-lookup"><span data-stu-id="f21b6-218">96</span></span>

<span data-ttu-id="f21b6-219">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="f21b6-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-220">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="f21b6-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-221">97</span><span class="sxs-lookup"><span data-stu-id="f21b6-221">97</span></span>

<span data-ttu-id="f21b6-222">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="f21b6-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-223">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="f21b6-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-224">98</span><span class="sxs-lookup"><span data-stu-id="f21b6-224">98</span></span>

<span data-ttu-id="f21b6-225">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="f21b6-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-226">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="f21b6-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-227">100</span><span class="sxs-lookup"><span data-stu-id="f21b6-227">100</span></span>

<span data-ttu-id="f21b6-228">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="f21b6-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f21b6-229">**Otros**</span><span class="sxs-lookup"><span data-stu-id="f21b6-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="f21b6-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="f21b6-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f21b6-231">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f21b6-231">Remarks</span></span>

<span data-ttu-id="f21b6-232">De forma predeterminada, la pila transmite paquetes en formato Ethernet digital, Intel, Xerox (DIX).</span><span class="sxs-lookup"><span data-stu-id="f21b6-232">By default, the stack transmits packets in Digital, Intel, Xerox (DIX) Ethernet format.</span></span> <span data-ttu-id="f21b6-233">Siempre recibe ambos formatos.</span><span class="sxs-lookup"><span data-stu-id="f21b6-233">It always receives both formats.</span></span>

## <a name="examples"></a><span data-ttu-id="f21b6-234">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f21b6-234">Examples</span></span>

<span data-ttu-id="f21b6-235">En el ejemplo de código de la opción [Modify ARP queries to use EtherSNAP](https://Gallery.TechNet.Microsoft.Com/2fe24075-fdb1-486d-8c0b-d25075fd8f21) VBScript en la galería de TechNet se usa **SetArpUseEtherSNAP** para configurar los adaptadores de red de un equipo para que usen la codificación de ajuste 802,3 para los paquetes Ethernet.</span><span class="sxs-lookup"><span data-stu-id="f21b6-235">The [Modify ARP Queries to Use EtherSNAP](https://Gallery.TechNet.Microsoft.Com/2fe24075-fdb1-486d-8c0b-d25075fd8f21) VBScript code sample on TechNet Gallery uses **SetArpUseEtherSNAP** to configure the network adapters on a computer to use 802.3 SNAP encoding for Ethernet packets.</span></span>

## <a name="requirements"></a><span data-ttu-id="f21b6-236">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f21b6-236">Requirements</span></span>



| <span data-ttu-id="f21b6-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="f21b6-237">Requirement</span></span> | <span data-ttu-id="f21b6-238">Value</span><span class="sxs-lookup"><span data-stu-id="f21b6-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f21b6-239">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f21b6-239">Minimum supported client</span></span><br/> | <span data-ttu-id="f21b6-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f21b6-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f21b6-241">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f21b6-241">Minimum supported server</span></span><br/> | <span data-ttu-id="f21b6-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f21b6-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f21b6-243">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f21b6-243">Namespace</span></span><br/>                | <span data-ttu-id="f21b6-244">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f21b6-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f21b6-245">MOF</span><span class="sxs-lookup"><span data-stu-id="f21b6-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f21b6-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f21b6-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f21b6-247">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f21b6-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f21b6-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f21b6-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f21b6-249">Vea también</span><span class="sxs-lookup"><span data-stu-id="f21b6-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f21b6-250">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="f21b6-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="f21b6-251">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="f21b6-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="f21b6-252">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="f21b6-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="f21b6-253">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="f21b6-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="f21b6-254">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="f21b6-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

