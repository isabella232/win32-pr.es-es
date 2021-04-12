---
description: Ejecuta una consulta para recuperar objetos.
ms.assetid: 50c7f62b-dd83-4117-b10e-acee1690ce8c
ms.tgt_platform: multiple
title: SWbemServices.Exemétodo cQueryAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQueryAsync
- ISWbemServices.ExecQueryAsync
- ISWbemServices.ExecQueryAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5564e53ef3ea185235e93bbbeb8e2a5fa001d67b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360539"
---
# <a name="swbemservicesexecqueryasync-method"></a><span data-ttu-id="7934e-103">SWbemServices.Exemétodo cQueryAsync</span><span class="sxs-lookup"><span data-stu-id="7934e-103">SWbemServices.ExecQueryAsync method</span></span>

<span data-ttu-id="7934e-104">El método **ExecQueryAsync** del objeto [**SWbemServices**](swbemservices.md) ejecuta una consulta para recuperar objetos.</span><span class="sxs-lookup"><span data-stu-id="7934e-104">The **ExecQueryAsync** method of the [**SWbemServices**](swbemservices.md) object executes a query to retrieve objects.</span></span> <span data-ttu-id="7934e-105">La llamada a este método se devuelve inmediatamente, y los resultados y el estado se devuelven al autor de la llamada a través de los eventos entregados al receptor que se especifica en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="7934e-105">The call to this method returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="7934e-106">Para controlar cada objeto devuelto, cree un *objWbemSink*. Subrutina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="7934e-106">To handle each returned object, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span>

<span data-ttu-id="7934e-107">Se llama al método en el modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="7934e-107">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="7934e-108">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="7934e-108">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="7934e-109">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7934e-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7934e-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7934e-110">Syntax</span></span>


