---
description: El método estático de la clase WMI SetIGMPLevel se usa para establecer la medida en la que el sistema admite la multidifusión IP y participa en el protocolo de administración de grupos de Internet.
ms.assetid: 38877576-aa23-4841-b3ae-1a02bfdd70d8
ms.tgt_platform: multiple
title: Método SetIGMPLevel de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIGMPLevel
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 97ead4df1d45b110c3d0a91976dc8eca6ffd72c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538992"
---
# <a name="setigmplevel-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="53587-103">Método SetIGMPLevel de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="53587-103">SetIGMPLevel method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="53587-104">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetIGMPLevel** se usa para establecer la medida en la que el sistema admite la multidifusión IP y participa en el protocolo de administración de grupos de Internet.</span><span class="sxs-lookup"><span data-stu-id="53587-104">The **SetIGMPLevel** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the extent to which the system supports IP multicasting and participates in the Internet Group Management Protocol.</span></span>

<span data-ttu-id="53587-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="53587-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="53587-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="53587-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="53587-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53587-107">Syntax</span></span>


```mof
uint32 SetIGMPLevel(
  [in] uint8 IGMPLevel
);
```



## <a name="parameters"></a><span data-ttu-id="53587-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53587-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53587-109">*IGMPLevel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="53587-109">*IGMPLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53587-110">Tipo de datos: **entero**</span><span class="sxs-lookup"><span data-stu-id="53587-110">Data type: **Integer**</span></span>

<span data-ttu-id="53587-111">Establece el nivel en el que el sistema admite la multidifusión IP y participa en el protocolo de administración de grupos de Internet.</span><span class="sxs-lookup"><span data-stu-id="53587-111">Sets the level at which the system supports IP multicast and participates in the Internet Group Management Protocol.</span></span> <span data-ttu-id="53587-112">En el nivel 0, el sistema no proporciona compatibilidad con multidifusión.</span><span class="sxs-lookup"><span data-stu-id="53587-112">At level 0, the system provides no multicast support.</span></span> <span data-ttu-id="53587-113">En el nivel 1, el sistema solo puede enviar paquetes de multidifusión IP.</span><span class="sxs-lookup"><span data-stu-id="53587-113">At level 1, the system may only send IP multicast packets.</span></span> <span data-ttu-id="53587-114">En el nivel 2, el sistema puede enviar paquetes de multidifusión IP y participar por completo en IGMP para recibir paquetes de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="53587-114">At level 2, the system may send IP multicast packets and fully participate in IGMP to receive multicast packets.</span></span>

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span data-ttu-id="53587-115">**Sin multidifusión** (0)</span><span class="sxs-lookup"><span data-stu-id="53587-115">**No Multicast** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span data-ttu-id="53587-116">**Multidifusión IP** (1)</span><span class="sxs-lookup"><span data-stu-id="53587-116">**IP Multicast** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span data-ttu-id="53587-117">**IP & multidifusión IGMP** (2)</span><span class="sxs-lookup"><span data-stu-id="53587-117">**IP & IGMP multicast** (2)</span></span>


<span data-ttu-id="53587-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="53587-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="53587-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53587-119">Return value</span></span>

<span data-ttu-id="53587-120">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="53587-120">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="53587-121">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="53587-121">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="53587-122">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="53587-122">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="53587-123">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="53587-123">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="53587-124">0</span><span class="sxs-lookup"><span data-stu-id="53587-124">0</span></span>

<span data-ttu-id="53587-125">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="53587-125">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="53587-126">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="53587-126">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="53587-127">1</span><span class="sxs-lookup"><span data-stu-id="53587-127">1</span></span>

<span data-ttu-id="53587-128">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="53587-128">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="53587-129">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="53587-129">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="53587-130">64</span><span class="sxs-lookup"><span data-stu-id="53587-130">64</span></span>

<span data-ttu-id="53587-131">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="53587-131">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="53587-132">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="53587-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="53587-133">65</span><span class="sxs-lookup"><span data-stu-id="53587-133">65</span></span>

<span data-ttu-id="53587-134">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="53587-134">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="53587-135">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="53587-135">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="53587-136">66</span><span class="sxs-lookup"><span data-stu-id="53587-136">66</span></span>

