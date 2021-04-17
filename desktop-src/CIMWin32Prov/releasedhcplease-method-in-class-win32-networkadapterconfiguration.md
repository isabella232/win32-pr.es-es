---
description: El método de clase WMI ReleaseDHCPLease libera la dirección IP enlazada a un adaptador de red habilitado para DHCP específico.
ms.assetid: 0cf4b531-8626-4388-bffa-e16a4aa8c794
ms.tgt_platform: multiple
title: Método ReleaseDHCPLease de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.ReleaseDHCPLease
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5520a6b2d0960c1d4258b19f8cd4d600c9b8fe34
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659684"
---
# <a name="releasedhcplease-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="da49f-103">Método ReleaseDHCPLease de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="da49f-103">ReleaseDHCPLease method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="da49f-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ReleaseDHCPLease** libera la dirección IP enlazada a un adaptador de red habilitado para DHCP específico.</span><span class="sxs-lookup"><span data-stu-id="da49f-104">The **ReleaseDHCPLease** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method releases the IP address bound to a specific DHCP-enabled network adapter.</span></span>

<span data-ttu-id="da49f-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="da49f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="da49f-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="da49f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="da49f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da49f-107">Syntax</span></span>


```mof
uint32 ReleaseDHCPLease();
```



## <a name="parameters"></a><span data-ttu-id="da49f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da49f-108">Parameters</span></span>

<span data-ttu-id="da49f-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="da49f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="da49f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da49f-110">Return value</span></span>

<span data-ttu-id="da49f-111">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="da49f-111">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="da49f-112">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="da49f-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="da49f-113">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="da49f-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="da49f-114">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="da49f-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-115">0</span><span class="sxs-lookup"><span data-stu-id="da49f-115">0</span></span>

<span data-ttu-id="da49f-116">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="da49f-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-117">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="da49f-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-118">1</span><span class="sxs-lookup"><span data-stu-id="da49f-118">1</span></span>

<span data-ttu-id="da49f-119">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="da49f-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-120">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="da49f-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-121">64</span><span class="sxs-lookup"><span data-stu-id="da49f-121">64</span></span>

<span data-ttu-id="da49f-122">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="da49f-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-123">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="da49f-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-124">65</span><span class="sxs-lookup"><span data-stu-id="da49f-124">65</span></span>

<span data-ttu-id="da49f-125">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="da49f-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-126">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="da49f-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-127">66</span><span class="sxs-lookup"><span data-stu-id="da49f-127">66</span></span>

<span data-ttu-id="da49f-128">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="da49f-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-129">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="da49f-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-130">67</span><span class="sxs-lookup"><span data-stu-id="da49f-130">67</span></span>

<span data-ttu-id="da49f-131">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="da49f-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-132">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="da49f-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-133">68</span><span class="sxs-lookup"><span data-stu-id="da49f-133">68</span></span>

<span data-ttu-id="da49f-134">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="da49f-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-135">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="da49f-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-136">69</span><span class="sxs-lookup"><span data-stu-id="da49f-136">69</span></span>

<span data-ttu-id="da49f-137">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="da49f-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-138">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="da49f-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-139">70</span><span class="sxs-lookup"><span data-stu-id="da49f-139">70</span></span>

<span data-ttu-id="da49f-140">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="da49f-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-141">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="da49f-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-142">71</span><span class="sxs-lookup"><span data-stu-id="da49f-142">71</span></span>

<span data-ttu-id="da49f-143">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="da49f-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-144">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="da49f-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-145">72</span><span class="sxs-lookup"><span data-stu-id="da49f-145">72</span></span>

<span data-ttu-id="da49f-146">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="da49f-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-147">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="da49f-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-148">73</span><span class="sxs-lookup"><span data-stu-id="da49f-148">73</span></span>

<span data-ttu-id="da49f-149">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="da49f-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-150">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="da49f-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-151">74</span><span class="sxs-lookup"><span data-stu-id="da49f-151">74</span></span>