```VB
objWbemObjectSet = .ExecQueryAsync( _
  [ ByVal objWbemSink ], _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7934e-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7934e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7934e-112">*objWbemSink* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="7934e-112">*objWbemSink* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7934e-113">Receptor de objeto que ejecuta la consulta de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="7934e-113">Object sink that executes the query asynchronously.</span></span> <span data-ttu-id="7934e-114">Cree un objeto [**SWbemSink**](swbemsink.md) para recibir los objetos.</span><span class="sxs-lookup"><span data-stu-id="7934e-114">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="7934e-115">*strQuery*</span><span class="sxs-lookup"><span data-stu-id="7934e-115">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="7934e-116">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7934e-116">Required.</span></span> <span data-ttu-id="7934e-117">Cadena que contiene el texto de la consulta.</span><span class="sxs-lookup"><span data-stu-id="7934e-117">String that contains the text of the query.</span></span> <span data-ttu-id="7934e-118">Este parámetro no puede estar en blanco.</span><span class="sxs-lookup"><span data-stu-id="7934e-118">This parameter cannot be blank.</span></span> <span data-ttu-id="7934e-119">Para obtener más información sobre la creación de cadenas de consulta de WMI, vea [consultas con WQL](querying-with-wql.md) y la referencia de [WQL](wql-sql-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="7934e-119">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="7934e-120">*strQueryLanguage* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="7934e-120">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7934e-121">Cadena que contiene el lenguaje de consulta que se va a utilizar.</span><span class="sxs-lookup"><span data-stu-id="7934e-121">String that contains the query language to be used.</span></span> <span data-ttu-id="7934e-122">Si se especifica, el valor debe ser "WQL".</span><span class="sxs-lookup"><span data-stu-id="7934e-122">If specified, the value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="7934e-123">*iFlags* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="7934e-123">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7934e-124">Entero que determina el comportamiento de la consulta.</span><span class="sxs-lookup"><span data-stu-id="7934e-124">Integer that determines the behavior of the query.</span></span> <span data-ttu-id="7934e-125">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="7934e-125">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="7934e-126"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="7934e-126"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="7934e-127">Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="7934e-127">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="7934e-128"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="7934e-128"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="7934e-129">Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="7934e-129">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span data-ttu-id="7934e-130"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemQueryFlagPrototype \* \* \* \* (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="7934e-130"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>\*\*\*\*wbemQueryFlagPrototype\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="7934e-131">Se utiliza para un prototipo.</span><span class="sxs-lookup"><span data-stu-id="7934e-131">Used for a prototype.</span></span> <span data-ttu-id="7934e-132">Detiene la consulta y, en su lugar, devuelve un objeto similar a un objeto de resultado típico.</span><span class="sxs-lookup"><span data-stu-id="7934e-132">It stops the query from happening and instead, returns an object that looks like a typical result object.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="7934e-133"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="7934e-133"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="7934e-134">Hace que WMI devuelva datos de modificación de clase con la definición de clase base.</span><span class="sxs-lookup"><span data-stu-id="7934e-134">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="7934e-135">Para obtener más información, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="7934e-135">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7934e-136">*objwbemNamedValueSet* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="7934e-136">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7934e-137">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="7934e-137">Typically, this is undefined.</span></span> <span data-ttu-id="7934e-138">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que presta servicio a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7934e-138">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="7934e-139">Un proveedor que admite o requiere información de contexto debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="7934e-139">A provider that supports or requires context information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="7934e-140">*objWbemAsyncContext* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="7934e-140">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7934e-141">Un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que devuelve al receptor del objeto para identificar el origen de la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="7934e-141">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="7934e-142">Use este parámetro para realizar varias llamadas asincrónicas mediante el mismo receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="7934e-142">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="7934e-143">Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando.</span><span class="sxs-lookup"><span data-stu-id="7934e-143">To use this parameter, create an **SWbemNamedValueSet** object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="7934e-144">Este objeto **SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="7934e-144">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="7934e-145">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="7934e-145">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7934e-146">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7934e-146">Return value</span></span>

<span data-ttu-id="7934e-147">Este método no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="7934e-147">This method has no return values.</span></span> <span data-ttu-id="7934e-148">Si se realiza correctamente, el receptor recibe un evento [**OnObjectReady**](swbemsink-onobjectready.md) por cada instancia.</span><span class="sxs-lookup"><span data-stu-id="7934e-148">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="7934e-149">Después de la última instancia, el receptor del objeto recibe un evento [**alcompleto**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="7934e-149">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7934e-150">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="7934e-150">Error codes</span></span>

<span data-ttu-id="7934e-151">Después de completar el método **ExecQueryAsync** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="7934e-151">After the completion of the **ExecQueryAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object can contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="7934e-152">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="7934e-152">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="7934e-153">El usuario actual no tiene permiso para ver el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="7934e-153">Current user does not have the permission to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="7934e-154">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="7934e-154">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="7934e-155">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="7934e-155">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="7934e-156">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="7934e-156">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="7934e-157">Se especificó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="7934e-157">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="7934e-158">**wbemErrInvalidQuery** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="7934e-158">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="7934e-159">La sintaxis de la consulta no es válida.</span><span class="sxs-lookup"><span data-stu-id="7934e-159">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="7934e-160">**wbemErrInvalidQueryType** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="7934e-160">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="7934e-161">No se admite el lenguaje de consulta solicitado.</span><span class="sxs-lookup"><span data-stu-id="7934e-161">Requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="7934e-162">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="7934e-162">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="7934e-163">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="7934e-163">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7934e-164">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7934e-164">Remarks</span></span>

<span data-ttu-id="7934e-165">Esta llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="7934e-165">This call returns immediately.</span></span> <span data-ttu-id="7934e-166">Los objetos y el estado solicitados se devuelven al autor de la llamada mediante devoluciones de llamada entregadas al receptor que se especifica en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="7934e-166">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="7934e-167">Para procesar cada objeto cuando vuelva, cree un *objWbemSink*. Subrutina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="7934e-167">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="7934e-168">Después de que se devuelvan todos los objetos, realice el procesamiento final en la implementación de *objWbemSink*. Evento [**Alcompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="7934e-168">After all the objects are returned, perform the final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="7934e-169">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="7934e-169">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="7934e-170">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="7934e-170">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="7934e-171">Para eliminar los riesgos, consulte [configuración de la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md) .</span><span class="sxs-lookup"><span data-stu-id="7934e-171">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md)</span></span>

<span data-ttu-id="7934e-172">El método **ExecQueryAsync** devuelve un conjunto de resultados vacío cuando no hay objetos que coincidan con los criterios de la consulta.</span><span class="sxs-lookup"><span data-stu-id="7934e-172">The **ExecQueryAsync** method returns an empty result set when there are no objects to match the criteria in the query.</span></span> <span data-ttu-id="7934e-173">Este método devuelve las propiedades clave tanto si se solicita la propiedad de [**clave**](standard-qualifiers.md) como si no en el parámetro *strQuery* .</span><span class="sxs-lookup"><span data-stu-id="7934e-173">This method returns key properties whether or not the [**Key**](standard-qualifiers.md) property is requested in the *strQuery* parameter.</span></span>

<span data-ttu-id="7934e-174">Hay límites en el número de palabras clave **and** y **or** que se pueden usar en las consultas WQL.</span><span class="sxs-lookup"><span data-stu-id="7934e-174">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="7934e-175">Un gran número de palabras clave WQL usadas en una consulta compleja puede hacer que WMI devuelva el código de error de infracción de la cuota de WBEM \_ E \_ \_ como un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7934e-175">Large numbers of WQL keywords used in a complex query can cause WMI to return the WBEM\_E\_QUOTA\_VIOLATION error code as an **HRESULT** value.</span></span> <span data-ttu-id="7934e-176">El límite de palabras clave de WQL depende de la complejidad de la consulta.</span><span class="sxs-lookup"><span data-stu-id="7934e-176">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="requirements"></a><span data-ttu-id="7934e-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7934e-177">Requirements</span></span>



| <span data-ttu-id="7934e-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="7934e-178">Requirement</span></span> | <span data-ttu-id="7934e-179">Value</span><span class="sxs-lookup"><span data-stu-id="7934e-179">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7934e-180">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7934e-180">Minimum supported client</span></span><br/> | <span data-ttu-id="7934e-181">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7934e-181">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7934e-182">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7934e-182">Minimum supported server</span></span><br/> | <span data-ttu-id="7934e-183">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7934e-183">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7934e-184">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7934e-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="7934e-185"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7934e-185"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7934e-186">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7934e-186">Type library</span></span><br/>             | <dl> <span data-ttu-id="7934e-187"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7934e-187"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7934e-188">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7934e-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7934e-189"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7934e-189"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7934e-190">CLSID</span><span class="sxs-lookup"><span data-stu-id="7934e-190">CLSID</span></span><br/>                    | <span data-ttu-id="7934e-191">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="7934e-191">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="7934e-192">IID</span><span class="sxs-lookup"><span data-stu-id="7934e-192">IID</span></span><br/>                      | <span data-ttu-id="7934e-193">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="7934e-193">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="7934e-194">Vea también</span><span class="sxs-lookup"><span data-stu-id="7934e-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7934e-195">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="7934e-195">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="7934e-196">Llamar a un método</span><span class="sxs-lookup"><span data-stu-id="7934e-196">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="7934e-197">**SWbemServices. get**</span><span class="sxs-lookup"><span data-stu-id="7934e-197">**SWbemServices.Get**</span></span>](swbemservices-get.md)
</dt> </dl>

 

