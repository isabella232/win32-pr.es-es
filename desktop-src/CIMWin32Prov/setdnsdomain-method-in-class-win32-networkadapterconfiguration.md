---
description: El método de clase WMI método SetDNSDomain permite la configuración del dominio DNS.
ms.assetid: a531133e-1b7c-4d85-979d-63bf4f7c9bed
ms.tgt_platform: multiple
title: Método método SetDNSDomain de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSDomain
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c440d8cb5c720bf6922707f04bc75e2383755c1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275056"
---
# <a name="setdnsdomain-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="573d2-103">Método método SetDNSDomain de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="573d2-103">SetDNSDomain method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="573d2-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **método SetDNSDomain** permite la configuración del dominio DNS.</span><span class="sxs-lookup"><span data-stu-id="573d2-104">The **SetDNSDomain** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method allows for the setting of the DNS domain.</span></span>

<span data-ttu-id="573d2-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="573d2-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="573d2-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="573d2-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="573d2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="573d2-107">Syntax</span></span>


```mof
uint32 SetDNSDomain(
  [in] string DNSDomain
);
```



## <a name="parameters"></a><span data-ttu-id="573d2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="573d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="573d2-109">*DNSDomain* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="573d2-109">*DNSDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="573d2-110">Dominio con el que está asociado el DNS, representado por un nombre de organización seguido de un punto y una extensión que indica el tipo de organización.</span><span class="sxs-lookup"><span data-stu-id="573d2-110">Domain with which the DNS is associated, represented by an organization name followed by a period and an extension that indicates the type of organization.</span></span>

<span data-ttu-id="573d2-111">Ejemplo: "microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="573d2-111">Example: "microsoft.com"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="573d2-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="573d2-112">Return value</span></span>

<span data-ttu-id="573d2-113">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="573d2-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required and a different number if there is an error.</span></span> <span data-ttu-id="573d2-114">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="573d2-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="573d2-115">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="573d2-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="573d2-116">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="573d2-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-117">0</span><span class="sxs-lookup"><span data-stu-id="573d2-117">0</span></span>

<span data-ttu-id="573d2-118">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="573d2-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-119">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="573d2-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-120">1</span><span class="sxs-lookup"><span data-stu-id="573d2-120">1</span></span>

<span data-ttu-id="573d2-121">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="573d2-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-122">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="573d2-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-123">64</span><span class="sxs-lookup"><span data-stu-id="573d2-123">64</span></span>

<span data-ttu-id="573d2-124">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="573d2-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-125">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="573d2-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-126">65</span><span class="sxs-lookup"><span data-stu-id="573d2-126">65</span></span>

<span data-ttu-id="573d2-127">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="573d2-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-128">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="573d2-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-129">66</span><span class="sxs-lookup"><span data-stu-id="573d2-129">66</span></span>

<span data-ttu-id="573d2-130">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="573d2-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-131">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="573d2-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-132">67</span><span class="sxs-lookup"><span data-stu-id="573d2-132">67</span></span>

<span data-ttu-id="573d2-133">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="573d2-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-134">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="573d2-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-135">68</span><span class="sxs-lookup"><span data-stu-id="573d2-135">68</span></span>

<span data-ttu-id="573d2-136">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="573d2-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-137">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="573d2-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-138">69</span><span class="sxs-lookup"><span data-stu-id="573d2-138">69</span></span>

<span data-ttu-id="573d2-139">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="573d2-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-140">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="573d2-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-141">70</span><span class="sxs-lookup"><span data-stu-id="573d2-141">70</span></span>

<span data-ttu-id="573d2-142">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="573d2-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-143">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="573d2-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-144">71</span><span class="sxs-lookup"><span data-stu-id="573d2-144">71</span></span>

<span data-ttu-id="573d2-145">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="573d2-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-146">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="573d2-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-147">72</span><span class="sxs-lookup"><span data-stu-id="573d2-147">72</span></span>

<span data-ttu-id="573d2-148">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="573d2-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-149">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="573d2-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-150">73</span><span class="sxs-lookup"><span data-stu-id="573d2-150">73</span></span>

<span data-ttu-id="573d2-151">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="573d2-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-152">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="573d2-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-153">74</span><span class="sxs-lookup"><span data-stu-id="573d2-153">74</span></span>

