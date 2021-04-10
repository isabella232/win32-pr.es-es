---
description: El método estático de la clase WMI SetTcpUseRFC1122UrgentPointer se usa para especificar si TCP usa la especificación RFC 1122 para los datos urgentes o el modo utilizado por los sistemas derivados del diseño de software Berkeley (BSD).
ms.assetid: f8d07690-2723-4bc3-b15f-a24d575456a7
ms.tgt_platform: multiple
title: Método SetTcpUseRFC1122UrgentPointer de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpUseRFC1122UrgentPointer
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 928a809211288eb7f024c735ce033b819e5d49f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153115"
---
# <a name="settcpuserfc1122urgentpointer-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="b05b5-103">Método SetTcpUseRFC1122UrgentPointer de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="b05b5-103">SetTcpUseRFC1122UrgentPointer method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="b05b5-104">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetTcpUseRFC1122UrgentPointer** se usa para especificar si TCP usa la especificación RFC 1122 para los datos urgentes o el modo utilizado por los sistemas derivados del diseño de software Berkeley (BSD).</span><span class="sxs-lookup"><span data-stu-id="b05b5-104">The **SetTcpUseRFC1122UrgentPointer** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to specify whether TCP uses the RFC 1122 specification for urgent data, or the mode used by Berkeley Software Design (BSD) derived systems.</span></span>

<span data-ttu-id="b05b5-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="b05b5-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b05b5-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b05b5-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b05b5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b05b5-107">Syntax</span></span>


```mof
uint32 SetTcpUseRFC1122UrgentPointer(
  [in] boolean TcpUseRFC1122UrgentPointer
);
```



## <a name="parameters"></a><span data-ttu-id="b05b5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b05b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b05b5-109">*TcpUseRFC1122UrgentPointer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b05b5-109">*TcpUseRFC1122UrgentPointer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-110">Si **es true**, TCP utiliza la especificación RFC 1122.</span><span class="sxs-lookup"><span data-stu-id="b05b5-110">If **true**, TCP uses the RFC 1122 specification.</span></span> <span data-ttu-id="b05b5-111">Si es **false**, los datos urgentes se envían en el modo utilizado por los sistemas derivados de BSD.</span><span class="sxs-lookup"><span data-stu-id="b05b5-111">If **false**, urgent data is sent in the mode used by BSD-derived systems.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b05b5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b05b5-112">Return value</span></span>

<span data-ttu-id="b05b5-113">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="b05b5-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="b05b5-114">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b05b5-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b05b5-115">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b05b5-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b05b5-116">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="b05b5-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-117">0</span><span class="sxs-lookup"><span data-stu-id="b05b5-117">0</span></span>

<span data-ttu-id="b05b5-118">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="b05b5-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-119">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="b05b5-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-120">1</span><span class="sxs-lookup"><span data-stu-id="b05b5-120">1</span></span>

<span data-ttu-id="b05b5-121">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="b05b5-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-122">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="b05b5-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-123">64</span><span class="sxs-lookup"><span data-stu-id="b05b5-123">64</span></span>

<span data-ttu-id="b05b5-124">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="b05b5-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-125">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="b05b5-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-126">65</span><span class="sxs-lookup"><span data-stu-id="b05b5-126">65</span></span>

<span data-ttu-id="b05b5-127">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="b05b5-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-128">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="b05b5-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-129">66</span><span class="sxs-lookup"><span data-stu-id="b05b5-129">66</span></span>

<span data-ttu-id="b05b5-130">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="b05b5-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-131">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="b05b5-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-132">67</span><span class="sxs-lookup"><span data-stu-id="b05b5-132">67</span></span>

<span data-ttu-id="b05b5-133">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="b05b5-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-134">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="b05b5-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-135">68</span><span class="sxs-lookup"><span data-stu-id="b05b5-135">68</span></span>

<span data-ttu-id="b05b5-136">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="b05b5-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-137">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="b05b5-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-138">69</span><span class="sxs-lookup"><span data-stu-id="b05b5-138">69</span></span>

<span data-ttu-id="b05b5-139">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="b05b5-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-140">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="b05b5-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-141">70</span><span class="sxs-lookup"><span data-stu-id="b05b5-141">70</span></span>

