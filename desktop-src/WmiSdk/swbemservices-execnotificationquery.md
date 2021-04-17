---
description: Ejecuta una consulta para recibir eventos. La llamada se devuelve inmediatamente.
ms.assetid: 3e1bb428-5395-4e90-9713-6d96242fef4e
ms.tgt_platform: multiple
title: SWbemServices.Exemétodo cNotificationQuery (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 44279d16e180d776dc4433c6d5246eab2419fca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716196"
---
# <a name="swbemservicesexecnotificationquery-method"></a><span data-ttu-id="5c749-104">SWbemServices.Exemétodo cNotificationQuery</span><span class="sxs-lookup"><span data-stu-id="5c749-104">SWbemServices.ExecNotificationQuery method</span></span>

<span data-ttu-id="5c749-105">El método **ExecNotificationQuery** del objeto [**SWbemServices**](swbemservices.md) ejecuta una consulta para recibir eventos.</span><span class="sxs-lookup"><span data-stu-id="5c749-105">The **ExecNotificationQuery** method of the [**SWbemServices**](swbemservices.md) object executes a query to receive events.</span></span> <span data-ttu-id="5c749-106">La llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="5c749-106">The call returns immediately.</span></span> <span data-ttu-id="5c749-107">El usuario puede sondear el enumerador devuelto para los eventos a medida que llegan.</span><span class="sxs-lookup"><span data-stu-id="5c749-107">The user can poll the returned enumerator for events as they arrive.</span></span>

<span data-ttu-id="5c749-108">Se llama al método en el modo semisincrónico.</span><span class="sxs-lookup"><span data-stu-id="5c749-108">The method is called in the semisynchronous mode.</span></span> <span data-ttu-id="5c749-109">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="5c749-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="5c749-110">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5c749-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5c749-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c749-111">Syntax</span></span>


```VB
objwbemEventsource = .ExecNotificationQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="5c749-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c749-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c749-113">*strQuery*</span><span class="sxs-lookup"><span data-stu-id="5c749-113">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="5c749-114">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5c749-114">Required.</span></span> <span data-ttu-id="5c749-115">Cadena que contiene el texto de la consulta relacionada con eventos.</span><span class="sxs-lookup"><span data-stu-id="5c749-115">String that contains the text of the event-related query.</span></span> <span data-ttu-id="5c749-116">Este parámetro no puede estar en blanco.</span><span class="sxs-lookup"><span data-stu-id="5c749-116">This parameter cannot be blank.</span></span> <span data-ttu-id="5c749-117">Para obtener más información sobre la creación de cadenas de consulta de WMI, vea [consultas con WQL](querying-with-wql.md) y la referencia de [WQL](wql-sql-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="5c749-117">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="5c749-118">*strQueryLanguage* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="5c749-118">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5c749-119">Cadena que contiene el lenguaje de consulta que se va a utilizar.</span><span class="sxs-lookup"><span data-stu-id="5c749-119">String that contains the query language to be used.</span></span> <span data-ttu-id="5c749-120">Si se especifica, este valor debe ser "WQL".</span><span class="sxs-lookup"><span data-stu-id="5c749-120">If specified, this value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="5c749-121">*iFlags* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="5c749-121">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5c749-122">Es un entero que determina el comportamiento de la consulta.</span><span class="sxs-lookup"><span data-stu-id="5c749-122">This is an integer that determines the behavior of the query.</span></span> <span data-ttu-id="5c749-123">El valor predeterminado es **wbemFlagReturnImmediately**  +  **wbemFlagForwardOnly**.</span><span class="sxs-lookup"><span data-stu-id="5c749-123">The default value is **wbemFlagReturnImmediately** + **wbemFlagForwardOnly**.</span></span> <span data-ttu-id="5c749-124">Si especifica este parámetro, este parámetro debe establecerse en **wbemFlagReturnImmediately** y **wbemFlagForwardOnly** o se producirá un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="5c749-124">If you specify this parameter, this parameter must be set to both **wbemFlagReturnImmediately** and **wbemFlagForwardOnly** or the call fails.</span></span> <span data-ttu-id="5c749-125">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5c749-125">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="5c749-126"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="5c749-126"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="5c749-127">Hace que se devuelva un enumerador de solo avance.</span><span class="sxs-lookup"><span data-stu-id="5c749-127">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="5c749-128">Los enumeradores de solo avance suelen ser mucho más rápidos y usan menos memoria que los enumeradores convencionales, pero no permiten llamadas a [**SWbemObject. \_ Clone**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="5c749-128">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="5c749-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="5c749-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="5c749-130">Hace que la llamada se devuelva inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="5c749-130">Causes the call to return immediately.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5c749-131">*objWbemNamedValueSet* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="5c749-131">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5c749-132">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="5c749-132">Typically, this is undefined.</span></span> <span data-ttu-id="5c749-133">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5c749-133">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="5c749-134">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="5c749-134">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c749-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c749-135">Return value</span></span>

<span data-ttu-id="5c749-136">Si no se produce ningún error, este método devuelve un objeto [**SWbemEventSource**](swbemeventsource.md) .</span><span class="sxs-lookup"><span data-stu-id="5c749-136">If no error occurs, this method returns an [**SWbemEventSource**](swbemeventsource.md) object.</span></span> <span data-ttu-id="5c749-137">Puede llamar al método [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) para recuperar los eventos a medida que llegan.</span><span class="sxs-lookup"><span data-stu-id="5c749-137">You can call the [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) method to retrieve events as they arrive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5c749-138">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="5c749-138">Error codes</span></span>

<span data-ttu-id="5c749-139">Después de completar el método **ExecNotificationQuery** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="5c749-139">After the completion of the **ExecNotificationQuery** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="5c749-140">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="5c749-140">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="5c749-141">El usuario actual no está autorizado para ver el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="5c749-141">Current user is not authorized to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="5c749-142">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="5c749-142">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="5c749-143">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="5c749-143">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="5c749-144">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="5c749-144">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="5c749-145">Se especificó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="5c749-145">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="5c749-146">**wbemErrInvalidQuery** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="5c749-146">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="5c749-147">La sintaxis de la consulta no es válida.</span><span class="sxs-lookup"><span data-stu-id="5c749-147">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5c749-148">**wbemErrInvalidQueryType** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="5c749-148">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="5c749-149">No se admite el lenguaje de consulta solicitado.</span><span class="sxs-lookup"><span data-stu-id="5c749-149">The requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5c749-150">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="5c749-150">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="5c749-151">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="5c749-151">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c749-152">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c749-152">Remarks</span></span>

<span data-ttu-id="5c749-153">A diferencia del método [**cQueryAsync deSWbemServices.Exe**](swbemservices-execqueryasync.md) , **ExecNotificationQuery** devuelve objetos de tipo de evento generados por eventos futuros en lugar de objetos existentes.</span><span class="sxs-lookup"><span data-stu-id="5c749-153">Unlike the [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) method, **ExecNotificationQuery** returns event type objects that are generated by future events rather than existing objects.</span></span> <span data-ttu-id="5c749-154">Los objetos de evento que las solicitudes **ExecNotificationQuery** pueden ser intrínsecos (por ejemplo, [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) o extrínsecos (como eventos de proveedor de registro como [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) o eventos SNMP).</span><span class="sxs-lookup"><span data-stu-id="5c749-154">The event objects that **ExecNotificationQuery** requests can either be intrinsic (such as [**\_\_InstanceCreationEvent**](--instancecreationevent.md)) or extrinsic (such as registry provider events like [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) or SNMP events).</span></span> <span data-ttu-id="5c749-155">Para obtener más información, vea [determinar el tipo de evento que se va a recibir](determining-the-type-of-event-to-receive.md) y [recibir notificaciones de eventos](receiving-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="5c749-155">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md) and [Receiving Event Notifications](receiving-event-notifications.md).</span></span>

<span data-ttu-id="5c749-156">Hay límites en el número de palabras clave **and** y **or** que se pueden usar en las consultas WQL.</span><span class="sxs-lookup"><span data-stu-id="5c749-156">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="5c749-157">Un gran número de palabras clave WQL usadas en una consulta compleja puede hacer que WMI devuelva el código de error de **\_ \_ \_ infracción de la cuota de WBEM E** como un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5c749-157">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="5c749-158">El límite de palabras clave de WQL depende de la complejidad de la consulta.</span><span class="sxs-lookup"><span data-stu-id="5c749-158">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="examples"></a><span data-ttu-id="5c749-159">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5c749-159">Examples</span></span>

<span data-ttu-id="5c749-160">En el siguiente ejemplo de código de VBScript se supervisan los cambios en los volúmenes de un equipo local.</span><span class="sxs-lookup"><span data-stu-id="5c749-160">The following VBScript code example monitors changes to volumes on a local computer.</span></span> <span data-ttu-id="5c749-161">Tenga en cuenta que [**Win32 \_ VolumeChangeEvent**](/windows/desktop/CIMWin32Prov/win32-volumechangeevent) es un evento extrínseco que está definido por un proveedor no es un evento intrínseco definido por WMI.</span><span class="sxs-lookup"><span data-stu-id="5c749-161">Note that [**Win32\_VolumeChangeEvent**](/windows/desktop/CIMWin32Prov/win32-volumechangeevent) is an extrinsic event that is defined by a provider not an intrinsic WMI-defined event.</span></span> <span data-ttu-id="5c749-162">Para obtener más información, vea [determinar el tipo de evento que se va a recibir](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="5c749-162">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>


```VB
Set colMonitoredEvents = _
   GetObject("Winmgmts:").ExecNotificationQuery_
      ("Select * from Win32_VolumeChangeEvent")

Do While i = 0
   Set strLatestEvent = colMonitoredEvents.NextEvent
   Wscript.Echo strLatestEvent.DriveName & "Time Created = " _
      & strLatestEvent.Time_Created

    Select Case strLatestEvent.EventType 
       Case 1        
            WScript.Echo "EventType = Configuration Changed"
       Case 2
            WScript.Echo "EventType = Device Arrival"
       Case 3
            WScript.Echo "EventType = Device Removal"
       Case 4
            WScript.Echo "EventType = Docking"

       Case Else
            WScript.Echo "Unrecognized EventType"
       End Select
Loop
```



<span data-ttu-id="5c749-163">El siguiente ejemplo de código de VBScript supervisa la eliminación del proceso.</span><span class="sxs-lookup"><span data-stu-id="5c749-163">The following VBScript code example monitors process deletion.</span></span> <span data-ttu-id="5c749-164">Si elimina un proceso en el administrador de tareas o cierra una aplicación, el script muestra un mensaje.</span><span class="sxs-lookup"><span data-stu-id="5c749-164">If you delete a process in Task Manager or close an application, then the script displays a message.</span></span> <span data-ttu-id="5c749-165">Tenga en cuenta que este script consulta un evento intrínseco definido por WMI- [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md).</span><span class="sxs-lookup"><span data-stu-id="5c749-165">Note that this script queries an intrinsic event that is defined by WMI - [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md).</span></span>


```VB
Set objWMIService = GetObject( _
    "Winmgmts:{impersonationLevel=impersonate}" )
Set colMonitoredProcesses = _
    objWMIService.ExecNotificationQuery( _
    "SELECT * FROM __InstanceDeletionEvent WITHIN 10 WHERE " _
    & "TargetInstance ISA 'Win32_Process'")
i = 0
Do While i < 11
    Set strLatestProcess = colMonitoredProcesses.NextEvent
    WScript.Echo strLatestProcess.TargetInstance.Name
    WScript.Sleep 10000
    i= i + 1
Loop
```



## <a name="requirements"></a><span data-ttu-id="5c749-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c749-166">Requirements</span></span>



| <span data-ttu-id="5c749-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c749-167">Requirement</span></span> | <span data-ttu-id="5c749-168">Value</span><span class="sxs-lookup"><span data-stu-id="5c749-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c749-169">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c749-169">Minimum supported client</span></span><br/> | <span data-ttu-id="5c749-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c749-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5c749-171">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c749-171">Minimum supported server</span></span><br/> | <span data-ttu-id="5c749-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c749-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5c749-173">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c749-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c749-174"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c749-174"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c749-175">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5c749-175">Type library</span></span><br/>             | <dl> <span data-ttu-id="5c749-176"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5c749-176"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5c749-177">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5c749-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c749-178"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c749-178"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5c749-179">CLSID</span><span class="sxs-lookup"><span data-stu-id="5c749-179">CLSID</span></span><br/>                    | <span data-ttu-id="5c749-180">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="5c749-180">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="5c749-181">IID</span><span class="sxs-lookup"><span data-stu-id="5c749-181">IID</span></span><br/>                      | <span data-ttu-id="5c749-182">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="5c749-182">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="5c749-183">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c749-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c749-184">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="5c749-184">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="5c749-185">**SWbemEventSource.NextEvent**</span><span class="sxs-lookup"><span data-stu-id="5c749-185">**SWbemEventSource.NextEvent**</span></span>](swbemeventsource-nextevent.md)
</dt> <dt>

[<span data-ttu-id="5c749-186">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="5c749-186">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
</dt> <dt>

[<span data-ttu-id="5c749-187">Recibir un evento de WMI</span><span class="sxs-lookup"><span data-stu-id="5c749-187">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)
</dt> <dt>

[<span data-ttu-id="5c749-188">Realizar consultas con WQL</span><span class="sxs-lookup"><span data-stu-id="5c749-188">Querying with WQL</span></span>](querying-with-wql.md)
</dt> <dt>

[<span data-ttu-id="5c749-189">WQL (SQL para WMI)</span><span class="sxs-lookup"><span data-stu-id="5c749-189">WQL (SQL for WMI)</span></span>](wql-sql-for-wmi.md)
</dt> <dt>

[<span data-ttu-id="5c749-190">Determinar el tipo de evento que se va a recibir</span><span class="sxs-lookup"><span data-stu-id="5c749-190">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

