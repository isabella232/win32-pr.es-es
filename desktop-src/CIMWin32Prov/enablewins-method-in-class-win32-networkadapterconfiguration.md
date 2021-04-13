---
description: EnableWINS &\# 32; El método estático de clase WMI habilita la configuración de Windows Internet Naming Service (WINS) específica de TCP/IP, pero es independiente del adaptador de red.
ms.assetid: ce0fb170-978f-4d70-bced-e530e43da719
ms.tgt_platform: multiple
title: Método EnableWINS de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableWINS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 77f5ba32606ff228908e8b7a1559a73ae5139e9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538692"
---
# <a name="enablewins-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="8123b-103">Método EnableWINS de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="8123b-103">EnableWINS method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="8123b-104">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableWINS** habilita la configuración de Windows Internet Naming Service (WINS) específica de TCP/IP, pero es independiente del adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="8123b-104">The **EnableWINS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method enables Windows Internet Naming Service (WINS) settings specific to TCP/IP, but independent of the network adapter.</span></span>

<span data-ttu-id="8123b-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="8123b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8123b-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8123b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8123b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8123b-107">Syntax</span></span>


```mof
uint32 EnableWINS(
  [in]           boolean DNSEnabledForWINSResolution,
  [in]           boolean WINSEnableLMHostsLookup,
  [in, optional] string  WINSHostLookupFile,
  [in, optional] string  WINSScopeID
);
```



## <a name="parameters"></a><span data-ttu-id="8123b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8123b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8123b-109">*DNSEnabledForWINSResolution* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8123b-109">*DNSEnabledForWINSResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8123b-110">Si es **true**, el sistema de nombres de dominio (DNS) está habilitado para la resolución de nombres a través de la resolución de WINS.</span><span class="sxs-lookup"><span data-stu-id="8123b-110">If **true**, the Domain Name System (DNS) is enabled for name resolution over WINS resolution.</span></span>

</dd> <dt>

<span data-ttu-id="8123b-111">*WINSEnableLMHostsLookup* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8123b-111">*WINSEnableLMHostsLookup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8123b-112">Si **es true**, se usan los archivos de búsqueda local.</span><span class="sxs-lookup"><span data-stu-id="8123b-112">If **true**, local lookup files are used.</span></span> <span data-ttu-id="8123b-113">Los archivos de búsqueda contendrán las asignaciones de direcciones IP a los nombres de host.</span><span class="sxs-lookup"><span data-stu-id="8123b-113">Lookup files will contain mappings of IP addresses to host names.</span></span>

</dd> <dt>

<span data-ttu-id="8123b-114">*WINSHostLookupFile* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8123b-114">*WINSHostLookupFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8123b-115">Archivos de búsqueda que contienen asignaciones de direcciones IP a nombres de host.</span><span class="sxs-lookup"><span data-stu-id="8123b-115">Lookup files that contain mappings of IP addresses to host names.</span></span> <span data-ttu-id="8123b-116">Si está disponible, los archivos se encuentran en% SystemRoot% \\ system32 \\ drivers \\ .</span><span class="sxs-lookup"><span data-stu-id="8123b-116">If available, the files will be found in %SystemRoot%\\system32\\drivers\\ .</span></span>

</dd> <dt>

<span data-ttu-id="8123b-117">*WINSScopeID* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8123b-117">*WINSScopeID* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8123b-118">Valor del identificador de ámbito que se anexará al final del nombre NetBIOS del equipo.</span><span class="sxs-lookup"><span data-stu-id="8123b-118">Scope identifier value that will be appended to the end of the computer's NetBIOS name.</span></span> <span data-ttu-id="8123b-119">Los sistemas que utilizan el mismo identificador de ámbito pueden comunicarse con este equipo.</span><span class="sxs-lookup"><span data-stu-id="8123b-119">Systems that use the same scope identifier can communicate with this computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8123b-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8123b-120">Return value</span></span>

