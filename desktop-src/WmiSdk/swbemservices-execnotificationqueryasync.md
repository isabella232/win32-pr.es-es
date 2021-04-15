---
description: Ejecuta una consulta para recibir eventos.
ms.assetid: 0b0e8313-4ffd-4d4a-8965-d2c6743e7573
ms.tgt_platform: multiple
title: SWbemServices.Exemétodo cNotificationQueryAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8e2ecddf290d83583b3108620b8b4bb23be7c957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715718"
---
# <a name="swbemservicesexecnotificationqueryasync-method"></a><span data-ttu-id="db5d2-103">SWbemServices.Exemétodo cNotificationQueryAsync</span><span class="sxs-lookup"><span data-stu-id="db5d2-103">SWbemServices.ExecNotificationQueryAsync method</span></span>

<span data-ttu-id="db5d2-104">El método **ExecNotificationQueryAsync** del objeto [**SWbemServices**](swbemservices.md) ejecuta una consulta para recibir eventos.</span><span class="sxs-lookup"><span data-stu-id="db5d2-104">The **ExecNotificationQueryAsync** method of the [**SWbemServices**](swbemservices.md) object executes a query to receive events.</span></span> <span data-ttu-id="db5d2-105">Esta llamada se devuelve inmediatamente, y los resultados y el estado se devuelven al autor de la llamada a través de los eventos entregados al receptor que se especifica en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="db5d2-105">This call returns immediately and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span>

