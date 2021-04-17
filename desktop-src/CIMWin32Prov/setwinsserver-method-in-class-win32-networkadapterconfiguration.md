---
description: El método de clase WMI SetWINSServer establece los servidores de Windows Internet Naming Service (WINS) principales y secundarios en este adaptador de red enlazado a TCP/IP. Este método se aplica independientemente del adaptador de red.
ms.assetid: fa8ce436-b67e-4975-a5c5-1a7d6aab4c8e
ms.tgt_platform: multiple
title: Método SetWINSServer de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetWINSServer
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 49bfb0103a7d9cbbd6ea3faa0e1a868bac7b0196
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652329"
---
# <a name="setwinsserver-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="8c148-104">Método SetWINSServer de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="8c148-104">SetWINSServer method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="8c148-105">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetWINSServer** establece los servidores de Windows Internet Naming Service (WINS) principales y secundarios en este adaptador de red enlazado a TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="8c148-105">The **SetWINSServer** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the primary and secondary Windows Internet Naming Service (WINS) servers on this TCP/IP-bound network adapter.</span></span> <span data-ttu-id="8c148-106">Este método se aplica independientemente del adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="8c148-106">This method is applied independently of the network adapter.</span></span>

<span data-ttu-id="8c148-107">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="8c148-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8c148-108">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8c148-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8c148-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c148-109">Syntax</span></span>


```mof
uint32 SetWINSServer(
  [in] string WINSPrimaryServer,
  [in] string WINSSecondaryServer
);
```



## <a name="parameters"></a><span data-ttu-id="8c148-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c148-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c148-111">*WINSPrimaryServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c148-111">*WINSPrimaryServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c148-112">Dirección IP del servidor WINS principal.</span><span class="sxs-lookup"><span data-stu-id="8c148-112">IP address of the primary WINS server.</span></span>

> [!Note]  
> <span data-ttu-id="8c148-113">Compruebe siempre la validez de esta dirección IP cuando se trata de un origen desconocido o de un origen que no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="8c148-113">Always verify the validity of this IP address when it is from an unknown source, or a source that you do not trust.</span></span>

 

</dd> <dt>

<span data-ttu-id="8c148-114">*WINSSecondaryServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c148-114">*WINSSecondaryServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c148-115">Dirección IP del servidor WINS secundario.</span><span class="sxs-lookup"><span data-stu-id="8c148-115">IP address of the secondary WINS server.</span></span>

> [!Note]  
> <span data-ttu-id="8c148-116">Compruebe siempre la validez de esta dirección IP cuando se trata de un origen desconocido o de un origen que no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="8c148-116">Always verify the validity of this IP address when it is from an unknown source, or a source that you do not trust.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c148-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c148-117">Return value</span></span>

<span data-ttu-id="8c148-118">Devuelve un valor entero de 0 (cero) si la finalización se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="8c148-118">Returns an integer value of 0 (zero) on successful completion, and any other number to indicate an error.</span></span> <span data-ttu-id="8c148-119">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8c148-119">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8c148-120">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8c148-120">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8c148-121">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="8c148-121">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-122">0</span><span class="sxs-lookup"><span data-stu-id="8c148-122">0</span></span>

<span data-ttu-id="8c148-123">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="8c148-123">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-124">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="8c148-124">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-125">1</span><span class="sxs-lookup"><span data-stu-id="8c148-125">1</span></span>

<span data-ttu-id="8c148-126">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="8c148-126">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-127">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="8c148-127">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-128">64</span><span class="sxs-lookup"><span data-stu-id="8c148-128">64</span></span>

<span data-ttu-id="8c148-129">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="8c148-129">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-130">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="8c148-130">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-131">65</span><span class="sxs-lookup"><span data-stu-id="8c148-131">65</span></span>

<span data-ttu-id="8c148-132">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="8c148-132">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-133">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="8c148-133">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-134">66</span><span class="sxs-lookup"><span data-stu-id="8c148-134">66</span></span>

<span data-ttu-id="8c148-135">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="8c148-135">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-136">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="8c148-136">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-137">67</span><span class="sxs-lookup"><span data-stu-id="8c148-137">67</span></span>

<span data-ttu-id="8c148-138">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="8c148-138">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-139">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="8c148-139">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-140">68</span><span class="sxs-lookup"><span data-stu-id="8c148-140">68</span></span>

<span data-ttu-id="8c148-141">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="8c148-141">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-142">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="8c148-142">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-143">69</span><span class="sxs-lookup"><span data-stu-id="8c148-143">69</span></span>