<span data-ttu-id="53587-137">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="53587-137">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="53587-138">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="53587-138">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="53587-139">67</span><span class="sxs-lookup"><span data-stu-id="53587-139">67</span></span>

<span data-ttu-id="53587-140">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="53587-140">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="53587-141">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="53587-141">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="53587-142">68</span><span class="sxs-lookup"><span data-stu-id="53587-142">68</span></span>

<span data-ttu-id="53587-143">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="53587-143">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="53587-144">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="53587-144">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="53587-145">69</span><span class="sxs-lookup"><span data-stu-id="53587-145">69</span></span>

<span data-ttu-id="53587-146">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="53587-146">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="53587-147">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="53587-147">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="53587-148">70</span><span class="sxs-lookup"><span data-stu-id="53587-148">70</span></span>

<span data-ttu-id="53587-149">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="53587-149">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="53587-150">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="53587-150">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="53587-151">71</span><span class="sxs-lookup"><span data-stu-id="53587-151">71</span></span>

<span data-ttu-id="53587-152">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="53587-152">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="53587-153">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="53587-153">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="53587-154">72</span><span class="sxs-lookup"><span data-stu-id="53587-154">72</span></span>

<span data-ttu-id="53587-155">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="53587-155">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="53587-156">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="53587-156">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="53587-157">73</span><span class="sxs-lookup"><span data-stu-id="53587-157">73</span></span>

<span data-ttu-id="53587-158">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="53587-158">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="53587-159">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="53587-159">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="53587-160">74</span><span class="sxs-lookup"><span data-stu-id="53587-160">74</span></span>

<span data-ttu-id="53587-161">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="53587-161">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="53587-162">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="53587-162">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="53587-163">75</span><span class="sxs-lookup"><span data-stu-id="53587-163">75</span></span>

<span data-ttu-id="53587-164">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="53587-164">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="53587-165">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="53587-165">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="53587-166">76</span><span class="sxs-lookup"><span data-stu-id="53587-166">76</span></span>

<span data-ttu-id="53587-167">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="53587-167">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="53587-168">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="53587-168">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="53587-169">77</span><span class="sxs-lookup"><span data-stu-id="53587-169">77</span></span>

<span data-ttu-id="53587-170">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="53587-170">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="53587-171">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="53587-171">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="53587-172">78</span><span class="sxs-lookup"><span data-stu-id="53587-172">78</span></span>

<span data-ttu-id="53587-173">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="53587-173">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="53587-174">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="53587-174">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="53587-175">79</span><span class="sxs-lookup"><span data-stu-id="53587-175">79</span></span>

<span data-ttu-id="53587-176">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="53587-176">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="53587-177">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="53587-177">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="53587-178">80</span><span class="sxs-lookup"><span data-stu-id="53587-178">80</span></span>

<span data-ttu-id="53587-179">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="53587-179">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="53587-180">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="53587-180">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="53587-181">81</span><span class="sxs-lookup"><span data-stu-id="53587-181">81</span></span>

<span data-ttu-id="53587-182">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="53587-182">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="53587-183">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="53587-183">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="53587-184">82</span><span class="sxs-lookup"><span data-stu-id="53587-184">82</span></span>

<span data-ttu-id="53587-185">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="53587-185">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="53587-186">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="53587-186">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="53587-187">83</span><span class="sxs-lookup"><span data-stu-id="53587-187">83</span></span>

<span data-ttu-id="53587-188">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="53587-188">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="53587-189">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="53587-189">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="53587-190">84</span><span class="sxs-lookup"><span data-stu-id="53587-190">84</span></span>

<span data-ttu-id="53587-191">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="53587-191">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="53587-192">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="53587-192">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="53587-193">85</span><span class="sxs-lookup"><span data-stu-id="53587-193">85</span></span>

<span data-ttu-id="53587-194">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="53587-194">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="53587-195">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="53587-195">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="53587-196">86</span><span class="sxs-lookup"><span data-stu-id="53587-196">86</span></span>

<span data-ttu-id="53587-197">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="53587-197">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="53587-198">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="53587-198">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="53587-199">87</span><span class="sxs-lookup"><span data-stu-id="53587-199">87</span></span>

