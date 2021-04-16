---
description: Si se produce un error, WMI devuelve un código de error como un valor HRESULT. Estos códigos pueden ser devueltos por scripts, aplicaciones de C++ o WMIC.
ms.assetid: b560f37c-da22-4745-8d1f-b27afdf572ec
ms.tgt_platform: multiple
title: Constantes de error de WMI (WbemCli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95db7220bdc9669716dbe19f5bf2f4e139dfe5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715707"
---
# <a name="wmi-error-constants"></a><span data-ttu-id="87ddf-104">Constantes de error de WMI</span><span class="sxs-lookup"><span data-stu-id="87ddf-104">WMI Error Constants</span></span>

<span data-ttu-id="87ddf-105">Si se produce un error, WMI devuelve un código de error como un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="87ddf-105">If an error occurs, WMI returns an error code as an **HRESULT** value.</span></span> <span data-ttu-id="87ddf-106">Estos códigos pueden ser devueltos por scripts, aplicaciones de C++ o [**WMIC**](wmic.md).</span><span class="sxs-lookup"><span data-stu-id="87ddf-106">These codes may be returned by scripts, C++ applications, or [**Wmic**](wmic.md).</span></span>

> [!Note]
>
> <span data-ttu-id="87ddf-107">La siguiente documentación está dirigida a desarrolladores y administradores de ti.</span><span class="sxs-lookup"><span data-stu-id="87ddf-107">The following documentation is targeted for developers and IT administrators.</span></span> <span data-ttu-id="87ddf-108">Si es un usuario final que ha experimentado un mensaje de error relacionado con WMI, debe ir a [soporte técnico de Microsoft](https://support.microsoft.com/) y buscar el código de error que aparece en el mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="87ddf-108">If you are an end-user that has experienced an error message concerning WMI, you should go to [Microsoft Support](https://support.microsoft.com/) and search for the error code you see on the error message.</span></span> <span data-ttu-id="87ddf-109">Para obtener más información acerca de la solución de problemas con los scripts de WMI y el servicio WMI, vea el tema sobre [WMI no funciona](/previous-versions/tn-archive/ff406382(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="87ddf-109">For more information about troubleshooting problems with WMI scripts and the WMI service, see [WMI Isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10)).</span></span>
>
> <span data-ttu-id="87ddf-110">Si WMI devuelve mensajes de error, tenga en cuenta que es posible que no indiquen problemas en el servicio WMI o en los proveedores WMI.</span><span class="sxs-lookup"><span data-stu-id="87ddf-110">If WMI returns error messages, be aware that they may not indicate problems in the WMI service or in WMI providers.</span></span> <span data-ttu-id="87ddf-111">Los errores pueden originarse en otras partes del sistema operativo y surgir como errores a través de WMI.</span><span class="sxs-lookup"><span data-stu-id="87ddf-111">Failures can originate in other parts of the operating system and emerge as errors through WMI.</span></span> <span data-ttu-id="87ddf-112">En cualquier circunstancia, no elimine el repositorio WMI como primera acción, ya que la eliminación del repositorio puede provocar daños en el sistema o en las aplicaciones instaladas.</span><span class="sxs-lookup"><span data-stu-id="87ddf-112">Under any circumstances, do not delete the WMI repository as a first action because deleting the repository can cause damage to the system or to installed applications.</span></span>
>
> <span data-ttu-id="87ddf-113">Para obtener más información sobre el origen del problema, puede descargar y ejecutar la herramienta de línea de comandos de diagnóstico de [utilidad de diagnóstico de WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) .</span><span class="sxs-lookup"><span data-stu-id="87ddf-113">To obtain more information about the source of the problem, you can download and run the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic command line tool.</span></span> <span data-ttu-id="87ddf-114">Esta herramienta genera un informe que normalmente puede aislar el origen del problema y proporcionar instrucciones sobre cómo corregirlo.</span><span class="sxs-lookup"><span data-stu-id="87ddf-114">This tool produces a report that can usually isolate the source of the problem and provide instructions on how to fix it.</span></span> <span data-ttu-id="87ddf-115">El informe también ayuda a los servicios de soporte técnico de Microsoft para ayudarle.</span><span class="sxs-lookup"><span data-stu-id="87ddf-115">The report also aids Microsoft support services in assisting you.</span></span> <span data-ttu-id="87ddf-116">Puede descargar el Utilidad de diagnóstico de WMI [aquí](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span><span class="sxs-lookup"><span data-stu-id="87ddf-116">You can download the WMI Diagnosis Utility [here](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span></span>

 

<span data-ttu-id="87ddf-117">Algunos métodos de las clases WMI pueden devolver códigos de error del sistema y de la red (por ejemplo, 64).</span><span class="sxs-lookup"><span data-stu-id="87ddf-117">Some methods in WMI classes can return system and network error codes (64 for example).</span></span> <span data-ttu-id="87ddf-118">Puede comprobar la definición de estos tipos de códigos de error mediante el comando **net helpmsg** en la ventana del símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="87ddf-118">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="87ddf-119">Por ejemplo, el comando **net helpmsg 64** devuelve el mensaje: el nombre de red especificado ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="87ddf-119">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span>

<span data-ttu-id="87ddf-120">En la lista siguiente se enumeran algunos intervalos de errores comunes.</span><span class="sxs-lookup"><span data-stu-id="87ddf-120">The following list lists some common ranges of errors.</span></span>

<dl> <dt>

<span data-ttu-id="87ddf-121"><span id="0x80041068_-_0x80041099"></span><span id="0X80041068_-_0X80041099"></span>0x80041068 - 0x80041099</span><span class="sxs-lookup"><span data-stu-id="87ddf-121"><span id="0x80041068_-_0x80041099"></span><span id="0X80041068_-_0X80041099"></span>0x80041068 - 0x80041099</span></span>
</dt> <dd>

<span data-ttu-id="87ddf-122">Errores que se originan en WMI.</span><span class="sxs-lookup"><span data-stu-id="87ddf-122">Errors that originate in WMI itself.</span></span>

<span data-ttu-id="87ddf-123">Error en una operación específica de WMI debido a</span><span class="sxs-lookup"><span data-stu-id="87ddf-123">A specific WMI operation failed because of</span></span>

-   <span data-ttu-id="87ddf-124">Se produce un error en la solicitud, por ejemplo, una consulta WQL o la cuenta no tiene los permisos correctos.</span><span class="sxs-lookup"><span data-stu-id="87ddf-124">An error in the request, for example, a WQL query fails or the account does not have the correct permissions.</span></span>
-   <span data-ttu-id="87ddf-125">Un problema de infraestructura WMI, como un registro de CIM o DCOM incorrecto.</span><span class="sxs-lookup"><span data-stu-id="87ddf-125">A WMI infrastructure problem, such as incorrect CIM or DCOM registration.</span></span>

</dd> <dt>

<span data-ttu-id="87ddf-126"><span id="0x8007xxxx"></span><span id="0X8007XXXX"></span>0x8007xxxx</span><span class="sxs-lookup"><span data-stu-id="87ddf-126"><span id="0x8007xxxx"></span><span id="0X8007XXXX"></span>0x8007xxxx</span></span>
</dt> <dd>

<span data-ttu-id="87ddf-127">Errores que se originan en el sistema operativo principal.</span><span class="sxs-lookup"><span data-stu-id="87ddf-127">Errors originating in the core operating system.</span></span> <span data-ttu-id="87ddf-128">WMI puede devolver este tipo de error debido a un error externo, por ejemplo, un error de seguridad de DCOM.</span><span class="sxs-lookup"><span data-stu-id="87ddf-128">WMI may return this type of error because of an external failure, for example, DCOM security failure.</span></span>

</dd> <dt>

<span data-ttu-id="87ddf-129"><span id="0x80040xxx"></span><span id="0X80040XXX"></span>0x80040xxx</span><span class="sxs-lookup"><span data-stu-id="87ddf-129"><span id="0x80040xxx"></span><span id="0X80040XXX"></span>0x80040xxx</span></span>
</dt> <dd>

<span data-ttu-id="87ddf-130">Errores que se originan en DCOM.</span><span class="sxs-lookup"><span data-stu-id="87ddf-130">Errors originating in DCOM.</span></span> <span data-ttu-id="87ddf-131">Por ejemplo, la configuración de DCOM para las operaciones en un equipo remoto puede ser incorrecta.</span><span class="sxs-lookup"><span data-stu-id="87ddf-131">For example, the DCOM configuration for operations to a remote computer may be incorrect.</span></span>

</dd> <dt>

<span data-ttu-id="87ddf-132"><span id="0x8005xxxx"></span><span id="0X8005XXXX"></span>0x8005xxxx</span><span class="sxs-lookup"><span data-stu-id="87ddf-132"><span id="0x8005xxxx"></span><span id="0X8005XXXX"></span>0x8005xxxx</span></span>
</dt> <dd>

<span data-ttu-id="87ddf-133">Error que se origina en ADSI (interfaces de servicio Active Directory) o LDAP (Protocolo ligero de acceso a directorios), por ejemplo, un error de Active Directory de acceso al usar los proveedores de Active Directory WMI.</span><span class="sxs-lookup"><span data-stu-id="87ddf-133">Error originating from ADSI (Active Directory Service Interfaces) or LDAP (Lightweight Directory Access Protocol), for example, an Active Directory access failure when using the WMI Active Directory providers.</span></span>

</dd> </dl>

<span data-ttu-id="87ddf-134">Algunos métodos de las clases WMI pueden devolver códigos de error del sistema y de la red (por ejemplo, 64).</span><span class="sxs-lookup"><span data-stu-id="87ddf-134">Some methods in WMI classes can return system and network error codes (64 for example).</span></span> <span data-ttu-id="87ddf-135">Puede comprobar la definición de estos tipos de códigos de error mediante el comando **net helpmsg** en la ventana del símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="87ddf-135">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="87ddf-136">Por ejemplo, el comando **net helpmsg 64** devuelve el mensaje: el nombre de red especificado ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="87ddf-136">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span> <span data-ttu-id="87ddf-137">En C++, puede llamar a [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) y especificar **C: \\ Windows \\ system32 \\ WBEM \\wmiutils.dll** como el módulo de mensajes.</span><span class="sxs-lookup"><span data-stu-id="87ddf-137">In C++, you can call [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) and specify **C:\\Windows\\System32\\wbem\\wmiutils.dll** as the message module.</span></span>

<dl> <dt>

<span data-ttu-id="87ddf-138"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**error de WBEM \_ E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-138"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM\_E\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-139">2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="87ddf-139">2147749889 (0x80041001)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-140">Error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="87ddf-140">Call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-141"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="87ddf-141"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM\_E\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-142">2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="87ddf-142">2147749890 (0x80041002)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-143">No se encuentra el objeto.</span><span class="sxs-lookup"><span data-stu-id="87ddf-143">Object cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-144"><span id="WBEM_E_ACCESS_DENIED"></span><span id="wbem_e_access_denied"></span>**WBEM \_ E \_ acceso \_ denegado**</span><span class="sxs-lookup"><span data-stu-id="87ddf-144"><span id="WBEM_E_ACCESS_DENIED"></span><span id="wbem_e_access_denied"></span>**WBEM\_E\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-145">2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="87ddf-145">2147749891 (0x80041003)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-146">El usuario actual no tiene permiso para realizar la acción.</span><span class="sxs-lookup"><span data-stu-id="87ddf-146">Current user does not have permission to perform the action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-147"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**error del proveedor de WBEM \_ E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-147"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**WBEM\_E\_PROVIDER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-148">2147749892 (0x80041004)</span><span class="sxs-lookup"><span data-stu-id="87ddf-148">2147749892 (0x80041004)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-149">Error en el proveedor en algún momento distinto de durante la inicialización.</span><span class="sxs-lookup"><span data-stu-id="87ddf-149">Provider has failed at some time other than during initialization.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-150"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**\_ \_ no coinciden los tipos E de WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-150"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**WBEM\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-151">2147749893 (0x80041005)</span><span class="sxs-lookup"><span data-stu-id="87ddf-151">2147749893 (0x80041005)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-152">Error de coincidencia de tipos.</span><span class="sxs-lookup"><span data-stu-id="87ddf-152">Type mismatch occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-153"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**\_ \_ memoria insuficiente \_ de \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="87ddf-153"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM\_E\_OUT\_OF\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-154">2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="87ddf-154">2147749894 (0x80041006)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-155">Memoria insuficiente para la operación.</span><span class="sxs-lookup"><span data-stu-id="87ddf-155">Not enough memory for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-156"><span id="WBEM_E_INVALID_CONTEXT"></span><span id="wbem_e_invalid_context"></span>**\_ \_ contexto no válido de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-156"><span id="WBEM_E_INVALID_CONTEXT"></span><span id="wbem_e_invalid_context"></span>**WBEM\_E\_INVALID\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-157">2147749895 (0x80041007)</span><span class="sxs-lookup"><span data-stu-id="87ddf-157">2147749895 (0x80041007)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-158">El objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) no es válido.</span><span class="sxs-lookup"><span data-stu-id="87ddf-158">The [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-159"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**\_ \_ parámetro no válido de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-159"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**WBEM\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-160">2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="87ddf-160">2147749896 (0x80041008)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-161">Uno de los parámetros de la llamada no es correcto.</span><span class="sxs-lookup"><span data-stu-id="87ddf-161">One of the parameters to the call is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-162"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ no \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="87ddf-162"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM\_E\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-163">2147749897 (0x80041009)</span><span class="sxs-lookup"><span data-stu-id="87ddf-163">2147749897 (0x80041009)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-164">El recurso, normalmente un servidor remoto, no está disponible actualmente.</span><span class="sxs-lookup"><span data-stu-id="87ddf-164">Resource, typically a remote server, is not currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-165"><span id="WBEM_E_CRITICAL_ERROR"></span><span id="wbem_e_critical_error"></span>**\_ \_ error crítico de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-165"><span id="WBEM_E_CRITICAL_ERROR"></span><span id="wbem_e_critical_error"></span>**WBEM\_E\_CRITICAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-166">2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="87ddf-166">2147749898 (0x8004100A)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-167">Se produjo un error interno, crítico e inesperado.</span><span class="sxs-lookup"><span data-stu-id="87ddf-167">Internal, critical, and unexpected error occurred.</span></span> <span data-ttu-id="87ddf-168">Informe del error al servicio de soporte técnico de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="87ddf-168">Report the error to Microsoft Technical Support.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-169"><span id="WBEM_E_INVALID_STREAM"></span><span id="wbem_e_invalid_stream"></span>**\_ \_ secuencia no válida de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-169"><span id="WBEM_E_INVALID_STREAM"></span><span id="wbem_e_invalid_stream"></span>**WBEM\_E\_INVALID\_STREAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-170">2147749899 (0x8004100B)</span><span class="sxs-lookup"><span data-stu-id="87ddf-170">2147749899 (0x8004100B)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-171">Se dañó uno o más paquetes de red durante una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="87ddf-171">One or more network packets were corrupted during a remote session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-172"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM \_ E \_ no \_ compatible**</span><span class="sxs-lookup"><span data-stu-id="87ddf-172"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM\_E\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-173">2147749900 (0x8004100C)</span><span class="sxs-lookup"><span data-stu-id="87ddf-173">2147749900 (0x8004100C)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-174">La característica u operación no se admiten.</span><span class="sxs-lookup"><span data-stu-id="87ddf-174">Feature or operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-175"><span id="WBEM_E_INVALID_SUPERCLASS"></span><span id="wbem_e_invalid_superclass"></span>**\_ \_ superclase no válida de WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-175"><span id="WBEM_E_INVALID_SUPERCLASS"></span><span id="wbem_e_invalid_superclass"></span>**WBEM\_E\_INVALID\_SUPERCLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-176">2147749901 (0x8004100D)</span><span class="sxs-lookup"><span data-stu-id="87ddf-176">2147749901 (0x8004100D)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-177">La clase primaria especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="87ddf-177">Parent class specified is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-178"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**\_espacio de \_ nombres no válido de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-178"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM\_E\_INVALID\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-179">2147749902 (0x8004100E)</span><span class="sxs-lookup"><span data-stu-id="87ddf-179">2147749902 (0x8004100E)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-180">No se encuentra el espacio de nombres especificado.</span><span class="sxs-lookup"><span data-stu-id="87ddf-180">Namespace specified cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-181"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**\_ \_ objeto no válido de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-181"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**WBEM\_E\_INVALID\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-182">2147749903 (0x8004100F)</span><span class="sxs-lookup"><span data-stu-id="87ddf-182">2147749903 (0x8004100F)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-183">La instancia especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="87ddf-183">Specified instance is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-184"><span id="WBEM_E_INVALID_CLASS"></span><span id="wbem_e_invalid_class"></span>**\_ \_ clase no válida WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-184"><span id="WBEM_E_INVALID_CLASS"></span><span id="wbem_e_invalid_class"></span>**WBEM\_E\_INVALID\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-185">2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="87ddf-185">2147749904 (0x80041010)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-186">La clase especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="87ddf-186">Specified class is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-187"><span id="WBEM_E_PROVIDER_NOT_FOUND"></span><span id="wbem_e_provider_not_found"></span>**\_ \_ \_ no \_ se encontró el proveedor WBEM E**</span><span class="sxs-lookup"><span data-stu-id="87ddf-187"><span id="WBEM_E_PROVIDER_NOT_FOUND"></span><span id="wbem_e_provider_not_found"></span>**WBEM\_E\_PROVIDER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-188">2147749905 (0x80041011)</span><span class="sxs-lookup"><span data-stu-id="87ddf-188">2147749905 (0x80041011)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-189">El proveedor al que se hace referencia en el esquema no tiene un registro correspondiente.</span><span class="sxs-lookup"><span data-stu-id="87ddf-189">Provider referenced in the schema does not have a corresponding registration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-190"><span id="WBEM_E_INVALID_PROVIDER_REGISTRATION"></span><span id="wbem_e_invalid_provider_registration"></span>**\_registro de \_ proveedor no válido de WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-190"><span id="WBEM_E_INVALID_PROVIDER_REGISTRATION"></span><span id="wbem_e_invalid_provider_registration"></span>**WBEM\_E\_INVALID\_PROVIDER\_REGISTRATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-191">2147749906</span><span class="sxs-lookup"><span data-stu-id="87ddf-191">2147749906</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-192">El proveedor al que se hace referencia en el esquema tiene un registro incorrecto o incompleto.</span><span class="sxs-lookup"><span data-stu-id="87ddf-192">Provider referenced in the schema has an incorrect or incomplete registration.</span></span>

<span data-ttu-id="87ddf-193">Este error puede deberse a muchas condiciones, entre las que se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="87ddf-193">This error may be caused by many conditions, including the following:</span></span>

-   <span data-ttu-id="87ddf-194">Un comando [ \# pragma de espacio de nombres](pragma-namespace.md) que falta en el archivo Managed Object Format (MOF) usado para registrar el proveedor.</span><span class="sxs-lookup"><span data-stu-id="87ddf-194">A missing [\#pragma namespace](pragma-namespace.md) command in the Managed Object Format (MOF) file used to register the provider.</span></span> <span data-ttu-id="87ddf-195">El proveedor puede estar registrado en el espacio de nombres WMI equivocado.</span><span class="sxs-lookup"><span data-stu-id="87ddf-195">The provider may be registered in the wrong WMI namespace.</span></span>
-   <span data-ttu-id="87ddf-196">No se pudo recuperar el registro COM.</span><span class="sxs-lookup"><span data-stu-id="87ddf-196">Failure to retrieve the COM registration.</span></span>
-   <span data-ttu-id="87ddf-197">El modelo de hospedaje no es válido.</span><span class="sxs-lookup"><span data-stu-id="87ddf-197">Hosting model is not valid.</span></span> <span data-ttu-id="87ddf-198">Para obtener más información, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="87ddf-198">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>
-   <span data-ttu-id="87ddf-199">Una clase especificada en el registro no es válida.</span><span class="sxs-lookup"><span data-stu-id="87ddf-199">An class specified in the registration is not valid.</span></span>
-   <span data-ttu-id="87ddf-200">Error al crear una instancia de o heredar de la clase [**\_ \_ Win32Provider**](--win32provider.md) para crear el registro del proveedor en el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="87ddf-200">Failure to create an instance of or inherit from the [**\_\_Win32Provider**](--win32provider.md) class to create the provider registration in the MOF file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-201"><span id="WBEM_E_PROVIDER_LOAD_FAILURE"></span><span id="wbem_e_provider_load_failure"></span>**\_error de \_ carga del proveedor \_ \_ de WBEM E**</span><span class="sxs-lookup"><span data-stu-id="87ddf-201"><span id="WBEM_E_PROVIDER_LOAD_FAILURE"></span><span id="wbem_e_provider_load_failure"></span>**WBEM\_E\_PROVIDER\_LOAD\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-202">2147749907 (0x80041013)</span><span class="sxs-lookup"><span data-stu-id="87ddf-202">2147749907 (0x80041013)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-203">COM no encuentra un proveedor al que se hace referencia en el esquema.</span><span class="sxs-lookup"><span data-stu-id="87ddf-203">COM cannot locate a provider referenced in the schema.</span></span>

<span data-ttu-id="87ddf-204">Este error puede deberse a muchas condiciones, entre las que se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="87ddf-204">This error may be caused by many conditions, including the following:</span></span>

-   <span data-ttu-id="87ddf-205">El proveedor está utilizando un archivo DLL de WMI que no coincide con el archivo. lib utilizado cuando se compiló el proveedor.</span><span class="sxs-lookup"><span data-stu-id="87ddf-205">Provider is using a WMI DLL that does not match the .lib file used when the provider was built.</span></span>
-   <span data-ttu-id="87ddf-206">La DLL del proveedor, o cualquiera de los archivos dll de los que depende, está dañada.</span><span class="sxs-lookup"><span data-stu-id="87ddf-206">Provider's DLL, or any of the DLLs on which it depends, is corrupt.</span></span>
-   <span data-ttu-id="87ddf-207">El proveedor no pudo exportar [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span><span class="sxs-lookup"><span data-stu-id="87ddf-207">Provider failed to export [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span></span>
-   <span data-ttu-id="87ddf-208">El proveedor en proceso no se registró con el comando **regsvr32** .</span><span class="sxs-lookup"><span data-stu-id="87ddf-208">In-process provider was not registered using the **regsvr32** command.</span></span>
-   <span data-ttu-id="87ddf-209">El proveedor fuera de proceso no se registró con el modificador **/regserver** .</span><span class="sxs-lookup"><span data-stu-id="87ddf-209">Out-of-process provider was not registered using the **/regserver** switch.</span></span> <span data-ttu-id="87ddf-210">Por ejemplo, **myprog.exe/regserver**.</span><span class="sxs-lookup"><span data-stu-id="87ddf-210">For example, **myprog.exe /regserver**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-211"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**\_error de \_ inicialización de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-211"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**WBEM\_E\_INITIALIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-212">2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="87ddf-212">2147749908 (0x80041014)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-213">No se pudo inicializar el componente, como un proveedor, por motivos internos.</span><span class="sxs-lookup"><span data-stu-id="87ddf-213">Component, such as a provider, failed to initialize for internal reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-214"><span id="WBEM_E_TRANSPORT_FAILURE"></span><span id="wbem_e_transport_failure"></span>**error de transporte de WBEM \_ E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-214"><span id="WBEM_E_TRANSPORT_FAILURE"></span><span id="wbem_e_transport_failure"></span>**WBEM\_E\_TRANSPORT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-215">2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="87ddf-215">2147749909 (0x80041015)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-216">Error de red que impide el funcionamiento normal.</span><span class="sxs-lookup"><span data-stu-id="87ddf-216">Networking error that prevents normal operation has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-217"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**\_ \_ operación no válida de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-217"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**WBEM\_E\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-218">2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="87ddf-218">2147749910 (0x80041016)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-219">La operación solicitada no es válida.</span><span class="sxs-lookup"><span data-stu-id="87ddf-219">Requested operation is not valid.</span></span> <span data-ttu-id="87ddf-220">Normalmente, este error está relacionado con intentos no válidos de eliminar clases o propiedades.</span><span class="sxs-lookup"><span data-stu-id="87ddf-220">This error usually applies to invalid attempts to delete classes or properties.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-221"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**\_ \_ consulta no válida de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-221"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**WBEM\_E\_INVALID\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-222">2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="87ddf-222">2147749911 (0x80041017)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-223">La consulta no era válida sintácticamente.</span><span class="sxs-lookup"><span data-stu-id="87ddf-223">Query was not syntactically valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-224"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**\_tipo de consulta WBEM E \_ no válido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-224"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**WBEM\_E\_INVALID\_QUERY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-225">2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="87ddf-225">2147749912 (0x80041018)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-226">No se admite el lenguaje de consulta solicitado.</span><span class="sxs-lookup"><span data-stu-id="87ddf-226">Requested query language is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-227"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="87ddf-227"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM\_E\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-228">2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="87ddf-228">2147749913 (0x80041019)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-229">En una operación PUT, se especificó la marca **wbemChangeFlagCreateOnly** , pero la instancia ya existe.</span><span class="sxs-lookup"><span data-stu-id="87ddf-229">In a put operation, the **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-230"><span id="WBEM_E_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_override_not_allowed"></span>**\_no se \_ permite la invalidación de WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-230"><span id="WBEM_E_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_override_not_allowed"></span>**WBEM\_E\_OVERRIDE\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-231">2147749914 (0x8004101A)</span><span class="sxs-lookup"><span data-stu-id="87ddf-231">2147749914 (0x8004101A)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-232">No es posible realizar la operación de agregar en este calificador porque el objeto propietario no permite invalidaciones.</span><span class="sxs-lookup"><span data-stu-id="87ddf-232">Not possible to perform the add operation on this qualifier because the owning object does not permit overrides.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-233"><span id="WBEM_E_PROPAGATED_QUALIFIER"></span><span id="wbem_e_propagated_qualifier"></span>**\_ \_ calificador propagado por WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-233"><span id="WBEM_E_PROPAGATED_QUALIFIER"></span><span id="wbem_e_propagated_qualifier"></span>**WBEM\_E\_PROPAGATED\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-234">2147749915 (0x8004101B)</span><span class="sxs-lookup"><span data-stu-id="87ddf-234">2147749915 (0x8004101B)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-235">El usuario intentó eliminar un calificador que no era propiedad.</span><span class="sxs-lookup"><span data-stu-id="87ddf-235">User attempted to delete a qualifier that was not owned.</span></span> <span data-ttu-id="87ddf-236">Se trataba de un calificador heredado de una clase principal.</span><span class="sxs-lookup"><span data-stu-id="87ddf-236">The qualifier was inherited from a parent class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-237"><span id="WBEM_E_PROPAGATED_PROPERTY"></span><span id="wbem_e_propagated_property"></span>**\_ \_ propiedad propagada de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-237"><span id="WBEM_E_PROPAGATED_PROPERTY"></span><span id="wbem_e_propagated_property"></span>**WBEM\_E\_PROPAGATED\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-238">2147749916 (0x8004101C)</span><span class="sxs-lookup"><span data-stu-id="87ddf-238">2147749916 (0x8004101C)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-239">El usuario intentó eliminar una propiedad que no era propiedad.</span><span class="sxs-lookup"><span data-stu-id="87ddf-239">User attempted to delete a property that was not owned.</span></span> <span data-ttu-id="87ddf-240">Se trataba de una propiedad heredada de una clase principal.</span><span class="sxs-lookup"><span data-stu-id="87ddf-240">The property was inherited from a parent class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-241"><span id="WBEM_E_UNEXPECTED"></span><span id="wbem_e_unexpected"></span>**WBEM \_ E \_ inesperado**</span><span class="sxs-lookup"><span data-stu-id="87ddf-241"><span id="WBEM_E_UNEXPECTED"></span><span id="wbem_e_unexpected"></span>**WBEM\_E\_UNEXPECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-242">2147749917 (0x8004101D)</span><span class="sxs-lookup"><span data-stu-id="87ddf-242">2147749917 (0x8004101D)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-243">El cliente realizó una secuencia de llamadas inesperada y no válida, como llamar a [**EndEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration) antes de llamar a [**BeginEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration).</span><span class="sxs-lookup"><span data-stu-id="87ddf-243">Client made an unexpected and illegal sequence of calls, such as calling [**EndEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration) before calling [**BeginEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-244"><span id="WBEM_E_ILLEGAL_OPERATION"></span><span id="wbem_e_illegal_operation"></span>**\_ \_ operación ilegal de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-244"><span id="WBEM_E_ILLEGAL_OPERATION"></span><span id="wbem_e_illegal_operation"></span>**WBEM\_E\_ILLEGAL\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-245">2147749918 (0x8004101E)</span><span class="sxs-lookup"><span data-stu-id="87ddf-245">2147749918 (0x8004101E)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-246">El usuario solicitó una operación no válida, como generar una clase a partir de una instancia.</span><span class="sxs-lookup"><span data-stu-id="87ddf-246">User requested an illegal operation, such as spawning a class from an instance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-247"><span id="WBEM_E_CANNOT_BE_KEY"></span><span id="wbem_e_cannot_be_key"></span>**WBEM \_ E \_ no puede \_ ser una \_ clave**</span><span class="sxs-lookup"><span data-stu-id="87ddf-247"><span id="WBEM_E_CANNOT_BE_KEY"></span><span id="wbem_e_cannot_be_key"></span>**WBEM\_E\_CANNOT\_BE\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-248">2147749919 (0x8004101F)</span><span class="sxs-lookup"><span data-stu-id="87ddf-248">2147749919 (0x8004101F)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-249">Intento no válido de especificar un calificador de clave en una propiedad que no puede ser una clave.</span><span class="sxs-lookup"><span data-stu-id="87ddf-249">Illegal attempt to specify a key qualifier on a property that cannot be a key.</span></span> <span data-ttu-id="87ddf-250">Las claves se especifican en la definición de la clase de un objeto, y no se pueden modificar instancia por instancia.</span><span class="sxs-lookup"><span data-stu-id="87ddf-250">The keys are specified in the class definition for an object and cannot be altered on a per-instance basis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-251"><span id="WBEM_E_INCOMPLETE_CLASS"></span><span id="wbem_e_incomplete_class"></span>**WBEM \_ E \_ clase incompleta \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-251"><span id="WBEM_E_INCOMPLETE_CLASS"></span><span id="wbem_e_incomplete_class"></span>**WBEM\_E\_INCOMPLETE\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-252">2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="87ddf-252">2147749920 (0x80041020)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-253">El objeto actual no es una definición de clase válida.</span><span class="sxs-lookup"><span data-stu-id="87ddf-253">Current object is not a valid class definition.</span></span> <span data-ttu-id="87ddf-254">O bien está incompleto o no se ha registrado con WMI mediante [**SWbemObject. put \_**](swbemobject-put-.md).</span><span class="sxs-lookup"><span data-stu-id="87ddf-254">Either it is incomplete or it has not been registered with WMI using [**SWbemObject.Put\_**](swbemobject-put-.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-255"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**\_ \_ sintaxis no válida de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-255"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**WBEM\_E\_INVALID\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-256">2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="87ddf-256">2147749921 (0x80041021)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-257">La consulta no es válida sintácticamente.</span><span class="sxs-lookup"><span data-stu-id="87ddf-257">Query is syntactically not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-258"><span id="WBEM_E_NONDECORATED_OBJECT"></span><span id="wbem_e_nondecorated_object"></span>**\_objeto no \_ representativo de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-258"><span id="WBEM_E_NONDECORATED_OBJECT"></span><span id="wbem_e_nondecorated_object"></span>**WBEM\_E\_NONDECORATED\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-259">2147749922 (0x80041022)</span><span class="sxs-lookup"><span data-stu-id="87ddf-259">2147749922 (0x80041022)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-260">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="87ddf-260">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-261"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM \_ E \_ \_ solo lectura**</span><span class="sxs-lookup"><span data-stu-id="87ddf-261"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM\_E\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-262">2147749923 (0x80041023)</span><span class="sxs-lookup"><span data-stu-id="87ddf-262">2147749923 (0x80041023)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-263">Se intentó modificar una propiedad de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="87ddf-263">An attempt was made to modify a read-only property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-264"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**proveedor de WBEM \_ E \_ \_ no \_ compatible**</span><span class="sxs-lookup"><span data-stu-id="87ddf-264"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**WBEM\_E\_PROVIDER\_NOT\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-265">2147749924 (0x80041024)</span><span class="sxs-lookup"><span data-stu-id="87ddf-265">2147749924 (0x80041024)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-266">El proveedor no puede realizar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="87ddf-266">Provider cannot perform the requested operation.</span></span> <span data-ttu-id="87ddf-267">Esto puede incluir una consulta demasiado compleja, recuperar una instancia, crear o actualizar una clase, eliminar una clase o enumerar una clase.</span><span class="sxs-lookup"><span data-stu-id="87ddf-267">This can include a query that is too complex, retrieving an instance, creating or updating a class, deleting a class, or enumerating a class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-268"><span id="WBEM_E_CLASS_HAS_CHILDREN"></span><span id="wbem_e_class_has_children"></span>**la \_ clase WBEM E \_ \_ tiene \_ elementos secundarios**</span><span class="sxs-lookup"><span data-stu-id="87ddf-268"><span id="WBEM_E_CLASS_HAS_CHILDREN"></span><span id="wbem_e_class_has_children"></span>**WBEM\_E\_CLASS\_HAS\_CHILDREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-269">2147749925 (0x80041025)</span><span class="sxs-lookup"><span data-stu-id="87ddf-269">2147749925 (0x80041025)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-270">Se intentó realizar un cambio que invalida una subclase.</span><span class="sxs-lookup"><span data-stu-id="87ddf-270">Attempt was made to make a change that invalidates a subclass.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-271"><span id="WBEM_E_CLASS_HAS_INSTANCES"></span><span id="wbem_e_class_has_instances"></span>**la \_ clase WBEM E \_ \_ tiene \_ instancias**</span><span class="sxs-lookup"><span data-stu-id="87ddf-271"><span id="WBEM_E_CLASS_HAS_INSTANCES"></span><span id="wbem_e_class_has_instances"></span>**WBEM\_E\_CLASS\_HAS\_INSTANCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-272">2147749926 (0x80041026)</span><span class="sxs-lookup"><span data-stu-id="87ddf-272">2147749926 (0x80041026)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-273">Se intentó eliminar o modificar una clase que tiene instancias.</span><span class="sxs-lookup"><span data-stu-id="87ddf-273">Attempt was made to delete or modify a class that has instances.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-274"><span id="WBEM_E_QUERY_NOT_IMPLEMENTED"></span><span id="wbem_e_query_not_implemented"></span>**consulta de WBEM \_ E \_ \_ no \_ implementada**</span><span class="sxs-lookup"><span data-stu-id="87ddf-274"><span id="WBEM_E_QUERY_NOT_IMPLEMENTED"></span><span id="wbem_e_query_not_implemented"></span>**WBEM\_E\_QUERY\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-275">2147749927 (0x80041027)</span><span class="sxs-lookup"><span data-stu-id="87ddf-275">2147749927 (0x80041027)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-276">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="87ddf-276">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-277"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E \_ no válido \_ null**</span><span class="sxs-lookup"><span data-stu-id="87ddf-277"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM\_E\_ILLEGAL\_NULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-278">2147749928 (0x80041028)</span><span class="sxs-lookup"><span data-stu-id="87ddf-278">2147749928 (0x80041028)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-279">Se especificó el valor Nothing/**null** para una propiedad que debe tener un valor, como uno marcado mediante un calificador de [**clave**](key-qualifier.md), [**indexado**](optional-qualifiers.md)o **not \_ null** .</span><span class="sxs-lookup"><span data-stu-id="87ddf-279">Value of Nothing/**NULL** was specified for a property that must have a value, such as one that is marked by a [**Key**](key-qualifier.md), [**Indexed**](optional-qualifiers.md), or **Not\_Null** qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-280"><span id="WBEM_E_INVALID_QUALIFIER_TYPE"></span><span id="wbem_e_invalid_qualifier_type"></span>**\_tipo de \_ \_ calificador de WBEM E no válido \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-280"><span id="WBEM_E_INVALID_QUALIFIER_TYPE"></span><span id="wbem_e_invalid_qualifier_type"></span>**WBEM\_E\_INVALID\_QUALIFIER\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-281">2147749929 (0x80041029)</span><span class="sxs-lookup"><span data-stu-id="87ddf-281">2147749929 (0x80041029)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-282">Se proporcionó un valor de variante para un calificador que no es un tipo de calificador válido.</span><span class="sxs-lookup"><span data-stu-id="87ddf-282">Variant value for a qualifier was provided that is not a legal qualifier type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-283"><span id="WBEM_E_INVALID_PROPERTY_TYPE"></span><span id="wbem_e_invalid_property_type"></span>**\_tipo de \_ propiedad no válido de WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-283"><span id="WBEM_E_INVALID_PROPERTY_TYPE"></span><span id="wbem_e_invalid_property_type"></span>**WBEM\_E\_INVALID\_PROPERTY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-284">2147749930 (0x8004102A)</span><span class="sxs-lookup"><span data-stu-id="87ddf-284">2147749930 (0x8004102A)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-285">El tipo CIM especificado para una propiedad no es válido.</span><span class="sxs-lookup"><span data-stu-id="87ddf-285">CIM type specified for a property is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-286"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**\_valor de WBEM E comprendido \_ \_ fuera \_ del \_ intervalo**</span><span class="sxs-lookup"><span data-stu-id="87ddf-286"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**WBEM\_E\_VALUE\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-287">2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="87ddf-287">2147749931 (0x8004102B)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-288">La solicitud se realizó con un valor fuera de intervalo o es incompatible con el tipo.</span><span class="sxs-lookup"><span data-stu-id="87ddf-288">Request was made with an out-of-range value or it is incompatible with the type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-289"><span id="WBEM_E_CANNOT_BE_SINGLETON"></span><span id="wbem_e_cannot_be_singleton"></span>**WBEM \_ E \_ no puede \_ ser \_ Singleton**</span><span class="sxs-lookup"><span data-stu-id="87ddf-289"><span id="WBEM_E_CANNOT_BE_SINGLETON"></span><span id="wbem_e_cannot_be_singleton"></span>**WBEM\_E\_CANNOT\_BE\_SINGLETON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-290">2147749932 (0x8004102C)</span><span class="sxs-lookup"><span data-stu-id="87ddf-290">2147749932 (0x8004102C)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-291">Se hizo un intento no válido de crear una clase singleton, como cuando la clase se deriva de una clase no singleton.</span><span class="sxs-lookup"><span data-stu-id="87ddf-291">Illegal attempt was made to make a class singleton, such as when the class is derived from a non-singleton class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-292"><span id="WBEM_E_INVALID_CIM_TYPE"></span><span id="wbem_e_invalid_cim_type"></span>**\_tipo CIM de WBEM E \_ no válido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-292"><span id="WBEM_E_INVALID_CIM_TYPE"></span><span id="wbem_e_invalid_cim_type"></span>**WBEM\_E\_INVALID\_CIM\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-293">2147749933 (0x8004102D)</span><span class="sxs-lookup"><span data-stu-id="87ddf-293">2147749933 (0x8004102D)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-294">El tipo CIM especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="87ddf-294">CIM type specified is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-295"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM \_ E \_ método no válido \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-295"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM\_E\_INVALID\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-296">2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="87ddf-296">2147749934 (0x8004102E)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-297">El método solicitado no está disponible.</span><span class="sxs-lookup"><span data-stu-id="87ddf-297">Requested method is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-298"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**\_parámetros de \_ método no válido de WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-298"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**WBEM\_E\_INVALID\_METHOD\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-299">2147749935 (0x8004102F)</span><span class="sxs-lookup"><span data-stu-id="87ddf-299">2147749935 (0x8004102F)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-300">Los parámetros proporcionados para el método no son válidos.</span><span class="sxs-lookup"><span data-stu-id="87ddf-300">Parameters provided for the method are not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-301"><span id="WBEM_E_SYSTEM_PROPERTY"></span><span id="wbem_e_system_property"></span>**\_ \_ propiedad del sistema WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-301"><span id="WBEM_E_SYSTEM_PROPERTY"></span><span id="wbem_e_system_property"></span>**WBEM\_E\_SYSTEM\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-302">2147749936 (0x80041030)</span><span class="sxs-lookup"><span data-stu-id="87ddf-302">2147749936 (0x80041030)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-303">Se intentó obtener calificadores en una propiedad del sistema.</span><span class="sxs-lookup"><span data-stu-id="87ddf-303">There was an attempt to get qualifiers on a system property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-304"><span id="WBEM_E_INVALID_PROPERTY"></span><span id="wbem_e_invalid_property"></span>**\_ \_ propiedad no válida de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-304"><span id="WBEM_E_INVALID_PROPERTY"></span><span id="wbem_e_invalid_property"></span>**WBEM\_E\_INVALID\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-305">2147749937 (0x80041031)</span><span class="sxs-lookup"><span data-stu-id="87ddf-305">2147749937 (0x80041031)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-306">No se reconoce el tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="87ddf-306">Property type is not recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-307"><span id="WBEM_E_CALL_CANCELLED"></span><span id="wbem_e_call_cancelled"></span>**llamada de WBEM \_ E \_ \_ cancelada**</span><span class="sxs-lookup"><span data-stu-id="87ddf-307"><span id="WBEM_E_CALL_CANCELLED"></span><span id="wbem_e_call_cancelled"></span>**WBEM\_E\_CALL\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-308">2147749938 (0x80041032)</span><span class="sxs-lookup"><span data-stu-id="87ddf-308">2147749938 (0x80041032)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-309">El proceso asincrónico ha sido cancelado internamente o por el usuario.</span><span class="sxs-lookup"><span data-stu-id="87ddf-309">Asynchronous process has been canceled internally or by the user.</span></span> <span data-ttu-id="87ddf-310">Tenga en cuenta que, debido a la sincronización y la naturaleza de la operación asincrónica, es posible que la operación no se haya cancelado realmente.</span><span class="sxs-lookup"><span data-stu-id="87ddf-310">Note that due to the timing and nature of the asynchronous operation, the operation may not have been truly canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-311"><span id="WBEM_E_SHUTTING_DOWN"></span><span id="wbem_e_shutting_down"></span>**Desactivación de WBEM \_ E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-311"><span id="WBEM_E_SHUTTING_DOWN"></span><span id="wbem_e_shutting_down"></span>**WBEM\_E\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-312">2147749939 (0x80041033)</span><span class="sxs-lookup"><span data-stu-id="87ddf-312">2147749939 (0x80041033)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-313">El usuario ha solicitado una operación mientras WMI está en proceso de apagado.</span><span class="sxs-lookup"><span data-stu-id="87ddf-313">User has requested an operation while WMI is in the process of shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-314"><span id="WBEM_E_PROPAGATED_METHOD"></span><span id="wbem_e_propagated_method"></span>**\_ \_ método propagado por WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-314"><span id="WBEM_E_PROPAGATED_METHOD"></span><span id="wbem_e_propagated_method"></span>**WBEM\_E\_PROPAGATED\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-315">2147749940 (0x80041034)</span><span class="sxs-lookup"><span data-stu-id="87ddf-315">2147749940 (0x80041034)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-316">Se intentó reutilizar un nombre de método existente de una clase primaria y las firmas no coinciden.</span><span class="sxs-lookup"><span data-stu-id="87ddf-316">Attempt was made to reuse an existing method name from a parent class and the signatures do not match.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-317"><span id="WBEM_E_UNSUPPORTED_PARAMETER"></span><span id="wbem_e_unsupported_parameter"></span>**\_ \_ parámetro no compatible de WBEM \_ E**</span><span class="sxs-lookup"><span data-stu-id="87ddf-317"><span id="WBEM_E_UNSUPPORTED_PARAMETER"></span><span id="wbem_e_unsupported_parameter"></span>**WBEM\_E\_UNSUPPORTED\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-318">2147749941 (0x80041035)</span><span class="sxs-lookup"><span data-stu-id="87ddf-318">2147749941 (0x80041035)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-319">Uno o más valores de parámetro, como un texto de consulta, es demasiado complejo o no se admite.</span><span class="sxs-lookup"><span data-stu-id="87ddf-319">One or more parameter values, such as a query text, is too complex or unsupported.</span></span> <span data-ttu-id="87ddf-320">Por lo tanto, se solicita a WMI que vuelva a intentar la operación con parámetros más sencillos.</span><span class="sxs-lookup"><span data-stu-id="87ddf-320">WMI is therefore requested to retry the operation with simpler parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-321"><span id="WBEM_E_MISSING_PARAMETER_ID"></span><span id="wbem_e_missing_parameter_id"></span>**\_falta el \_ \_ \_ ID. de parámetro de WBEM E**</span><span class="sxs-lookup"><span data-stu-id="87ddf-321"><span id="WBEM_E_MISSING_PARAMETER_ID"></span><span id="wbem_e_missing_parameter_id"></span>**WBEM\_E\_MISSING\_PARAMETER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-322">2147749942 (0x80041036)</span><span class="sxs-lookup"><span data-stu-id="87ddf-322">2147749942 (0x80041036)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-323">Falta el parámetro en la llamada al método.</span><span class="sxs-lookup"><span data-stu-id="87ddf-323">Parameter was missing from the method call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-324"><span id="WBEM_E_INVALID_PARAMETER_ID"></span><span id="wbem_e_invalid_parameter_id"></span>**\_ID. de parámetro de WBEM E \_ no válido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-324"><span id="WBEM_E_INVALID_PARAMETER_ID"></span><span id="wbem_e_invalid_parameter_id"></span>**WBEM\_E\_INVALID\_PARAMETER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-325">2147749943 (0x80041037)</span><span class="sxs-lookup"><span data-stu-id="87ddf-325">2147749943 (0x80041037)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-326">El parámetro de método tiene un calificador de [**ID**](standard-wmi-qualifiers.md) . que no es válido.</span><span class="sxs-lookup"><span data-stu-id="87ddf-326">Method parameter has an [**ID**](standard-wmi-qualifiers.md) qualifier that is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-327"><span id="WBEM_E_NONCONSECUTIVE_PARAMETER_IDS"></span><span id="wbem_e_nonconsecutive_parameter_ids"></span>**\_ \_ identificadores de parámetros no consecutivos de WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-327"><span id="WBEM_E_NONCONSECUTIVE_PARAMETER_IDS"></span><span id="wbem_e_nonconsecutive_parameter_ids"></span>**WBEM\_E\_NONCONSECUTIVE\_PARAMETER\_IDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-328">2147749944 (0x80041038)</span><span class="sxs-lookup"><span data-stu-id="87ddf-328">2147749944 (0x80041038)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-329">Uno o varios de los parámetros del método tienen calificadores de [**identificador**](standard-wmi-qualifiers.md) que están fuera de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="87ddf-329">One or more of the method parameters have [**ID**](standard-wmi-qualifiers.md) qualifiers that are out of sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-330"><span id="WBEM_E_PARAMETER_ID_ON_RETVAL"></span><span id="wbem_e_parameter_id_on_retval"></span>**\_ \_ \_ ID. de parámetro \_ de WBEM E en \_ retval**</span><span class="sxs-lookup"><span data-stu-id="87ddf-330"><span id="WBEM_E_PARAMETER_ID_ON_RETVAL"></span><span id="wbem_e_parameter_id_on_retval"></span>**WBEM\_E\_PARAMETER\_ID\_ON\_RETVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-331">2147749945 (0x80041039)</span><span class="sxs-lookup"><span data-stu-id="87ddf-331">2147749945 (0x80041039)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-332">El valor devuelto para un método tiene un calificador de [**identificador**](standard-wmi-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="87ddf-332">Return value for a method has an [**ID**](standard-wmi-qualifiers.md) qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-333"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**\_ruta de \_ objeto no válida de WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-333"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM\_E\_INVALID\_OBJECT\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-334">2147749946 (0x8004103A)</span><span class="sxs-lookup"><span data-stu-id="87ddf-334">2147749946 (0x8004103A)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-335">La ruta de acceso del objeto especificado no era válida.</span><span class="sxs-lookup"><span data-stu-id="87ddf-335">Specified object path was not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-336"><span id="WBEM_E_OUT_OF_DISK_SPACE"></span><span id="wbem_e_out_of_disk_space"></span>**WBEM \_ E \_ insuficiente \_ \_ espacio en disco \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-336"><span id="WBEM_E_OUT_OF_DISK_SPACE"></span><span id="wbem_e_out_of_disk_space"></span>**WBEM\_E\_OUT\_OF\_DISK\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-337">2147749947 (0x8004103B)</span><span class="sxs-lookup"><span data-stu-id="87ddf-337">2147749947 (0x8004103B)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-338">Espacio insuficiente en el disco o se alcanzó el límite de 4 GB en el repositorio de WMI (repositorio CIM).</span><span class="sxs-lookup"><span data-stu-id="87ddf-338">Disk is out of space or the 4 GB limit on WMI repository (CIM repository) size is reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-339"><span id="WBEM_E_BUFFER_TOO_SMALL"></span><span id="wbem_e_buffer_too_small"></span>**\_búfer E de WBEM \_ \_ demasiado \_ pequeño**</span><span class="sxs-lookup"><span data-stu-id="87ddf-339"><span id="WBEM_E_BUFFER_TOO_SMALL"></span><span id="wbem_e_buffer_too_small"></span>**WBEM\_E\_BUFFER\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-340">2147749948 (0x8004103C)</span><span class="sxs-lookup"><span data-stu-id="87ddf-340">2147749948 (0x8004103C)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-341">El búfer proporcionado era demasiado pequeño para contener todos los objetos del enumerador o para leer una propiedad de cadena.</span><span class="sxs-lookup"><span data-stu-id="87ddf-341">Supplied buffer was too small to hold all of the objects in the enumerator or to read a string property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-342"><span id="WBEM_E_UNSUPPORTED_PUT_EXTENSION"></span><span id="wbem_e_unsupported_put_extension"></span>**\_extensión put de WBEM E \_ no admitida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-342"><span id="WBEM_E_UNSUPPORTED_PUT_EXTENSION"></span><span id="wbem_e_unsupported_put_extension"></span>**WBEM\_E\_UNSUPPORTED\_PUT\_EXTENSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-343">2147749949 (0x8004103D)</span><span class="sxs-lookup"><span data-stu-id="87ddf-343">2147749949 (0x8004103D)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-344">El proveedor no admite la operación PUT solicitada.</span><span class="sxs-lookup"><span data-stu-id="87ddf-344">Provider does not support the requested put operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-345"><span id="WBEM_E_UNKNOWN_OBJECT_TYPE"></span><span id="wbem_e_unknown_object_type"></span>**\_tipo de \_ \_ objeto desconocido \_ de WBEM E**</span><span class="sxs-lookup"><span data-stu-id="87ddf-345"><span id="WBEM_E_UNKNOWN_OBJECT_TYPE"></span><span id="wbem_e_unknown_object_type"></span>**WBEM\_E\_UNKNOWN\_OBJECT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-346">2147749950 (0x8004103E)</span><span class="sxs-lookup"><span data-stu-id="87ddf-346">2147749950 (0x8004103E)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-347">Se encontró un objeto con un tipo o una versión incorrectos durante el cálculo de referencias.</span><span class="sxs-lookup"><span data-stu-id="87ddf-347">Object with an incorrect type or version was encountered during marshaling.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-348"><span id="WBEM_E_UNKNOWN_PACKET_TYPE"></span><span id="wbem_e_unknown_packet_type"></span>**\_tipo de \_ \_ paquete desconocido E WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-348"><span id="WBEM_E_UNKNOWN_PACKET_TYPE"></span><span id="wbem_e_unknown_packet_type"></span>**WBEM\_E\_UNKNOWN\_PACKET\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-349">2147749951 (0x8004103F)</span><span class="sxs-lookup"><span data-stu-id="87ddf-349">2147749951 (0x8004103F)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-350">Se encontró un paquete con un tipo o una versión incorrectos durante el cálculo de referencias.</span><span class="sxs-lookup"><span data-stu-id="87ddf-350">Packet with an incorrect type or version was encountered during marshaling.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-351"><span id="WBEM_E_MARSHAL_VERSION_MISMATCH"></span><span id="wbem_e_marshal_version_mismatch"></span>**la \_ versión de serialización de WBEM E \_ \_ \_ no coincide**</span><span class="sxs-lookup"><span data-stu-id="87ddf-351"><span id="WBEM_E_MARSHAL_VERSION_MISMATCH"></span><span id="wbem_e_marshal_version_mismatch"></span>**WBEM\_E\_MARSHAL\_VERSION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-352">2147749952 (0x80041040)</span><span class="sxs-lookup"><span data-stu-id="87ddf-352">2147749952 (0x80041040)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-353">El paquete tiene una versión no admitida.</span><span class="sxs-lookup"><span data-stu-id="87ddf-353">Packet has an unsupported version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-354"><span id="WBEM_E_MARSHAL_INVALID_SIGNATURE"></span><span id="wbem_e_marshal_invalid_signature"></span>**\_referencias a \_ la \_ firma no válida \_ de WBEM E**</span><span class="sxs-lookup"><span data-stu-id="87ddf-354"><span id="WBEM_E_MARSHAL_INVALID_SIGNATURE"></span><span id="wbem_e_marshal_invalid_signature"></span>**WBEM\_E\_MARSHAL\_INVALID\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-355">2147749953 (0x80041041)</span><span class="sxs-lookup"><span data-stu-id="87ddf-355">2147749953 (0x80041041)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-356">Parece que el paquete está dañado.</span><span class="sxs-lookup"><span data-stu-id="87ddf-356">Packet appears to be corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-357"><span id="WBEM_E_INVALID_QUALIFIER"></span><span id="wbem_e_invalid_qualifier"></span>**\_calificador de WBEM E \_ no válido \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-357"><span id="WBEM_E_INVALID_QUALIFIER"></span><span id="wbem_e_invalid_qualifier"></span>**WBEM\_E\_INVALID\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-358">2147749954 (0x80041042)</span><span class="sxs-lookup"><span data-stu-id="87ddf-358">2147749954 (0x80041042)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-359">Se intentó usar calificadores no coincidentes, como colocar \[ \] la clave en un objeto en lugar de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="87ddf-359">Attempt was made to mismatch qualifiers, such as putting \[key\] on an object instead of a property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-360"><span id="WBEM_E_INVALID_DUPLICATE_PARAMETER"></span><span id="wbem_e_invalid_duplicate_parameter"></span>**\_ \_ \_ parámetro duplicado de WBEM E no válido \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-360"><span id="WBEM_E_INVALID_DUPLICATE_PARAMETER"></span><span id="wbem_e_invalid_duplicate_parameter"></span>**WBEM\_E\_INVALID\_DUPLICATE\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-361">2147749955 (0x80041043)</span><span class="sxs-lookup"><span data-stu-id="87ddf-361">2147749955 (0x80041043)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-362">Se declaró un parámetro duplicado en un método CIM.</span><span class="sxs-lookup"><span data-stu-id="87ddf-362">Duplicate parameter was declared in a CIM method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-363"><span id="WBEM_E_TOO_MUCH_DATA"></span><span id="wbem_e_too_much_data"></span>**WBEM \_ E \_ demasiados \_ \_ datos**</span><span class="sxs-lookup"><span data-stu-id="87ddf-363"><span id="WBEM_E_TOO_MUCH_DATA"></span><span id="wbem_e_too_much_data"></span>**WBEM\_E\_TOO\_MUCH\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-364">2147749956 (0x80041044)</span><span class="sxs-lookup"><span data-stu-id="87ddf-364">2147749956 (0x80041044)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-365">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="87ddf-365">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-366"><span id="WBEM_E_SERVER_TOO_BUSY"></span><span id="wbem_e_server_too_busy"></span>**el \_ servidor WBEM E está \_ \_ demasiado \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="87ddf-366"><span id="WBEM_E_SERVER_TOO_BUSY"></span><span id="wbem_e_server_too_busy"></span>**WBEM\_E\_SERVER\_TOO\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-367">2147749957 (0x80041045)</span><span class="sxs-lookup"><span data-stu-id="87ddf-367">2147749957 (0x80041045)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-368">Se produjo un error en la llamada a [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .</span><span class="sxs-lookup"><span data-stu-id="87ddf-368">Call to [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) has failed.</span></span> <span data-ttu-id="87ddf-369">El proveedor puede reactivar el evento.</span><span class="sxs-lookup"><span data-stu-id="87ddf-369">The provider can refire the event.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-370"><span id="WBEM_E_INVALID_FLAVOR"></span><span id="wbem_e_invalid_flavor"></span>**tipo de WBEM \_ E \_ no válido \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-370"><span id="WBEM_E_INVALID_FLAVOR"></span><span id="wbem_e_invalid_flavor"></span>**WBEM\_E\_INVALID\_FLAVOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-371">2147749958 (0x80041046)</span><span class="sxs-lookup"><span data-stu-id="87ddf-371">2147749958 (0x80041046)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-372">El tipo de calificador especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="87ddf-372">Specified qualifier flavor was not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-373"><span id="WBEM_E_CIRCULAR_REFERENCE"></span><span id="wbem_e_circular_reference"></span>**\_ \_ referencia circular de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-373"><span id="WBEM_E_CIRCULAR_REFERENCE"></span><span id="wbem_e_circular_reference"></span>**WBEM\_E\_CIRCULAR\_REFERENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-374">2147749959 (0x80041047)</span><span class="sxs-lookup"><span data-stu-id="87ddf-374">2147749959 (0x80041047)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-375">Se intentó crear una referencia circular (por ejemplo, derivar una clase de sí misma).</span><span class="sxs-lookup"><span data-stu-id="87ddf-375">Attempt was made to create a reference that is circular (for example, deriving a class from itself).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-376"><span id="WBEM_E_UNSUPPORTED_CLASS_UPDATE"></span><span id="wbem_e_unsupported_class_update"></span>**\_actualización de \_ clase no compatible de WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-376"><span id="WBEM_E_UNSUPPORTED_CLASS_UPDATE"></span><span id="wbem_e_unsupported_class_update"></span>**WBEM\_E\_UNSUPPORTED\_CLASS\_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-377">2147749960 (0x80041048)</span><span class="sxs-lookup"><span data-stu-id="87ddf-377">2147749960 (0x80041048)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-378">No se admite la clase especificada.</span><span class="sxs-lookup"><span data-stu-id="87ddf-378">Specified class is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-379"><span id="WBEM_E_CANNOT_CHANGE_KEY_INHERITANCE"></span><span id="wbem_e_cannot_change_key_inheritance"></span>**WBEM \_ E \_ no puede \_ cambiar la \_ herencia de claves \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-379"><span id="WBEM_E_CANNOT_CHANGE_KEY_INHERITANCE"></span><span id="wbem_e_cannot_change_key_inheritance"></span>**WBEM\_E\_CANNOT\_CHANGE\_KEY\_INHERITANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-380">2147749961 (0x80041049)</span><span class="sxs-lookup"><span data-stu-id="87ddf-380">2147749961 (0x80041049)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-381">Se intentó cambiar una clave cuando las instancias o subclases ya usan la clave.</span><span class="sxs-lookup"><span data-stu-id="87ddf-381">Attempt was made to change a key when instances or subclasses are already using the key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-382"><span id="WBEM_E_CANNOT_CHANGE_INDEX_INHERITANCE"></span><span id="wbem_e_cannot_change_index_inheritance"></span>**WBEM \_ E \_ no puede \_ cambiar la \_ herencia de índices \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-382"><span id="WBEM_E_CANNOT_CHANGE_INDEX_INHERITANCE"></span><span id="wbem_e_cannot_change_index_inheritance"></span>**WBEM\_E\_CANNOT\_CHANGE\_INDEX\_INHERITANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-383">2147749968 (0x80041050)</span><span class="sxs-lookup"><span data-stu-id="87ddf-383">2147749968 (0x80041050)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-384">Se intentó cambiar un índice cuando las instancias o subclases ya usan el índice.</span><span class="sxs-lookup"><span data-stu-id="87ddf-384">An attempt was made to change an index when instances or subclasses are already using the index.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-385"><span id="WBEM_E_TOO_MANY_PROPERTIES"></span><span id="wbem_e_too_many_properties"></span>**propiedades de WBEM \_ E \_ demasiadas \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-385"><span id="WBEM_E_TOO_MANY_PROPERTIES"></span><span id="wbem_e_too_many_properties"></span>**WBEM\_E\_TOO\_MANY\_PROPERTIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-386">2147749969 (0x80041051)</span><span class="sxs-lookup"><span data-stu-id="87ddf-386">2147749969 (0x80041051)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-387">Se intentó crear más propiedades de las que admite la versión actual de la clase.</span><span class="sxs-lookup"><span data-stu-id="87ddf-387">Attempt was made to create more properties than the current version of the class supports.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-388"><span id="WBEM_E_UPDATE_TYPE_MISMATCH"></span><span id="wbem_e_update_type_mismatch"></span>**error \_ de \_ \_ coincidencia de tipo de actualización de WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-388"><span id="WBEM_E_UPDATE_TYPE_MISMATCH"></span><span id="wbem_e_update_type_mismatch"></span>**WBEM\_E\_UPDATE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-389">2147749970 (0x80041052)</span><span class="sxs-lookup"><span data-stu-id="87ddf-389">2147749970 (0x80041052)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-390">La propiedad se ha redefinido con un tipo en conflicto en una clase derivada.</span><span class="sxs-lookup"><span data-stu-id="87ddf-390">Property was redefined with a conflicting type in a derived class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-391"><span id="WBEM_E_UPDATE_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_update_override_not_allowed"></span>**\_no se \_ permite la \_ invalidación de la actualización WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-391"><span id="WBEM_E_UPDATE_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_update_override_not_allowed"></span>**WBEM\_E\_UPDATE\_OVERRIDE\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-392">2147749971 (0x80041053)</span><span class="sxs-lookup"><span data-stu-id="87ddf-392">2147749971 (0x80041053)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-393">Se intentó realizar una clase derivada para invalidar un calificador que no se puede invalidar.</span><span class="sxs-lookup"><span data-stu-id="87ddf-393">Attempt was made in a derived class to override a qualifier that cannot be overridden.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-394"><span id="WBEM_E_UPDATE_PROPAGATED_METHOD"></span><span id="wbem_e_update_propagated_method"></span>**\_ \_ \_ método propagado por la actualización de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-394"><span id="WBEM_E_UPDATE_PROPAGATED_METHOD"></span><span id="wbem_e_update_propagated_method"></span>**WBEM\_E\_UPDATE\_PROPAGATED\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-395">2147749972 (0x80041054)</span><span class="sxs-lookup"><span data-stu-id="87ddf-395">2147749972 (0x80041054)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-396">El método se ha vuelto a declarar con una signatura en conflicto en una clase derivada.</span><span class="sxs-lookup"><span data-stu-id="87ddf-396">Method was re-declared with a conflicting signature in a derived class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-397"><span id="WBEM_E_METHOD_NOT_IMPLEMENTED"></span><span id="wbem_e_method_not_implemented"></span>**\_método WBEM \_ E \_ no \_ implementado**</span><span class="sxs-lookup"><span data-stu-id="87ddf-397"><span id="WBEM_E_METHOD_NOT_IMPLEMENTED"></span><span id="wbem_e_method_not_implemented"></span>**WBEM\_E\_METHOD\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-398">2147749973 (0x80041055)</span><span class="sxs-lookup"><span data-stu-id="87ddf-398">2147749973 (0x80041055)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-399">Se intentó ejecutar un método no marcado con \[ implementado \] en cualquier clase relevante.</span><span class="sxs-lookup"><span data-stu-id="87ddf-399">Attempt was made to execute a method not marked with \[implemented\] in any relevant class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-400"><span id="WBEM_E_METHOD_DISABLED"></span><span id="wbem_e_method_disabled"></span>**WBEM \_ E \_ método \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="87ddf-400"><span id="WBEM_E_METHOD_DISABLED"></span><span id="wbem_e_method_disabled"></span>**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="87ddf-401"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="87ddf-401"><dt>


</dt> <dt></span></span>



<span data-ttu-id="87ddf-402">Se intentó ejecutar un método marcado con \[ deshabilitado \] .</span><span class="sxs-lookup"><span data-stu-id="87ddf-402">Attempt was made to execute a method marked with \[disabled\].</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-403"><span id="WBEM_E_REFRESHER_BUSY"></span><span id="wbem_e_refresher_busy"></span>**\_ \_ actualizador de WBEM E \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="87ddf-403"><span id="WBEM_E_REFRESHER_BUSY"></span><span id="wbem_e_refresher_busy"></span>**WBEM\_E\_REFRESHER\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-404">2147749975 (0x80041057)</span><span class="sxs-lookup"><span data-stu-id="87ddf-404">2147749975 (0x80041057)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-405">El actualizador está ocupado con otra operación.</span><span class="sxs-lookup"><span data-stu-id="87ddf-405">Refresher is busy with another operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-406"><span id="WBEM_E_UNPARSABLE_QUERY"></span><span id="wbem_e_unparsable_query"></span>**\_consulta no \_ analizable de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-406"><span id="WBEM_E_UNPARSABLE_QUERY"></span><span id="wbem_e_unparsable_query"></span>**WBEM\_E\_UNPARSABLE\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-407">2147749976 (0x80041058)</span><span class="sxs-lookup"><span data-stu-id="87ddf-407">2147749976 (0x80041058)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-408">La consulta de filtrado no es válida sintácticamente.</span><span class="sxs-lookup"><span data-stu-id="87ddf-408">Filtering query is syntactically not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-409"><span id="WBEM_E_NOT_EVENT_CLASS"></span><span id="wbem_e_not_event_class"></span>**WBEM \_ E \_ not \_ ( \_ clase de eventos)**</span><span class="sxs-lookup"><span data-stu-id="87ddf-409"><span id="WBEM_E_NOT_EVENT_CLASS"></span><span id="wbem_e_not_event_class"></span>**WBEM\_E\_NOT\_EVENT\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-410">2147749977 (0x80041059)</span><span class="sxs-lookup"><span data-stu-id="87ddf-410">2147749977 (0x80041059)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-411">La cláusula FROM de una consulta de filtrado hace referencia a una clase que no es una clase de eventos (no se deriva de [**\_ \_ Event**](--event.md)).</span><span class="sxs-lookup"><span data-stu-id="87ddf-411">The FROM clause of a filtering query references a class that is not an event class (not derived from [**\_\_Event**](--event.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-412"><span id="WBEM_E_MISSING_GROUP_WITHIN"></span><span id="wbem_e_missing_group_within"></span>**\_falta el \_ grupo de WBEM E \_ \_ en**</span><span class="sxs-lookup"><span data-stu-id="87ddf-412"><span id="WBEM_E_MISSING_GROUP_WITHIN"></span><span id="wbem_e_missing_group_within"></span>**WBEM\_E\_MISSING\_GROUP\_WITHIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-413">2147749978 (0x8004105A)</span><span class="sxs-lookup"><span data-stu-id="87ddf-413">2147749978 (0x8004105A)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-414">Se utilizó una cláusula GROUP BY sin la cláusula GROUP WITHIN correspondiente.</span><span class="sxs-lookup"><span data-stu-id="87ddf-414">A GROUP BY clause was used without the corresponding GROUP WITHIN clause.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-415"><span id="WBEM_E_MISSING_AGGREGATION_LIST"></span><span id="wbem_e_missing_aggregation_list"></span>**\_lista de \_ \_ agregación de WBEM E ausente \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-415"><span id="WBEM_E_MISSING_AGGREGATION_LIST"></span><span id="wbem_e_missing_aggregation_list"></span>**WBEM\_E\_MISSING\_AGGREGATION\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-416">2147749979 (0x8004105B)</span><span class="sxs-lookup"><span data-stu-id="87ddf-416">2147749979 (0x8004105B)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-417">Se utilizó una cláusula GROUP BY.</span><span class="sxs-lookup"><span data-stu-id="87ddf-417">A GROUP BY clause was used.</span></span> <span data-ttu-id="87ddf-418">No se admite la agregación en todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="87ddf-418">Aggregation on all properties is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-419"><span id="WBEM_E_PROPERTY_NOT_AN_OBJECT"></span><span id="wbem_e_property_not_an_object"></span>**la \_ propiedad WBEM E \_ \_ no es \_ un \_ objeto**</span><span class="sxs-lookup"><span data-stu-id="87ddf-419"><span id="WBEM_E_PROPERTY_NOT_AN_OBJECT"></span><span id="wbem_e_property_not_an_object"></span>**WBEM\_E\_PROPERTY\_NOT\_AN\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-420">2147749980 (0x8004105C)</span><span class="sxs-lookup"><span data-stu-id="87ddf-420">2147749980 (0x8004105C)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-421">Se utilizó la notación de punto en una propiedad que no es un objeto incrustado.</span><span class="sxs-lookup"><span data-stu-id="87ddf-421">Dot notation was used on a property that is not an embedded object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-422"><span id="WBEM_E_AGGREGATING_BY_OBJECT"></span><span id="wbem_e_aggregating_by_object"></span>**\_ \_ agregación de WBEM E \_ por \_ objeto**</span><span class="sxs-lookup"><span data-stu-id="87ddf-422"><span id="WBEM_E_AGGREGATING_BY_OBJECT"></span><span id="wbem_e_aggregating_by_object"></span>**WBEM\_E\_AGGREGATING\_BY\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-423">2147749981 (0x8004105D)</span><span class="sxs-lookup"><span data-stu-id="87ddf-423">2147749981 (0x8004105D)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-424">Una cláusula GROUP BY hace referencia a una propiedad que es un objeto incrustado sin utilizar la notación de punto.</span><span class="sxs-lookup"><span data-stu-id="87ddf-424">A GROUP BY clause references a property that is an embedded object without using dot notation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-425"><span id="WBEM_E_UNINTERPRETABLE_PROVIDER_QUERY"></span><span id="wbem_e_uninterpretable_provider_query"></span>**\_consulta de \_ proveedor no interpretable de WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-425"><span id="WBEM_E_UNINTERPRETABLE_PROVIDER_QUERY"></span><span id="wbem_e_uninterpretable_provider_query"></span>**WBEM\_E\_UNINTERPRETABLE\_PROVIDER\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-426">2147749983 (0x8004105F)</span><span class="sxs-lookup"><span data-stu-id="87ddf-426">2147749983 (0x8004105F)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-427">La consulta de registro de proveedor de eventos ([**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)) no especificó las clases para las que se proporcionaron eventos.</span><span class="sxs-lookup"><span data-stu-id="87ddf-427">Event provider registration query ([**\_\_EventProviderRegistration**](--eventproviderregistration.md)) did not specify the classes for which events were provided.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-428"><span id="WBEM_E_BACKUP_RESTORE_WINMGMT_RUNNING"></span><span id="wbem_e_backup_restore_winmgmt_running"></span>**WBEM \_ E \_ restauración de copia de seguridad de \_ WinMgmt en \_ \_ ejecución**</span><span class="sxs-lookup"><span data-stu-id="87ddf-428"><span id="WBEM_E_BACKUP_RESTORE_WINMGMT_RUNNING"></span><span id="wbem_e_backup_restore_winmgmt_running"></span>**WBEM\_E\_BACKUP\_RESTORE\_WINMGMT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-429">2147749984 (0x80041060)</span><span class="sxs-lookup"><span data-stu-id="87ddf-429">2147749984 (0x80041060)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-430">Se realizó una solicitud para realizar una copia de seguridad o restaurar el repositorio mientras estaba en uso por WinMgmt.exe, o por el proceso SVCHOST que contiene el servicio WMI.</span><span class="sxs-lookup"><span data-stu-id="87ddf-430">Request was made to back up or restore the repository while it was in use by WinMgmt.exe, or by the SVCHOST process that contains the WMI service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-431"><span id="WBEM_E_QUEUE_OVERFLOW"></span><span id="wbem_e_queue_overflow"></span>**desbordamiento de la \_ cola WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-431"><span id="WBEM_E_QUEUE_OVERFLOW"></span><span id="wbem_e_queue_overflow"></span>**WBEM\_E\_QUEUE\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-432">2147749985 (0x80041061)</span><span class="sxs-lookup"><span data-stu-id="87ddf-432">2147749985 (0x80041061)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-433">La cola de entrega asincrónica se ha desbordado del consumidor de eventos demasiado lento.</span><span class="sxs-lookup"><span data-stu-id="87ddf-433">Asynchronous delivery queue overflowed from the event consumer being too slow.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-434"><span id="WBEM_E_PRIVILEGE_NOT_HELD"></span><span id="wbem_e_privilege_not_held"></span>**\_privilegio E de WBEM \_ \_ no \_ contenida**</span><span class="sxs-lookup"><span data-stu-id="87ddf-434"><span id="WBEM_E_PRIVILEGE_NOT_HELD"></span><span id="wbem_e_privilege_not_held"></span>**WBEM\_E\_PRIVILEGE\_NOT\_HELD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-435">2147749986 (0x80041062)</span><span class="sxs-lookup"><span data-stu-id="87ddf-435">2147749986 (0x80041062)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-436">No se pudo realizar la operación porque el cliente no tenía los privilegios de seguridad necesarios.</span><span class="sxs-lookup"><span data-stu-id="87ddf-436">Operation failed because the client did not have the necessary security privilege.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-437"><span id="WBEM_E_INVALID_OPERATOR"></span><span id="wbem_e_invalid_operator"></span>**\_ \_ operador no válido de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-437"><span id="WBEM_E_INVALID_OPERATOR"></span><span id="wbem_e_invalid_operator"></span>**WBEM\_E\_INVALID\_OPERATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-438">2147749987 (0x80041063)</span><span class="sxs-lookup"><span data-stu-id="87ddf-438">2147749987 (0x80041063)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-439">El operador no es válido para este tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="87ddf-439">Operator is not valid for this property type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-440"><span id="WBEM_E_LOCAL_CREDENTIALS"></span><span id="wbem_e_local_credentials"></span>**\_ \_ credenciales locales de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-440"><span id="WBEM_E_LOCAL_CREDENTIALS"></span><span id="wbem_e_local_credentials"></span>**WBEM\_E\_LOCAL\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-441">2147749988 (0x80041064)</span><span class="sxs-lookup"><span data-stu-id="87ddf-441">2147749988 (0x80041064)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-442">El usuario especificó un nombre de usuario/contraseña/autoridad en una conexión local.</span><span class="sxs-lookup"><span data-stu-id="87ddf-442">User specified a username/password/authority on a local connection.</span></span> <span data-ttu-id="87ddf-443">El usuario debe usar un nombre de usuario y una contraseña en blanco y basarse en la seguridad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="87ddf-443">The user must use a blank username/password and rely on default security.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-444"><span id="WBEM_E_CANNOT_BE_ABSTRACT"></span><span id="wbem_e_cannot_be_abstract"></span>**WBEM \_ E \_ no puede \_ ser \_ abstracto**</span><span class="sxs-lookup"><span data-stu-id="87ddf-444"><span id="WBEM_E_CANNOT_BE_ABSTRACT"></span><span id="wbem_e_cannot_be_abstract"></span>**WBEM\_E\_CANNOT\_BE\_ABSTRACT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-445">2147749989 (0x80041065)</span><span class="sxs-lookup"><span data-stu-id="87ddf-445">2147749989 (0x80041065)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-446">La clase se hizo abstracta cuando su clase primaria no es abstracta.</span><span class="sxs-lookup"><span data-stu-id="87ddf-446">Class was made abstract when its parent class is not abstract.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-447"><span id="WBEM_E_AMENDED_OBJECT"></span><span id="wbem_e_amended_object"></span>**WBEM \_ E \_ \_ objeto modificado**</span><span class="sxs-lookup"><span data-stu-id="87ddf-447"><span id="WBEM_E_AMENDED_OBJECT"></span><span id="wbem_e_amended_object"></span>**WBEM\_E\_AMENDED\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-448">2147749990 (0x80041066)</span><span class="sxs-lookup"><span data-stu-id="87ddf-448">2147749990 (0x80041066)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-449">El objeto corregido se escribió sin la marca WBEM usar la marca de **\_ \_ \_ \_ calificadores modificados** que se está especificando.</span><span class="sxs-lookup"><span data-stu-id="87ddf-449">Amended object was written without the **WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS** flag being specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-450"><span id="WBEM_E_CLIENT_TOO_SLOW"></span><span id="wbem_e_client_too_slow"></span>**el \_ cliente WBEM E \_ \_ es demasiado \_ lento**</span><span class="sxs-lookup"><span data-stu-id="87ddf-450"><span id="WBEM_E_CLIENT_TOO_SLOW"></span><span id="wbem_e_client_too_slow"></span>**WBEM\_E\_CLIENT\_TOO\_SLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-451">2147749991 (0x80041067)</span><span class="sxs-lookup"><span data-stu-id="87ddf-451">2147749991 (0x80041067)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-452">El cliente no recuperó objetos con la rapidez suficiente de una enumeración.</span><span class="sxs-lookup"><span data-stu-id="87ddf-452">Client did not retrieve objects quickly enough from an enumeration.</span></span> <span data-ttu-id="87ddf-453">Esta constante se devuelve cuando un cliente crea un objeto de enumeración, pero no recupera objetos del enumerador a tiempo, lo que hace que las memorias caché del objeto del enumerador realicen una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="87ddf-453">This constant is returned when a client creates an enumeration object, but does not retrieve objects from the enumerator in a timely fashion, causing the enumerator's object caches to back up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-454"><span id="WBEM_E_NULL_SECURITY_DESCRIPTOR"></span><span id="wbem_e_null_security_descriptor"></span>**descriptor de seguridad de WBEM \_ E \_ null \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-454"><span id="WBEM_E_NULL_SECURITY_DESCRIPTOR"></span><span id="wbem_e_null_security_descriptor"></span>**WBEM\_E\_NULL\_SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-455">2147749992 (0x80041068)</span><span class="sxs-lookup"><span data-stu-id="87ddf-455">2147749992 (0x80041068)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-456">Se usó un descriptor de seguridad nulo.</span><span class="sxs-lookup"><span data-stu-id="87ddf-456">Null security descriptor was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-457"><span id="WBEM_E_TIMED_OUT"></span><span id="wbem_e_timed_out"></span>**se \_ \_ agotó el tiempo de \_ espera de WBEM E**</span><span class="sxs-lookup"><span data-stu-id="87ddf-457"><span id="WBEM_E_TIMED_OUT"></span><span id="wbem_e_timed_out"></span>**WBEM\_E\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-458">2147749993 (0x80041069)</span><span class="sxs-lookup"><span data-stu-id="87ddf-458">2147749993 (0x80041069)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-459">Se agotó el tiempo de espera de la operación.</span><span class="sxs-lookup"><span data-stu-id="87ddf-459">Operation timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-460"><span id="WBEM_E_INVALID_ASSOCIATION"></span><span id="wbem_e_invalid_association"></span>**Asociación de WBEM \_ E \_ no válida \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-460"><span id="WBEM_E_INVALID_ASSOCIATION"></span><span id="wbem_e_invalid_association"></span>**WBEM\_E\_INVALID\_ASSOCIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-461">2147749994</span><span class="sxs-lookup"><span data-stu-id="87ddf-461">2147749994</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-462">La asociación no es válida.</span><span class="sxs-lookup"><span data-stu-id="87ddf-462">Association is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-463"><span id="WBEM_E_AMBIGUOUS_OPERATION"></span><span id="wbem_e_ambiguous_operation"></span>**\_ \_ funcionamiento AMBIGUO de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-463"><span id="WBEM_E_AMBIGUOUS_OPERATION"></span><span id="wbem_e_ambiguous_operation"></span>**WBEM\_E\_AMBIGUOUS\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-464">2147749995 (0x8004106B)</span><span class="sxs-lookup"><span data-stu-id="87ddf-464">2147749995 (0x8004106B)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-465">La operación era ambigua.</span><span class="sxs-lookup"><span data-stu-id="87ddf-465">Operation was ambiguous.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-466"><span id="WBEM_E_QUOTA_VIOLATION"></span><span id="wbem_e_quota_violation"></span>**infracción de cuota de WBEM \_ E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-466"><span id="WBEM_E_QUOTA_VIOLATION"></span><span id="wbem_e_quota_violation"></span>**WBEM\_E\_QUOTA\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-467">2147749996 (0x8004106C)</span><span class="sxs-lookup"><span data-stu-id="87ddf-467">2147749996 (0x8004106C)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-468">WMI ocupa demasiada memoria.</span><span class="sxs-lookup"><span data-stu-id="87ddf-468">WMI is taking up too much memory.</span></span> <span data-ttu-id="87ddf-469">Esto puede deberse a una disponibilidad de memoria insuficiente o a un consumo excesivo de memoria por parte de WMI.</span><span class="sxs-lookup"><span data-stu-id="87ddf-469">This can be caused by low memory availability or excessive memory consumption by WMI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-470"><span id="WBEM_E_TRANSACTION_CONFLICT"></span><span id="wbem_e_transaction_conflict"></span>**conflicto de transacciones de WBEM \_ E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-470"><span id="WBEM_E_TRANSACTION_CONFLICT"></span><span id="wbem_e_transaction_conflict"></span>**WBEM\_E\_TRANSACTION\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-471">2147749997 (0x8004106D)</span><span class="sxs-lookup"><span data-stu-id="87ddf-471">2147749997 (0x8004106D)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-472">La operación provocó un conflicto de transacción.</span><span class="sxs-lookup"><span data-stu-id="87ddf-472">Operation resulted in a transaction conflict.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-473"><span id="WBEM_E_FORCED_ROLLBACK"></span><span id="wbem_e_forced_rollback"></span>**reversión forzada de WBEM \_ E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-473"><span id="WBEM_E_FORCED_ROLLBACK"></span><span id="wbem_e_forced_rollback"></span>**WBEM\_E\_FORCED\_ROLLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-474">2147749998 (0x8004106E)</span><span class="sxs-lookup"><span data-stu-id="87ddf-474">2147749998 (0x8004106E)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-475">La transacción forzó una reversión.</span><span class="sxs-lookup"><span data-stu-id="87ddf-475">Transaction forced a rollback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-476"><span id="WBEM_E_UNSUPPORTED_LOCALE"></span><span id="wbem_e_unsupported_locale"></span>**\_ \_ configuración regional no admitida de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-476"><span id="WBEM_E_UNSUPPORTED_LOCALE"></span><span id="wbem_e_unsupported_locale"></span>**WBEM\_E\_UNSUPPORTED\_LOCALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-477">2147749999 (0x8004106F)</span><span class="sxs-lookup"><span data-stu-id="87ddf-477">2147749999 (0x8004106F)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-478">La configuración regional usada en la llamada no es compatible.</span><span class="sxs-lookup"><span data-stu-id="87ddf-478">Locale used in the call is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-479"><span id="WBEM_E_HANDLE_OUT_OF_DATE"></span><span id="wbem_e_handle_out_of_date"></span>**\_controlador de WBEM E no \_ \_ \_ \_ actualizado**</span><span class="sxs-lookup"><span data-stu-id="87ddf-479"><span id="WBEM_E_HANDLE_OUT_OF_DATE"></span><span id="wbem_e_handle_out_of_date"></span>**WBEM\_E\_HANDLE\_OUT\_OF\_DATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-480">2147750000 (0x80041070)</span><span class="sxs-lookup"><span data-stu-id="87ddf-480">2147750000 (0x80041070)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-481">El identificador de objeto no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="87ddf-481">Object handle is out-of-date.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-482"><span id="WBEM_E_CONNECTION_FAILED"></span><span id="wbem_e_connection_failed"></span>**error de conexión de WBEM \_ E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-482"><span id="WBEM_E_CONNECTION_FAILED"></span><span id="wbem_e_connection_failed"></span>**WBEM\_E\_CONNECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-483">2147750001 (0x80041071)</span><span class="sxs-lookup"><span data-stu-id="87ddf-483">2147750001 (0x80041071)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-484">Error en la conexión con la base de datos SQL.</span><span class="sxs-lookup"><span data-stu-id="87ddf-484">Connection to the SQL database failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-485"><span id="WBEM_E_INVALID_HANDLE_REQUEST"></span><span id="wbem_e_invalid_handle_request"></span>**\_solicitud de \_ identificador no válida de \_ WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-485"><span id="WBEM_E_INVALID_HANDLE_REQUEST"></span><span id="wbem_e_invalid_handle_request"></span>**WBEM\_E\_INVALID\_HANDLE\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-486">2147750002 (0x80041072)</span><span class="sxs-lookup"><span data-stu-id="87ddf-486">2147750002 (0x80041072)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-487">La solicitud de administración no era válida.</span><span class="sxs-lookup"><span data-stu-id="87ddf-487">Handle request was not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-488"><span id="WBEM_E_PROPERTY_NAME_TOO_WIDE"></span><span id="wbem_e_property_name_too_wide"></span>**nombre de propiedad de WBEM \_ E \_ \_ \_ demasiado \_ ancho**</span><span class="sxs-lookup"><span data-stu-id="87ddf-488"><span id="WBEM_E_PROPERTY_NAME_TOO_WIDE"></span><span id="wbem_e_property_name_too_wide"></span>**WBEM\_E\_PROPERTY\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-489">2147750003 (0x80041073)</span><span class="sxs-lookup"><span data-stu-id="87ddf-489">2147750003 (0x80041073)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-490">El nombre de la propiedad contiene más de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="87ddf-490">Property name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-491"><span id="WBEM_E_CLASS_NAME_TOO_WIDE"></span><span id="wbem_e_class_name_too_wide"></span>**nombre de clase de WBEM \_ E \_ \_ \_ demasiado \_ ancho**</span><span class="sxs-lookup"><span data-stu-id="87ddf-491"><span id="WBEM_E_CLASS_NAME_TOO_WIDE"></span><span id="wbem_e_class_name_too_wide"></span>**WBEM\_E\_CLASS\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-492">2147750004 (0x80041074)</span><span class="sxs-lookup"><span data-stu-id="87ddf-492">2147750004 (0x80041074)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-493">El nombre de clase contiene más de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="87ddf-493">Class name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-494"><span id="WBEM_E_METHOD_NAME_TOO_WIDE"></span><span id="wbem_e_method_name_too_wide"></span>**nombre del método de WBEM \_ E \_ \_ \_ demasiado \_ ancho**</span><span class="sxs-lookup"><span data-stu-id="87ddf-494"><span id="WBEM_E_METHOD_NAME_TOO_WIDE"></span><span id="wbem_e_method_name_too_wide"></span>**WBEM\_E\_METHOD\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-495">2147750005 (0x80041075)</span><span class="sxs-lookup"><span data-stu-id="87ddf-495">2147750005 (0x80041075)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-496">El nombre del método contiene más de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="87ddf-496">Method name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-497"><span id="WBEM_E_QUALIFIER_NAME_TOO_WIDE"></span><span id="wbem_e_qualifier_name_too_wide"></span>**\_ \_ el nombre del calificador de WBEM E \_ \_ es demasiado \_ amplio**</span><span class="sxs-lookup"><span data-stu-id="87ddf-497"><span id="WBEM_E_QUALIFIER_NAME_TOO_WIDE"></span><span id="wbem_e_qualifier_name_too_wide"></span>**WBEM\_E\_QUALIFIER\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-498">2147750006 (0x80041076)</span><span class="sxs-lookup"><span data-stu-id="87ddf-498">2147750006 (0x80041076)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-499">El nombre del calificador contiene más de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="87ddf-499">Qualifier name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-500"><span id="WBEM_E_RERUN_COMMAND"></span><span id="wbem_e_rerun_command"></span>**\_ \_ comando volver a ejecutar WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-500"><span id="WBEM_E_RERUN_COMMAND"></span><span id="wbem_e_rerun_command"></span>**WBEM\_E\_RERUN\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-501">2147750007 (0x80041077)</span><span class="sxs-lookup"><span data-stu-id="87ddf-501">2147750007 (0x80041077)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-502">El comando SQL debe volver a ejecutarse porque hay un interbloqueo en SQL.</span><span class="sxs-lookup"><span data-stu-id="87ddf-502">The SQL command must be rerun because there is a deadlock in SQL.</span></span> <span data-ttu-id="87ddf-503">Solo se puede devolver cuando los datos se almacenan en una base de datos SQL.</span><span class="sxs-lookup"><span data-stu-id="87ddf-503">This can be returned only when data is being stored in an SQL database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-504"><span id="WBEM_E_DATABASE_VER_MISMATCH"></span><span id="wbem_e_database_ver_mismatch"></span>**versión de base de datos de WBEM \_ E \_ \_ \_ no coincidente**</span><span class="sxs-lookup"><span data-stu-id="87ddf-504"><span id="WBEM_E_DATABASE_VER_MISMATCH"></span><span id="wbem_e_database_ver_mismatch"></span>**WBEM\_E\_DATABASE\_VER\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-505">2147750008 (0x80041078)</span><span class="sxs-lookup"><span data-stu-id="87ddf-505">2147750008 (0x80041078)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-506">La versión de la base de datos no coincide con la versión que procesa el controlador del repositorio.</span><span class="sxs-lookup"><span data-stu-id="87ddf-506">The database version does not match the version that the repository driver processes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-507"><span id="WBEM_E_VETO_DELETE"></span><span id="wbem_e_veto_delete"></span>**WBEM \_ E \_ veto \_ eliminar**</span><span class="sxs-lookup"><span data-stu-id="87ddf-507"><span id="WBEM_E_VETO_DELETE"></span><span id="wbem_e_veto_delete"></span>**WBEM\_E\_VETO\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-508">2147750009 (0x80041079)</span><span class="sxs-lookup"><span data-stu-id="87ddf-508">2147750009 (0x80041079)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-509">WMI no puede ejecutar la operación de eliminación porque el proveedor no la permite.</span><span class="sxs-lookup"><span data-stu-id="87ddf-509">WMI cannot execute the delete operation because the provider does not allow it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-510"><span id="WBEM_E_VETO_PUT"></span><span id="wbem_e_veto_put"></span>**WBEM \_ E \_ veto \_ Put**</span><span class="sxs-lookup"><span data-stu-id="87ddf-510"><span id="WBEM_E_VETO_PUT"></span><span id="wbem_e_veto_put"></span>**WBEM\_E\_VETO\_PUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-511">2147750010 (0x8004107A)</span><span class="sxs-lookup"><span data-stu-id="87ddf-511">2147750010 (0x8004107A)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-512">WMI no puede ejecutar la operación PUT porque el proveedor no lo permite.</span><span class="sxs-lookup"><span data-stu-id="87ddf-512">WMI cannot execute the put operation because the provider does not allow it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-513"><span id="WBEM_E_INVALID_LOCALE"></span><span id="wbem_e_invalid_locale"></span>**\_ \_ configuración regional no válida de WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-513"><span id="WBEM_E_INVALID_LOCALE"></span><span id="wbem_e_invalid_locale"></span>**WBEM\_E\_INVALID\_LOCALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-514">2147750016 (0x80041080)</span><span class="sxs-lookup"><span data-stu-id="87ddf-514">2147750016 (0x80041080)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-515">El identificador de configuración regional especificado no era válido para la operación.</span><span class="sxs-lookup"><span data-stu-id="87ddf-515">Specified locale identifier was not valid for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-516"><span id="WBEM_E_PROVIDER_SUSPENDED"></span><span id="wbem_e_provider_suspended"></span>**proveedor de WBEM \_ E \_ \_ suspendido**</span><span class="sxs-lookup"><span data-stu-id="87ddf-516"><span id="WBEM_E_PROVIDER_SUSPENDED"></span><span id="wbem_e_provider_suspended"></span>**WBEM\_E\_PROVIDER\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-517">2147750017 (0x80041081)</span><span class="sxs-lookup"><span data-stu-id="87ddf-517">2147750017 (0x80041081)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-518">El proveedor está suspendido.</span><span class="sxs-lookup"><span data-stu-id="87ddf-518">Provider is suspended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-519"><span id="WBEM_E_SYNCHRONIZATION_REQUIRED"></span><span id="wbem_e_synchronization_required"></span>**se \_ \_ requiere la sincronización \_ de WBEM E**</span><span class="sxs-lookup"><span data-stu-id="87ddf-519"><span id="WBEM_E_SYNCHRONIZATION_REQUIRED"></span><span id="wbem_e_synchronization_required"></span>**WBEM\_E\_SYNCHRONIZATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-520">2147750018 (0x80041082)</span><span class="sxs-lookup"><span data-stu-id="87ddf-520">2147750018 (0x80041082)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-521">El objeto debe escribirse en el repositorio WMI y volver a recuperarse antes de que la operación solicitada pueda realizarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="87ddf-521">Object must be written to the WMI repository and retrieved again before the requested operation can succeed.</span></span> <span data-ttu-id="87ddf-522">Se devuelve esta constante cuando se debe confirmar y recuperar un objeto para ver el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="87ddf-522">This constant is returned when an object must be committed and retrieved to see the property value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-523"><span id="WBEM_E_NO_SCHEMA"></span><span id="wbem_e_no_schema"></span>**WBEM \_ E \_ no \_ esquema**</span><span class="sxs-lookup"><span data-stu-id="87ddf-523"><span id="WBEM_E_NO_SCHEMA"></span><span id="wbem_e_no_schema"></span>**WBEM\_E\_NO\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-524">2147750019 (0x80041083)</span><span class="sxs-lookup"><span data-stu-id="87ddf-524">2147750019 (0x80041083)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-525">No se puede completar la operación; no hay ningún esquema disponible.</span><span class="sxs-lookup"><span data-stu-id="87ddf-525">Operation cannot be completed; no schema is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-526"><span id="WBEM_E_PROVIDER_ALREADY_REGISTERED"></span><span id="wbem_e_provider_already_registered"></span>**proveedor de WBEM \_ E \_ \_ ya \_ registrado**</span><span class="sxs-lookup"><span data-stu-id="87ddf-526"><span id="WBEM_E_PROVIDER_ALREADY_REGISTERED"></span><span id="wbem_e_provider_already_registered"></span>**WBEM\_E\_PROVIDER\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-527">02147750020 (0x119FD010)</span><span class="sxs-lookup"><span data-stu-id="87ddf-527">02147750020 (0x119FD010)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-528">No se puede registrar el proveedor porque ya está registrado.</span><span class="sxs-lookup"><span data-stu-id="87ddf-528">Provider cannot be registered because it is already registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-529"><span id="WBEM_E_PROVIDER_NOT_REGISTERED"></span><span id="wbem_e_provider_not_registered"></span>**proveedor de WBEM \_ E \_ \_ no \_ registrado**</span><span class="sxs-lookup"><span data-stu-id="87ddf-529"><span id="WBEM_E_PROVIDER_NOT_REGISTERED"></span><span id="wbem_e_provider_not_registered"></span>**WBEM\_E\_PROVIDER\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-530">2147750021 (0x80041085)</span><span class="sxs-lookup"><span data-stu-id="87ddf-530">2147750021 (0x80041085)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-531">No se registró el proveedor.</span><span class="sxs-lookup"><span data-stu-id="87ddf-531">Provider was not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-532"><span id="WBEM_E_FATAL_TRANSPORT_ERROR"></span><span id="wbem_e_fatal_transport_error"></span>**\_error de \_ \_ transporte fatal \_ de WBEM E**</span><span class="sxs-lookup"><span data-stu-id="87ddf-532"><span id="WBEM_E_FATAL_TRANSPORT_ERROR"></span><span id="wbem_e_fatal_transport_error"></span>**WBEM\_E\_FATAL\_TRANSPORT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-533">2147750022 (0x80041086)</span><span class="sxs-lookup"><span data-stu-id="87ddf-533">2147750022 (0x80041086)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-534">Se produjo un error grave de transporte.</span><span class="sxs-lookup"><span data-stu-id="87ddf-534">A fatal transport error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-535"><span id="WBEM_E_ENCRYPTED_CONNECTION_REQUIRED"></span><span id="wbem_e_encrypted_connection_required"></span>**se \_ \_ requiere la \_ conexión cifrada WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-535"><span id="WBEM_E_ENCRYPTED_CONNECTION_REQUIRED"></span><span id="wbem_e_encrypted_connection_required"></span>**WBEM\_E\_ENCRYPTED\_CONNECTION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-536">2147750023 (0x80041087)</span><span class="sxs-lookup"><span data-stu-id="87ddf-536">2147750023 (0x80041087)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-537">El usuario intentó establecer un nombre de equipo o dominio sin una conexión cifrada.</span><span class="sxs-lookup"><span data-stu-id="87ddf-537">User attempted to set a computer name or domain without an encrypted connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-538"><span id="WBEM_E_PROVIDER_TIMED_OUT"></span><span id="wbem_e_provider_timed_out"></span>**se \_ \_ \_ agotó el tiempo de \_ espera del proveedor de WBEM E**</span><span class="sxs-lookup"><span data-stu-id="87ddf-538"><span id="WBEM_E_PROVIDER_TIMED_OUT"></span><span id="wbem_e_provider_timed_out"></span>**WBEM\_E\_PROVIDER\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-539">2147750024 (0x80041088)</span><span class="sxs-lookup"><span data-stu-id="87ddf-539">2147750024 (0x80041088)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-540">Un proveedor no pudo informar de los resultados en el tiempo de espera especificado.</span><span class="sxs-lookup"><span data-stu-id="87ddf-540">A provider failed to report results within the specified timeout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-541"><span id="WBEM_E_NO_KEY"></span><span id="wbem_e_no_key"></span>**WBEM \_ E \_ no \_ clave**</span><span class="sxs-lookup"><span data-stu-id="87ddf-541"><span id="WBEM_E_NO_KEY"></span><span id="wbem_e_no_key"></span>**WBEM\_E\_NO\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-542">2147750025 (0x80041089)</span><span class="sxs-lookup"><span data-stu-id="87ddf-542">2147750025 (0x80041089)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-543">El usuario intentó colocar una instancia sin ninguna clave definida.</span><span class="sxs-lookup"><span data-stu-id="87ddf-543">User attempted to put an instance with no defined key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-544"><span id="WBEM_E_PROVIDER_DISABLED"></span><span id="wbem_e_provider_disabled"></span>**proveedor de WBEM \_ E \_ \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="87ddf-544"><span id="WBEM_E_PROVIDER_DISABLED"></span><span id="wbem_e_provider_disabled"></span>**WBEM\_E\_PROVIDER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-545">2147750026 (0x8004108A)</span><span class="sxs-lookup"><span data-stu-id="87ddf-545">2147750026 (0x8004108A)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-546">El usuario intentó registrar una instancia de proveedor, pero se descargó el servidor COM para la instancia del proveedor.</span><span class="sxs-lookup"><span data-stu-id="87ddf-546">User attempted to register a provider instance but the COM server for the provider instance was unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-547"><span id="WBEMESS_E_REGISTRATION_TOO_BROAD"></span><span id="wbemess_e_registration_too_broad"></span>**el \_ registro de WBEMESS E \_ \_ es demasiado \_ amplio**</span><span class="sxs-lookup"><span data-stu-id="87ddf-547"><span id="WBEMESS_E_REGISTRATION_TOO_BROAD"></span><span id="wbemess_e_registration_too_broad"></span>**WBEMESS\_E\_REGISTRATION\_TOO\_BROAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-548">2147753985 (0x80042001)</span><span class="sxs-lookup"><span data-stu-id="87ddf-548">2147753985 (0x80042001)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-549">El registro del proveedor se superpone con el dominio de eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="87ddf-549">Provider registration overlaps with the system event domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-550"><span id="WBEMESS_E_REGISTRATION_TOO_PRECISE"></span><span id="wbemess_e_registration_too_precise"></span>**WBEMESS \_ E \_ Registro \_ demasiado \_ preciso**</span><span class="sxs-lookup"><span data-stu-id="87ddf-550"><span id="WBEMESS_E_REGISTRATION_TOO_PRECISE"></span><span id="wbemess_e_registration_too_precise"></span>**WBEMESS\_E\_REGISTRATION\_TOO\_PRECISE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-551">2147753986 (0x80042002)</span><span class="sxs-lookup"><span data-stu-id="87ddf-551">2147753986 (0x80042002)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-552">No se utilizó una cláusula WITHIN en esta consulta.</span><span class="sxs-lookup"><span data-stu-id="87ddf-552">A WITHIN clause was not used in this query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-553"><span id="WBEMESS_E_AUTHZ_NOT_PRIVILEGED"></span><span id="wbemess_e_authz_not_privileged"></span>**WBEMESS \_ E \_ AUTHZ \_ no tiene \_ privilegios**</span><span class="sxs-lookup"><span data-stu-id="87ddf-553"><span id="WBEMESS_E_AUTHZ_NOT_PRIVILEGED"></span><span id="wbemess_e_authz_not_privileged"></span>**WBEMESS\_E\_AUTHZ\_NOT\_PRIVILEGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-554">2147753987 (0x80042003)</span><span class="sxs-lookup"><span data-stu-id="87ddf-554">2147753987 (0x80042003)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-555">Este equipo no tiene los permisos de dominio necesarios para admitir las funciones de seguridad relacionadas con la instancia de suscripción creada.</span><span class="sxs-lookup"><span data-stu-id="87ddf-555">This computer does not have the necessary domain permissions to support the security functions that relate to the created subscription instance.</span></span> <span data-ttu-id="87ddf-556">Póngase en contacto con el administrador del dominio para agregar este equipo al grupo de acceso de autorización de Windows.</span><span class="sxs-lookup"><span data-stu-id="87ddf-556">Contact the Domain Administrator to get this computer added to the Windows Authorization Access Group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-557"><span id="WBEM_E_RETRY_LATER"></span><span id="wbem_e_retry_later"></span>**WBEM \_ E \_ inténtelo de nuevo \_ más tarde**</span><span class="sxs-lookup"><span data-stu-id="87ddf-557"><span id="WBEM_E_RETRY_LATER"></span><span id="wbem_e_retry_later"></span>**WBEM\_E\_RETRY\_LATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-558">2147758081 (0x80043001)</span><span class="sxs-lookup"><span data-stu-id="87ddf-558">2147758081 (0x80043001)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-559">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="87ddf-559">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-560"><span id="WBEM_E_RESOURCE_CONTENTION"></span><span id="wbem_e_resource_contention"></span>**contención de recursos de WBEM \_ E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-560"><span id="WBEM_E_RESOURCE_CONTENTION"></span><span id="wbem_e_resource_contention"></span>**WBEM\_E\_RESOURCE\_CONTENTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-561">2147758082 (0x80043002)</span><span class="sxs-lookup"><span data-stu-id="87ddf-561">2147758082 (0x80043002)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-562">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="87ddf-562">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-563"><span id="WBEMMOF_E_EXPECTED_QUALIFIER_NAME"></span><span id="wbemmof_e_expected_qualifier_name"></span>**WBEMMOF \_ E \_ esperaba \_ el nombre del calificador \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-563"><span id="WBEMMOF_E_EXPECTED_QUALIFIER_NAME"></span><span id="wbemmof_e_expected_qualifier_name"></span>**WBEMMOF\_E\_EXPECTED\_QUALIFIER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-564">2147762177 (0x80044001)</span><span class="sxs-lookup"><span data-stu-id="87ddf-564">2147762177 (0x80044001)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-565">Se esperaba un nombre de calificador.</span><span class="sxs-lookup"><span data-stu-id="87ddf-565">Expected a qualifier name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-566"><span id="WBEMMOF_E_EXPECTED_SEMI"></span><span id="wbemmof_e_expected_semi"></span>**WBEMMOF \_ E \_ esperaba \_ semi**</span><span class="sxs-lookup"><span data-stu-id="87ddf-566"><span id="WBEMMOF_E_EXPECTED_SEMI"></span><span id="wbemmof_e_expected_semi"></span>**WBEMMOF\_E\_EXPECTED\_SEMI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-567">2147762178 (0x80044002)</span><span class="sxs-lookup"><span data-stu-id="87ddf-567">2147762178 (0x80044002)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-568">Se esperaba un punto y coma o ' = '.</span><span class="sxs-lookup"><span data-stu-id="87ddf-568">Expected semicolon or '='.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-569"><span id="WBEMMOF_E_EXPECTED_OPEN_BRACE"></span><span id="wbemmof_e_expected_open_brace"></span>**WBEMMOF \_ E \_ esperaba \_ una \_ llave de apertura**</span><span class="sxs-lookup"><span data-stu-id="87ddf-569"><span id="WBEMMOF_E_EXPECTED_OPEN_BRACE"></span><span id="wbemmof_e_expected_open_brace"></span>**WBEMMOF\_E\_EXPECTED\_OPEN\_BRACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-570">2147762179 (0x80044003)</span><span class="sxs-lookup"><span data-stu-id="87ddf-570">2147762179 (0x80044003)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-571">Se esperaba una llave de apertura.</span><span class="sxs-lookup"><span data-stu-id="87ddf-571">Expected an opening brace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-572"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACE"></span><span id="wbemmof_e_expected_close_brace"></span>**WBEMMOF \_ E \_ esperaba \_ llave de cierre \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-572"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACE"></span><span id="wbemmof_e_expected_close_brace"></span>**WBEMMOF\_E\_EXPECTED\_CLOSE\_BRACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-573">2147762180 (0x80044004)</span><span class="sxs-lookup"><span data-stu-id="87ddf-573">2147762180 (0x80044004)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-574">Falta una llave de cierre o un elemento de matriz no válido.</span><span class="sxs-lookup"><span data-stu-id="87ddf-574">Missing closing brace or an illegal array element.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-575"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACKET"></span><span id="wbemmof_e_expected_close_bracket"></span>**WBEMMOF \_ E \_ \_ \_ corchete de cierre esperado**</span><span class="sxs-lookup"><span data-stu-id="87ddf-575"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACKET"></span><span id="wbemmof_e_expected_close_bracket"></span>**WBEMMOF\_E\_EXPECTED\_CLOSE\_BRACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-576">2147762181 (0x80044005)</span><span class="sxs-lookup"><span data-stu-id="87ddf-576">2147762181 (0x80044005)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-577">Se esperaba un corchete de cierre.</span><span class="sxs-lookup"><span data-stu-id="87ddf-577">Expected a closing bracket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-578"><span id="WBEMMOF_E_EXPECTED_CLOSE_PAREN"></span><span id="wbemmof_e_expected_close_paren"></span>**WBEMMOF \_ E \_ espera \_ cerrar \_ paréntesis**</span><span class="sxs-lookup"><span data-stu-id="87ddf-578"><span id="WBEMMOF_E_EXPECTED_CLOSE_PAREN"></span><span id="wbemmof_e_expected_close_paren"></span>**WBEMMOF\_E\_EXPECTED\_CLOSE\_PAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-579">2147762182 (0x80044006)</span><span class="sxs-lookup"><span data-stu-id="87ddf-579">2147762182 (0x80044006)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-580">Paréntesis de cierre esperado.</span><span class="sxs-lookup"><span data-stu-id="87ddf-580">Expected closing parenthesis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-581"><span id="WBEMMOF_E_ILLEGAL_CONSTANT_VALUE"></span><span id="wbemmof_e_illegal_constant_value"></span>**WBEMMOF \_ E \_ \_ valor constante no válido \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-581"><span id="WBEMMOF_E_ILLEGAL_CONSTANT_VALUE"></span><span id="wbemmof_e_illegal_constant_value"></span>**WBEMMOF\_E\_ILLEGAL\_CONSTANT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-582">2147762183 (0x80044007)</span><span class="sxs-lookup"><span data-stu-id="87ddf-582">2147762183 (0x80044007)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-583">Valor numérico fuera del intervalo o cadenas sin comillas.</span><span class="sxs-lookup"><span data-stu-id="87ddf-583">Numeric value out of range or strings without quotes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-584"><span id="WBEMMOF_E_EXPECTED_TYPE_IDENTIFIER"></span><span id="wbemmof_e_expected_type_identifier"></span>**WBEMMOF \_ E \_ esperaba \_ un \_ identificador de tipo**</span><span class="sxs-lookup"><span data-stu-id="87ddf-584"><span id="WBEMMOF_E_EXPECTED_TYPE_IDENTIFIER"></span><span id="wbemmof_e_expected_type_identifier"></span>**WBEMMOF\_E\_EXPECTED\_TYPE\_IDENTIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-585">2147762184 (0x80044008)</span><span class="sxs-lookup"><span data-stu-id="87ddf-585">2147762184 (0x80044008)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-586">Se esperaba un identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="87ddf-586">Expected a type identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-587"><span id="WBEMMOF_E_EXPECTED_OPEN_PAREN"></span><span id="wbemmof_e_expected_open_paren"></span>**WBEMMOF \_ E \_ esperaba \_ un \_ paréntesis abierto**</span><span class="sxs-lookup"><span data-stu-id="87ddf-587"><span id="WBEMMOF_E_EXPECTED_OPEN_PAREN"></span><span id="wbemmof_e_expected_open_paren"></span>**WBEMMOF\_E\_EXPECTED\_OPEN\_PAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-588">2147762185 (0x80044009)</span><span class="sxs-lookup"><span data-stu-id="87ddf-588">2147762185 (0x80044009)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-589">Se esperaba un paréntesis de apertura.</span><span class="sxs-lookup"><span data-stu-id="87ddf-589">Expected an open parenthesis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-590"><span id="WBEMMOF_E_UNRECOGNIZED_TOKEN"></span><span id="wbemmof_e_unrecognized_token"></span>**WBEMMOF \_ \_ \_ token desconocido**</span><span class="sxs-lookup"><span data-stu-id="87ddf-590"><span id="WBEMMOF_E_UNRECOGNIZED_TOKEN"></span><span id="wbemmof_e_unrecognized_token"></span>**WBEMMOF\_E\_UNRECOGNIZED\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-591">2147762186 (0x8004400A)</span><span class="sxs-lookup"><span data-stu-id="87ddf-591">2147762186 (0x8004400A)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-592">Token inesperado en el archivo.</span><span class="sxs-lookup"><span data-stu-id="87ddf-592">Unexpected token in the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-593"><span id="WBEMMOF_E_UNRECOGNIZED_TYPE"></span><span id="wbemmof_e_unrecognized_type"></span>**WBEMMOF \_ \_ \_ tipo desconocido**</span><span class="sxs-lookup"><span data-stu-id="87ddf-593"><span id="WBEMMOF_E_UNRECOGNIZED_TYPE"></span><span id="wbemmof_e_unrecognized_type"></span>**WBEMMOF\_E\_UNRECOGNIZED\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-594">2147762187 (0x8004400B)</span><span class="sxs-lookup"><span data-stu-id="87ddf-594">2147762187 (0x8004400B)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-595">Identificador de tipo no reconocido o no admitido.</span><span class="sxs-lookup"><span data-stu-id="87ddf-595">Unrecognized or unsupported type identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-596"><span id="WBEMMOF_E_EXPECTED_PROPERTY_NAME"></span><span id="wbemmof_e_expected_property_name"></span>**WBEMMOF \_ E \_ esperaba \_ \_ el nombre de la propiedad**</span><span class="sxs-lookup"><span data-stu-id="87ddf-596"><span id="WBEMMOF_E_EXPECTED_PROPERTY_NAME"></span><span id="wbemmof_e_expected_property_name"></span>**WBEMMOF\_E\_EXPECTED\_PROPERTY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-597">2147762187 (0x8004400B)</span><span class="sxs-lookup"><span data-stu-id="87ddf-597">2147762187 (0x8004400B)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-598">Se esperaba un nombre de método o propiedad.</span><span class="sxs-lookup"><span data-stu-id="87ddf-598">Expected property or method name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-599"><span id="WBEMMOF_E_TYPEDEF_NOT_SUPPORTED"></span><span id="wbemmof_e_typedef_not_supported"></span>**\_no se \_ admite la definición \_ \_ de tipo WBEMMOF E**</span><span class="sxs-lookup"><span data-stu-id="87ddf-599"><span id="WBEMMOF_E_TYPEDEF_NOT_SUPPORTED"></span><span id="wbemmof_e_typedef_not_supported"></span>**WBEMMOF\_E\_TYPEDEF\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-600">2147762189 (0x8004400D)</span><span class="sxs-lookup"><span data-stu-id="87ddf-600">2147762189 (0x8004400D)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-601">No se admiten definiciones de tipo y tipos enumerados.</span><span class="sxs-lookup"><span data-stu-id="87ddf-601">Typedefs and enumerated types are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-602"><span id="WBEMMOF_E_UNEXPECTED_ALIAS"></span><span id="wbemmof_e_unexpected_alias"></span>**WBEMMOF \_ \_ alias inesperado \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-602"><span id="WBEMMOF_E_UNEXPECTED_ALIAS"></span><span id="wbemmof_e_unexpected_alias"></span>**WBEMMOF\_E\_UNEXPECTED\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-603">2147762190 (0x8004400E)</span><span class="sxs-lookup"><span data-stu-id="87ddf-603">2147762190 (0x8004400E)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-604">Solo una referencia a un objeto de clase puede tener un valor de alias.</span><span class="sxs-lookup"><span data-stu-id="87ddf-604">Only a reference to a class object can have an alias value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-605"><span id="WBEMMOF_E_UNEXPECTED_ARRAY_INIT"></span><span id="wbemmof_e_unexpected_array_init"></span>**WBEMMOF \_ E \_ inesperada \_ init de matriz \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-605"><span id="WBEMMOF_E_UNEXPECTED_ARRAY_INIT"></span><span id="wbemmof_e_unexpected_array_init"></span>**WBEMMOF\_E\_UNEXPECTED\_ARRAY\_INIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-606">2147762191 (0x8004400F)</span><span class="sxs-lookup"><span data-stu-id="87ddf-606">2147762191 (0x8004400F)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-607">Inicialización de matriz inesperada.</span><span class="sxs-lookup"><span data-stu-id="87ddf-607">Unexpected array initialization.</span></span> <span data-ttu-id="87ddf-608">Las matrices se deben declarar con \[ \] .</span><span class="sxs-lookup"><span data-stu-id="87ddf-608">Arrays must be declared with \[\].</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-609"><span id="WBEMMOF_E_INVALID_AMENDMENT_SYNTAX"></span><span id="wbemmof_e_invalid_amendment_syntax"></span>**WBEMMOF \_ \_ Sintaxis de \_ modificación no válida \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-609"><span id="WBEMMOF_E_INVALID_AMENDMENT_SYNTAX"></span><span id="wbemmof_e_invalid_amendment_syntax"></span>**WBEMMOF\_E\_INVALID\_AMENDMENT\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-610">2147762192 (0x80044010)</span><span class="sxs-lookup"><span data-stu-id="87ddf-610">2147762192 (0x80044010)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-611">La sintaxis de la ruta de acceso del espacio de nombres no es válida.</span><span class="sxs-lookup"><span data-stu-id="87ddf-611">Namespace path syntax is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-612"><span id="WBEMMOF_E_INVALID_DUPLICATE_AMENDMENT"></span><span id="wbemmof_e_invalid_duplicate_amendment"></span>**WBEMMOF \_ E \_ \_ modificación de duplicación no válida \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-612"><span id="WBEMMOF_E_INVALID_DUPLICATE_AMENDMENT"></span><span id="wbemmof_e_invalid_duplicate_amendment"></span>**WBEMMOF\_E\_INVALID\_DUPLICATE\_AMENDMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-613">2147762193 (0x80044011)</span><span class="sxs-lookup"><span data-stu-id="87ddf-613">2147762193 (0x80044011)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-614">Especificadores de modificación duplicados.</span><span class="sxs-lookup"><span data-stu-id="87ddf-614">Duplicate amendment specifiers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-615"><span id="WBEMMOF_E_INVALID_PRAGMA"></span><span id="wbemmof_e_invalid_pragma"></span>**WBEMMOF \_ \_ Pragma no válido \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-615"><span id="WBEMMOF_E_INVALID_PRAGMA"></span><span id="wbemmof_e_invalid_pragma"></span>**WBEMMOF\_E\_INVALID\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-616">2147762194 (0x80044012)</span><span class="sxs-lookup"><span data-stu-id="87ddf-616">2147762194 (0x80044012)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-617">[ \# pragma](pragma-namespace.md) debe ir seguida de una palabra clave válida.</span><span class="sxs-lookup"><span data-stu-id="87ddf-617">[\#pragma](pragma-namespace.md) must be followed by a valid keyword.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-618"><span id="WBEMMOF_E_INVALID_NAMESPACE_SYNTAX"></span><span id="wbemmof_e_invalid_namespace_syntax"></span>**WBEMMOF \_ \_ Sintaxis de \_ espacio de nombres no válida \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-618"><span id="WBEMMOF_E_INVALID_NAMESPACE_SYNTAX"></span><span id="wbemmof_e_invalid_namespace_syntax"></span>**WBEMMOF\_E\_INVALID\_NAMESPACE\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-619">2147762195 (0x80044013)</span><span class="sxs-lookup"><span data-stu-id="87ddf-619">2147762195 (0x80044013)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-620">La sintaxis de la ruta de acceso del espacio de nombres no es válida.</span><span class="sxs-lookup"><span data-stu-id="87ddf-620">Namespace path syntax is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-621"><span id="WBEMMOF_E_EXPECTED_CLASS_NAME"></span><span id="wbemmof_e_expected_class_name"></span>**WBEMMOF \_ E \_ esperaba \_ \_ el nombre de clase**</span><span class="sxs-lookup"><span data-stu-id="87ddf-621"><span id="WBEMMOF_E_EXPECTED_CLASS_NAME"></span><span id="wbemmof_e_expected_class_name"></span>**WBEMMOF\_E\_EXPECTED\_CLASS\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-622">2147762196 (0x80044014)</span><span class="sxs-lookup"><span data-stu-id="87ddf-622">2147762196 (0x80044014)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-623">Un carácter inesperado en el nombre de clase debe ser un identificador.</span><span class="sxs-lookup"><span data-stu-id="87ddf-623">Unexpected character in class name must be an identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-624"><span id="WBEMMOF_E_TYPE_MISMATCH"></span><span id="wbemmof_e_type_mismatch"></span>**error \_ de \_ coincidencia de tipo de WBEMMOF \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-624"><span id="WBEMMOF_E_TYPE_MISMATCH"></span><span id="wbemmof_e_type_mismatch"></span>**WBEMMOF\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-625">2147762197 (0x80044015)</span><span class="sxs-lookup"><span data-stu-id="87ddf-625">2147762197 (0x80044015)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-626">El valor especificado no se puede establecer en el tipo adecuado.</span><span class="sxs-lookup"><span data-stu-id="87ddf-626">The value specified cannot be made into the appropriate type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-627"><span id="WBEMMOF_E_EXPECTED_ALIAS_NAME"></span><span id="wbemmof_e_expected_alias_name"></span>**WBEMMOF \_ E \_ esperaba \_ \_ el nombre de alias**</span><span class="sxs-lookup"><span data-stu-id="87ddf-627"><span id="WBEMMOF_E_EXPECTED_ALIAS_NAME"></span><span id="wbemmof_e_expected_alias_name"></span>**WBEMMOF\_E\_EXPECTED\_ALIAS\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-628">2147762198 (0x80044016)</span><span class="sxs-lookup"><span data-stu-id="87ddf-628">2147762198 (0x80044016)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-629">El signo de dólar debe ir seguido de un nombre de alias como identificador.</span><span class="sxs-lookup"><span data-stu-id="87ddf-629">Dollar sign must be followed by an alias name as an identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-630"><span id="WBEMMOF_E_INVALID_CLASS_DECLARATION"></span><span id="wbemmof_e_invalid_class_declaration"></span>**WBEMMOF \_ \_ declaración de \_ clase no válida \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-630"><span id="WBEMMOF_E_INVALID_CLASS_DECLARATION"></span><span id="wbemmof_e_invalid_class_declaration"></span>**WBEMMOF\_E\_INVALID\_CLASS\_DECLARATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-631">2147762199 (0x80044017)</span><span class="sxs-lookup"><span data-stu-id="87ddf-631">2147762199 (0x80044017)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-632">La declaración de clase no es válida.</span><span class="sxs-lookup"><span data-stu-id="87ddf-632">Class declaration is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-633"><span id="WBEMMOF_E_INVALID_INSTANCE_DECLARATION"></span><span id="wbemmof_e_invalid_instance_declaration"></span>**WBEMMOF \_ \_ declaración de \_ instancia no válida \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-633"><span id="WBEMMOF_E_INVALID_INSTANCE_DECLARATION"></span><span id="wbemmof_e_invalid_instance_declaration"></span>**WBEMMOF\_E\_INVALID\_INSTANCE\_DECLARATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-634">2147762200 (0x80044018)</span><span class="sxs-lookup"><span data-stu-id="87ddf-634">2147762200 (0x80044018)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-635">La declaración de instancia no es válida.</span><span class="sxs-lookup"><span data-stu-id="87ddf-635">The instance declaration is not valid.</span></span> <span data-ttu-id="87ddf-636">Debe empezar por "instancia de"</span><span class="sxs-lookup"><span data-stu-id="87ddf-636">It must start with "instance of"</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-637"><span id="WBEMMOF_E_EXPECTED_DOLLAR"></span><span id="wbemmof_e_expected_dollar"></span>**\_ \_ dólar esperado de WBEMMOF E \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-637"><span id="WBEMMOF_E_EXPECTED_DOLLAR"></span><span id="wbemmof_e_expected_dollar"></span>**WBEMMOF\_E\_EXPECTED\_DOLLAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-638">2147762201 (0x80044019)</span><span class="sxs-lookup"><span data-stu-id="87ddf-638">2147762201 (0x80044019)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-639">Signo de dólar esperado.</span><span class="sxs-lookup"><span data-stu-id="87ddf-639">Expected dollar sign.</span></span> <span data-ttu-id="87ddf-640">Un alias con el formato "$name" debe seguir la palabra clave "as".</span><span class="sxs-lookup"><span data-stu-id="87ddf-640">An alias in the form "$name" must follow the "as" keyword.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-641"><span id="WBEMMOF_E_CIMTYPE_QUALIFIER"></span><span id="wbemmof_e_cimtype_qualifier"></span>**\_ \_ calificador WBEMMOF E CIMTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-641"><span id="WBEMMOF_E_CIMTYPE_QUALIFIER"></span><span id="wbemmof_e_cimtype_qualifier"></span>**WBEMMOF\_E\_CIMTYPE\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-642">2147762202 (0x8004401A)</span><span class="sxs-lookup"><span data-stu-id="87ddf-642">2147762202 (0x8004401A)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-643">El calificador "CIMTYPE" no se puede especificar directamente en un archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="87ddf-643">"CIMTYPE" qualifier cannot be specified directly in a MOF file.</span></span> <span data-ttu-id="87ddf-644">Use la notación de tipo estándar.</span><span class="sxs-lookup"><span data-stu-id="87ddf-644">Use standard type notation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-645"><span id="WBEMMOF_E_DUPLICATE_PROPERTY"></span><span id="wbemmof_e_duplicate_property"></span>**WBEMMOF \_ \_ propiedad duplicada \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-645"><span id="WBEMMOF_E_DUPLICATE_PROPERTY"></span><span id="wbemmof_e_duplicate_property"></span>**WBEMMOF\_E\_DUPLICATE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-646">2147762203 (0x8004401B)</span><span class="sxs-lookup"><span data-stu-id="87ddf-646">2147762203 (0x8004401B)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-647">Se encontró un nombre de propiedad duplicado en MOF.</span><span class="sxs-lookup"><span data-stu-id="87ddf-647">Duplicate property name was found in the MOF.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-648"><span id="WBEMMOF_E_INVALID_NAMESPACE_SPECIFICATION"></span><span id="wbemmof_e_invalid_namespace_specification"></span>**WBEMMOF \_ E \_ especificación de espacio de nombres no válida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-648"><span id="WBEMMOF_E_INVALID_NAMESPACE_SPECIFICATION"></span><span id="wbemmof_e_invalid_namespace_specification"></span>**WBEMMOF\_E\_INVALID\_NAMESPACE\_SPECIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-649">2147762204 (0x8004401C)</span><span class="sxs-lookup"><span data-stu-id="87ddf-649">2147762204 (0x8004401C)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-650">La sintaxis del espacio de nombres no es válida.</span><span class="sxs-lookup"><span data-stu-id="87ddf-650">Namespace syntax is not valid.</span></span> <span data-ttu-id="87ddf-651">No se permiten referencias a otros servidores.</span><span class="sxs-lookup"><span data-stu-id="87ddf-651">References to other servers are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-652"><span id="WBEMMOF_E_OUT_OF_RANGE"></span><span id="wbemmof_e_out_of_range"></span>**WBEMMOF \_ E \_ fuera \_ del \_ intervalo**</span><span class="sxs-lookup"><span data-stu-id="87ddf-652"><span id="WBEMMOF_E_OUT_OF_RANGE"></span><span id="wbemmof_e_out_of_range"></span>**WBEMMOF\_E\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-653">2147762205 (0x8004401D)</span><span class="sxs-lookup"><span data-stu-id="87ddf-653">2147762205 (0x8004401D)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-654">Valor fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="87ddf-654">Value out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-655"><span id="WBEMMOF_E_INVALID_FILE"></span><span id="wbemmof_e_invalid_file"></span>**WBEMMOF \_ \_ archivo no válido \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-655"><span id="WBEMMOF_E_INVALID_FILE"></span><span id="wbemmof_e_invalid_file"></span>**WBEMMOF\_E\_INVALID\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-656">2147762206 (0x8004401E)</span><span class="sxs-lookup"><span data-stu-id="87ddf-656">2147762206 (0x8004401E)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-657">El archivo no es un archivo MOF de texto o archivo MOF binario válido.</span><span class="sxs-lookup"><span data-stu-id="87ddf-657">The file is not a valid text MOF file or binary MOF file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-658"><span id="WBEMMOF_E_ALIASES_IN_EMBEDDED"></span><span id="wbemmof_e_aliases_in_embedded"></span>**\_alias WBEMMOF E \_ \_ en \_ Embedded**</span><span class="sxs-lookup"><span data-stu-id="87ddf-658"><span id="WBEMMOF_E_ALIASES_IN_EMBEDDED"></span><span id="wbemmof_e_aliases_in_embedded"></span>**WBEMMOF\_E\_ALIASES\_IN\_EMBEDDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-659">2147762207 (0x8004401F)</span><span class="sxs-lookup"><span data-stu-id="87ddf-659">2147762207 (0x8004401F)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-660">Los objetos incrustados no pueden ser alias.</span><span class="sxs-lookup"><span data-stu-id="87ddf-660">Embedded objects cannot be aliases.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-661"><span id="WBEMMOF_E_NULL_ARRAY_ELEM"></span><span id="wbemmof_e_null_array_elem"></span>**WBEMMOF \_ E \_ null \_ array \_ Elem**</span><span class="sxs-lookup"><span data-stu-id="87ddf-661"><span id="WBEMMOF_E_NULL_ARRAY_ELEM"></span><span id="wbemmof_e_null_array_elem"></span>**WBEMMOF\_E\_NULL\_ARRAY\_ELEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-662">2147762208 (0x80044020)</span><span class="sxs-lookup"><span data-stu-id="87ddf-662">2147762208 (0x80044020)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-663">No se admiten elementos NULL en una matriz.</span><span class="sxs-lookup"><span data-stu-id="87ddf-663">NULL elements in an array are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-664"><span id="WBEMMOF_E_DUPLICATE_QUALIFIER"></span><span id="wbemmof_e_duplicate_qualifier"></span>**\_ \_ calificador WBEMMOF E duplicado \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-664"><span id="WBEMMOF_E_DUPLICATE_QUALIFIER"></span><span id="wbemmof_e_duplicate_qualifier"></span>**WBEMMOF\_E\_DUPLICATE\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-665">2147762209 (0x80044021)</span><span class="sxs-lookup"><span data-stu-id="87ddf-665">2147762209 (0x80044021)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-666">El calificador se ha utilizado más de una vez en el objeto.</span><span class="sxs-lookup"><span data-stu-id="87ddf-666">Qualifier was used more than once on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-667"><span id="WBEMMOF_E_EXPECTED_FLAVOR_TYPE"></span><span id="wbemmof_e_expected_flavor_type"></span>**WBEMMOF \_ E \_ esperaba \_ el \_ tipo de sabor**</span><span class="sxs-lookup"><span data-stu-id="87ddf-667"><span id="WBEMMOF_E_EXPECTED_FLAVOR_TYPE"></span><span id="wbemmof_e_expected_flavor_type"></span>**WBEMMOF\_E\_EXPECTED\_FLAVOR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-668">2147762210 (0x80044022)</span><span class="sxs-lookup"><span data-stu-id="87ddf-668">2147762210 (0x80044022)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-669">Se esperaba un tipo de sabor como **ToInstance**, **ToSubClass**, **EnableOverride** o **DisableOverride**.</span><span class="sxs-lookup"><span data-stu-id="87ddf-669">Expected a flavor type such as **ToInstance**, **ToSubClass**, **EnableOverride**, or **DisableOverride**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-670"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES"></span><span id="wbemmof_e_incompatible_flavor_types"></span>**\_tipos de tipo WBEMMOF E \_ incompatibles \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-670"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES"></span><span id="wbemmof_e_incompatible_flavor_types"></span>**WBEMMOF\_E\_INCOMPATIBLE\_FLAVOR\_TYPES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-671">2147762211 (0x80044023)</span><span class="sxs-lookup"><span data-stu-id="87ddf-671">2147762211 (0x80044023)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-672">La combinación de **EnableOverride** y **DisableOverride** en el mismo calificador no es legal.</span><span class="sxs-lookup"><span data-stu-id="87ddf-672">Combining **EnableOverride** and **DisableOverride** on same qualifier is not legal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-673"><span id="WBEMMOF_E_MULTIPLE_ALIASES"></span><span id="wbemmof_e_multiple_aliases"></span>**WBEMMOF \_ de \_ varios \_ alias**</span><span class="sxs-lookup"><span data-stu-id="87ddf-673"><span id="WBEMMOF_E_MULTIPLE_ALIASES"></span><span id="wbemmof_e_multiple_aliases"></span>**WBEMMOF\_E\_MULTIPLE\_ALIASES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-674">2147762212 (0x80044024)</span><span class="sxs-lookup"><span data-stu-id="87ddf-674">2147762212 (0x80044024)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-675">No se puede usar un alias dos veces.</span><span class="sxs-lookup"><span data-stu-id="87ddf-675">An alias cannot be used twice.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-676"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES2"></span><span id="wbemmof_e_incompatible_flavor_types2"></span>**WBEMMOF \_ E \_ incompatible \_ \_ TYPES2**</span><span class="sxs-lookup"><span data-stu-id="87ddf-676"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES2"></span><span id="wbemmof_e_incompatible_flavor_types2"></span>**WBEMMOF\_E\_INCOMPATIBLE\_FLAVOR\_TYPES2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-677">2147762213 (0x80044025)</span><span class="sxs-lookup"><span data-stu-id="87ddf-677">2147762213 (0x80044025)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-678">La combinación de los **permisos restringidos** y **ToInstance** o **ToSubClass** no es legal.</span><span class="sxs-lookup"><span data-stu-id="87ddf-678">Combining **Restricted**, and **ToInstance** or **ToSubClass** is not legal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-679"><span id="WBEMMOF_E_NO_ARRAYS_RETURNED"></span><span id="wbemmof_e_no_arrays_returned"></span>**WBEMMOF \_ E \_ no se \_ \_ devolvieron matrices**</span><span class="sxs-lookup"><span data-stu-id="87ddf-679"><span id="WBEMMOF_E_NO_ARRAYS_RETURNED"></span><span id="wbemmof_e_no_arrays_returned"></span>**WBEMMOF\_E\_NO\_ARRAYS\_RETURNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-680">2147762214 (0x80044026)</span><span class="sxs-lookup"><span data-stu-id="87ddf-680">2147762214 (0x80044026)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-681">Los métodos no pueden devolver valores de matriz.</span><span class="sxs-lookup"><span data-stu-id="87ddf-681">Methods cannot return array values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-682"><span id="WBEMMOF_E_MUST_BE_IN_OR_OUT"></span><span id="wbemmof_e_must_be_in_or_out"></span>**WBEMMOF \_ E \_ debe \_ estar \_ dentro \_ o \_ fuera**</span><span class="sxs-lookup"><span data-stu-id="87ddf-682"><span id="WBEMMOF_E_MUST_BE_IN_OR_OUT"></span><span id="wbemmof_e_must_be_in_or_out"></span>**WBEMMOF\_E\_MUST\_BE\_IN\_OR\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-683">2147762215 (0x80044027)</span><span class="sxs-lookup"><span data-stu-id="87ddf-683">2147762215 (0x80044027)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-684">Los argumentos deben tener un calificador **in** o **out** .</span><span class="sxs-lookup"><span data-stu-id="87ddf-684">Arguments must have an **In** or **Out** qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-685"><span id="WBEMMOF_E_INVALID_FLAGS_SYNTAX"></span><span id="wbemmof_e_invalid_flags_syntax"></span>**WBEMMOF \_ \_ Sintaxis de \_ marcas no válidas \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-685"><span id="WBEMMOF_E_INVALID_FLAGS_SYNTAX"></span><span id="wbemmof_e_invalid_flags_syntax"></span>**WBEMMOF\_E\_INVALID\_FLAGS\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-686">2147762216 (0x80044028)</span><span class="sxs-lookup"><span data-stu-id="87ddf-686">2147762216 (0x80044028)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-687">La sintaxis de flags no es válida.</span><span class="sxs-lookup"><span data-stu-id="87ddf-687">Flags syntax is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-688"><span id="WBEMMOF_E_EXPECTED_BRACE_OR_BAD_TYPE"></span><span id="wbemmof_e_expected_brace_or_bad_type"></span>**WBEMMOF \_ E \_ la \_ llave esperada o el \_ \_ \_ tipo incorrecto**</span><span class="sxs-lookup"><span data-stu-id="87ddf-688"><span id="WBEMMOF_E_EXPECTED_BRACE_OR_BAD_TYPE"></span><span id="wbemmof_e_expected_brace_or_bad_type"></span>**WBEMMOF\_E\_EXPECTED\_BRACE\_OR\_BAD\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-689">2147762217 (0x80044029)</span><span class="sxs-lookup"><span data-stu-id="87ddf-689">2147762217 (0x80044029)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-690">Faltan la llave final y el punto y coma para una clase.</span><span class="sxs-lookup"><span data-stu-id="87ddf-690">The final brace and semi-colon for a class are missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-691"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_QUAL_VALUE"></span><span id="wbemmof_e_unsupported_cimv22_qual_value"></span>**WBEMMOF \_ E \_ \_ CIMV22 de \_ \_ valor no admitido**</span><span class="sxs-lookup"><span data-stu-id="87ddf-691"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_QUAL_VALUE"></span><span id="wbemmof_e_unsupported_cimv22_qual_value"></span>**WBEMMOF\_E\_UNSUPPORTED\_CIMV22\_QUAL\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-692">2147762218 (0x8004402A)</span><span class="sxs-lookup"><span data-stu-id="87ddf-692">2147762218 (0x8004402A)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-693">No se admite una característica de la versión 2,2 de CIM para un valor de calificador.</span><span class="sxs-lookup"><span data-stu-id="87ddf-693">A CIM version 2.2 feature is not supported for a qualifier value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-694"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_DATA_TYPE"></span><span id="wbemmof_e_unsupported_cimv22_data_type"></span>**WBEMMOF \_ E \_ \_ CIMV22, tipo de \_ datos no admitido \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-694"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_DATA_TYPE"></span><span id="wbemmof_e_unsupported_cimv22_data_type"></span>**WBEMMOF\_E\_UNSUPPORTED\_CIMV22\_DATA\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-695">2147762219 (0x8004402B)</span><span class="sxs-lookup"><span data-stu-id="87ddf-695">2147762219 (0x8004402B)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-696">No se admite el tipo de datos de la versión 2,2 de CIM.</span><span class="sxs-lookup"><span data-stu-id="87ddf-696">The CIM version 2.2 data type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-697"><span id="WBEMMOF_E_INVALID_DELETEINSTANCE_SYNTAX"></span><span id="wbemmof_e_invalid_deleteinstance_syntax"></span>**WBEMMOF \_ , \_ \_ Sintaxis de DELETEINSTANCE no válida \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-697"><span id="WBEMMOF_E_INVALID_DELETEINSTANCE_SYNTAX"></span><span id="wbemmof_e_invalid_deleteinstance_syntax"></span>**WBEMMOF\_E\_INVALID\_DELETEINSTANCE\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-698">2147762220 (0x8004402C)</span><span class="sxs-lookup"><span data-stu-id="87ddf-698">2147762220 (0x8004402C)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-699">La sintaxis de eliminar instancia no es válida.</span><span class="sxs-lookup"><span data-stu-id="87ddf-699">The delete instance syntax is not valid.</span></span> <span data-ttu-id="87ddf-700">Debe ser `#pragma DeleteInstance("instancepath", FAIL|NOFAIL)`</span><span class="sxs-lookup"><span data-stu-id="87ddf-700">It should be `#pragma DeleteInstance("instancepath", FAIL|NOFAIL)`</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-701"><span id="WBEMMOF_E_INVALID_QUALIFIER_SYNTAX"></span><span id="wbemmof_e_invalid_qualifier_syntax"></span>**WBEMMOF \_ \_ Sintaxis de \_ calificador no válida \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-701"><span id="WBEMMOF_E_INVALID_QUALIFIER_SYNTAX"></span><span id="wbemmof_e_invalid_qualifier_syntax"></span>**WBEMMOF\_E\_INVALID\_QUALIFIER\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-702">2147762221 (0x8004402D)</span><span class="sxs-lookup"><span data-stu-id="87ddf-702">2147762221 (0x8004402D)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-703">La sintaxis del calificador no es válida.</span><span class="sxs-lookup"><span data-stu-id="87ddf-703">The qualifier syntax is not valid.</span></span> <span data-ttu-id="87ddf-704">Debería ser `qualifiername:type=value,scope(class|instance), flavorname`.</span><span class="sxs-lookup"><span data-stu-id="87ddf-704">It should be `qualifiername:type=value,scope(class|instance), flavorname`.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-705"><span id="WBEMMOF_E_QUALIFIER_USED_OUTSIDE_SCOPE"></span><span id="wbemmof_e_qualifier_used_outside_scope"></span>**WBEMMOF \_ E \_ calificador \_ usado \_ fuera del \_ ámbito**</span><span class="sxs-lookup"><span data-stu-id="87ddf-705"><span id="WBEMMOF_E_QUALIFIER_USED_OUTSIDE_SCOPE"></span><span id="wbemmof_e_qualifier_used_outside_scope"></span>**WBEMMOF\_E\_QUALIFIER\_USED\_OUTSIDE\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-706">2147762222 (0x8004402E)</span><span class="sxs-lookup"><span data-stu-id="87ddf-706">2147762222 (0x8004402E)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-707">El calificador se usa fuera de su ámbito.</span><span class="sxs-lookup"><span data-stu-id="87ddf-707">The qualifier is used outside of its scope.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-708"><span id="WBEMMOF_E_ERROR_CREATING_TEMP_FILE"></span><span id="wbemmof_e_error_creating_temp_file"></span>**WBEMMOF \_ E \_ error al \_ crear el \_ \_ archivo temporal**</span><span class="sxs-lookup"><span data-stu-id="87ddf-708"><span id="WBEMMOF_E_ERROR_CREATING_TEMP_FILE"></span><span id="wbemmof_e_error_creating_temp_file"></span>**WBEMMOF\_E\_ERROR\_CREATING\_TEMP\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-709">2147762223 (0x8004402F)</span><span class="sxs-lookup"><span data-stu-id="87ddf-709">2147762223 (0x8004402F)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-710">Error al crear el archivo temporal.</span><span class="sxs-lookup"><span data-stu-id="87ddf-710">Error creating temporary file.</span></span> <span data-ttu-id="87ddf-711">El archivo temporal es una fase intermedia de la compilación MOF.</span><span class="sxs-lookup"><span data-stu-id="87ddf-711">The temporary file is an intermediate stage in the MOF compilation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-712"><span id="WBEMMOF_E_ERROR_INVALID_INCLUDE_FILE"></span><span id="wbemmof_e_error_invalid_include_file"></span>**ERROR de WBEMMOF \_ E \_ \_ archivo de inclusión no válido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87ddf-712"><span id="WBEMMOF_E_ERROR_INVALID_INCLUDE_FILE"></span><span id="wbemmof_e_error_invalid_include_file"></span>**WBEMMOF\_E\_ERROR\_INVALID\_INCLUDE\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-713">2147762224 (0x80044030)</span><span class="sxs-lookup"><span data-stu-id="87ddf-713">2147762224 (0x80044030)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-714">Un archivo incluido en el MOF por el comando de preprocesador [ \# include](-include.md) no es válido.</span><span class="sxs-lookup"><span data-stu-id="87ddf-714">A file included in the MOF by the preprocessor command [\#include](-include.md) is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="87ddf-715"><span id="WBEMMOF_E_INVALID_DELETECLASS_SYNTAX"></span><span id="wbemmof_e_invalid_deleteclass_syntax"></span>**WBEMMOF \_ \_ \_ Sintaxis DELETECLASS no \_ válida**</span><span class="sxs-lookup"><span data-stu-id="87ddf-715"><span id="WBEMMOF_E_INVALID_DELETECLASS_SYNTAX"></span><span id="wbemmof_e_invalid_deleteclass_syntax"></span>**WBEMMOF\_E\_INVALID\_DELETECLASS\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87ddf-716">2147762225 (0x80044031)</span><span class="sxs-lookup"><span data-stu-id="87ddf-716">2147762225 (0x80044031)</span></span>
</dt> <dt>



<span data-ttu-id="87ddf-717">La sintaxis de los comandos de preprocesador [ \# pragma deleteinstance](pragma-deleteinstance.md) o [ \# pragma deleteclass](pragma-deleteclass.md) no es válida.</span><span class="sxs-lookup"><span data-stu-id="87ddf-717">The syntax for the preprocessor commands [\#pragma deleteinstance](pragma-deleteinstance.md) or [\#pragma deleteclass](pragma-deleteclass.md) is not valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87ddf-718">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87ddf-718">Requirements</span></span>



| <span data-ttu-id="87ddf-719">Requisito</span><span class="sxs-lookup"><span data-stu-id="87ddf-719">Requirement</span></span> | <span data-ttu-id="87ddf-720">Value</span><span class="sxs-lookup"><span data-stu-id="87ddf-720">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87ddf-721">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87ddf-721">Minimum supported client</span></span><br/> | <span data-ttu-id="87ddf-722">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87ddf-722">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="87ddf-723">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87ddf-723">Minimum supported server</span></span><br/> | <span data-ttu-id="87ddf-724">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87ddf-724">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="87ddf-725">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87ddf-725">Header</span></span><br/>                   | <dl> <span data-ttu-id="87ddf-726"><dt>WbemCli. h</dt></span><span class="sxs-lookup"><span data-stu-id="87ddf-726"><dt>WbemCli.h</dt></span></span> </dl>   |
| <span data-ttu-id="87ddf-727">IDL</span><span class="sxs-lookup"><span data-stu-id="87ddf-727">IDL</span></span><br/>                      | <dl> <span data-ttu-id="87ddf-728"><dt>WbemCli. idl</dt></span><span class="sxs-lookup"><span data-stu-id="87ddf-728"><dt>WbemCli.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87ddf-729">Vea también</span><span class="sxs-lookup"><span data-stu-id="87ddf-729">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87ddf-730">Códigos de retorno de WMI</span><span class="sxs-lookup"><span data-stu-id="87ddf-730">WMI Return Codes</span></span>](wmi-return-codes.md)
</dt> </dl>

 

