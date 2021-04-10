---
description: El método estático de la clase WMI SetTcpMaxConnectRetransmissions se usa para establecer el número de intentos que TCP va a retransmitir una solicitud de conexión antes de anular la operación.
ms.assetid: cb0dfba3-4ef5-4052-94f3-f688a1c55d90
ms.tgt_platform: multiple
title: Método SetTcpMaxConnectRetransmissions de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpMaxConnectRetransmissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 160d84c2a466bff34070a6dec4a34804d5a3a7fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153553"
---
# <a name="settcpmaxconnectretransmissions-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="f44d6-103">Método SetTcpMaxConnectRetransmissions de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="f44d6-103">SetTcpMaxConnectRetransmissions method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="f44d6-104">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetTcpMaxConnectRetransmissions** se usa para establecer el número de intentos que TCP va a retransmitir una solicitud de conexión antes de anular la operación.</span><span class="sxs-lookup"><span data-stu-id="f44d6-104">The **SetTcpMaxConnectRetransmissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the number of attempts TCP will retransmit a connect request before aborting.</span></span>

<span data-ttu-id="f44d6-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f44d6-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f44d6-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f44d6-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f44d6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f44d6-107">Syntax</span></span>


```mof
uint32 SetTcpMaxConnectRetransmissions(
  [in] uint32 TcpMaxConnectRetransmissions
);
```



## <a name="parameters"></a><span data-ttu-id="f44d6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f44d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f44d6-109">*TcpMaxConnectRetransmissions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f44d6-109">*TcpMaxConnectRetransmissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-110">Número de intentos que TCP retransmitirá una solicitud de conexión antes de anular la operación.</span><span class="sxs-lookup"><span data-stu-id="f44d6-110">Number of attempts TCP will retransmit a connect request before aborting.</span></span> <span data-ttu-id="f44d6-111">El intervalo válido para los valores es 0-0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="f44d6-111">The valid range for values is 0 - 0xFFFFFFFF.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f44d6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f44d6-112">Return value</span></span>

<span data-ttu-id="f44d6-113">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="f44d6-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="f44d6-114">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f44d6-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f44d6-115">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f44d6-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f44d6-116">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="f44d6-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-117">0</span><span class="sxs-lookup"><span data-stu-id="f44d6-117">0</span></span>

<span data-ttu-id="f44d6-118">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="f44d6-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-119">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="f44d6-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-120">1</span><span class="sxs-lookup"><span data-stu-id="f44d6-120">1</span></span>

<span data-ttu-id="f44d6-121">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="f44d6-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-122">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="f44d6-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-123">64</span><span class="sxs-lookup"><span data-stu-id="f44d6-123">64</span></span>

<span data-ttu-id="f44d6-124">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="f44d6-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-125">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="f44d6-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-126">65</span><span class="sxs-lookup"><span data-stu-id="f44d6-126">65</span></span>

<span data-ttu-id="f44d6-127">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="f44d6-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-128">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="f44d6-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-129">66</span><span class="sxs-lookup"><span data-stu-id="f44d6-129">66</span></span>

<span data-ttu-id="f44d6-130">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="f44d6-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-131">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="f44d6-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-132">67</span><span class="sxs-lookup"><span data-stu-id="f44d6-132">67</span></span>

<span data-ttu-id="f44d6-133">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="f44d6-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-134">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="f44d6-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-135">68</span><span class="sxs-lookup"><span data-stu-id="f44d6-135">68</span></span>

<span data-ttu-id="f44d6-136">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="f44d6-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-137">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="f44d6-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-138">69</span><span class="sxs-lookup"><span data-stu-id="f44d6-138">69</span></span>

<span data-ttu-id="f44d6-139">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="f44d6-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-140">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="f44d6-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-141">70</span><span class="sxs-lookup"><span data-stu-id="f44d6-141">70</span></span>

<span data-ttu-id="f44d6-142">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="f44d6-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-143">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="f44d6-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-144">71</span><span class="sxs-lookup"><span data-stu-id="f44d6-144">71</span></span>

