---
description: Devuelve todas las instancias o clases de asociación que hacen referencia a una clase o instancia de origen específica.
ms.assetid: 2ad66ea1-b8f0-4b6b-b68f-29496afbe4bf
ms.tgt_platform: multiple
title: Método SWbemServices. ReferencesToAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ReferencesToAsync
- ISWbemServices.ReferencesToAsync
- ISWbemServices.ReferencesToAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 64a8b9b336a1e7aa6007b17d2e878f1ace5e6163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715717"
---
# <a name="swbemservicesreferencestoasync-method"></a><span data-ttu-id="55092-103">SWbemServices. ReferencesToAsync, método</span><span class="sxs-lookup"><span data-stu-id="55092-103">SWbemServices.ReferencesToAsync method</span></span>

<span data-ttu-id="55092-104">El método **ReferencesToAsync** del objeto [**SWbemServices**](swbemservices.md) devuelve todas las instancias o clases de asociación que hacen referencia a una instancia o clase de origen específica.</span><span class="sxs-lookup"><span data-stu-id="55092-104">The **ReferencesToAsync** method of the [**SWbemServices**](swbemservices.md) object returns all association classes or instances that refer to a specific source class or instance.</span></span> <span data-ttu-id="55092-105">Este método realiza la misma función que realizan las [referencias de](references-of-statement.md) la consulta WQL.</span><span class="sxs-lookup"><span data-stu-id="55092-105">This method performs the same function that the [REFERENCES OF](references-of-statement.md) WQL query performs.</span></span>

<span data-ttu-id="55092-106">Para obtener más información sobre el modo asincrónico, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="55092-106">For more information about the asynchronous mode, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="55092-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="55092-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="55092-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55092-108">Syntax</span></span>


