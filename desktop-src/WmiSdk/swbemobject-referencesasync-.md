---
description: El \_ método ReferencesAsync de SWbemObject proporciona una colección de todas las instancias o clases de asociación que hacen referencia al objeto actual. Este método realiza la misma función que realizan las referencias WQL de la consulta.
ms.assetid: 44989726-3f68-453b-b9f5-e76fb0fbb152
ms.tgt_platform: multiple
title: Método SWbemObject.ReferencesAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ReferencesAsync_
- ISWbemObject.ReferencesAsync_
- ISWbemObject.ReferencesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: aa4b85475a0dc9f736254c8f207469a52897b7ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687238"
---
# <a name="swbemobjectreferencesasync_-method"></a><span data-ttu-id="8c4f9-104">SWbemObject. ReferencesAsync, \_ método</span><span class="sxs-lookup"><span data-stu-id="8c4f9-104">SWbemObject.ReferencesAsync\_ method</span></span>

<span data-ttu-id="8c4f9-105">El **método \_ ReferencesAsync** de [**SWbemObject**](swbemobject.md) proporciona una colección de todas las instancias o clases de asociación que hacen referencia al objeto actual.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-105">The **ReferencesAsync\_** method of [**SWbemObject**](swbemobject.md) supplies a collection of all association classes or instances that refer to the current object.</span></span> <span data-ttu-id="8c4f9-106">Este método realiza la misma función que realizan las [referencias WQL de](references-of-statement.md) la consulta.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-106">This method performs the same function that the WQL [REFERENCES OF](references-of-statement.md) query performs.</span></span>

<span data-ttu-id="8c4f9-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8c4f9-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8c4f9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c4f9-108">Syntax</span></span>