<span data-ttu-id="f44d6-145">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="f44d6-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-146">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="f44d6-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-147">72</span><span class="sxs-lookup"><span data-stu-id="f44d6-147">72</span></span>

<span data-ttu-id="f44d6-148">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="f44d6-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-149">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="f44d6-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-150">73</span><span class="sxs-lookup"><span data-stu-id="f44d6-150">73</span></span>

<span data-ttu-id="f44d6-151">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="f44d6-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-152">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="f44d6-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-153">74</span><span class="sxs-lookup"><span data-stu-id="f44d6-153">74</span></span>

<span data-ttu-id="f44d6-154">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="f44d6-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-155">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="f44d6-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-156">75</span><span class="sxs-lookup"><span data-stu-id="f44d6-156">75</span></span>

<span data-ttu-id="f44d6-157">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="f44d6-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-158">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="f44d6-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-159">76</span><span class="sxs-lookup"><span data-stu-id="f44d6-159">76</span></span>

<span data-ttu-id="f44d6-160">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="f44d6-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-161">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="f44d6-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-162">77</span><span class="sxs-lookup"><span data-stu-id="f44d6-162">77</span></span>

<span data-ttu-id="f44d6-163">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="f44d6-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-164">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="f44d6-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-165">78</span><span class="sxs-lookup"><span data-stu-id="f44d6-165">78</span></span>

<span data-ttu-id="f44d6-166">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="f44d6-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-167">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="f44d6-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-168">79</span><span class="sxs-lookup"><span data-stu-id="f44d6-168">79</span></span>

<span data-ttu-id="f44d6-169">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="f44d6-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-170">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="f44d6-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-171">80</span><span class="sxs-lookup"><span data-stu-id="f44d6-171">80</span></span>

<span data-ttu-id="f44d6-172">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f44d6-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-173">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="f44d6-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-174">81</span><span class="sxs-lookup"><span data-stu-id="f44d6-174">81</span></span>

<span data-ttu-id="f44d6-175">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="f44d6-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-176">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="f44d6-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-177">82</span><span class="sxs-lookup"><span data-stu-id="f44d6-177">82</span></span>

<span data-ttu-id="f44d6-178">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="f44d6-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-179">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="f44d6-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-180">83</span><span class="sxs-lookup"><span data-stu-id="f44d6-180">83</span></span>

<span data-ttu-id="f44d6-181">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="f44d6-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-182">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="f44d6-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-183">84</span><span class="sxs-lookup"><span data-stu-id="f44d6-183">84</span></span>

<span data-ttu-id="f44d6-184">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="f44d6-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-185">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="f44d6-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-186">85</span><span class="sxs-lookup"><span data-stu-id="f44d6-186">85</span></span>

<span data-ttu-id="f44d6-187">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="f44d6-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-188">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="f44d6-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-189">86</span><span class="sxs-lookup"><span data-stu-id="f44d6-189">86</span></span>

<span data-ttu-id="f44d6-190">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="f44d6-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-191">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="f44d6-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-192">87</span><span class="sxs-lookup"><span data-stu-id="f44d6-192">87</span></span>

<span data-ttu-id="f44d6-193">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="f44d6-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-194">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="f44d6-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-195">88</span><span class="sxs-lookup"><span data-stu-id="f44d6-195">88</span></span>

<span data-ttu-id="f44d6-196">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="f44d6-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-197">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="f44d6-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-198">89</span><span class="sxs-lookup"><span data-stu-id="f44d6-198">89</span></span>

<span data-ttu-id="f44d6-199">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="f44d6-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-200">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="f44d6-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-201">90</span><span class="sxs-lookup"><span data-stu-id="f44d6-201">90</span></span>

<span data-ttu-id="f44d6-202">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="f44d6-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-203">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="f44d6-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-204">91</span><span class="sxs-lookup"><span data-stu-id="f44d6-204">91</span></span>

<span data-ttu-id="f44d6-205">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="f44d6-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-206">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="f44d6-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-207">92</span><span class="sxs-lookup"><span data-stu-id="f44d6-207">92</span></span>

