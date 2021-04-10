---
description: El método estático de la clase WMI SetTcpWindowSize se usa para establecer el tamaño máximo de la ventana de recepción de TCP ofrecido por el sistema.
ms.assetid: c108fd9c-6de4-4f3e-9691-b0b5c1a3dc5f
ms.tgt_platform: multiple
title: Método SetTcpWindowSize de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpWindowSize
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d4a77acdc81c06d1f78da8bbc0160bd0d21bcfd8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153114"
---
# <a name="settcpwindowsize-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="21b62-103">Método SetTcpWindowSize de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="21b62-103">SetTcpWindowSize method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="21b62-104">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetTcpWindowSize** se usa para establecer el tamaño máximo de la ventana de recepción de TCP ofrecido por el sistema.</span><span class="sxs-lookup"><span data-stu-id="21b62-104">The **SetTcpWindowSize** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the maximum TCP Receive Window size offered by the system.</span></span>

<span data-ttu-id="21b62-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="21b62-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="21b62-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="21b62-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="21b62-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21b62-107">Syntax</span></span>


```mof
uint32 SetTcpWindowSize(
  [in] uint16 TcpWindowSize
);
```



## <a name="parameters"></a><span data-ttu-id="21b62-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21b62-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21b62-109">*TcpWindowSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21b62-109">*TcpWindowSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21b62-110">Tamaño máximo de la ventana de recepción de TCP ofrecido por el sistema.</span><span class="sxs-lookup"><span data-stu-id="21b62-110">Maximum TCP receive window size offered by the system.</span></span> <span data-ttu-id="21b62-111">El intervalo válido de valores en bytes es 0-65535.</span><span class="sxs-lookup"><span data-stu-id="21b62-111">The valid range of values in bytes is 0 - 65535.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21b62-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21b62-112">Return value</span></span>

<span data-ttu-id="21b62-113">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="21b62-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="21b62-114">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="21b62-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="21b62-115">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="21b62-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="21b62-116">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="21b62-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-117">0</span><span class="sxs-lookup"><span data-stu-id="21b62-117">0</span></span>

<span data-ttu-id="21b62-118">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="21b62-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-119">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="21b62-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-120">1</span><span class="sxs-lookup"><span data-stu-id="21b62-120">1</span></span>

<span data-ttu-id="21b62-121">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="21b62-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-122">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="21b62-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-123">64</span><span class="sxs-lookup"><span data-stu-id="21b62-123">64</span></span>

<span data-ttu-id="21b62-124">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="21b62-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-125">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="21b62-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-126">65</span><span class="sxs-lookup"><span data-stu-id="21b62-126">65</span></span>

<span data-ttu-id="21b62-127">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="21b62-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-128">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="21b62-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-129">66</span><span class="sxs-lookup"><span data-stu-id="21b62-129">66</span></span>

<span data-ttu-id="21b62-130">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="21b62-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-131">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="21b62-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-132">67</span><span class="sxs-lookup"><span data-stu-id="21b62-132">67</span></span>

<span data-ttu-id="21b62-133">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="21b62-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-134">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="21b62-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-135">68</span><span class="sxs-lookup"><span data-stu-id="21b62-135">68</span></span>

<span data-ttu-id="21b62-136">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="21b62-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-137">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="21b62-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-138">69</span><span class="sxs-lookup"><span data-stu-id="21b62-138">69</span></span>

<span data-ttu-id="21b62-139">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="21b62-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-140">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="21b62-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-141">70</span><span class="sxs-lookup"><span data-stu-id="21b62-141">70</span></span>

<span data-ttu-id="21b62-142">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="21b62-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-143">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="21b62-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-144">71</span><span class="sxs-lookup"><span data-stu-id="21b62-144">71</span></span>

<span data-ttu-id="21b62-145">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="21b62-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-146">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="21b62-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-147">72</span><span class="sxs-lookup"><span data-stu-id="21b62-147">72</span></span>

<span data-ttu-id="21b62-148">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="21b62-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-149">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="21b62-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-150">73</span><span class="sxs-lookup"><span data-stu-id="21b62-150">73</span></span>

<span data-ttu-id="21b62-151">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="21b62-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-152">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="21b62-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-153">74</span><span class="sxs-lookup"><span data-stu-id="21b62-153">74</span></span>