<span data-ttu-id="53587-200">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="53587-200">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="53587-201">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="53587-201">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="53587-202">88</span><span class="sxs-lookup"><span data-stu-id="53587-202">88</span></span>

<span data-ttu-id="53587-203">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="53587-203">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="53587-204">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="53587-204">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="53587-205">89</span><span class="sxs-lookup"><span data-stu-id="53587-205">89</span></span>

<span data-ttu-id="53587-206">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="53587-206">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="53587-207">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="53587-207">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="53587-208">90</span><span class="sxs-lookup"><span data-stu-id="53587-208">90</span></span>

<span data-ttu-id="53587-209">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="53587-209">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="53587-210">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="53587-210">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="53587-211">91</span><span class="sxs-lookup"><span data-stu-id="53587-211">91</span></span>

<span data-ttu-id="53587-212">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="53587-212">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="53587-213">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="53587-213">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="53587-214">92</span><span class="sxs-lookup"><span data-stu-id="53587-214">92</span></span>

<span data-ttu-id="53587-215">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="53587-215">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="53587-216">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="53587-216">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="53587-217">93</span><span class="sxs-lookup"><span data-stu-id="53587-217">93</span></span>

<span data-ttu-id="53587-218">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="53587-218">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="53587-219">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="53587-219">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="53587-220">94</span><span class="sxs-lookup"><span data-stu-id="53587-220">94</span></span>

<span data-ttu-id="53587-221">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="53587-221">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="53587-222">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="53587-222">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="53587-223">95</span><span class="sxs-lookup"><span data-stu-id="53587-223">95</span></span>

<span data-ttu-id="53587-224">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="53587-224">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="53587-225">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="53587-225">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="53587-226">96</span><span class="sxs-lookup"><span data-stu-id="53587-226">96</span></span>

<span data-ttu-id="53587-227">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="53587-227">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="53587-228">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="53587-228">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="53587-229">97</span><span class="sxs-lookup"><span data-stu-id="53587-229">97</span></span>

<span data-ttu-id="53587-230">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="53587-230">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="53587-231">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="53587-231">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="53587-232">98</span><span class="sxs-lookup"><span data-stu-id="53587-232">98</span></span>

<span data-ttu-id="53587-233">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="53587-233">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="53587-234">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="53587-234">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="53587-235">100</span><span class="sxs-lookup"><span data-stu-id="53587-235">100</span></span>

<span data-ttu-id="53587-236">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="53587-236">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="53587-237">**Otros**</span><span class="sxs-lookup"><span data-stu-id="53587-237">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="53587-238">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="53587-238">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="53587-239">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="53587-239">Examples</span></span>

<span data-ttu-id="53587-240">El ejemplo de VBScript [Modify the IGMP LEVEL for All Network adapters deshabilita la](https://Gallery.TechNet.Microsoft.Com/b92f894c-5cf8-4484-b5f0-d54761bacd5c) multidifusión IGMP en un equipo.</span><span class="sxs-lookup"><span data-stu-id="53587-240">The [Modify the IGMP Level for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/b92f894c-5cf8-4484-b5f0-d54761bacd5c) VBScript sample disables IGMP multicasting on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="53587-241">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53587-241">Requirements</span></span>



| <span data-ttu-id="53587-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="53587-242">Requirement</span></span> | <span data-ttu-id="53587-243">Value</span><span class="sxs-lookup"><span data-stu-id="53587-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53587-244">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53587-244">Minimum supported client</span></span><br/> | <span data-ttu-id="53587-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53587-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="53587-246">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53587-246">Minimum supported server</span></span><br/> | <span data-ttu-id="53587-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53587-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="53587-248">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="53587-248">Namespace</span></span><br/>                | <span data-ttu-id="53587-249">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="53587-249">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="53587-250">MOF</span><span class="sxs-lookup"><span data-stu-id="53587-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53587-251"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53587-251"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="53587-252">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="53587-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53587-253"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53587-253"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53587-254">Vea también</span><span class="sxs-lookup"><span data-stu-id="53587-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53587-255">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="53587-255">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="53587-256">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="53587-256">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="53587-257">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="53587-257">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="53587-258">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="53587-258">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="53587-259">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="53587-259">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

