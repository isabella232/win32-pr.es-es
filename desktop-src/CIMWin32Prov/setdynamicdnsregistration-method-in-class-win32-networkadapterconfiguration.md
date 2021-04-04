---
description: El método SetDynamicDNSRegistration indica el registro de DNS dinámico de las direcciones IP para este adaptador de enlace de IP.
ms.assetid: 8e6ca408-3283-40b8-b621-9befdc39b730
ms.tgt_platform: multiple
title: Método SetDynamicDNSRegistration de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDynamicDNSRegistration
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 36818205e356f873b391159293e9204a9ced44a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907356"
---
# <a name="setdynamicdnsregistration-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="f8943-103">Método SetDynamicDNSRegistration de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="f8943-103">SetDynamicDNSRegistration method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="f8943-104">El método **SetDynamicDNSRegistration** indica el registro de DNS dinámico de las direcciones IP para este adaptador de enlace de IP.</span><span class="sxs-lookup"><span data-stu-id="f8943-104">The **SetDynamicDNSRegistration** method indicates the dynamic DNS registration of IP addresses for this IP-bound adapter.</span></span>

<span data-ttu-id="f8943-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f8943-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f8943-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f8943-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f8943-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8943-107">Syntax</span></span>


```mof
uint32 SetDynamicDNSRegistration(
  [in]           boolean FullDNSRegistrationEnabled,
  [in, optional] boolean DomainDNSRegistrationEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="f8943-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8943-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8943-109">*FullDNSRegistrationEnabled* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f8943-109">*FullDNSRegistrationEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8943-110">Si **es true**, las direcciones IP de esta conexión se registran en DNS con el nombre DNS completo del equipo.</span><span class="sxs-lookup"><span data-stu-id="f8943-110">If **true**, the IP addresses for this connection is registered in DNS under the computer's full DNS name.</span></span> <span data-ttu-id="f8943-111">El nombre DNS completo del equipo se muestra en la pestaña **identificación de red** del panel de control del sistema.</span><span class="sxs-lookup"><span data-stu-id="f8943-111">The full DNS name of the computer is displayed on the **Network Identification** tab of the system Control Panel.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-112">*DomainDNSRegistrationEnabled* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f8943-112">*DomainDNSRegistrationEnabled* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f8943-113">Si **es true**, las direcciones IP de esta conexión se registran en el nombre de dominio de esta conexión, además de registrarse con el nombre DNS completo del equipo.</span><span class="sxs-lookup"><span data-stu-id="f8943-113">If **true**, the IP addresses for this connection are registered under the domain name of this connection, in addition to being registered under the computer's full DNS name.</span></span> <span data-ttu-id="f8943-114">El nombre de dominio de esta conexión se establece mediante el método [**método SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md) o asignado por DHCP.</span><span class="sxs-lookup"><span data-stu-id="f8943-114">The domain name of this connection is either set using the method [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md) or assigned by DHCP.</span></span> <span data-ttu-id="f8943-115">El nombre registrado es el nombre de host del equipo con el nombre de dominio anexado.</span><span class="sxs-lookup"><span data-stu-id="f8943-115">The registered name is the host name of the computer with the domain name appended.</span></span> <span data-ttu-id="f8943-116">Este parámetro solo tiene significado cuando *FullDNSRegistrationEnabled* está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f8943-116">This parameter has meaning only when *FullDNSRegistrationEnabled* is enabled.</span></span> <span data-ttu-id="f8943-117">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="f8943-117">The default value is **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8943-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8943-118">Return value</span></span>

<span data-ttu-id="f8943-119">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="f8943-119">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="f8943-120">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f8943-120">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f8943-121">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f8943-121">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f8943-122">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="f8943-122">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-123">0</span><span class="sxs-lookup"><span data-stu-id="f8943-123">0</span></span>

<span data-ttu-id="f8943-124">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="f8943-124">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-125">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="f8943-125">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-126">1</span><span class="sxs-lookup"><span data-stu-id="f8943-126">1</span></span>

<span data-ttu-id="f8943-127">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="f8943-127">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-128">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="f8943-128">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-129">64</span><span class="sxs-lookup"><span data-stu-id="f8943-129">64</span></span>

<span data-ttu-id="f8943-130">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="f8943-130">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-131">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="f8943-131">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-132">65</span><span class="sxs-lookup"><span data-stu-id="f8943-132">65</span></span>

<span data-ttu-id="f8943-133">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="f8943-133">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-134">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="f8943-134">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-135">66</span><span class="sxs-lookup"><span data-stu-id="f8943-135">66</span></span>

<span data-ttu-id="f8943-136">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="f8943-136">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-137">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="f8943-137">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-138">67</span><span class="sxs-lookup"><span data-stu-id="f8943-138">67</span></span>

<span data-ttu-id="f8943-139">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="f8943-139">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-140">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="f8943-140">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-141">68</span><span class="sxs-lookup"><span data-stu-id="f8943-141">68</span></span>

<span data-ttu-id="f8943-142">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="f8943-142">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-143">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="f8943-143">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-144">69</span><span class="sxs-lookup"><span data-stu-id="f8943-144">69</span></span>

<span data-ttu-id="f8943-145">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="f8943-145">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-146">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="f8943-146">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-147">70</span><span class="sxs-lookup"><span data-stu-id="f8943-147">70</span></span>

<span data-ttu-id="f8943-148">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="f8943-148">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-149">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="f8943-149">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-150">71</span><span class="sxs-lookup"><span data-stu-id="f8943-150">71</span></span>

<span data-ttu-id="f8943-151">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="f8943-151">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-152">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="f8943-152">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-153">72</span><span class="sxs-lookup"><span data-stu-id="f8943-153">72</span></span>

<span data-ttu-id="f8943-154">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="f8943-154">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-155">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="f8943-155">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-156">73</span><span class="sxs-lookup"><span data-stu-id="f8943-156">73</span></span>

<span data-ttu-id="f8943-157">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="f8943-157">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-158">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="f8943-158">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-159">74</span><span class="sxs-lookup"><span data-stu-id="f8943-159">74</span></span>

<span data-ttu-id="f8943-160">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="f8943-160">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-161">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="f8943-161">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-162">75</span><span class="sxs-lookup"><span data-stu-id="f8943-162">75</span></span>

<span data-ttu-id="f8943-163">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="f8943-163">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-164">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="f8943-164">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-165">76</span><span class="sxs-lookup"><span data-stu-id="f8943-165">76</span></span>

<span data-ttu-id="f8943-166">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="f8943-166">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-167">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="f8943-167">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-168">77</span><span class="sxs-lookup"><span data-stu-id="f8943-168">77</span></span>

<span data-ttu-id="f8943-169">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="f8943-169">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-170">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="f8943-170">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-171">78</span><span class="sxs-lookup"><span data-stu-id="f8943-171">78</span></span>

<span data-ttu-id="f8943-172">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="f8943-172">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-173">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="f8943-173">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-174">79</span><span class="sxs-lookup"><span data-stu-id="f8943-174">79</span></span>

<span data-ttu-id="f8943-175">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="f8943-175">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-176">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="f8943-176">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-177">80</span><span class="sxs-lookup"><span data-stu-id="f8943-177">80</span></span>

<span data-ttu-id="f8943-178">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f8943-178">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-179">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="f8943-179">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-180">81</span><span class="sxs-lookup"><span data-stu-id="f8943-180">81</span></span>

<span data-ttu-id="f8943-181">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="f8943-181">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-182">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="f8943-182">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-183">82</span><span class="sxs-lookup"><span data-stu-id="f8943-183">82</span></span>

<span data-ttu-id="f8943-184">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="f8943-184">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-185">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="f8943-185">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-186">83</span><span class="sxs-lookup"><span data-stu-id="f8943-186">83</span></span>

<span data-ttu-id="f8943-187">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="f8943-187">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-188">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="f8943-188">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-189">84</span><span class="sxs-lookup"><span data-stu-id="f8943-189">84</span></span>

<span data-ttu-id="f8943-190">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="f8943-190">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-191">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="f8943-191">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-192">85</span><span class="sxs-lookup"><span data-stu-id="f8943-192">85</span></span>

<span data-ttu-id="f8943-193">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="f8943-193">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-194">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="f8943-194">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-195">86</span><span class="sxs-lookup"><span data-stu-id="f8943-195">86</span></span>

<span data-ttu-id="f8943-196">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="f8943-196">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-197">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="f8943-197">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-198">87</span><span class="sxs-lookup"><span data-stu-id="f8943-198">87</span></span>

<span data-ttu-id="f8943-199">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="f8943-199">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-200">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="f8943-200">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-201">88</span><span class="sxs-lookup"><span data-stu-id="f8943-201">88</span></span>

<span data-ttu-id="f8943-202">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="f8943-202">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-203">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="f8943-203">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-204">89</span><span class="sxs-lookup"><span data-stu-id="f8943-204">89</span></span>

<span data-ttu-id="f8943-205">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="f8943-205">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-206">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="f8943-206">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-207">90</span><span class="sxs-lookup"><span data-stu-id="f8943-207">90</span></span>

<span data-ttu-id="f8943-208">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="f8943-208">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-209">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="f8943-209">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-210">91</span><span class="sxs-lookup"><span data-stu-id="f8943-210">91</span></span>

<span data-ttu-id="f8943-211">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="f8943-211">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-212">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="f8943-212">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-213">92</span><span class="sxs-lookup"><span data-stu-id="f8943-213">92</span></span>

<span data-ttu-id="f8943-214">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="f8943-214">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-215">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="f8943-215">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-216">93</span><span class="sxs-lookup"><span data-stu-id="f8943-216">93</span></span>

<span data-ttu-id="f8943-217">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="f8943-217">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-218">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="f8943-218">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-219">94</span><span class="sxs-lookup"><span data-stu-id="f8943-219">94</span></span>

<span data-ttu-id="f8943-220">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="f8943-220">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-221">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="f8943-221">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-222">95</span><span class="sxs-lookup"><span data-stu-id="f8943-222">95</span></span>

<span data-ttu-id="f8943-223">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="f8943-223">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-224">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="f8943-224">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-225">96</span><span class="sxs-lookup"><span data-stu-id="f8943-225">96</span></span>

<span data-ttu-id="f8943-226">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="f8943-226">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-227">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="f8943-227">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-228">97</span><span class="sxs-lookup"><span data-stu-id="f8943-228">97</span></span>

<span data-ttu-id="f8943-229">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="f8943-229">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-230">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="f8943-230">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-231">98</span><span class="sxs-lookup"><span data-stu-id="f8943-231">98</span></span>

<span data-ttu-id="f8943-232">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="f8943-232">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-233">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="f8943-233">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-234">100</span><span class="sxs-lookup"><span data-stu-id="f8943-234">100</span></span>

<span data-ttu-id="f8943-235">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="f8943-235">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f8943-236">**Otros**</span><span class="sxs-lookup"><span data-stu-id="f8943-236">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="f8943-237">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="f8943-237">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f8943-238">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f8943-238">Examples</span></span>

<span data-ttu-id="f8943-239">En el ejemplo de VBScript [modificar registro de DNS dinámico para un adaptador de red](https://Gallery.TechNet.Microsoft.Com/6c72969c-16c8-4bb6-92e9-b9020001759f) se configura el registro de DNS dinámico para un adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="f8943-239">The [Modify Dynamic DNS Registration for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/6c72969c-16c8-4bb6-92e9-b9020001759f) VBScript sample configures dynamic DNS registration for a network adapter.</span></span>

<span data-ttu-id="f8943-240">El ejemplo de configuración de [tarjetas de red iSCSI según prácticas recomendadas de Microsoft](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) automatiza la configuración de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f8943-240">The [Configure iSCSI Network Cards as per Microsoft Best Practices PowerShell](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) sample automates the configuration settings for a Virtual Machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8943-241">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8943-241">Requirements</span></span>



| <span data-ttu-id="f8943-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8943-242">Requirement</span></span> | <span data-ttu-id="f8943-243">Value</span><span class="sxs-lookup"><span data-stu-id="f8943-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8943-244">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8943-244">Minimum supported client</span></span><br/> | <span data-ttu-id="f8943-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8943-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f8943-246">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8943-246">Minimum supported server</span></span><br/> | <span data-ttu-id="f8943-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8943-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f8943-248">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f8943-248">Namespace</span></span><br/>                | <span data-ttu-id="f8943-249">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f8943-249">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f8943-250">MOF</span><span class="sxs-lookup"><span data-stu-id="f8943-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8943-251"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8943-251"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8943-252">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f8943-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8943-253"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8943-253"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8943-254">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8943-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8943-255">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="f8943-255">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="f8943-256">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="f8943-256">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="f8943-257">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="f8943-257">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="f8943-258">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="f8943-258">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="f8943-259">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="f8943-259">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

