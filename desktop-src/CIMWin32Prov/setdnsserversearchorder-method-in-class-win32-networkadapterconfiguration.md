---
description: SetDNSServerSearchOrder &\# 32; El método de clase WMI utiliza una matriz de elementos de cadena para establecer el orden de búsqueda de servidores.
ms.assetid: fce688fa-7264-4965-8e1c-138160e03a7e
ms.tgt_platform: multiple
title: Método SetDNSServerSearchOrder de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSServerSearchOrder
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2bfe731ea1d89e8e0ad702bfa229a61fba30dfc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080236"
---
# <a name="setdnsserversearchorder-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="cb9d2-103">Método SetDNSServerSearchOrder de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="cb9d2-103">SetDNSServerSearchOrder method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="cb9d2-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDNSServerSearchOrder** utiliza una matriz de elementos de cadena para establecer el orden de búsqueda de servidores.</span><span class="sxs-lookup"><span data-stu-id="cb9d2-104">The **SetDNSServerSearchOrder** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uses an array of string elements to set the server search order.</span></span>

<span data-ttu-id="cb9d2-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="cb9d2-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cb9d2-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cb9d2-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cb9d2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb9d2-107">Syntax</span></span>


```mof
uint32 SetDNSServerSearchOrder(
  [in] string DNSServerSearchOrder[]
);
```



## <a name="parameters"></a><span data-ttu-id="cb9d2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb9d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb9d2-109">*DNSServerSearchOrder* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb9d2-109">*DNSServerSearchOrder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb9d2-110">Lista de direcciones IP de servidor para consultar los servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="cb9d2-110">List of server IP addresses to query for DNS servers.</span></span>

<span data-ttu-id="cb9d2-111">Ejemplo: 130.215.24.1 o 157.54.164.1</span><span class="sxs-lookup"><span data-stu-id="cb9d2-111">Example: 130.215.24.1 or 157.54.164.1</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb9d2-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb9d2-112">Return value</span></span>