<span data-ttu-id="8c148-144">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="8c148-144">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-145">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="8c148-145">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-146">70</span><span class="sxs-lookup"><span data-stu-id="8c148-146">70</span></span>

<span data-ttu-id="8c148-147">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="8c148-147">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-148">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="8c148-148">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-149">71</span><span class="sxs-lookup"><span data-stu-id="8c148-149">71</span></span>

<span data-ttu-id="8c148-150">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="8c148-150">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-151">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="8c148-151">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-152">72</span><span class="sxs-lookup"><span data-stu-id="8c148-152">72</span></span>

<span data-ttu-id="8c148-153">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="8c148-153">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-154">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="8c148-154">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-155">73</span><span class="sxs-lookup"><span data-stu-id="8c148-155">73</span></span>

<span data-ttu-id="8c148-156">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="8c148-156">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-157">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="8c148-157">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-158">74</span><span class="sxs-lookup"><span data-stu-id="8c148-158">74</span></span>

<span data-ttu-id="8c148-159">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="8c148-159">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-160">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="8c148-160">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-161">75</span><span class="sxs-lookup"><span data-stu-id="8c148-161">75</span></span>

<span data-ttu-id="8c148-162">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="8c148-162">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-163">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="8c148-163">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-164">76</span><span class="sxs-lookup"><span data-stu-id="8c148-164">76</span></span>

<span data-ttu-id="8c148-165">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="8c148-165">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-166">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="8c148-166">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-167">77</span><span class="sxs-lookup"><span data-stu-id="8c148-167">77</span></span>

<span data-ttu-id="8c148-168">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="8c148-168">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-169">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="8c148-169">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-170">78</span><span class="sxs-lookup"><span data-stu-id="8c148-170">78</span></span>

<span data-ttu-id="8c148-171">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="8c148-171">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-172">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="8c148-172">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-173">79</span><span class="sxs-lookup"><span data-stu-id="8c148-173">79</span></span>

<span data-ttu-id="8c148-174">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="8c148-174">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-175">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="8c148-175">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-176">80</span><span class="sxs-lookup"><span data-stu-id="8c148-176">80</span></span>

<span data-ttu-id="8c148-177">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="8c148-177">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-178">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="8c148-178">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-179">81</span><span class="sxs-lookup"><span data-stu-id="8c148-179">81</span></span>

<span data-ttu-id="8c148-180">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="8c148-180">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-181">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="8c148-181">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-182">82</span><span class="sxs-lookup"><span data-stu-id="8c148-182">82</span></span>

<span data-ttu-id="8c148-183">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="8c148-183">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-184">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="8c148-184">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-185">83</span><span class="sxs-lookup"><span data-stu-id="8c148-185">83</span></span>

<span data-ttu-id="8c148-186">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="8c148-186">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-187">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="8c148-187">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-188">84</span><span class="sxs-lookup"><span data-stu-id="8c148-188">84</span></span>

<span data-ttu-id="8c148-189">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="8c148-189">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-190">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="8c148-190">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-191">85</span><span class="sxs-lookup"><span data-stu-id="8c148-191">85</span></span>

<span data-ttu-id="8c148-192">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="8c148-192">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-193">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="8c148-193">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-194">86</span><span class="sxs-lookup"><span data-stu-id="8c148-194">86</span></span>

<span data-ttu-id="8c148-195">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="8c148-195">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-196">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="8c148-196">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-197">87</span><span class="sxs-lookup"><span data-stu-id="8c148-197">87</span></span>

<span data-ttu-id="8c148-198">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="8c148-198">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-199">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="8c148-199">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-200">88</span><span class="sxs-lookup"><span data-stu-id="8c148-200">88</span></span>

<span data-ttu-id="8c148-201">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="8c148-201">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-202">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="8c148-202">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-203">89</span><span class="sxs-lookup"><span data-stu-id="8c148-203">89</span></span>

<span data-ttu-id="8c148-204">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="8c148-204">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-205">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="8c148-205">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-206">90</span><span class="sxs-lookup"><span data-stu-id="8c148-206">90</span></span>

<span data-ttu-id="8c148-207">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="8c148-207">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-208">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="8c148-208">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-209">91</span><span class="sxs-lookup"><span data-stu-id="8c148-209">91</span></span>

<span data-ttu-id="8c148-210">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="8c148-210">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-211">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="8c148-211">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-212">92</span><span class="sxs-lookup"><span data-stu-id="8c148-212">92</span></span>