<span data-ttu-id="da49f-152">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="da49f-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-153">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="da49f-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-154">75</span><span class="sxs-lookup"><span data-stu-id="da49f-154">75</span></span>

<span data-ttu-id="da49f-155">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="da49f-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-156">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="da49f-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-157">76</span><span class="sxs-lookup"><span data-stu-id="da49f-157">76</span></span>

<span data-ttu-id="da49f-158">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="da49f-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-159">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="da49f-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-160">77</span><span class="sxs-lookup"><span data-stu-id="da49f-160">77</span></span>

<span data-ttu-id="da49f-161">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="da49f-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-162">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="da49f-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-163">78</span><span class="sxs-lookup"><span data-stu-id="da49f-163">78</span></span>

<span data-ttu-id="da49f-164">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="da49f-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-165">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="da49f-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-166">79</span><span class="sxs-lookup"><span data-stu-id="da49f-166">79</span></span>

<span data-ttu-id="da49f-167">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="da49f-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-168">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="da49f-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-169">80</span><span class="sxs-lookup"><span data-stu-id="da49f-169">80</span></span>

<span data-ttu-id="da49f-170">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="da49f-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-171">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="da49f-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-172">81</span><span class="sxs-lookup"><span data-stu-id="da49f-172">81</span></span>

<span data-ttu-id="da49f-173">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="da49f-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-174">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="da49f-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-175">82</span><span class="sxs-lookup"><span data-stu-id="da49f-175">82</span></span>

<span data-ttu-id="da49f-176">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="da49f-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-177">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="da49f-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-178">83</span><span class="sxs-lookup"><span data-stu-id="da49f-178">83</span></span>

<span data-ttu-id="da49f-179">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="da49f-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-180">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="da49f-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-181">84</span><span class="sxs-lookup"><span data-stu-id="da49f-181">84</span></span>

<span data-ttu-id="da49f-182">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="da49f-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-183">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="da49f-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-184">85</span><span class="sxs-lookup"><span data-stu-id="da49f-184">85</span></span>

<span data-ttu-id="da49f-185">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="da49f-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-186">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="da49f-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-187">86</span><span class="sxs-lookup"><span data-stu-id="da49f-187">86</span></span>

<span data-ttu-id="da49f-188">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="da49f-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-189">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="da49f-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-190">87</span><span class="sxs-lookup"><span data-stu-id="da49f-190">87</span></span>

<span data-ttu-id="da49f-191">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="da49f-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-192">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="da49f-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-193">88</span><span class="sxs-lookup"><span data-stu-id="da49f-193">88</span></span>

<span data-ttu-id="da49f-194">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="da49f-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-195">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="da49f-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-196">89</span><span class="sxs-lookup"><span data-stu-id="da49f-196">89</span></span>

<span data-ttu-id="da49f-197">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="da49f-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-198">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="da49f-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-199">90</span><span class="sxs-lookup"><span data-stu-id="da49f-199">90</span></span>

<span data-ttu-id="da49f-200">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="da49f-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-201">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="da49f-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-202">91</span><span class="sxs-lookup"><span data-stu-id="da49f-202">91</span></span>

<span data-ttu-id="da49f-203">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="da49f-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-204">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="da49f-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-205">92</span><span class="sxs-lookup"><span data-stu-id="da49f-205">92</span></span>

<span data-ttu-id="da49f-206">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="da49f-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-207">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="da49f-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-208">93</span><span class="sxs-lookup"><span data-stu-id="da49f-208">93</span></span>

<span data-ttu-id="da49f-209">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="da49f-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-210">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="da49f-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-211">94</span><span class="sxs-lookup"><span data-stu-id="da49f-211">94</span></span>

<span data-ttu-id="da49f-212">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="da49f-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-213">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="da49f-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-214">95</span><span class="sxs-lookup"><span data-stu-id="da49f-214">95</span></span>