<span data-ttu-id="21b62-154">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="21b62-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-155">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="21b62-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-156">75</span><span class="sxs-lookup"><span data-stu-id="21b62-156">75</span></span>

<span data-ttu-id="21b62-157">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="21b62-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-158">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="21b62-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-159">76</span><span class="sxs-lookup"><span data-stu-id="21b62-159">76</span></span>

<span data-ttu-id="21b62-160">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="21b62-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-161">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="21b62-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-162">77</span><span class="sxs-lookup"><span data-stu-id="21b62-162">77</span></span>

<span data-ttu-id="21b62-163">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="21b62-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-164">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="21b62-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-165">78</span><span class="sxs-lookup"><span data-stu-id="21b62-165">78</span></span>

<span data-ttu-id="21b62-166">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="21b62-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-167">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="21b62-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-168">79</span><span class="sxs-lookup"><span data-stu-id="21b62-168">79</span></span>

<span data-ttu-id="21b62-169">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="21b62-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-170">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="21b62-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-171">80</span><span class="sxs-lookup"><span data-stu-id="21b62-171">80</span></span>

<span data-ttu-id="21b62-172">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="21b62-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-173">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="21b62-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-174">81</span><span class="sxs-lookup"><span data-stu-id="21b62-174">81</span></span>

<span data-ttu-id="21b62-175">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="21b62-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-176">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="21b62-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-177">82</span><span class="sxs-lookup"><span data-stu-id="21b62-177">82</span></span>

<span data-ttu-id="21b62-178">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="21b62-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-179">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="21b62-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-180">83</span><span class="sxs-lookup"><span data-stu-id="21b62-180">83</span></span>

<span data-ttu-id="21b62-181">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="21b62-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-182">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="21b62-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-183">84</span><span class="sxs-lookup"><span data-stu-id="21b62-183">84</span></span>

<span data-ttu-id="21b62-184">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="21b62-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-185">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="21b62-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-186">85</span><span class="sxs-lookup"><span data-stu-id="21b62-186">85</span></span>

<span data-ttu-id="21b62-187">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="21b62-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-188">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="21b62-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-189">86</span><span class="sxs-lookup"><span data-stu-id="21b62-189">86</span></span>

<span data-ttu-id="21b62-190">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="21b62-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-191">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="21b62-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-192">87</span><span class="sxs-lookup"><span data-stu-id="21b62-192">87</span></span>

<span data-ttu-id="21b62-193">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="21b62-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-194">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="21b62-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-195">88</span><span class="sxs-lookup"><span data-stu-id="21b62-195">88</span></span>

<span data-ttu-id="21b62-196">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="21b62-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-197">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="21b62-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-198">89</span><span class="sxs-lookup"><span data-stu-id="21b62-198">89</span></span>

<span data-ttu-id="21b62-199">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="21b62-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-200">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="21b62-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-201">90</span><span class="sxs-lookup"><span data-stu-id="21b62-201">90</span></span>

<span data-ttu-id="21b62-202">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="21b62-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-203">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="21b62-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-204">91</span><span class="sxs-lookup"><span data-stu-id="21b62-204">91</span></span>

<span data-ttu-id="21b62-205">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="21b62-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-206">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="21b62-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-207">92</span><span class="sxs-lookup"><span data-stu-id="21b62-207">92</span></span>

<span data-ttu-id="21b62-208">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="21b62-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-209">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="21b62-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-210">93</span><span class="sxs-lookup"><span data-stu-id="21b62-210">93</span></span>

<span data-ttu-id="21b62-211">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="21b62-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-212">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="21b62-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-213">94</span><span class="sxs-lookup"><span data-stu-id="21b62-213">94</span></span>

<span data-ttu-id="21b62-214">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="21b62-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-215">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="21b62-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-216">95</span><span class="sxs-lookup"><span data-stu-id="21b62-216">95</span></span>

<span data-ttu-id="21b62-217">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="21b62-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-218">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="21b62-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-219">96</span><span class="sxs-lookup"><span data-stu-id="21b62-219">96</span></span>

<span data-ttu-id="21b62-220">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="21b62-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-221">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="21b62-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-222">97</span><span class="sxs-lookup"><span data-stu-id="21b62-222">97</span></span>