```VB
SWbemObject.ReferencesAsync_( _
  ByVal objWbemSink, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="8c4f9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c4f9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c4f9-110">*objWbemSink* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c4f9-110">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c4f9-111">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-111">Required.</span></span> <span data-ttu-id="8c4f9-112">Receptor de objeto que recibe los objetos de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-112">Object sink that receives the objects asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="8c4f9-113">*strResultClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8c4f9-113">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8c4f9-114">Cadena que contiene un nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-114">String that contains a class name.</span></span> <span data-ttu-id="8c4f9-115">Si se especifica, este parámetro indica que los objetos de asociación devueltos deben pertenecer a la clase especificada en este parámetro o derivarse de ella.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-115">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8c4f9-116">*strRole* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8c4f9-116">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8c4f9-117">Cadena que contiene un nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-117">String that contains a property name.</span></span> <span data-ttu-id="8c4f9-118">Si se especifica, este parámetro indica que los objetos de asociación devueltos se deben limitar a aquellos en los que el objeto de origen desempeña un rol específico.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-118">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="8c4f9-119">El nombre de una propiedad de referencia especificada define el rol de una asociación.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-119">The name of a specified reference property defines the role of an association.</span></span>

</dd> <dt>

<span data-ttu-id="8c4f9-120">*bClassesOnly* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8c4f9-120">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8c4f9-121">Valor booleano que indica si se debe devolver o no una lista de nombres de clase en lugar de instancias reales de las clases.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-121">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="8c4f9-122">Estas son las clases a las que pertenecen los objetos de asociación.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-122">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="8c4f9-123">El valor predeterminado de este parámetro es **false**.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-123">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="8c4f9-124">*bSchemaOnly* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8c4f9-124">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8c4f9-125">Valor booleano que indica si la consulta se aplica o no al esquema en lugar de a los datos.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-125">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="8c4f9-126">El valor predeterminado de este parámetro es **false**.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-126">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="8c4f9-127">Solo se puede establecer en **true** si el objeto en el que se invoca este método es una clase.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-127">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="8c4f9-128">Cuando se establece en **true**, el conjunto de extremos devueltos representa las clases que están asociadas adecuadamente a la clase de origen en el esquema.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-128">When set to **TRUE**, the set of returned endpoints represents classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="8c4f9-129">*strRequiredQualifier* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8c4f9-129">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8c4f9-130">Cadena que contiene un nombre de calificador.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-130">String that contains a qualifier name.</span></span> <span data-ttu-id="8c4f9-131">Si se especifica, este parámetro indica que los objetos de asociación devueltos deben incluir el calificador especificado.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-131">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="8c4f9-132">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8c4f9-132">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8c4f9-133">Entero que especifica marcas adicionales para la operación.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-133">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="8c4f9-134">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-134">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="8c4f9-135"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="8c4f9-135"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="8c4f9-136">Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**SWbemSink. OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-136">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="8c4f9-137"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="8c4f9-137"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="8c4f9-138">Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-138">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="8c4f9-139"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="8c4f9-139"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="8c4f9-140">Hace que Instrumental de administración de Windows (WMI) devuelva datos de modificación de clase con la definición de clase base.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-140">Causes Windows Management Instrumentation (WMI) to return class amendment data with the base class definition.</span></span> <span data-ttu-id="8c4f9-141">Para obtener más información, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="8c4f9-141">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8c4f9-142">*objwbemNamedValueSet* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8c4f9-142">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8c4f9-143">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-143">Typically, this is undefined.</span></span> <span data-ttu-id="8c4f9-144">De lo contrario, se trata de un objeto [SWbemNamedValueSet](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-144">Otherwise, this is an [SWbemNamedValueSet](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="8c4f9-145">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-145">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="8c4f9-146">*objWbemAsyncContext* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8c4f9-146">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8c4f9-147">Se trata de un objeto [SWbemNamedValueSet](swbemnamedvalueset.md) que devuelve al receptor del objeto para identificar el origen de la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-147">This is an [SWbemNamedValueSet](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="8c4f9-148">Utilice este parámetro si va a realizar varias llamadas asincrónicas mediante el mismo receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-148">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="8c4f9-149">Para usar este parámetro, cree un objeto SWbemNamedValueSet y use el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-149">To use this parameter, create an SWbemNamedValueSet object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="8c4f9-150">Este objeto SWbemNamedValueSet se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="8c4f9-150">This SWbemNamedValueSet object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="8c4f9-151">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="8c4f9-151">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c4f9-152">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c4f9-152">Return value</span></span>

<span data-ttu-id="8c4f9-153">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-153">This method does not return a value.</span></span> <span data-ttu-id="8c4f9-154">Si se realiza correctamente, el receptor recibe un evento [**OnObjectReady**](swbemsink-onobjectready.md) por cada instancia.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-154">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="8c4f9-155">Después de la última instancia, el receptor del objeto recibe un evento [**alcompleto**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="8c4f9-155">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8c4f9-156">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="8c4f9-156">Error codes</span></span>

<span data-ttu-id="8c4f9-157">Después de completar el método **ReferencesAsync \_** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-157">After the completion of the **ReferencesAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="8c4f9-158">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="8c4f9-158">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="8c4f9-159">El usuario actual no tiene permiso para ver una o varias de las clases devueltas por la llamada.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-159">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="8c4f9-160">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="8c4f9-160">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="8c4f9-161">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-161">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="8c4f9-162">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="8c4f9-162">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="8c4f9-163">Se especificó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-163">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="8c4f9-164">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="8c4f9-164">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="8c4f9-165">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-165">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c4f9-166">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c4f9-166">Remarks</span></span>

<span data-ttu-id="8c4f9-167">Esta llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-167">This call returns immediately.</span></span> <span data-ttu-id="8c4f9-168">Los objetos y el estado solicitados se devuelven al autor de la llamada mediante devoluciones de llamada entregadas al receptor que se especifica en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-168">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="8c4f9-169">Para procesar cada objeto cuando llegue, cree un *objWbemSink*. Subrutina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="8c4f9-169">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="8c4f9-170">Después de que se devuelvan todos los objetos, puede realizar el procesamiento final en la implementación de *objWbemSink*. Evento [**Alcompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="8c4f9-170">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="8c4f9-171">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-171">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="8c4f9-172">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-172">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="8c4f9-173">Para eliminar los riesgos, utilice la comunicación semisincrónica o la comunicación sincrónica.</span><span class="sxs-lookup"><span data-stu-id="8c4f9-173">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="8c4f9-174">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="8c4f9-174">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="8c4f9-175">Para obtener más información sobre las referencias de la consulta WQL asociada, las instancias de origen y los objetos de asociación, vea [ASSOCIATORS OF Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="8c4f9-175">For more information about the REFERENCES OF associated WQL query, source instances, and association objects, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c4f9-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c4f9-176">Requirements</span></span>



| <span data-ttu-id="8c4f9-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c4f9-177">Requirement</span></span> | <span data-ttu-id="8c4f9-178">Value</span><span class="sxs-lookup"><span data-stu-id="8c4f9-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c4f9-179">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c4f9-179">Minimum supported client</span></span><br/> | <span data-ttu-id="8c4f9-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c4f9-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8c4f9-181">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c4f9-181">Minimum supported server</span></span><br/> | <span data-ttu-id="8c4f9-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c4f9-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8c4f9-183">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c4f9-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c4f9-184"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c4f9-184"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8c4f9-185">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8c4f9-185">Type library</span></span><br/>             | <dl> <span data-ttu-id="8c4f9-186"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8c4f9-186"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8c4f9-187">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8c4f9-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c4f9-188"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c4f9-188"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8c4f9-189">CLSID</span><span class="sxs-lookup"><span data-stu-id="8c4f9-189">CLSID</span></span><br/>                    | <span data-ttu-id="8c4f9-190">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="8c4f9-190">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="8c4f9-191">IID</span><span class="sxs-lookup"><span data-stu-id="8c4f9-191">IID</span></span><br/>                      | <span data-ttu-id="8c4f9-192">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="8c4f9-192">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="8c4f9-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c4f9-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c4f9-194">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="8c4f9-194">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="8c4f9-195">**SWbemObject. ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="8c4f9-195">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="8c4f9-196">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="8c4f9-196">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> <dt>

[<span data-ttu-id="8c4f9-197">**SWbemServices. References**</span><span class="sxs-lookup"><span data-stu-id="8c4f9-197">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> <dt>

[<span data-ttu-id="8c4f9-198">**SWbemServices. ReferencesToAsync**</span><span class="sxs-lookup"><span data-stu-id="8c4f9-198">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)
</dt> </dl>

 