<span data-ttu-id="db5d2-106">Los eventos que se especifican en la consulta pueden ser eventos intrínsecos instrumental de administración de Windows (WMI), como [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md), o eventos extrínsecos, como [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent) o [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span><span class="sxs-lookup"><span data-stu-id="db5d2-106">The events that are specified in the query can be intrinsic Windows Management Instrumentation (WMI) events, such as [**\_\_InstanceCreationEvent**](--instancecreationevent.md), or extrinsic events, such as [**Win32\_IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent) or [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span></span> <span data-ttu-id="db5d2-107">Para obtener más información, vea [determinar el tipo de evento que se va a recibir](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="db5d2-107">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="db5d2-108">Se llama al método en el modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="db5d2-108">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="db5d2-109">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="db5d2-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="db5d2-110">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="db5d2-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="db5d2-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db5d2-111">Syntax</span></span>


```VB
SWbemServices.ExecNotificationQueryAsync( _
  ByVal objWbemSink, _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="db5d2-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db5d2-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db5d2-113">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="db5d2-113">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="db5d2-114">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="db5d2-114">Required.</span></span> <span data-ttu-id="db5d2-115">Receptor de objeto que recibe la notificación de eventos de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="db5d2-115">Object sink that receives the notification of events asynchronously.</span></span> <span data-ttu-id="db5d2-116">Cree un objeto [**SWbemSink**](swbemsink.md) para recibir los objetos.</span><span class="sxs-lookup"><span data-stu-id="db5d2-116">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="db5d2-117">*strQuery*</span><span class="sxs-lookup"><span data-stu-id="db5d2-117">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="db5d2-118">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="db5d2-118">Required.</span></span> <span data-ttu-id="db5d2-119">Cadena que contiene el texto de la consulta relacionada con eventos.</span><span class="sxs-lookup"><span data-stu-id="db5d2-119">String that contains the text of the event-related query.</span></span> <span data-ttu-id="db5d2-120">Este parámetro no puede estar en blanco.</span><span class="sxs-lookup"><span data-stu-id="db5d2-120">This parameter cannot be blank.</span></span> <span data-ttu-id="db5d2-121">Para obtener más información sobre la creación de cadenas de consulta de WMI, vea [consultas con WQL](querying-with-wql.md) y la referencia de [WQL](wql-sql-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="db5d2-121">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="db5d2-122">*strQueryLanguage* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="db5d2-122">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="db5d2-123">Cadena que contiene el lenguaje de consulta que se va a utilizar.</span><span class="sxs-lookup"><span data-stu-id="db5d2-123">String that contains the query language to be used.</span></span> <span data-ttu-id="db5d2-124">Si se especifica, este valor debe ser "WQL".</span><span class="sxs-lookup"><span data-stu-id="db5d2-124">If specified, this value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="db5d2-125">*iFlags* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="db5d2-125">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="db5d2-126">Entero que determina el comportamiento de la consulta.</span><span class="sxs-lookup"><span data-stu-id="db5d2-126">Integer that determines the behavior of the query.</span></span> <span data-ttu-id="db5d2-127">Este parámetro se puede establecer en los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="db5d2-127">This parameter can be set to the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="db5d2-128"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="db5d2-128"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="db5d2-129">Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="db5d2-129">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="db5d2-130"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="db5d2-130"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="db5d2-131">Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="db5d2-131">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="db5d2-132">*objwbemNamedValueSet* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="db5d2-132">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="db5d2-133">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="db5d2-133">Typically, this is undefined.</span></span> <span data-ttu-id="db5d2-134">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que presta servicio a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="db5d2-134">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="db5d2-135">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="db5d2-135">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="db5d2-136">*objWbemAsyncContext* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="db5d2-136">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="db5d2-137">Se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que devuelve al receptor del objeto para identificar el origen de la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="db5d2-137">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="db5d2-138">Use este parámetro para realizar varias llamadas asincrónicas mediante el mismo receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="db5d2-138">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="db5d2-139">Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando.</span><span class="sxs-lookup"><span data-stu-id="db5d2-139">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="db5d2-140">El objeto **SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="db5d2-140">The **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="db5d2-141">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="db5d2-141">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db5d2-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db5d2-142">Return value</span></span>

<span data-ttu-id="db5d2-143">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="db5d2-143">This method does not return a value.</span></span> <span data-ttu-id="db5d2-144">Si se realiza correctamente, el receptor recibe un evento [**OnObjectReady**](swbemsink-onobjectready.md) por cada instancia.</span><span class="sxs-lookup"><span data-stu-id="db5d2-144">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="db5d2-145">Después de la última instancia, el receptor del objeto recibe un evento [**alcompleto**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="db5d2-145">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="db5d2-146">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="db5d2-146">Error codes</span></span>

<span data-ttu-id="db5d2-147">Después de completar el método **ExecNotificationQueryAsync** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error identificados en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="db5d2-147">After the completion of the **ExecNotificationQueryAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes identified in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="db5d2-148">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="db5d2-148">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="db5d2-149">El usuario actual no está autorizado para ver el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="db5d2-149">Current user is not authorized to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="db5d2-150">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="db5d2-150">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="db5d2-151">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="db5d2-151">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="db5d2-152">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="db5d2-152">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="db5d2-153">Se ha especificado un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="db5d2-153">Invalid parameter is specified.</span></span>

</dd> <dt>

<span data-ttu-id="db5d2-154">**wbemErrInvalidQuery** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="db5d2-154">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="db5d2-155">La sintaxis de la consulta no es válida.</span><span class="sxs-lookup"><span data-stu-id="db5d2-155">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="db5d2-156">**wbemErrInvalidQueryType** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="db5d2-156">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="db5d2-157">No se admite el lenguaje de consulta solicitado.</span><span class="sxs-lookup"><span data-stu-id="db5d2-157">Requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="db5d2-158">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="db5d2-158">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="db5d2-159">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="db5d2-159">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db5d2-160">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db5d2-160">Remarks</span></span>

<span data-ttu-id="db5d2-161">El método **ExecNotificationQueryAsync** devuelve objetos de tipo de evento que generan eventos futuros.</span><span class="sxs-lookup"><span data-stu-id="db5d2-161">The **ExecNotificationQueryAsync** method returns event type objects that future events generate.</span></span> <span data-ttu-id="db5d2-162">Los objetos de evento que las solicitudes **ExecNotificationQueryAsync** pueden ser intrínsecos (por ejemplo, [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) o extrínsecos (por ejemplo, eventos [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) o SNMP).</span><span class="sxs-lookup"><span data-stu-id="db5d2-162">The event objects that **ExecNotificationQueryAsync** requests can be intrinsic (for example, [**\_\_InstanceCreationEvent**](--instancecreationevent.md)), or extrinsic (for example, [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) or SNMP events).</span></span> <span data-ttu-id="db5d2-163">Para obtener más información, vea [determinar el tipo de evento que se va a recibir](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="db5d2-163">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="db5d2-164">La llamada a **ExecNotificationQueryAsync** se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="db5d2-164">The call to **ExecNotificationQueryAsync** returns immediately.</span></span> <span data-ttu-id="db5d2-165">Los objetos y el estado solicitados se devuelven al autor de la llamada mediante devoluciones de llamada entregadas al receptor que se especifica en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="db5d2-165">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="db5d2-166">Para procesar cada objeto cuando se devuelve, cree un *objWbemSink*. Subrutina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="db5d2-166">To process each object when it is returned, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="db5d2-167">Después de que se devuelvan todos los objetos, realice el procesamiento final para implementar el *objWbemSink*. Evento [**Alcompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="db5d2-167">After all the objects are returned, perform the final processing to implement the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="db5d2-168">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="db5d2-168">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="db5d2-169">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="db5d2-169">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="db5d2-170">Para eliminar los riesgos, consulte [configuración de la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="db5d2-170">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="db5d2-171">Hay límites en el número de palabras clave **and** y **or** que se pueden usar en las consultas WQL.</span><span class="sxs-lookup"><span data-stu-id="db5d2-171">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="db5d2-172">Un gran número de palabras clave WQL usadas en una consulta compleja puede hacer que WMI devuelva el valor **HRESULT** de la cuota de la **\_ \_ cuota E \_ infracción** de Asan de WBEM.</span><span class="sxs-lookup"><span data-stu-id="db5d2-172">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code asan **HRESULT** value.</span></span> <span data-ttu-id="db5d2-173">El límite de palabras clave de WQL depende de la complejidad de la consulta.</span><span class="sxs-lookup"><span data-stu-id="db5d2-173">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="examples"></a><span data-ttu-id="db5d2-174">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="db5d2-174">Examples</span></span>

<span data-ttu-id="db5d2-175">En el ejemplo de código de VBScript siguiente se muestra un script que está esperando una notificación de eventos WMI que indica que un proceso ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="db5d2-175">The following VBScript code example shows a script that is waiting for a WMI event notification that indicates that a process has terminated.</span></span> <span data-ttu-id="db5d2-176">Está esperando un evento intrínseco de WMI, una instancia de la clase de evento [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md).</span><span class="sxs-lookup"><span data-stu-id="db5d2-176">It is waiting for a WMI intrinsic event, an instance of the event class [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md).</span></span> <span data-ttu-id="db5d2-177">**\_ \_ InstanceDeletionEvent** debe representar la eliminación de una instancia del [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="db5d2-177">The **\_\_InstanceDeletionEvent** must represent the deletion of an instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span> <span data-ttu-id="db5d2-178">Para obtener más información sobre los eventos intrínsecos de WMI, vea [determinar el tipo de evento que se va a recibir](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="db5d2-178">For more information about WMI intrinsic events, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="db5d2-179">El script siguiente se ejecuta indefinidamente hasta que se reinicia el equipo, se detiene WMI o se detiene el script.</span><span class="sxs-lookup"><span data-stu-id="db5d2-179">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="db5d2-180">Para detener el script manualmente, use el administrador de tareas para detener el proceso.</span><span class="sxs-lookup"><span data-stu-id="db5d2-180">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="db5d2-181">Para detenerlo mediante programación, use el método [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) en la clase de proceso de Win32 \_ .</span><span class="sxs-lookup"><span data-stu-id="db5d2-181">To stop it programmatically, use the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method in the Win32\_Process class.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & _strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, "SELECT * FROM __InstanceCreationEvent WITHIN 1 " _
                                               & "WHERE TargetInstance ISA 'Win32_Process'"

WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo "Event occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
```



## <a name="requirements"></a><span data-ttu-id="db5d2-182">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db5d2-182">Requirements</span></span>



| <span data-ttu-id="db5d2-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="db5d2-183">Requirement</span></span> | <span data-ttu-id="db5d2-184">Value</span><span class="sxs-lookup"><span data-stu-id="db5d2-184">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db5d2-185">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db5d2-185">Minimum supported client</span></span><br/> | <span data-ttu-id="db5d2-186">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db5d2-186">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="db5d2-187">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db5d2-187">Minimum supported server</span></span><br/> | <span data-ttu-id="db5d2-188">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db5d2-188">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="db5d2-189">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db5d2-189">Header</span></span><br/>                   | <dl> <span data-ttu-id="db5d2-190"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="db5d2-190"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="db5d2-191">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="db5d2-191">Type library</span></span><br/>             | <dl> <span data-ttu-id="db5d2-192"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="db5d2-192"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="db5d2-193">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="db5d2-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db5d2-194"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db5d2-194"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="db5d2-195">CLSID</span><span class="sxs-lookup"><span data-stu-id="db5d2-195">CLSID</span></span><br/>                    | <span data-ttu-id="db5d2-196">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="db5d2-196">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="db5d2-197">IID</span><span class="sxs-lookup"><span data-stu-id="db5d2-197">IID</span></span><br/>                      | <span data-ttu-id="db5d2-198">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="db5d2-198">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="db5d2-199">Vea también</span><span class="sxs-lookup"><span data-stu-id="db5d2-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db5d2-200">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="db5d2-200">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="db5d2-201">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="db5d2-201">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
</dt> <dt>

[<span data-ttu-id="db5d2-202">**SWbemServices.ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="db5d2-202">**SWbemServices.ExecQueryAsync**</span></span>](swbemservices-execqueryasync.md)
</dt> <dt>

[<span data-ttu-id="db5d2-203">Registrar eventos del registro del sistema</span><span class="sxs-lookup"><span data-stu-id="db5d2-203">Registering for System Registry Events</span></span>](registering-for-system-registry-events.md)
</dt> <dt>

[<span data-ttu-id="db5d2-204">Determinar el tipo de evento que se va a recibir</span><span class="sxs-lookup"><span data-stu-id="db5d2-204">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[<span data-ttu-id="db5d2-205">Llamar a un método</span><span class="sxs-lookup"><span data-stu-id="db5d2-205">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="db5d2-206">Establecer la seguridad en una llamada asincrónica</span><span class="sxs-lookup"><span data-stu-id="db5d2-206">Setting Security on an Asynchronous Call</span></span>](setting-security-on-an-asynchronous-call.md)
</dt> </dl>

 