<span data-ttu-id="573d2-154">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="573d2-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-155">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="573d2-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-156">75</span><span class="sxs-lookup"><span data-stu-id="573d2-156">75</span></span>

<span data-ttu-id="573d2-157">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="573d2-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-158">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="573d2-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-159">76</span><span class="sxs-lookup"><span data-stu-id="573d2-159">76</span></span>

<span data-ttu-id="573d2-160">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="573d2-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-161">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="573d2-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-162">77</span><span class="sxs-lookup"><span data-stu-id="573d2-162">77</span></span>

<span data-ttu-id="573d2-163">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="573d2-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-164">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="573d2-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-165">78</span><span class="sxs-lookup"><span data-stu-id="573d2-165">78</span></span>

<span data-ttu-id="573d2-166">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="573d2-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-167">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="573d2-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-168">79</span><span class="sxs-lookup"><span data-stu-id="573d2-168">79</span></span>

<span data-ttu-id="573d2-169">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="573d2-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-170">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="573d2-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-171">80</span><span class="sxs-lookup"><span data-stu-id="573d2-171">80</span></span>

<span data-ttu-id="573d2-172">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="573d2-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-173">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="573d2-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-174">81</span><span class="sxs-lookup"><span data-stu-id="573d2-174">81</span></span>

<span data-ttu-id="573d2-175">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="573d2-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-176">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="573d2-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-177">82</span><span class="sxs-lookup"><span data-stu-id="573d2-177">82</span></span>

<span data-ttu-id="573d2-178">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="573d2-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-179">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="573d2-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-180">83</span><span class="sxs-lookup"><span data-stu-id="573d2-180">83</span></span>

<span data-ttu-id="573d2-181">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="573d2-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-182">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="573d2-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-183">84</span><span class="sxs-lookup"><span data-stu-id="573d2-183">84</span></span>

<span data-ttu-id="573d2-184">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="573d2-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-185">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="573d2-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-186">85</span><span class="sxs-lookup"><span data-stu-id="573d2-186">85</span></span>

<span data-ttu-id="573d2-187">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="573d2-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-188">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="573d2-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-189">86</span><span class="sxs-lookup"><span data-stu-id="573d2-189">86</span></span>

<span data-ttu-id="573d2-190">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="573d2-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-191">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="573d2-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-192">87</span><span class="sxs-lookup"><span data-stu-id="573d2-192">87</span></span>

<span data-ttu-id="573d2-193">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="573d2-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-194">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="573d2-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-195">88</span><span class="sxs-lookup"><span data-stu-id="573d2-195">88</span></span>

<span data-ttu-id="573d2-196">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="573d2-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-197">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="573d2-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-198">89</span><span class="sxs-lookup"><span data-stu-id="573d2-198">89</span></span>

<span data-ttu-id="573d2-199">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="573d2-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-200">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="573d2-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-201">90</span><span class="sxs-lookup"><span data-stu-id="573d2-201">90</span></span>

<span data-ttu-id="573d2-202">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="573d2-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-203">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="573d2-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-204">91</span><span class="sxs-lookup"><span data-stu-id="573d2-204">91</span></span>

<span data-ttu-id="573d2-205">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="573d2-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-206">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="573d2-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-207">92</span><span class="sxs-lookup"><span data-stu-id="573d2-207">92</span></span>

<span data-ttu-id="573d2-208">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="573d2-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-209">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="573d2-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-210">93</span><span class="sxs-lookup"><span data-stu-id="573d2-210">93</span></span>

<span data-ttu-id="573d2-211">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="573d2-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-212">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="573d2-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-213">94</span><span class="sxs-lookup"><span data-stu-id="573d2-213">94</span></span>

<span data-ttu-id="573d2-214">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="573d2-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-215">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="573d2-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-216">95</span><span class="sxs-lookup"><span data-stu-id="573d2-216">95</span></span>

<span data-ttu-id="573d2-217">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="573d2-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-218">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="573d2-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-219">96</span><span class="sxs-lookup"><span data-stu-id="573d2-219">96</span></span>

<span data-ttu-id="573d2-220">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="573d2-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-221">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="573d2-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-222">97</span><span class="sxs-lookup"><span data-stu-id="573d2-222">97</span></span>

<span data-ttu-id="573d2-223">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="573d2-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-224">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="573d2-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-225">98</span><span class="sxs-lookup"><span data-stu-id="573d2-225">98</span></span>