<span data-ttu-id="da49f-215">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="da49f-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-216">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="da49f-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-217">96</span><span class="sxs-lookup"><span data-stu-id="da49f-217">96</span></span>

<span data-ttu-id="da49f-218">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="da49f-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-219">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="da49f-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-220">97</span><span class="sxs-lookup"><span data-stu-id="da49f-220">97</span></span>

<span data-ttu-id="da49f-221">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="da49f-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-222">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="da49f-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-223">98</span><span class="sxs-lookup"><span data-stu-id="da49f-223">98</span></span>

<span data-ttu-id="da49f-224">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="da49f-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-225">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="da49f-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-226">100</span><span class="sxs-lookup"><span data-stu-id="da49f-226">100</span></span>

<span data-ttu-id="da49f-227">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="da49f-227">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="da49f-228">**Otros**</span><span class="sxs-lookup"><span data-stu-id="da49f-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="da49f-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="da49f-229">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da49f-230">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da49f-230">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="da49f-231">Si DHCP está habilitado en el sistema del equipo local, la opción deshabilita TCP/IP en este adaptador de red específico.</span><span class="sxs-lookup"><span data-stu-id="da49f-231">If DHCP is enabled on the local computer system, the option disables TCP/IP on this specific network adapter.</span></span> <span data-ttu-id="da49f-232">A menos que tenga una ruta de acceso alternativa al sistema de destino, es decir, a otro adaptador de red enlazado TCP/IP, se perderán todas las comunicaciones TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="da49f-232">Unless you have an alternate path to the target system, that is, another TCP/IP bound network adapter, all TCP/IP communications will be lost.</span></span>

 

## <a name="examples"></a><span data-ttu-id="da49f-233">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="da49f-233">Examples</span></span>

<span data-ttu-id="da49f-234">En el ejemplo [Release Renew IP Addressing Using PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell en la galería de TechNet se usa **ReleaseDHCPLease** para liberar y renovar una dirección IP.</span><span class="sxs-lookup"><span data-stu-id="da49f-234">The [Release Renew IP Adresses Using PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell example on TechNet Gallery uses **ReleaseDHCPLease** to release and renew an IP address.</span></span>

<span data-ttu-id="da49f-235">El siguiente código VBScript libera las concesiones DHCP para todos los adaptadores de red enlazados a TCP/IP en un equipo.</span><span class="sxs-lookup"><span data-stu-id="da49f-235">The following VBScript code releases the DHCP leases for all TCP/IP-bound network adapters on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colNetCards = objWMIService.ExecQuery _ 
    ("Select * From Win32_NetworkAdapterConfiguration Where IPEnabled = True") 
 
For Each objNetCard in colNetCards 
    objNetCard.ReleaseDHCPLease() 
Next 
```



## <a name="requirements"></a><span data-ttu-id="da49f-236">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da49f-236">Requirements</span></span>



| <span data-ttu-id="da49f-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="da49f-237">Requirement</span></span> | <span data-ttu-id="da49f-238">Value</span><span class="sxs-lookup"><span data-stu-id="da49f-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da49f-239">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da49f-239">Minimum supported client</span></span><br/> | <span data-ttu-id="da49f-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da49f-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da49f-241">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da49f-241">Minimum supported server</span></span><br/> | <span data-ttu-id="da49f-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da49f-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da49f-243">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="da49f-243">Namespace</span></span><br/>                | <span data-ttu-id="da49f-244">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="da49f-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="da49f-245">MOF</span><span class="sxs-lookup"><span data-stu-id="da49f-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da49f-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da49f-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="da49f-247">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="da49f-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da49f-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da49f-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da49f-249">Vea también</span><span class="sxs-lookup"><span data-stu-id="da49f-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da49f-250">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="da49f-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="da49f-251">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="da49f-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="da49f-252">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="da49f-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="da49f-253">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="da49f-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="da49f-254">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="da49f-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