<span data-ttu-id="cb9d2-113">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="cb9d2-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="cb9d2-114">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="cb9d2-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="cb9d2-115">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="cb9d2-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="cb9d2-116">**Finalización correcta, no es necesario reiniciar** (0)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-116">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-117">**Finalización correcta, se requiere un reinicio** (1)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-117">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-118">**Método no admitido en esta plataforma** (64)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-118">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-119">**Error desconocido** (65)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-119">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-120">**Máscara de subred no válida** (66)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-120">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-121">**Se produjo un error al procesar una instancia devuelta** (67)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-121">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-122">**Parámetro de entrada no válido** (68)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-122">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-123">Se **especificaron más de 5 puertas de enlace** (69)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-123">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-124">**Dirección IP no válida** (70)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-124">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-125">**Dirección IP de puerta de enlace no válida** (71)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-125">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-126">**Se produjo un error al obtener acceso al registro para obtener la información solicitada** (72)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-126">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-127">**Nombre de dominio no válido** (73)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-127">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-128">**Nombre de host no válido** (74)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-128">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-129">**No se definió ningún servidor WINS principal/secundario** (75)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-129">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-130">**Archivo no válido** (76)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-130">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-131">**Ruta de acceso del sistema no válida** (77)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-131">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-132">**No se pudo copiar el archivo** (78)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-132">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-133">**Parámetro de seguridad no válido** (79)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-133">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-134">**No se puede configurar el servicio TCP/IP** (80)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-134">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-135">**No se puede configurar el servicio DHCP** (81)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-135">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-136">**No se puede renovar la concesión DHCP** (82)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-136">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-137">**No se puede liberar la concesión DHCP** (83)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-137">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-138">**IP no habilitada en el adaptador** (84)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-138">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-139">**IPX no habilitado en el adaptador** (85)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-139">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-140">**Error de límite de número de trama/red** (86)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-140">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-141">**Tipo de marco no válido** (87)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-141">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-142">**Número de red no válido** (88)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-142">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-143">**Número de red duplicada** (89)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-143">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-144">**Parámetro fuera de los límites** (90)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-144">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-145">**Acceso denegado** (91)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-145">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-146">**Memoria insuficiente** (92)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-146">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-147">**Ya existe** (93)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-147">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-148">**Ruta de acceso, archivo u objeto no encontrado** (94)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-148">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-149">**No se puede notificar al servicio** (95)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-149">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-150">**No se puede notificar al servicio DNS** (96)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-150">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-151">**Interfaz no configurable** (97)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-151">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-152">**No todas las concesiones DHCP se pueden liberar o renovar** (98)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-152">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-153">**DHCP no está habilitado en el adaptador** (100)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-153">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="cb9d2-154">**Otro** (101 4294967295)</span><span class="sxs-lookup"><span data-stu-id="cb9d2-154">**Other** (101 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="cb9d2-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb9d2-155">Remarks</span></span>

<span data-ttu-id="cb9d2-156">Se trata de una llamada de método dependiente de la instancia que se aplica por cada adaptador.</span><span class="sxs-lookup"><span data-stu-id="cb9d2-156">This is an instance-dependent method call that applies on a per-adapter basis.</span></span> <span data-ttu-id="cb9d2-157">Una vez especificados los servidores DNS estáticos para empezar a usar el protocolo de configuración dinámica de host (DHCP) en lugar de los servidores DNS estáticos, puede llamar al método sin proporcionar parámetros "in".</span><span class="sxs-lookup"><span data-stu-id="cb9d2-157">After static DNS servers are specified to start using Dynamic Host Configuration Protocol (DHCP) instead of static DNS servers, you can call the method without supplying "in" parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="cb9d2-158">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cb9d2-158">Examples</span></span>

<span data-ttu-id="cb9d2-159">El ejemplo [establecer el orden de búsqueda de servidores DNS para varios equipos de una unidad organizativa](https://Gallery.TechNet.Microsoft.Com/Set-DNS-Server-Search-6a3e3ede) de VBScript en la galería de TechNet recupera o establece el orden de búsqueda del servidor DNS para varios equipos que pertenecen a una unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="cb9d2-159">The [Set DNS Server Search Order for Multiple Computers in an Organizational Unit](https://Gallery.TechNet.Microsoft.Com/Set-DNS-Server-Search-6a3e3ede) VBScript sample on TechNet Gallery retrieves or sets DNS Server search order for multiple computers that belongs to one organizational unit.</span></span>

<span data-ttu-id="cb9d2-160">En el ejemplo de VBScript [modificar el orden de búsqueda del servidor DNS para un adaptador de red](https://Gallery.TechNet.Microsoft.Com/7824348c-5a92-42cb-b4e9-ef2187702e02) se configura un adaptador de red enlazado a TCP/IP para usar dos servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="cb9d2-160">The [Modify the DNS Server Search Order for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/7824348c-5a92-42cb-b4e9-ef2187702e02) VBScript sample configures a TCP/IP-bound network adapter to use two DNS servers.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb9d2-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb9d2-161">Requirements</span></span>



| <span data-ttu-id="cb9d2-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb9d2-162">Requirement</span></span> | <span data-ttu-id="cb9d2-163">Value</span><span class="sxs-lookup"><span data-stu-id="cb9d2-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb9d2-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb9d2-164">Minimum supported client</span></span><br/> | <span data-ttu-id="cb9d2-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb9d2-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cb9d2-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb9d2-166">Minimum supported server</span></span><br/> | <span data-ttu-id="cb9d2-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb9d2-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cb9d2-168">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cb9d2-168">Namespace</span></span><br/>                | <span data-ttu-id="cb9d2-169">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cb9d2-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cb9d2-170">MOF</span><span class="sxs-lookup"><span data-stu-id="cb9d2-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb9d2-171"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb9d2-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb9d2-172">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cb9d2-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb9d2-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb9d2-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb9d2-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb9d2-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb9d2-175">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="cb9d2-175">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="cb9d2-176">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="cb9d2-176">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="cb9d2-177">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="cb9d2-177">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="cb9d2-178">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="cb9d2-178">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="cb9d2-179">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="cb9d2-179">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