<span data-ttu-id="8123b-121">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere ningún reinicio; 1 (uno) para una finalización correcta cuando se requiere un reinicio; un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="8123b-121">Returns a value of 0 (zero) for a successful completion when no reboot is required; 1 (one) for a successful completion when a reboot is required; a different number if there is an error.</span></span> <span data-ttu-id="8123b-122">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8123b-122">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8123b-123">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8123b-123">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8123b-124">**Finalización correcta, no es necesario reiniciar** (0)</span><span class="sxs-lookup"><span data-stu-id="8123b-124">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-125">**Finalización correcta, se requiere un reinicio** (1)</span><span class="sxs-lookup"><span data-stu-id="8123b-125">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-126">**Método no admitido en esta plataforma** (64)</span><span class="sxs-lookup"><span data-stu-id="8123b-126">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-127">**Error desconocido** (65)</span><span class="sxs-lookup"><span data-stu-id="8123b-127">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-128">**Máscara de subred no válida** (66)</span><span class="sxs-lookup"><span data-stu-id="8123b-128">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-129">**Se produjo un error al procesar una instancia devuelta** (67)</span><span class="sxs-lookup"><span data-stu-id="8123b-129">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-130">**Parámetro de entrada no válido** (68)</span><span class="sxs-lookup"><span data-stu-id="8123b-130">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-131">Se **especificaron más de 5 puertas de enlace** (69)</span><span class="sxs-lookup"><span data-stu-id="8123b-131">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-132">**Dirección IP no válida** (70)</span><span class="sxs-lookup"><span data-stu-id="8123b-132">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-133">**Dirección IP de puerta de enlace no válida** (71)</span><span class="sxs-lookup"><span data-stu-id="8123b-133">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-134">**Se produjo un error al obtener acceso al registro para obtener la información solicitada** (72)</span><span class="sxs-lookup"><span data-stu-id="8123b-134">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-135">**Nombre de dominio no válido** (73)</span><span class="sxs-lookup"><span data-stu-id="8123b-135">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-136">**Nombre de host no válido** (74)</span><span class="sxs-lookup"><span data-stu-id="8123b-136">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-137">**No se definió ningún servidor WINS principal/secundario** (75)</span><span class="sxs-lookup"><span data-stu-id="8123b-137">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-138">**Archivo no válido** (76)</span><span class="sxs-lookup"><span data-stu-id="8123b-138">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-139">**Ruta de acceso del sistema no válida** (77)</span><span class="sxs-lookup"><span data-stu-id="8123b-139">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-140">**No se pudo copiar el archivo** (78)</span><span class="sxs-lookup"><span data-stu-id="8123b-140">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-141">**Parámetro de seguridad no válido** (79)</span><span class="sxs-lookup"><span data-stu-id="8123b-141">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-142">**No se puede configurar el servicio TCP/IP** (80)</span><span class="sxs-lookup"><span data-stu-id="8123b-142">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-143">**No se puede configurar el servicio DHCP** (81)</span><span class="sxs-lookup"><span data-stu-id="8123b-143">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-144">**No se puede renovar la concesión DHCP** (82)</span><span class="sxs-lookup"><span data-stu-id="8123b-144">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-145">**No se puede liberar la concesión DHCP** (83)</span><span class="sxs-lookup"><span data-stu-id="8123b-145">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-146">**IP no habilitada en el adaptador** (84)</span><span class="sxs-lookup"><span data-stu-id="8123b-146">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-147">**IPX no habilitado en el adaptador** (85)</span><span class="sxs-lookup"><span data-stu-id="8123b-147">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-148">**Error de límite de número de trama/red** (86)</span><span class="sxs-lookup"><span data-stu-id="8123b-148">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-149">**Tipo de marco no válido** (87)</span><span class="sxs-lookup"><span data-stu-id="8123b-149">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-150">**Número de red no válido** (88)</span><span class="sxs-lookup"><span data-stu-id="8123b-150">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-151">**Número de red duplicada** (89)</span><span class="sxs-lookup"><span data-stu-id="8123b-151">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-152">**Parámetro fuera de los límites** (90)</span><span class="sxs-lookup"><span data-stu-id="8123b-152">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-153">**Acceso denegado** (91)</span><span class="sxs-lookup"><span data-stu-id="8123b-153">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-154">**Memoria insuficiente** (92)</span><span class="sxs-lookup"><span data-stu-id="8123b-154">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-155">**Ya existe** (93)</span><span class="sxs-lookup"><span data-stu-id="8123b-155">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-156">**Ruta de acceso, archivo u objeto no encontrado** (94)</span><span class="sxs-lookup"><span data-stu-id="8123b-156">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-157">**No se puede notificar al servicio** (95)</span><span class="sxs-lookup"><span data-stu-id="8123b-157">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-158">**No se puede notificar al servicio DNS** (96)</span><span class="sxs-lookup"><span data-stu-id="8123b-158">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-159">**Interfaz no configurable** (97)</span><span class="sxs-lookup"><span data-stu-id="8123b-159">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-160">**No todas las concesiones DHCP se pueden liberar o renovar** (98)</span><span class="sxs-lookup"><span data-stu-id="8123b-160">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-161">**DHCP no está habilitado en el adaptador** (100)</span><span class="sxs-lookup"><span data-stu-id="8123b-161">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="8123b-162">**Otro** (101 4294967295)</span><span class="sxs-lookup"><span data-stu-id="8123b-162">**Other** (101 4294967295)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="8123b-163">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8123b-163">Examples</span></span>

<span data-ttu-id="8123b-164">En el ejemplo de código de VBScript [enable WINS for All Network adapters](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) , en la galería de TechNet, se usa **ENABLEWINS** para habilitar WINS en todos los adaptadores de red instalados en un equipo.</span><span class="sxs-lookup"><span data-stu-id="8123b-164">The [Enable WINS for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) VBScript code sample, on TechNet Gallery, uses **EnableWINS** to Enables WINS on all the network adapters installed in a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="8123b-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8123b-165">Requirements</span></span>



| <span data-ttu-id="8123b-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="8123b-166">Requirement</span></span> | <span data-ttu-id="8123b-167">Value</span><span class="sxs-lookup"><span data-stu-id="8123b-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8123b-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8123b-168">Minimum supported client</span></span><br/> | <span data-ttu-id="8123b-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8123b-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8123b-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8123b-170">Minimum supported server</span></span><br/> | <span data-ttu-id="8123b-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8123b-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8123b-172">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8123b-172">Namespace</span></span><br/>                | <span data-ttu-id="8123b-173">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8123b-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8123b-174">MOF</span><span class="sxs-lookup"><span data-stu-id="8123b-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8123b-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8123b-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8123b-176">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8123b-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8123b-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8123b-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8123b-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="8123b-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8123b-179">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="8123b-179">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="8123b-180">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="8123b-180">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="8123b-181">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="8123b-181">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="8123b-182">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="8123b-182">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="8123b-183">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="8123b-183">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