<span data-ttu-id="573d2-226">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="573d2-226">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-227">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="573d2-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-228">100</span><span class="sxs-lookup"><span data-stu-id="573d2-228">100</span></span>

<span data-ttu-id="573d2-229">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="573d2-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="573d2-230">**Otros**</span><span class="sxs-lookup"><span data-stu-id="573d2-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="573d2-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="573d2-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="573d2-232">Observaciones</span><span class="sxs-lookup"><span data-stu-id="573d2-232">Remarks</span></span>

<span data-ttu-id="573d2-233">Se trata de una llamada de método dependiente de la instancia que se aplica por cada adaptador.</span><span class="sxs-lookup"><span data-stu-id="573d2-233">This is an instance-dependent method call that applies on a per-adapter basis.</span></span> <span data-ttu-id="573d2-234">La configuración se aplica al adaptador de destino.</span><span class="sxs-lookup"><span data-stu-id="573d2-234">The setting applies to the targeted adapter.</span></span>

## <a name="examples"></a><span data-ttu-id="573d2-235">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="573d2-235">Examples</span></span>

<span data-ttu-id="573d2-236">En el ejemplo de código de VBScript [para asignar el dominio DNS de un adaptador de red](https://Gallery.TechNet.Microsoft.Com/6044a0a4-d320-4c18-a94b-c125796d219b) a la galería de TechNet se usa **método SetDNSDomain** para establecer el dominio DNS de un adaptador de red enlazado a TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="573d2-236">The [Assign the DNS Domain for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/6044a0a4-d320-4c18-a94b-c125796d219b) VBScript code sample on TechNet gallery uses **SetDNSDomain** to set the DNS domain for a TCP/IP-bound network adapter.</span></span>

<span data-ttu-id="573d2-237">En el ejemplo de código [modificar la configuración de TCP/IP para un equipo](https://Gallery.TechNet.Microsoft.Com/3d5ae334-1d75-4cea-8079-78c6bd836faf) de VBScript en la galería de TechNet se usa **método SetDNSDomain** para modificar la configuración de TCP/IP para un adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="573d2-237">The [Modify the TCP/IP Configuration for a Computer](https://Gallery.TechNet.Microsoft.Com/3d5ae334-1d75-4cea-8079-78c6bd836faf) VBScript code sample on TechNet Gallery uses **SetDNSDomain** to modify TCP/IP settings for a network adapter.</span></span>

<span data-ttu-id="573d2-238">En el ejemplo de [habilitación de la configuración de DHCP en un equipo](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) de VBScript en la galería de TechNet se usa **método SetDNSDomain** para configurar todas las opciones que suelen ser necesarias para habilitar DHCP en un equipo.</span><span class="sxs-lookup"><span data-stu-id="573d2-238">The [Enable DHCP Settings on a Computer](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) VBScript sample on TechNet Gallery uses **SetDNSDomain** to configure all the settings typically required to enable DHCP on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="573d2-239">Requisitos</span><span class="sxs-lookup"><span data-stu-id="573d2-239">Requirements</span></span>



| <span data-ttu-id="573d2-240">Requisito</span><span class="sxs-lookup"><span data-stu-id="573d2-240">Requirement</span></span> | <span data-ttu-id="573d2-241">Value</span><span class="sxs-lookup"><span data-stu-id="573d2-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="573d2-242">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="573d2-242">Minimum supported client</span></span><br/> | <span data-ttu-id="573d2-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="573d2-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="573d2-244">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="573d2-244">Minimum supported server</span></span><br/> | <span data-ttu-id="573d2-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="573d2-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="573d2-246">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="573d2-246">Namespace</span></span><br/>                | <span data-ttu-id="573d2-247">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="573d2-247">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="573d2-248">MOF</span><span class="sxs-lookup"><span data-stu-id="573d2-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="573d2-249"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="573d2-249"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="573d2-250">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="573d2-250">DLL</span></span><br/>                      | <dl> <span data-ttu-id="573d2-251"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="573d2-251"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="573d2-252">Vea también</span><span class="sxs-lookup"><span data-stu-id="573d2-252">See also</span></span>

<dl> <dt>

[<span data-ttu-id="573d2-253">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="573d2-253">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="573d2-254">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="573d2-254">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="573d2-255">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="573d2-255">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="573d2-256">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="573d2-256">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="573d2-257">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="573d2-257">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