```VB
SWbemServices.ReferencesToAsync( _
  ByVal ObjWbemSink, _
  ByVal strObjectPath, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="55092-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55092-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55092-110">*ObjWbemSink*</span><span class="sxs-lookup"><span data-stu-id="55092-110">*ObjWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="55092-111">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="55092-111">Required.</span></span> <span data-ttu-id="55092-112">Receptor de objeto que recibe los objetos de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="55092-112">Object sink that receives the objects asynchronously.</span></span> <span data-ttu-id="55092-113">Cree un objeto [**SWbemSink**](swbemsink.md) para recibir los objetos.</span><span class="sxs-lookup"><span data-stu-id="55092-113">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="55092-114">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="55092-114">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="55092-115">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="55092-115">Required.</span></span> <span data-ttu-id="55092-116">Cadena que contiene la ruta de acceso del objeto de origen para este método.</span><span class="sxs-lookup"><span data-stu-id="55092-116">String that contains the object path of the source for this method.</span></span> <span data-ttu-id="55092-117">Para obtener más información, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="55092-117">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> <dt>

<span data-ttu-id="55092-118">*strResultClass* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="55092-118">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="55092-119">Cadena que contiene un nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="55092-119">String that contains a class name.</span></span> <span data-ttu-id="55092-120">Si se especifica, este parámetro indica que los objetos de asociación devueltos deben pertenecer a la clase especificada en este parámetro o derivarse de ella.</span><span class="sxs-lookup"><span data-stu-id="55092-120">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class that is specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="55092-121">*strRole* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="55092-121">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="55092-122">Cadena que contiene un nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="55092-122">String that contains a property name.</span></span> <span data-ttu-id="55092-123">Si se especifica, este parámetro indica que los objetos de asociación devueltos se deben limitar a aquellos en los que el objeto de origen desempeña un rol específico.</span><span class="sxs-lookup"><span data-stu-id="55092-123">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="55092-124">El rol se define mediante el nombre de una propiedad de referencia especificada de una asociación.</span><span class="sxs-lookup"><span data-stu-id="55092-124">The role is defined by the name of a specified reference property of an association.</span></span>

</dd> <dt>

<span data-ttu-id="55092-125">*bClassesOnly* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="55092-125">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="55092-126">Valor booleano que indica si se debe devolver o no una lista de nombres de clase en lugar de instancias reales de las clases.</span><span class="sxs-lookup"><span data-stu-id="55092-126">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="55092-127">Estas son las clases a las que pertenecen los objetos de asociación.</span><span class="sxs-lookup"><span data-stu-id="55092-127">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="55092-128">El valor predeterminado de este parámetro es **false**.</span><span class="sxs-lookup"><span data-stu-id="55092-128">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="55092-129">*bSchemaOnly* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="55092-129">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="55092-130">Valor booleano que indica si la consulta se aplica o no al esquema en lugar de a los datos.</span><span class="sxs-lookup"><span data-stu-id="55092-130">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="55092-131">El valor predeterminado de este parámetro es **false**.</span><span class="sxs-lookup"><span data-stu-id="55092-131">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="55092-132">Solo se puede establecer en **true** si el parámetro *strObjectPath* especifica la ruta de acceso del objeto de una clase.</span><span class="sxs-lookup"><span data-stu-id="55092-132">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="55092-133">Cuando se establece en **true**, el conjunto de extremos devueltos representa las clases que están asociadas a la clase de origen en el esquema.</span><span class="sxs-lookup"><span data-stu-id="55092-133">When set to **TRUE**, the set of returned endpoints represents classes that are associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="55092-134">*strRequiredQualifier* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="55092-134">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="55092-135">Cadena que contiene un nombre de calificador.</span><span class="sxs-lookup"><span data-stu-id="55092-135">String that contains a qualifier name.</span></span> <span data-ttu-id="55092-136">Si se especifica, este parámetro indica que los objetos de asociación devueltos deben incluir el calificador especificado.</span><span class="sxs-lookup"><span data-stu-id="55092-136">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="55092-137">*iFlags* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="55092-137">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="55092-138">Entero que especifica las marcas adicionales para la operación.</span><span class="sxs-lookup"><span data-stu-id="55092-138">Integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="55092-139">El valor predeterminado para este parámetro es **wbemFlagBidirectional**.</span><span class="sxs-lookup"><span data-stu-id="55092-139">The default for this parameter is **wbemFlagBidirectional**.</span></span> <span data-ttu-id="55092-140">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="55092-140">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="55092-141"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="55092-141"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="55092-142">Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="55092-142">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="55092-143"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="55092-143"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="55092-144">Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="55092-144">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="55092-145"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="55092-145"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="55092-146">Hace que Instrumental de administración de Windows (WMI) devuelva datos de modificación de clase junto con la definición de clase base.</span><span class="sxs-lookup"><span data-stu-id="55092-146">Causes Windows Management Instrumentation (WMI) to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="55092-147">Para obtener más información, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="55092-147">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="55092-148">*objWbemNamedValueSet* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="55092-148">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="55092-149">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="55092-149">Typically, this is undefined.</span></span> <span data-ttu-id="55092-150">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="55092-150">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="55092-151">Un proveedor que admite o requiere información de contexto debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="55092-151">A provider that supports or requires context information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="55092-152">*objWbemAsyncContext* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="55092-152">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="55092-153">Se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que devuelve al receptor del objeto para identificar el origen de la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="55092-153">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="55092-154">Use este parámetro para realizar varias llamadas asincrónicas mediante el mismo receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="55092-154">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="55092-155">Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando.</span><span class="sxs-lookup"><span data-stu-id="55092-155">To use this parameter, create an **SWbemNamedValueSet** object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="55092-156">Este objeto **SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="55092-156">This **SWbemNamedValueSet** object is returned to the object sink, and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="55092-157">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="55092-157">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55092-158">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55092-158">Return value</span></span>

<span data-ttu-id="55092-159">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="55092-159">This method does not return a value.</span></span> <span data-ttu-id="55092-160">Si se realiza correctamente, el receptor recibe un evento [**OnObjectReady**](swbemsink-onobjectready.md) por cada instancia.</span><span class="sxs-lookup"><span data-stu-id="55092-160">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="55092-161">Después de la última instancia, el receptor del objeto recibe un evento [**alcompleto**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="55092-161">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="55092-162">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="55092-162">Error codes</span></span>

<span data-ttu-id="55092-163">Después de completar el método **ReferencesToAsync** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="55092-163">After the completion of the **ReferencesToAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="55092-164">Una colección devuelta con cero elementos no es un error.</span><span class="sxs-lookup"><span data-stu-id="55092-164">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="55092-165">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="55092-165">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="55092-166">El usuario actual no tiene permiso para ver una o varias de las clases devueltas por la llamada.</span><span class="sxs-lookup"><span data-stu-id="55092-166">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="55092-167">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="55092-167">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="55092-168">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="55092-168">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="55092-169">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="55092-169">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="55092-170">Se especificó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="55092-170">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="55092-171">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="55092-171">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="55092-172">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="55092-172">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55092-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55092-173">Remarks</span></span>

<span data-ttu-id="55092-174">Esta llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="55092-174">This call returns immediately.</span></span> <span data-ttu-id="55092-175">Los objetos y el estado solicitados se devuelven al autor de la llamada mediante devoluciones de llamada entregadas al receptor que se especifica en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="55092-175">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="55092-176">Para procesar cada objeto cuando vuelva, cree un *objWbemSink*. Subrutina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="55092-176">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="55092-177">Después de que se devuelvan todos los objetos, puede realizar el procesamiento final en la implementación de *objWbemSink*. Evento [**Alcompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="55092-177">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="55092-178">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="55092-178">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="55092-179">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="55092-179">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="55092-180">Para eliminar los riesgos, consulte [configuración de la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="55092-180">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55092-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55092-181">Requirements</span></span>



| <span data-ttu-id="55092-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="55092-182">Requirement</span></span> | <span data-ttu-id="55092-183">Value</span><span class="sxs-lookup"><span data-stu-id="55092-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55092-184">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55092-184">Minimum supported client</span></span><br/> | <span data-ttu-id="55092-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55092-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="55092-186">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55092-186">Minimum supported server</span></span><br/> | <span data-ttu-id="55092-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55092-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="55092-188">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55092-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="55092-189"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="55092-189"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="55092-190">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="55092-190">Type library</span></span><br/>             | <dl> <span data-ttu-id="55092-191"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="55092-191"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="55092-192">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="55092-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55092-193"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55092-193"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="55092-194">CLSID</span><span class="sxs-lookup"><span data-stu-id="55092-194">CLSID</span></span><br/>                    | <span data-ttu-id="55092-195">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="55092-195">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="55092-196">IID</span><span class="sxs-lookup"><span data-stu-id="55092-196">IID</span></span><br/>                      | <span data-ttu-id="55092-197">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="55092-197">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="55092-198">Vea también</span><span class="sxs-lookup"><span data-stu-id="55092-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55092-199">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="55092-199">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="55092-200">**SWbemObject. ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="55092-200">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="55092-201">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="55092-201">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="55092-202">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="55092-202">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