<span data-ttu-id="b05b5-142">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="b05b5-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-143">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="b05b5-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-144">71</span><span class="sxs-lookup"><span data-stu-id="b05b5-144">71</span></span>

<span data-ttu-id="b05b5-145">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="b05b5-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-146">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="b05b5-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-147">72</span><span class="sxs-lookup"><span data-stu-id="b05b5-147">72</span></span>

<span data-ttu-id="b05b5-148">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="b05b5-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-149">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="b05b5-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-150">73</span><span class="sxs-lookup"><span data-stu-id="b05b5-150">73</span></span>

<span data-ttu-id="b05b5-151">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="b05b5-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-152">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="b05b5-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-153">74</span><span class="sxs-lookup"><span data-stu-id="b05b5-153">74</span></span>

<span data-ttu-id="b05b5-154">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="b05b5-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-155">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="b05b5-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-156">75</span><span class="sxs-lookup"><span data-stu-id="b05b5-156">75</span></span>

<span data-ttu-id="b05b5-157">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="b05b5-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-158">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="b05b5-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-159">76</span><span class="sxs-lookup"><span data-stu-id="b05b5-159">76</span></span>

<span data-ttu-id="b05b5-160">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="b05b5-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-161">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="b05b5-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-162">77</span><span class="sxs-lookup"><span data-stu-id="b05b5-162">77</span></span>

<span data-ttu-id="b05b5-163">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="b05b5-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-164">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="b05b5-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-165">78</span><span class="sxs-lookup"><span data-stu-id="b05b5-165">78</span></span>

<span data-ttu-id="b05b5-166">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="b05b5-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-167">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="b05b5-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-168">79</span><span class="sxs-lookup"><span data-stu-id="b05b5-168">79</span></span>

<span data-ttu-id="b05b5-169">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="b05b5-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-170">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="b05b5-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-171">80</span><span class="sxs-lookup"><span data-stu-id="b05b5-171">80</span></span>

<span data-ttu-id="b05b5-172">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="b05b5-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-173">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="b05b5-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-174">81</span><span class="sxs-lookup"><span data-stu-id="b05b5-174">81</span></span>

<span data-ttu-id="b05b5-175">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="b05b5-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-176">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="b05b5-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-177">82</span><span class="sxs-lookup"><span data-stu-id="b05b5-177">82</span></span>

<span data-ttu-id="b05b5-178">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="b05b5-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-179">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="b05b5-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-180">83</span><span class="sxs-lookup"><span data-stu-id="b05b5-180">83</span></span>

<span data-ttu-id="b05b5-181">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="b05b5-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-182">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="b05b5-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-183">84</span><span class="sxs-lookup"><span data-stu-id="b05b5-183">84</span></span>

<span data-ttu-id="b05b5-184">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="b05b5-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-185">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="b05b5-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-186">85</span><span class="sxs-lookup"><span data-stu-id="b05b5-186">85</span></span>

<span data-ttu-id="b05b5-187">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="b05b5-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-188">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="b05b5-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-189">86</span><span class="sxs-lookup"><span data-stu-id="b05b5-189">86</span></span>

<span data-ttu-id="b05b5-190">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="b05b5-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-191">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="b05b5-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-192">87</span><span class="sxs-lookup"><span data-stu-id="b05b5-192">87</span></span>

<span data-ttu-id="b05b5-193">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="b05b5-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-194">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="b05b5-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-195">88</span><span class="sxs-lookup"><span data-stu-id="b05b5-195">88</span></span>

<span data-ttu-id="b05b5-196">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="b05b5-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-197">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="b05b5-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-198">89</span><span class="sxs-lookup"><span data-stu-id="b05b5-198">89</span></span>

<span data-ttu-id="b05b5-199">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="b05b5-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-200">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="b05b5-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-201">90</span><span class="sxs-lookup"><span data-stu-id="b05b5-201">90</span></span>

<span data-ttu-id="b05b5-202">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="b05b5-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-203">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="b05b5-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-204">91</span><span class="sxs-lookup"><span data-stu-id="b05b5-204">91</span></span>

<span data-ttu-id="b05b5-205">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="b05b5-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-206">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="b05b5-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-207">92</span><span class="sxs-lookup"><span data-stu-id="b05b5-207">92</span></span>