<span data-ttu-id="8c148-213">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="8c148-213">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-214">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="8c148-214">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-215">93</span><span class="sxs-lookup"><span data-stu-id="8c148-215">93</span></span>

<span data-ttu-id="8c148-216">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="8c148-216">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-217">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="8c148-217">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-218">94</span><span class="sxs-lookup"><span data-stu-id="8c148-218">94</span></span>

<span data-ttu-id="8c148-219">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="8c148-219">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-220">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="8c148-220">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-221">95</span><span class="sxs-lookup"><span data-stu-id="8c148-221">95</span></span>

<span data-ttu-id="8c148-222">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="8c148-222">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-223">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="8c148-223">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-224">96</span><span class="sxs-lookup"><span data-stu-id="8c148-224">96</span></span>

<span data-ttu-id="8c148-225">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="8c148-225">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-226">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="8c148-226">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-227">97</span><span class="sxs-lookup"><span data-stu-id="8c148-227">97</span></span>

<span data-ttu-id="8c148-228">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="8c148-228">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-229">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="8c148-229">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-230">98</span><span class="sxs-lookup"><span data-stu-id="8c148-230">98</span></span>

<span data-ttu-id="8c148-231">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="8c148-231">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-232">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="8c148-232">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-233">100</span><span class="sxs-lookup"><span data-stu-id="8c148-233">100</span></span>

<span data-ttu-id="8c148-234">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="8c148-234">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8c148-235">**Otros**</span><span class="sxs-lookup"><span data-stu-id="8c148-235">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="8c148-236">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="8c148-236">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c148-237">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c148-237">Remarks</span></span>

<span data-ttu-id="8c148-238">Si *WINSPrimaryServer* y *WINSSecondaryServer* se establecen en "" (una cadena vacía), los servidores WINS explícitos se revierten a DHCP.</span><span class="sxs-lookup"><span data-stu-id="8c148-238">If both *WINSPrimaryServer* and *WINSSecondaryServer* are set to "" (an empty string), then explicit WINS servers revert back to DHCP.</span></span>

## <a name="examples"></a><span data-ttu-id="8c148-239">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8c148-239">Examples</span></span>

<span data-ttu-id="8c148-240">[Asignación de una dirección IP recuperada de una base de datos](https://Gallery.TechNet.Microsoft.Com/d4526355-e682-4116-a79a-8bba569b084d) El ejemplo de código VBScript busca un equipo en una base de datos y asigna ese equipo a la dirección IP especificada.</span><span class="sxs-lookup"><span data-stu-id="8c148-240">[The Assign an IP Address Retrieved from a Database](https://Gallery.TechNet.Microsoft.Com/d4526355-e682-4116-a79a-8bba569b084d) VBScript code sample looks up a computer in a database and assigns that computer the specified IP address.</span></span>

<span data-ttu-id="8c148-241">El siguiente ejemplo de código de VBScript establece el servidor WINS principal y secundario para un adaptador de red enlazado a TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="8c148-241">The following VBScript code sample sets the primary and secondary WINS server for a TCP/IP-bound network adapter.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colNetCards = objWMIService.ExecQuery _ 
    ("Select * From Win32_NetworkAdapterConfiguration Where IPEnabled = True") 
 
For Each objNetCard in colNetCards 
    strPrimaryServer = "192.168.1.100" 
    strSecondaryServer = "192.168.1.200" 
    objNetCard.SetWINSServer strPrimaryServer, strSecondaryServer 
Next 
```



## <a name="requirements"></a><span data-ttu-id="8c148-242">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c148-242">Requirements</span></span>



| <span data-ttu-id="8c148-243">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c148-243">Requirement</span></span> | <span data-ttu-id="8c148-244">Value</span><span class="sxs-lookup"><span data-stu-id="8c148-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c148-245">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c148-245">Minimum supported client</span></span><br/> | <span data-ttu-id="8c148-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c148-246">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8c148-247">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c148-247">Minimum supported server</span></span><br/> | <span data-ttu-id="8c148-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c148-248">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8c148-249">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8c148-249">Namespace</span></span><br/>                | <span data-ttu-id="8c148-250">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8c148-250">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8c148-251">MOF</span><span class="sxs-lookup"><span data-stu-id="8c148-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c148-252"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c148-252"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c148-253">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8c148-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c148-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c148-254"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c148-255">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c148-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c148-256">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="8c148-256">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="8c148-257">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="8c148-257">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="8c148-258">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="8c148-258">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="8c148-259">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="8c148-259">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="8c148-260">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="8c148-260">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