<span data-ttu-id="21b62-223">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="21b62-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-224">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="21b62-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-225">98</span><span class="sxs-lookup"><span data-stu-id="21b62-225">98</span></span>

<span data-ttu-id="21b62-226">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="21b62-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-227">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="21b62-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-228">100</span><span class="sxs-lookup"><span data-stu-id="21b62-228">100</span></span>

<span data-ttu-id="21b62-229">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="21b62-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="21b62-230">**Otros**</span><span class="sxs-lookup"><span data-stu-id="21b62-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="21b62-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="21b62-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21b62-232">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21b62-232">Remarks</span></span>

<span data-ttu-id="21b62-233">La ventana de recepción determina el número de bytes que un remitente puede transmitir sin recibir una confirmación.</span><span class="sxs-lookup"><span data-stu-id="21b62-233">The receive window specifies the number of bytes a sender can transmit without receiving an acknowledgment.</span></span> <span data-ttu-id="21b62-234">En general, las ventanas de recepción de mayor tamaño mejoran el rendimiento en redes de alto retraso y ancho de banda alto.</span><span class="sxs-lookup"><span data-stu-id="21b62-234">In general, larger receive windows improve performance over high-delay and high-bandwidth networks.</span></span> <span data-ttu-id="21b62-235">Por motivos de eficacia, la ventana de recepción debe ser un múltiplo par del tamaño máximo de segmento (MSS) de TCP.</span><span class="sxs-lookup"><span data-stu-id="21b62-235">For efficiency, the receive window should be an even multiple of the TCP Maximum Segment Size (MSS).</span></span>

> [!Note]  
> <span data-ttu-id="21b62-236">Windows Vista: este método obtiene acceso a la `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` entrada del registro, que no se usa en la implementación actual del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="21b62-236">Windows Vista: This method accesses the `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` registry entry, which is not used in the current implementation of the operating system.</span></span>

 

## <a name="examples"></a><span data-ttu-id="21b62-237">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="21b62-237">Examples</span></span>

<span data-ttu-id="21b62-238">El ejemplo [modificar el tamaño de la ventana TCP para todos los adaptadores de red de](https://Gallery.TechNet.Microsoft.Com/74cf7be0-0044-4a88-85a3-9bc98490897b) VBScript establece el tamaño de la ventana TCP para todos los adaptadores de red de un equipo.</span><span class="sxs-lookup"><span data-stu-id="21b62-238">The [Modify the TCP Window Size for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/74cf7be0-0044-4a88-85a3-9bc98490897b) VBScript sample sets the TCP window size for all network adapters on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="21b62-239">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21b62-239">Requirements</span></span>



| <span data-ttu-id="21b62-240">Requisito</span><span class="sxs-lookup"><span data-stu-id="21b62-240">Requirement</span></span> | <span data-ttu-id="21b62-241">Value</span><span class="sxs-lookup"><span data-stu-id="21b62-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21b62-242">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21b62-242">Minimum supported client</span></span><br/> | <span data-ttu-id="21b62-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21b62-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="21b62-244">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21b62-244">Minimum supported server</span></span><br/> | <span data-ttu-id="21b62-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21b62-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="21b62-246">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="21b62-246">End of client support</span></span><br/>    | <span data-ttu-id="21b62-247">Windows 7</span><span class="sxs-lookup"><span data-stu-id="21b62-247">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="21b62-248">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="21b62-248">End of server support</span></span><br/>    | <span data-ttu-id="21b62-249">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21b62-249">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="21b62-250">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="21b62-250">Namespace</span></span><br/>                | <span data-ttu-id="21b62-251">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="21b62-251">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="21b62-252">MOF</span><span class="sxs-lookup"><span data-stu-id="21b62-252">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21b62-253"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="21b62-253"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="21b62-254">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="21b62-254">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21b62-255"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21b62-255"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21b62-256">Vea también</span><span class="sxs-lookup"><span data-stu-id="21b62-256">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21b62-257">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="21b62-257">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="21b62-258">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="21b62-258">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="21b62-259">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="21b62-259">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="21b62-260">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="21b62-260">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="21b62-261">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="21b62-261">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