<span data-ttu-id="f44d6-208">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="f44d6-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-209">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="f44d6-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-210">93</span><span class="sxs-lookup"><span data-stu-id="f44d6-210">93</span></span>

<span data-ttu-id="f44d6-211">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="f44d6-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-212">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="f44d6-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-213">94</span><span class="sxs-lookup"><span data-stu-id="f44d6-213">94</span></span>

<span data-ttu-id="f44d6-214">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="f44d6-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-215">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="f44d6-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-216">95</span><span class="sxs-lookup"><span data-stu-id="f44d6-216">95</span></span>

<span data-ttu-id="f44d6-217">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="f44d6-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-218">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="f44d6-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-219">96</span><span class="sxs-lookup"><span data-stu-id="f44d6-219">96</span></span>

<span data-ttu-id="f44d6-220">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="f44d6-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-221">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="f44d6-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-222">97</span><span class="sxs-lookup"><span data-stu-id="f44d6-222">97</span></span>

<span data-ttu-id="f44d6-223">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="f44d6-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-224">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="f44d6-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-225">98</span><span class="sxs-lookup"><span data-stu-id="f44d6-225">98</span></span>

<span data-ttu-id="f44d6-226">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="f44d6-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-227">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="f44d6-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-228">100</span><span class="sxs-lookup"><span data-stu-id="f44d6-228">100</span></span>

<span data-ttu-id="f44d6-229">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="f44d6-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f44d6-230">**Otros**</span><span class="sxs-lookup"><span data-stu-id="f44d6-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="f44d6-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="f44d6-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f44d6-232">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f44d6-232">Remarks</span></span>

<span data-ttu-id="f44d6-233">El tiempo de espera de la retransmisión inicial es de tres segundos y el doble para cada intento sucesivo.</span><span class="sxs-lookup"><span data-stu-id="f44d6-233">The initial retransmission timeout is three seconds, and doubles for each successive attempt.</span></span>

## <a name="examples"></a><span data-ttu-id="f44d6-234">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f44d6-234">Examples</span></span>

<span data-ttu-id="f44d6-235">En el ejemplo de VBScript [Modify the retransmisións de conexiones TCP máximas permitidas](https://Gallery.TechNet.Microsoft.Com/e599c6bc-fa37-457d-b7e3-3c003517ed46) se configura el número de veces que TCP retransmitirá un intento de conexión antes de abandonar el esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="f44d6-235">The [Modify the Maximum Allowed TCP Connection Retransmissions](https://Gallery.TechNet.Microsoft.Com/e599c6bc-fa37-457d-b7e3-3c003517ed46) VBScript sample configures the number of times TCP will retransmit a connection attempt before abandoning the effort.</span></span>

## <a name="requirements"></a><span data-ttu-id="f44d6-236">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f44d6-236">Requirements</span></span>



| <span data-ttu-id="f44d6-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="f44d6-237">Requirement</span></span> | <span data-ttu-id="f44d6-238">Value</span><span class="sxs-lookup"><span data-stu-id="f44d6-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f44d6-239">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f44d6-239">Minimum supported client</span></span><br/> | <span data-ttu-id="f44d6-240">Windows Vista, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f44d6-240">Windows Vista, Windows Vista</span></span><br/>                                                 |
| <span data-ttu-id="f44d6-241">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f44d6-241">Minimum supported server</span></span><br/> | <span data-ttu-id="f44d6-242">Windows Server 2008, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f44d6-242">Windows Server 2008, Windows Server 2008</span></span><br/>                                     |
| <span data-ttu-id="f44d6-243">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f44d6-243">Namespace</span></span><br/>                | <span data-ttu-id="f44d6-244">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f44d6-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f44d6-245">MOF</span><span class="sxs-lookup"><span data-stu-id="f44d6-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f44d6-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f44d6-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f44d6-247">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f44d6-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f44d6-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f44d6-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f44d6-249">Vea también</span><span class="sxs-lookup"><span data-stu-id="f44d6-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f44d6-250">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="f44d6-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="f44d6-251">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="f44d6-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="f44d6-252">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="f44d6-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="f44d6-253">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="f44d6-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="f44d6-254">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="f44d6-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