<span data-ttu-id="b05b5-208">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="b05b5-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-209">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="b05b5-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-210">93</span><span class="sxs-lookup"><span data-stu-id="b05b5-210">93</span></span>

<span data-ttu-id="b05b5-211">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="b05b5-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-212">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="b05b5-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-213">94</span><span class="sxs-lookup"><span data-stu-id="b05b5-213">94</span></span>

<span data-ttu-id="b05b5-214">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="b05b5-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-215">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="b05b5-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-216">95</span><span class="sxs-lookup"><span data-stu-id="b05b5-216">95</span></span>

<span data-ttu-id="b05b5-217">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="b05b5-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-218">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="b05b5-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-219">96</span><span class="sxs-lookup"><span data-stu-id="b05b5-219">96</span></span>

<span data-ttu-id="b05b5-220">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="b05b5-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-221">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="b05b5-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-222">97</span><span class="sxs-lookup"><span data-stu-id="b05b5-222">97</span></span>

<span data-ttu-id="b05b5-223">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="b05b5-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-224">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="b05b5-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-225">98</span><span class="sxs-lookup"><span data-stu-id="b05b5-225">98</span></span>

<span data-ttu-id="b05b5-226">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="b05b5-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-227">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="b05b5-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-228">100</span><span class="sxs-lookup"><span data-stu-id="b05b5-228">100</span></span>

<span data-ttu-id="b05b5-229">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="b05b5-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b05b5-230">**Otros**</span><span class="sxs-lookup"><span data-stu-id="b05b5-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="b05b5-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="b05b5-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b05b5-232">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b05b5-232">Remarks</span></span>

<span data-ttu-id="b05b5-233">RFC 1122 y BSD interpretan de forma diferente el puntero urgente en el encabezado TCP y la longitud de los datos urgentes.</span><span class="sxs-lookup"><span data-stu-id="b05b5-233">RFC 1122 and BSD interpret the urgent pointer in the TCP header and the length of the urgent data differently.</span></span> <span data-ttu-id="b05b5-234">No son interoperables.</span><span class="sxs-lookup"><span data-stu-id="b05b5-234">They are not interoperable.</span></span> <span data-ttu-id="b05b5-235">El valor predeterminado es el modo BSD.</span><span class="sxs-lookup"><span data-stu-id="b05b5-235">The default is BSD mode.</span></span>

## <a name="examples"></a><span data-ttu-id="b05b5-236">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b05b5-236">Examples</span></span>

<span data-ttu-id="b05b5-237">El ejemplo de [modificación del puntero de urgencia usar para todos los adaptadores de red](https://Gallery.TechNet.Microsoft.Com/0ff22a90-0be6-4914-8db7-aaf72cbea9cb) configura un equipo para que use la especificación RFC 1122 para datos urgentes.</span><span class="sxs-lookup"><span data-stu-id="b05b5-237">The [Modify Urgent Pointer Use for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/0ff22a90-0be6-4914-8db7-aaf72cbea9cb) VBScript sample configures a computer to use the RFC 1122 specification for urgent data.</span></span>

## <a name="requirements"></a><span data-ttu-id="b05b5-238">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b05b5-238">Requirements</span></span>



| <span data-ttu-id="b05b5-239">Requisito</span><span class="sxs-lookup"><span data-stu-id="b05b5-239">Requirement</span></span> | <span data-ttu-id="b05b5-240">Value</span><span class="sxs-lookup"><span data-stu-id="b05b5-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b05b5-241">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b05b5-241">Minimum supported client</span></span><br/> | <span data-ttu-id="b05b5-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b05b5-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b05b5-243">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b05b5-243">Minimum supported server</span></span><br/> | <span data-ttu-id="b05b5-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b05b5-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b05b5-245">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b05b5-245">Namespace</span></span><br/>                | <span data-ttu-id="b05b5-246">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b05b5-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b05b5-247">MOF</span><span class="sxs-lookup"><span data-stu-id="b05b5-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b05b5-248"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b05b5-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b05b5-249">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b05b5-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b05b5-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b05b5-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b05b5-251">Vea también</span><span class="sxs-lookup"><span data-stu-id="b05b5-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b05b5-252">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="b05b5-252">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="b05b5-253">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="b05b5-253">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="b05b5-254">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="b05b5-254">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="b05b5-255">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="b05b5-255">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="b05b5-256">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="b05b5-256">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

